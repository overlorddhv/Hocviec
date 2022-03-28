# Cài đặt Mariadb

Bước 1: update hệ thống 

![image](https://user-images.githubusercontent.com/62273292/160348938-8663e20e-d80e-4885-82df-2bc14337a428.png)

Bước 2: Cài đặt MariaDB

`apt install -y software-properties-common mariadb-server mariadb-client`

![image](https://user-images.githubusercontent.com/62273292/160349325-f6ea7a7c-9cbd-47f9-844e-1b044d456a78.png)


Bước 3: Khởi động dịch vụ MariaDB

![image](https://user-images.githubusercontent.com/62273292/160349505-243b27e2-e6e0-4764-8781-8fab3c3254d0.png)

Bước 4: Kiểm tra trạng thái của MariaDB

`systemctl status mariadb`

![image](https://user-images.githubusercontent.com/62273292/160349846-04c87961-a329-41d2-ba59-75740cd04fcf.png)


## Cấu hình và thao tác cơ bản với MariaDB

Cấu hình ban đầu cho MariaDB

`mysql_secure_installation`

![image](https://user-images.githubusercontent.com/62273292/160350778-93f60dcf-7c39-4fe0-a9bb-f4b24194ad35.png)

Đăng nhập MariaDB

`mysql -u root -p`

![image](https://user-images.githubusercontent.com/62273292/160351171-6bea6c4b-75ef-4370-9d06-eeef7d04d8dd.png)


##  Thao tác cơ bản với MariaDB

Để xem các bảng cơ sở dữ liệu có sẵn trong MariaDB như sau :

`show databases;`


![image](https://user-images.githubusercontent.com/62273292/160351829-de3c0627-482f-4a98-8933-c801f87bc999.png)


Để tạo 1 cơ sở dữ liệu mới , thực hiện câu lệnh sau :

`create database Thiendatabase1;`

![image](https://user-images.githubusercontent.com/62273292/160352206-4651a041-528e-4e10-ad53-5239c59ee309.png)






























