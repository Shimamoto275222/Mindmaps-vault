Sửa thông tin của user đã có (home dir, shell, group...).

```bash
# sudo usermod [options] user
# -d : đổi home dir
# -s : đổi shell
# -aG: thêm user vào group
sudo usermod -d /home/new_home user1
sudo usermod -s /bin/zsh user1
sudo usermod -aG docker user1
```

⚠️ Dùng `-G` mà thiếu `-a` → user bị **thay** toàn bộ group phụ (mất các group cũ). Group mới chỉ có hiệu lực sau khi login lại, hoặc dùng [[newgrp]].
