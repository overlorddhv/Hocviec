# Các lệnh quản lý cơ sở dũ liệu MariaDB 

1. Đăng nhập vào MariaDB

Bạn nhập vào cú pháp `mysql -u root -p` khi đó MySQL sẽ yêu cầu bạn nhập vào Password của MySQL. Đây là password cao nhất quản lý toàn bộ cơ sở dữ liệu.

![image](https://user-images.githubusercontent.com/62273292/160741411-9e5ae112-646b-467f-aa58-5e9538b28f30.png)


2. Tạo Database

Cú pháp: `Create database thiendzai;`

![image](https://user-images.githubusercontent.com/62273292/160741644-5bef1061-408b-493e-a8cc-485b3bc30993.png)


3. Tạo User Password

`CREATE USER 'thien2k3'@'localhost' IDENTIFIED BY 'thiendzai123@hihi';`

![image](https://user-images.githubusercontent.com/62273292/160743508-e271bf76-b6f6-4527-ab12-a771f8f5e21f.png)


4. Gán quyền User Database

` GRANT ALL ON thiendzai.* TO thien2k3@localhost;`

![image](https://user-images.githubusercontent.com/62273292/160743635-6ac64bd8-e72d-4af5-baa5-1c675627b6a7.png)

5. Show Database

`show databases;`

![image](https://user-images.githubusercontent.com/62273292/160743796-554e724e-afdc-4216-bf97-e52e6c726e89.png)


6. Truy cập vào Database

`use thiendzai`

![image](https://user-images.githubusercontent.com/62273292/160743910-80eb908f-1346-415d-bf8d-8eba501ea295.png)

7. Tạo table cho database

  ![image](https://user-images.githubusercontent.com/62273292/160744488-90c8d080-9602-48f6-9f62-a500faa248ab.png)

8. Show Table Database

![image](https://user-images.githubusercontent.com/62273292/160744569-bca10abf-591e-4542-b2f1-5b0d4d081e6a.png)

9. Kiểm tra các trường trong bảng 

`desc user`;

![image](https://user-images.githubusercontent.com/62273292/160744729-be151ef1-575e-4348-9888-e74ba99d731b.png)

10. Chèn dữ liệu vào trong bảng

![image](https://user-images.githubusercontent.com/62273292/160746980-daee98aa-c55b-4654-a02d-69a8bc3ea1a9.png)

![image](https://user-images.githubusercontent.com/62273292/160747586-cb8aa925-93ae-4013-b080-8ddfef1939aa.png)


## Phân quyền cho user database

- ALL PRIVILEGES – cấp cho user tất cả các đặc quyền.

- CREATE – user có quyền tạo CSDL và bảng.

- DROP – user xóa CSDL và bảng.

- DELETE – user được phép xóa các hàng khỏi một bảng cụ thể.

- INSERT – user được phép chèn các hàng vào bảng cụ thể.

- SELECT – user được phép đọc CSDL.

- UPDATE – user được phép cập nhật các hàng của bảng.
























