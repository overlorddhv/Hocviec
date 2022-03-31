Bước 1: Cài đặt Apache và cấu hình cơ bản

Tắt Selinux

`sed -i 's/SELINUX=enforcing/SELINUX=disabled/g' /etc/selinux/config && setenforce 0`

 Cài đặt Apache
 
 ```
 yum -y install epel-release
yum -y update
yum -y install httpd
```

![image](https://user-images.githubusercontent.com/62273292/160996220-e14a03c0-3cf6-4ae3-8d5f-39180fb05feb.png)


Nếu bạn sử dụng Firewalld thì bạn sẽ cần mở port để có thể truy cập website

```
firewall-cmd --add-service=http --permanent
firewall-cmd --add-service=https --permanent
firewall-cmd --reload
```
![image](https://user-images.githubusercontent.com/62273292/160996455-8ab7ccaa-96be-4555-ba0b-c077e901a680.png)


Cấu hình Apache cơ bản

Dưới đây là các thông số cần sửa

```
#ServerName www.example.com:80
DirectoryIndex index.html
```

Các bạn sửa lại thành như sau

```
ServerName www.vanthien.com:80
DirectoryIndex index.html index.htm index.php
```


 Thêm 2 rules sau phía dưới dòng Listen 80
 
 ```
 ServerTokens Prod
KeepAlive On
ServerSignature Off
```
![image](https://user-images.githubusercontent.com/62273292/160997226-87edca23-f41c-4cab-9f36-73805a4e1e91.png)


Bật Userdir

Để bật Userdir các bạn mở file /etc/httpd/conf.d/userdir.conf. Tại đây các bạn cần sửa các rules sau

```
UserDir disabled
#UserDir public_html
```

Sửa lại thành như sau

```
#UserDir disabled
UserDir public_html
```

![image](https://user-images.githubusercontent.com/62273292/160997666-293d3c36-1e13-414a-96ab-e1ace976f641.png)


Tiếp theo các bạn tìm đoạn rule sau

```
<Directory "/home/*/public_html">
    AllowOverride FileInfo AuthConfig Limit Indexes
    Options MultiViews Indexes SymLinksIfOwnerMatch IncludesNoExec
    Require method GET POST OPTIONS
</Directory>
```

Sửa nó lại thành như sau

```
<Directory "/home/*/public_html">
    AllowOverride All
    Options None
    Require method GET POST OPTIONS
</Directory>
```


![image](https://user-images.githubusercontent.com/62273292/160997863-ee36d356-4f89-47e3-b058-d42ec1c32e44.png)

Chặn truy cập IP VPS tự động redirect về website trên VPS

Theo mặc định thì khi truy cập IP của VPS hoặc khi trỏ một tên miền về VPS mà tên miền này không được cấu hình vhost thì bạn sẽ được redirect tới một website bất kỳ trên VPS, điều này là không nên và để hạn chế điều này các bạn mở file /etc/httpd/conf/httpd.conf và thêm phía trên dòng IncludeOptional conf.d/*.conf rules sau:

```
<VirtualHost *:80>
	DocumentRoot /var/www/html
	ServerName www.vanthien.com
	<Directory "/var/www/html">
		AllowOverride All
                Options None
                Require method GET POST OPTIONS
	</Directory>
</VirtualHost>
```

![image](https://user-images.githubusercontent.com/62273292/160999741-debfa384-6817-4213-91c6-b700a5170ff9.png)


Tạo virtual host (vhost) cho website

![image](https://user-images.githubusercontent.com/62273292/161000959-cfe109d2-e6a7-4b42-9ce3-06c0fc8d03dc.png)


Tiếp theo các bạn cần tạo thư mục chứa mã nguồn website và thư mục chứa file log bằng các lệnh sau

```
mkdir -p /home/hostvn.net/public_html
mkdir -p /home/hostvn.net/logs
chown -R apache:apache /home/hostvn.net
```

![image](https://user-images.githubusercontent.com/62273292/161001339-d156e5ea-87d2-4d53-ad8e-00175945d5d8.png)


Khởi động Apache

```
systemctl start httpd
systemctl enable httpd
```

Kiểm tra

Sau khi cấu hình hoàn tất các bạn trỏ tên miền về vps sau đó tạo file /home/vanthien.com/public_html/index.html với nội dung sau và gõ tên miền của bạn vào thanh địa chỉ của trình duyệt để kiểm tra

```
<!DOCTYPE html>
<html lang="en">
<head>
        <meta charset="UTF-8">
        <title>vanthien.com dzai</title>
</head>
<body>
        <p><center>Huynh đệ chào anh thiên vippro</center></p>
</body>
</html>
```

![image](https://user-images.githubusercontent.com/62273292/161002043-671c4a81-afce-4a27-8e40-3a55e6e80492.png)














































