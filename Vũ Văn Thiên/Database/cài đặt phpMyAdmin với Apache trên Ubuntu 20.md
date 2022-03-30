# CÀI ĐẶT LAMP 

## Cài đặt apache 

`sudo apt update`

![image](https://user-images.githubusercontent.com/62273292/160549614-cc3b1a03-90e3-45a7-8ccb-991515de112a.png)

`sudo apt install apache2 -y`

![image](https://user-images.githubusercontent.com/62273292/160549858-c84d1f5d-98f2-4e25-ba22-ee5c82692a1c.png)

```
sudo a2enmod rewrite
sudo a2enmod ssl
sudo a2enmod headers
sudo systemctl restart apache2
```

![image](https://user-images.githubusercontent.com/62273292/160549981-54f05597-7b53-4644-a8ab-b5a8eeecff9c.png)


`sudo ufw app list`

![image](https://user-images.githubusercontent.com/62273292/160550330-1d61a907-824c-415d-b64a-4e1039a1dfef.png)


`sudo ufw allow 'Apache'`

![image](https://user-images.githubusercontent.com/62273292/160550636-00a27ff2-8f0a-4ebc-b20c-7c90958a68a4.png)


![image](https://user-images.githubusercontent.com/62273292/160550854-110abcaa-440c-4d8f-b6b4-e03dda42d95b.png)

`sudo systemctl status apache2`

![image](https://user-images.githubusercontent.com/62273292/160550975-b3067241-e032-44d6-bb00-3167a99cc68a.png)

Đăng nhập bằng địa chỉ IP

![image](https://user-images.githubusercontent.com/62273292/160551117-051401b2-b556-46af-8346-422c4f017546.png)


![image](https://user-images.githubusercontent.com/62273292/160552078-40e8e420-ff76-41fe-b472-ec4b51b58b49.png)


![image](https://user-images.githubusercontent.com/62273292/160552124-e614aa75-abf7-45d9-85af-358e29a0994c.png)

![image](https://user-images.githubusercontent.com/62273292/160553041-47c10574-fb11-46c2-b9cc-0790f4a5af41.png)


![image](https://user-images.githubusercontent.com/62273292/160553770-edc1cffe-2fe0-4ae8-8729-02b0a1ce5e42.png)

![image](https://user-images.githubusercontent.com/62273292/160555448-a2c58aef-d5bb-494a-a2c1-951c960aa081.png)



![image](https://user-images.githubusercontent.com/62273292/160555459-0db26348-00ac-4413-9924-ed4655c6e225.png)
![image](https://user-images.githubusercontent.com/62273292/160556227-32927173-eaed-49e1-8a1e-0ea2e7473465.png)


![image](https://user-images.githubusercontent.com/62273292/160561476-43baeb1f-b798-4366-a1fc-6ccbe92b4a3b.png)


![image](https://user-images.githubusercontent.com/62273292/160561782-5559ec29-1998-4713-ba75-8cb84be29593.png)


![image](https://user-images.githubusercontent.com/62273292/160563201-38c7edc1-df1e-44f4-9460-c3b33ffb2124.png)

![image](https://user-images.githubusercontent.com/62273292/160563996-df1bc1bd-acdc-41b6-b58c-5d038942307f.png)


Cài đặt Mariadb 
![image](https://user-images.githubusercontent.com/62273292/160564327-60c3671a-d697-41eb-afd4-eb4890c4eb4c.png)

Bảo mật Mariadb
![image](https://user-images.githubusercontent.com/62273292/160564836-89cb0714-57d3-4e52-b7dd-5a1f427ba1dd.png)

Kết nối Mariadb

![image](https://user-images.githubusercontent.com/62273292/160564789-52a8d104-2953-4b92-80e4-c0237c00d896.png)

Khởi động Mariadb

![image](https://user-images.githubusercontent.com/62273292/160565178-d204da24-9abc-4822-8f7d-b1c67a8cf31a.png)


Tạo cơ sở dữ liệu và tạo người dùng (tạo 1 bảng trước)

![image](https://user-images.githubusercontent.com/62273292/160574024-40cf36bc-85fe-4484-a37d-e24e0979b1e9.png)




Cài đặt

Thêm PHP PPA

![image](https://user-images.githubusercontent.com/62273292/160574717-2256149b-944b-4adb-a744-1c3a0c98b2a5.png)


Cài đặt php trên ubuntu

![image](https://user-images.githubusercontent.com/62273292/160578790-95c11031-e7ab-4e84-a310-d501efe86548.png)


Kiểm tra phiên bản php 

![image](https://user-images.githubusercontent.com/62273292/160578893-a0fcc227-87a5-4f34-a36b-9728d372bb76.png)

Cài đặt php modules

![image](https://user-images.githubusercontent.com/62273292/160579111-153f411c-eb0b-41c0-8850-dfdd93ad0d90.png)

![image](https://user-images.githubusercontent.com/62273292/160579359-ba67fbb9-32e2-4f70-a165-a5e3ed47a1f8.png)


Cấu hình php modules

![image](https://user-images.githubusercontent.com/62273292/160579766-f11cc0d5-9710-4ca9-8d19-6bc1b477f969.png)

tạo file info.php trong đường dần ( /var/www/vanthien.com/info.php)

![image](https://user-images.githubusercontent.com/62273292/160580019-ac404121-302e-4f91-8720-49733f96fdbd.png)



![image](https://user-images.githubusercontent.com/62273292/160587600-7e2b5cdb-d4ac-4b9a-9f97-65e69ce06ddd.png)






Đăng nhập địa chỉ/phpmyadmin

![image](https://user-images.githubusercontent.com/62273292/160588828-97ec8ab2-8987-4fd1-96ac-685d6b50505a.png)



đăng nhập vanthienn mk: Vanthien97@1234a

![image](https://user-images.githubusercontent.com/62273292/160589319-92b648b2-39a1-49bc-8d6c-51a713f7699b.png)








