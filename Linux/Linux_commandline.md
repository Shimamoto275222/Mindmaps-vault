---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin settings under 'Saving'

# Excalidraw Data

## Text Elements
Linux ^4g4lXgyK

File & Dir ^yBZGkcKm

/etc stores system-wide configuration.
/home stores ordinary users' home directories.
/tmp stores temporary data.
/usr contains many installed programs and shared resources.
/var contains changing data such as logs and caches. ^OvfrloLZ

list the contents of a directory ^jwprhufN

print working dir ^bWVwxtvn

change current dir ^T6P6b1YZ

create a dir ^paFRDJxM

find files and dirs ^3OuNA8S3

file Name matching (file globbing) ^MSofzPtZ

# any character 
"*.txt" -> a.txt,document.txt,...

# only 1 char
"?.txt" -> a.txt, b.txt,..

# char in group
"file[1-3].txt" -> file1.txt, file2.txt, file3.txt
 ^X81cQEQ6

Commands ^lul7FxK8

Terminal
(GUI) ^PZbWslpI

Shell 
(bash/sh/...)
 ^iQEnF4kW

OS ^KjiyhM5J

Shell takes keyboard commands
then pass to OS ^ymKzm9ku

- absolute path: root -> destination
- relative path: start from working dir ^MBSlJInx

change to home dir of other user ^9fQilHPe

cd ~user_name ^V1Ge56xT

pwd ^hR7aq7Ah

ls ^faEmJAOV

cd ^wZ841Xmg

mkdir ^F4Wl8kYN

find ^21ZXnj56

determine file's type ^PqHJOj9P

Filenames not reflect file's type ^yzPIPGEb

file ^NnYQ7rMd

file ^5w1WoXvw

Symbolic links & Hard links ^Bu7l2sBv

4 types of command: 
- executable program: "/usr/bin" programs can be compiled binaries or scripting languages
- command built-in shell: like "cd"
- shell function: miniature shell scripts incorporated into the environment 
- alias ^hIPnjNVZ

display type of command ^vsBcc2HJ

type ^7fXMrx42

display executable's location ^cgog6awQ

which ^3p9YTFWr

works only for 
executable programs ^tXCR8iJb

Redirection ^E3o4c8G5

Everything is a file ^xNBE3NLh

- programs send results to a tmp file -> standard output ( stdout)

- send status msg to another tmp file -> standard error (stderr)

- commonly take input from facility -> standard input (stdin)  ^wPMuVyIY

redirect stdout ^i1RVbXHo

> ^nxt1eMXh

>> ^win2A5OL

 if redirect only stdout 

-> error msg sent to the screen ^H1RSVN4V

redirect stderr ^y3RQ7S8l

File descriptor: 

- stdin -> 0 
- stdout -> 1
- stderr -> 2 ^slFxvhWJ

  ^42ddaN1f

> file_output 2>&1 
or 
&> file_output ^BTIpAtMS

dispose unwanted output ^240KRtTc

2> /dev/null ^D4nevgRD

redirect stdin ^8jNsSk85

< ^P300xo8K

write multi lines to file ^kYCjqNR6

cat >> file_name <<"EOF" ^GBjgDq8F

Pipeline ^1LGPu5dh

connects stdout of Command A 
to stdin of Command B ^InsAZb3G

command_A | command_B ^maYWI4aV

read from stdin and 
Output to stdout and files ^8VG42E9Z

tee ^BANCH90a

About Shell  ^YSebg4Rn

Command from terminal ^C8D2PhmE

Shell expand qualifying characters  ^8Qmjbz4a

OS executes ^S7FbnvIY

Shell expansion & substitution  ^lD7Pmt4i

Permissions ^NkfxeCmh

find identity info ^inpvXWUn

id ^Si94KchK

/etc/group: info about groups 

/etc/passwd: info about user accounts

/etc/shadow: info about user passwords ^OwmwjlVQ

directories ^kiilTN4S

files ^9CgOMQI7

r ^vLQgoyTk

x ^dxKTJ17n

w ^6ibgzhsS

r ^rW7dCepD

x ^nibMWNq8

w ^kiJ5eMT3

Permission attributes ^06DCFXeU

change file owner ^9JdqveYh

chown ^fCkHVnB4

change file mode 
(permissions) ^0oxHnFUg

chmod ^WTyQon2F

octal representation ^v1ENneID

symbolic representation ^TL3PhJy4

4 = Read (r)

2= Write (w)

1 = Execute (x) ^RYaWRxS1

u - g - o
user(owner) - group - other 

u+x -> add x to owner
g-w -> remove w from group
go=rx -> add r,x to group, other. Remove other ^hL0nqIdz

default permissions ^ny7AGj5s

umask ^npC1I4re

default permissions:

- files: 0666

- directories: 0777 ^1BvzqhfE

E.g: umask 0022 

-> remove write from (g,o)

create text.txt (default: 666)
-> 644  ^SZ5nYQNG

special permissions ^wt0hcOPR

setuid bit (4000 | s) ^jWi6pxsy

setgid bit (2000 | s) ^hgutb7ib

sticky bit (1000 | t) ^oNhwyKDB

When applied to an executable file, 
it sets the effective user ID from that of the real user (the user actually running the 
program) to that of the program's owner ^zXXHmFIt

 changes the effective group ID from the real group ID of the real user to that of the file owner

->  shared directory when members of a common group need access to all the files in the directory, regardless of the file owner's primary group ^7MvCaSb2

 - On files, Linux ignores the sticky bit

- If applied to a directory, it prevents users 
from deleting or renaming files 
(unless the user is either the owner of the directory, the owner of the file, or the superuser) 

-> often used to control access to a 
shared directory, such as /tmp ^UUJdYbkq

create new user ^AsCDwXU6

useradd ^0WzFfN8f

modify user account ^M4F6gJg2

usermod ^1IcbCHdf

delete user ^Ij71GDMi

userdel ^qs3T0QkS

change user's 
password ^oKkyM9Fi

passwd ^86m9ufIW

switch user ^8KwqMYZx

su / sudo -u ^7KWWKN4T

switch current 
active group ^5VF4ufk6

newgrp ^3UI1EFWT

Vim ^rrYag5ky

create a file ^OA6uLLBq

touch ^8icr88ij

Package Management ^zxO7v21L

low-level tools (dpkg/rpm)
-> Handle tasks such as installing and 
removing package ^c9aMk0yU

high-level tools (apt/ dnf)
-> metadata searching and dependency resolution ^yyOhs4CC

Package files: unit of Package system - .deb/.rpm (like .exe/.msi)

- Binaries & Data
- Dependencies
- Installation scripts (pre scripts/ post scripts) ^Mq2urxzA

Processes ^pYbpjbGq

system start up ^slXVXspO

kernel initiates and run "init"  -> init - PID 1 ^Em5AXKd7

"Init" start "systemd" -> start all services ^hzjJKTDv

view processes ^uIRUJNCd

ps / ps aux ^eE7Fj0Hn

view processes 
dynamically ^XmskFlt2

top ^y2JgEo7J

run a process 
in the background ^sOJ1274M

"process_name" & ^yHBTBlHn

list the jobs from terminal ^oTVd5yA6

jobs ^Wk3Dw2Gd

put process to background ^edLCymRw

bg %"job_id" ^LoTSof2l

put process to foreground ^GCflKIFC

fg %"job_id" ^YKCbQmJt

jobs -l ^XEXbntji

see job-process ^kg0aQjUr

"kill" command ^EpRgps5E

process ^J0moLZb6

sends "signal" to processes ^APM1QXJ3

kill a process ^cbuVfkyE

kill ^lTzmBqSO

Shell ^9ksOXjpZ

Environment ^wotTp7lN

Shell startup files: 

Khi Shell được mở, hệ điều hành đi tìm và đọc file cấu hình để thiết lập môi trường làm việc

VD: Terminal kích hoạt Zsh -> đọc ~/.zshrc ^XJyhc6U3

2 types variables:
 
- Local variables: Biến nội bộ trong process đó 

- Environment variables: Biến được exported, có thể truyền vào process con ^i1se7seC

show 2 types + functions ^j2c2ZHeo

set ^G7nDtK1X

show only env_variables  ^ydNjDxCb

printenv 
||
printenv "var_name" ^yEM245hH

pass variables to child process ^xjZWezRH

export ^NaHf6aKj

add var in current shell: foo="bar" ^quYLVbsA

pass to 
child process ^1H1vJd2k

export foo ^bUPZ59cZ

make var persistent  ^Rvzm03PJ

add to .zshrc + . ~/.zshrc ^bIxQYPU6

## Element Links
sWhJyI9I: [[ls]]

E9MIKuON: [[cd]]

uScJmPma: [[mkdir]]

Rls0FoHo: [[find]]

E8npY1lY: [[Shell expansion && substitution]]

n9eybEgP: [[Permission attributes]]

4RuAkxZ1: [[chown]]

7yfOC2Oo: [[useradd]]

JvNImhrN: [[usermod]]

amwHsAIO: [[userdel]]

rgwbs7tS: [[passwd]]

o0mi6hEe: [[su]]

xyKVc2Ry: [[newgrp]]

EOcfMQ9O: [[Vim]]

ZDdzTYu4: [[Package Management (apt)]]

8RqBljqC: [[ps]]

rTx9da3F: [[ps]]

m1eg7j8v: [[kill]]

s9aBDBPi: [[shell script]]

A9bYrQK2: [[export]]

%%
## Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.28.1",
	"elements": [
		{
			"id": "AZcNg1xx",
			"type": "arrow",
			"x": -3481.8759501128325,
			"y": 2355.462807143998,
			"width": 671.2965262735634,
			"height": 710.9408735804102,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "Zu",
			"roundness": {
				"type": 2
			},
			"seed": 567906420,
			"version": 365,
			"versionNonce": 562310146,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770707,
			"created": 1792075766605,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					558.380939804937,
					-305.0237792268217
				],
				[
					671.2965262735634,
					-710.9408735804102
				]
			],
			"startBinding": {
				"elementId": "llv3BdCf_N2n4b9eD2fy7",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "uIRUJNCd",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					1
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "PZbWslpI",
			"type": "text",
			"x": -1063.5715736229672,
			"y": -1756.3080094597917,
			"width": 110.87992858886719,
			"height": 70,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"kFWltwxbEEKlvED2NVOxj"
			],
			"frameId": null,
			"index": "Zv",
			"roundness": null,
			"seed": 689113494,
			"version": 1082,
			"versionNonce": 25971972,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790869887601,
			"locked": false,
			"text": "Terminal\n(GUI)",
			"rawText": "Terminal\n(GUI)",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Terminal\n(GUI)",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "iQEnF4kW",
			"type": "text",
			"x": -1074.4240110855658,
			"y": -1616.351056521946,
			"width": 171.86392211914062,
			"height": 105,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"kFWltwxbEEKlvED2NVOxj"
			],
			"frameId": null,
			"index": "Zw",
			"roundness": null,
			"seed": 559079062,
			"version": 1048,
			"versionNonce": 805571716,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790869906834,
			"locked": false,
			"text": "Shell \n(bash/sh/...)\n",
			"rawText": "Shell \n(bash/sh/...)\n",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Shell \n(bash/sh/...)\n",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "KjiyhM5J",
			"type": "text",
			"x": -1032.1031779806885,
			"y": -1461.1752066058982,
			"width": 38.891998291015625,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"kFWltwxbEEKlvED2NVOxj"
			],
			"frameId": null,
			"index": "Zx",
			"roundness": null,
			"seed": 337998346,
			"version": 1024,
			"versionNonce": 1213717508,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790869921896,
			"locked": false,
			"text": "OS",
			"rawText": "OS",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "OS",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "Oktu7hvzbZQKdfP727Jra",
			"type": "freedraw",
			"x": -1015.3726508516347,
			"y": -1668.7399631340902,
			"width": 6.8212747473901345,
			"height": 47.74905333755237,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"kFWltwxbEEKlvED2NVOxj"
			],
			"frameId": null,
			"index": "Zy",
			"roundness": null,
			"seed": 2025146186,
			"version": 1030,
			"versionNonce": 1418050436,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790869937635,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					2.273729336725296,
					0
				],
				[
					4.547545410664952,
					3.4106373736949536
				],
				[
					5.68441007902743,
					9.095047452722383
				],
				[
					5.68441007902743,
					14.77945753175004
				],
				[
					5.68441007902743,
					21.600732279140175
				],
				[
					5.68441007902743,
					27.285142358167604
				],
				[
					3.410594005087887,
					32.96955243719526
				],
				[
					2.273729336725296,
					37.517097847860214
				],
				[
					1.1368646683627048,
					42.06464325852494
				],
				[
					1.1368646683627048,
					44.33837259525012
				],
				[
					1.1368646683627048,
					45.47528063222012
				],
				[
					1.1368646683627048,
					47.74905333755237
				],
				[
					1.1368646683627048,
					46.6121453005826
				],
				[
					1.1368646683627048,
					45.47528063222012
				],
				[
					1.1368646683627048,
					44.33837259525012
				],
				[
					-1.1368646683627048,
					44.33837259525012
				],
				[
					-1.1368646683627048,
					44.33837259525012
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "Ss_WwG3MXFQnFZkSufXTk",
			"type": "freedraw",
			"x": -1018.783331593937,
			"y": -1537.9985313164577,
			"width": 22.73764031611006,
			"height": 65.93919161160466,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"kFWltwxbEEKlvED2NVOxj"
			],
			"frameId": null,
			"index": "Zz",
			"roundness": null,
			"seed": 1169369622,
			"version": 1029,
			"versionNonce": 1858841348,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790869941041,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					2.2738160739395425,
					0
				],
				[
					3.4106807423022474,
					0
				],
				[
					5.684410079027543,
					2.2737293367251823
				],
				[
					10.231955489692382,
					5.68441007902743
				],
				[
					14.779500900357334,
					13.642549494780269
				],
				[
					20.463910979384764,
					19.326959573807926
				],
				[
					21.60077564774747,
					26.14832105841242
				],
				[
					22.73764031611006,
					30.695779731862785
				],
				[
					22.73764031611006,
					36.38018981089044
				],
				[
					22.73764031611006,
					42.064599889917645
				],
				[
					21.60077564774747,
					48.88596137452214
				],
				[
					19.327046311022173,
					54.5703714535498
				],
				[
					17.053230237082516,
					56.844100790275206
				],
				[
					13.64263623199463,
					61.39164620093993
				],
				[
					12.505684826417678,
					64.80224020602782
				],
				[
					11.368820158055087,
					65.93919161160466
				],
				[
					11.368820158055087,
					65.93919161160466
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "ZpVcCTjTwf0tJ_DvODOna",
			"type": "freedraw",
			"x": -980.129325709107,
			"y": -1500.4813900999904,
			"width": 105.73006216479735,
			"height": 14.779500900357107,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"kFWltwxbEEKlvED2NVOxj"
			],
			"frameId": null,
			"index": "a0",
			"roundness": null,
			"seed": 1834941334,
			"version": 1028,
			"versionNonce": 967289476,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790869953296,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-2.2738160739395425
				],
				[
					3.4106807423022474,
					-5.684410079027657
				],
				[
					9.095090821329677,
					-7.9582261529672
				],
				[
					18.190094905445108,
					-10.231955489692382
				],
				[
					31.832731137439737,
					-11.36882015805486
				],
				[
					46.61214530058271,
					-13.64263623199463
				],
				[
					63.66537553766523,
					-14.779500900357107
				],
				[
					78.44487643802245,
					-14.779500900357107
				],
				[
					89.81369659607753,
					-14.779500900357107
				],
				[
					95.49810667510496,
					-14.779500900357107
				],
				[
					97.77183601183026,
					-14.779500900357107
				],
				[
					100.04565208576992,
					-14.779500900357107
				],
				[
					101.18251675413251,
					-14.779500900357107
				],
				[
					102.3193814224951,
					-14.779500900357107
				],
				[
					105.73006216479735,
					-14.779500900357107
				],
				[
					105.73006216479735,
					-14.779500900357107
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "ymKzm9ku",
			"type": "text",
			"x": -867.5779887969193,
			"y": -1548.7642155097985,
			"width": 424.0877990722656,
			"height": 70,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"kFWltwxbEEKlvED2NVOxj"
			],
			"frameId": null,
			"index": "a1",
			"roundness": null,
			"seed": 991569238,
			"version": 1176,
			"versionNonce": 1473755652,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790869956339,
			"locked": false,
			"text": "Shell takes keyboard commands\nthen pass to OS",
			"rawText": "Shell takes keyboard commands\nthen pass to OS",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Shell takes keyboard commands\nthen pass to OS",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "BgtGftaI",
			"type": "rectangle",
			"x": -1089.5873477826608,
			"y": -1782.5663179086778,
			"width": 661.2604947551022,
			"height": 382.64941975166505,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"kFWltwxbEEKlvED2NVOxj"
			],
			"frameId": null,
			"index": "a2",
			"roundness": {
				"type": 3
			},
			"seed": 186261706,
			"version": 1078,
			"versionNonce": 247458733,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "bw8W3jIW",
					"type": "arrow"
				},
				{
					"id": "xzx8aca4",
					"type": "arrow"
				},
				{
					"id": "B6hXG4MREPkAajuyXPV8Y",
					"type": "arrow"
				}
			],
			"updated": 1792684251159,
			"created": 1790870488558,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "qvrFhxju",
			"type": "rectangle",
			"x": -993.2010772170524,
			"y": 420.03888069445026,
			"width": 410.03768780550354,
			"height": 319.92201091187763,
			"angle": 0,
			"strokeColor": "#1971c2",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "a3",
			"roundness": {
				"type": 3
			},
			"seed": 301446963,
			"version": 548,
			"versionNonce": 1738625346,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "4g4lXgyK"
				},
				{
					"id": "Lh5UQ6rA",
					"type": "arrow"
				},
				{
					"id": "gd5p5BlK",
					"type": "arrow"
				},
				{
					"id": "XcVPNBXB",
					"type": "arrow"
				},
				{
					"id": "9YveESuI",
					"type": "arrow"
				},
				{
					"id": "bw8W3jIW",
					"type": "arrow"
				},
				{
					"id": "F0KE4YF2",
					"type": "arrow"
				},
				{
					"id": "4I1zwTud",
					"type": "arrow"
				},
				{
					"id": "wsUiAAMQ",
					"type": "arrow"
				},
				{
					"id": "qThcCr3r",
					"type": "arrow"
				},
				{
					"id": "t9m1CJyc",
					"type": "arrow"
				},
				{
					"id": "9w2mGQC6",
					"type": "arrow"
				}
			],
			"updated": 1792945849868,
			"created": 1790827495405,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "4g4lXgyK",
			"type": "text",
			"x": -832.3182120130311,
			"y": 557.4998861503891,
			"width": 88.27195739746094,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "a4",
			"roundness": null,
			"seed": 959434035,
			"version": 494,
			"versionNonce": 1112860757,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665804317,
			"created": 1790827567378,
			"locked": false,
			"text": "Linux",
			"rawText": "Linux",
			"fontSize": 36,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "qvrFhxju",
			"originalText": "Linux",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "7_1cj0rG0M09Pa5fcUjM4",
			"type": "rectangle",
			"x": 160.39503620482583,
			"y": -858.0725598236035,
			"width": 178,
			"height": 152,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "a5V",
			"roundness": {
				"type": 3
			},
			"seed": 1702948061,
			"version": 715,
			"versionNonce": 426558753,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "yBZGkcKm"
				},
				{
					"id": "Lh5UQ6rA",
					"type": "arrow"
				},
				{
					"id": "snFTnuN9",
					"type": "arrow"
				},
				{
					"id": "EOTOl5In",
					"type": "arrow"
				},
				{
					"id": "LGaa7upO",
					"type": "arrow"
				},
				{
					"id": "21Az3Y5h",
					"type": "arrow"
				},
				{
					"id": "TcAP655l",
					"type": "arrow"
				},
				{
					"id": "PDupNevs",
					"type": "arrow"
				},
				{
					"id": "jxME1U2P",
					"type": "arrow"
				},
				{
					"id": "fSoX4a1o",
					"type": "arrow"
				},
				{
					"id": "FZh0jed6",
					"type": "arrow"
				}
			],
			"updated": 1791932049977,
			"created": 1790846975804,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "yBZGkcKm",
			"type": "text",
			"x": 184.70107410765786,
			"y": -799.5725598236035,
			"width": 129.38792419433594,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "a6",
			"roundness": null,
			"seed": 1139362109,
			"version": 686,
			"versionNonce": 841938820,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790846975804,
			"locked": false,
			"text": "File & Dir",
			"rawText": "File & Dir",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7_1cj0rG0M09Pa5fcUjM4",
			"originalText": "File & Dir",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "Lh5UQ6rA",
			"type": "arrow",
			"x": -569.3418943169813,
			"y": 580.0318783514803,
			"width": 723.736930521807,
			"height": 1362.0892381750837,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "aD",
			"roundness": {
				"type": 2
			},
			"seed": 1759180733,
			"version": 1580,
			"versionNonce": 1786307419,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791667109587,
			"created": 1790846988171,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					380.1391681585819,
					-1067.0440475645157
				],
				[
					723.736930521807,
					-1362.0892381750837
				]
			],
			"startBinding": {
				"elementId": "qvrFhxju",
				"mode": "orbit",
				"fixedPoint": [
					1.0337078651685394,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "7_1cj0rG0M09Pa5fcUjM4",
				"mode": "orbit",
				"fixedPoint": [
					-0.033707865168539804,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"fixedSegments": [
				{
					"index": 2,
					"start": [
						204.03708815352056,
						0
					],
					"end": [
						204.03708815352056,
						564.0776713436479
					]
				}
			],
			"startIsSpecial": false,
			"endIsSpecial": false,
			"hasTextLink": false
		},
		{
			"id": "zDvkAxvp",
			"type": "stickynote",
			"x": 113.31869827645255,
			"y": -1451.7899425177357,
			"width": 338.66158675741593,
			"height": 338.66158675741593,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffdf6b",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "aM",
			"roundness": {
				"type": 2
			},
			"seed": 800819850,
			"version": 691,
			"versionNonce": 2051465857,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "OvfrloLZ"
				},
				{
					"id": "FZh0jed6",
					"type": "arrow"
				}
			],
			"updated": 1791932205927,
			"created": 1790867470954,
			"link": null,
			"locked": false,
			"baseHeight": 338.66158675741593,
			"hasTextLink": false
		},
		{
			"id": "OvfrloLZ",
			"type": "text",
			"x": 129.31869827645255,
			"y": -1394.9591491390277,
			"width": 305.499755859375,
			"height": 225,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "aMV",
			"roundness": null,
			"seed": 262856778,
			"version": 536,
			"versionNonce": 1659054191,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791932206652,
			"created": 1790867477481,
			"locked": false,
			"text": "/etc stores system-wide\nconfiguration.\n/home stores ordinary users'\nhome directories.\n/tmp stores temporary data.\n/usr contains many installed\nprograms and shared resources.\n/var contains changing data\nsuch as logs and caches.",
			"rawText": "/etc stores system-wide configuration.\n/home stores ordinary users' home directories.\n/tmp stores temporary data.\n/usr contains many installed programs and shared resources.\n/var contains changing data such as logs and caches.",
			"fontSize": 20,
			"baseFontSize": 28,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "middle",
			"containerId": "zDvkAxvp",
			"originalText": "/etc stores system-wide configuration.\n/home stores ordinary users' home directories.\n/tmp stores temporary data.\n/usr contains many installed programs and shared resources.\n/var contains changing data such as logs and caches.",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "FZh0jed6",
			"type": "arrow",
			"x": 249.4277048975237,
			"y": -864.0725598236036,
			"width": 32.007344713520865,
			"height": 243.5557959367161,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "aP",
			"roundness": {
				"type": 2
			},
			"seed": 1962267658,
			"version": 650,
			"versionNonce": 1849620033,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791932205928,
			"created": 1790867567324,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.2568925299602256,
					-103.66447212817002
				],
				[
					32.007344713520865,
					-243.5557959367161
				]
			],
			"startBinding": {
				"elementId": "7_1cj0rG0M09Pa5fcUjM4",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					0
				]
			},
			"endBinding": {
				"elementId": "zDvkAxvp",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					1.0000000000000002
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "jwprhufN",
			"type": "text",
			"x": 573.2717643637898,
			"y": -907.3885355018335,
			"width": 437.1918029785156,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "aR",
			"roundness": null,
			"seed": 492605066,
			"version": 232,
			"versionNonce": 1792001284,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "snFTnuN9",
					"type": "arrow"
				},
				{
					"id": "ppLUyr0Z",
					"type": "arrow"
				},
				{
					"id": "SLKRiXOf",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790867586893,
			"link": null,
			"locked": false,
			"text": "list the contents of a directory",
			"rawText": "list the contents of a directory",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "list the contents of a directory",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false
		},
		{
			"id": "snFTnuN9",
			"type": "arrow",
			"x": 337.269047193849,
			"y": -787.9936420869448,
			"width": 230.50271716994075,
			"height": 99.51683319582855,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "aS",
			"roundness": {
				"type": 2
			},
			"seed": 136919690,
			"version": 452,
			"versionNonce": 303596676,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790867595355,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					230.50271716994075,
					-99.51683319582855
				]
			],
			"startBinding": {
				"elementId": "7_1cj0rG0M09Pa5fcUjM4",
				"mode": "inside",
				"fixedPoint": [
					0.9936742190394561,
					0.46104551142538613
				]
			},
			"endBinding": {
				"elementId": "jwprhufN",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "bWVwxtvn",
			"type": "text",
			"x": 650.757684053384,
			"y": -811.3677901042153,
			"width": 221.6478729248047,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "aT",
			"roundness": null,
			"seed": 241310998,
			"version": 113,
			"versionNonce": 1629312004,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "EOTOl5In",
					"type": "arrow"
				},
				{
					"id": "iZhyEdP1",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790867610865,
			"locked": false,
			"text": "print working dir",
			"rawText": "print working dir",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "print working dir",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "EOTOl5In",
			"type": "arrow",
			"x": 344.3950362048258,
			"y": -782.284152566499,
			"width": 300.8626478485582,
			"height": 11.372244190062133,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "aU",
			"roundness": {
				"type": 2
			},
			"seed": 338678230,
			"version": 253,
			"versionNonce": 108333019,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124990,
			"created": 1790867616233,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					300.8626478485582,
					-11.372244190062133
				]
			],
			"startBinding": {
				"elementId": "7_1cj0rG0M09Pa5fcUjM4",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "bWVwxtvn",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "T6P6b1YZ",
			"type": "text",
			"x": 649.3362515841608,
			"y": -704.750593816626,
			"width": 246.34390258789062,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "aV",
			"roundness": null,
			"seed": 343019146,
			"version": 118,
			"versionNonce": 1049830148,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "LGaa7upO",
					"type": "arrow"
				},
				{
					"id": "P28dLEI6",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790867626757,
			"locked": false,
			"text": "change current dir",
			"rawText": "change current dir",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "change current dir",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "LGaa7upO",
			"type": "arrow",
			"x": 338.01379981983496,
			"y": -780.2305145500724,
			"width": 305.8224517643258,
			"height": 91.34072258837,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "aW",
			"roundness": {
				"type": 2
			},
			"seed": 531122518,
			"version": 283,
			"versionNonce": 1876776059,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124990,
			"created": 1790867629303,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					305.8224517643258,
					91.34072258837
				]
			],
			"startBinding": {
				"elementId": "7_1cj0rG0M09Pa5fcUjM4",
				"mode": "inside",
				"fixedPoint": [
					0.997858222556231,
					0.5121187189048098
				]
			},
			"endBinding": {
				"elementId": "T6P6b1YZ",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "paFRDJxM",
			"type": "text",
			"x": 655.0223068309152,
			"y": -598.0402358078936,
			"width": 160.60792541503906,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "aX",
			"roundness": null,
			"seed": 184380106,
			"version": 141,
			"versionNonce": 337648057,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "TcAP655l",
					"type": "arrow"
				},
				{
					"id": "4631YEES",
					"type": "arrow"
				}
			],
			"updated": 1791850264715,
			"created": 1790867638243,
			"locked": false,
			"text": "create a dir",
			"rawText": "create a dir",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "create a dir",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "TcAP655l",
			"type": "arrow",
			"x": 344.39503620482583,
			"y": -778.2385992294722,
			"width": 305.1272706260893,
			"height": 194.20133287695808,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "aZ",
			"roundness": {
				"type": 2
			},
			"seed": 740101450,
			"version": 361,
			"versionNonce": 499691963,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124990,
			"created": 1790867646233,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					305.1272706260893,
					194.20133287695808
				]
			],
			"startBinding": {
				"elementId": "7_1cj0rG0M09Pa5fcUjM4",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "paFRDJxM",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "3OuNA8S3",
			"type": "text",
			"x": 664.9733102250625,
			"y": -494.83435209564254,
			"width": 241.6118621826172,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "aa",
			"roundness": null,
			"seed": 701180362,
			"version": 41,
			"versionNonce": 1052213508,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "21Az3Y5h",
					"type": "arrow"
				},
				{
					"id": "fdn8NzlW",
					"type": "arrow"
				},
				{
					"id": "N6HKW5fC",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790867668947,
			"locked": false,
			"text": "find files and dirs",
			"rawText": "find files and dirs",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "find files and dirs",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "21Az3Y5h",
			"type": "arrow",
			"x": 338.0139082764556,
			"y": -781.9294071616737,
			"width": 321.4594019486068,
			"height": 300.7882277138476,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "ab",
			"roundness": {
				"type": 2
			},
			"seed": 647896074,
			"version": 188,
			"versionNonce": 1808993563,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124990,
			"created": 1790867674513,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					142.24803279959883,
					176.63295831553637
				],
				[
					321.4594019486068,
					300.7882277138476
				]
			],
			"startBinding": {
				"elementId": "7_1cj0rG0M09Pa5fcUjM4",
				"mode": "inside",
				"fixedPoint": [
					0.9978588318630885,
					0.5009417938284854
				]
			},
			"endBinding": {
				"elementId": "3OuNA8S3",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "MSofzPtZ",
			"type": "text",
			"x": 1116.1437280829762,
			"y": -497.3987073428657,
			"width": 443.519775390625,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "ac",
			"roundness": null,
			"seed": 1390725462,
			"version": 154,
			"versionNonce": 1933971460,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "fdn8NzlW",
					"type": "arrow"
				},
				{
					"id": "kyI7EVbn",
					"type": "arrow"
				},
				{
					"id": "SbXwcm3S",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790869165265,
			"locked": false,
			"text": "file Name matching (file globbing)",
			"rawText": "file Name matching (file globbing)",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "file Name matching (file globbing)",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "fdn8NzlW",
			"type": "arrow",
			"x": 912.0851724076798,
			"y": -477.39815525973563,
			"width": 198.55855567529636,
			"height": 2.4297489190369674,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "ad",
			"roundness": {
				"type": 2
			},
			"seed": 1047261526,
			"version": 130,
			"versionNonce": 1804431236,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790869170039,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					198.55855567529636,
					-2.4297489190369674
				]
			],
			"startBinding": {
				"elementId": "3OuNA8S3",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "MSofzPtZ",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "nekX0iNS",
			"type": "rectangle",
			"x": 1678.6815889833897,
			"y": -661.925509531125,
			"width": 442.9976791772255,
			"height": 360,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "af",
			"roundness": {
				"type": 3
			},
			"seed": 733100298,
			"version": 756,
			"versionNonce": 851238660,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "X81cQEQ6"
				},
				{
					"id": "kyI7EVbn",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790869229556,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "X81cQEQ6",
			"type": "text",
			"x": 1683.6815889833897,
			"y": -656.925509531125,
			"width": 430.89178466796875,
			"height": 350,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "ag",
			"roundness": null,
			"seed": 793007638,
			"version": 272,
			"versionNonce": 1364352644,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790869230906,
			"locked": false,
			"text": "# any character \n\"*.txt\" -> a.txt,document.txt,...\n\n# only 1 char\n\"?.txt\" -> a.txt, b.txt,..\n\n# char in group\n\"file[1-3].txt\" -> file1.txt,\nfile2.txt, file3.txt\n",
			"rawText": "# any character \n\"*.txt\" -> a.txt,document.txt,...\n\n# only 1 char\n\"?.txt\" -> a.txt, b.txt,..\n\n# char in group\n\"file[1-3].txt\" -> file1.txt, file2.txt, file3.txt\n",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "middle",
			"containerId": "nekX0iNS",
			"originalText": "# any character \n\"*.txt\" -> a.txt,document.txt,...\n\n# only 1 char\n\"?.txt\" -> a.txt, b.txt,..\n\n# char in group\n\"file[1-3].txt\" -> file1.txt, file2.txt, file3.txt\n",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "kyI7EVbn",
			"type": "arrow",
			"x": 1558.8935088328521,
			"y": -475.1931305482343,
			"width": 114.28808015053755,
			"height": 6.3889186382586445,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "ah",
			"roundness": {
				"type": 2
			},
			"seed": 391983318,
			"version": 299,
			"versionNonce": 1074495938,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770677,
			"created": 1790869263609,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					114.28808015053755,
					-6.3889186382586445
				]
			],
			"startBinding": {
				"elementId": "MSofzPtZ",
				"mode": "inside",
				"fixedPoint": [
					0.9982639000931338,
					0.6344450512751824
				]
			},
			"endBinding": {
				"elementId": "nekX0iNS",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "gd5p5BlK",
			"type": "arrow",
			"x": -577.1633894115489,
			"y": 580.4274090153754,
			"width": 889.6668710342162,
			"height": 58.64842135762569,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b0c",
			"roundness": {
				"type": 2
			},
			"seed": 459550090,
			"version": 530,
			"versionNonce": 1811715861,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665804317,
			"created": 1790870537753,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					889.6668710342162,
					58.64842135762569
				]
			],
			"startBinding": {
				"elementId": "qvrFhxju",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "YgY2yAgwHN22eybuHXTev",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "8QVf9SFV",
			"type": "rectangle",
			"x": 1094.340356483533,
			"y": -938.7792603145871,
			"width": 560.4565171534929,
			"height": 87.82356244416769,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b0d",
			"roundness": {
				"type": 3
			},
			"seed": 898407126,
			"version": 166,
			"versionNonce": 3996804,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "MBSlJInx"
				},
				{
					"id": "ppLUyr0Z",
					"type": "arrow"
				},
				{
					"id": "4xlHS6vq",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790870698497,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "MBSlJInx",
			"type": "text",
			"x": 1114.7287407927013,
			"y": -929.8674790925032,
			"width": 519.6797485351562,
			"height": 70,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b0dV",
			"roundness": null,
			"seed": 204538390,
			"version": 325,
			"versionNonce": 66243588,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790870717273,
			"locked": false,
			"text": "- absolute path: root -> destination\n- relative path: start from working dir",
			"rawText": "- absolute path: root -> destination\n- relative path: start from working dir",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8QVf9SFV",
			"originalText": "- absolute path: root -> destination\n- relative path: start from working dir",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "ppLUyr0Z",
			"type": "arrow",
			"x": 1015.9635673423053,
			"y": -890.2111702653291,
			"width": 72.87678914122773,
			"height": 4.321391707434145,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b0f",
			"roundness": {
				"type": 2
			},
			"seed": 1794944458,
			"version": 30,
			"versionNonce": 396393531,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124992,
			"created": 1790870778025,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					72.87678914122773,
					-4.321391707434145
				]
			],
			"startBinding": {
				"elementId": "jwprhufN",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "8QVf9SFV",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "9fQilHPe",
			"type": "text",
			"x": 1757.7468339209474,
			"y": -912.1424056986722,
			"width": 455.05584716796875,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b0g",
			"roundness": null,
			"seed": 1397661462,
			"version": 121,
			"versionNonce": 1416272644,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "4xlHS6vq",
					"type": "arrow"
				},
				{
					"id": "NJeVggp3",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790870811213,
			"locked": false,
			"text": "change to home dir of other user",
			"rawText": "change to home dir of other user",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "change to home dir of other user",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "4xlHS6vq",
			"type": "arrow",
			"x": 1660.2968736370256,
			"y": -894.8469546170447,
			"width": 91.94996028392188,
			"height": 0.1963067991587195,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b0h",
			"roundness": {
				"type": 2
			},
			"seed": 1265812630,
			"version": 70,
			"versionNonce": 1213938907,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124992,
			"created": 1790870829516,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					91.94996028392188,
					0.1963067991587195
				]
			],
			"startBinding": {
				"elementId": "8QVf9SFV",
				"mode": "orbit",
				"fixedPoint": [
					0.9999999999999998,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "9fQilHPe",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "TKUjEnLN",
			"type": "rectangle",
			"x": 2212.802681224196,
			"y": -811.3677900757564,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b0i",
			"roundness": {
				"type": 3
			},
			"seed": 1381069398,
			"version": 355,
			"versionNonce": 1710525527,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "V1Ge56xT"
				},
				{
					"id": "NJeVggp3",
					"type": "arrow"
				}
			],
			"updated": 1791850303560,
			"created": 1790870842143,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "V1Ge56xT",
			"type": "text",
			"x": 2247.943481467577,
			"y": -799.9574154055485,
			"width": 201.31993103027344,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b0j",
			"roundness": null,
			"seed": 2023614678,
			"version": 340,
			"versionNonce": 40823159,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791850303560,
			"created": 1790870843209,
			"locked": false,
			"text": "cd ~user_name",
			"rawText": "cd ~user_name",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "TKUjEnLN",
			"originalText": "cd ~user_name",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "NJeVggp3",
			"type": "arrow",
			"x": 2212.8070754554665,
			"y": -871.6425165891811,
			"width": 0.0042859801342274295,
			"height": 59.730700602076126,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b0k",
			"roundness": {
				"type": 2
			},
			"seed": 925985814,
			"version": 252,
			"versionNonce": 367043223,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791850303560,
			"created": 1790870857621,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.0042859801342274295,
					59.730700602076126
				]
			],
			"startBinding": {
				"elementId": "9fQilHPe",
				"mode": "orbit",
				"fixedPoint": [
					0.9999999999999994,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "TKUjEnLN",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "bKpAk8f3OdWwpPhqyqk6L",
			"type": "rectangle",
			"x": 967.4496448117284,
			"y": -816.880649456509,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b0l",
			"roundness": {
				"type": 3
			},
			"seed": 579473814,
			"version": 324,
			"versionNonce": 836057220,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "hR7aq7Ah"
				},
				{
					"id": "iZhyEdP1",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790870872316,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "hR7aq7Ah",
			"type": "text",
			"x": 1077.5604233876288,
			"y": -805.4702747863012,
			"width": 51.379974365234375,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b0m",
			"roundness": null,
			"seed": 700411606,
			"version": 310,
			"versionNonce": 1327728644,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790870872316,
			"locked": false,
			"text": "pwd",
			"rawText": "pwd",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "bKpAk8f3OdWwpPhqyqk6L",
			"originalText": "pwd",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "iZhyEdP1",
			"type": "arrow",
			"x": 871.0778758267019,
			"y": -790.6760862082128,
			"width": 90.87176898502639,
			"height": 2.5568410793096064,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b0n",
			"roundness": {
				"type": 2
			},
			"seed": 1449289610,
			"version": 152,
			"versionNonce": 1466958363,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124993,
			"created": 1790870876155,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					90.87176898502639,
					2.5568410793096064
				]
			],
			"startBinding": {
				"elementId": "bWVwxtvn",
				"mode": "inside",
				"fixedPoint": [
					0.9940099531118117,
					0.5911915398857835
				]
			},
			"endBinding": {
				"elementId": "bKpAk8f3OdWwpPhqyqk6L",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "sWhJyI9I",
			"type": "rectangle",
			"x": 1108.750411330611,
			"y": -1068.4083660784265,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b0o",
			"roundness": {
				"type": 3
			},
			"seed": 864112202,
			"version": 318,
			"versionNonce": 1604081419,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "faEmJAOV"
				},
				{
					"id": "SLKRiXOf",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790870910468,
			"link": "[[ls]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "faEmJAOV",
			"type": "text",
			"x": 1233.799185817156,
			"y": -1056.9979914082187,
			"width": 21.503982543945312,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b0p",
			"roundness": null,
			"seed": 932508938,
			"version": 294,
			"versionNonce": 595777156,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790870910468,
			"locked": false,
			"text": "ls",
			"rawText": "ls",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "sWhJyI9I",
			"originalText": "ls",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "SLKRiXOf",
			"type": "arrow",
			"x": 1015.9635673423053,
			"y": -898.2568523461192,
			"width": 87.28684398830558,
			"height": 132.86354014287974,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b0q",
			"roundness": {
				"type": 2
			},
			"seed": 1796892054,
			"version": 50,
			"versionNonce": 1409222331,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124994,
			"created": 1790870924089,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					87.28684398830558,
					-132.86354014287974
				]
			],
			"startBinding": {
				"elementId": "jwprhufN",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "sWhJyI9I",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "E9MIKuON",
			"type": "rectangle",
			"x": 965.707218059724,
			"y": -715.8575529006589,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b1H",
			"roundness": {
				"type": 3
			},
			"seed": 343590934,
			"version": 367,
			"versionNonce": 1515849099,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "wZ841Xmg"
				},
				{
					"id": "P28dLEI6",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790870929873,
			"link": "[[cd]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "wZ841Xmg",
			"type": "text",
			"x": 1085.9819904710737,
			"y": -704.4471782304511,
			"width": 31.051986694335938,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b1I",
			"roundness": null,
			"seed": 961893718,
			"version": 343,
			"versionNonce": 126268676,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790870929873,
			"locked": false,
			"text": "cd",
			"rawText": "cd",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "E9MIKuON",
			"originalText": "cd",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "P28dLEI6",
			"type": "arrow",
			"x": 901.1801541720513,
			"y": -687.2230839975251,
			"width": 59.02706388767274,
			"height": 0.25767802290738473,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b1j",
			"roundness": {
				"type": 2
			},
			"seed": 1203408778,
			"version": 37,
			"versionNonce": 1032091483,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124994,
			"created": 1790870945253,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					59.02706388767274,
					0.25767802290738473
				]
			],
			"startBinding": {
				"elementId": "T6P6b1YZ",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "E9MIKuON",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "uScJmPma",
			"type": "rectangle",
			"x": 848.3639937674001,
			"y": -616.5911877873511,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b1k",
			"roundness": {
				"type": 3
			},
			"seed": 1727541270,
			"version": 411,
			"versionNonce": 282608651,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "F4Wl8kYN"
				},
				{
					"id": "4631YEES",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790870951023,
			"link": "[[mkdir]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "F4Wl8kYN",
			"type": "text",
			"x": 949.7667797895896,
			"y": -605.1808131171433,
			"width": 68.79595947265625,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b1l",
			"roundness": null,
			"seed": 669367638,
			"version": 401,
			"versionNonce": 12133252,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790870951023,
			"locked": false,
			"text": "mkdir",
			"rawText": "mkdir",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "uScJmPma",
			"originalText": "mkdir",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "4631YEES",
			"type": "arrow",
			"x": 821.1302322459543,
			"y": -581.7361281772371,
			"width": 21.733761521445672,
			"height": 4.739510495628451,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b2C",
			"roundness": {
				"type": 2
			},
			"seed": 348760458,
			"version": 96,
			"versionNonce": 138836633,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791850264716,
			"created": 1790871016872,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					21.733761521445672,
					-4.739510495628451
				]
			],
			"startBinding": {
				"elementId": "paFRDJxM",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "uScJmPma",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "Rls0FoHo",
			"type": "rectangle",
			"x": 876.6739181492142,
			"y": -408.65877099498675,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b2D",
			"roundness": {
				"type": 3
			},
			"seed": 1028108874,
			"version": 324,
			"versionNonce": 773919371,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "21ZXnj56"
				},
				{
					"id": "N6HKW5fC",
					"type": "arrow"
				},
				{
					"id": "SbXwcm3S",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790871023612,
			"link": "[[find]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "21ZXnj56",
			"type": "text",
			"x": 986.2666989834154,
			"y": -397.2483963247789,
			"width": 52.41596984863281,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b2E",
			"roundness": null,
			"seed": 49207562,
			"version": 301,
			"versionNonce": 1222910468,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790871023612,
			"locked": false,
			"text": "find",
			"rawText": "find",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Rls0FoHo",
			"originalText": "find",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "N6HKW5fC",
			"type": "arrow",
			"x": 788.9239310359636,
			"y": -454.33435209564254,
			"width": 82.24998711325054,
			"height": 72.23586282662359,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b2F",
			"roundness": {
				"type": 2
			},
			"seed": 1992532042,
			"version": 73,
			"versionNonce": 577543323,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124994,
			"created": 1790871028735,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					27.735987520578988,
					48.88528649287127
				],
				[
					82.24998711325054,
					72.23586282662359
				]
			],
			"startBinding": {
				"elementId": "3OuNA8S3",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					1
				]
			},
			"endBinding": {
				"elementId": "Rls0FoHo",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "SbXwcm3S",
			"type": "arrow",
			"x": 1153.7754496662494,
			"y": -380.9380584037644,
			"width": 176.8894335474622,
			"height": 75.96064893910136,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b2G",
			"roundness": {
				"type": 2
			},
			"seed": 495641098,
			"version": 92,
			"versionNonce": 1417279874,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770680,
			"created": 1790871034121,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					107.13925512950641,
					-23.287090218157175
				],
				[
					176.8894335474622,
					-75.96064893910136
				]
			],
			"startBinding": {
				"elementId": "Rls0FoHo",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "MSofzPtZ",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					1
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "PqHJOj9P",
			"type": "text",
			"x": 648.7376848789138,
			"y": -198.4076863585924,
			"width": 274.53985595703125,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b2h",
			"roundness": null,
			"seed": 1427072342,
			"version": 94,
			"versionNonce": 907128964,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "PDupNevs",
					"type": "arrow"
				},
				{
					"id": "wQa6z1co",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790872298186,
			"locked": false,
			"text": "determine file's type",
			"rawText": "determine file's type",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "determine file's type",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "PDupNevs",
			"type": "arrow",
			"x": 344.39503620482583,
			"y": -769.3242484701658,
			"width": 298.84264867408797,
			"height": 578.4984878194767,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b2j",
			"roundness": {
				"type": 2
			},
			"seed": 1428803978,
			"version": 118,
			"versionNonce": 383828571,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124990,
			"created": 1790872323447,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					123.82691876864465,
					262.78365753904325
				],
				[
					298.84264867408797,
					578.4984878194767
				]
			],
			"startBinding": {
				"elementId": "7_1cj0rG0M09Pa5fcUjM4",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "PqHJOj9P",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "SCQ-UGVoI3IE1J2fzxyeS",
			"type": "rectangle",
			"x": 983.7527953903957,
			"y": -223.25034067749345,
			"width": 446.48868359796296,
			"height": 85.17308657687113,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b2k",
			"roundness": {
				"type": 3
			},
			"seed": 1558961366,
			"version": 298,
			"versionNonce": 1719295876,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "wQa6z1co",
					"type": "arrow"
				},
				{
					"type": "text",
					"id": "yzPIPGEb"
				},
				{
					"id": "yrjDu9Sh",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790872345319,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "yzPIPGEb",
			"type": "text",
			"x": 988.7527953903957,
			"y": -198.1637973890579,
			"width": 431.955810546875,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b2kV",
			"roundness": null,
			"seed": 1212150218,
			"version": 214,
			"versionNonce": 579587844,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790872357714,
			"locked": false,
			"text": "Filenames not reflect file's type",
			"rawText": "Filenames not reflect file's type",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "middle",
			"containerId": "SCQ-UGVoI3IE1J2fzxyeS",
			"originalText": "Filenames not reflect file's type",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "wQa6z1co",
			"type": "arrow",
			"x": 928.777540835945,
			"y": -180.8815492561917,
			"width": 49.475254554450544,
			"height": 0.20363207339082123,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b2m",
			"roundness": {
				"type": 2
			},
			"seed": 754601034,
			"version": 119,
			"versionNonce": 1224503771,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124994,
			"created": 1790872349733,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					49.475254554450544,
					0.20363207339082123
				]
			],
			"startBinding": {
				"elementId": "PqHJOj9P",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "SCQ-UGVoI3IE1J2fzxyeS",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "01YdFQAP",
			"type": "rectangle",
			"x": 1513.6138005969913,
			"y": -211.88742972119348,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b2n",
			"roundness": {
				"type": 3
			},
			"seed": 992168074,
			"version": 387,
			"versionNonce": 752803332,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "NnYQ7rMd"
				},
				{
					"id": "yrjDu9Sh",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790872422798,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "NnYQ7rMd",
			"type": "text",
			"x": 1628.3725817974034,
			"y": -200.47705505098565,
			"width": 42.08396911621094,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b2o",
			"roundness": null,
			"seed": 1702733642,
			"version": 377,
			"versionNonce": 1423736196,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790872422798,
			"locked": false,
			"text": "file",
			"rawText": "file",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "01YdFQAP",
			"originalText": "file",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "yrjDu9Sh",
			"type": "arrow",
			"x": 1435.7414789883587,
			"y": -180.80806413007411,
			"width": 72.37232160863232,
			"height": 2.0104247963035675,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b2p",
			"roundness": {
				"type": 2
			},
			"seed": 553967114,
			"version": 75,
			"versionNonce": 31948411,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124995,
			"created": 1790872428121,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					72.37232160863232,
					-2.0104247963035675
				]
			],
			"startBinding": {
				"elementId": "SCQ-UGVoI3IE1J2fzxyeS",
				"mode": "orbit",
				"fixedPoint": [
					1.0000000000000002,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "01YdFQAP",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "bWWf4fCysrsb72C5PcUXs",
			"type": "rectangle",
			"x": 2646.401792937063,
			"y": 278.4588100202907,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b2q",
			"roundness": {
				"type": 3
			},
			"seed": 277817750,
			"version": 398,
			"versionNonce": 11922564,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "5w1WoXvw"
				}
			],
			"updated": 1791327429679,
			"created": 1790872475802,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "5w1WoXvw",
			"type": "text",
			"x": 2761.160574137475,
			"y": 289.8691846904985,
			"width": 42.08396911621094,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b2r",
			"roundness": null,
			"seed": 1197573846,
			"version": 388,
			"versionNonce": 1741536260,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790872475802,
			"locked": false,
			"text": "file",
			"rawText": "file",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "bWWf4fCysrsb72C5PcUXs",
			"originalText": "file",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "eebMXZ3r79Jpg-vBW_sQq",
			"type": "rectangle",
			"x": 642.9286343919334,
			"y": 23.46316364465099,
			"width": 446.48868359796296,
			"height": 85.17308657687113,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b2t",
			"roundness": {
				"type": 3
			},
			"seed": 758058442,
			"version": 363,
			"versionNonce": 1245682564,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Bu7l2sBv"
				},
				{
					"id": "jxME1U2P",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790872697721,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "Bu7l2sBv",
			"type": "text",
			"x": 690.2070643256806,
			"y": 48.549706933086554,
			"width": 351.93182373046875,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b2u",
			"roundness": null,
			"seed": 1147061386,
			"version": 335,
			"versionNonce": 1380551428,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790872697722,
			"locked": false,
			"text": "Symbolic links & Hard links",
			"rawText": "Symbolic links & Hard links",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "eebMXZ3r79Jpg-vBW_sQq",
			"originalText": "Symbolic links & Hard links",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "jxME1U2P",
			"type": "arrow",
			"x": 344.39503620482583,
			"y": -753.4569879981957,
			"width": 293.0335981871076,
			"height": 809.4658142750134,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b2v",
			"roundness": {
				"type": 2
			},
			"seed": 1447382090,
			"version": 104,
			"versionNonce": 535674619,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124990,
			"created": 1790872718799,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					93.22656694229727,
					444.3857464259918
				],
				[
					293.0335981871076,
					809.4658142750134
				]
			],
			"startBinding": {
				"elementId": "7_1cj0rG0M09Pa5fcUjM4",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "eebMXZ3r79Jpg-vBW_sQq",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "YgY2yAgwHN22eybuHXTev",
			"type": "rectangle",
			"x": 318.5034816226673,
			"y": 563.4561610368962,
			"width": 178,
			"height": 152,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"YCi2oPJ60Z8bbjDDAILYE"
			],
			"frameId": null,
			"index": "b2v4",
			"roundness": {
				"type": 3
			},
			"seed": 1284824918,
			"version": 1048,
			"versionNonce": 492673540,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "lul7FxK8"
				},
				{
					"id": "gd5p5BlK",
					"type": "arrow"
				},
				{
					"id": "6g0fdvzT",
					"type": "arrow"
				},
				{
					"id": "l4noPW38",
					"type": "arrow"
				},
				{
					"id": "KALI8jhO",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790869292780,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "lul7FxK8",
			"type": "text",
			"x": 340.2335078677845,
			"y": 621.9561610368962,
			"width": 134.53994750976562,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"YCi2oPJ60Z8bbjDDAILYE"
			],
			"frameId": null,
			"index": "b2v8",
			"roundness": null,
			"seed": 1823114390,
			"version": 1048,
			"versionNonce": 1042528644,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790869292780,
			"locked": false,
			"text": "Commands",
			"rawText": "Commands",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YgY2yAgwHN22eybuHXTev",
			"originalText": "Commands",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "I28D3N_aEkJfppySELFgM",
			"type": "rectangle",
			"x": 659.4236568671345,
			"y": 213.1382642829733,
			"width": 662.5122723866352,
			"height": 292.65371051511534,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YCi2oPJ60Z8bbjDDAILYE"
			],
			"frameId": null,
			"index": "b2vG",
			"roundness": {
				"type": 3
			},
			"seed": 28277014,
			"version": 1372,
			"versionNonce": 804907268,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "hIPnjNVZ"
				},
				{
					"id": "6g0fdvzT",
					"type": "arrow"
				},
				{
					"id": "4bCd6XSe",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790874542770,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "hIPnjNVZ",
			"type": "text",
			"x": 664.4236568671345,
			"y": 236.96511954053096,
			"width": 619.0517578125,
			"height": 245,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YCi2oPJ60Z8bbjDDAILYE"
			],
			"frameId": null,
			"index": "b2vO",
			"roundness": null,
			"seed": 1590421078,
			"version": 1074,
			"versionNonce": 1985882244,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790874542770,
			"locked": false,
			"text": "4 types of command: \n- executable program: \"/usr/bin\" programs can\nbe compiled binaries or scripting languages\n- command built-in shell: like \"cd\"\n- shell function: miniature shell scripts\nincorporated into the environment \n- alias",
			"rawText": "4 types of command: \n- executable program: \"/usr/bin\" programs can be compiled binaries or scripting languages\n- command built-in shell: like \"cd\"\n- shell function: miniature shell scripts incorporated into the environment \n- alias",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "middle",
			"containerId": "I28D3N_aEkJfppySELFgM",
			"originalText": "4 types of command: \n- executable program: \"/usr/bin\" programs can be compiled binaries or scripting languages\n- command built-in shell: like \"cd\"\n- shell function: miniature shell scripts incorporated into the environment \n- alias",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "6g0fdvzT",
			"type": "arrow",
			"x": 502.5034816226673,
			"y": 629.1604105715461,
			"width": 151.42017524446715,
			"height": 260.214321066726,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YCi2oPJ60Z8bbjDDAILYE"
			],
			"frameId": null,
			"index": "b2vV",
			"roundness": {
				"type": 2
			},
			"seed": 138402186,
			"version": 508,
			"versionNonce": 1325922075,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124995,
			"created": 1790874701093,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					151.42017524446715,
					-260.214321066726
				]
			],
			"startBinding": {
				"elementId": "YgY2yAgwHN22eybuHXTev",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "I28D3N_aEkJfppySELFgM",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "vsBcc2HJ",
			"type": "text",
			"x": 621.7186120244661,
			"y": 660.4543082735125,
			"width": 331.8278503417969,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YCi2oPJ60Z8bbjDDAILYE"
			],
			"frameId": null,
			"index": "b2vd",
			"roundness": null,
			"seed": 1800023766,
			"version": 157,
			"versionNonce": 1745409924,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "l4noPW38",
					"type": "arrow"
				},
				{
					"id": "tVLeUghx",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790874713427,
			"locked": false,
			"text": "display type of command",
			"rawText": "display type of command",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "display type of command",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "w7PLkDCgGpreQCB8T8w4g",
			"type": "rectangle",
			"x": 1034.4811911885117,
			"y": 645.5172647781277,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YCi2oPJ60Z8bbjDDAILYE"
			],
			"frameId": null,
			"index": "b2vl",
			"roundness": {
				"type": 3
			},
			"seed": 9053706,
			"version": 519,
			"versionNonce": 1535854340,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "7fXMrx42"
				},
				{
					"id": "tVLeUghx",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790874727108,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "7fXMrx42",
			"type": "text",
			"x": 1140.083966529549,
			"y": 656.9276394483355,
			"width": 60.39598083496094,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YCi2oPJ60Z8bbjDDAILYE"
			],
			"frameId": null,
			"index": "b2vt",
			"roundness": null,
			"seed": 1697436874,
			"version": 512,
			"versionNonce": 605275780,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790874727108,
			"locked": false,
			"text": "type",
			"rawText": "type",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "w7PLkDCgGpreQCB8T8w4g",
			"originalText": "type",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "l4noPW38",
			"type": "arrow",
			"x": 502.5034816226674,
			"y": 641.3155365984176,
			"width": 113.71513040179872,
			"height": 34.95177741036707,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YCi2oPJ60Z8bbjDDAILYE"
			],
			"frameId": null,
			"index": "b2w",
			"roundness": {
				"type": 2
			},
			"seed": 893761994,
			"version": 148,
			"versionNonce": 1590713275,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124996,
			"created": 1790874732200,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					113.71513040179872,
					34.95177741036707
				]
			],
			"startBinding": {
				"elementId": "YgY2yAgwHN22eybuHXTev",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "vsBcc2HJ",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "tVLeUghx",
			"type": "arrow",
			"x": 953.3885953876311,
			"y": 676.191108394716,
			"width": 75.59259580088064,
			"height": 1.638474041995437,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YCi2oPJ60Z8bbjDDAILYE"
			],
			"frameId": null,
			"index": "b2w8",
			"roundness": {
				"type": 2
			},
			"seed": 699002710,
			"version": 132,
			"versionNonce": 937562523,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124996,
			"created": 1790874734374,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					75.59259580088064,
					-1.638474041995437
				]
			],
			"startBinding": {
				"elementId": "vsBcc2HJ",
				"mode": "inside",
				"fixedPoint": [
					0.9995242503651539,
					0.4496228606058139
				]
			},
			"endBinding": {
				"elementId": "w7PLkDCgGpreQCB8T8w4g",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "cgog6awQ",
			"type": "text",
			"x": 610.535134542992,
			"y": 762.5959744832666,
			"width": 385.8957824707031,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YCi2oPJ60Z8bbjDDAILYE"
			],
			"frameId": null,
			"index": "b2wG",
			"roundness": null,
			"seed": 2051063830,
			"version": 236,
			"versionNonce": 1551738116,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "KALI8jhO",
					"type": "arrow"
				},
				{
					"id": "bb94Wr5m",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790874744875,
			"locked": false,
			"text": "display executable's location",
			"rawText": "display executable's location",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "display executable's location",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "IsewfvWv1_j5WOtCiEmZ-",
			"type": "rectangle",
			"x": 1038.0079945474808,
			"y": 753.0822783515324,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YCi2oPJ60Z8bbjDDAILYE"
			],
			"frameId": null,
			"index": "b2wV",
			"roundness": {
				"type": 3
			},
			"seed": 1858626314,
			"version": 518,
			"versionNonce": 1393190020,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "3p9YTFWr"
				},
				{
					"id": "bb94Wr5m",
					"type": "arrow"
				},
				{
					"id": "4bCd6XSe",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790874774310,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "3p9YTFWr",
			"type": "text",
			"x": 1137.7587801424243,
			"y": 764.4926530217402,
			"width": 72.09996032714844,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YCi2oPJ60Z8bbjDDAILYE"
			],
			"frameId": null,
			"index": "b2wl",
			"roundness": null,
			"seed": 1251701194,
			"version": 508,
			"versionNonce": 1758671876,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790874774311,
			"locked": false,
			"text": "which",
			"rawText": "which",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "IsewfvWv1_j5WOtCiEmZ-",
			"originalText": "which",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "KALI8jhO",
			"type": "arrow",
			"x": 494.91465235742703,
			"y": 642.6872164203656,
			"width": 110.12048218556492,
			"height": 130.8756357875069,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YCi2oPJ60Z8bbjDDAILYE"
			],
			"frameId": null,
			"index": "b2x",
			"roundness": {
				"type": 2
			},
			"seed": 407675862,
			"version": 188,
			"versionNonce": 197359938,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770681,
			"created": 1790874779477,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					110.12048218556492,
					130.8756357875069
				]
			],
			"startBinding": {
				"elementId": "YgY2yAgwHN22eybuHXTev",
				"mode": "inside",
				"fixedPoint": [
					0.9910739928919085,
					0.5212569433122989
				]
			},
			"endBinding": {
				"elementId": "cgog6awQ",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "bb94Wr5m",
			"type": "arrow",
			"x": 996.3964429006282,
			"y": 781.9927875555323,
			"width": 36.111551646852604,
			"height": 0.004901078319790031,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YCi2oPJ60Z8bbjDDAILYE"
			],
			"frameId": null,
			"index": "b2xV",
			"roundness": {
				"type": 2
			},
			"seed": 972977034,
			"version": 159,
			"versionNonce": 1699152130,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770682,
			"created": 1790874785847,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					36.111551646852604,
					0.004901078319790031
				]
			],
			"startBinding": {
				"elementId": "cgog6awQ",
				"mode": "inside",
				"fixedPoint": [
					0.9999106647062941,
					0.5541946592075939
				]
			},
			"endBinding": {
				"elementId": "IsewfvWv1_j5WOtCiEmZ-",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "4bCd6XSe",
			"type": "arrow",
			"x": 1315.1095260645163,
			"y": 774.3164230482826,
			"width": 199.02788815516624,
			"height": 410.9064254393717,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YCi2oPJ60Z8bbjDDAILYE"
			],
			"frameId": null,
			"index": "b2y",
			"roundness": {
				"type": 2
			},
			"seed": 820421130,
			"version": 545,
			"versionNonce": 244508923,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "tXCR8iJb"
				}
			],
			"updated": 1791665124996,
			"created": 1790874815320,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					199.02788815516624,
					-277.98811541343764
				],
				[
					12.326403189253142,
					-410.9064254393717
				]
			],
			"startBinding": {
				"elementId": "IsewfvWv1_j5WOtCiEmZ-",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "I28D3N_aEkJfppySELFgM",
				"mode": "orbit",
				"fixedPoint": [
					0.9999999999999998,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "tXCR8iJb",
			"type": "text",
			"x": 1359.0109804628403,
			"y": 510.88982337383936,
			"width": 274.9878845214844,
			"height": 70,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YCi2oPJ60Z8bbjDDAILYE"
			],
			"frameId": null,
			"index": "b2z",
			"roundness": null,
			"seed": 1634515542,
			"version": 102,
			"versionNonce": 333910532,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790874881545,
			"locked": false,
			"text": "works only for \nexecutable programs",
			"rawText": "works only for \nexecutable programs",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4bCd6XSe",
			"originalText": "works only for \nexecutable programs",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": 0.5,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "qTxe6TzSuJ-OTI1jRjQiE",
			"type": "rectangle",
			"x": 234.15895492272216,
			"y": 1150.184775104853,
			"width": 178,
			"height": 152,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"9_JQ9UZH6Xel_p2xaku47"
			],
			"frameId": null,
			"index": "b3F",
			"roundness": {
				"type": 3
			},
			"seed": 1225792778,
			"version": 1093,
			"versionNonce": 348008836,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "E3o4c8G5"
				},
				{
					"id": "XcVPNBXB",
					"type": "arrow"
				},
				{
					"id": "t2pX68fE",
					"type": "arrow"
				},
				{
					"id": "BIsZKtij",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790875039007,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "E3o4c8G5",
			"type": "text",
			"x": 246.4669993563159,
			"y": 1208.684775104853,
			"width": 153.3839111328125,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"9_JQ9UZH6Xel_p2xaku47"
			],
			"frameId": null,
			"index": "b3G",
			"roundness": null,
			"seed": 937159626,
			"version": 1118,
			"versionNonce": 1015374084,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790875039007,
			"locked": false,
			"text": "Redirection",
			"rawText": "Redirection",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "qTxe6TzSuJ-OTI1jRjQiE",
			"originalText": "Redirection",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "XcVPNBXB",
			"type": "arrow",
			"x": -577.1633894115489,
			"y": 584.7754273409286,
			"width": 805.3223443342711,
			"height": 636.6809987744767,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b3H",
			"roundness": {
				"type": 2
			},
			"seed": 960581462,
			"version": 343,
			"versionNonce": 1927474293,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665804317,
			"created": 1790875044327,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					805.3223443342711,
					636.6809987744767
				]
			],
			"startBinding": {
				"elementId": "qvrFhxju",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "qTxe6TzSuJ-OTI1jRjQiE",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "2hJMOSPNjUvZS0oISlLRz",
			"type": "rectangle",
			"x": -971.6402621852759,
			"y": 916.814296116311,
			"width": 387.0301548687478,
			"height": 158.41683257476905,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"Xqtd31h6i8snSjhI6xinm"
			],
			"frameId": null,
			"index": "b3j",
			"roundness": {
				"type": 3
			},
			"seed": 512375993,
			"version": 1598,
			"versionNonce": 1928497653,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "9YveESuI",
					"type": "arrow"
				},
				{
					"id": "T5SEChUx",
					"type": "arrow"
				}
			],
			"updated": 1791665804318,
			"created": 1790951013154,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "xNBE3NLh",
			"type": "text",
			"x": -909.6240157051762,
			"y": 975.000568685995,
			"width": 258.21588134765625,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"Xqtd31h6i8snSjhI6xinm"
			],
			"frameId": null,
			"index": "b3k",
			"roundness": null,
			"seed": 1562504345,
			"version": 412,
			"versionNonce": 496390325,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665804318,
			"created": 1790951028181,
			"locked": false,
			"text": "Everything is a file",
			"rawText": "Everything is a file",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Everything is a file",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "MDRUeqETIN-g2XnB7ggHL",
			"type": "freedraw",
			"x": -908.9788052733837,
			"y": 1016.1302726247134,
			"width": 265.4777197823672,
			"height": 5.899504884052703,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"Xqtd31h6i8snSjhI6xinm"
			],
			"frameId": null,
			"index": "b3l",
			"roundness": null,
			"seed": 106999767,
			"version": 402,
			"versionNonce": 1750364693,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665804318,
			"created": 1790951038574,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-1.1798829729502813
				],
				[
					3.5397389381517996,
					-2.35976594590079
				],
				[
					11.799009768105293,
					-4.71953189180158
				],
				[
					24.777902509160867,
					-5.899504884052703
				],
				[
					43.656390153569646,
					-5.899504884052703
				],
				[
					66.07443669752911,
					-5.899504884052703
				],
				[
					90.85242922599048,
					-5.899504884052703
				],
				[
					114.45044876220095,
					-5.899504884052703
				],
				[
					141.5881172172625,
					-5.899504884052703
				],
				[
					166.36601972642336,
					-5.899504884052703
				],
				[
					189.96403926263372,
					-5.899504884052703
				],
				[
					207.6625539147916,
					-5.899504884052703
				],
				[
					220.6415366751479,
					-5.899504884052703
				],
				[
					231.26057345100207,
					-5.899504884052703
				],
				[
					239.51993430025607,
					-5.899504884052703
				],
				[
					245.41943918430866,
					-3.5396489188512987
				],
				[
					248.95908810315984,
					-3.5396489188512987
				],
				[
					250.13906109541085,
					-3.5396489188512987
				],
				[
					253.67871001426204,
					-3.5396489188512987
				],
				[
					257.21844895241384,
					-3.5396489188512987
				],
				[
					261.93807086351603,
					-3.5396489188512987
				],
				[
					263.1179538364664,
					-3.5396489188512987
				],
				[
					265.4777197823672,
					-3.5396489188512987
				],
				[
					265.4777197823672,
					-3.5396489188512987
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "9YveESuI",
			"type": "arrow",
			"x": -787.8001081120493,
			"y": 745.9608916063278,
			"width": 9.400931729285844,
			"height": 165.35340450998308,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b3m",
			"roundness": {
				"type": 2
			},
			"seed": 1058874457,
			"version": 445,
			"versionNonce": 1842987003,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791667109588,
			"created": 1790951066813,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					9.400931729285844,
					165.35340450998308
				]
			],
			"startBinding": {
				"elementId": "qvrFhxju",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					1
				]
			},
			"endBinding": {
				"elementId": "2hJMOSPNjUvZS0oISlLRz",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					0
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "Di6CFRLtcvvh7iyihZeJN",
			"type": "rectangle",
			"x": 510.7618748106588,
			"y": 1044.3201740701422,
			"width": 633.7309666570548,
			"height": 291.6056216554613,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"DIqIKmqPm0Q3p1N0AjVes"
			],
			"frameId": null,
			"index": "b3n",
			"roundness": {
				"type": 3
			},
			"seed": 436216535,
			"version": 2015,
			"versionNonce": 301059588,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "wPMuVyIY"
				},
				{
					"id": "BIsZKtij",
					"type": "arrow"
				},
				{
					"id": "T5SEChUx",
					"type": "arrow"
				},
				{
					"id": "3nCNXrdK",
					"type": "arrow"
				},
				{
					"id": "vGjwkon6",
					"type": "arrow"
				},
				{
					"id": "ciEuoENm",
					"type": "arrow"
				},
				{
					"id": "CsC8W0co",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790951133036,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "wPMuVyIY",
			"type": "text",
			"x": 515.7618748106588,
			"y": 1050.1229848978728,
			"width": 561.119873046875,
			"height": 280,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"DIqIKmqPm0Q3p1N0AjVes"
			],
			"frameId": null,
			"index": "b3o",
			"roundness": null,
			"seed": 230928375,
			"version": 2897,
			"versionNonce": 2047962500,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790951133036,
			"locked": false,
			"text": "- programs send results to a tmp file ->\nstandard output ( stdout)\n\n- send status msg to another tmp file ->\nstandard error (stderr)\n\n- commonly take input from facility ->\nstandard input (stdin) ",
			"rawText": "- programs send results to a tmp file -> standard output ( stdout)\n\n- send status msg to another tmp file -> standard error (stderr)\n\n- commonly take input from facility -> standard input (stdin) ",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "middle",
			"containerId": "Di6CFRLtcvvh7iyihZeJN",
			"originalText": "- programs send results to a tmp file -> standard output ( stdout)\n\n- send status msg to another tmp file -> standard error (stderr)\n\n- commonly take input from facility -> standard input (stdin) ",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "BIsZKtij",
			"type": "arrow",
			"x": 418.15895492272216,
			"y": 1224.006460165187,
			"width": 87.1029198879366,
			"height": 31.843592677121478,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b3q",
			"roundness": {
				"type": 2
			},
			"seed": 875082167,
			"version": 139,
			"versionNonce": 116724603,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124997,
			"created": 1790951359210,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					87.1029198879366,
					-31.843592677121478
				]
			],
			"startBinding": {
				"elementId": "qTxe6TzSuJ-OTI1jRjQiE",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "Di6CFRLtcvvh7iyihZeJN",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "T5SEChUx",
			"type": "arrow",
			"x": 814.1460590936647,
			"y": 1341.4257957256036,
			"width": 1582.3781756437,
			"height": 522.8464568423121,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b3r",
			"roundness": {
				"type": 2
			},
			"seed": 1242232343,
			"version": 571,
			"versionNonce": 1347912533,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665804318,
			"created": 1790951363710,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-645.5927353516395,
					262.1517898077884
				],
				[
					-1582.3781756437,
					-260.6946670345237
				]
			],
			"startBinding": {
				"elementId": "Di6CFRLtcvvh7iyihZeJN",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					0.9999999999999996
				]
			},
			"endBinding": {
				"elementId": "2hJMOSPNjUvZS0oISlLRz",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					1
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "i1RVbXHo",
			"type": "text",
			"x": 1301.6993422902772,
			"y": 1140.764027543591,
			"width": 211.847900390625,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b3t",
			"roundness": null,
			"seed": 1225537431,
			"version": 182,
			"versionNonce": 1944628228,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "1QXzhOqp",
					"type": "arrow"
				},
				{
					"id": "InoPTDpJ",
					"type": "arrow"
				},
				{
					"id": "3nCNXrdK",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790951474190,
			"locked": false,
			"text": "redirect stdout",
			"rawText": "redirect stdout",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "redirect stdout",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "3SmNW_TLHU_3ZAksGVVb-",
			"type": "rectangle",
			"x": 1665.74452999149,
			"y": 1086.9313277494655,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"4FI8TuH5E4o3qX3Ib7D7l"
			],
			"frameId": null,
			"index": "b3u",
			"roundness": {
				"type": 3
			},
			"seed": 1619683319,
			"version": 686,
			"versionNonce": 1971096452,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "nxt1eMXh"
				},
				{
					"id": "1QXzhOqp",
					"type": "arrow"
				},
				{
					"id": "77la94At",
					"type": "arrow"
				},
				{
					"id": "4mLrVcPh",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790951489789,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "nxt1eMXh",
			"type": "text",
			"x": 1793.8452988017655,
			"y": 1098.3417024196733,
			"width": 15.399993896484375,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"4FI8TuH5E4o3qX3Ib7D7l"
			],
			"frameId": null,
			"index": "b3v",
			"roundness": null,
			"seed": 1359499543,
			"version": 677,
			"versionNonce": 1751677700,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790951489789,
			"locked": false,
			"text": ">",
			"rawText": ">",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "3SmNW_TLHU_3ZAksGVVb-",
			"originalText": ">",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "b6oXe440KSjT92u9LxKiU",
			"type": "rectangle",
			"x": 1673.3199575770304,
			"y": 1189.9570735577092,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"WOFUDikOZeWBz1Mxtsj7J"
			],
			"frameId": null,
			"index": "b3w",
			"roundness": {
				"type": 3
			},
			"seed": 1790336089,
			"version": 708,
			"versionNonce": 120224388,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "win2A5OL"
				},
				{
					"id": "InoPTDpJ",
					"type": "arrow"
				},
				{
					"id": "WQgKRAV6",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790951494996,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "win2A5OL",
			"type": "text",
			"x": 1793.7207294390637,
			"y": 1201.367448227917,
			"width": 30.79998779296875,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"WOFUDikOZeWBz1Mxtsj7J"
			],
			"frameId": null,
			"index": "b3x",
			"roundness": null,
			"seed": 1144744249,
			"version": 702,
			"versionNonce": 209750532,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790951494996,
			"locked": false,
			"text": ">>",
			"rawText": ">>",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "b6oXe440KSjT92u9LxKiU",
			"originalText": ">>",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "3nCNXrdK",
			"type": "arrow",
			"x": 1149.9928414677136,
			"y": 1189.036635620287,
			"width": 146.2065008225636,
			"height": 29.65359823694439,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b3y",
			"roundness": {
				"type": 2
			},
			"seed": 1517485657,
			"version": 171,
			"versionNonce": 859615419,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124999,
			"created": 1790951509911,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					146.2065008225636,
					-29.65359823694439
				]
			],
			"startBinding": {
				"elementId": "Di6CFRLtcvvh7iyihZeJN",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "i1RVbXHo",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "1QXzhOqp",
			"type": "arrow",
			"x": 1519.047242680902,
			"y": 1156.7345814517644,
			"width": 141.19728731058785,
			"height": 39.35415086533021,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b3z",
			"roundness": {
				"type": 2
			},
			"seed": 1998002841,
			"version": 132,
			"versionNonce": 416450203,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124999,
			"created": 1790951512074,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					141.19728731058785,
					-39.35415086533021
				]
			],
			"startBinding": {
				"elementId": "i1RVbXHo",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "3SmNW_TLHU_3ZAksGVVb-",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "InoPTDpJ",
			"type": "arrow",
			"x": 1519.0472426809022,
			"y": 1160.3538122098598,
			"width": 148.77271489612826,
			"height": 56.433133426722634,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b42",
			"roundness": {
				"type": 2
			},
			"seed": 1806092535,
			"version": 120,
			"versionNonce": 626894971,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665125000,
			"created": 1790951531056,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					148.77271489612826,
					56.433133426722634
				]
			],
			"startBinding": {
				"elementId": "i1RVbXHo",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "b6oXe440KSjT92u9LxKiU",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "28SDz_mPoyfepHPJnuUwm",
			"type": "rectangle",
			"x": 2056.745401402061,
			"y": 1068.9696142547182,
			"width": 449.6394062091264,
			"height": 180.26885151348623,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"XYyZ3XULlkAEJo5Ozp-iE"
			],
			"frameId": null,
			"index": "b43",
			"roundness": {
				"type": 3
			},
			"seed": 1721508025,
			"version": 2490,
			"versionNonce": 54093828,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "H1RSVN4V"
				},
				{
					"id": "77la94At",
					"type": "arrow"
				},
				{
					"id": "WQgKRAV6",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790951538396,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "H1RSVN4V",
			"type": "text",
			"x": 2061.745401402061,
			"y": 1106.6040400114614,
			"width": 434.0838623046875,
			"height": 105,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"XYyZ3XULlkAEJo5Ozp-iE"
			],
			"frameId": null,
			"index": "b44",
			"roundness": null,
			"seed": 1537843609,
			"version": 3456,
			"versionNonce": 1398130564,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790951538396,
			"locked": false,
			"text": " if redirect only stdout \n\n-> error msg sent to the screen",
			"rawText": " if redirect only stdout \n\n-> error msg sent to the screen",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "middle",
			"containerId": "28SDz_mPoyfepHPJnuUwm",
			"originalText": " if redirect only stdout \n\n-> error msg sent to the screen",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "77la94At",
			"type": "arrow",
			"x": 1942.8460615085253,
			"y": 1117.8408808016827,
			"width": 108.39933989353563,
			"height": 39.28778978785431,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b46",
			"roundness": {
				"type": 2
			},
			"seed": 1898928857,
			"version": 161,
			"versionNonce": 1067252539,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124999,
			"created": 1790951605904,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					108.39933989353563,
					39.28778978785431
				]
			],
			"startBinding": {
				"elementId": "3SmNW_TLHU_3ZAksGVVb-",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "28SDz_mPoyfepHPJnuUwm",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "WQgKRAV6",
			"type": "arrow",
			"x": 1948.0902482189379,
			"y": 1222.2377110994648,
			"width": 103.1551531831235,
			"height": 59.92080223773496,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b48",
			"roundness": {
				"type": 2
			},
			"seed": 1203854679,
			"version": 257,
			"versionNonce": 908648731,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665125000,
			"created": 1790951616401,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					103.1551531831235,
					-59.92080223773496
				]
			],
			"startBinding": {
				"elementId": "b6oXe440KSjT92u9LxKiU",
				"mode": "inside",
				"fixedPoint": [
					1.0116669412987953,
					0.5582881216517201
				]
			},
			"endBinding": {
				"elementId": "28SDz_mPoyfepHPJnuUwm",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "y3RQ7S8l",
			"type": "text",
			"x": 1334.9412581917998,
			"y": 1373.1161777880443,
			"width": 202.32791137695312,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b49",
			"roundness": null,
			"seed": 1852203447,
			"version": 94,
			"versionNonce": 1066616324,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "KCt8YGO6",
					"type": "arrow"
				},
				{
					"id": "emL1Spcn",
					"type": "arrow"
				},
				{
					"id": "vGjwkon6",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790951758354,
			"locked": false,
			"text": "redirect stderr",
			"rawText": "redirect stderr",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "redirect stderr",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "vGjwkon6",
			"type": "arrow",
			"x": 1144.152020801925,
			"y": 1184.8821541809461,
			"width": 185.28923738987487,
			"height": 199.80660006382345,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4A",
			"roundness": {
				"type": 2
			},
			"seed": 700782135,
			"version": 120,
			"versionNonce": 1690559876,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790951768569,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					185.28923738987487,
					199.80660006382345
				]
			],
			"startBinding": {
				"elementId": "Di6CFRLtcvvh7iyihZeJN",
				"mode": "inside",
				"fixedPoint": [
					0.9994621997602761,
					0.48202767598520824
				]
			},
			"endBinding": {
				"elementId": "y3RQ7S8l",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "texdSTNFOzPf4jXfimd08",
			"type": "rectangle",
			"x": 691.985545372138,
			"y": 1644.796082187089,
			"width": 414.0436822682237,
			"height": 229.48713857239755,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"Ojo_MAgRxEFW8M8jnM56R"
			],
			"frameId": null,
			"index": "b4B",
			"roundness": {
				"type": 3
			},
			"seed": 416083191,
			"version": 2099,
			"versionNonce": 1773442308,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "slFxvhWJ"
				},
				{
					"id": "KCt8YGO6",
					"type": "arrow"
				},
				{
					"id": "ciEuoENm",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790951777774,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "slFxvhWJ",
			"type": "text",
			"x": 696.985545372138,
			"y": 1672.039651473288,
			"width": 215.54388427734375,
			"height": 175,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"Ojo_MAgRxEFW8M8jnM56R"
			],
			"frameId": null,
			"index": "b4C",
			"roundness": null,
			"seed": 1219638807,
			"version": 3040,
			"versionNonce": 2078495876,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790951777774,
			"locked": false,
			"text": "File descriptor: \n\n- stdin -> 0 \n- stdout -> 1\n- stderr -> 2",
			"rawText": "File descriptor: \n\n- stdin -> 0 \n- stdout -> 1\n- stderr -> 2",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "middle",
			"containerId": "texdSTNFOzPf4jXfimd08",
			"originalText": "File descriptor: \n\n- stdin -> 0 \n- stdout -> 1\n- stderr -> 2",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"text": " ",
			"fontSize": 28,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"id": "42ddaN1f",
			"type": "text",
			"x": 775.527835947639,
			"y": 1601.2132033762998,
			"width": 11.199996948242188,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"roundness": null,
			"seed": 7273,
			"version": 7,
			"versionNonce": 1762534404,
			"updated": 1791327429679,
			"isDeleted": false,
			"groupIds": [],
			"boundElements": [],
			"link": null,
			"locked": false,
			"frameId": null,
			"hasTextLink": false,
			"created": 1790951780524,
			"containerId": null,
			"originalText": " ",
			"rawText": " ",
			"lineHeight": 1.25,
			"autoResize": true,
			"index": "b4D",
			"labelPosition": null,
			"baseFontSize": null
		},
		{
			"id": "ciEuoENm",
			"type": "arrow",
			"x": 830.0621103038113,
			"y": 1341.4257957256036,
			"width": 68.65961555517242,
			"height": 297.8702864614852,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4E",
			"roundness": {
				"type": 2
			},
			"seed": 99662137,
			"version": 157,
			"versionNonce": 2071781723,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124999,
			"created": 1790951822774,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					59.09713942693952,
					137.06550388330584
				],
				[
					68.65961555517242,
					297.8702864614852
				]
			],
			"startBinding": {
				"elementId": "Di6CFRLtcvvh7iyihZeJN",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					1.0000000000000004
				]
			},
			"endBinding": {
				"elementId": "texdSTNFOzPf4jXfimd08",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					0
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "KCt8YGO6",
			"type": "arrow",
			"x": 1435.126768222153,
			"y": 1407.8951885630604,
			"width": 323.59754058179146,
			"height": 347.1146419653862,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4F",
			"roundness": {
				"type": 2
			},
			"seed": 1444236921,
			"version": 81,
			"versionNonce": 1178863035,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665125000,
			"created": 1790951829980,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-134.57215052914785,
					190.6439036826
				],
				[
					-323.59754058179146,
					347.1146419653862
				]
			],
			"startBinding": {
				"elementId": "y3RQ7S8l",
				"mode": "inside",
				"fixedPoint": [
					0.4951640599091622,
					0.9936860221433172
				]
			},
			"endBinding": {
				"elementId": "texdSTNFOzPf4jXfimd08",
				"mode": "orbit",
				"fixedPoint": [
					0.9999999999999999,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "K-5zwvUnvkSC5ciOvQatL",
			"type": "rectangle",
			"x": 1675.8884167481872,
			"y": 1320.1202643426072,
			"width": 297.35793907113344,
			"height": 115,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"QeT5MCYJDBsnQ6qU68r6O"
			],
			"frameId": null,
			"index": "b4G",
			"roundness": {
				"type": 3
			},
			"seed": 552336855,
			"version": 667,
			"versionNonce": 396554884,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "BTIpAtMS"
				},
				{
					"id": "emL1Spcn",
					"type": "arrow"
				},
				{
					"id": "GF8kYgTq",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790951876861,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "BTIpAtMS",
			"type": "text",
			"x": 1690.0694309614883,
			"y": 1325.1202643426072,
			"width": 268.99591064453125,
			"height": 105,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"QeT5MCYJDBsnQ6qU68r6O"
			],
			"frameId": null,
			"index": "b4H",
			"roundness": null,
			"seed": 545008375,
			"version": 720,
			"versionNonce": 1730806276,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790951876861,
			"locked": false,
			"text": "> file_output 2>&1 \nor \n&> file_output",
			"rawText": "> file_output 2>&1 \nor \n&> file_output",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "K-5zwvUnvkSC5ciOvQatL",
			"originalText": "> file_output 2>&1 \nor \n&> file_output",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "emL1Spcn",
			"type": "arrow",
			"x": 1542.7691695687531,
			"y": 1390.1043559593418,
			"width": 127.61924717943407,
			"height": 11.957269788031908,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4I",
			"roundness": {
				"type": 2
			},
			"seed": 1220146233,
			"version": 46,
			"versionNonce": 1020368475,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665125001,
			"created": 1790951915823,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					127.61924717943407,
					-11.957269788031908
				]
			],
			"startBinding": {
				"elementId": "y3RQ7S8l",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "K-5zwvUnvkSC5ciOvQatL",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "240KRtTc",
			"type": "text",
			"x": 2074.570873518928,
			"y": 1352.7418593706996,
			"width": 343.8958435058594,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4J",
			"roundness": null,
			"seed": 349569367,
			"version": 112,
			"versionNonce": 1875661060,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "GF8kYgTq",
					"type": "arrow"
				},
				{
					"id": "yiRLkAr3",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790951929792,
			"locked": false,
			"text": "dispose unwanted output",
			"rawText": "dispose unwanted output",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "dispose unwanted output",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "GF8kYgTq",
			"type": "arrow",
			"x": 1978.7463558193206,
			"y": 1377.2308226133218,
			"width": 90.32451769960767,
			"height": 6.584521513336767,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4K",
			"roundness": {
				"type": 2
			},
			"seed": 2106254807,
			"version": 69,
			"versionNonce": 2024018683,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665125001,
			"created": 1790951968910,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					90.32451769960767,
					-6.584521513336767
				]
			],
			"startBinding": {
				"elementId": "K-5zwvUnvkSC5ciOvQatL",
				"mode": "orbit",
				"fixedPoint": [
					0.9999999999999998,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "240KRtTc",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "S0F8p7TfMpl2DPI_Bsn6G",
			"type": "rectangle",
			"x": 2527.366777901786,
			"y": 1333.7560571149509,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"98bsdHUIbu0OVkYZinp2Z"
			],
			"frameId": null,
			"index": "b4N",
			"roundness": {
				"type": 3
			},
			"seed": 2042898519,
			"version": 673,
			"versionNonce": 1634131972,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "D4nevgRD"
				},
				{
					"id": "yiRLkAr3",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790951980290,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "D4nevgRD",
			"type": "text",
			"x": 2580.3855841266122,
			"y": 1345.1664317851587,
			"width": 165.5639190673828,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"98bsdHUIbu0OVkYZinp2Z"
			],
			"frameId": null,
			"index": "b4O",
			"roundness": null,
			"seed": 837485943,
			"version": 685,
			"versionNonce": 2098478980,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790951980290,
			"locked": false,
			"text": "2> /dev/null",
			"rawText": "2> /dev/null",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "S0F8p7TfMpl2DPI_Bsn6G",
			"originalText": "2> /dev/null",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "yiRLkAr3",
			"type": "arrow",
			"x": 2423.966717024787,
			"y": 1369.8628774880187,
			"width": 97.9000608769993,
			"height": 6.808181745244838,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4P",
			"roundness": {
				"type": 2
			},
			"seed": 1260121113,
			"version": 67,
			"versionNonce": 1514011547,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665125001,
			"created": 1790951991883,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					97.9000608769993,
					-6.808181745244838
				]
			],
			"startBinding": {
				"elementId": "240KRtTc",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "S0F8p7TfMpl2DPI_Bsn6G",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "8jNsSk85",
			"type": "text",
			"x": 1267.3700063742963,
			"y": 951.3320040046101,
			"width": 185.7799072265625,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4R",
			"roundness": null,
			"seed": 1051682617,
			"version": 80,
			"versionNonce": 728051332,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "CJcSkqoW",
					"type": "arrow"
				},
				{
					"id": "CsC8W0co",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790952429188,
			"locked": false,
			"text": "redirect stdin",
			"rawText": "redirect stdin",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "redirect stdin",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "_asaUtB0owH-lTjDmS8uB",
			"type": "rectangle",
			"x": 1665.3491721810149,
			"y": 927.8009567567224,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"os_EE840RbdsJ5ozmvYfV"
			],
			"frameId": null,
			"index": "b4S",
			"roundness": {
				"type": 3
			},
			"seed": 429263001,
			"version": 768,
			"versionNonce": 1061469700,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "P300xo8K"
				},
				{
					"id": "CJcSkqoW",
					"type": "arrow"
				},
				{
					"id": "8hQSZGnX",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790952441228,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "P300xo8K",
			"type": "text",
			"x": 1793.4499409912903,
			"y": 939.2113314269302,
			"width": 15.399993896484375,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"os_EE840RbdsJ5ozmvYfV"
			],
			"frameId": null,
			"index": "b4T",
			"roundness": null,
			"seed": 182160761,
			"version": 760,
			"versionNonce": 1602641284,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790952441228,
			"locked": false,
			"text": "<",
			"rawText": "<",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "_asaUtB0owH-lTjDmS8uB",
			"originalText": "<",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "CsC8W0co",
			"type": "arrow",
			"x": 1149.9928414677136,
			"y": 1180.2459799903984,
			"width": 111.87716490658272,
			"height": 201.50431051614817,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4U",
			"roundness": {
				"type": 2
			},
			"seed": 34161975,
			"version": 87,
			"versionNonce": 2041445883,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124999,
			"created": 1790952447526,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					111.87716490658272,
					-201.50431051614817
				]
			],
			"startBinding": {
				"elementId": "Di6CFRLtcvvh7iyihZeJN",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "8jNsSk85",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "CJcSkqoW",
			"type": "arrow",
			"x": 1458.6499136008588,
			"y": 968.5214070176032,
			"width": 201.1992585801563,
			"height": 11.490196528732213,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4V",
			"roundness": {
				"type": 2
			},
			"seed": 576468663,
			"version": 84,
			"versionNonce": 231854139,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665125001,
			"created": 1790952460220,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					201.1992585801563,
					-11.490196528732213
				]
			],
			"startBinding": {
				"elementId": "8jNsSk85",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "_asaUtB0owH-lTjDmS8uB",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "kYCjqNR6",
			"type": "text",
			"x": 2093.035470503399,
			"y": 922.3258135053468,
			"width": 308.643798828125,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4W",
			"roundness": null,
			"seed": 5224377,
			"version": 68,
			"versionNonce": 675519492,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "8hQSZGnX",
					"type": "arrow"
				},
				{
					"id": "4mLrVcPh",
					"type": "arrow"
				},
				{
					"id": "5rjOAKNk",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790952578967,
			"locked": false,
			"text": "write multi lines to file",
			"rawText": "write multi lines to file",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "write multi lines to file",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "8hQSZGnX",
			"type": "arrow",
			"x": 1942.4507036980503,
			"y": 956.1220336495383,
			"width": 145.0847668053484,
			"height": 15.697640291865468,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4X",
			"roundness": {
				"type": 2
			},
			"seed": 821861911,
			"version": 48,
			"versionNonce": 356651227,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665125001,
			"created": 1790952592399,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					145.0847668053484,
					-15.697640291865468
				]
			],
			"startBinding": {
				"elementId": "_asaUtB0owH-lTjDmS8uB",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "kYCjqNR6",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "4mLrVcPh",
			"type": "arrow",
			"x": 1935.2497765115518,
			"y": 1115.5757681674484,
			"width": 152.28569399184744,
			"height": 169.62038913494746,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4Y",
			"roundness": {
				"type": 2
			},
			"seed": 1825482873,
			"version": 63,
			"versionNonce": 1517280219,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665125000,
			"created": 1790952594767,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					152.28569399184744,
					-169.62038913494746
				]
			],
			"startBinding": {
				"elementId": "3SmNW_TLHU_3ZAksGVVb-",
				"mode": "inside",
				"fixedPoint": [
					0.9922817629736302,
					0.4954007124560202
				]
			},
			"endBinding": {
				"elementId": "kYCjqNR6",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "TP0AnMghsFMoyWCGJuS0m",
			"type": "rectangle",
			"x": 2503.9636606164754,
			"y": 906.3701938429995,
			"width": 424.6252612184404,
			"height": 63.98154200052976,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"KtuZSFvk7Y5lXFBl94AqB"
			],
			"frameId": null,
			"index": "b4Z",
			"roundness": {
				"type": 3
			},
			"seed": 1819235897,
			"version": 910,
			"versionNonce": 1814784644,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "GBjgDq8F"
				},
				{
					"id": "5rjOAKNk",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790952598220,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "GBjgDq8F",
			"type": "text",
			"x": 2542.8863681299927,
			"y": 920.8609648432644,
			"width": 346.77984619140625,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"KtuZSFvk7Y5lXFBl94AqB"
			],
			"frameId": null,
			"index": "b4a",
			"roundness": null,
			"seed": 2088380185,
			"version": 950,
			"versionNonce": 65239556,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790952598220,
			"locked": false,
			"text": "cat >> file_name <<\"EOF\"",
			"rawText": "cat >> file_name <<\"EOF\"",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "TP0AnMghsFMoyWCGJuS0m",
			"originalText": "cat >> file_name <<\"EOF\"",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "5rjOAKNk",
			"type": "arrow",
			"x": 2407.179269331524,
			"y": 939.7507020213037,
			"width": 91.2843912849512,
			"height": 1.3047275397963176,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4b",
			"roundness": {
				"type": 2
			},
			"seed": 1050176023,
			"version": 86,
			"versionNonce": 304168315,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665125002,
			"created": 1790952630223,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					91.2843912849512,
					-1.3047275397963176
				]
			],
			"startBinding": {
				"elementId": "kYCjqNR6",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "TP0AnMghsFMoyWCGJuS0m",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "PpR3rN92Mn0jyqewTgCm-",
			"type": "rectangle",
			"x": 414.7523831727517,
			"y": 1984.6847353789449,
			"width": 178,
			"height": 152,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"X50q9p4HhQqpgwJwKg1dB"
			],
			"frameId": null,
			"index": "b4c",
			"roundness": {
				"type": 3
			},
			"seed": 747700505,
			"version": 1349,
			"versionNonce": 1451739396,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "1LGPu5dh"
				},
				{
					"id": "t2pX68fE",
					"type": "arrow"
				},
				{
					"id": "uiBgWGqm",
					"type": "arrow"
				},
				{
					"id": "L0iXqAKj",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790952655004,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "1LGPu5dh",
			"type": "text",
			"x": 454.08041662001733,
			"y": 2043.1847353789449,
			"width": 99.34393310546875,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"X50q9p4HhQqpgwJwKg1dB"
			],
			"frameId": null,
			"index": "b4d",
			"roundness": null,
			"seed": 1692628473,
			"version": 1395,
			"versionNonce": 1345325188,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790952655004,
			"locked": false,
			"text": "Pipeline",
			"rawText": "Pipeline",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "PpR3rN92Mn0jyqewTgCm-",
			"originalText": "Pipeline",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "t2pX68fE",
			"type": "arrow",
			"x": 324.76438954919894,
			"y": 1308.184775104853,
			"width": 177.41815899707592,
			"height": 670.4999602740918,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4e",
			"roundness": {
				"type": 2
			},
			"seed": 654179033,
			"version": 213,
			"versionNonce": 1566090971,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665124997,
			"created": 1790952671733,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					177.41815899707592,
					670.4999602740918
				]
			],
			"startBinding": {
				"elementId": "qTxe6TzSuJ-OTI1jRjQiE",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					1
				]
			},
			"endBinding": {
				"elementId": "PpR3rN92Mn0jyqewTgCm-",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					0
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "InsAZb3G",
			"type": "text",
			"x": 723.0743111782444,
			"y": 2020.926429596887,
			"width": 440.4398193359375,
			"height": 70,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4f",
			"roundness": null,
			"seed": 878611545,
			"version": 237,
			"versionNonce": 518174596,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "uiBgWGqm",
					"type": "arrow"
				},
				{
					"id": "jxv7CIbk",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790952692106,
			"locked": false,
			"text": "connects stdout of Command A \nto stdin of Command B",
			"rawText": "connects stdout of Command A \nto stdin of Command B",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "connects stdout of Command A \nto stdin of Command B",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "uiBgWGqm",
			"type": "arrow",
			"x": 598.7523831727517,
			"y": 2060.4804862414894,
			"width": 118.82192800549262,
			"height": 4.345894935268461,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4g",
			"roundness": {
				"type": 2
			},
			"seed": 883244953,
			"version": 231,
			"versionNonce": 1337054747,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665125002,
			"created": 1790952718447,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					118.82192800549262,
					-4.345894935268461
				]
			],
			"startBinding": {
				"elementId": "PpR3rN92Mn0jyqewTgCm-",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "InsAZb3G",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "LPnGjxvW_sF3tpPUpVH_x",
			"type": "rectangle",
			"x": 1294.6852987051598,
			"y": 2011.712328477678,
			"width": 459.4720431649654,
			"height": 80,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"7Zor1o96_T8olqOyhP_tW"
			],
			"frameId": null,
			"index": "b4h",
			"roundness": {
				"type": 3
			},
			"seed": 1521812665,
			"version": 835,
			"versionNonce": 368420484,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "maYWI4aV"
				},
				{
					"id": "jxv7CIbk",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790952730255,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "maYWI4aV",
			"type": "text",
			"x": 1354.321375219283,
			"y": 2034.212328477678,
			"width": 340.19989013671875,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"7Zor1o96_T8olqOyhP_tW"
			],
			"frameId": null,
			"index": "b4i",
			"roundness": null,
			"seed": 587597209,
			"version": 872,
			"versionNonce": 1896232452,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790952730255,
			"locked": false,
			"text": "command_A | command_B",
			"rawText": "command_A | command_B",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "LPnGjxvW_sF3tpPUpVH_x",
			"originalText": "command_A | command_B",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "jxv7CIbk",
			"type": "arrow",
			"x": 1169.014130514182,
			"y": 2055.7567744944345,
			"width": 120.17116819097782,
			"height": 3.8597909143031757,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4j",
			"roundness": {
				"type": 2
			},
			"seed": 857303863,
			"version": 150,
			"versionNonce": 107039579,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665125003,
			"created": 1790952748631,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					120.17116819097782,
					-3.8597909143031757
				]
			],
			"startBinding": {
				"elementId": "InsAZb3G",
				"mode": "orbit",
				"fixedPoint": [
					1.0000000000000002,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "LPnGjxvW_sF3tpPUpVH_x",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "8VG42E9Z",
			"type": "text",
			"x": 761.5642518328758,
			"y": 2208.597872405733,
			"width": 375.59185791015625,
			"height": 70,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4l",
			"roundness": null,
			"seed": 918005337,
			"version": 139,
			"versionNonce": 791381252,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "L0iXqAKj",
					"type": "arrow"
				},
				{
					"id": "qMWg0FwC",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790952796254,
			"locked": false,
			"text": "read from stdin and \nOutput to stdout and files",
			"rawText": "read from stdin and \nOutput to stdout and files",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "read from stdin and \nOutput to stdout and files",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "L0iXqAKj",
			"type": "arrow",
			"x": 598.7523831727517,
			"y": 2067.2008386085054,
			"width": 157.3118686601241,
			"height": 170.44487250346356,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4m",
			"roundness": {
				"type": 2
			},
			"seed": 2105391865,
			"version": 68,
			"versionNonce": 478384322,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770689,
			"created": 1790952821950,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					157.3118686601241,
					170.44487250346356
				]
			],
			"startBinding": {
				"elementId": "PpR3rN92Mn0jyqewTgCm-",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "8VG42E9Z",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "e6J13IafxHpnj6OpK1_vx",
			"type": "rectangle",
			"x": 1308.6955484396767,
			"y": 2220.023980379004,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"hDHd-GPrlOQy95hiIwDE9"
			],
			"frameId": null,
			"index": "b4p",
			"roundness": {
				"type": 3
			},
			"seed": 757257049,
			"version": 751,
			"versionNonce": 294196228,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "BANCH90a"
				},
				{
					"id": "qMWg0FwC",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790952828854,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "BANCH90a",
			"type": "text",
			"x": 1421.7183219496592,
			"y": 2231.434355049212,
			"width": 45.55598449707031,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"hDHd-GPrlOQy95hiIwDE9"
			],
			"frameId": null,
			"index": "b4q",
			"roundness": null,
			"seed": 268501049,
			"version": 748,
			"versionNonce": 1081419771,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665125003,
			"created": 1790952828854,
			"locked": false,
			"text": "tee",
			"rawText": "tee",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "e6J13IafxHpnj6OpK1_vx",
			"originalText": "tee",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "qMWg0FwC",
			"type": "arrow",
			"x": 1142.6561097430322,
			"y": 2243.7759348516306,
			"width": 160.5394386966443,
			"height": 4.9931398266176075,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4r",
			"roundness": {
				"type": 2
			},
			"seed": 2031496919,
			"version": 53,
			"versionNonce": 622340226,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770690,
			"created": 1790952834248,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					160.5394386966443,
					4.9931398266176075
				]
			],
			"startBinding": {
				"elementId": "8VG42E9Z",
				"mode": "orbit",
				"fixedPoint": [
					0.9999999999999997,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "e6J13IafxHpnj6OpK1_vx",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "8xUZULoDcQhngc8HD42v3",
			"type": "rectangle",
			"x": -60.18011696797589,
			"y": -1781.6133549143653,
			"width": 178,
			"height": 152,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4s",
			"roundness": {
				"type": 3
			},
			"seed": 794122201,
			"version": 852,
			"versionNonce": 1690559108,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "YSebg4Rn"
				},
				{
					"id": "XpLyv3p8",
					"type": "arrow"
				},
				{
					"id": "F0KE4YF2",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790954810807,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "YSebg4Rn",
			"type": "text",
			"x": -53.89207680684308,
			"y": -1723.1133549143653,
			"width": 165.42391967773438,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b4t",
			"roundness": null,
			"seed": 577696953,
			"version": 865,
			"versionNonce": 1118630404,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790954810807,
			"locked": false,
			"text": "About Shell ",
			"rawText": "About Shell ",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8xUZULoDcQhngc8HD42v3",
			"originalText": "About Shell ",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "C8D2PhmE",
			"type": "text",
			"x": 533.0474395414647,
			"y": -1954.1987686741868,
			"width": 307.15985107421875,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"zBg2qG4CdB0W6pDV0zibK"
			],
			"frameId": null,
			"index": "b5B8",
			"roundness": null,
			"seed": 403025815,
			"version": 1181,
			"versionNonce": 801640836,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790954831719,
			"locked": false,
			"text": "Command from terminal",
			"rawText": "Command from terminal",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Command from terminal",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "8Qmjbz4a",
			"type": "text",
			"x": 522.1950020788661,
			"y": -1814.2418157363409,
			"width": 469.727783203125,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"zBg2qG4CdB0W6pDV0zibK"
			],
			"frameId": null,
			"index": "b5BG",
			"roundness": null,
			"seed": 1962517687,
			"version": 1169,
			"versionNonce": 458440964,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790954831719,
			"locked": false,
			"text": "Shell expand qualifying characters ",
			"rawText": "Shell expand qualifying characters ",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Shell expand qualifying characters ",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "S7FbnvIY",
			"type": "text",
			"x": 616.7719467061443,
			"y": -1661.7457782065326,
			"width": 171.89195251464844,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"zBg2qG4CdB0W6pDV0zibK"
			],
			"frameId": null,
			"index": "b5BV",
			"roundness": null,
			"seed": 905049559,
			"version": 1122,
			"versionNonce": 1556906116,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790954831719,
			"locked": false,
			"text": "OS executes",
			"rawText": "OS executes",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "OS executes",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "cYQoEE7I432dHuQoUdfo1",
			"type": "freedraw",
			"x": 627.6463867268596,
			"y": -1908.2307589695793,
			"width": 6.8212747473901345,
			"height": 47.74905333755237,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"zBg2qG4CdB0W6pDV0zibK"
			],
			"frameId": null,
			"index": "b5Bl",
			"roundness": null,
			"seed": 302195447,
			"version": 1127,
			"versionNonce": 737267716,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790954831719,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					2.273729336725296,
					0
				],
				[
					4.547545410664952,
					3.4106373736949536
				],
				[
					5.68441007902743,
					9.095047452722383
				],
				[
					5.68441007902743,
					14.77945753175004
				],
				[
					5.68441007902743,
					21.600732279140175
				],
				[
					5.68441007902743,
					27.285142358167604
				],
				[
					3.410594005087887,
					32.96955243719526
				],
				[
					2.273729336725296,
					37.517097847860214
				],
				[
					1.1368646683627048,
					42.06464325852494
				],
				[
					1.1368646683627048,
					44.33837259525012
				],
				[
					1.1368646683627048,
					45.47528063222012
				],
				[
					1.1368646683627048,
					47.74905333755237
				],
				[
					1.1368646683627048,
					46.6121453005826
				],
				[
					1.1368646683627048,
					45.47528063222012
				],
				[
					1.1368646683627048,
					44.33837259525012
				],
				[
					-1.1368646683627048,
					44.33837259525012
				],
				[
					-1.1368646683627048,
					44.33837259525012
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "D5JdG7g71sAdnaEKs1Bw2",
			"type": "freedraw",
			"x": 658.8996867969204,
			"y": -1761.347380417201,
			"width": 22.73764031611006,
			"height": 65.93919161160466,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"zBg2qG4CdB0W6pDV0zibK"
			],
			"frameId": null,
			"index": "b5C",
			"roundness": null,
			"seed": 1773251607,
			"version": 1132,
			"versionNonce": 415313796,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790954831719,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					2.2738160739395425,
					0
				],
				[
					3.4106807423022474,
					0
				],
				[
					5.684410079027543,
					2.2737293367251823
				],
				[
					10.231955489692382,
					5.68441007902743
				],
				[
					14.779500900357334,
					13.642549494780269
				],
				[
					20.463910979384764,
					19.326959573807926
				],
				[
					21.60077564774747,
					26.14832105841242
				],
				[
					22.73764031611006,
					30.695779731862785
				],
				[
					22.73764031611006,
					36.38018981089044
				],
				[
					22.73764031611006,
					42.064599889917645
				],
				[
					21.60077564774747,
					48.88596137452214
				],
				[
					19.327046311022173,
					54.5703714535498
				],
				[
					17.053230237082516,
					56.844100790275206
				],
				[
					13.64263623199463,
					61.39164620093993
				],
				[
					12.505684826417678,
					64.80224020602782
				],
				[
					11.368820158055087,
					65.93919161160466
				],
				[
					11.368820158055087,
					65.93919161160466
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "apuvgjTTlGdjEmjOQ095b",
			"type": "rectangle",
			"x": 456.73839745960834,
			"y": -1969.5353662687346,
			"width": 572.0987439958327,
			"height": 349.869255461702,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"zBg2qG4CdB0W6pDV0zibK"
			],
			"frameId": null,
			"index": "b5C8",
			"roundness": {
				"type": 3
			},
			"seed": 53112695,
			"version": 1363,
			"versionNonce": 58236676,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "XpLyv3p8",
					"type": "arrow"
				},
				{
					"id": "xzx8aca4",
					"type": "arrow"
				},
				{
					"id": "Rw9P3xDK",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1790954831719,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "WVHl6zig7HnK8o9j8QkTW",
			"type": "freedraw",
			"x": 619.1692385246135,
			"y": -1879.4183000013052,
			"width": 25.19015325758187,
			"height": 17.011541308193728,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"zBg2qG4CdB0W6pDV0zibK"
			],
			"frameId": null,
			"index": "b5CG",
			"roundness": null,
			"seed": 898042647,
			"version": 37,
			"versionNonce": 345382532,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790954871020,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.32713998532290134,
					0
				],
				[
					0.327139985323015,
					0.32713998532290134
				],
				[
					0.9814449151498366,
					1.6357248857955256
				],
				[
					2.6171698009455895,
					3.2714497715912785
				],
				[
					4.252894686741342,
					4.58003467206413
				],
				[
					5.888619572537095,
					6.215759557859883
				],
				[
					7.197179513828814,
					7.851484443655636
				],
				[
					8.505764414301666,
					8.505764414301439
				],
				[
					8.832904399624567,
					10.141489300097192
				],
				[
					9.487209329451503,
					11.450074200570043
				],
				[
					9.487209329451503,
					13.085799086365796
				],
				[
					9.487209329451503,
					14.721523972161549
				],
				[
					9.487209329451503,
					15.375816422397975
				],
				[
					9.487209329451503,
					16.357248857957302
				],
				[
					9.487209329451503,
					16.684388843280203
				],
				[
					9.487209329451503,
					17.011541308193728
				],
				[
					10.46862928542032,
					17.011541308193728
				],
				[
					12.104354171216073,
					15.375816422397975
				],
				[
					14.394383986838648,
					13.740091536602222
				],
				[
					16.684388843280317,
					11.777214185892944
				],
				[
					18.97441865890289,
					10.468641765010716
				],
				[
					20.610143544698644,
					9.160056864537864
				],
				[
					21.591563500667462,
					8.178624428978537
				],
				[
					22.573008415817412,
					7.19719199341921
				],
				[
					23.88159331629015,
					6.870039528505686
				],
				[
					24.20873330161305,
					6.870039528505686
				],
				[
					24.863013272258968,
					6.870039528505686
				],
				[
					24.863013272258968,
					6.870039528505686
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "aAUawWcm47eDwdBgYbJcl",
			"type": "freedraw",
			"x": 667.0890571770128,
			"y": -1721.0802456925828,
			"width": 29.47778290912197,
			"height": 22.108337181841534,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"zBg2qG4CdB0W6pDV0zibK"
			],
			"frameId": null,
			"index": "b5CV",
			"roundness": null,
			"seed": 11926521,
			"version": 35,
			"versionNonce": 886550020,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790954922219,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.6699403182673223,
					0.6699403182674359
				],
				[
					2.0098209548019668,
					2.0098209548020805
				],
				[
					3.3497527045065,
					2.6798123862392913
				],
				[
					5.35957365930858,
					4.019693022773936
				],
				[
					6.029513977575903,
					6.699505409013227
				],
				[
					6.699505409013227,
					7.369445727280663
				],
				[
					6.699505409013227,
					9.379317795252518
				],
				[
					6.699505409013227,
					12.059079068321807
				],
				[
					6.699505409013227,
					13.399010818026454
				],
				[
					6.699505409013227,
					15.408831772828307
				],
				[
					6.699505409013227,
					16.748763522532954
				],
				[
					6.699505409013227,
					18.758584477335035
				],
				[
					6.699505409013227,
					19.428575908772245
				],
				[
					6.699505409013227,
					20.09851622703968
				],
				[
					6.699505409013227,
					20.76845654530689
				],
				[
					6.699505409013227,
					22.108337181841534
				],
				[
					7.369445727280436,
					21.4383968635741
				],
				[
					10.049258113519727,
					20.76845654530689
				],
				[
					14.068951136293663,
					18.0886441590676
				],
				[
					18.75858447733492,
					14.738891454561099
				],
				[
					22.778277500108857,
					13.399010818026454
				],
				[
					26.12803020461547,
					12.729070499759018
				],
				[
					27.467961954320003,
					11.389138750054599
				],
				[
					28.80784259085476,
					10.719198431787163
				],
				[
					29.47778290912197,
					10.719198431787163
				],
				[
					29.47778290912197,
					10.719198431787163
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "acKsUBlvD7ho7qBCS2Oyw",
			"type": "freedraw",
			"x": 701.7794100228073,
			"y": -1777.391305850014,
			"width": 290.79517918172314,
			"height": 0,
			"angle": 0,
			"strokeColor": "#f08c00",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"zBg2qG4CdB0W6pDV0zibK"
			],
			"frameId": null,
			"index": "b5Cl",
			"roundness": null,
			"seed": 1824356087,
			"version": 27,
			"versionNonce": 87772548,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790954938054,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.8332112586979292,
					0
				],
				[
					3.332908604736531,
					0
				],
				[
					12.498359590303835,
					0
				],
				[
					23.330233093267225,
					0
				],
				[
					37.49507877091128,
					0
				],
				[
					54.1595582246498,
					0
				],
				[
					73.32367145448234,
					0
				],
				[
					94.98754560029761,
					0
				],
				[
					119.98426478090505,
					0
				],
				[
					147.48061773760696,
					0
				],
				[
					177.47666804034702,
					0
				],
				[
					207.4727183430873,
					0
				],
				[
					235.80240969837564,
					0
				],
				[
					258.2994315329447,
					0
				],
				[
					276.6303335040793,
					0
				],
				[
					287.46227057698684,
					0
				],
				[
					289.9619679230252,
					0
				],
				[
					289.9619679230252,
					0
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "hic3HoJITRwxaOG_crcnd",
			"type": "freedraw",
			"x": 240.61075398511662,
			"y": -2208.285846800916,
			"width": 0.0001,
			"height": 0.0001,
			"angle": 0,
			"strokeColor": "#f08c00",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b5D",
			"roundness": null,
			"seed": 706124919,
			"version": 8,
			"versionNonce": 1459551492,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790954940740,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.0001,
					0.0001
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "XpLyv3p8",
			"type": "arrow",
			"x": 123.81988303202412,
			"y": -1707.173181233271,
			"width": 327.41851442758417,
			"height": 85.94879625340286,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b5E",
			"roundness": {
				"type": 2
			},
			"seed": 912930969,
			"version": 74,
			"versionNonce": 1780589883,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665125003,
			"created": 1790954959220,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					327.41851442758417,
					-85.94879625340286
				]
			],
			"startBinding": {
				"elementId": "8xUZULoDcQhngc8HD42v3",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "apuvgjTTlGdjEmjOQ095b",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "F0KE4YF2",
			"type": "arrow",
			"x": -787.4456616312027,
			"y": 420.7092242481808,
			"width": 728.5337500311023,
			"height": 2136.905683969354,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b5F",
			"roundness": {
				"type": 2
			},
			"seed": 2003095673,
			"version": 307,
			"versionNonce": 2041582389,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665804317,
			"created": 1790954968004,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					728.5337500311023,
					-2136.905683969354
				]
			],
			"startBinding": {
				"elementId": "qvrFhxju",
				"mode": "inside",
				"fixedPoint": [
					0.5017963511769858,
					0.002095334271686629
				]
			},
			"endBinding": {
				"elementId": "8xUZULoDcQhngc8HD42v3",
				"mode": "inside",
				"fixedPoint": [
					0.007124749257727263,
					0.43037431048152763
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "xzx8aca4",
			"type": "arrow",
			"x": -422.8268530275587,
			"y": -1596.101826185058,
			"width": 874.0652504871671,
			"height": 314.82388344750075,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b5G",
			"roundness": {
				"type": 2
			},
			"seed": 1372756407,
			"version": 219,
			"versionNonce": 750152580,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1790954983439,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					353.4831754376799,
					-314.82388344750075
				],
				[
					874.0652504871671,
					-199.6804271852061
				]
			],
			"startBinding": {
				"elementId": "BgtGftaI",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "apuvgjTTlGdjEmjOQ095b",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"hasTextLink": false
		},
		{
			"id": "E8npY1lY",
			"type": "rectangle",
			"x": 1157.312755706131,
			"y": -1847.1404658426272,
			"width": 560.4565171534929,
			"height": 87.82356244416769,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b5J",
			"roundness": {
				"type": 3
			},
			"seed": 1011639959,
			"version": 229,
			"versionNonce": 230534159,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "lD7Pmt4i"
				},
				{
					"id": "Rw9P3xDK",
					"type": "arrow"
				}
			],
			"updated": 1792684214682,
			"created": 1790955054432,
			"link": "[[Shell expansion && substitution]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "lD7Pmt4i",
			"type": "text",
			"x": 1224.9651170660804,
			"y": -1820.7286846205434,
			"width": 425.15179443359375,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b5JG",
			"roundness": null,
			"seed": 1834056631,
			"version": 380,
			"versionNonce": 861498819,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792684217155,
			"created": 1790955054432,
			"locked": false,
			"text": "Shell expansion & substitution ",
			"rawText": "Shell expansion & substitution ",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "E8npY1lY",
			"originalText": "Shell expansion & substitution ",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "Rw9P3xDK",
			"type": "arrow",
			"x": 1034.337141455441,
			"y": -1794.9362330368735,
			"width": 117.47561425068966,
			"height": 7.91318780288907,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b5JV",
			"roundness": {
				"type": 2
			},
			"seed": 1831609561,
			"version": 111,
			"versionNonce": 132238541,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792684214682,
			"created": 1790955043917,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					117.47561425068966,
					-7.91318780288907
				]
			],
			"startBinding": {
				"elementId": "apuvgjTTlGdjEmjOQ095b",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "E8npY1lY",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "kuvh8UwcrlyoAaloUwi5c",
			"type": "rectangle",
			"x": -1697.9149046750877,
			"y": -573.63152019881,
			"width": 178,
			"height": 152,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b5K",
			"roundness": {
				"type": 3
			},
			"seed": 1047743512,
			"version": 940,
			"versionNonce": 662862165,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "NkfxeCmh"
				},
				{
					"id": "4I1zwTud",
					"type": "arrow"
				},
				{
					"id": "48RBvvWd",
					"type": "arrow"
				},
				{
					"id": "gIrczonc",
					"type": "arrow"
				},
				{
					"id": "Tp7pMqo3",
					"type": "arrow"
				},
				{
					"id": "76aspaG6",
					"type": "arrow"
				},
				{
					"id": "zeYUQLba",
					"type": "arrow"
				},
				{
					"id": "0eld076r",
					"type": "arrow"
				},
				{
					"id": "96eclTQE",
					"type": "arrow"
				},
				{
					"id": "7XIo5LwO",
					"type": "arrow"
				},
				{
					"id": "f3rc52wS",
					"type": "arrow"
				},
				{
					"id": "fvaIqFFW",
					"type": "arrow"
				},
				{
					"id": "wrUXVHmC",
					"type": "arrow"
				}
			],
			"updated": 1791666063961,
			"created": 1791220648622,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "NkfxeCmh",
			"type": "text",
			"x": -1686.2368651243064,
			"y": -515.13152019881,
			"width": 154.6439208984375,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b5L",
			"roundness": null,
			"seed": 794954008,
			"version": 915,
			"versionNonce": 665040155,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665632628,
			"created": 1791220648622,
			"locked": false,
			"text": "Permissions",
			"rawText": "Permissions",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "kuvh8UwcrlyoAaloUwi5c",
			"originalText": "Permissions",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "4I1zwTud",
			"type": "arrow",
			"x": -792.9258611222859,
			"y": 414.03888069445026,
			"width": 720.9890435528017,
			"height": 904.1311106007464,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b5M",
			"roundness": {
				"type": 2
			},
			"seed": 631869720,
			"version": 418,
			"versionNonce": 617653211,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665813928,
			"created": 1791220658657,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-720.9890435528017,
					-904.1311106007464
				]
			],
			"startBinding": {
				"elementId": "qvrFhxju",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					0
				]
			},
			"endBinding": {
				"elementId": "kuvh8UwcrlyoAaloUwi5c",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "inpvXWUn",
			"type": "text",
			"x": -2292.9974030464195,
			"y": -852.8239434327759,
			"width": 233.2678680419922,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b5N",
			"roundness": null,
			"seed": 470548072,
			"version": 479,
			"versionNonce": 1481590788,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "gIrczonc",
					"type": "arrow"
				},
				{
					"id": "PBUj2Ugf",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1791220697973,
			"locked": false,
			"text": "find identity info",
			"rawText": "find identity info",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "find identity info",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "Q4DbNbC4R85gFcEGc8xRD",
			"type": "rectangle",
			"x": -2730.9289190020127,
			"y": -866.240279800786,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b5O",
			"roundness": {
				"type": 3
			},
			"seed": 1911276904,
			"version": 931,
			"versionNonce": 1253025668,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Si94KchK"
				},
				{
					"id": "PBUj2Ugf",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1791220720100,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "Si94KchK",
			"type": "text",
			"x": -2607.01413957162,
			"y": -854.8299051305781,
			"width": 23.77197265625,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b5P",
			"roundness": null,
			"seed": 371120232,
			"version": 918,
			"versionNonce": 1624774404,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1791220720100,
			"locked": false,
			"text": "id",
			"rawText": "id",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Q4DbNbC4R85gFcEGc8xRD",
			"originalText": "id",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "gIrczonc",
			"type": "arrow",
			"x": -1703.9149046750877,
			"y": -503.216493794774,
			"width": 350.3146303293397,
			"height": 326.97045717503477,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b5Q",
			"roundness": {
				"type": 2
			},
			"seed": 112204648,
			"version": 512,
			"versionNonce": 782198523,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665632628,
			"created": 1791220726158,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-350.3146303293397,
					-326.97045717503477
				]
			],
			"startBinding": {
				"elementId": "kuvh8UwcrlyoAaloUwi5c",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "inpvXWUn",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "PBUj2Ugf",
			"type": "arrow",
			"x": -2298.4974030464195,
			"y": -835.3866987021607,
			"width": 155.32998443855786,
			"height": 1.8711690840983692,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b5S",
			"roundness": {
				"type": 2
			},
			"seed": 1614659352,
			"version": 664,
			"versionNonce": 102841595,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665125005,
			"created": 1791220734724,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-155.32998443855786,
					-1.8711690840983692
				]
			],
			"startBinding": {
				"elementId": "inpvXWUn",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "Q4DbNbC4R85gFcEGc8xRD",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "X2vsx9y875CbiKe0cK4Cz",
			"type": "stickynote",
			"x": -2345.165407518779,
			"y": -1652.6933654014251,
			"width": 338.66158675741593,
			"height": 338.66158675741593,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffdf6b",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b5T",
			"roundness": {
				"type": 2
			},
			"seed": 222957416,
			"version": 956,
			"versionNonce": 2004663899,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "OwmwjlVQ"
				},
				{
					"id": "48RBvvWd",
					"type": "arrow"
				}
			],
			"updated": 1791666240028,
			"created": 1791220820938,
			"link": null,
			"locked": false,
			"baseHeight": 338.66158675741593,
			"hasTextLink": false
		},
		{
			"id": "OwmwjlVQ",
			"type": "text",
			"x": -2329.165407518779,
			"y": -1630.0317786440091,
			"width": 300.2718505859375,
			"height": 280,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b5U",
			"roundness": null,
			"seed": 52683368,
			"version": 982,
			"versionNonce": 1206968001,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791932204996,
			"created": 1791220820938,
			"locked": false,
			"text": "/etc/group: info\nabout groups \n\n/etc/passwd: info\nabout user accounts\n\n/etc/shadow: info\nabout user passwords",
			"rawText": "/etc/group: info about groups \n\n/etc/passwd: info about user accounts\n\n/etc/shadow: info about user passwords",
			"fontSize": 28,
			"baseFontSize": 28,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "middle",
			"containerId": "X2vsx9y875CbiKe0cK4Cz",
			"originalText": "/etc/group: info about groups \n\n/etc/passwd: info about user accounts\n\n/etc/shadow: info about user passwords",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "48RBvvWd",
			"type": "arrow",
			"x": -1695.3230500491984,
			"y": -493.95293635456267,
			"width": 305.68077071216453,
			"height": 977.5729398051575,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b5W",
			"roundness": {
				"type": 2
			},
			"seed": 1169210136,
			"version": 667,
			"versionNonce": 455471861,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791666242109,
			"created": 1791220839831,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-101.84187841495987,
					-540.1409883685611
				],
				[
					-305.68077071216453,
					-977.5729398051575
				]
			],
			"startBinding": {
				"elementId": "kuvh8UwcrlyoAaloUwi5c",
				"mode": "inside",
				"fixedPoint": [
					0.014560981044321656,
					0.5242012095016272
				]
			},
			"endBinding": {
				"elementId": "X2vsx9y875CbiKe0cK4Cz",
				"mode": "orbit",
				"fixedPoint": [
					1.0000000000000002,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "n9eybEgP",
			"type": "rectangle",
			"x": -2393.525676584901,
			"y": -1208.6237187521263,
			"width": 446.48868359796296,
			"height": 85.17308657687113,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b6j",
			"roundness": {
				"type": 3
			},
			"seed": 288252264,
			"version": 352,
			"versionNonce": 111517523,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "06DCFXeU"
				},
				{
					"id": "96eclTQE",
					"type": "arrow"
				},
				{
					"id": "dncqSg6L",
					"type": "arrow"
				}
			],
			"updated": 1791934110561,
			"created": 1791222207646,
			"link": "[[Permission attributes]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "06DCFXeU",
			"type": "text",
			"x": -2316.917260078888,
			"y": -1183.5371754636908,
			"width": 293.2718505859375,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b6j8",
			"roundness": null,
			"seed": 1789785192,
			"version": 263,
			"versionNonce": 456904821,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791666321706,
			"created": 1791222207646,
			"locked": false,
			"text": "Permission attributes",
			"rawText": "Permission attributes",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "n9eybEgP",
			"originalText": "Permission attributes",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "dncqSg6L",
			"type": "arrow",
			"x": -2399.025676584901,
			"y": -1166.0004684349133,
			"width": 91.62065344534722,
			"height": 0.46959283232990856,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b6jG",
			"roundness": {
				"type": 2
			},
			"seed": 1036077416,
			"version": 433,
			"versionNonce": 1479920289,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791221263854,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-91.62065344534722,
					0.46959283232990856
				]
			],
			"startBinding": {
				"elementId": "n9eybEgP",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "mGlRGlvkg4kMT7GGjxe-M",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "96eclTQE",
			"type": "arrow",
			"x": -1703.9149046750877,
			"y": -515.0078491010801,
			"width": 243.44161505343163,
			"height": 617.9161069828873,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b6jV",
			"roundness": {
				"type": 2
			},
			"seed": 674924568,
			"version": 342,
			"versionNonce": 1745413589,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791666244390,
			"created": 1791221051369,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-105.02149720068564,
					-304.4140673209132
				],
				[
					-243.44161505343163,
					-617.9161069828873
				]
			],
			"startBinding": {
				"elementId": "kuvh8UwcrlyoAaloUwi5c",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "9JdqveYh",
			"type": "text",
			"x": -2313.5221875454836,
			"y": -654.6616180937167,
			"width": 233.40789794921875,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b6m",
			"roundness": null,
			"seed": 2047339836,
			"version": 125,
			"versionNonce": 1178325281,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "Tp7pMqo3",
					"type": "arrow"
				},
				{
					"id": "e5x9IQEB",
					"type": "arrow"
				}
			],
			"updated": 1791934332705,
			"created": 1791223145529,
			"locked": false,
			"text": "change file owner",
			"rawText": "change file owner",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "change file owner",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "Tp7pMqo3",
			"type": "arrow",
			"x": -1703.9149046750879,
			"y": -499.80693279632146,
			"width": 370.6993849211774,
			"height": 135.34312374967647,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b6n",
			"roundness": {
				"type": 2
			},
			"seed": 921482500,
			"version": 325,
			"versionNonce": 1571737499,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665632628,
			"created": 1791223161272,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-370.6993849211774,
					-135.34312374967647
				]
			],
			"startBinding": {
				"elementId": "kuvh8UwcrlyoAaloUwi5c",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "9JdqveYh",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "4RuAkxZ1",
			"type": "rectangle",
			"x": -2731.8353182551004,
			"y": -658.3024347873086,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b6o",
			"roundness": {
				"type": 3
			},
			"seed": 246746500,
			"version": 1262,
			"versionNonce": 687738227,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fCkHVnB4"
				},
				{
					"id": "e5x9IQEB",
					"type": "arrow"
				}
			],
			"updated": 1791934332705,
			"created": 1791223178371,
			"link": "[[chown]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "fCkHVnB4",
			"type": "text",
			"x": -2636.4945363222664,
			"y": -646.8920601171008,
			"width": 80.91996765136719,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b6p",
			"roundness": null,
			"seed": 188792068,
			"version": 1246,
			"versionNonce": 935523681,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934332704,
			"created": 1791223178371,
			"locked": false,
			"text": "chown",
			"rawText": "chown",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4RuAkxZ1",
			"originalText": "chown",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "e5x9IQEB",
			"type": "arrow",
			"x": -2319.022187545484,
			"y": -636.8667633506782,
			"width": 135.71159919258116,
			"height": 7.189130565472851,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b6q",
			"roundness": {
				"type": 2
			},
			"seed": 197436604,
			"version": 329,
			"versionNonce": 1377455407,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934332704,
			"created": 1791223185179,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-135.71159919258116,
					7.189130565472851
				]
			],
			"startBinding": {
				"elementId": "9JdqveYh",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "4RuAkxZ1",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "0oxHnFUg",
			"type": "text",
			"x": -2298.4974032188034,
			"y": -464.4413037420114,
			"width": 234.4438934326172,
			"height": 70,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b6t",
			"roundness": null,
			"seed": 1889024956,
			"version": 108,
			"versionNonce": 1447212420,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "76aspaG6",
					"type": "arrow"
				},
				{
					"id": "cNIyYjWY",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1791327284440,
			"locked": false,
			"text": "change file mode \n(permissions)",
			"rawText": "change file mode \n(permissions)",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "change file mode \n(permissions)",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "76aspaG6",
			"type": "arrow",
			"x": -1703.9149046750877,
			"y": -496.49900535402145,
			"width": 354.6386051110985,
			"height": 66.04049633762054,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b6u",
			"roundness": {
				"type": 2
			},
			"seed": 939611068,
			"version": 233,
			"versionNonce": 336077883,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665632629,
			"created": 1791327294725,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-354.6386051110985,
					66.04049633762054
				]
			],
			"startBinding": {
				"elementId": "kuvh8UwcrlyoAaloUwi5c",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "0oxHnFUg",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "UcqMZcix",
			"type": "rectangle",
			"x": -2694.393520408647,
			"y": -453.89584455011146,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b6v",
			"roundness": {
				"type": 3
			},
			"seed": 957432324,
			"version": 1334,
			"versionNonce": 401482884,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "WTyQon2F"
				},
				{
					"id": "cNIyYjWY",
					"type": "arrow"
				},
				{
					"id": "ynzD9GIj",
					"type": "arrow"
				},
				{
					"id": "UvE2CgiC",
					"type": "arrow"
				}
			],
			"updated": 1791327429679,
			"created": 1791327308245,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "WTyQon2F",
			"type": "text",
			"x": -2599.7387354850903,
			"y": -442.48546987990363,
			"width": 82.29196166992188,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b6w",
			"roundness": null,
			"seed": 1965187460,
			"version": 1330,
			"versionNonce": 1530852356,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327429679,
			"created": 1791327308245,
			"locked": false,
			"text": "chmod",
			"rawText": "chmod",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "UcqMZcix",
			"originalText": "chmod",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "cNIyYjWY",
			"type": "arrow",
			"x": -2303.997403218803,
			"y": -429.23718825607847,
			"width": 113.29458567280881,
			"height": 4.060384965176013,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b6x",
			"roundness": {
				"type": 2
			},
			"seed": 1104002820,
			"version": 62,
			"versionNonce": 1233943099,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665125006,
			"created": 1791327342550,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-113.29458567280881,
					4.060384965176013
				]
			],
			"startBinding": {
				"elementId": "0oxHnFUg",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "UcqMZcix",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "v1ENneID",
			"type": "text",
			"x": -3184.6430516285423,
			"y": -591.4117704070018,
			"width": 277.50787353515625,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b6y",
			"roundness": null,
			"seed": 24653188,
			"version": 78,
			"versionNonce": 1490215556,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "ynzD9GIj",
					"type": "arrow"
				},
				{
					"id": "NyhGXiRG",
					"type": "arrow"
				}
			],
			"updated": 1791327457103,
			"created": 1791327359059,
			"locked": false,
			"text": "octal representation",
			"rawText": "octal representation",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "octal representation",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "TL3PhJy4",
			"type": "text",
			"x": -3142.0688307329256,
			"y": -233.19757731800462,
			"width": 316.8758544921875,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b6z",
			"roundness": null,
			"seed": 2074563132,
			"version": 105,
			"versionNonce": 1689588100,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "UvE2CgiC",
					"type": "arrow"
				},
				{
					"id": "CFY9fYq1",
					"type": "arrow"
				}
			],
			"updated": 1791327555587,
			"created": 1791327369528,
			"locked": false,
			"text": "symbolic representation",
			"rawText": "symbolic representation",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "symbolic representation",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "ynzD9GIj",
			"type": "arrow",
			"x": -2699.893520408647,
			"y": -428.82993139724715,
			"width": 201.74165768473904,
			"height": 141.228095417477,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b70",
			"roundness": {
				"type": 2
			},
			"seed": 2124989116,
			"version": 97,
			"versionNonce": 1557918212,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327457104,
			"created": 1791327382968,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-201.74165768473904,
					-141.228095417477
				]
			],
			"startBinding": {
				"elementId": "UcqMZcix",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "v1ENneID",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "UvE2CgiC",
			"type": "arrow",
			"x": -2699.8935204086465,
			"y": -416.1794152781796,
			"width": 119.79945583209155,
			"height": 191.6850654333853,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b72",
			"roundness": {
				"type": 2
			},
			"seed": 1791051580,
			"version": 102,
			"versionNonce": 650364994,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770695,
			"created": 1791327389930,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-119.79945583209155,
					191.6850654333853
				]
			],
			"startBinding": {
				"elementId": "UcqMZcix",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "TL3PhJy4",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "l2QImZe70J57qCXaJ-INe",
			"type": "rectangle",
			"x": -3726.0727456722707,
			"y": -687.5818274835043,
			"width": 389.6869886455845,
			"height": 223.89402040546906,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"06gmSvoPPvhxsxR0OKpsR"
			],
			"frameId": null,
			"index": "b73",
			"roundness": {
				"type": 3
			},
			"seed": 970680324,
			"version": 2166,
			"versionNonce": 1903677060,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "RYaWRxS1"
				},
				{
					"id": "NyhGXiRG",
					"type": "arrow"
				},
				{
					"id": "yeTt205r",
					"type": "arrow"
				}
			],
			"updated": 1791327607781,
			"created": 1791327427064,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "RYaWRxS1",
			"type": "text",
			"x": -3637.461207831412,
			"y": -663.1348172807698,
			"width": 212.4639129638672,
			"height": 175,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"06gmSvoPPvhxsxR0OKpsR"
			],
			"frameId": null,
			"index": "b74",
			"roundness": null,
			"seed": 1706542980,
			"version": 3052,
			"versionNonce": 1923414076,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327455262,
			"created": 1791327427064,
			"locked": false,
			"text": "4 = Read (r)\n\n2= Write (w)\n\n1 = Execute (x)",
			"rawText": "4 = Read (r)\n\n2= Write (w)\n\n1 = Execute (x)",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "l2QImZe70J57qCXaJ-INe",
			"originalText": "4 = Read (r)\n\n2= Write (w)\n\n1 = Execute (x)",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "NyhGXiRG",
			"type": "arrow",
			"x": -3190.143051628542,
			"y": -573.9700385563826,
			"width": 140.74270539814506,
			"height": 1.5806211729657207,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b75",
			"roundness": {
				"type": 2
			},
			"seed": 1982616196,
			"version": 109,
			"versionNonce": 739709316,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327457104,
			"created": 1791327451950,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-140.74270539814506,
					-1.5806211729657207
				]
			],
			"startBinding": {
				"elementId": "v1ENneID",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "l2QImZe70J57qCXaJ-INe",
				"mode": "orbit",
				"fixedPoint": [
					0.9999999999999994,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "4hSXU3m_sdHfrGbzOqHW4",
			"type": "rectangle",
			"x": -3762.04458252174,
			"y": -355.69757719837105,
			"width": 534.7704966722805,
			"height": 280,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"0rYkBJVKr0K0ZK9uN_IHO"
			],
			"frameId": null,
			"index": "b76",
			"roundness": {
				"type": 3
			},
			"seed": 242186940,
			"version": 2449,
			"versionNonce": 473935292,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "hL0nqIdz"
				},
				{
					"id": "CFY9fYq1",
					"type": "arrow"
				},
				{
					"id": "ZGWS8OwX",
					"type": "arrow"
				}
			],
			"updated": 1791327611132,
			"created": 1791327459250,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "hL0nqIdz",
			"type": "text",
			"x": -3740.7568988828652,
			"y": -350.54672956097784,
			"width": 492.19512939453125,
			"height": 269.6983047252136,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"0rYkBJVKr0K0ZK9uN_IHO"
			],
			"frameId": null,
			"index": "b77",
			"roundness": null,
			"seed": 1151910716,
			"version": 3695,
			"versionNonce": 464191292,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327559593,
			"created": 1791327459250,
			"locked": false,
			"text": "u - g - o\nuser(owner) - group - other \n\nu+x -> add x to owner\ng-w -> remove w from group\ngo=rx -> add r,x to group, other.\nRemove other",
			"rawText": "u - g - o\nuser(owner) - group - other \n\nu+x -> add x to owner\ng-w -> remove w from group\ngo=rx -> add r,x to group, other. Remove other",
			"fontSize": 30.82266339716726,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4hSXU3m_sdHfrGbzOqHW4",
			"originalText": "u - g - o\nuser(owner) - group - other \n\nu+x -> add x to owner\ng-w -> remove w from group\ngo=rx -> add r,x to group, other. Remove other",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "CFY9fYq1",
			"type": "arrow",
			"x": -3147.568830732926,
			"y": -215.69249583505734,
			"width": 74.20525511653341,
			"height": 0.021337153739011683,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b78",
			"roundness": {
				"type": 2
			},
			"seed": 1960567556,
			"version": 59,
			"versionNonce": 2036690946,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770696,
			"created": 1791327555587,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-74.20525511653341,
					0.021337153739011683
				]
			],
			"startBinding": {
				"elementId": "TL3PhJy4",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "4hSXU3m_sdHfrGbzOqHW4",
				"mode": "orbit",
				"fixedPoint": [
					0.9999999999999998,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "ny7AGj5s",
			"type": "text",
			"x": -4242.511978925166,
			"y": -417.09128908354234,
			"width": 261.3238525390625,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b79",
			"roundness": null,
			"seed": 2024443908,
			"version": 78,
			"versionNonce": 863670660,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "yeTt205r",
					"type": "arrow"
				},
				{
					"id": "ZGWS8OwX",
					"type": "arrow"
				},
				{
					"id": "vo40sMVu",
					"type": "arrow"
				},
				{
					"id": "aOztxteR",
					"type": "arrow"
				}
			],
			"updated": 1791327840520,
			"created": 1791327595579,
			"locked": false,
			"text": "default permissions",
			"rawText": "default permissions",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "default permissions",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "yeTt205r",
			"type": "arrow",
			"x": -3725.1869233669013,
			"y": -577.8023626809494,
			"width": 250.50120301920242,
			"height": 174.38576286048198,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7A",
			"roundness": {
				"type": 2
			},
			"seed": 1484095492,
			"version": 105,
			"versionNonce": 1229685564,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327614392,
			"created": 1791327607780,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-250.50120301920242,
					174.38576286048198
				]
			],
			"startBinding": {
				"elementId": "l2QImZe70J57qCXaJ-INe",
				"mode": "inside",
				"fixedPoint": [
					0.002273163670278574,
					0.4903188776714348
				]
			},
			"endBinding": {
				"elementId": "ny7AGj5s",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "ZGWS8OwX",
			"type": "arrow",
			"x": -3767.54458252174,
			"y": -220.285502210492,
			"width": 208.14354386436344,
			"height": 174.68636186092917,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7B",
			"roundness": {
				"type": 2
			},
			"seed": 1817482300,
			"version": 70,
			"versionNonce": 1206893500,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327614393,
			"created": 1791327611131,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-208.14354386436344,
					-174.68636186092917
				]
			],
			"startBinding": {
				"elementId": "4hSXU3m_sdHfrGbzOqHW4",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "ny7AGj5s",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "-CEQHoY_K2jPfj-WacQPf",
			"type": "rectangle",
			"x": -4570.548999464584,
			"y": -423.8822386130639,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7C",
			"roundness": {
				"type": 3
			},
			"seed": 1801946940,
			"version": 1428,
			"versionNonce": 1665833860,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "npC1I4re"
				},
				{
					"id": "vo40sMVu",
					"type": "arrow"
				},
				{
					"id": "BLNubeUh",
					"type": "arrow"
				},
				{
					"id": "k5HQahBK",
					"type": "arrow"
				}
			],
			"updated": 1791327678494,
			"created": 1791327618121,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "npC1I4re",
			"type": "text",
			"x": -4474.830219179699,
			"y": -412.4718639428561,
			"width": 80.16397094726562,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7D",
			"roundness": null,
			"seed": 1340817340,
			"version": 1427,
			"versionNonce": 436372796,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327629032,
			"created": 1791327618121,
			"locked": false,
			"text": "umask",
			"rawText": "umask",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "-CEQHoY_K2jPfj-WacQPf",
			"originalText": "umask",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "vo40sMVu",
			"type": "arrow",
			"x": -4248.011978925166,
			"y": -399.13737410307084,
			"width": 45.43548902238308,
			"height": 3.720877254677532,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7E",
			"roundness": {
				"type": 2
			},
			"seed": 1140607292,
			"version": 59,
			"versionNonce": 1398378500,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327626440,
			"created": 1791327623128,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-45.43548902238308,
					3.720877254677532
				]
			],
			"startBinding": {
				"elementId": "ny7AGj5s",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "-CEQHoY_K2jPfj-WacQPf",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "HrLa3h3SJ-RzGms0Q7161",
			"type": "stickynote",
			"x": -4609.128642605779,
			"y": -952.8400396586553,
			"width": 338.66158675741593,
			"height": 338.66158675741593,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffdf6b",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7F",
			"roundness": {
				"type": 2
			},
			"seed": 89008644,
			"version": 879,
			"versionNonce": 1473186948,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "1BvzqhfE"
				},
				{
					"id": "BLNubeUh",
					"type": "arrow"
				}
			],
			"updated": 1791327674666,
			"created": 1791327635608,
			"link": null,
			"locked": false,
			"baseHeight": 338.66158675741593,
			"hasTextLink": false
		},
		{
			"id": "1BvzqhfE",
			"type": "text",
			"x": -4593.128642605779,
			"y": -871.0092462799473,
			"width": 268.71588134765625,
			"height": 175,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7G",
			"roundness": null,
			"seed": 2038581636,
			"version": 997,
			"versionNonce": 608588292,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327666668,
			"created": 1791327635608,
			"locked": false,
			"text": "default permissions:\n\n- files: 0666\n\n- directories: 0777",
			"rawText": "default permissions:\n\n- files: 0666\n\n- directories: 0777",
			"fontSize": 28,
			"baseFontSize": 28,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "middle",
			"containerId": "HrLa3h3SJ-RzGms0Q7161",
			"originalText": "default permissions:\n\n- files: 0666\n\n- directories: 0777",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "BLNubeUh",
			"type": "arrow",
			"x": -4434.866825282339,
			"y": -429.3822386130639,
			"width": 4.751406056632732,
			"height": 179.29621428817552,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7H",
			"roundness": {
				"type": 2
			},
			"seed": 1348591748,
			"version": 41,
			"versionNonce": 404191963,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665125007,
			"created": 1791327673510,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-4.751406056632732,
					-179.29621428817552
				]
			],
			"startBinding": {
				"elementId": "-CEQHoY_K2jPfj-WacQPf",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					0
				]
			},
			"endBinding": {
				"elementId": "HrLa3h3SJ-RzGms0Q7161",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					1.0000000000000002
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"hasTextLink": false,
			"moveMidPointsWithElement": false
		},
		{
			"id": "BfDTra-LmZWTDM6VgHRZt",
			"type": "rectangle",
			"x": -5140.539207083745,
			"y": -524.6900556737248,
			"width": 462.283308907205,
			"height": 255,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"cEK9PvyC5g5CscgPardiS"
			],
			"frameId": null,
			"index": "b7I",
			"roundness": {
				"type": 3
			},
			"seed": 2011486596,
			"version": 2239,
			"versionNonce": 287539844,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "SZ5nYQNG"
				},
				{
					"id": "k5HQahBK",
					"type": "arrow"
				}
			],
			"updated": 1791328056106,
			"created": 1791327675874,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "SZ5nYQNG",
			"type": "text",
			"x": -5120.405487200455,
			"y": -502.1900556737248,
			"width": 422.015869140625,
			"height": 210,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"cEK9PvyC5g5CscgPardiS"
			],
			"frameId": null,
			"index": "b7J",
			"roundness": null,
			"seed": 1419184388,
			"version": 3310,
			"versionNonce": 35164676,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791328056106,
			"created": 1791327675874,
			"locked": false,
			"text": "E.g: umask 0022 \n\n-> remove write from (g,o)\n\ncreate text.txt (default: 666)\n-> 644 ",
			"rawText": "E.g: umask 0022 \n\n-> remove write from (g,o)\n\ncreate text.txt (default: 666)\n-> 644 ",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "BfDTra-LmZWTDM6VgHRZt",
			"originalText": "E.g: umask 0022 \n\n-> remove write from (g,o)\n\ncreate text.txt (default: 666)\n-> 644 ",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "k5HQahBK",
			"type": "arrow",
			"x": -4576.048999464583,
			"y": -395.0783458554337,
			"width": 96.70689871195736,
			"height": 1.9739458307794848,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7K",
			"roundness": {
				"type": 2
			},
			"seed": 673524996,
			"version": 29,
			"versionNonce": 1086304644,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791328056106,
			"created": 1791327678494,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-96.70689871195736,
					-1.9739458307794848
				]
			],
			"startBinding": {
				"elementId": "-CEQHoY_K2jPfj-WacQPf",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "BfDTra-LmZWTDM6VgHRZt",
				"mode": "orbit",
				"fixedPoint": [
					0.9999999999999994,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "wt0hcOPR",
			"type": "text",
			"x": -4447.865681078951,
			"y": 94.9658951619565,
			"width": 250.82386779785156,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7M",
			"roundness": null,
			"seed": 525832252,
			"version": 76,
			"versionNonce": 2115768324,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "aOztxteR",
					"type": "arrow"
				},
				{
					"id": "4HcykM8k",
					"type": "arrow"
				},
				{
					"id": "hWHq7NjI",
					"type": "arrow"
				},
				{
					"id": "GAQNh8KJ",
					"type": "arrow"
				}
			],
			"updated": 1791328240476,
			"created": 1791327833005,
			"locked": false,
			"text": "special permissions",
			"rawText": "special permissions",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "special permissions",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "aOztxteR",
			"type": "arrow",
			"x": -4111.719055720561,
			"y": -376.59128908354234,
			"width": 83.82603502050551,
			"height": 471.8762331857776,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7N",
			"roundness": {
				"type": 2
			},
			"seed": 632382212,
			"version": 95,
			"versionNonce": 481116092,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791327848809,
			"created": 1791327840520,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					4.003277459967649,
					209.9663429421069
				],
				[
					-79.82275756053787,
					471.8762331857776
				]
			],
			"startBinding": {
				"elementId": "ny7AGj5s",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					1
				]
			},
			"endBinding": {
				"elementId": "wt0hcOPR",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "jWi6pxsy",
			"type": "text",
			"x": -5095.807843021905,
			"y": -83.91050312678357,
			"width": 286.8318786621094,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7O",
			"roundness": null,
			"seed": 695419268,
			"version": 60,
			"versionNonce": 1353785788,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "4HcykM8k",
					"type": "arrow"
				},
				{
					"id": "SuL8ZYdq",
					"type": "arrow"
				}
			],
			"updated": 1791328233405,
			"created": 1791327869556,
			"locked": false,
			"text": "setuid bit (4000 | s)",
			"rawText": "setuid bit (4000 | s)",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "setuid bit (4000 | s)",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "hgutb7ib",
			"type": "text",
			"x": -5076.518999144401,
			"y": 195.7753785639507,
			"width": 290.24786376953125,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7P",
			"roundness": null,
			"seed": 84659716,
			"version": 84,
			"versionNonce": 699992836,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "hWHq7NjI",
					"type": "arrow"
				},
				{
					"id": "g4Cm3iJg",
					"type": "arrow"
				}
			],
			"updated": 1791328138474,
			"created": 1791327888060,
			"locked": false,
			"text": "setgid bit (2000 | s)",
			"rawText": "setgid bit (2000 | s)",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "setgid bit (2000 | s)",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "oNhwyKDB",
			"type": "text",
			"x": -5060.015031153713,
			"y": 534.5891136308686,
			"width": 279.243896484375,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7Q",
			"roundness": null,
			"seed": 125681852,
			"version": 194,
			"versionNonce": 1530411452,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "GAQNh8KJ",
					"type": "arrow"
				},
				{
					"id": "0PISQ2Cd",
					"type": "arrow"
				}
			],
			"updated": 1791328361696,
			"created": 1791327927283,
			"locked": false,
			"text": "sticky bit (1000 | t)",
			"rawText": "sticky bit (1000 | t)",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "sticky bit (1000 | t)",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "4HcykM8k",
			"type": "arrow",
			"x": -4453.365681078951,
			"y": 109.74496377315872,
			"width": 350.11028328084376,
			"height": 173.42753551114419,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7R",
			"roundness": {
				"type": 2
			},
			"seed": 702656516,
			"version": 38,
			"versionNonce": 1042123324,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791328233405,
			"created": 1791327941194,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-350.11028328084376,
					-173.42753551114419
				]
			],
			"startBinding": {
				"elementId": "wt0hcOPR",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "jWi6pxsy",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "hWHq7NjI",
			"type": "arrow",
			"x": -4453.365681078951,
			"y": 114.10782075963063,
			"width": 327.4054542959193,
			"height": 97.53263220664594,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7S",
			"roundness": {
				"type": 2
			},
			"seed": 1160552452,
			"version": 86,
			"versionNonce": 608486148,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791328130990,
			"created": 1791327943395,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-327.4054542959193,
					97.53263220664594
				]
			],
			"startBinding": {
				"elementId": "wt0hcOPR",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "hgutb7ib",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "GAQNh8KJ",
			"type": "arrow",
			"x": -4453.365681078951,
			"y": 119.73250147488002,
			"width": 321.90545359038697,
			"height": 425.09700584306654,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7T",
			"roundness": {
				"type": 2
			},
			"seed": 330159876,
			"version": 191,
			"versionNonce": 402760252,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791328361696,
			"created": 1791327945603,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-321.90545359038697,
					425.09700584306654
				]
			],
			"startBinding": {
				"elementId": "wt0hcOPR",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "oNhwyKDB",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "I5-x8RADUVcYuyr6Irm-e",
			"type": "rectangle",
			"x": -5885.319662796284,
			"y": -156.13673887030518,
			"width": 635.9959995042461,
			"height": 188.8854958136077,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"UAzNC3PPg9Mf-47lo2aMF"
			],
			"frameId": null,
			"index": "b7U",
			"roundness": {
				"type": 3
			},
			"seed": 625246780,
			"version": 2519,
			"versionNonce": 1027414844,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "zXXHmFIt"
				},
				{
					"id": "SuL8ZYdq",
					"type": "arrow"
				}
			],
			"updated": 1791328232377,
			"created": 1791328056763,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "zXXHmFIt",
			"type": "text",
			"x": -5868.265571735567,
			"y": -131.69399096350134,
			"width": 601.8878173828125,
			"height": 140,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"UAzNC3PPg9Mf-47lo2aMF"
			],
			"frameId": null,
			"index": "b7V",
			"roundness": null,
			"seed": 1517345468,
			"version": 3597,
			"versionNonce": 2045662140,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791328232377,
			"created": 1791328056763,
			"locked": false,
			"text": "When applied to an executable file, \nit sets the effective user ID from that of\nthe real user (the user actually running the \nprogram) to that of the program's owner",
			"rawText": "When applied to an executable file, \nit sets the effective user ID from that of the real user (the user actually running the \nprogram) to that of the program's owner",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "I5-x8RADUVcYuyr6Irm-e",
			"originalText": "When applied to an executable file, \nit sets the effective user ID from that of the real user (the user actually running the \nprogram) to that of the program's owner",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "SuL8ZYdq",
			"type": "arrow",
			"x": -5101.307843021904,
			"y": -66.23747366802843,
			"width": 142.5158202701341,
			"height": 4.39284179535327,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7W",
			"roundness": {
				"type": 2
			},
			"seed": 245799428,
			"version": 233,
			"versionNonce": 48816828,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791328233405,
			"created": 1791328097310,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-142.5158202701341,
					4.39284179535327
				]
			],
			"startBinding": {
				"elementId": "jWi6pxsy",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "I5-x8RADUVcYuyr6Irm-e",
				"mode": "orbit",
				"fixedPoint": [
					1.0000000000000004,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "S4yCO4-2Rk74RpiBWtEeR",
			"type": "rectangle",
			"x": -6077.13710379491,
			"y": 86.36095138216142,
			"width": 827.8134403718217,
			"height": 255,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"d2mVMqFZ481NG2KMBPKdB"
			],
			"frameId": null,
			"index": "b7X",
			"roundness": {
				"type": 3
			},
			"seed": 1019857852,
			"version": 2661,
			"versionNonce": 1444021052,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "7MvCaSb2"
				},
				{
					"id": "g4Cm3iJg",
					"type": "arrow"
				}
			],
			"updated": 1791328257681,
			"created": 1791328124625,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "7MvCaSb2",
			"type": "text",
			"x": -6067.508276675406,
			"y": 108.86095138216142,
			"width": 808.5557861328125,
			"height": 210,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"d2mVMqFZ481NG2KMBPKdB"
			],
			"frameId": null,
			"index": "b7Y",
			"roundness": null,
			"seed": 898692156,
			"version": 3760,
			"versionNonce": 2011577276,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791328257681,
			"created": 1791328124625,
			"locked": false,
			"text": " changes the effective group ID from the real group ID of\nthe real user to that of the file owner\n\n->  shared directory when members of a common group need\naccess to all the files in the directory, regardless of the\nfile owner's primary group",
			"rawText": " changes the effective group ID from the real group ID of the real user to that of the file owner\n\n->  shared directory when members of a common group need access to all the files in the directory, regardless of the file owner's primary group",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "S4yCO4-2Rk74RpiBWtEeR",
			"originalText": " changes the effective group ID from the real group ID of the real user to that of the file owner\n\n->  shared directory when members of a common group need access to all the files in the directory, regardless of the file owner's primary group",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "riDnCgRTnj_h6IH_H8ujh",
			"type": "rectangle",
			"x": -6077.137104,
			"y": 381.6772332406184,
			"width": 833.3134407098896,
			"height": 359.307605463055,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"D5j4axvyycNz-mxU9RsoE"
			],
			"frameId": null,
			"index": "b7Z",
			"roundness": {
				"type": 3
			},
			"seed": 1295226684,
			"version": 2675,
			"versionNonce": 136936580,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "UUJdYbkq"
				},
				{
					"id": "0PISQ2Cd",
					"type": "arrow"
				}
			],
			"updated": 1791328340925,
			"created": 1791328125285,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "UUJdYbkq",
			"type": "text",
			"x": -6068.197485695837,
			"y": 398.46192015148574,
			"width": 815.4342041015625,
			"height": 325.73823164132034,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"D5j4axvyycNz-mxU9RsoE"
			],
			"frameId": null,
			"index": "b7a",
			"roundness": null,
			"seed": 1035292604,
			"version": 3891,
			"versionNonce": 1804012348,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791328355157,
			"created": 1791328125285,
			"locked": false,
			"text": " - On files, Linux ignores the sticky bit\n\n- If applied to a directory, it prevents users \nfrom deleting or renaming files \n(unless the user is either the owner of the directory, the\nowner of the file, or the superuser) \n\n-> often used to control access to a \nshared directory, such as /tmp",
			"rawText": " - On files, Linux ignores the sticky bit\n\n- If applied to a directory, it prevents users \nfrom deleting or renaming files \n(unless the user is either the owner of the directory, the owner of the file, or the superuser) \n\n-> often used to control access to a \nshared directory, such as /tmp",
			"fontSize": 28.954509479228477,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "riDnCgRTnj_h6IH_H8ujh",
			"originalText": " - On files, Linux ignores the sticky bit\n\n- If applied to a directory, it prevents users \nfrom deleting or renaming files \n(unless the user is either the owner of the directory, the owner of the file, or the superuser) \n\n-> often used to control access to a \nshared directory, such as /tmp",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "g4Cm3iJg",
			"type": "arrow",
			"x": -5082.018999144401,
			"y": 213.29821629718904,
			"width": 161.8046642786876,
			"height": 0.5688973517340514,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7b",
			"roundness": {
				"type": 2
			},
			"seed": 435514500,
			"version": 163,
			"versionNonce": 866083900,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791328257681,
			"created": 1791328138473,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-161.8046642786876,
					0.5688973517340514
				]
			],
			"startBinding": {
				"elementId": "hgutb7ib",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "S4yCO4-2Rk74RpiBWtEeR",
				"mode": "orbit",
				"fixedPoint": [
					1.0000000000000004,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "0PISQ2Cd",
			"type": "arrow",
			"x": -5065.515031153713,
			"y": 552.3701247655044,
			"width": 172.80863213639805,
			"height": 8.719330832551918,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7c",
			"roundness": {
				"type": 2
			},
			"seed": 1823366276,
			"version": 247,
			"versionNonce": 948566716,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791328361697,
			"created": 1791328140435,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-172.80863213639805,
					8.719330832551918
				]
			],
			"startBinding": {
				"elementId": "oNhwyKDB",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "riDnCgRTnj_h6IH_H8ujh",
				"mode": "orbit",
				"fixedPoint": [
					1.0000000000000004,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "AsCDwXU6",
			"type": "text",
			"x": -2283.859734107179,
			"y": -74.78677812084152,
			"width": 215.45993041992188,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7d",
			"roundness": null,
			"seed": 1220136859,
			"version": 106,
			"versionNonce": 1143768443,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "zeYUQLba",
					"type": "arrow"
				},
				{
					"id": "jWSzjcHi",
					"type": "arrow"
				}
			],
			"updated": 1791665533801,
			"created": 1791665458087,
			"locked": false,
			"text": "create new user",
			"rawText": "create new user",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "create new user",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "zeYUQLba",
			"type": "arrow",
			"x": -1703.9149046750877,
			"y": -490.48513007604856,
			"width": 358.98489901216954,
			"height": 426.6649276760091,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7e",
			"roundness": {
				"type": 2
			},
			"seed": 1322064667,
			"version": 180,
			"versionNonce": 697165019,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665632629,
			"created": 1791665475785,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-358.98489901216954,
					426.6649276760091
				]
			],
			"startBinding": {
				"elementId": "kuvh8UwcrlyoAaloUwi5c",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "AsCDwXU6",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "7yfOC2Oo",
			"type": "rectangle",
			"x": -2804.0697194782797,
			"y": -86.19715243507865,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7h",
			"roundness": {
				"type": 3
			},
			"seed": 1205307771,
			"version": 1476,
			"versionNonce": 1776606715,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "0WzFfN8f"
				},
				{
					"id": "jWSzjcHi",
					"type": "arrow"
				}
			],
			"updated": 1791666121322,
			"created": 1791665530982,
			"link": "[[useradd]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "0WzFfN8f",
			"type": "text",
			"x": -2721.272928634313,
			"y": -74.78677776487082,
			"width": 106.00794982910156,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7i",
			"roundness": null,
			"seed": 280928795,
			"version": 1472,
			"versionNonce": 1574917973,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791666121322,
			"created": 1791665530982,
			"locked": false,
			"text": "useradd",
			"rawText": "useradd",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7yfOC2Oo",
			"originalText": "useradd",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "jWSzjcHi",
			"type": "arrow",
			"x": -2289.359734107179,
			"y": -57.28322762629966,
			"width": 237.60845385406583,
			"height": 0.002181441821036856,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7j",
			"roundness": {
				"type": 2
			},
			"seed": 1426342811,
			"version": 146,
			"versionNonce": 1392747701,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791666121322,
			"created": 1791665533801,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-237.60845385406583,
					0.002181441821036856
				]
			],
			"startBinding": {
				"elementId": "AsCDwXU6",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "7yfOC2Oo",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "M4F6gJg2",
			"type": "text",
			"x": -2313.189705079738,
			"y": 96.22385099234049,
			"width": 274.119873046875,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7k",
			"roundness": null,
			"seed": 881825723,
			"version": 104,
			"versionNonce": 500472315,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "0eld076r",
					"type": "arrow"
				},
				{
					"id": "LmA0Xajn",
					"type": "arrow"
				}
			],
			"updated": 1791665652023,
			"created": 1791665595021,
			"locked": false,
			"text": "modify user account",
			"rawText": "modify user account",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "modify user account",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "0eld076r",
			"type": "arrow",
			"x": -1697.5107604286818,
			"y": -505.841694024945,
			"width": 336.0590716041813,
			"height": 610.1977022318752,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7l",
			"roundness": {
				"type": 2
			},
			"seed": 972221371,
			"version": 410,
			"versionNonce": 534301973,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665647126,
			"created": 1791665614438,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-128.182012384588,
					256.00003329190326
				],
				[
					-336.0590716041813,
					610.1977022318752
				]
			],
			"startBinding": {
				"elementId": "kuvh8UwcrlyoAaloUwi5c",
				"mode": "inside",
				"fixedPoint": [
					0.0022704732944148825,
					0.4459856985122696
				]
			},
			"endBinding": {
				"elementId": "M4F6gJg2",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "JvNImhrN",
			"type": "rectangle",
			"x": -2804.069720423333,
			"y": 84.81347661135229,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7o",
			"roundness": {
				"type": 3
			},
			"seed": 690046267,
			"version": 1536,
			"versionNonce": 1116829089,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "1IcbCHdf"
				},
				{
					"id": "LmA0Xajn",
					"type": "arrow"
				}
			],
			"updated": 1791666117894,
			"created": 1791665648770,
			"link": "[[usermod]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "1IcbCHdf",
			"type": "text",
			"x": -2722.9809297624715,
			"y": 96.22385128156012,
			"width": 109.4239501953125,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7p",
			"roundness": null,
			"seed": 1624958427,
			"version": 1534,
			"versionNonce": 1369836091,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791666117894,
			"created": 1791665648770,
			"locked": false,
			"text": "usermod",
			"rawText": "usermod",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "JvNImhrN",
			"originalText": "usermod",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "LmA0Xajn",
			"type": "arrow",
			"x": -2318.689705079738,
			"y": 113.7274082391922,
			"width": 208.2784838265602,
			"height": 0.002167870450264786,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7q",
			"roundness": {
				"type": 2
			},
			"seed": 469501979,
			"version": 82,
			"versionNonce": 108989147,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791666117894,
			"created": 1791665652022,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-208.2784838265602,
					0.002167870450264786
				]
			],
			"startBinding": {
				"elementId": "M4F6gJg2",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "JvNImhrN",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "Ij71GDMi",
			"type": "text",
			"x": -2191.221763959367,
			"y": 234.16558675540762,
			"width": 152.1519317626953,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7s",
			"roundness": null,
			"seed": 567949083,
			"version": 111,
			"versionNonce": 1801978939,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "7XIo5LwO",
					"type": "arrow"
				},
				{
					"id": "GVv3ohvf",
					"type": "arrow"
				}
			],
			"updated": 1791665734941,
			"created": 1791665694353,
			"locked": false,
			"text": "delete user",
			"rawText": "delete user",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "delete user",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "7XIo5LwO",
			"type": "arrow",
			"x": -1703.9149046750877,
			"y": -482.66441818186394,
			"width": 329.6549275215839,
			"height": 723.8424379258201,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7t",
			"roundness": {
				"type": 2
			},
			"seed": 531631675,
			"version": 121,
			"versionNonce": 1883325973,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791665720043,
			"created": 1791665712970,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-162.59003800363598,
					405.17171952698635
				],
				[
					-329.6549275215839,
					723.8424379258201
				]
			],
			"startBinding": {
				"elementId": "kuvh8UwcrlyoAaloUwi5c",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "Ij71GDMi",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "amwHsAIO",
			"type": "rectangle",
			"x": -2797.807019965887,
			"y": 226.49815985981036,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7u",
			"roundness": {
				"type": 3
			},
			"seed": 728357109,
			"version": 1707,
			"versionNonce": 381211867,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "qs3T0QkS"
				},
				{
					"id": "GVv3ohvf",
					"type": "arrow"
				}
			],
			"updated": 1791666116133,
			"created": 1791665724688,
			"link": "[[userdel]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "qs3T0QkS",
			"type": "text",
			"x": -2709.7042293660606,
			"y": 237.9085345300182,
			"width": 95.39595031738281,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7v",
			"roundness": null,
			"seed": 990704213,
			"version": 1713,
			"versionNonce": 2127655477,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791666116133,
			"created": 1791665724688,
			"locked": false,
			"text": "userdel",
			"rawText": "userdel",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "amwHsAIO",
			"originalText": "userdel",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "GVv3ohvf",
			"type": "arrow",
			"x": -2196.721763959367,
			"y": 251.7305785911793,
			"width": 323.9837244894843,
			"height": 3.6222461780012623,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7w",
			"roundness": {
				"type": 2
			},
			"seed": 503007835,
			"version": 220,
			"versionNonce": 145712021,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791666116133,
			"created": 1791665734940,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-323.9837244894843,
					3.6222461780012623
				]
			],
			"startBinding": {
				"elementId": "Ij71GDMi",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "amwHsAIO",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "oKkyM9Fi",
			"type": "text",
			"x": -2272.372248472875,
			"y": 388.35712918722857,
			"width": 191.40792846679688,
			"height": 70,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7y",
			"roundness": null,
			"seed": 1183271445,
			"version": 46,
			"versionNonce": 493760987,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "f3rc52wS",
					"type": "arrow"
				},
				{
					"id": "nRs2PBbf",
					"type": "arrow"
				}
			],
			"updated": 1791665852652,
			"created": 1791665823797,
			"locked": false,
			"text": "change user's \npassword",
			"rawText": "change user's \npassword",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "change user's \npassword",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "f3rc52wS",
			"type": "arrow",
			"x": -1703.9149046750877,
			"y": -480.21008582409587,
			"width": 371.54941533099054,
			"height": 892.3643193409898,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b7z",
			"roundness": {
				"type": 2
			},
			"seed": 2003426965,
			"version": 49,
			"versionNonce": 1446381723,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791667109609,
			"created": 1791665838084,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-156.55328343401789,
					454.16719059726194
				],
				[
					-371.54941533099054,
					892.3643193409898
				]
			],
			"startBinding": {
				"elementId": "kuvh8UwcrlyoAaloUwi5c",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "oKkyM9Fi",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "rgwbs7tS",
			"type": "rectangle",
			"x": -2804.0697204535613,
			"y": 396.2468043451458,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b80",
			"roundness": {
				"type": 3
			},
			"seed": 1804495413,
			"version": 1675,
			"versionNonce": 1103509019,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "86m9ufIW"
				},
				{
					"id": "nRs2PBbf",
					"type": "arrow"
				}
			],
			"updated": 1791666106088,
			"created": 1791665843106,
			"link": "[[passwd]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "86m9ufIW",
			"type": "text",
			"x": -2717.2269319899656,
			"y": 407.6571790153536,
			"width": 97.91595458984375,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b81",
			"roundness": null,
			"seed": 1124948885,
			"version": 1696,
			"versionNonce": 1008774005,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791666106088,
			"created": 1791665843106,
			"locked": false,
			"text": "passwd",
			"rawText": "passwd",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rgwbs7tS",
			"originalText": "passwd",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "nRs2PBbf",
			"type": "arrow",
			"x": -2277.8722484728755,
			"y": 423.4021673644074,
			"width": 249.09594046365055,
			"height": 1.7227555487015138,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b82",
			"roundness": {
				"type": 2
			},
			"seed": 493655035,
			"version": 51,
			"versionNonce": 1648719061,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791666106089,
			"created": 1791665852652,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-249.09594046365055,
					1.7227555487015138
				]
			],
			"startBinding": {
				"elementId": "oKkyM9Fi",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "rgwbs7tS",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "8KwqMYZx",
			"type": "text",
			"x": -2298.0841549059805,
			"y": 554.8571291872286,
			"width": 155.23193359375,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b83",
			"roundness": null,
			"seed": 147708661,
			"version": 16,
			"versionNonce": 1597937877,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "fvaIqFFW",
					"type": "arrow"
				},
				{
					"id": "uSMyygg0",
					"type": "arrow"
				}
			],
			"updated": 1791665920639,
			"created": 1791665902964,
			"locked": false,
			"text": "switch user",
			"rawText": "switch user",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "switch user",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "fvaIqFFW",
			"type": "arrow",
			"x": -1703.9149046750877,
			"y": -477.15278608937535,
			"width": 433.4373166371429,
			"height": 1039.6222851261355,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b84",
			"roundness": {
				"type": 2
			},
			"seed": 302687451,
			"version": 81,
			"versionNonce": 1228946747,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791667109609,
			"created": 1791665908439,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-161.35333226214289,
					550.3099030695727
				],
				[
					-433.4373166371429,
					1039.6222851261355
				]
			],
			"startBinding": {
				"elementId": "kuvh8UwcrlyoAaloUwi5c",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "8KwqMYZx",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "o0mi6hEe",
			"type": "rectangle",
			"x": -2804.069719867623,
			"y": 539.1934732748332,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b85",
			"roundness": {
				"type": 3
			},
			"seed": 1471941435,
			"version": 1711,
			"versionNonce": 1117937697,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "7KWWKN4T"
				},
				{
					"id": "uSMyygg0",
					"type": "arrow"
				}
			],
			"updated": 1791666104047,
			"created": 1791665913157,
			"link": "[[su]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "7KWWKN4T",
			"type": "text",
			"x": -2753.7669170607655,
			"y": 550.603847945041,
			"width": 170.9959259033203,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b86",
			"roundness": null,
			"seed": 1009576923,
			"version": 1743,
			"versionNonce": 624272571,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791666104047,
			"created": 1791665913157,
			"locked": false,
			"text": "su / sudo -u",
			"rawText": "su / sudo -u",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "o0mi6hEe",
			"originalText": "su / sudo -u",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "uSMyygg0",
			"type": "arrow",
			"x": -2303.5841549059805,
			"y": 572.2608762515176,
			"width": 223.3840334446072,
			"height": 4.051493295831619,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b87",
			"roundness": {
				"type": 2
			},
			"seed": 1737963701,
			"version": 46,
			"versionNonce": 1792739195,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791666104022,
			"created": 1791665920639,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-223.3840334446072,
					-4.051493295831619
				]
			],
			"startBinding": {
				"elementId": "8KwqMYZx",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "o0mi6hEe",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "5VF4ufk6",
			"type": "text",
			"x": -2343.880144660739,
			"y": 669.9608919828017,
			"width": 206.52792358398438,
			"height": 70,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b88",
			"roundness": null,
			"seed": 296181237,
			"version": 72,
			"versionNonce": 428021915,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "wrUXVHmC",
					"type": "arrow"
				},
				{
					"id": "EQ0K5hl3",
					"type": "arrow"
				}
			],
			"updated": 1791666094082,
			"created": 1791666051954,
			"locked": false,
			"text": "switch current \nactive group",
			"rawText": "switch current \nactive group",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "switch current \nactive group",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "wrUXVHmC",
			"type": "arrow",
			"x": -1697.3189246968718,
			"y": -500.2145159136826,
			"width": 434.53329637988236,
			"height": 1193.870857517858,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b89",
			"roundness": {
				"type": 2
			},
			"seed": 1280788789,
			"version": 101,
			"versionNonce": 1194210997,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791666072594,
			"created": 1791666063960,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-152,
					612.8000183105469
				],
				[
					-434.53329637988236,
					1193.870857517858
				]
			],
			"startBinding": {
				"elementId": "kuvh8UwcrlyoAaloUwi5c",
				"mode": "inside",
				"fixedPoint": [
					0.0033482021248080734,
					0.48300660713899607
				]
			},
			"endBinding": {
				"elementId": "5VF4ufk6",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "xyKVc2Ry",
			"type": "rectangle",
			"x": -2804.069719869452,
			"y": 682.1401424844689,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b8A",
			"roundness": {
				"type": 3
			},
			"seed": 308659285,
			"version": 1732,
			"versionNonce": 331158427,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "3UI1EFWT"
				},
				{
					"id": "EQ0K5hl3",
					"type": "arrow"
				}
			],
			"updated": 1791666150233,
			"created": 1791666076927,
			"link": "[[newgrp]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "3UI1EFWT",
			"type": "text",
			"x": -2713.628939462497,
			"y": 693.5505171546768,
			"width": 90.719970703125,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b8B",
			"roundness": null,
			"seed": 1714713013,
			"version": 1763,
			"versionNonce": 1605104443,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791666100526,
			"created": 1791666076927,
			"locked": false,
			"text": "newgrp",
			"rawText": "newgrp",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "xyKVc2Ry",
			"originalText": "newgrp",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "EQ0K5hl3",
			"type": "arrow",
			"x": -2343.7189491109343,
			"y": 701.3855512249893,
			"width": 183.24923924148243,
			"height": 9.388950238234997,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b8D",
			"roundness": {
				"type": 2
			},
			"seed": 860095163,
			"version": 58,
			"versionNonce": 232772571,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791666100526,
			"created": 1791666094082,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-183.24923924148243,
					9.388950238234997
				]
			],
			"startBinding": {
				"elementId": "5VF4ufk6",
				"mode": "inside",
				"fixedPoint": [
					0.0007805024473561716,
					0.4489237034598221
				]
			},
			"endBinding": {
				"elementId": "xyKVc2Ry",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "mGlRGlvkg4kMT7GGjxe-M",
			"type": "rectangle",
			"x": -3157.40682478535,
			"y": -1356.8656607002713,
			"width": 661.2604947551022,
			"height": 382.64941975166505,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8T",
			"roundness": {
				"type": 3
			},
			"seed": 1759452264,
			"version": 1966,
			"versionNonce": 1468137761,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "dncqSg6L",
					"type": "arrow"
				}
			],
			"updated": 1791934110561,
			"created": 1791220981916,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "6ilZ5Q35h5gQLfv-X-ZkR",
			"type": "line",
			"x": -2787.7056446091997,
			"y": -1288.9095388647331,
			"width": 0,
			"height": 251.56337582306173,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8U",
			"roundness": {
				"type": 2
			},
			"seed": 834992232,
			"version": 618,
			"versionNonce": 2068172417,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791221069285,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					251.56337582306173
				]
			],
			"startBinding": null,
			"endBinding": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"polygon": false,
			"hasTextLink": false
		},
		{
			"id": "kiilTN4S",
			"type": "text",
			"x": -3014.5077504996825,
			"y": -1300.1283546625534,
			"width": 145.34791564941406,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8V",
			"roundness": null,
			"seed": 1517083240,
			"version": 255,
			"versionNonce": 530912783,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791221112987,
			"locked": false,
			"text": "directories",
			"rawText": "directories",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "directories",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "9CgOMQI7",
			"type": "text",
			"x": -2672.9998207103904,
			"y": -1300.1283547844375,
			"width": 57.2879638671875,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8W",
			"roundness": null,
			"seed": 771144472,
			"version": 266,
			"versionNonce": 1768576609,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791221119976,
			"locked": false,
			"text": "files",
			"rawText": "files",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "files",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "vLQgoyTk",
			"type": "text",
			"x": -3064.935329989183,
			"y": -1241.3925422619957,
			"width": 11.535995483398438,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8X",
			"roundness": null,
			"seed": 687372648,
			"version": 237,
			"versionNonce": 2044034095,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791221138725,
			"locked": false,
			"text": "r",
			"rawText": "r",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "r",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "dxKTJ17n",
			"type": "text",
			"x": -2997.644109421091,
			"y": -1075.624184522442,
			"width": 16.547988891601562,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8Y",
			"roundness": null,
			"seed": 649757208,
			"version": 237,
			"versionNonce": 1433592385,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791221142003,
			"locked": false,
			"text": "x",
			"rawText": "x",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "x",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "6ibgzhsS",
			"type": "text",
			"x": -2897.866159092981,
			"y": -1160.2532838394516,
			"width": 19.40399169921875,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8Z",
			"roundness": null,
			"seed": 353643112,
			"version": 237,
			"versionNonce": 424943183,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791221145909,
			"locked": false,
			"text": "w",
			"rawText": "w",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "w",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "rW7dCepD",
			"type": "text",
			"x": -2762.1898601327543,
			"y": -1236.1577642793438,
			"width": 11.535995483398438,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8a",
			"roundness": null,
			"seed": 1443219560,
			"version": 237,
			"versionNonce": 1816064545,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791221150363,
			"locked": false,
			"text": "r",
			"rawText": "r",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "r",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "nibMWNq8",
			"type": "text",
			"x": -2668.724749651403,
			"y": -1066.0270138964645,
			"width": 16.547988891601562,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8b",
			"roundness": null,
			"seed": 1712915224,
			"version": 237,
			"versionNonce": 821656687,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791221152162,
			"locked": false,
			"text": "x",
			"rawText": "x",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "x",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "kiJ5eMT3",
			"type": "text",
			"x": -2585.3932092293844,
			"y": -1160.2532837512654,
			"width": 19.40399169921875,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8c",
			"roundness": null,
			"seed": 103928088,
			"version": 254,
			"versionNonce": 314443265,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791221154095,
			"locked": false,
			"text": "w",
			"rawText": "w",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "w",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "V4dn0HP8viBynXnmQfTxY",
			"type": "freedraw",
			"x": -3053.0600357978788,
			"y": -1191.6113558991312,
			"width": 50.60294258405247,
			"height": 110.80308907598919,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8d",
			"roundness": null,
			"seed": 1151651352,
			"version": 266,
			"versionNonce": 76420751,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791221166643,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.8724519031397904
				],
				[
					0,
					2.617422273232478
				],
				[
					0,
					7.852200255884327
				],
				[
					0.8724519031397904,
					12.214526335396613
				],
				[
					3.4898076125587068,
					19.194241406234596
				],
				[
					5.234777982651849,
					28.791378750305284
				],
				[
					7.852133692070765,
					41.00587180379512
				],
				[
					12.214459771582824,
					54.09285004233152
				],
				[
					15.704333947955547,
					64.562439289542
				],
				[
					20.939111930607396,
					73.28709144856612
				],
				[
					24.428986106979664,
					79.39435461626454
				],
				[
					26.173956477072352,
					83.7566806957766
				],
				[
					29.663764089631513,
					86.3741029690093
				],
				[
					33.15363826600378,
					90.73642904852136
				],
				[
					34.898608636096924,
					94.22623666108029
				],
				[
					35.77106053923626,
					97.71611083745256
				],
				[
					38.38841624865563,
					99.4610812075457
				],
				[
					40.13338661874877,
					102.07843691696485
				],
				[
					41.8782904250279,
					102.95088882010441
				],
				[
					41.8782904250279,
					103.82340728705776
				],
				[
					42.75074232816769,
					103.82340728705776
				],
				[
					43.62326079512104,
					105.56831109333734
				],
				[
					44.49571269826083,
					105.56831109333734
				],
				[
					46.24061650453996,
					105.56831109333734
				],
				[
					46.24061650453996,
					106.4407629964769
				],
				[
					46.24061650453996,
					107.3132148996167
				],
				[
					47.11306840767975,
					108.18573336656982
				],
				[
					48.85803877777289,
					108.18573336656982
				],
				[
					48.85803877777289,
					109.9306371728494
				],
				[
					50.60294258405247,
					109.9306371728494
				],
				[
					50.60294258405247,
					109.9306371728494
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "UG5tJ5PZll2-vC2GeKsrK",
			"type": "freedraw",
			"x": -3004.201997020106,
			"y": -1098.2575711411907,
			"width": 25.301504573933016,
			"height": 20.939178494420958,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8e",
			"roundness": null,
			"seed": 923940200,
			"version": 254,
			"versionNonce": 1676647905,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791221167592,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.8724519031397904,
					0
				],
				[
					-0.8724519031397904,
					3.4898741763724956
				],
				[
					1.7449038062795807,
					6.107296449605201
				],
				[
					2.617355709419371,
					10.46962252911726
				],
				[
					4.362326079512059,
					12.21452633539684
				],
				[
					6.107229885791639,
					14.831948608629318
				],
				[
					6.97968178893143,
					16.5768524149089
				],
				[
					6.97968178893143,
					18.321756221188252
				],
				[
					7.852200255884327,
					18.321756221188252
				],
				[
					7.852200255884327,
					19.194274688141377
				],
				[
					7.852200255884327,
					20.939178494420958
				],
				[
					5.234777982651849,
					20.939178494420958
				],
				[
					1.7449038062795807,
					19.194274688141377
				],
				[
					-2.6174222732329326,
					19.194274688141377
				],
				[
					-6.979748352744991,
					18.321756221188252
				],
				[
					-11.34207443225705,
					18.321756221188252
				],
				[
					-13.959430141675966,
					18.321756221188252
				],
				[
					-17.44930431804869,
					18.321756221188252
				],
				[
					-17.44930431804869,
					18.321756221188252
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "k9-s-aW3gtR9Q9KGXE8gb",
			"type": "freedraw",
			"x": -2963.8499794723757,
			"y": -1067.9566345422065,
			"width": 58.164704188013275,
			"height": 53.3177159440595,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8f",
			"roundness": null,
			"seed": 1042829592,
			"version": 264,
			"versionNonce": 1254780079,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791221169525,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.6924268919933638,
					0
				],
				[
					2.0772806759800915,
					0
				],
				[
					6.231947685511386,
					-1.3849066127722836
				],
				[
					10.38656186625758,
					-4.154667009531522
				],
				[
					16.618509551768966,
					-6.924374577504977
				],
				[
					20.773123732514705,
					-11.0790415870365
				],
				[
					25.620164805254262,
					-14.541228875788875
				],
				[
					29.774778986,
					-18.69584305653484
				],
				[
					33.236966274752376,
					-21.465603453293852
				],
				[
					36.69915356350475,
					-24.927790742046454
				],
				[
					39.46891396026422,
					-27.69749831001991
				],
				[
					41.546247465029865,
					-30.46725870677892
				],
				[
					43.623528141009956,
					-32.54459221154457
				],
				[
					44.316007861788876,
					-36.00677950029717
				],
				[
					45.00843475378224,
					-37.391659698676676
				],
				[
					47.08571542976233,
					-39.46896678904977
				],
				[
					48.470622042534615,
					-40.85384698742928
				],
				[
					49.85547582652134,
					-42.238700771416006
				],
				[
					50.547902718514706,
					-45.00846116817502
				],
				[
					51.240382439293626,
					-46.39334136655452
				],
				[
					51.240382439293626,
					-47.77822156493403
				],
				[
					51.93280933128699,
					-47.77822156493403
				],
				[
					53.31766311527372,
					-48.47064845692739
				],
				[
					54.010090007267536,
					-51.24040885368663
				],
				[
					54.702569728046,
					-51.932835745679995
				],
				[
					56.77985040402655,
					-52.62526263767336
				],
				[
					56.77985040402655,
					-53.3177159440595
				],
				[
					57.47227729601991,
					-53.3177159440595
				],
				[
					57.47227729601991,
					-53.3177159440595
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "xgR_pypnjGErypJ-Kd0kX",
			"type": "freedraw",
			"x": -2925.7659192960987,
			"y": -1117.8121631975137,
			"width": 24.9277379132609,
			"height": 13.848749155009727,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8g",
			"roundness": null,
			"seed": 1693011816,
			"version": 254,
			"versionNonce": 1860385217,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791221170408,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.6924268919933638,
					0
				],
				[
					0,
					0
				],
				[
					2.769760396759466,
					0
				],
				[
					6.231947685511841,
					0
				],
				[
					9.694134974264216,
					0
				],
				[
					12.463842542237671,
					-1.3848801983795056
				],
				[
					15.233602938996682,
					-2.7697339823662332
				],
				[
					16.618509551768966,
					-2.7697339823662332
				],
				[
					16.618509551768966,
					-3.462187288752375
				],
				[
					17.310936443762785,
					-3.462187288752375
				],
				[
					20.080696840521796,
					-3.462187288752375
				],
				[
					20.77312373251516,
					-2.7697339823662332
				],
				[
					22.157977516501887,
					0
				],
				[
					22.157977516501887,
					2.7697603967592386
				],
				[
					22.157977516501887,
					6.231947685511614
				],
				[
					22.85040440849525,
					8.309254775884483
				],
				[
					23.54288412927417,
					9.694134974263989
				],
				[
					24.235311021267535,
					10.386561866257352
				],
				[
					24.235311021267535,
					10.386561866257352
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "H3njf-KqLnhRuLUIGhXPu",
			"type": "freedraw",
			"x": -2733.9607646307254,
			"y": -1214.753407282583,
			"width": 142.64205290205973,
			"height": 55.39499662003982,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8h",
			"roundness": null,
			"seed": 1753277720,
			"version": 261,
			"versionNonce": 1331101391,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791221240687,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.6923740632078079,
					0
				],
				[
					4.847041072739103,
					0
				],
				[
					13.848749155009955,
					0
				],
				[
					22.850457237280807,
					0
				],
				[
					35.31435260830358,
					1.3848801983795056
				],
				[
					46.39328853776897,
					4.154640595138744
				],
				[
					56.77985040402655,
					7.616827883891347
				],
				[
					67.85889199106305,
					11.079015172643722
				],
				[
					78.24545385732017,
					15.23362935338946
				],
				[
					88.63201572357775,
					20.08069684052157
				],
				[
					98.32609786905641,
					24.235311021267535
				],
				[
					108.02028567210573,
					28.38995161640605
				],
				[
					115.63703431281874,
					32.54456579715202
				],
				[
					123.25388861110241,
					37.3916332842839
				],
				[
					128.7934094046209,
					40.8538205730365
				],
				[
					132.94797075658107,
					42.93112766340937
				],
				[
					135.71778398212564,
					46.393314952161745
				],
				[
					137.10263776611237,
					49.163075348920984
				],
				[
					139.179971270878,
					49.85550224091435
				],
				[
					139.87234533408582,
					52.62526263767336
				],
				[
					140.5648250548652,
					52.62526263767336
				],
				[
					140.5648250548652,
					53.31768952966695
				],
				[
					140.5648250548652,
					54.702569728046456
				],
				[
					141.94967883885192,
					54.702569728046456
				],
				[
					141.94967883885192,
					55.39499662003982
				],
				[
					141.94967883885192,
					55.39499662003982
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "usgHQGISodeKjJfl2K0d3",
			"type": "freedraw",
			"x": -2590.6262320078868,
			"y": -1171.8222796191737,
			"width": 11.771415650244307,
			"height": 16.618509551768966,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8i",
			"roundness": null,
			"seed": 1496674920,
			"version": 256,
			"versionNonce": 884496801,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791221242878,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1.3848537839867276,
					0
				],
				[
					-1.3848537839867276,
					1.3848801983795056
				],
				[
					-0.6923740632082627,
					2.769760396759011
				],
				[
					-0.6923740632082627,
					4.847067487132108
				],
				[
					-0.6923740632082627,
					8.309254775884483
				],
				[
					-1.3848537839867276,
					9.001681667877847
				],
				[
					-1.3848537839867276,
					11.771442064637085
				],
				[
					-1.3848537839867276,
					13.156322263016591
				],
				[
					-2.0772278471949903,
					15.23362935338946
				],
				[
					-2.0772278471949903,
					15.926056245382824
				],
				[
					-2.7697075679734553,
					16.618509551768966
				],
				[
					-2.7697075679734553,
					15.926056245382824
				],
				[
					-3.4621872887528298,
					14.541176047003319
				],
				[
					-4.847041072739557,
					13.848749155009955
				],
				[
					-6.231894856726285,
					13.156322263016591
				],
				[
					-8.309228361491932,
					13.156322263016591
				],
				[
					-8.309228361491932,
					12.46386895663045
				],
				[
					-9.69408214547866,
					11.078988758250944
				],
				[
					-10.38656186625758,
					11.078988758250944
				],
				[
					-11.771415650244307,
					11.078988758250944
				],
				[
					-11.771415650244307,
					11.078988758250944
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "95_xNsYbEkxStJMX2hLxt",
			"type": "freedraw",
			"x": -2598.9354603693787,
			"y": -1141.3550209123948,
			"width": 256.89428625967685,
			"height": 0,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8j",
			"roundness": null,
			"seed": 762928744,
			"version": 257,
			"versionNonce": 1422675183,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791221245496,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.6923740632078079,
					0
				],
				[
					-1.3848537839867276,
					0
				],
				[
					-2.0773335047656474,
					0
				],
				[
					-4.154561351960183,
					0
				],
				[
					-5.539520793518022,
					0
				],
				[
					-10.38656186625758,
					0
				],
				[
					-15.926082659775602,
					0
				],
				[
					-24.927685084475343,
					0
				],
				[
					-38.7764342394853,
					0
				],
				[
					-55.394996620039365,
					0
				],
				[
					-74.7832665685678,
					0
				],
				[
					-98.32609786905641,
					0
				],
				[
					-124.63874239508914,
					0
				],
				[
					-150.2589072003434,
					0
				],
				[
					-177.26397861836995,
					0
				],
				[
					-201.49928963963703,
					0
				],
				[
					-223.65726715613891,
					0
				],
				[
					-239.58334981591452,
					0
				],
				[
					-250.66233857416546,
					0
				],
				[
					-256.2018593676835,
					0
				],
				[
					-256.89428625967685,
					0
				],
				[
					-256.89428625967685,
					0
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "ut6jhaEPT6oQ-Y2en0Wth",
			"type": "freedraw",
			"x": -2844.7507578708046,
			"y": -1148.2793954898998,
			"width": 11.771415650244307,
			"height": 12.46386895663045,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8k",
			"roundness": null,
			"seed": 1078233192,
			"version": 254,
			"versionNonce": 1721662849,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791221246217,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.6924268919933638,
					0
				],
				[
					-1.3848537839867276,
					0
				],
				[
					-4.154614180745739,
					0.6924268919933638
				],
				[
					-6.924374577505205,
					2.077307090373097
				],
				[
					-8.309228361491932,
					3.4621872887526024
				],
				[
					-9.001655253485296,
					4.154614180745966
				],
				[
					-11.078988758250944,
					5.539494379125472
				],
				[
					-11.078988758250944,
					6.231921271118836
				],
				[
					-11.078988758250944,
					6.924374577504977
				],
				[
					-11.078988758250944,
					7.616801469498341
				],
				[
					-11.078988758250944,
					9.69410855987121
				],
				[
					-9.694134974264216,
					9.69410855987121
				],
				[
					-9.001655253485296,
					10.386561866257352
				],
				[
					-6.924374577505205,
					11.078988758250944
				],
				[
					-4.847041072739557,
					12.46386895663045
				],
				[
					-2.769760396759011,
					12.46386895663045
				],
				[
					-2.0772806759800915,
					12.46386895663045
				],
				[
					-1.3848537839867276,
					12.46386895663045
				],
				[
					-1.3848537839867276,
					12.46386895663045
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "L2zhqX3igl06KBS6N2X72",
			"type": "freedraw",
			"x": -2738.9455836795614,
			"y": -1183.3055803295476,
			"width": 70.09527297247041,
			"height": 114.28571428571422,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8l",
			"roundness": null,
			"seed": 1367213109,
			"version": 28,
			"versionNonce": 917690127,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791666296500,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-1.5238444010417425
				],
				[
					0,
					2.2856794084821104
				],
				[
					2.2857375372022943,
					8.380940755208258
				],
				[
					6.857154482886926,
					19.047619047619037
				],
				[
					13.714308965773853,
					34.28571428571422
				],
				[
					20.57146344866078,
					49.523809523809405
				],
				[
					28.190511067708485,
					63.99995349702385
				],
				[
					35.80955868675619,
					76.19047619047615
				],
				[
					41.14286876860115,
					83.04757254464289
				],
				[
					47.238130115327294,
					90.6666201636906
				],
				[
					51.809547061011926,
					97.52377464657752
				],
				[
					56.38096400669656,
					102.85714285714289
				],
				[
					58.66670154389885,
					106.66666666666674
				],
				[
					60.952380952380736,
					109.7142392113094
				],
				[
					64.00001162574426,
					110.4761904761906
				],
				[
					64.76190476190459,
					112.76186988467248
				],
				[
					66.28574916294656,
					112.76186988467248
				],
				[
					67.04764229910734,
					112.76186988467248
				],
				[
					67.80953543526812,
					112.76186988467248
				],
				[
					68.57142857142844,
					112.76186988467248
				],
				[
					70.09527297247041,
					112.76186988467248
				],
				[
					70.09527297247041,
					112.76186988467248
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "FX9_89l8crHrWMqV2onwI",
			"type": "freedraw",
			"x": -2739.707476815722,
			"y": -1174.1627464381786,
			"width": 15.238095238094957,
			"height": 9.142833891369037,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"F_XIysil63U59ILz5HjCj"
			],
			"frameId": null,
			"index": "b8m",
			"roundness": null,
			"seed": 521603739,
			"version": 22,
			"versionNonce": 1674913121,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791934110560,
			"created": 1791666307951,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1.5237862723211038,
					0
				],
				[
					-1.5237862723211038,
					-1.5237862723215585
				],
				[
					-1.5237862723211038,
					-3.0476306733630736
				],
				[
					-1.5237862723211038,
					-3.809523809523853
				],
				[
					-1.5237862723211038,
					-5.333310081845184
				],
				[
					-0.7618931361607792,
					-5.333310081845184
				],
				[
					-0.7618931361607792,
					-6.857154482886926
				],
				[
					-0.7618931361607792,
					-7.619047619047706
				],
				[
					-0.7618931361607792,
					-8.380940755208258
				],
				[
					-0.7618931361607792,
					-9.142833891369037
				],
				[
					2.285737537202749,
					-8.380940755208258
				],
				[
					6.095261346726147,
					-6.095261346726147
				],
				[
					8.380940755208485,
					-5.333310081845184
				],
				[
					11.428571428571558,
					-4.571416945684632
				],
				[
					13.714308965773853,
					-4.571416945684632
				],
				[
					13.714308965773853,
					-4.571416945684632
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "EOcfMQ9O",
			"type": "rectangle",
			"x": -1589.186746196343,
			"y": 517.2280751266479,
			"width": 178,
			"height": 152,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b8n",
			"roundness": {
				"type": 3
			},
			"seed": 1406782523,
			"version": 1061,
			"versionNonce": 2116643663,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "rrYag5ky"
				},
				{
					"id": "wsUiAAMQ",
					"type": "arrow"
				}
			],
			"updated": 1792684151548,
			"created": 1791667081048,
			"link": "[[Vim]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "rrYag5ky",
			"type": "text",
			"x": -1521.172730998589,
			"y": 575.7280751266479,
			"width": 41.97196960449219,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b8o",
			"roundness": null,
			"seed": 1357548763,
			"version": 1032,
			"versionNonce": 836270509,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792684151548,
			"created": 1791667081048,
			"locked": false,
			"text": "Vim",
			"rawText": "Vim",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "EOcfMQ9O",
			"originalText": "Vim",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "wsUiAAMQ",
			"type": "arrow",
			"x": -999.2010772170524,
			"y": 580.2215221276523,
			"width": 405.9856689792905,
			"height": 12.832109222823533,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b8p",
			"roundness": {
				"type": 2
			},
			"seed": 615749461,
			"version": 106,
			"versionNonce": 223788045,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792684151549,
			"created": 1791667097145,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-405.9856689792905,
					12.832109222823533
				]
			],
			"startBinding": {
				"elementId": "qvrFhxju",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "EOcfMQ9O",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "OA6uLLBq",
			"type": "text",
			"x": 613.9723026743419,
			"y": -1158.1709451804065,
			"width": 167.38392639160156,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b8q",
			"roundness": null,
			"seed": 863050743,
			"version": 122,
			"versionNonce": 1552563609,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "fSoX4a1o",
					"type": "arrow"
				},
				{
					"id": "Y9AzBf0w",
					"type": "arrow"
				}
			],
			"updated": 1791850292855,
			"created": 1791850255132,
			"locked": false,
			"text": "create a file",
			"rawText": "create a file",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "create a file",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "fSoX4a1o",
			"type": "arrow",
			"x": 336.96779613079536,
			"y": -784.6424449046492,
			"width": 271.50450654354654,
			"height": 348.956026828537,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b8r",
			"roundness": {
				"type": 2
			},
			"seed": 614941143,
			"version": 119,
			"versionNonce": 729883257,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791850292855,
			"created": 1791850268509,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					271.50450654354654,
					-348.956026828537
				]
			],
			"startBinding": {
				"elementId": "7_1cj0rG0M09Pa5fcUjM4",
				"mode": "inside",
				"fixedPoint": [
					0.9919817973369075,
					0.4830928613089095
				]
			},
			"endBinding": {
				"elementId": "OA6uLLBq",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "ySeff8IGYp2AQmJVPrnW1",
			"type": "rectangle",
			"x": 841.6566277596628,
			"y": -1170.8786003738546,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b8s",
			"roundness": {
				"type": 3
			},
			"seed": 575778233,
			"version": 373,
			"versionNonce": 2036208343,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8icr88ij"
				},
				{
					"id": "Y9AzBf0w",
					"type": "arrow"
				}
			],
			"updated": 1791850279466,
			"created": 1791850272322,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "8icr88ij",
			"type": "text",
			"x": 938.6494101197429,
			"y": -1159.4682257036468,
			"width": 77.615966796875,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b8t",
			"roundness": null,
			"seed": 52792985,
			"version": 365,
			"versionNonce": 1351591191,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791850276093,
			"created": 1791850272322,
			"locked": false,
			"text": "touch",
			"rawText": "touch",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ySeff8IGYp2AQmJVPrnW1",
			"originalText": "touch",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "Y9AzBf0w",
			"type": "arrow",
			"x": 786.8562290659435,
			"y": -1140.7855620025168,
			"width": 49.300398693719444,
			"height": 1.0587648040855129,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b8u",
			"roundness": {
				"type": 2
			},
			"seed": 1321142391,
			"version": 89,
			"versionNonce": 1208511321,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1791850292856,
			"created": 1791850278075,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					49.300398693719444,
					-1.0587648040855129
				]
			],
			"startBinding": {
				"elementId": "OA6uLLBq",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "ySeff8IGYp2AQmJVPrnW1",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "ZDdzTYu4",
			"type": "rectangle",
			"x": -2311.94794253763,
			"y": 955.4595845787965,
			"width": 178,
			"height": 152,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b8v",
			"roundness": {
				"type": 3
			},
			"seed": 1677645551,
			"version": 1254,
			"versionNonce": 478548255,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "zxO7v21L"
				},
				{
					"id": "qThcCr3r",
					"type": "arrow"
				},
				{
					"id": "9X52cqwV",
					"type": "arrow"
				}
			],
			"updated": 1792945756300,
			"created": 1791931971080,
			"link": "[[Package Management (apt)]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "zxO7v21L",
			"type": "text",
			"x": -2304.357915682161,
			"y": 996.4595845787965,
			"width": 162.8199462890625,
			"height": 70,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b8w",
			"roundness": null,
			"seed": 319037711,
			"version": 1263,
			"versionNonce": 1780628830,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945756300,
			"created": 1791931971080,
			"locked": false,
			"text": "Package\nManagement",
			"rawText": "Package Management",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ZDdzTYu4",
			"originalText": "Package Management",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "qThcCr3r",
			"type": "arrow",
			"x": -999.2010772170523,
			"y": 582.4063380319832,
			"width": 1128.7468653205774,
			"height": 446.69398686631064,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b8x",
			"roundness": {
				"type": 2
			},
			"seed": 1084143809,
			"version": 225,
			"versionNonce": 1139728798,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945756300,
			"created": 1791931985776,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1128.7468653205774,
					446.69398686631064
				]
			],
			"startBinding": {
				"elementId": "qvrFhxju",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "ZDdzTYu4",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "c9aMk0yU",
			"type": "text",
			"x": -3840.374621066589,
			"y": 872.8961132955974,
			"width": 525.1677856445312,
			"height": 105,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b91",
			"roundness": null,
			"seed": 818683663,
			"version": 294,
			"versionNonce": 1025310174,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "4dvpEG4m",
					"type": "arrow"
				}
			],
			"updated": 1792945756300,
			"created": 1791932219850,
			"locked": false,
			"text": "low-level tools (dpkg/rpm)\n-> Handle tasks such as installing and \nremoving package",
			"rawText": "low-level tools (dpkg/rpm)\n-> Handle tasks such as installing and \nremoving package",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "low-level tools (dpkg/rpm)\n-> Handle tasks such as installing and \nremoving package",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "yyOhs4CC",
			"type": "text",
			"x": -3904.23817020211,
			"y": 1200.7903776926205,
			"width": 671.523681640625,
			"height": 70,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b92",
			"roundness": null,
			"seed": 1857100321,
			"version": 332,
			"versionNonce": 1522373150,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "YR8VPcrF",
					"type": "arrow"
				}
			],
			"updated": 1792945756300,
			"created": 1791932266778,
			"locked": false,
			"text": "high-level tools (apt/ dnf)\n-> metadata searching and dependency resolution",
			"rawText": "high-level tools (apt/ dnf)\n-> metadata searching and dependency resolution",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "high-level tools (apt/ dnf)\n-> metadata searching and dependency resolution",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "IgZ76x4iMgL1UYGihfc7D",
			"type": "rectangle",
			"x": -2995.4383480936153,
			"y": 911.9679567894284,
			"width": 470.5625442609373,
			"height": 318.2594309963568,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"cdmaHzGtXlfS9gI2TyLeK"
			],
			"frameId": null,
			"index": "b95",
			"roundness": {
				"type": 3
			},
			"seed": 1542229743,
			"version": 2458,
			"versionNonce": 1472306782,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Mq2urxzA"
				},
				{
					"id": "9X52cqwV",
					"type": "arrow"
				},
				{
					"id": "4dvpEG4m",
					"type": "arrow"
				},
				{
					"id": "YR8VPcrF",
					"type": "arrow"
				}
			],
			"updated": 1792945756300,
			"created": 1791933273472,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "Mq2urxzA",
			"type": "text",
			"x": -2990.4383480936153,
			"y": 948.5976722876068,
			"width": 459.31182861328125,
			"height": 245,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"cdmaHzGtXlfS9gI2TyLeK"
			],
			"frameId": null,
			"index": "b954",
			"roundness": null,
			"seed": 880466191,
			"version": 3402,
			"versionNonce": 1235670914,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770701,
			"created": 1791933273472,
			"locked": false,
			"text": "Package files: unit of Package\nsystem - .deb/.rpm (like .exe/.msi)\n\n- Binaries & Data\n- Dependencies\n- Installation scripts (pre\nscripts/ post scripts)",
			"rawText": "Package files: unit of Package system - .deb/.rpm (like .exe/.msi)\n\n- Binaries & Data\n- Dependencies\n- Installation scripts (pre scripts/ post scripts)",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "middle",
			"containerId": "IgZ76x4iMgL1UYGihfc7D",
			"originalText": "Package files: unit of Package system - .deb/.rpm (like .exe/.msi)\n\n- Binaries & Data\n- Dependencies\n- Installation scripts (pre scripts/ post scripts)",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "YR8VPcrF",
			"type": "arrow",
			"x": -3000.938348093616,
			"y": 1074.9464573874707,
			"width": 226.27614046786903,
			"height": 157.03396114838574,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b958",
			"roundness": {
				"type": 2
			},
			"seed": 30947567,
			"version": 408,
			"versionNonce": 2136235778,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770702,
			"created": 1791932304134,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-226.27614046786903,
					157.03396114838574
				]
			],
			"startBinding": {
				"elementId": "IgZ76x4iMgL1UYGihfc7D",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "yyOhs4CC",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "4dvpEG4m",
			"type": "arrow",
			"x": -3000.938348093615,
			"y": 1068.6230728044889,
			"width": 308.76848732844246,
			"height": 140.71003408267393,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b95G",
			"roundness": {
				"type": 2
			},
			"seed": 1217903887,
			"version": 326,
			"versionNonce": 1134860098,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770702,
			"created": 1791932301154,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-308.76848732844246,
					-140.71003408267393
				]
			],
			"startBinding": {
				"elementId": "IgZ76x4iMgL1UYGihfc7D",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "c9aMk0yU",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "9X52cqwV",
			"type": "arrow",
			"x": -2317.9479425376303,
			"y": 1032.592197210776,
			"width": 201.42786129504793,
			"height": 37.51300610728231,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b95V",
			"roundness": {
				"type": 2
			},
			"seed": 1338231823,
			"version": 348,
			"versionNonce": 553394114,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770701,
			"created": 1791932214577,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-201.42786129504793,
					37.51300610728231
				]
			],
			"startBinding": {
				"elementId": "ZDdzTYu4",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "IgZ76x4iMgL1UYGihfc7D",
				"mode": "orbit",
				"fixedPoint": [
					1.0000000000000002,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "OVrER2pCfDV0SCDg7qvZ2",
			"type": "rectangle",
			"x": -2265.242475422492,
			"y": 1682.3344386873252,
			"width": 178,
			"height": 152,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"jHOkSo8u7trEGT8aOUGj_"
			],
			"frameId": null,
			"index": "b97",
			"roundness": {
				"type": 3
			},
			"seed": 1735997377,
			"version": 1433,
			"versionNonce": 301015682,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "pYbpjbGq"
				},
				{
					"id": "t9m1CJyc",
					"type": "arrow"
				},
				{
					"id": "pluObPXN",
					"type": "arrow"
				},
				{
					"id": "BSvY0wYN",
					"type": "arrow"
				},
				{
					"id": "3f5Uvl9S",
					"type": "arrow"
				},
				{
					"id": "8RI0afyQ",
					"type": "arrow"
				}
			],
			"updated": 1792945845726,
			"created": 1791933911886,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "pYbpjbGq",
			"type": "text",
			"x": -2245.080449970832,
			"y": 1740.8344386873252,
			"width": 137.6759490966797,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"jHOkSo8u7trEGT8aOUGj_"
			],
			"frameId": null,
			"index": "b98",
			"roundness": null,
			"seed": 1709086625,
			"version": 1457,
			"versionNonce": 710176898,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945815630,
			"created": 1791933911886,
			"locked": false,
			"text": "Processes",
			"rawText": "Processes",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "OVrER2pCfDV0SCDg7qvZ2",
			"originalText": "Processes",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "t9m1CJyc",
			"type": "arrow",
			"x": -992.3947157291725,
			"y": 573.373933164773,
			"width": 1088.8477596933196,
			"height": 1178.4817850937184,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b99",
			"roundness": {
				"type": 2
			},
			"seed": 1071317249,
			"version": 316,
			"versionNonce": 1295454274,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945815631,
			"created": 1791933919928,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1088.8477596933196,
					1178.4817850937184
				]
			],
			"startBinding": {
				"elementId": "qvrFhxju",
				"mode": "inside",
				"fixedPoint": [
					0.001966554567692392,
					0.47928884928320487
				]
			},
			"endBinding": {
				"elementId": "OVrER2pCfDV0SCDg7qvZ2",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "slXVXspO",
			"type": "text",
			"x": -2592.791847782239,
			"y": 2278.310075066618,
			"width": 221.7879180908203,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"yjl0bhXJuprdPhLL4PLVA"
			],
			"frameId": null,
			"index": "b9N8",
			"roundness": null,
			"seed": 1538997871,
			"version": 1848,
			"versionNonce": 1321289374,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945802878,
			"created": 1791934116602,
			"locked": false,
			"text": "system start up",
			"rawText": "system start up",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "system start up",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "Em5AXKd7",
			"type": "text",
			"x": -2603.6442852448376,
			"y": 2418.267028004464,
			"width": 607.0677490234375,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"yjl0bhXJuprdPhLL4PLVA"
			],
			"frameId": null,
			"index": "b9NG",
			"roundness": null,
			"seed": 902273167,
			"version": 1873,
			"versionNonce": 1784333022,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945802878,
			"created": 1791934116603,
			"locked": false,
			"text": "kernel initiates and run \"init\"  -> init - PID 1",
			"rawText": "kernel initiates and run \"init\"  -> init - PID 1",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "kernel initiates and run \"init\"  -> init - PID 1",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "hzjJKTDv",
			"type": "text",
			"x": -2620.4921147201085,
			"y": 2555.3941783470937,
			"width": 584.1357421875,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"yjl0bhXJuprdPhLL4PLVA"
			],
			"frameId": null,
			"index": "b9NV",
			"roundness": null,
			"seed": 1568911023,
			"version": 1866,
			"versionNonce": 100316958,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945802878,
			"created": 1791934116603,
			"locked": false,
			"text": "\"Init\" start \"systemd\" -> start all services",
			"rawText": "\"Init\" start \"systemd\" -> start all services",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "\"Init\" start \"systemd\" -> start all services",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "UjVgysCfK0ErnTqIR7f9l",
			"type": "freedraw",
			"x": -2498.192900596844,
			"y": 2324.2780847712256,
			"width": 6.8212747473901345,
			"height": 47.74905333755237,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"yjl0bhXJuprdPhLL4PLVA"
			],
			"frameId": null,
			"index": "b9Nd",
			"roundness": null,
			"seed": 2107113679,
			"version": 1745,
			"versionNonce": 1242702686,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945802878,
			"created": 1791934116603,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					2.273729336725296,
					0
				],
				[
					4.547545410664952,
					3.4106373736949536
				],
				[
					5.68441007902743,
					9.095047452722383
				],
				[
					5.68441007902743,
					14.77945753175004
				],
				[
					5.68441007902743,
					21.600732279140175
				],
				[
					5.68441007902743,
					27.285142358167604
				],
				[
					3.410594005087887,
					32.96955243719526
				],
				[
					2.273729336725296,
					37.517097847860214
				],
				[
					1.1368646683627048,
					42.06464325852494
				],
				[
					1.1368646683627048,
					44.33837259525012
				],
				[
					1.1368646683627048,
					45.47528063222012
				],
				[
					1.1368646683627048,
					47.74905333755237
				],
				[
					1.1368646683627048,
					46.6121453005826
				],
				[
					1.1368646683627048,
					45.47528063222012
				],
				[
					1.1368646683627048,
					44.33837259525012
				],
				[
					-1.1368646683627048,
					44.33837259525012
				],
				[
					-1.1368646683627048,
					44.33837259525012
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "NmEuJW3gFgJGwO5o203Dr",
			"type": "freedraw",
			"x": -2466.9396005267836,
			"y": 2471.161463323604,
			"width": 22.73764031611006,
			"height": 65.93919161160466,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"yjl0bhXJuprdPhLL4PLVA"
			],
			"frameId": null,
			"index": "b9Nl",
			"roundness": null,
			"seed": 1469910767,
			"version": 1750,
			"versionNonce": 686950302,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945802878,
			"created": 1791934116603,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					2.2738160739395425,
					0
				],
				[
					3.4106807423022474,
					0
				],
				[
					5.684410079027543,
					2.2737293367251823
				],
				[
					10.231955489692382,
					5.68441007902743
				],
				[
					14.779500900357334,
					13.642549494780269
				],
				[
					20.463910979384764,
					19.326959573807926
				],
				[
					21.60077564774747,
					26.14832105841242
				],
				[
					22.73764031611006,
					30.695779731862785
				],
				[
					22.73764031611006,
					36.38018981089044
				],
				[
					22.73764031611006,
					42.064599889917645
				],
				[
					21.60077564774747,
					48.88596137452214
				],
				[
					19.327046311022173,
					54.5703714535498
				],
				[
					17.053230237082516,
					56.844100790275206
				],
				[
					13.64263623199463,
					61.39164620093993
				],
				[
					12.505684826417678,
					64.80224020602782
				],
				[
					11.368820158055087,
					65.93919161160466
				],
				[
					11.368820158055087,
					65.93919161160466
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "DDzfmAz3P6pfbl80G0ibv",
			"type": "rectangle",
			"x": -2630.615641493761,
			"y": 2272.6960176563516,
			"width": 646.3768278108603,
			"height": 346.5573028855761,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"yjl0bhXJuprdPhLL4PLVA"
			],
			"frameId": null,
			"index": "b9O",
			"roundness": {
				"type": 3
			},
			"seed": 1713068303,
			"version": 2218,
			"versionNonce": 583754718,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "pluObPXN",
					"type": "arrow"
				}
			],
			"updated": 1792945802878,
			"created": 1791934116603,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "BFE448HOhYFEg98KkaemN",
			"type": "freedraw",
			"x": -2506.67004879909,
			"y": 2353.0905437394995,
			"width": 25.19015325758187,
			"height": 17.011541308193728,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"yjl0bhXJuprdPhLL4PLVA"
			],
			"frameId": null,
			"index": "b9OG",
			"roundness": null,
			"seed": 1049321263,
			"version": 655,
			"versionNonce": 1166967902,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945802878,
			"created": 1791934116603,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.32713998532290134,
					0
				],
				[
					0.327139985323015,
					0.32713998532290134
				],
				[
					0.9814449151498366,
					1.6357248857955256
				],
				[
					2.6171698009455895,
					3.2714497715912785
				],
				[
					4.252894686741342,
					4.58003467206413
				],
				[
					5.888619572537095,
					6.215759557859883
				],
				[
					7.197179513828814,
					7.851484443655636
				],
				[
					8.505764414301666,
					8.505764414301439
				],
				[
					8.832904399624567,
					10.141489300097192
				],
				[
					9.487209329451503,
					11.450074200570043
				],
				[
					9.487209329451503,
					13.085799086365796
				],
				[
					9.487209329451503,
					14.721523972161549
				],
				[
					9.487209329451503,
					15.375816422397975
				],
				[
					9.487209329451503,
					16.357248857957302
				],
				[
					9.487209329451503,
					16.684388843280203
				],
				[
					9.487209329451503,
					17.011541308193728
				],
				[
					10.46862928542032,
					17.011541308193728
				],
				[
					12.104354171216073,
					15.375816422397975
				],
				[
					14.394383986838648,
					13.740091536602222
				],
				[
					16.684388843280317,
					11.777214185892944
				],
				[
					18.97441865890289,
					10.468641765010716
				],
				[
					20.610143544698644,
					9.160056864537864
				],
				[
					21.591563500667462,
					8.178624428978537
				],
				[
					22.573008415817412,
					7.19719199341921
				],
				[
					23.88159331629015,
					6.870039528505686
				],
				[
					24.20873330161305,
					6.870039528505686
				],
				[
					24.863013272258968,
					6.870039528505686
				],
				[
					24.863013272258968,
					6.870039528505686
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "Vl0SByP-4Zs8xLDWV2YVc",
			"type": "freedraw",
			"x": -2458.750230146691,
			"y": 2511.428598048222,
			"width": 29.47778290912197,
			"height": 22.108337181841534,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"yjl0bhXJuprdPhLL4PLVA"
			],
			"frameId": null,
			"index": "b9OV",
			"roundness": null,
			"seed": 861249871,
			"version": 653,
			"versionNonce": 406472862,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945802878,
			"created": 1791934116603,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.6699403182673223,
					0.6699403182674359
				],
				[
					2.0098209548019668,
					2.0098209548020805
				],
				[
					3.3497527045065,
					2.6798123862392913
				],
				[
					5.35957365930858,
					4.019693022773936
				],
				[
					6.029513977575903,
					6.699505409013227
				],
				[
					6.699505409013227,
					7.369445727280663
				],
				[
					6.699505409013227,
					9.379317795252518
				],
				[
					6.699505409013227,
					12.059079068321807
				],
				[
					6.699505409013227,
					13.399010818026454
				],
				[
					6.699505409013227,
					15.408831772828307
				],
				[
					6.699505409013227,
					16.748763522532954
				],
				[
					6.699505409013227,
					18.758584477335035
				],
				[
					6.699505409013227,
					19.428575908772245
				],
				[
					6.699505409013227,
					20.09851622703968
				],
				[
					6.699505409013227,
					20.76845654530689
				],
				[
					6.699505409013227,
					22.108337181841534
				],
				[
					7.369445727280436,
					21.4383968635741
				],
				[
					10.049258113519727,
					20.76845654530689
				],
				[
					14.068951136293663,
					18.0886441590676
				],
				[
					18.75858447733492,
					14.738891454561099
				],
				[
					22.778277500108857,
					13.399010818026454
				],
				[
					26.12803020461547,
					12.729070499759018
				],
				[
					27.467961954320003,
					11.389138750054599
				],
				[
					28.80784259085476,
					10.719198431787163
				],
				[
					29.47778290912197,
					10.719198431787163
				],
				[
					29.47778290912197,
					10.719198431787163
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "qpQdtjR9z-LWb0Sb9qotN",
			"type": "freedraw",
			"x": -2216.6906948789747,
			"y": 2406.8464280276794,
			"width": 100.89281850302018,
			"height": 64.99826661420411,
			"angle": 0,
			"strokeColor": "#e03131",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"yjl0bhXJuprdPhLL4PLVA"
			],
			"frameId": null,
			"index": "b9P",
			"roundness": null,
			"seed": 813355009,
			"version": 615,
			"versionNonce": 1633912030,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945802878,
			"created": 1791934230893,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1.9402180425297502,
					-1.9402920571037612
				],
				[
					-5.820728142163034,
					-3.880510099633284
				],
				[
					-14.551857362694136,
					-3.880510099633284
				],
				[
					-25.223204625755216,
					-3.880510099633284
				],
				[
					-40.74517100971411,
					-3.880510099633284
				],
				[
					-56.267211408246794,
					-3.880510099633284
				],
				[
					-65.96844965004288,
					0
				],
				[
					-70.81906877094093,
					4.850619120898045
				],
				[
					-73.72939583473544,
					12.611565305590375
				],
				[
					-73.72939583473544,
					20.372585504856943
				],
				[
					-73.72939583473544,
					28.13360570412351
				],
				[
					-72.75928681347068,
					34.92444286755108
				],
				[
					-67.90866769257264,
					44.62568110934717
				],
				[
					-58.207429450776544,
					52.38670130861374
				],
				[
					-46.5659731664507,
					57.23732042951178
				],
				[
					-29.103714725388272,
					61.11775651457083
				],
				[
					-13.581748341429375,
					61.11775651457083
				],
				[
					4.850619120898045,
					58.207429450776544
				],
				[
					19.40247648359218,
					48.506191208980454
				],
				[
					26.19338766159376,
					36.8646609100806
				],
				[
					27.16342266828474,
					25.22320462575499
				],
				[
					24.253095604490227,
					16.49207540522366
				],
				[
					19.40247648359218,
					11.641456284325614
				],
				[
					16.492075405223886,
					9.70123824179609
				],
				[
					12.611639320164386,
					7.7609461846923296
				],
				[
					9.70123824179609,
					7.7609461846923296
				],
				[
					9.70123824179609,
					7.7609461846923296
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "P5wFoNrdCYX3fhEYZXp1x",
			"type": "freedraw",
			"x": -2331.1653357379982,
			"y": 2540.723471355721,
			"width": 148.42890069073565,
			"height": 67.90866769257264,
			"angle": 0,
			"strokeColor": "#e03131",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"yjl0bhXJuprdPhLL4PLVA"
			],
			"frameId": null,
			"index": "b9PV",
			"roundness": null,
			"seed": 1462267535,
			"version": 624,
			"versionNonce": 1654339870,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945802878,
			"created": 1791934232758,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-7.760946184692557,
					-0.9701090212647614
				],
				[
					-19.40247648359218,
					-2.910327063794284
				],
				[
					-33.95433384628632,
					-4.850619120898045
				],
				[
					-48.506191208980454,
					-4.850619120898045
				],
				[
					-62.087865535836045,
					-4.850619120898045
				],
				[
					-76.63972289853018,
					-3.8804360850590456
				],
				[
					-90.22147123995933,
					-2.910327063794284
				],
				[
					-101.86300153885895,
					1.9402920571037612
				],
				[
					-110.59405674481627,
					6.7909111780018065
				],
				[
					-115.44467586571432,
					14.551857362694136
				],
				[
					-119.3251859653476,
					21.342768540695943
				],
				[
					-120.29529498661236,
					31.044006782492033
				],
				[
					-120.29529498661236,
					40.745245024288124
				],
				[
					-116.41485890155309,
					49.47637424481945
				],
				[
					-110.59405674481627,
					54.3269933657175
				],
				[
					-97.98249143922567,
					59.177612486615544
				],
				[
					-84.40074309779652,
					63.05804857167459
				],
				[
					-67.90866769257264,
					63.05804857167459
				],
				[
					-49.476300230245215,
					63.05804857167459
				],
				[
					-33.95433384628632,
					63.05804857167459
				],
				[
					-18.432293447753636,
					63.05804857167459
				],
				[
					-5.820728142162807,
					62.08793955040983
				],
				[
					4.850619120898045,
					58.207429450776544
				],
				[
					14.551857362694136,
					52.38670130861374
				],
				[
					20.372659519430727,
					43.65557208808241
				],
				[
					25.223278640328772,
					32.984224825021556
				],
				[
					28.133605704123283,
					23.282986583225465
				],
				[
					28.133605704123283,
					13.581748341429375
				],
				[
					21.342768540695715,
					3.880510099633284
				],
				[
					11.641530298899625,
					-1.9402180425295228
				],
				[
					0,
					-2.910327063794284
				],
				[
					-12.611565305590602,
					-2.910327063794284
				],
				[
					-22.312803547386693,
					-2.910327063794284
				],
				[
					-27.16342266828474,
					0
				],
				[
					-29.103714725388272,
					0
				],
				[
					-29.103714725388272,
					0
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "90W00PKK6v6xJb2PHGvY8",
			"type": "freedraw",
			"x": -2174.975414847996,
			"y": 2597.9607917852327,
			"width": 137.75755342767502,
			"height": 5.820728142162807,
			"angle": 0,
			"strokeColor": "#e03131",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"yjl0bhXJuprdPhLL4PLVA"
			],
			"frameId": null,
			"index": "b9Q",
			"roundness": null,
			"seed": 268351279,
			"version": 608,
			"versionNonce": 55731550,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945802878,
			"created": 1791934234608,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.9700350066909778,
					0
				],
				[
					-2.9102530492205005,
					0
				],
				[
					-3.8804360850595003,
					0
				],
				[
					0,
					0
				],
				[
					11.641604313473636,
					-0.9701090212647614
				],
				[
					26.19346167616777,
					-1.9402180425295228
				],
				[
					41.71535404555266,
					-4.850619120898045
				],
				[
					60.14779552245409,
					-5.820728142162807
				],
				[
					77.60990593436873,
					-5.820728142162807
				],
				[
					94.1021293687404,
					-5.820728142162807
				],
				[
					100.89296653216797,
					-5.820728142162807
				],
				[
					105.74358565306602,
					-5.820728142162807
				],
				[
					109.6240217381253,
					-5.820728142162807
				],
				[
					114.47464085902334,
					-5.820728142162807
				],
				[
					120.29544301576016,
					-5.820728142162807
				],
				[
					125.1460621366582,
					-5.820728142162807
				],
				[
					129.99668125755625,
					-5.820728142162807
				],
				[
					132.90708233592477,
					-5.820728142162807
				],
				[
					133.87711734261552,
					-5.820728142162807
				],
				[
					133.87711734261552,
					-5.820728142162807
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "pluObPXN",
			"type": "arrow",
			"x": -2178.0196034559863,
			"y": 1840.3344386873252,
			"width": 127.69763575219349,
			"height": 426.8615789690259,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9Z",
			"roundness": {
				"type": 2
			},
			"seed": 623906241,
			"version": 774,
			"versionNonce": 36681730,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945815631,
			"created": 1791934246271,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-127.69763575219349,
					426.8615789690259
				]
			],
			"startBinding": {
				"elementId": "OVrER2pCfDV0SCDg7qvZ2",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					1.0000000000000016
				]
			},
			"endBinding": {
				"elementId": "DDzfmAz3P6pfbl80G0ibv",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					0
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "uIRUJNCd",
			"type": "text",
			"x": -2909.2394607900515,
			"y": 1604.0219335635875,
			"width": 200.3399200439453,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9a",
			"roundness": null,
			"seed": 634239137,
			"version": 254,
			"versionNonce": 144815362,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "OSmLolwc",
					"type": "arrow"
				},
				{
					"id": "AZcNg1xx",
					"type": "arrow"
				},
				{
					"id": "BSvY0wYN",
					"type": "arrow"
				}
			],
			"updated": 1792945783991,
			"created": 1791934337270,
			"locked": false,
			"text": "view processes",
			"rawText": "view processes",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "view processes",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "BSvY0wYN",
			"type": "arrow",
			"x": -2271.242475422492,
			"y": 1756.4992337351498,
			"width": 432.15706532361355,
			"height": 133.27759563206837,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9b",
			"roundness": {
				"type": 2
			},
			"seed": 2048799439,
			"version": 332,
			"versionNonce": 691890114,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945815631,
			"created": 1791934343721,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-432.15706532361355,
					-133.27759563206837
				]
			],
			"startBinding": {
				"elementId": "OVrER2pCfDV0SCDg7qvZ2",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "uIRUJNCd",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"hasTextLink": false,
			"moveMidPointsWithElement": false
		},
		{
			"id": "8RqBljqC",
			"type": "rectangle",
			"x": -3372.0492959424787,
			"y": 1595.4809455442376,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9c",
			"roundness": {
				"type": 3
			},
			"seed": 538257583,
			"version": 1539,
			"versionNonce": 274062467,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "eE7Fj0Hn"
				},
				{
					"id": "z8FI1qb5",
					"type": "arrow"
				},
				{
					"id": "OSmLolwc",
					"type": "arrow"
				}
			],
			"updated": 1792945783991,
			"created": 1791934347097,
			"link": "[[ps]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "eE7Fj0Hn",
			"type": "text",
			"x": -3315.152498994996,
			"y": 1606.8913202144454,
			"width": 157.8079376220703,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9d",
			"roundness": null,
			"seed": 602553039,
			"version": 1529,
			"versionNonce": 1210776642,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945783991,
			"created": 1791934347097,
			"locked": false,
			"text": "ps / ps aux",
			"rawText": "ps / ps aux",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8RqBljqC",
			"originalText": "ps / ps aux",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "OSmLolwc",
			"type": "arrow",
			"x": -2908.7509771892073,
			"y": 1619.4376673790503,
			"width": 186.1967872362361,
			"height": 4.8171430524419065,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9e",
			"roundness": {
				"type": 2
			},
			"seed": 706457505,
			"version": 273,
			"versionNonce": 98961026,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770704,
			"created": 1791934352077,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-186.1967872362361,
					4.8171430524419065
				]
			],
			"startBinding": {
				"elementId": "uIRUJNCd",
				"mode": "inside",
				"fixedPoint": [
					0.00243827391334173,
					0.44044953758465066
				]
			},
			"endBinding": {
				"elementId": "8RqBljqC",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "XmskFlt2",
			"type": "text",
			"x": -3711.784833772809,
			"y": 1585.3361287634225,
			"width": 211.5399169921875,
			"height": 70,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9f",
			"roundness": null,
			"seed": 2037515873,
			"version": 347,
			"versionNonce": 1361466306,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "z8FI1qb5",
					"type": "arrow"
				},
				{
					"id": "hW7aUmut",
					"type": "arrow"
				}
			],
			"updated": 1792945783991,
			"created": 1791934535407,
			"locked": false,
			"text": "view processes \ndynamically",
			"rawText": "view processes \ndynamically",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "view processes \ndynamically",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "z8FI1qb5",
			"type": "arrow",
			"x": -3370.2464629669334,
			"y": 1624.3971022893795,
			"width": 124.49845381368823,
			"height": 3.882457221426648,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9g",
			"roundness": {
				"type": 2
			},
			"seed": 602363009,
			"version": 341,
			"versionNonce": 154480322,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770704,
			"created": 1791934554685,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-124.49845381368823,
					-3.882457221426648
				]
			],
			"startBinding": {
				"elementId": "8RqBljqC",
				"mode": "inside",
				"fixedPoint": [
					0.006637786486237714,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "XmskFlt2",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "rTx9da3F",
			"type": "rectangle",
			"x": -4082.146685064514,
			"y": 1588.155592637406,
			"width": 271.60153151703526,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9h",
			"roundness": {
				"type": 3
			},
			"seed": 524903457,
			"version": 1562,
			"versionNonce": 1842465603,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "y2JgEo7J"
				},
				{
					"id": "hW7aUmut",
					"type": "arrow"
				}
			],
			"updated": 1792945783991,
			"created": 1791934561703,
			"link": "[[ps]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "y2JgEo7J",
			"type": "text",
			"x": -3970.0059077093165,
			"y": 1599.5659673076138,
			"width": 47.319976806640625,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9i",
			"roundness": null,
			"seed": 531249153,
			"version": 1547,
			"versionNonce": 1438323458,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945783991,
			"created": 1791934561703,
			"locked": false,
			"text": "top",
			"rawText": "top",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rTx9da3F",
			"originalText": "top",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "hW7aUmut",
			"type": "arrow",
			"x": -3717.2848337728096,
			"y": 1620.1609443938717,
			"width": 87.76031977466891,
			"height": 2.9070106417727857,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9j",
			"roundness": {
				"type": 2
			},
			"seed": 76368655,
			"version": 254,
			"versionNonce": 774235714,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770704,
			"created": 1791934566352,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-87.76031977466891,
					-2.9070106417727857
				]
			],
			"startBinding": {
				"elementId": "XmskFlt2",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "rTx9da3F",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"hasTextLink": false,
			"moveMidPointsWithElement": false
		},
		{
			"id": "3f5Uvl9S",
			"type": "arrow",
			"x": -2271.242475422492,
			"y": 1759.5623608007302,
			"width": 441.84165731247276,
			"height": 89.30519140773663,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9l",
			"roundness": {
				"type": 2
			},
			"seed": 1325671372,
			"version": 351,
			"versionNonce": 1249845122,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945815631,
			"created": 1792074552886,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-441.84165731247276,
					89.30519140773663
				]
			],
			"startBinding": {
				"elementId": "OVrER2pCfDV0SCDg7qvZ2",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "sOJ1274M",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "-qAq7DqYIgl8Q0PaHY79G",
			"type": "rectangle",
			"x": -3384.562881626233,
			"y": 1814.6472050181997,
			"width": 314.7591906879011,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9m",
			"roundness": {
				"type": 3
			},
			"seed": 1191918412,
			"version": 1270,
			"versionNonce": 1310267970,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "yHBTBlHn"
				},
				{
					"id": "KMRgKind",
					"type": "arrow"
				},
				{
					"id": "6yseZbLr",
					"type": "arrow"
				}
			],
			"updated": 1792945783991,
			"created": 1792074565286,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "yHBTBlHn",
			"type": "text",
			"x": -3346.295232388239,
			"y": 1826.0575796884075,
			"width": 238.22389221191406,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9n",
			"roundness": null,
			"seed": 320729548,
			"version": 1363,
			"versionNonce": 1849721346,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945783991,
			"created": 1792074565286,
			"locked": false,
			"text": "\"process_name\" &",
			"rawText": "\"process_name\" &",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "-qAq7DqYIgl8Q0PaHY79G",
			"originalText": "\"process_name\" &",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "KMRgKind",
			"type": "arrow",
			"x": -2959.2534216571753,
			"y": 1850.7839112422275,
			"width": 105.05026928115694,
			"height": 6.861319036553141,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9o",
			"roundness": {
				"type": 2
			},
			"seed": 1952042444,
			"version": 318,
			"versionNonce": 1255394818,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770704,
			"created": 1792075499830,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-105.05026928115694,
					-6.861319036553141
				]
			],
			"startBinding": {
				"elementId": "sOJ1274M",
				"mode": "inside",
				"fixedPoint": [
					0.005284618545806711,
					0.5115956728067561
				]
			},
			"endBinding": {
				"elementId": "-qAq7DqYIgl8Q0PaHY79G",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "oTVd5yA6",
			"type": "text",
			"x": -3407.8555435726794,
			"y": 2034.8849593469458,
			"width": 357.1678161621094,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9q",
			"roundness": null,
			"seed": 668927564,
			"version": 325,
			"versionNonce": 1281714562,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "6yseZbLr",
					"type": "arrow"
				},
				{
					"id": "7tGIf4hP",
					"type": "arrow"
				}
			],
			"updated": 1792945783991,
			"created": 1792075549723,
			"locked": false,
			"text": "list the jobs from terminal",
			"rawText": "list the jobs from terminal",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "list the jobs from terminal",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "6yseZbLr",
			"type": "arrow",
			"x": -3227.2223854603726,
			"y": 1877.9679543586155,
			"width": 1.9429581524768764,
			"height": 151.4170049883303,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9r",
			"roundness": {
				"type": 2
			},
			"seed": 590681164,
			"version": 303,
			"versionNonce": 820952514,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770705,
			"created": 1792075567503,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1.9429581524768764,
					151.4170049883303
				]
			],
			"startBinding": {
				"elementId": "-qAq7DqYIgl8Q0PaHY79G",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					1
				]
			},
			"endBinding": {
				"elementId": "oTVd5yA6",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					0
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "M3uyH2UvX3hjluyBP7dbZ",
			"type": "rectangle",
			"x": -3814.051442771002,
			"y": 2023.4746908918896,
			"width": 314.7591906879011,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9s",
			"roundness": {
				"type": 3
			},
			"seed": 301237324,
			"version": 1371,
			"versionNonce": 219574530,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Wk3Dw2Gd"
				},
				{
					"id": "7tGIf4hP",
					"type": "arrow"
				},
				{
					"id": "AhsYahQB",
					"type": "arrow"
				},
				{
					"id": "KlQikiU5",
					"type": "arrow"
				},
				{
					"id": "9SfHvlMQ",
					"type": "arrow"
				}
			],
			"updated": 1792945783991,
			"created": 1792075571906,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "Wk3Dw2Gd",
			"type": "text",
			"x": -3685.035830581348,
			"y": 2034.8850655620975,
			"width": 56.72796630859375,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9t",
			"roundness": null,
			"seed": 603331276,
			"version": 1463,
			"versionNonce": 2028273858,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945783991,
			"created": 1792075571906,
			"locked": false,
			"text": "jobs",
			"rawText": "jobs",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "M3uyH2UvX3hjluyBP7dbZ",
			"originalText": "jobs",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "7tGIf4hP",
			"type": "arrow",
			"x": -3413.3555435726794,
			"y": 2052.3886030047356,
			"width": 80.43670851042089,
			"height": 0.002100974505992781,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9u",
			"roundness": {
				"type": 2
			},
			"seed": 539942092,
			"version": 317,
			"versionNonce": 1033221506,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770705,
			"created": 1792075573980,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-80.43670851042089,
					0.002100974505992781
				]
			],
			"startBinding": {
				"elementId": "oTVd5yA6",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "M3uyH2UvX3hjluyBP7dbZ",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "edLCymRw",
			"type": "text",
			"x": -4389.113420217509,
			"y": 1911.6762655773032,
			"width": 366.2678527832031,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9w",
			"roundness": null,
			"seed": 1877747020,
			"version": 271,
			"versionNonce": 227096642,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "GpZZwey8",
					"type": "arrow"
				},
				{
					"id": "AhsYahQB",
					"type": "arrow"
				}
			],
			"updated": 1792945783991,
			"created": 1792075667770,
			"locked": false,
			"text": "put process to background",
			"rawText": "put process to background",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "put process to background",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "kxSfY6qyus8epU6LsH6hs",
			"type": "rectangle",
			"x": -4832.942853033486,
			"y": 1907.1636893714972,
			"width": 314.7591906879011,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9x",
			"roundness": {
				"type": 3
			},
			"seed": 2044056308,
			"version": 1440,
			"versionNonce": 1174200322,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "LoTSof2l"
				},
				{
					"id": "GpZZwey8",
					"type": "arrow"
				}
			],
			"updated": 1792945783991,
			"created": 1792075687066,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "LoTSof2l",
			"type": "text",
			"x": -4762.11120080477,
			"y": 1918.574064041705,
			"width": 173.09588623046875,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9y",
			"roundness": null,
			"seed": 50812020,
			"version": 1574,
			"versionNonce": 1227198402,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945783991,
			"created": 1792075687066,
			"locked": false,
			"text": "bg %\"job_id\"",
			"rawText": "bg %\"job_id\"",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "kxSfY6qyus8epU6LsH6hs",
			"originalText": "bg %\"job_id\"",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "GpZZwey8",
			"type": "arrow",
			"x": -4394.613420217509,
			"y": 1929.4737949549556,
			"width": 118.07024212807664,
			"height": 6.312021784031231,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "b9z",
			"roundness": {
				"type": 2
			},
			"seed": 88892404,
			"version": 265,
			"versionNonce": 1953883266,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770706,
			"created": 1792075713517,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-118.07024212807664,
					6.312021784031231
				]
			],
			"startBinding": {
				"elementId": "edLCymRw",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "kxSfY6qyus8epU6LsH6hs",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "GCflKIFC",
			"type": "text",
			"x": -4379.510289536211,
			"y": 2070.2622464406195,
			"width": 362.2918701171875,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bA0",
			"roundness": null,
			"seed": 537832012,
			"version": 289,
			"versionNonce": 607258434,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "_W8qu2AtnDKXH52bwmxR5",
					"type": "arrow"
				},
				{
					"id": "KlQikiU5",
					"type": "arrow"
				}
			],
			"updated": 1792945783991,
			"created": 1792075716603,
			"locked": false,
			"text": "put process to foreground",
			"rawText": "put process to foreground",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "put process to foreground",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "tBH0VcAz4tB6Blytd5FHC",
			"type": "rectangle",
			"x": -4826.852554275867,
			"y": 2065.7496702348135,
			"width": 314.7591906879011,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bA1",
			"roundness": {
				"type": 3
			},
			"seed": 2010874060,
			"version": 1454,
			"versionNonce": 1286852354,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "YKCbQmJt"
				},
				{
					"id": "_W8qu2AtnDKXH52bwmxR5",
					"type": "arrow"
				}
			],
			"updated": 1792945783991,
			"created": 1792075716603,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "YKCbQmJt",
			"type": "text",
			"x": -4755.20890558719,
			"y": 2077.160044905021,
			"width": 171.47189331054688,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bA2",
			"roundness": null,
			"seed": 482969420,
			"version": 1588,
			"versionNonce": 1495703234,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945783991,
			"created": 1792075716603,
			"locked": false,
			"text": "fg %\"job_id\"",
			"rawText": "fg %\"job_id\"",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "tBH0VcAz4tB6Blytd5FHC",
			"originalText": "fg %\"job_id\"",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "_W8qu2AtnDKXH52bwmxR5",
			"type": "arrow",
			"x": -4385.010289536211,
			"y": 2088.051985413714,
			"width": 121.58307405175583,
			"height": 6.327602593145912,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bA3",
			"roundness": {
				"type": 2
			},
			"seed": 858963404,
			"version": 286,
			"versionNonce": 990512194,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770706,
			"created": 1792075716603,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-121.58307405175583,
					6.327602593145912
				]
			],
			"startBinding": {
				"elementId": "GCflKIFC",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "tBH0VcAz4tB6Blytd5FHC",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "AhsYahQB",
			"type": "arrow",
			"x": -3819.5514427710023,
			"y": 2049.1452536701454,
			"width": 197.7941246633045,
			"height": 116.71989412595644,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bA4",
			"roundness": {
				"type": 2
			},
			"seed": 19926644,
			"version": 277,
			"versionNonce": 1376236866,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770705,
			"created": 1792075727141,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-197.7941246633045,
					-116.71989412595644
				]
			],
			"startBinding": {
				"elementId": "M3uyH2UvX3hjluyBP7dbZ",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "edLCymRw",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "KlQikiU5",
			"type": "arrow",
			"x": -3819.5514427710013,
			"y": 2053.3484931492585,
			"width": 192.16697664802223,
			"height": 33.459607779133876,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bA5",
			"roundness": {
				"type": 2
			},
			"seed": 157717748,
			"version": 267,
			"versionNonce": 1336130818,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770706,
			"created": 1792075729905,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-192.16697664802223,
					33.459607779133876
				]
			],
			"startBinding": {
				"elementId": "M3uyH2UvX3hjluyBP7dbZ",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "GCflKIFC",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "llv3BdCf_N2n4b9eD2fy7",
			"type": "rectangle",
			"x": -3802.135140800733,
			"y": 2329.5511060780445,
			"width": 314.7591906879011,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bA6",
			"roundness": {
				"type": 3
			},
			"seed": 2110604660,
			"version": 1389,
			"versionNonce": 78130626,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XEXbntji"
				},
				{
					"id": "AZcNg1xx",
					"type": "arrow"
				},
				{
					"id": "RgCfJyJZ",
					"type": "arrow"
				}
			],
			"updated": 1792945783991,
			"created": 1792075741102,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "XEXbntji",
			"type": "text",
			"x": -3687.6235187844195,
			"y": 2340.961480748252,
			"width": 85.73594665527344,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bA7",
			"roundness": null,
			"seed": 745305844,
			"version": 1496,
			"versionNonce": 950084994,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945783991,
			"created": 1792075741102,
			"locked": false,
			"text": "jobs -l",
			"rawText": "jobs -l",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "llv3BdCf_N2n4b9eD2fy7",
			"originalText": "jobs -l",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "kg0aQjUr",
			"type": "text",
			"x": -3757.9870148083683,
			"y": 2192.748878670241,
			"width": 212.4359130859375,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bA8",
			"roundness": null,
			"seed": 1047436236,
			"version": 350,
			"versionNonce": 975512898,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "9SfHvlMQ",
					"type": "arrow"
				},
				{
					"id": "RgCfJyJZ",
					"type": "arrow"
				}
			],
			"updated": 1792945783991,
			"created": 1792075751783,
			"locked": false,
			"text": "see job-process",
			"rawText": "see job-process",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "see job-process",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "9SfHvlMQ",
			"type": "arrow",
			"x": -3656.6997845660576,
			"y": 2086.7954402323053,
			"width": 1.1688687377923088,
			"height": 108.20479985544944,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bA9",
			"roundness": {
				"type": 2
			},
			"seed": 272712908,
			"version": 329,
			"versionNonce": 334023874,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770706,
			"created": 1792075759811,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1.1688687377923088,
					108.20479985544944
				]
			],
			"startBinding": {
				"elementId": "M3uyH2UvX3hjluyBP7dbZ",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					1
				]
			},
			"endBinding": {
				"elementId": "kg0aQjUr",
				"mode": "inside",
				"fixedPoint": [
					0.4712873640344281,
					0.06432461192896101
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "RgCfJyJZ",
			"type": "arrow",
			"x": -3651.368347552067,
			"y": 2233.2488786702406,
			"width": 6.2648108923294785,
			"height": 90.80222740780346,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bAA",
			"roundness": {
				"type": 2
			},
			"seed": 1322921332,
			"version": 281,
			"versionNonce": 1306745794,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770707,
			"created": 1792075764231,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					6.2648108923294785,
					90.80222740780346
				]
			],
			"startBinding": {
				"elementId": "kg0aQjUr",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					1
				]
			},
			"endBinding": {
				"elementId": "llv3BdCf_N2n4b9eD2fy7",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					0
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "sOJ1274M",
			"type": "text",
			"x": -2960.5320239703165,
			"y": 1814.9722141457546,
			"width": 241.94789123535156,
			"height": 70,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bAD",
			"roundness": null,
			"seed": 1347832012,
			"version": 368,
			"versionNonce": 373904514,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "3f5Uvl9S",
					"type": "arrow"
				},
				{
					"id": "KMRgKind",
					"type": "arrow"
				}
			],
			"updated": 1792945783991,
			"created": 1792074529794,
			"locked": false,
			"text": "run a process \nin the background",
			"rawText": "run a process \nin the background",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "run a process \nin the background",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "EpRgps5E",
			"type": "text",
			"x": -3156.788793446808,
			"y": 2698.78997985246,
			"width": 182.16787719726562,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"SWj7cpeVxUbSCQAP0QJnJ"
			],
			"frameId": null,
			"index": "bAa",
			"roundness": null,
			"seed": 467116660,
			"version": 1960,
			"versionNonce": 1898006018,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946797615,
			"created": 1792075983443,
			"locked": false,
			"text": "\"kill\" command",
			"rawText": "\"kill\" command",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "\"kill\" command",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "vGesXCsIJG7SVWPHWNdq9",
			"type": "rectangle",
			"x": -3271.846834848784,
			"y": 2677.797875983161,
			"width": 646.3768278108603,
			"height": 346.5573028855761,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"SWj7cpeVxUbSCQAP0QJnJ"
			],
			"frameId": null,
			"index": "bAb",
			"roundness": {
				"type": 3
			},
			"seed": 1426037236,
			"version": 2371,
			"versionNonce": 516765122,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "KGyHOMbx",
					"type": "arrow"
				}
			],
			"updated": 1792946797615,
			"created": 1792075983443,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "J0moLZb6",
			"type": "text",
			"x": -3146.140135146805,
			"y": 2978.9381485861327,
			"width": 102.92796325683594,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"SWj7cpeVxUbSCQAP0QJnJ"
			],
			"frameId": null,
			"index": "bAc",
			"roundness": null,
			"seed": 263002444,
			"version": 486,
			"versionNonce": 1151872322,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946797615,
			"created": 1792076015320,
			"locked": false,
			"text": "process",
			"rawText": "process",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "process",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "gW3nsyegI9GpQFO4Mttb2",
			"type": "freedraw",
			"x": -3076.6550999991837,
			"y": 2747.838290429983,
			"width": 22.86662924161692,
			"height": 203.97032585688066,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"SWj7cpeVxUbSCQAP0QJnJ"
			],
			"frameId": null,
			"index": "bAd",
			"roundness": null,
			"seed": 1066874996,
			"version": 497,
			"versionNonce": 125121794,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946797615,
			"created": 1792076024976,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.9147209963962268,
					4.573325848323293
				],
				[
					2.743953638945186,
					13.719977544969879
				],
				[
					6.4026282742870535,
					27.439955089940213
				],
				[
					10.975954122610347,
					46.647944587922666
				],
				[
					15.54927997093364,
					69.51457382953959
				],
				[
					20.122605819256933,
					95.12519160180864
				],
				[
					21.951908245220693,
					119.82115816109626
				],
				[
					21.951908245220693,
					138.1144615543899
				],
				[
					21.951908245220693,
					155.49311373470118
				],
				[
					21.951908245220693,
					170.1277424926534
				],
				[
					19.207954606275507,
					181.10369661526374
				],
				[
					17.3785823968974,
					186.59174345998326
				],
				[
					16.46393118391552,
					192.07972052128844
				],
				[
					13.719977544970334,
					194.82367416023362
				],
				[
					11.890605335592227,
					197.5676975825936
				],
				[
					10.061302909628466,
					202.1410234309169
				],
				[
					9.146651696646586,
					203.97032585688066
				],
				[
					8.23193070025036,
					203.97032585688066
				],
				[
					8.23193070025036,
					203.97032585688066
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "Jcl6DS8Q64NMvA5vpJokZ",
			"type": "freedraw",
			"x": -3076.6550999991837,
			"y": 2939.0033597382894,
			"width": 39.33056042553244,
			"height": 25.610582880562106,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"SWj7cpeVxUbSCQAP0QJnJ"
			],
			"frameId": null,
			"index": "bAe",
			"roundness": null,
			"seed": 1859937996,
			"version": 501,
			"versionNonce": 1120617666,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946797615,
			"created": 1792076025576,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-1.829372209378107
				],
				[
					0,
					-0.9147209963962268
				],
				[
					2.743953638945186,
					0
				],
				[
					3.658604851927066,
					3.658604851927066
				],
				[
					4.573325848323293,
					5.487977061305173
				],
				[
					6.4026282742870535,
					9.146651696646586
				],
				[
					6.4026282742870535,
					12.805256548574107
				],
				[
					7.317279487268479,
					13.719977544969879
				],
				[
					8.23193070025036,
					15.54927997093364
				],
				[
					9.146651696646586,
					15.54927997093364
				],
				[
					9.146651696646586,
					17.3785823968974
				],
				[
					10.975954122610347,
					17.3785823968974
				],
				[
					11.890605335592227,
					16.46393118391552
				],
				[
					12.805256548573652,
					16.46393118391552
				],
				[
					13.719977544970334,
					14.63462875795176
				],
				[
					15.54927997093364,
					11.890605335592227
				],
				[
					17.3785823968974,
					9.146651696646586
				],
				[
					21.951908245220693,
					4.573325848323293
				],
				[
					26.525234093543986,
					0
				],
				[
					33.842583364227266,
					-4.573325848323293
				],
				[
					35.67188579019057,
					-7.31734927068328
				],
				[
					39.33056042553244,
					-8.232000483664706
				],
				[
					39.33056042553244,
					-8.232000483664706
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "APM1QXJ3",
			"type": "text",
			"x": -3023.1148030211793,
			"y": 2822.719493501139,
			"width": 370.8318176269531,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"SWj7cpeVxUbSCQAP0QJnJ"
			],
			"frameId": null,
			"index": "bAf",
			"roundness": null,
			"seed": 533938804,
			"version": 573,
			"versionNonce": 273243266,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946797615,
			"created": 1792076027590,
			"locked": false,
			"text": "sends \"signal\" to processes",
			"rawText": "sends \"signal\" to processes",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "sends \"signal\" to processes",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "SrLk5ikIeTShunJXBrpza",
			"type": "freedraw",
			"x": -2849.8181797923935,
			"y": 2810.950201093528,
			"width": 107.93051793379709,
			"height": 113.41849499510226,
			"angle": 0,
			"strokeColor": "#e03131",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"SWj7cpeVxUbSCQAP0QJnJ"
			],
			"frameId": null,
			"index": "bAg",
			"roundness": null,
			"seed": 1541003508,
			"version": 514,
			"versionNonce": 2108587074,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946797615,
			"created": 1792076052383,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-2.7439885306525866
				],
				[
					-1.8293024259637605,
					-8.232000483664706
				],
				[
					-7.31734927068328,
					-13.719977544969879
				],
				[
					-13.719977544970334,
					-16.463966075622466
				],
				[
					-24.695931667580226,
					-20.122640710964333
				],
				[
					-36.586606786587254,
					-21.95197802863504
				],
				[
					-48.47728190559337,
					-21.95197802863504
				],
				[
					-58.53851503180749,
					-21.03729192394576
				],
				[
					-68.5998877248503,
					-13.719977544969879
				],
				[
					-79.57584184746065,
					-5.487977061305173
				],
				[
					-86.89319111814393,
					5.487977061305173
				],
				[
					-93.29581939243099,
					19.207954606275507
				],
				[
					-95.12512181839429,
					36.5866067865868
				],
				[
					-95.12512181839429,
					52.13592164922784
				],
				[
					-92.38109839603476,
					68.5999226165577
				],
				[
					-85.06388869218063,
					79.57587673916805
				],
				[
					-71.34391114721029,
					86.89322600985133
				],
				[
					-54.879910179880426,
					88.72252843581464
				],
				[
					-39.330630208946786,
					88.72252843581464
				],
				[
					-21.951908245220693,
					80.49052795214993
				],
				[
					-8.231930700250814,
					68.5999226165577
				],
				[
					0.9147209963962268,
					54.879910179880426
				],
				[
					8.232070267079507,
					39.330595317239386
				],
				[
					10.975954122610347,
					27.439955089940213
				],
				[
					10.975954122610347,
					11.890640227299627
				],
				[
					12.8053961154028,
					0
				],
				[
					12.8053961154028,
					-10.975989014317292
				],
				[
					10.975954122610347,
					-18.293303393293172
				],
				[
					5.48804684471952,
					-21.95197802863504
				],
				[
					-1.8293024259637605,
					-24.695966559287626
				],
				[
					-10.975954122610347,
					-24.695966559287626
				],
				[
					-20.122605819256933,
					-21.95197802863504
				],
				[
					-25.610652663976907,
					-17.378652180311747
				],
				[
					-31.09855994186728,
					-11.890640227299173
				],
				[
					-32.013280938263506,
					-10.061302909628466
				],
				[
					-32.013280938263506,
					-10.061302909628466
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "cbuVfkyE",
			"type": "text",
			"x": -3036.5643735144295,
			"y": 2522.2802678556955,
			"width": 175.81190490722656,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bAh",
			"roundness": null,
			"seed": 2015520588,
			"version": 355,
			"versionNonce": 304820866,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "8RI0afyQ",
					"type": "arrow"
				},
				{
					"id": "KGyHOMbx",
					"type": "arrow"
				},
				{
					"id": "Oc0GDYjX",
					"type": "arrow"
				}
			],
			"updated": 1792945783991,
			"created": 1792076080346,
			"locked": false,
			"text": "kill a process",
			"rawText": "kill a process",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "kill a process",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "8RI0afyQ",
			"type": "arrow",
			"x": -2271.242475422492,
			"y": 1766.2228982944998,
			"width": 584.0099931847108,
			"height": 766.343714921285,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bAi",
			"roundness": {
				"type": 2
			},
			"seed": 418556916,
			"version": 393,
			"versionNonce": 305389378,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945815631,
			"created": 1792076088630,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-584.0099931847108,
					766.343714921285
				]
			],
			"startBinding": {
				"elementId": "OVrER2pCfDV0SCDg7qvZ2",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "cbuVfkyE",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "KGyHOMbx",
			"type": "arrow",
			"x": -2948.638692372066,
			"y": 2562.7802678556955,
			"width": 0.042761613234233664,
			"height": 109.51760812746534,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bAj",
			"roundness": {
				"type": 2
			},
			"seed": 82086860,
			"version": 377,
			"versionNonce": 1491414402,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946797615,
			"created": 1792076092309,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.042761613234233664,
					109.51760812746534
				]
			],
			"startBinding": {
				"elementId": "cbuVfkyE",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					1
				]
			},
			"endBinding": {
				"elementId": "vGesXCsIJG7SVWPHWNdq9",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					0
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "m1eg7j8v",
			"type": "rectangle",
			"x": -3786.3320594642946,
			"y": 2521.681314557888,
			"width": 314.7591906879011,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bAk",
			"roundness": {
				"type": 3
			},
			"seed": 721130828,
			"version": 1427,
			"versionNonce": 1353935299,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "lTzmBqSO"
				},
				{
					"id": "Oc0GDYjX",
					"type": "arrow"
				}
			],
			"updated": 1792945783991,
			"created": 1792076350713,
			"link": "[[kill]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "lTzmBqSO",
			"type": "text",
			"x": -3646.1304426359693,
			"y": 2533.0916892280957,
			"width": 34.35595703125,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bAl",
			"roundness": null,
			"seed": 200477644,
			"version": 1536,
			"versionNonce": 1474617730,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945783991,
			"created": 1792076350713,
			"locked": false,
			"text": "kill",
			"rawText": "kill",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "m1eg7j8v",
			"originalText": "kill",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "Oc0GDYjX",
			"type": "arrow",
			"x": -3042.0643735144295,
			"y": 2539.9204901717144,
			"width": 424.0084952619641,
			"height": 10.54025881529651,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bAm",
			"roundness": {
				"type": 2
			},
			"seed": 144787956,
			"version": 261,
			"versionNonce": 1313248130,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770708,
			"created": 1792076358761,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-424.0084952619641,
					10.54025881529651
				]
			],
			"startBinding": {
				"elementId": "cbuVfkyE",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "m1eg7j8v",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "s9aBDBPi",
			"type": "rectangle",
			"x": -950.7262414258832,
			"y": -2357.2504252734734,
			"width": 289.2428820192458,
			"height": 217.73447120016203,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bAn",
			"roundness": {
				"type": 3
			},
			"seed": 310446339,
			"version": 1665,
			"versionNonce": 321553823,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "9ksOXjpZ"
				},
				{
					"id": "bw8W3jIW",
					"type": "arrow"
				},
				{
					"id": "B6hXG4MREPkAajuyXPV8Y",
					"type": "arrow"
				}
			],
			"updated": 1792946185687,
			"created": 1792684156141,
			"link": "[[shell script]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "9ksOXjpZ",
			"type": "text",
			"x": -845.2727844250494,
			"y": -2270.8831896733923,
			"width": 78.33596801757812,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bAnG",
			"roundness": null,
			"seed": 807334051,
			"version": 1656,
			"versionNonce": 351064898,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946770708,
			"created": 1792684156141,
			"locked": false,
			"text": "Shell",
			"rawText": "Shell",
			"fontSize": 36,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "s9aBDBPi",
			"originalText": "Shell",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "bw8W3jIW",
			"type": "arrow",
			"x": -789.3508012198287,
			"y": 414.0388806944502,
			"width": 522.8829931322897,
			"height": 2547.5548347677613,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bAnV",
			"roundness": {
				"type": 2
			},
			"seed": 2046794762,
			"version": 1881,
			"versionNonce": 266784158,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946197772,
			"created": 1790870085126,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-522.8829931322897,
					-1909.1124753121999
				],
				[
					-16.31015573355546,
					-2547.5548347677613
				]
			],
			"startBinding": {
				"elementId": "qvrFhxju",
				"mode": "orbit",
				"fixedPoint": [
					0.4971500963441139,
					-0.018754570787105487
				]
			},
			"endBinding": {
				"elementId": "s9aBDBPi",
				"mode": "orbit",
				"fixedPoint": [
					0.5015345009003426,
					1.0275565002037934
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "B6hXG4MREPkAajuyXPV8Y",
			"type": "arrow",
			"x": -780.4305055301633,
			"y": -2133.515954073311,
			"width": 21.347002543264352,
			"height": 345.4496361646329,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bAp",
			"roundness": {
				"type": 2
			},
			"seed": 1075272461,
			"version": 1892,
			"versionNonce": 1485860702,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946203063,
			"created": 1792684244658,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					13.323279707752135,
					116.23450434014899
				],
				[
					21.347002543264352,
					345.4496361646329
				]
			],
			"startBinding": {
				"elementId": "s9aBDBPi",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					0
				]
			},
			"endBinding": {
				"elementId": "BgtGftaI",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					0
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "odJVWkXGMXdbZOsWxXYwx",
			"type": "rectangle",
			"x": -2271.2424749323195,
			"y": 3455.060137813433,
			"width": 178,
			"height": 152,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"uan_7q6_JedLWalAUS3Y9"
			],
			"frameId": null,
			"index": "bAs",
			"roundness": {
				"type": 3
			},
			"seed": 798748638,
			"version": 1726,
			"versionNonce": 1813150914,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "wotTp7lN"
				},
				{
					"id": "9w2mGQC6",
					"type": "arrow"
				},
				{
					"id": "x7NDITGN",
					"type": "arrow"
				},
				{
					"id": "0oi7xlAl",
					"type": "arrow"
				}
			],
			"updated": 1792946374669,
			"created": 1792945818539,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "wotTp7lN",
			"type": "text",
			"x": -2263.7084402033156,
			"y": 3513.560137813433,
			"width": 162.9319305419922,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"uan_7q6_JedLWalAUS3Y9"
			],
			"frameId": null,
			"index": "bAt",
			"roundness": null,
			"seed": 1150174238,
			"version": 1760,
			"versionNonce": 1681296834,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946290824,
			"created": 1792945818539,
			"locked": false,
			"text": "Environment",
			"rawText": "Environment",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "odJVWkXGMXdbZOsWxXYwx",
			"originalText": "Environment",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "9w2mGQC6",
			"type": "arrow",
			"x": -999.2010772170523,
			"y": 594.5397229307789,
			"width": 1180.5421815542913,
			"height": 2854.520414882654,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bAv",
			"roundness": {
				"type": 2
			},
			"seed": 734521858,
			"version": 274,
			"versionNonce": 205360386,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946290992,
			"created": 1792945849867,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1180.5421815542913,
					2854.520414882654
				]
			],
			"startBinding": {
				"elementId": "qvrFhxju",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "odJVWkXGMXdbZOsWxXYwx",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					0
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "RRWJG8hs4C8LslUVod7Li",
			"type": "rectangle",
			"x": -2901.4893919637557,
			"y": 3373.7227324724777,
			"width": 470.5625442609373,
			"height": 318.2594309963568,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"lGDL7IRts_wUc7_y89kNj"
			],
			"frameId": null,
			"index": "bAw",
			"roundness": {
				"type": 3
			},
			"seed": 1670868190,
			"version": 2523,
			"versionNonce": 1401094046,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XJyhc6U3"
				},
				{
					"id": "x7NDITGN",
					"type": "arrow"
				},
				{
					"id": "UZpKCs31",
					"type": "arrow"
				},
				{
					"id": "qmApG4e7",
					"type": "arrow"
				}
			],
			"updated": 1792946933368,
			"created": 1792945899700,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "XJyhc6U3",
			"type": "text",
			"x": -2896.4893919637557,
			"y": 3392.852447970656,
			"width": 428.6311340332031,
			"height": 280,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"lGDL7IRts_wUc7_y89kNj"
			],
			"frameId": null,
			"index": "bAx",
			"roundness": null,
			"seed": 1175593246,
			"version": 3466,
			"versionNonce": 362758046,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945984251,
			"created": 1792945899700,
			"locked": false,
			"text": "Shell startup files: \n\nKhi Shell được mở, hệ điều hành\nđi tìm và đọc file cấu hình để\nthiết lập môi trường làm việc\n\nVD: Terminal kích hoạt Zsh ->\nđọc ~/.zshrc",
			"rawText": "Shell startup files: \n\nKhi Shell được mở, hệ điều hành đi tìm và đọc file cấu hình để thiết lập môi trường làm việc\n\nVD: Terminal kích hoạt Zsh -> đọc ~/.zshrc",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "middle",
			"containerId": "RRWJG8hs4C8LslUVod7Li",
			"originalText": "Shell startup files: \n\nKhi Shell được mở, hệ điều hành đi tìm và đọc file cấu hình để thiết lập môi trường làm việc\n\nVD: Terminal kích hoạt Zsh -> đọc ~/.zshrc",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "x7NDITGN",
			"type": "arrow",
			"x": -2269.4632048467624,
			"y": 3529.9912286644953,
			"width": 155.96364285605569,
			"height": 2.7944983033994504,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bAy",
			"roundness": {
				"type": 2
			},
			"seed": 1310332354,
			"version": 120,
			"versionNonce": 295404866,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946290825,
			"created": 1792945920202,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-155.96364285605569,
					2.7944983033994504
				]
			],
			"startBinding": {
				"elementId": "odJVWkXGMXdbZOsWxXYwx",
				"mode": "inside",
				"fixedPoint": [
					0.009995899357062207,
					0.492967702967516
				]
			},
			"endBinding": {
				"elementId": "RRWJG8hs4C8LslUVod7Li",
				"mode": "orbit",
				"fixedPoint": [
					0.9999999999999997,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "D5jacCMcflzfzemyzOyOR",
			"type": "rectangle",
			"x": -3507.1281075314955,
			"y": 3382.651243394299,
			"width": 470.5625442609373,
			"height": 318.2594309963568,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffec99",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"41BjOGt43FYR64bDCfMZf"
			],
			"frameId": null,
			"index": "bAz",
			"roundness": {
				"type": 3
			},
			"seed": 1930466242,
			"version": 2556,
			"versionNonce": 541573442,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "i1se7seC"
				},
				{
					"id": "UZpKCs31",
					"type": "arrow"
				},
				{
					"id": "BptAaT3U",
					"type": "arrow"
				},
				{
					"id": "D5muilQe",
					"type": "arrow"
				}
			],
			"updated": 1792946348140,
			"created": 1792945964794,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "i1se7seC",
			"type": "text",
			"x": -3502.1281075314955,
			"y": 3401.7809588924774,
			"width": 407.9458923339844,
			"height": 280,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"41BjOGt43FYR64bDCfMZf"
			],
			"frameId": null,
			"index": "bB0",
			"roundness": null,
			"seed": 1225575298,
			"version": 3507,
			"versionNonce": 823706178,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945981573,
			"created": 1792945964794,
			"locked": false,
			"text": "2 types variables:\n \n- Local variables: Biến nội bộ\ntrong process đó \n\n- Environment variables: Biến\nđược exported, có thể truyền\nvào process con",
			"rawText": "2 types variables:\n \n- Local variables: Biến nội bộ trong process đó \n\n- Environment variables: Biến được exported, có thể truyền vào process con",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "middle",
			"containerId": "D5jacCMcflzfzemyzOyOR",
			"originalText": "2 types variables:\n \n- Local variables: Biến nội bộ trong process đó \n\n- Environment variables: Biến được exported, có thể truyền vào process con",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "UZpKCs31",
			"type": "arrow",
			"x": -2906.9893919637557,
			"y": 3533.247822936466,
			"width": 124.07617130680319,
			"height": 8.201412876401719,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bB1",
			"roundness": {
				"type": 2
			},
			"seed": 1800285250,
			"version": 19,
			"versionNonce": 726988382,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792945971182,
			"created": 1792945967827,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-124.07617130680319,
					8.201412876401719
				]
			],
			"startBinding": {
				"elementId": "RRWJG8hs4C8LslUVod7Li",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "D5jacCMcflzfzemyzOyOR",
				"mode": "orbit",
				"fixedPoint": [
					0.9999999999999997,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "j2c2ZHeo",
			"type": "text",
			"x": -4087.30930205619,
			"y": 3425.3709394883854,
			"width": 349.83184814453125,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bB2",
			"roundness": null,
			"seed": 413827742,
			"version": 461,
			"versionNonce": 207922626,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "BptAaT3U",
					"type": "arrow"
				},
				{
					"id": "6DGgrib5",
					"type": "arrow"
				}
			],
			"updated": 1792946090341,
			"created": 1792946044599,
			"locked": false,
			"text": "show 2 types + functions",
			"rawText": "show 2 types + functions",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "show 2 types + functions",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "BptAaT3U",
			"type": "arrow",
			"x": -3512.6281075314955,
			"y": 3539.4504560164987,
			"width": 219.3493463801633,
			"height": 94.21368770903564,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bB3",
			"roundness": {
				"type": 2
			},
			"seed": 624925442,
			"version": 34,
			"versionNonce": 1473073310,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946348141,
			"created": 1792946081245,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-219.3493463801633,
					-94.21368770903564
				]
			],
			"startBinding": {
				"elementId": "D5jacCMcflzfzemyzOyOR",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "j2c2ZHeo",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "k9Vq9g5_dRxeZ7UOvWI3c",
			"type": "rectangle",
			"x": -4632.41783875975,
			"y": 3412.275091764969,
			"width": 314.7591906879011,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bB4",
			"roundness": {
				"type": 3
			},
			"seed": 2133026718,
			"version": 1410,
			"versionNonce": 1156395230,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "G7nDtK1X"
				},
				{
					"id": "6DGgrib5",
					"type": "arrow"
				}
			],
			"updated": 1792946379192,
			"created": 1792946085593,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "G7nDtK1X",
			"type": "text",
			"x": -4497.900235298124,
			"y": 3423.6854664351767,
			"width": 45.72398376464844,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bB5",
			"roundness": null,
			"seed": 1808843742,
			"version": 1520,
			"versionNonce": 1008926,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946379192,
			"created": 1792946085593,
			"locked": false,
			"text": "set",
			"rawText": "set",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "k9Vq9g5_dRxeZ7UOvWI3c",
			"originalText": "set",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "6DGgrib5",
			"type": "arrow",
			"x": -4092.8093020561896,
			"y": 3442.834250312507,
			"width": 219.3493460156592,
			"height": 1.6028126265173341,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bB6",
			"roundness": {
				"type": 2
			},
			"seed": 471002754,
			"version": 31,
			"versionNonce": 962662750,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946379193,
			"created": 1792946090340,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-219.3493460156592,
					-1.6028126265173341
				]
			],
			"startBinding": {
				"elementId": "j2c2ZHeo",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "k9Vq9g5_dRxeZ7UOvWI3c",
				"mode": "orbit",
				"fixedPoint": [
					1.0000000000000016,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "ydNjDxCb",
			"type": "text",
			"x": -4059.5545921003277,
			"y": 3620.730295986804,
			"width": 333.89984130859375,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bB7",
			"roundness": null,
			"seed": 1133456158,
			"version": 69,
			"versionNonce": 43374786,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "D5muilQe",
					"type": "arrow"
				},
				{
					"id": "iGWXOGqh",
					"type": "arrow"
				}
			],
			"updated": 1792946348140,
			"created": 1792946094410,
			"locked": false,
			"text": "show only env_variables ",
			"rawText": "show only env_variables ",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "show only env_variables ",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "D5muilQe",
			"type": "arrow",
			"x": -3512.6281075314955,
			"y": 3544.2395624285514,
			"width": 207.52664326023887,
			"height": 91.5674559652789,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bB8",
			"roundness": {
				"type": 2
			},
			"seed": 743727618,
			"version": 61,
			"versionNonce": 394381762,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946348139,
			"created": 1792946121557,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-207.52664326023887,
					91.5674559652789
				]
			],
			"startBinding": {
				"elementId": "D5jacCMcflzfzemyzOyOR",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "ydNjDxCb",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "3x_EjnVk9zpJDHW_sJb63",
			"type": "rectangle",
			"x": -4626.917839081002,
			"y": 3585.9106742410568,
			"width": 314.7591906879011,
			"height": 115,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bB9",
			"roundness": {
				"type": 3
			},
			"seed": 625493058,
			"version": 1485,
			"versionNonce": 2095221854,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "yEM245hH"
				},
				{
					"id": "iGWXOGqh",
					"type": "arrow"
				}
			],
			"updated": 1792946348140,
			"created": 1792946125224,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "yEM245hH",
			"type": "text",
			"x": -4602.216191735099,
			"y": 3590.9106742410568,
			"width": 265.35589599609375,
			"height": 105,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBA",
			"roundness": null,
			"seed": 704277506,
			"version": 1651,
			"versionNonce": 1013486466,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946151170,
			"created": 1792946125224,
			"locked": false,
			"text": "printenv \n||\nprintenv \"var_name\"",
			"rawText": "printenv \n||\nprintenv \"var_name\"",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "3x_EjnVk9zpJDHW_sJb63",
			"originalText": "printenv \n||\nprintenv \"var_name\"",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "iGWXOGqh",
			"type": "arrow",
			"x": -4065.054592100328,
			"y": 3638.346763612174,
			"width": 241.60405629277238,
			"height": 4.962443003511908,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBB",
			"roundness": {
				"type": 2
			},
			"seed": 2138555138,
			"version": 50,
			"versionNonce": 1906977630,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946348139,
			"created": 1792946128485,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-241.60405629277238,
					4.962443003511908
				]
			],
			"startBinding": {
				"elementId": "ydNjDxCb",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "3x_EjnVk9zpJDHW_sJb63",
				"mode": "orbit",
				"fixedPoint": [
					1.0000000000000016,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "xjZWezRH",
			"type": "text",
			"x": -2766.212848631492,
			"y": 4346.104143976251,
			"width": 418.767822265625,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBC",
			"roundness": null,
			"seed": 245961118,
			"version": 260,
			"versionNonce": 766474974,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "0oi7xlAl",
					"type": "arrow"
				},
				{
					"id": "KaDQym8u",
					"type": "arrow"
				}
			],
			"updated": 1792946394333,
			"created": 1792946349935,
			"locked": false,
			"text": "pass variables to child process",
			"rawText": "pass variables to child process",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "pass variables to child process",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "0oi7xlAl",
			"type": "arrow",
			"x": -2276.2597042618154,
			"y": 3585.9006432400897,
			"width": 69.11700329228279,
			"height": 755.1101140145934,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBD",
			"roundness": {
				"type": 2
			},
			"seed": 543253890,
			"version": 121,
			"versionNonce": 1844997918,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946394334,
			"created": 1792946374668,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-69.11700329228279,
					755.1101140145934
				]
			],
			"startBinding": {
				"elementId": "odJVWkXGMXdbZOsWxXYwx",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "xjZWezRH",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "A9bYrQK2",
			"type": "rectangle",
			"x": -3216.1937282220306,
			"y": 4335.615112560095,
			"width": 314.7591906879011,
			"height": 57.82074934041566,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBE",
			"roundness": {
				"type": 3
			},
			"seed": 846493342,
			"version": 1535,
			"versionNonce": 451685214,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "NaHf6aKj"
				},
				{
					"id": "KaDQym8u",
					"type": "arrow"
				},
				{
					"id": "bHlLrvMz",
					"type": "arrow"
				}
			],
			"updated": 1792946937256,
			"created": 1792946382505,
			"link": "[[export]]",
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "NaHf6aKj",
			"type": "text",
			"x": -3104.454109379545,
			"y": 4347.025487230303,
			"width": 91.27995300292969,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBF",
			"roundness": null,
			"seed": 1344795358,
			"version": 1669,
			"versionNonce": 816506626,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946463413,
			"created": 1792946382505,
			"locked": false,
			"text": "export",
			"rawText": "export",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "A9bYrQK2",
			"originalText": "export",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "KaDQym8u",
			"type": "arrow",
			"x": -2771.712848631492,
			"y": 4363.645211465243,
			"width": 124.22168890263765,
			"height": 0.8484903510006916,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBG",
			"roundness": {
				"type": 2
			},
			"seed": 1087413598,
			"version": 120,
			"versionNonce": 1585100482,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946463413,
			"created": 1792946387194,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-124.22168890263765,
					0.8484903510006916
				]
			],
			"startBinding": {
				"elementId": "xjZWezRH",
				"mode": "orbit",
				"fixedPoint": [
					0,
					0.5001
				]
			},
			"endBinding": {
				"elementId": "A9bYrQK2",
				"mode": "orbit",
				"fixedPoint": [
					1,
					0.5001
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false,
			"hasTextLink": false
		},
		{
			"id": "quYLVbsA",
			"type": "text",
			"x": -3274.203402847393,
			"y": 3878.8550447946586,
			"width": 459.311767578125,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"aNv3hBx1yZJlrdFPip6lZ"
			],
			"frameId": null,
			"index": "bBX",
			"roundness": null,
			"seed": 86320798,
			"version": 2133,
			"versionNonce": 58646914,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1792946941180,
			"created": 1792946799200,
			"locked": false,
			"text": "add var in current shell: foo=\"bar\"",
			"rawText": "add var in current shell: foo=\"bar\"",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "add var in current shell: foo=\"bar\"",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false
		},
		{
			"id": "l5alMI3yAH0xXmxY7MhW8",
			"type": "rectangle",
			"x": -3399.8103206826763,
			"y": 3847.0291963655923,
			"width": 731.0617804483531,
			"height": 321.7714842285397,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"aNv3hBx1yZJlrdFPip6lZ"
			],
			"frameId": null,
			"index": "bBY",
			"roundness": {
				"type": 3
			},
			"seed": 1765974750,
			"version": 2714,
			"versionNonce": 1508598082,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "qmApG4e7",
					"type": "arrow"
				},
				{
					"id": "bHlLrvMz",
					"type": "arrow"
				}
			],
			"updated": 1792946941180,
			"created": 1792946799200,
			"link": null,
			"locked": false,
			"hasTextLink": false
		},
		{
			"id": "Z6jyfmLOL6lKT985yrxyW",
			"type": "freedraw",
			"x": -3142.2138974639633,
			"y": 3948.919821188521,
			"width": 98.61733554223292,
			"height": 144.7240948167696,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"aNv3hBx1yZJlrdFPip6lZ"
			],
			"frameId": null,
			"index": "bBZ",
			"roundness": null,
			"seed": 1942385154,
			"version": 49,
			"versionNonce": 1449726082,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1792946941180,
			"created": 1792946842485,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					1.2807243134311648,
					0
				],
				[
					1.2807243134311648,
					6.4037192801579295
				],
				[
					-1.2808220264332704,
					17.93043352704217
				],
				[
					-7.6845413065912,
					34.58014274065363
				],
				[
					-16.64970921361146,
					51.22975424126298
				],
				[
					-26.895699147064988,
					67.87946345487444
				],
				[
					-39.70313770738085,
					83.24835064205263
				],
				[
					-52.510576267696706,
					99.89805985566409
				],
				[
					-62.75646848814813,
					111.42477410254878
				],
				[
					-75.56390704846399,
					121.6706663230002
				],
				[
					-85.80989698191752,
					131.91665625645373
				],
				[
					-92.21361626207499,
					139.60109985004283
				],
				[
					-97.33661122880176,
					143.44337050333843
				],
				[
					-97.33661122880176,
					144.7240948167696
				],
				[
					-97.33661122880176,
					144.7240948167696
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			}
		},
		{
			"id": "j3bofhxv1y5sbQcMqZxmM",
			"type": "freedraw",
			"x": -3080.7382510022485,
			"y": 3947.6390968750898,
			"width": 208.76128761834843,
			"height": 119.10921769613788,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"aNv3hBx1yZJlrdFPip6lZ"
			],
			"frameId": null,
			"index": "bBa",
			"roundness": null,
			"seed": 128350622,
			"version": 47,
			"versionNonce": 1303883842,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1792946941180,
			"created": 1792946844589,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					3.842270653295145
				],
				[
					15.36898490017984,
					10.245989933453075
				],
				[
					30.737872087358483,
					19.211157840473334
				],
				[
					51.229754241263436,
					33.29932071422081
				],
				[
					76.84463136189515,
					48.66830561440065
				],
				[
					107.58250344925318,
					64.03719280157884
				],
				[
					137.03965122318004,
					78.12535567532586
				],
				[
					163.93525265724338,
					93.49434057550616
				],
				[
					188.26930775144228,
					106.30177913582202
				],
				[
					202.3575683381905,
					113.98622272941111
				],
				[
					207.48046559191607,
					119.10921769613788
				],
				[
					208.76128761834843,
					119.10921769613788
				],
				[
					208.76128761834843,
					119.10921769613788
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			}
		},
		{
			"id": "1H1vJd2k",
			"type": "text",
			"x": -3385.60596266421,
			"y": 3969.764246884964,
			"width": 174.1879119873047,
			"height": 70,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"aNv3hBx1yZJlrdFPip6lZ"
			],
			"frameId": null,
			"index": "bBb",
			"roundness": null,
			"seed": 1793546590,
			"version": 114,
			"versionNonce": 1771853826,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1792946941180,
			"created": 1792946849228,
			"locked": false,
			"text": "pass to \nchild process",
			"rawText": "pass to \nchild process",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "pass to \nchild process",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false
		},
		{
			"id": "bUPZ59cZ",
			"type": "text",
			"x": -3340.2040627355486,
			"y": 4099.889775136422,
			"width": 149.9959259033203,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"aNv3hBx1yZJlrdFPip6lZ"
			],
			"frameId": null,
			"index": "bBc",
			"roundness": null,
			"seed": 1600755202,
			"version": 78,
			"versionNonce": 974522306,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1792946941180,
			"created": 1792946865646,
			"locked": false,
			"text": "export foo",
			"rawText": "export foo",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "export foo",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false
		},
		{
			"id": "Rvzm03PJ",
			"type": "text",
			"x": -2976.8126084033133,
			"y": 3967.182392416355,
			"width": 279.35589599609375,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"aNv3hBx1yZJlrdFPip6lZ"
			],
			"frameId": null,
			"index": "bBd",
			"roundness": null,
			"seed": 1063591134,
			"version": 82,
			"versionNonce": 2000928642,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1792946941180,
			"created": 1792946888226,
			"locked": false,
			"text": "make var persistent ",
			"rawText": "make var persistent ",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "make var persistent ",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false
		},
		{
			"id": "bIxQYPU6",
			"type": "text",
			"x": -3033.783775019687,
			"y": 4081.3003914456585,
			"width": 356.6358642578125,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"aNv3hBx1yZJlrdFPip6lZ"
			],
			"frameId": null,
			"index": "bBe",
			"roundness": null,
			"seed": 2131663554,
			"version": 124,
			"versionNonce": 2103738178,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1792946941180,
			"created": 1792946896384,
			"locked": false,
			"text": "add to .zshrc + . ~/.zshrc",
			"rawText": "add to .zshrc + . ~/.zshrc",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "add to .zshrc + . ~/.zshrc",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false
		},
		{
			"id": "qmApG4e7",
			"type": "arrow",
			"x": -2679.2167725211066,
			"y": 3697.4821634688346,
			"width": 341.9338428171027,
			"height": 144.04703289675808,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBf",
			"roundness": {
				"type": 2
			},
			"seed": 1254669022,
			"version": 92,
			"versionNonce": 1618415454,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1792946950285,
			"created": 1792946933367,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-341.9338428171027,
					144.04703289675808
				]
			],
			"startBinding": {
				"elementId": "RRWJG8hs4C8LslUVod7Li",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					1.0000000000000004
				]
			},
			"endBinding": {
				"elementId": "l5alMI3yAH0xXmxY7MhW8",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					0
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false
		},
		{
			"id": "bHlLrvMz",
			"type": "arrow",
			"x": -3057.972356386458,
			"y": 4330.1151125600945,
			"width": 22.95573153345049,
			"height": 155.81443196596229,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBg",
			"roundness": {
				"type": 2
			},
			"seed": 1641959070,
			"version": 126,
			"versionNonce": 1738716674,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1792946948004,
			"created": 1792946937255,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					22.95573153345049,
					-155.81443196596229
				]
			],
			"startBinding": {
				"elementId": "A9bYrQK2",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					0
				]
			},
			"endBinding": {
				"elementId": "l5alMI3yAH0xXmxY7MhW8",
				"mode": "orbit",
				"fixedPoint": [
					0.5001,
					1.0000000000000009
				]
			},
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"elbowed": false,
			"moveMidPointsWithElement": false
		},
		{
			"id": "xegYGzEK",
			"type": "text",
			"x": -3041.587596242666,
			"y": 3985.50014430151,
			"width": 11.199996948242188,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBIG",
			"roundness": null,
			"seed": 1629111490,
			"version": 3,
			"versionNonce": 446223298,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1792946925094,
			"created": 1792946924500,
			"locked": false,
			"text": "",
			"rawText": "",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "l5alMI3yAH0xXmxY7MhW8",
			"originalText": "",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false
		},
		{
			"id": "ok6FZ7tc",
			"type": "text",
			"x": -3041.587596242666,
			"y": 3985.50014430151,
			"width": 11.199996948242188,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBIV",
			"roundness": null,
			"seed": 890118814,
			"version": 3,
			"versionNonce": 1139860382,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1792946924269,
			"created": 1792946923724,
			"locked": false,
			"text": "",
			"rawText": "",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "l5alMI3yAH0xXmxY7MhW8",
			"originalText": "",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false
		},
		{
			"id": "N9iFuPBg",
			"type": "text",
			"x": -3182.4733817701226,
			"y": 4136.613326738228,
			"width": 102.92796325683594,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBJ",
			"roundness": null,
			"seed": 484874014,
			"version": 537,
			"versionNonce": 187782082,
			"isDeleted": true,
			"boundElements": [],
			"updated": 1792946832115,
			"created": 1792946799200,
			"locked": false,
			"text": "process",
			"rawText": "process",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "process",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "n7nBEMzZ5IRmxYcz7Iaee",
			"type": "freedraw",
			"x": -3112.988346622502,
			"y": 3905.5134685820776,
			"width": 22.86662924161692,
			"height": 203.97032585688066,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBK",
			"roundness": null,
			"seed": 1484915550,
			"version": 548,
			"versionNonce": 116966914,
			"isDeleted": true,
			"boundElements": [],
			"updated": 1792946830300,
			"created": 1792946799200,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.9147209963962268,
					4.573325848323293
				],
				[
					2.743953638945186,
					13.719977544969879
				],
				[
					6.4026282742870535,
					27.439955089940213
				],
				[
					10.975954122610347,
					46.647944587922666
				],
				[
					15.54927997093364,
					69.51457382953959
				],
				[
					20.122605819256933,
					95.12519160180864
				],
				[
					21.951908245220693,
					119.82115816109626
				],
				[
					21.951908245220693,
					138.1144615543899
				],
				[
					21.951908245220693,
					155.49311373470118
				],
				[
					21.951908245220693,
					170.1277424926534
				],
				[
					19.207954606275507,
					181.10369661526374
				],
				[
					17.3785823968974,
					186.59174345998326
				],
				[
					16.46393118391552,
					192.07972052128844
				],
				[
					13.719977544970334,
					194.82367416023362
				],
				[
					11.890605335592227,
					197.5676975825936
				],
				[
					10.061302909628466,
					202.1410234309169
				],
				[
					9.146651696646586,
					203.97032585688066
				],
				[
					8.23193070025036,
					203.97032585688066
				],
				[
					8.23193070025036,
					203.97032585688066
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "cPDw7dVzen_KEALq6UuaQ",
			"type": "freedraw",
			"x": -3112.988346622502,
			"y": 4096.678537890384,
			"width": 39.33056042553244,
			"height": 25.610582880562106,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBL",
			"roundness": null,
			"seed": 509994910,
			"version": 552,
			"versionNonce": 917004510,
			"isDeleted": true,
			"boundElements": [],
			"updated": 1792946831535,
			"created": 1792946799200,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-1.829372209378107
				],
				[
					0,
					-0.9147209963962268
				],
				[
					2.743953638945186,
					0
				],
				[
					3.658604851927066,
					3.658604851927066
				],
				[
					4.573325848323293,
					5.487977061305173
				],
				[
					6.4026282742870535,
					9.146651696646586
				],
				[
					6.4026282742870535,
					12.805256548574107
				],
				[
					7.317279487268479,
					13.719977544969879
				],
				[
					8.23193070025036,
					15.54927997093364
				],
				[
					9.146651696646586,
					15.54927997093364
				],
				[
					9.146651696646586,
					17.3785823968974
				],
				[
					10.975954122610347,
					17.3785823968974
				],
				[
					11.890605335592227,
					16.46393118391552
				],
				[
					12.805256548573652,
					16.46393118391552
				],
				[
					13.719977544970334,
					14.63462875795176
				],
				[
					15.54927997093364,
					11.890605335592227
				],
				[
					17.3785823968974,
					9.146651696646586
				],
				[
					21.951908245220693,
					4.573325848323293
				],
				[
					26.525234093543986,
					0
				],
				[
					33.842583364227266,
					-4.573325848323293
				],
				[
					35.67188579019057,
					-7.31734927068328
				],
				[
					39.33056042553244,
					-8.232000483664706
				],
				[
					39.33056042553244,
					-8.232000483664706
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "vyBAf8CJ",
			"type": "text",
			"x": -3059.4480496444976,
			"y": 3980.3946716532337,
			"width": 370.8318176269531,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBM",
			"roundness": null,
			"seed": 2126726110,
			"version": 624,
			"versionNonce": 1502454430,
			"isDeleted": true,
			"boundElements": [],
			"updated": 1792946829864,
			"created": 1792946799200,
			"locked": false,
			"text": "sends \"signal\" to processes",
			"rawText": "sends \"signal\" to processes",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "sends \"signal\" to processes",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false,
			"link": null
		},
		{
			"id": "kmd-E4JId9HEvKxsPcKyB",
			"type": "freedraw",
			"x": -2886.1514264157113,
			"y": 3968.6253792456228,
			"width": 107.93051793379709,
			"height": 113.41849499510226,
			"angle": 0,
			"strokeColor": "#e03131",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBN",
			"roundness": null,
			"seed": 1537939486,
			"version": 565,
			"versionNonce": 665195266,
			"isDeleted": true,
			"boundElements": [],
			"updated": 1792946833292,
			"created": 1792946799200,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-2.7439885306525866
				],
				[
					-1.8293024259637605,
					-8.232000483664706
				],
				[
					-7.31734927068328,
					-13.719977544969879
				],
				[
					-13.719977544970334,
					-16.463966075622466
				],
				[
					-24.695931667580226,
					-20.122640710964333
				],
				[
					-36.586606786587254,
					-21.95197802863504
				],
				[
					-48.47728190559337,
					-21.95197802863504
				],
				[
					-58.53851503180749,
					-21.03729192394576
				],
				[
					-68.5998877248503,
					-13.719977544969879
				],
				[
					-79.57584184746065,
					-5.487977061305173
				],
				[
					-86.89319111814393,
					5.487977061305173
				],
				[
					-93.29581939243099,
					19.207954606275507
				],
				[
					-95.12512181839429,
					36.5866067865868
				],
				[
					-95.12512181839429,
					52.13592164922784
				],
				[
					-92.38109839603476,
					68.5999226165577
				],
				[
					-85.06388869218063,
					79.57587673916805
				],
				[
					-71.34391114721029,
					86.89322600985133
				],
				[
					-54.879910179880426,
					88.72252843581464
				],
				[
					-39.330630208946786,
					88.72252843581464
				],
				[
					-21.951908245220693,
					80.49052795214993
				],
				[
					-8.231930700250814,
					68.5999226165577
				],
				[
					0.9147209963962268,
					54.879910179880426
				],
				[
					8.232070267079507,
					39.330595317239386
				],
				[
					10.975954122610347,
					27.439955089940213
				],
				[
					10.975954122610347,
					11.890640227299627
				],
				[
					12.8053961154028,
					0
				],
				[
					12.8053961154028,
					-10.975989014317292
				],
				[
					10.975954122610347,
					-18.293303393293172
				],
				[
					5.48804684471952,
					-21.95197802863504
				],
				[
					-1.8293024259637605,
					-24.695966559287626
				],
				[
					-10.975954122610347,
					-24.695966559287626
				],
				[
					-20.122605819256933,
					-21.95197802863504
				],
				[
					-25.610652663976907,
					-17.378652180311747
				],
				[
					-31.09855994186728,
					-11.890640227299173
				],
				[
					-32.013280938263506,
					-10.061302909628466
				],
				[
					-32.013280938263506,
					-10.061302909628466
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			},
			"hasTextLink": false
		},
		{
			"id": "uy3Ej5_slN2HRgM1JzOnf",
			"type": "freedraw",
			"x": -3090.5896824606243,
			"y": 3930.372107338711,
			"width": 106.30177913582202,
			"height": 126.79366128972697,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBO",
			"roundness": null,
			"seed": 2087724354,
			"version": 37,
			"versionNonce": 1898491970,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1792946840000,
			"created": 1792946839016,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-1.2807243134311648
				],
				[
					-3.8422706532956,
					2.5615463398639804
				],
				[
					-6.4037192801579295,
					8.96526562002191
				],
				[
					-15.368984900180294,
					19.21115784047379
				],
				[
					-24.334152807200553,
					29.457147773926863
				],
				[
					-34.58014274065408,
					40.98386202081156
				],
				[
					-40.98386202081201,
					49.949029927831816
				],
				[
					-49.94902992783227,
					62.756468488147675
				],
				[
					-57.633473521421365,
					73.0024584216012
				],
				[
					-66.59873914144373,
					79.40617770175913
				],
				[
					-73.0024584216012,
					85.80989698191706
				],
				[
					-75.56390704846399,
					92.21361626207499
				],
				[
					-79.40617770175913,
					94.77506488893732
				],
				[
					-80.68690201519075,
					96.05578920236849
				],
				[
					-81.96762632862192,
					99.89805985566409
				],
				[
					-83.24835064205308,
					99.89805985566409
				],
				[
					-85.80989698191706,
					101.17878416909525
				],
				[
					-85.80989698191706,
					102.45950848252642
				],
				[
					-85.80989698191706,
					105.02105482239085
				],
				[
					-87.09062129534868,
					105.02105482239085
				],
				[
					-88.37134560877985,
					106.30177913582202
				],
				[
					-92.21361626207499,
					108.86322776268435
				],
				[
					-93.49434057550661,
					113.98622272941111
				],
				[
					-94.77506488893778,
					115.26694704284228
				],
				[
					-96.05578920236894,
					117.82849338270671
				],
				[
					-99.89805985566454,
					117.82849338270671
				],
				[
					-101.1787841690957,
					119.10921769613788
				],
				[
					-101.1787841690957,
					120.38994200956904
				],
				[
					-102.45950848252687,
					120.38994200956904
				],
				[
					-105.02105482239085,
					121.6706663230002
				],
				[
					-105.02105482239085,
					124.23221266286464
				],
				[
					-106.30177913582202,
					124.23221266286464
				],
				[
					-106.30177913582202,
					125.5129369762958
				],
				[
					-106.30177913582202,
					125.5129369762958
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			}
		},
		{
			"id": "lLnUsQi27C5FG32AG2i7R",
			"type": "freedraw",
			"x": -3104.6778453343713,
			"y": 3949.5832651791848,
			"width": 81.96762632862192,
			"height": 121.67066632300066,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBP",
			"roundness": null,
			"seed": 993370398,
			"version": 17,
			"versionNonce": 1968731038,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1792946840850,
			"created": 1792946840245,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-1.2807243134316195
				],
				[
					-1.2808220264332704,
					3.842270653295145
				],
				[
					-5.122994966726765,
					12.807438560315859
				],
				[
					-14.08826058674913,
					28.1764234604957
				],
				[
					-24.334152807200553,
					47.38758130096949
				],
				[
					-37.14159136751641,
					66.59873914144328
				],
				[
					-49.94902992783227,
					83.24835064205263
				],
				[
					-61.475744174716965,
					94.77506488893732
				],
				[
					-69.16018776830606,
					105.02105482239085
				],
				[
					-75.56390704846399,
					112.70549841597995
				],
				[
					-80.68690201519075,
					115.26694704284228
				],
				[
					-81.96762632862192,
					119.10921769613788
				],
				[
					-81.96762632862192,
					120.38994200956904
				],
				[
					-81.96762632862192,
					120.38994200956904
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			}
		},
		{
			"id": "AW6GYJPcwhsw6CCwW4LBN",
			"type": "freedraw",
			"x": -3095.712677427351,
			"y": 3934.214377992006,
			"width": 99.89805985566409,
			"height": 134.47810488331652,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBQ",
			"roundness": null,
			"seed": 1972348162,
			"version": 18,
			"versionNonce": 783660702,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1792946842278,
			"created": 1792946841643,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					6.4037192801579295
				],
				[
					-5.122994966726765,
					17.930433527042624
				],
				[
					-10.24598993345353,
					30.737872087358483
				],
				[
					-17.930433527042624,
					44.826034961105506
				],
				[
					-26.895601434062883,
					58.91419783485253
				],
				[
					-38.42231568094758,
					75.56390704846399
				],
				[
					-48.668305614401106,
					88.37134560877985
				],
				[
					-58.91419783485253,
					101.1787841690957
				],
				[
					-69.16018776830606,
					108.8632277626848
				],
				[
					-75.56390704846399,
					115.26694704284273
				],
				[
					-83.24835064205308,
					121.67066632300066
				],
				[
					-90.93279423564218,
					126.79366128972742
				],
				[
					-97.3365135158001,
					130.63583423002092
				],
				[
					-99.89805985566409,
					134.47810488331652
				],
				[
					-99.89805985566409,
					134.47810488331652
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"strokeOptions": {
				"variability": "constant",
				"streamline": 0.5
			}
		},
		{
			"id": "547H8LF5",
			"type": "text",
			"x": -3237.711916111436,
			"y": 3935.2851248192637,
			"width": 11.199996948242188,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBT",
			"roundness": null,
			"seed": 1431973058,
			"version": 3,
			"versionNonce": 396584002,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1792946848069,
			"created": 1792946847405,
			"locked": false,
			"text": "",
			"rawText": "",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false
		},
		{
			"id": "QKHClC94",
			"type": "text",
			"x": -2951.847909050018,
			"y": 3942.6455279141574,
			"width": 11.199996948242188,
			"height": 35,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"index": "bBW",
			"roundness": null,
			"seed": 1294774658,
			"version": 3,
			"versionNonce": 1789638914,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1792946877133,
			"created": 1792946874158,
			"locked": false,
			"text": "",
			"rawText": "",
			"fontSize": 28,
			"baseFontSize": null,
			"fontFamily": 5,
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "",
			"autoResize": true,
			"lineHeight": 1.25,
			"labelPosition": null,
			"hasTextLink": false
		}
	],
	"appState": {
		"theme": "light",
		"viewBackgroundColor": "#ffffff",
		"currentItemStrokeColor": "#1e1e1e",
		"currentItemBackgroundColor": "#ffc9c9",
		"currentItemFillStyle": "hachure",
		"currentItemStickynoteStrokeColor": "#1e1e1e",
		"currentItemStrokeWidthKey": "thin",
		"currentItemStrokeVariability": "constant",
		"currentItemStrokeStyle": "dashed",
		"currentItemRoughness": 0,
		"currentItemOpacity": 100,
		"currentItemFontFamily": 5,
		"currentItemFontSize": 28,
		"currentItemTextAlign": "center",
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": "arrow",
		"currentItemArrowType": "round",
		"currentItemFrameRole": null,
		"scrollX": 4687.272871472618,
		"scrollY": -2500.9478025453263,
		"zoom": {
			"value": 0.474637
		},
		"currentItemRoundness": "round",
		"gridSize": 20,
		"gridStep": 5,
		"gridModeEnabled": false,
		"gridColor": {
			"Bold": "rgba(179, 179, 179, 0.5)",
			"Regular": "rgba(204, 204, 204, 0.5)"
		},
		"colorTopPicks": {
			"elementStroke": null,
			"elementBackground": null,
			"bucketFill": null,
			"stickyNoteStroke": null,
			"stickyNoteBackground": null
		},
		"fontTopPicks": null,
		"currentStrokeOptions": null,
		"frameRendering": {
			"enabled": true,
			"clip": true,
			"name": true,
			"outline": true,
			"markerName": true,
			"markerEnabled": true
		},
		"objectsSnapModeEnabled": false,
		"activeTool": {
			"type": "selection",
			"customType": null,
			"locked": false,
			"fromSelection": false,
			"lastActiveTool": null
		},
		"disableContextMenu": false,
		"bindingPreference": "enabled",
		"isMidpointSnappingEnabled": true,
		"boxSelectionMode": "contain",
		"inputDevice": "auto"
	},
	"files": {}
}
```
%%