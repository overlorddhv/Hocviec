# **Hướng dẫn sử dụng MobaXterm để SSH vào server linux**
Đối với các hệ điều hành của họ Linux như CentOS, Ubuntu, Fedora, Debian … thì việc điều khiển thông thường thực hiện qua thao tác dòng lệnh CLI. Để thực hiện việc này, người dùng sẽ sử dụng các phần mềm như Putty, MobaXterm, XShell để thực hiện SSH tới port mặc định 22 của máy chủ. Trong hướng dẫn này, mình sẽ hướng dẫn với các bạn sử dụng MobaXtem.

**1. Các tình năng hay của MobaXtem**

MobaXterm có những tính năng hay ho hơn so với việc sử dụng Putty, nó giúp người dùng thao tác tốt hơn khi điều khiển các máy chủ linux, bao gồm:

- Hỗ trợ mở nhiều cửa sổ để làm việc.
- Hỗ trợ tích hợp việc FTP hoặc SFTP để truyền file từ máy người dùng lên máy chủ.
- Hỗ trợ các thao tác zoom màn hình CLI hoặc thay đổi màu sắc bắt mắt hơn.
- Hỗ trợ các phương thức kết nối như FTP, Telnet, RDP (remote desktop với các máy là windows)
- Hỗ trợ các công cụ dùng để scan port, scan network.
- Lưu phiên đăng nhập sau lần đầu truy cập vào SSH hoặc các giao thức khác.

**2. Cách sử dụng MobaXterm**

**2.1. Tải MobaXterm**

MobaXtem cung cấp 2 phiên bản, phiên bản free – Home Edition và phiên bản mất phí – Professional Edition. Đối với người dùng thông thường, chỉ cần tải bản free là đủ (bản free) cho phép lưu 10 section SSH đầu tiên (có thể hiểu là 10 máy chủ).

Khi tải bản free, bạn có thể chọn dạng portable (giải nén và dùng ngay) hoặc dạng install (tải và cài đặt). Thực hiện tải bản free – Home Edition ở link dưới: https://mobaxterm.mobatek.net/download-home-edition.html

Trong hướng dẫn này sẽ chọn dạng file cài đặt đối với bản Home Edition

![image](https://user-images.githubusercontent.com/65167293/157795810-74ce247d-d5b2-4207-88f6-3ac6f132c4d4.png)

*Hình 1. 1   Tải MobaXterm Home Edition (bản Free) – tải file dạng cài đặt*

Sau khi tải về, tiếp tục thực hiện các thao tác cài đặt. Trong quá trình cài đặt thực hiện các tùy chọn mặc định là đủ để sử dụng.
###
### **2.2. Sử dụng MobaXterm để truy cập SSH**
Sau khi cài đặt xong, tiến hành mở MobaXterm, ta sẽ có giao diện dưới.

![image](https://user-images.githubusercontent.com/65167293/157795881-cb29bfdb-84ef-4f06-8e59-6c5b41180a5a.png)
*Hình 2. 1   Giao diện của MobaXterm*

Thưc hiện thao tác để mở cửa sổ kết nối SSH tới server của bạn. Ta chọn tab Section=> New section. Ngoài ra, có thể thực hiện tổ hợp phím Ctl + Shif + N , ta cũng có kết quả tương tự.

![image](https://user-images.githubusercontent.com/65167293/157795909-6c48e6bd-285a-4764-94a8-331bc09fca22.png)

Cửa sổ mới hiện ra sau thao tác trên sẽ có dạng như bên dưới. Chọn tab SSH

![image](https://user-images.githubusercontent.com/65167293/157795939-f31881ed-c405-4e85-a58b-52b30734e3c2.png)

*Hình 2. 2    Cửa sổ hiển thị yêu cầu người dùng nhập vào để truy cập SSH.*

Tại cửa sổ trên, tiến hành nhập địa chỉ IP và port của máy chủ. Thường thì mặc định giá trị port SSH sẽ là 22 nếu như bạn không có thay đổi gì. Trong hướng dẫn này mình sẽ kết nối tới IP có địa chỉ là 103.124.92.133 với các thông tin như sau:

- Remote host: điền địa chỉ IP, trong hướng dẫn này là 103.124.92.133
- Port: Điền port SSH của máy chủ, mặc định là: 22
- Trường còn lại bỏ trống.

Sau khi nhập xong, chọn OK.

![image](https://user-images.githubusercontent.com/65167293/157795956-1bb3623f-b904-4bcf-9e4b-06840b5fc9ac.png)

Sau khi chọn OK, ta sẽ có giao diện để nhập user và mật khẩu của máy chủ. Thường sẽ sử dụng user có tên là root và mật khẩu được cung cấp trước đó.

![image](https://user-images.githubusercontent.com/65167293/157796004-579144d9-5bce-4d75-b5c0-ceb6cdba9b91.png)

*Hình 2. 3   Nhập tài khoản và mật khẩu.*

Lưu ý, khi nhập mật khẩu sẽ không hiển thị dấu \* như các ứng dụng khác, bạn có thể chép mật khẩu ra notepad và paste lại ở màn hình trên.


![image](https://user-images.githubusercontent.com/65167293/157796021-74b51aaf-0313-4d0c-91bf-9bc0971bbbe5.png)
*Hình 2. 4   Màn hình sau khi nhập đúng mật khẩu cho tài khoản root*

Ở màn hình trên, ta chọn Yes để mỗi lần đăng nhập lại ta không cần khai báo lại mật khẩu. Cũng lưu ý việc này nên cân nhắc vì mật khẩu sẽ được lưu trên máy của bạn. Trong hướng dẫn của cửa sổ trên cho phép xóa các mật khẩu được lưu này nếu bạn muốn.

Sau khi chọn YES ta sẽ có màn hình dưới.

![image](https://user-images.githubusercontent.com/65167293/157796039-5531e222-2bf2-40dd-9b2b-796556f46bfc.png)

*Hình 2. 5   Màn hình CLI sau khi đăng nhập thành công.*

Ta có thể kiểm tra phiên bản hệ điều hành bằng lệnh cat /etc/\*-release. Kết quả sẽ hiển thị dạng như bên dưới.

![image](https://user-images.githubusercontent.com/65167293/157796059-d945e01a-8bc8-4230-acf8-eba381bf32b8.png)

*Hình 2. 6    Kết quả lệnh cat /etc/\*-release*

Hoặc có thể kiểm tra bằng các lệnh khác như: ip address

Tới đây bạn đã truy cập SSH thành công và có thể bắt đầu thao tác.


### **2.3. Các thao tác khác với MobaXterm**
Ngoài sử dụng SSH, MobaXterm còn có có thế sử dụng để thực hiện truyền file thông qua sftp. Trong hướng dẫn này mình sẽ hướng dẫn bạn up file từ máy tính cá nhân lên máy chủ thông qua MobaXterm.

Chọn tab sftp theo hình dưới.

![image](https://user-images.githubusercontent.com/65167293/157796079-7f5df9f9-08e9-4f54-b740-07e4daa7ad4d.png)

*Hình 2. 7    Tab SFTP*

Chọn biểu tượng upload
![image](https://user-images.githubusercontent.com/65167293/157796094-aceabea8-ec97-4b36-9f29-510faea63bc4.png)

*Hình 2. 8   Chọn biểu tượng upload*

Chọn file cần upload từ máy tính và chọn Open

![image](https://user-images.githubusercontent.com/65167293/157796115-0949d65a-207f-41ba-b767-d5cc402ff431.png)

Sau khi chọn file, tùy thuộc vào dung lượng mà thời gian up sẽ là nhanh hay chậm. Ta có thể quan sát ở màn hình giống như bên dưới.

![image](https://user-images.githubusercontent.com/65167293/157796142-47734ab0-8f42-4326-b6a1-dea5190d3d8e.png)

*Hình 2. 9  Màn hình theo dõi tỉ lệ up dữ liệu từ máy tính cá nhân lên server.*

Sau khi thực hiện upload xong, ta có thể kiểm tra tại thư mục /root/ của máy chủ xem file đã có hay chưa bằng lệnh ls -alh tại thư mục /root/.

![image](https://user-images.githubusercontent.com/65167293/157796164-be20eee2-6f4a-4e11-97fb-2c089149bce0.png)

*Hình 2. 10   Kết quả file đã được đưa lên máy chủ.*
## **3. Kết luận**
Trong hướng dẫn này, mình đã hướng dẫn bạn sử dụng cơ bản về MobaXteam. Bạn có thể trải nghiệm thêm các tính năng khác của nó ở trên các tab, hãy tự trải nghiệm và chia sẻ cùng chúng tôi nếu bạn muốn nhé.

# **TÀI LIỆU THAM KHẢO**
[1]. <https://thachpham.com/tools/mobaxterm-giup-ban-quan-ly-vps-qua-ssh-tot-hon.html>

[2]. <https://news.cloud365.vn/ssh-mobaxterm-huong-dan-su-dung-mobaxterm-de-ssh-vao-server-linux/>

[3] <https://tinhte.vn/thread/moba-xterm-cong-cu-aio-cho-cac-lap-trinh-vien.2807754/>


