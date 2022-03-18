# Hướng dẫn cài đặt Ubuntu Server 20.04 LTS

Các bước chuẩn bị  
1. File iso của Ubuntu Server 20.04 LTS   

![image](https://user-images.githubusercontent.com/65167293/158922034-60e31310-aa41-4fc5-97bf-15902de7861a.png)

2. Máy ảo VirtualBox, VMWare hoặc có thể ghi file iso ra đĩa và cài trên máy tính thật.  

Yêu cầu phần cứng tối thiểu
Sự khác biệt lớn giữa phiên bản máy chủ của Ubuntu và phiên bản máy tính để bàn là phiên bản máy chủ không đi kèm với giao diện đồ họa và bản thân quá trình cài đặt có một chút khác biệt.

Vì mọi thứ trên máy chủ Ubuntu 20.04 đều được thực hiện bởi dòng lệnh, việc thiếu GUI và nhiều phần mềm nên các yêu cầu hệ thống tối thiểu thấp hơn nhiều.

- 1 GHz CPU
- 512 MB RAM (system memory)
- 2.5 GB hard drive

Sau khi tiến hành mount file .iso cài đặt và khởi động, đầu  tiên máy chủ sẽ tiến hành kiểm tra file cài đặt. Quá trình này sẽ diễn ra trong khoảng thời gian ngắn.  

![Huong-Dan-Cai-Dat-Ubuntu-Server-20-04-LTS-Buoc-1 (1)](https://user-images.githubusercontent.com/65167293/158922330-678e8e93-d066-4061-b98d-2286c7964b95.png)

Sau đó các bạn tiến hành chọn ngôn ngữ cài đặt.

Ở đây mình mặc định chọn là English.

![Huong-Dan-Cai-Dat-Ubuntu-Server-20-04-LTS-Buoc-2](https://user-images.githubusercontent.com/65167293/158922374-1a34a911-cdbd-48b5-878a-60c91a0f1ad6.png)

Do file iso của mình down khá lâu, nên nó hỏi bạn có cần cập nhật lên phiên bản mới nhất là 20.04.3 không? Mình chọn [Continue without updating], sau này sẽ update sau.

Trường hợp file iso các bạn mới down về thì sẽ không có bước này trong quá trình cài đặt.  

![Huong-Dan-Cai-Dat-Ubuntu-Server-20-04-LTS-Buoc-3](https://user-images.githubusercontent.com/65167293/158922594-603ae5cb-5a87-45f4-8c63-9796e2d94788.png)

Chọn kiểu bàn phím. Tốt nhất là nên để mặc định

![Huong-Dan-Cai-Dat-Ubuntu-Server-20-04-LTS-Buoc-4](https://user-images.githubusercontent.com/65167293/158922650-1bed55fc-7adc-43e7-baaa-aacc3b4c8599.png)

Cấu hình network => Để mặc định DHCP nếu chúng ta chưa có kinh nghiệm thiết lập network  

![Huong-Dan-Cai-Dat-Ubuntu-Server-20-04-LTS-Buoc-5](https://user-images.githubusercontent.com/65167293/158922718-84409cda-be18-44c7-ad7a-b370ef4a3779.png)

Nếu cần setting proxy server để kết nối với Internet thì chúng ta cấu hình ở bước này. Còn nếu không thì bỏ qua => Bấm [ Done ]

![Huong-Dan-Cai-Dat-Ubuntu-Server-20-04-LTS-Buoc-6](https://user-images.githubusercontent.com/65167293/158922775-3f38421d-fd6a-4b8b-ae58-5351f9b5f7eb.png)

Cấu hình mirror cho việc cập nhật và cài đặt phần mềm.

![Huong-Dan-Cai-Dat-Ubuntu-Server-20-04-LTS-Buoc-7](https://user-images.githubusercontent.com/65167293/158922812-8c33899d-44f4-4f27-803b-0eec05083732.png)

Cấu hình ổ đĩa cài đặt và định dạng phần vùng. Để mặc định và bấm [ Done ] để tiếp tục

![Huong-Dan-Cai-Dat-Ubuntu-Server-20-04-LTS-Buoc-8](https://user-images.githubusercontent.com/65167293/158922835-3e7ba732-61ba-4d39-8901-72129f89855b.png)

Cấu hình file system

![Huong-Dan-Cai-Dat-Ubuntu-Server-20-04-LTS-Buoc-9](https://user-images.githubusercontent.com/65167293/158922923-2ea79c15-0cb0-4729-bdda-dc1a8b269095.png)

Nó sẽ hỏi bạn là việc cài đặt sẽ làm mất dữ liệu, bạn có muốn tiếp tục không?

Chọn [ Continue ] để tiếp tục

![Huong-Dan-Cai-Dat-Ubuntu-Server-20-04-LTS-Buoc-10](https://user-images.githubusercontent.com/65167293/158922972-1f878ce3-8594-4e4c-94d1-8b4a749b75d5.png)

Cấu hình user để đăng nhập vào máy chủ

- Your name: Tên của bạn  
- Your server’s name: Tên Server  
- Pick a username: Tên đăng nhập  
- Choose a password: Mật khẩu  
- Confirm your password: Nhập lại mật khẩu của bạn  

![Huong-Dan-Cai-Dat-Ubuntu-Server-20-04-LTS-Buoc-11](https://user-images.githubusercontent.com/65167293/158923053-43c5cc02-0616-4ed9-ac40-3365e82a1440.png)

Thiết lập kết nối SSH (OpenSSH)

Bạn chọn “Install OpenSSH Server” bấm vào phím [ Space ] để đánh dấu [X] => Chấp nhận cài đặt


![Huong-Dan-Cai-Dat-Ubuntu-Server-20-04-LTS-Buoc-12](https://user-images.githubusercontent.com/65167293/158923612-22aabf42-6dce-4399-917b-e845de51698d.png)

Ở bước này sẽ liệt kê danh sách các phần mềm, tính năng, gói để cài đặt cho máy chủ.

Như mình chọn aws-cli, các bạn có thể chọn cài đặt phần mềm như PostgreSQL 10 chẳng hạn.

![Huong-Dan-Cai-Dat-Ubuntu-Server-20-04-LTS-Buoc-13](https://user-images.githubusercontent.com/65167293/158923716-1d20a73e-884a-4fbd-94ab-a9e06055303b.png)

Sau khi bấm [ Done ] quá trình cài đặt sẽ diễn ra.

![Huong-Dan-Cai-Dat-Ubuntu-Server-20-04-LTS-Buoc-14](https://user-images.githubusercontent.com/65167293/158923757-79bc113d-60eb-4339-9982-915603e5ca77.png)

Sau khi quá trình cài đặt kết thúc chọn [ Reboot ] để hoàn thành.

![Huong-Dan-Cai-Dat-Ubuntu-Server-20-04-LTS-Buoc-15](https://user-images.githubusercontent.com/65167293/158923828-2806e4b8-07eb-48f4-a72a-fae35c205b62.png)

Sau khi khởi động lại, chúng ta có thể đăng nhập với tài khoản mà đã được thiết lập ở bên trên.

![image](https://user-images.githubusercontent.com/65167293/158923939-33ddb9a5-7ba7-45af-b572-4cd86d6ddf40.png)

Như vậy chúng ta đã thành công việc cài đặt Ubuntu Server 20.04 LTS rồi đúng không? Quá trình cài đặt thực sự khá dễ dàng.
