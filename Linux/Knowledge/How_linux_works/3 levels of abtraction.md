
## 1. Trừu tượng hóa và các tầng (abstraction & layers)

Một hệ điều hành như Linux rất phức tạp, nên cách dễ hiểu nhất là nhìn nó qua **trừu tượng hóa**: bỏ qua chi tiết bên trong một thành phần, chỉ quan tâm nó làm gì. Giống như lái xe, ta không cần biết từng con ốc trong động cơ, chỉ cần biết xe chạy được.

Các thành phần của Linux được xếp thành ba tầng chính, tầng trên dựa vào tầng dưới:

```
+---------------------------------------------------+
|  User processes (user space)                      |
|  Giao diện đồ họa, server, shell, ứng dụng...     |
+---------------------------------------------------+
|  Linux kernel                                     |
|  Quản lý process, bộ nhớ, driver, system call     |
+---------------------------------------------------+
|  Hardware                                         |
|  CPU, RAM, ổ đĩa, card mạng...                    |
+---------------------------------------------------+
```

**Kernel mode và user mode.** Kernel chạy ở _kernel mode_, có toàn quyền truy cập CPU và bộ nhớ. Vùng nhớ chỉ kernel được truy cập gọi là _kernel space_. Các process thông thường chạy ở _user mode_, chỉ được dùng một phần bộ nhớ và các thao tác an toàn; vùng nhớ đó gọi là _user space_. Nhờ vậy, một process bị lỗi thường chỉ hỏng chính nó, còn lỗi trong kernel có thể làm sập cả hệ thống.

## 2. Phần cứng: bộ nhớ chính (main memory)

Bộ nhớ chính (RAM) có thể xem là một vùng khổng lồ các bit 0 và 1. Mọi thứ đang chạy đều nằm trong đó: **kernel, code của các process và dữ liệu của chúng**. Thiết bị ngoại vi và dữ liệu vào/ra cũng đều đi qua RAM.

CPU là nơi **thực thi lệnh**: đọc instruction từ RAM, xử lý, rồi ghi kết quả trở lại RAM. Sách dùng khái niệm **state (trạng thái)**: tại một thời điểm, cách sắp xếp các bit trong bộ nhớ chính là trạng thái của hệ thống. Vì trạng thái gồm quá nhiều bit, ta thường mô tả nó ở mức trừu tượng hơn, ví dụ "process đang chờ input". Ảnh chụp trạng thái tại một thời điểm gọi là _image_.

## 3. Kernel

Kernel chủ yếu quản lý tài nguyên phần cứng, đặc biệt là RAM, và làm trung gian giữa phần cứng với process. Kernel đảm nhiệm bốn mảng chính.

### 3.1. Quản lý process

Gồm việc khởi động, tạm dừng, tiếp tục, lập lịch và kết thúc process. Sách không đưa ra định nghĩa chính thức, nhưng có thể hiểu process là **một chương trình đang chạy**, gồm vùng nhớ riêng và trạng thái thực thi.

Trên một lõi CPU, tại mỗi thời điểm chỉ có **một** thứ chạy (một process hoặc kernel). Cảm giác nhiều chương trình chạy cùng lúc đến từ việc kernel liên tục chuyển CPU giữa các process sau mỗi khoảng thời gian rất ngắn (_time slice_). Việc chuyển này gọi là **context switch**, diễn ra như sau:

1. CPU (nhờ timer bên trong) ngắt process đang chạy, chuyển sang kernel mode và trao quyền cho kernel.
2. Kernel ghi lại trạng thái hiện tại của CPU và bộ nhớ để sau này process có thể chạy tiếp.
3. Kernel xử lý các việc phát sinh trong time slice vừa rồi, ví dụ thu thập dữ liệu từ I/O.
4. Kernel chọn process tiếp theo, chuẩn bị bộ nhớ và CPU cho nó.
5. Kernel báo cho CPU độ dài time slice mới.
6. Kernel chuyển CPU về user mode và trao quyền cho process mới.

Điểm quan trọng: **kernel cũng phải dùng CPU để chạy**. Nó giành lại CPU vào giữa các time slice nhờ interrupt. Process không chủ động "xin" CPU; kernel quyết định ai được chạy. Trên máy nhiều lõi, nhiều process có thể chạy song song thật sự, nhưng kernel vẫn dùng cơ chế tương tự trên từng lõi.

### 3.2. Quản lý bộ nhớ

Kernel phải đảm bảo:

- Kernel có vùng nhớ riêng mà process không đụng vào được.
- Mỗi process có vùng nhớ riêng, process này không được đọc/ghi vùng nhớ của process khác.
- Process có thể chia sẻ bộ nhớ khi cần, và một số vùng có thể là chỉ đọc.
- Hệ thống có thể dùng nhiều bộ nhớ hơn RAM thực có, bằng cách dùng ổ đĩa làm bộ nhớ phụ (swap).

CPU hiện đại hỗ trợ việc này bằng **MMU (memory management unit)** và cơ chế **virtual memory**. Process không truy cập trực tiếp địa chỉ vật lý; nó dùng địa chỉ ảo, MMU dịch sang địa chỉ thật dựa trên bảng ánh xạ (_page table_) do kernel quản lý. Khi context switch, kernel thay bảng ánh xạ cho process tiếp theo.

### 3.3. Driver và quản lý thiết bị

Thiết bị phần cứng thường chỉ truy cập được ở kernel mode, vì thao tác sai có thể làm hỏng hệ thống. Mỗi loại thiết bị lại có cách điều khiển khác nhau, nên **device driver** nằm trong kernel để làm việc trực tiếp với thiết bị và cung cấp một giao diện thống nhất cho process sử dụng.

### 3.4. System call và hỗ trợ

**System call (syscall)** là cách process yêu cầu kernel làm những việc nó không có quyền hoặc không thể tự làm, như mở, đọc, ghi file. Khi gọi syscall, CPU chuyển sang chạy code kernel rồi trả kết quả về cho process.

Hai system call quan trọng nhất để hiểu cách process ra đời:

- **fork()**: kernel tạo một bản sao gần như y hệt của process đang gọi.
- **exec(program)**: kernel nạp chương trình `program` từ đĩa vào, thay thế process hiện tại.

Mọi process mới (trừ `init`, process đầu tiên) đều được tạo bằng `fork()`, và thường sau đó gọi `exec()` để chạy chương trình khác. Ví dụ khi bạn gõ `ls` trong shell: shell gọi `fork()` tạo bản sao của nó, rồi bản sao đó gọi `exec(ls)` để trở thành `ls`.

Kernel cũng hỗ trợ **pseudodevice**: trông như thiết bị đối với process nhưng thực ra được kernel giả lập bằng phần mềm, ví dụ `/dev/random` sinh số ngẫu nhiên.

---

## Ghi chú thêm: những điểm dễ hiểu nhầm

**Process không phải là thứ đi xin CPU.** Kernel mới là bên quyết định process nào chạy và chạy bao lâu. Khi được chạy, process thực thi lệnh trực tiếp trên CPU ở user mode; chỉ khi cần việc đặc quyền (I/O, xin bộ nhớ...) nó mới gọi kernel qua system call.

**Kernel cũng nằm trong RAM và chạy trên CPU.** Kernel không phải phần cứng riêng. CPU chuyển từ process sang kernel theo hai cách: process chủ động gọi system call, hoặc phần cứng gửi interrupt (ví dụ timer).

**RAM và ổ đĩa khác nhau ở tính lưu trữ.** RAM là bộ nhớ tạm, mất điện là mất; ổ đĩa lưu lâu dài. Chương trình nằm trên đĩa dưới dạng file, được kernel nạp vào RAM khi chạy. RAM không tự lấy dữ liệu từ đĩa; process phải yêu cầu và kernel cùng driver thực hiện.

**CPU không phải phần cứng "động" duy nhất.** CPU là nơi duy nhất thực thi code phần mềm (cả kernel và process), nhưng các thiết bị như bộ điều khiển đĩa, card mạng có mạch xử lý riêng, tự chép dữ liệu vào RAM (DMA) và báo cho CPU bằng interrupt khi xong.