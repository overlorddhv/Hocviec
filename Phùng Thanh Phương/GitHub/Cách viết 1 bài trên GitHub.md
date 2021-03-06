# Các cách viết 1 bài đẩy lên Github
## Cách 1. Viết trực tiếp trên Server của GitHub
**Bước 1.** Tạo file mới.

Vào thư mục bạn muốn tạo bài viết mới, chọn Add file -> Create new file
![image](https://user-images.githubusercontent.com/48250210/157367105-d2fcdaa3-d64c-471f-91d7-8a99a12d4c46.png)


**Bước 2.** Làm theo trình tự
1. Tạo tên file
2. Nhập nội dung
3. Chọn Commit new file để đăng bài viết lên GitHub
![image](https://user-images.githubusercontent.com/48250210/157366961-5025efe2-77cd-47e4-9fc2-e0b99dff2558.png)

## Cách 2. Tạo Repository và đưa về Local Repository
**Bước 1.** Tạo Repository\
![image](https://user-images.githubusercontent.com/48250210/157367601-3f286595-af25-4124-9a7c-34206407546f.png)

**Bước 2.** Nhập tên và ấn chọn Create Repository\
![image](https://user-images.githubusercontent.com/48250210/157367915-f7c37c79-f7c4-423e-b064-8e1fbdaf9bc1.png)

**Bước 3.** Để đưa Clone Respository từ Server về Local Respository (Github desktop).Trước tiên ta cần tạo 1 thư mục trên máy tính để lưu trữ Respository được đưa từ Server về. Ở đây mình tạo thư mục PhungThanhPhuong ngoài Desktop\
![image](https://user-images.githubusercontent.com/48250210/157368124-009fd525-4f43-4fde-9ece-c300a305f731.png)

**Bước 4.** Tại Github desktop vào mục File -> Clone Repository và đưa Repository từ Server về thư mục PhungThanhPhuong.
![image](https://user-images.githubusercontent.com/48250210/157368437-7f4e12c7-e942-4680-9961-af82e6ad0172.png)

## Thao tác qua lại giữa Git Server và Local Repository
Đưa dữ liệu vào local Respository đã tạo

Ta có thể dùng Visual Studio Code đăng nhập với tài khoản Git đã tạo và viết project để nạp dữ liệu cho Local Respository trong GitHub Desktop
![image](https://user-images.githubusercontent.com/48250210/157370988-36d4fcfc-ca70-42cb-b34b-5d1c8127c477.png)

Sau khi chọn File -> Save ở bên VS Code, GitHub Desktop sẽ nhận được thay đổi. Khi đó ta có thể click vào Commit to main để thực thi thay đổi\
![image](https://user-images.githubusercontent.com/48250210/157371402-fa24cad1-557f-439c-b54f-2f0776ea92f0.png)

Muốn đưa dữ liệu từ Local Repository lên Git Server, ta vào GitHub Desktop, chọn Repository -> Push (Ctrl + P)  ta sẽ nhận thấy được thay đổi trên Git Server
![image](https://user-images.githubusercontent.com/48250210/157372582-4bbf1cb6-f05a-474e-9e85-6c404a5022bb.png)
