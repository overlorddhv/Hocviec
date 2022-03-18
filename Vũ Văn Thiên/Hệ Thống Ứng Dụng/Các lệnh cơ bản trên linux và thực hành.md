## Phím tắt

Lệnh `pwd` Hiển thị vị trí hiện tại trong hệ thống file.

![image](https://user-images.githubusercontent.com/62273292/158973004-bd5e09f3-52a2-43f8-b093-b7df249a5292.png)


Lệnh `whoami` Hiển thị tên người dùng - hữu ích nhất nếu chuyển đổi người dùng bằng lệnh su và cần được nhắc nhở về tài khoản nào đang được sử dụng

![image](https://user-images.githubusercontent.com/62273292/158973852-bb9d138c-de24-49c8-8545-0e635db97373.png)

Lệnh `ls` Cung cấp một danh sách file. Với tham số -a, lệnh hiển thị các file có tên bắt đầu bằng dấu chấm (ví dụ: .bashrc). Với tham số -l, lệnh hiển thị quyền, kích thước file và ngày/giờ cập nhật mới nhất.

Lệnh `ls -l`

![image](https://user-images.githubusercontent.com/62273292/158975410-6ba3fe70-2648-4164-ba84-c2f43a07e765.png)

Lệnh `ls -a` 

![image](https://user-images.githubusercontent.com/62273292/158975568-01184921-febb-4f58-a666-2b77a03acc66.png)

Lệnh `env` 

![image](https://user-images.githubusercontent.com/62273292/158976741-42662b23-f58c-40ab-9c55-5379d2496fe2.png)

Lệnh `history`  Liệt kê các lệnh đã đưa ra trước đó.

![image](https://user-images.githubusercontent.com/62273292/158977036-4b438f4c-1aa9-4284-823e-b8cc42044b9e.png)

Lệnh `passwd` Thay đổi mật khẩu

Lệnh mikdir Tạo một thư mục mới





1. Trong terminal

Ctrl + L: xoá toàn bộ màn hình, giống lệnh clear

Ctrl + D: exit session, giống lệnh exit

Ctrl + R: tìm một lệnh đã chạy trước đây, nhấn Ctrl + R sau đó bắt đầu gõ một phần của câu lệnh, hệ thống sẽ tự hoàn tất phần còn lại dựa trên các câu lệnh đã được thực hiện trước đó

Tab: tự động hoàn tất câu lệnh

Shift + Insert: dán paste nội dung đã copy vào terminal
  
Ctrl + Alt + F2 (Alt + F2 nếu đang ở chế độ console): chuyển sang virtual terminal thứ 2, tương tự với F3, F4 ...
    
## Những lệnh command cơ bản trên Linux
  
  Lệnh liên quan đến hệ thống
  
  exit: thoát khỏi cửa sổ dòng lệnh.
  
  logout: tương tự exit.
  
  reboot: khởi động lại hệ thống.
  
  halt: tắt máy.
  
  startx: khởi động chế độ xwindows từ cửa sổ terminal.
  
  mount: gắn hệ thống tập tin từ một thiết bị lưu trữ vào cây thư mục chính.
  
  unmount: ngược với lệnh mount.
  
## Lệnh thao tác trên tập tin

ls: lấy danh sách tất cả các file và thư mục trong thư mục hiện hành.

pwd: xuất đường dẫn của thư mục làm việc.

cd: thay đổi thư mục làm việc đến một thư mục mới.

mkdir: tạo thư mục mới.

rmdir: xoá thư mục rỗng.

cp: copy một hay nhiều tập tin đến thư mục mới.

mv: đổi tên hay di chuyển tập tin, thư mục.

rm: xóa tập tin.

wc: đếm số dòng, số kí tự… trong tập tin.

touch: tạo một tập tin.

cat: xem nội dung tập tin.

vi: khởi động trình soạn thảo văn bản vi.

df: kiểm tra dung lượng đĩa.

du: xem dung lượng đĩa đã dùng cho một số tập tin nhất định

nano: Khởi dộng trình soạn thảo văn bản nano

less: Xem nội dung tập tin theo dòng

tail: Xem nội dung tập tin (mặc định xem 10 dòng cuối, muốn xem 100 dòng cuối thì dùng lệnh sau: tail 100 tenfile)

more: Xem nội dung tập tin theo trang

head: Xem nội dung tập tin (mặc định xem 10 dòng đầu, muốn xem 100 dòng đầu thì dùng lệnh sau: head 100 tenfile)
  
## Lệnh khi làm việc trên terminal 
  
  clear: xoá trắng cửa sổ dòng lệnh.
  
  date: xem ngày, giờ hệ thống.
  
  cal: xem lịch hệ thống.
  
## Lệnh quản lí hệ thống 
  
  rpm: kiểm tra gói đã cài đặt hay chưa, hoặc cài đặt một gói, hoặc sử dụng để gỡ bỏ một gói.
  
  ps: kiểm tra hệ thống tiến trình đang chạy.
  
  kill: dừng tiến trình khi tiến trình bị treo. Chỉ có người dùng super-user mới có thể dừng tất cả các tiến trình còn người dùng bình thường chỉ có thể dừng tiến      trình mà mình tạo ra.
  
  top: hiển thị sự hoạt động của các tiến trình, đặc biệt là thông tin về tài nguyên hệ thống và việc sử dụng các tài nguyên đó của từng tiến trình.
  
  pstree: hiển thị tất cả các tiến trình dưới dạng cây.
  
  sleep: cho hệ thống ngừng hoạt động trong một khoảng thời gian.
  
  useradd: tạo một người dùng mới.
  
  groupadd: tạo một nhóm người dùng mới.
  
  passwd: thay đổi password cho người dùng.
  
  userdel: xoá người dùng đã tạo.
  
  groupdel: xoá nhóm người dùng đã tạo.
  
  gpasswd: thay đổi password của một nhóm người dùng.
  
  su: cho phép đăng nhập với tư cách người dùng khác.
  
  groups: hiển thị nhóm của user hiện tại.
  
  who: cho biết ai đang đăng nhập hệ thống.
  
  w: tương tự như lệnh who.
  
  man: xem hướng dẫn về dòng lệnh như cú pháp, các tham số…
  
  Để hiểu và sử dụng tốt các câu lệnh trên, các bạn nên sử dụng lệnh man với cú pháp: man ten_cau_lenh để có được những thông tin đầy đủ về chức năng cũng như cú pháp của câu lệnh.
  
## Các câu lệnh kiểm tra thông tin hệ thống (system information) trong Linux
  
  
  **Lệnh Linux	Mô tả**
  
  cat /proc/cpuinfo	Kiểm tra thông tin CPU (số core)
  
  cat /proc/meminfo	Kiểm tra thông tin về RAM đang sử dụng
  
  cat /proc/version	Kiểm tra phiên bản của Kernel Linux
  
  cat /proc/ioports	Xem thông tin port I/O
  
  cat /etc/redhat-release	Kiểm tra phiên bản Centos
  
  uname -a	Kiểm tra các thông tin về Kernel
  
  free -m	Kiểm tra dung lượng RAM còn trống
  
  init 0	Tắt máy (tương đương lệnh shutdown -h now hoặc telinit 0)
  
  df -h	Hiển thị thông tin những file hệ thống, nơi file được lưu hoặc tất cả những file mặc định. Lệnh này có thể xem được dung lượng ổ cứng đã sử dụng và còn trống.
  
  du -sh	Kiểm tra dung lượng thư mục hiện tại
  
  du  -ah	Hiển thị dung lượng của thư mục con và các file trong thư mục hiện tại
  
  du -h –max-depth=1	Hiển thị dung lượng các thư mục con ở cấp 1 (ngay trong thư mục hiện tại)
  
  df	Kiểm tra dung lượng đĩa cứng, các phân vùng đĩa
  
  lspci	Xem thông tin mainboard   /sbin/ifconfig Xem các địa chỉ IP của máy
  
  hostname	Xem tên máy (hostname)
  
  finger user@server	Thu thập thông tin chi tiết về người dùng hiện đang dùng hệ thống
  arch	Kiểm tra kiến trúc của máy (architech)
  
  cat /proc/swaps	Kiểm tra thông tin SWAP của máy (tương tự như virtual RAM của Windows)
  last reboot	Xem lịch sử reboot máy
  
  
## Các lệnh shutdown, restart… trong Linux
   
  Lệnh Linux	Mô tả
  
  logout	Kết thúc session (phiên làm việc) hiện tại
  
  reboot	Khởi động lại máy
  
  shutdown -r now	Khởi động lại máy (tương đương với lệnh reboot)
  
  shutdown -h now	Tắt máy (ngay lập tức)
  
  shutdown -h 9:30	Hẹn giờ tắt máy (schedule) vào lúc 9h30 (tính theo khung 24h)
  
  shutdown -c	Hủy bỏ tất cả các lệnh tắt máy trước đó (các lệnh tắt máy theo schedule)
  
  telinit 0	Tắt máy (tương đương lệnh shutdown -h now)
  
  init 0	Tắt máy (tương đương lệnh shutdown -h now hoặc telinit 0)
  
  exit	Thoát khỏi terminal
  
  halt	Tắt máy (tương tự shutdown)
  
  sleep	Cho hệ thống ngừng hoạt động trong một thời gian (ngủ – tương tự Windows)
  
## Các lệnh về quản lý user trong Linux
  
  
  Lệnh Linux	Mô tả
  
passwd	Đổi mật khẩu (standard user có thể đổi pass của họ còn user root thì thay đổi được password của mọi user)

pwck	Kiểm tra syntax và định dạng của dữ liệu user/password (/etc/passwd)

useradd	Tạo user mới, ví dụ: useradd -c “test user 1” -g group1

userdel	Xóa User

usermod	Thay đổi thông tin user (group, name…)

groupadd	Tạo một nhóm user mới

groupdel	Xóa nhóm user

groupmod	Thay đổi thông tin group, ví dụ, groupmod -n “old group name”  “new name”

who /w	Hiển thị những user đang đăng nhập hệ thống

uname	Hiển thị tên của hệ thống (host)

id	Hiển thị user ID (Chỉ danh của user)

logname	Hiển thị tên user đang login

su	Cho phép đăng nhập với tên user khác (tương tự secondary logon của Windows)

groups	Hiển thị nhóm của user hiện tại

#vi /etc/passwd	Xem danh sách user

#vi /etc/group	Xem danh sách nhóm (group)

chmod [tên file=””][/tên]	Thay đổi quyền cho file/thư mục (chỉ user sở hữu file mới thực hiện được)

chown user [tên file=””][/tên]	Thay đổi chủ sở hữu file/thư mục

chgrp group [file][/file]	Thay đổi group sở hữu file/thư mục
  
## Các lệnh Quản lý services và process trong Linux
  
  Lệnh Linux	Mô tả
  
top	Lệnh top khá giống như Task Manager trong Windows. Nó đưa ra thông tin về tất cả tài nguyên hệ thống, các process đang chạy, tốc độ load trung bình… Lệnh top -d thiết lập khoảng thời gian làm mới lại hệ thống

ps –u username	Kiểm tra những process được thực hiện bởi một user nhất định

ps –U root	Kiểm tra mọi process ngoại trừ những process hệ thống

ps –A	Kiểm tra mọi process trong hệ thống

Ss	Kiểm tra socket đang kết nối

ss –l	Hiển thị các cổng đang mở

w username	Kiểm tra user đăng nhập, lịch sử đăng nhập, các process user đó đang chạy

vmstat3	Kiểm soát hành vi hệ thống, phần cứng và thông tin hệ thống trong Linux

ps	Hiển thị các chương trình hiện đang chạy

uptime	Hiển thị thời gian đã vận hành của hệ thống trong bao lâu

rpm	Kiểm tra, gỡ bỏ hoặc cài đặt 1 gói .rpm

yum	Cài đặt các ứng dụng đóng gói (giống rpm)

wget	Tải các ứng dụng từ một website về

sh	Chạy một ứng dụng có đuôi .sh

Startx	Khởi động chế độ xwindows từ cửa sổ terminal

yum update -y	Update Linux (CentOS)

stop/start/restart	Dừng/ khởi động/khởi động lại một service hoặc ứng dụng, ví dụ: service mysql stop hoặc /etc/init.d/mysqld start

kill	Dừng proccess (thường dùng khi process bị treo). Chỉ có super-user mới có thể dừng tất cả các process còn user khác chỉ có thể dừng proccess mà user đó tạo ra

kill PID hoặc %job	Ngừng một process bằng số PID (Process Identification Number) hoặc số công việc

pstree	Hiển thị tất cả các process dưới dạng cây

service –status-all	Kiểm tra tất cả các service và tình trạng của nó

whereis mysql	Hiển thị nơi các file dịch vụ được cài đặt

service –status-all | grep abc	Xem tình trạng của process abc

kill -9 PID	Bắt buộc đóng một process ID

kill -1 PID	Bắt buộc đóng một process ID và load lại cấu hình mặc định của process đó
  
  
  

