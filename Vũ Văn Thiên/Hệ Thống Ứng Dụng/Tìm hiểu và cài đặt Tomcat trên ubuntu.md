
## Cài đặt Tomcat trên ubuntu

Môi trường cài đặt là một máy tính cài Ubuntu 20 với quyền root hoặc user với quyền sudo.

**Cài đặt Java**

Tomcat 9 yêu cầu  Java 8 hoặc cao hơn. Bạn có thể cài Java bằng lệnh dưới đây, hoặc bỏ qua nếu hệ thống đã có sẵn.

```sudo apt install openjdk-11-jdk```

![image](https://user-images.githubusercontent.com/62273292/159657010-735eb186-e89e-4bbf-b0d0-67633609e73f.png)


Kiểm tra phiên bản Java

```java -version```

![image](https://user-images.githubusercontent.com/62273292/159657281-9b5d3f74-37dd-4d84-b160-6678317923b3.png)

 
```
openjdk version "11.0.7" 2020-04-14 
OpenJDK Runtime Environment (build 11.0.7+10-post-Ubuntu-3ubuntu1) 
OpenJDK 64-Bit Server VM (build 11.0.7+10-post-Ubuntu-3ubuntu1, mixed mode, sharing)
```

Tạo user account cho Tomcat

Để tăng bảo mật, chúng ta nên tạo user riêng cho Tomcat.

Tạo user cho Tomcat bằng lệnh sau:

```sudo useradd -m -d /opt/tomcat -U -s /bin/false tomcat```

![image](https://user-images.githubusercontent.com/62273292/159657394-41f3f30e-09d3-4086-905f-cd1a8035d938.png)


Lệnh trên sẽ tạo ra user và group “tomcat” trên hệ thống.

Download Tomcat
Các bạn có thể kiểm tra phiên bản mới nhất của Tomcat tại **ficial download server**Câu lệnh dưới đây sẽ tải về Tomcat 9.0.35.

![image](https://user-images.githubusercontent.com/62273292/159657748-a076a5fa-1836-47be-a264-5d60f2d1caaf.png)


wget https://www-us.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz


Giải nén và copy vào thư mục của tomcat.

```tar xzf apache-tomcat-9.0.35.tar.gz ```



```sudo mv apache-tomcat-9.0.35/* /opt/tomcat/```

Cấp quyền thư mục cho user tomcat

```sudo chown -R tomcat:tomcat /opt/tomcat/```

![image](https://user-images.githubusercontent.com/62273292/159657915-de32f687-043a-4220-a137-cef958c0ad4a.png)


Tạo Tomcat Access Credentials

Chỉnh sửa file conf/tomcat-users.xml để bảo mật truy cập vào trang quản lý admin.

```sudo nano /opt/tomcat/conf/tomcat-users.xml```

Thêm các dòng sau vào giữa thẻ <tomcat-users> </ tomcat-users>. Các bạn nên thay đổi mật khẩu trong cấu hình bên dưới để đảm bảo tính bảo mật cao.

![image](https://user-images.githubusercontent.com/62273292/159658876-88d65b91-f8f2-4617-9eba-a6e1f30fb152.png)


```
<!-- user manager can access only manager section -->
<role rolename="manager-gui" />
<user username="manager" password="_SECRET_PASSWORD_" roles="manager-gui" />
```

```
<!-- user admin can access manager and admin section both -->
<role rolename="admin-gui" />
<user username="admin" password="_SECRET_PASSWORD_" roles="manager-gui,admin-gui" />
```

Tạo file script  Tomcat Service

Reload the systemd daemon service bằng lệnh

```sudo systemctl daemon-reload```

Sau đó cho phép Tomcat khởi động cùng hệ thống và bật Tomcat bằng lệnh sau:
```
sudo systemctl enable tomcat 
sudo systemctl start tomcat
```
Kiểm tra xem tomcat đã được khởi động chưa

```./startup.sh```

![image](https://user-images.githubusercontent.com/62273292/159659636-2ed908ea-b658-47e5-afa1-70ef0c0b5f5b.png)

![image](https://user-images.githubusercontent.com/62273292/159659767-f96e3b50-e719-4e0e-ac36-fae48e237dbe.png)

![image](https://user-images.githubusercontent.com/62273292/159659838-9f93f6f7-a741-421f-b831-a0614336018e.png)

![image](https://user-images.githubusercontent.com/62273292/159659955-6eba4429-dafc-446e-876b-87420eac54df.png)






