 # 1. Cài đặt Apache trên CentOS 7
 
 **Bước 1: Cài đặt Apache**

Apache có sẵn trong kho lưu trữ CentOS mặc định nên việc cài đặt khá đơn giản. Để cài đặt Apache hãy chạy lệnh sau:

`yum install httpd -y`

**Bước 2: Khởi động Apache**

Khi quá trình cài đặt hoàn tất, hãy bật và khởi động dịch vụ Apache bằng các lệnh sau:

`systemctl enable httpd`

`systemctl start httpd`

![image](https://user-images.githubusercontent.com/55913475/158977583-942482b4-7c9b-4aba-9c4b-8b47b3da1af8.png)

Để kiểm tra trạng thái của Apache hãy sử dụng lệnh sau:

`systemctl status httpd`

![image](https://user-images.githubusercontent.com/55913475/158977753-4a78f300-b37b-4e1c-a9ee-82517fb08444.png)

**Bước 3: Cấu hình Firewalld (Nếu có)**

Nếu các bạn sử dụng Firewalld để có thể truy cập được website các bạn sẽ cần mở port bằng các lệnh sau đây

`firewall-cmd --permanent --zone=public --add-service=http`

`firewall-cmd --permanent --zone=public --add-service=https`

`firewall-cmd --reload`

![image](https://user-images.githubusercontent.com/55913475/158978027-e2e504e4-e9a2-4d7c-80a2-469aa1ccbd79.png)

# 2. Quản lý Apache Service với systemctl

- Để dừng Apache, dùng lệnh:

`systemctl stop httpd`

- Để khởi động Apache dùng lệnh:

`systemctl start httpd`

- Lệnh khởi động lại Apache:

`systemctl restart httpd`

- Tải lại dịch vụ Apache mỗi khi bạn thay đổi cấu hình:

`systemctl reload httpd`

- Nếu không muốn Apache tự động chạy mỗi khi khởi động lại VPS sử dụng lệnh sau:

`systemctl disable httpd`

- Nếu muốn Apache tự động chạy mỗi khi khởi động lại VPS sử dụng lệnh sau:

`systemctl enable httpd`

# 3. Các file cấu hình
- Tất cả các file cấu hình của Apache đều nằm trong thư mục /etc/httpd.

- File cấu hình chính của Apache là /etc/httpd/conf/httpd.conf.

- Tất cả các tệp cấu hình đều phải kết thúc bằng .conf và nằm trong thư mục /etc/httpd/conf.d.

- Các tệp cấu hình chịu trách nhiệm tải các modules Apache được đặt trong thư mục /etc/httpd/conf.modules.d.

- Để quản lý tốt hơn, nên tạo một tệp cấu hình riêng (vhost) cho mỗi tên miền.

- Các tệp vhost Apache phải kết thúc bằng .conf và được lưu trữ trong thư mục /etc/httpd/conf.d. Ví dụ: nếu tên miền của bạn là mydomain.com thì tệp cấu hình sẽ được đặt tên /etc/httpd/conf.d/mydomain.com.conf

- Các file log của Apache (access_log và error_log) nằm trong thư mục /var/log/httpd/. Bạn nên có file log riêng cho mỗi vhost.

# 4. Tạo Virtualhost (Vhost)

**Bật userdir**

Mặc định thư mục chứa code sẽ nằm trong /var/www/html, với chức năng userdir cho phép di chuyển thư mục chứa code sang vị trí khác đồng thời dễ dàng quản lý vhost theo từng user.

Để bật Userdir các bạn mở file **/etc/httpd/conf.d/userdir.conf**.

`nano /etc/httpd/conf.d/userdir.conf`

Tại đây các bạn cần sửa các rules sau

`UserDir disabled`

`#UserDir public_html`

Sửa lại thành như sau

`#UserDir disabled`

`UserDir public_html`

![image](https://user-images.githubusercontent.com/55913475/158985372-8efa153c-2bb1-4d82-af8e-f880e855cc01.png)

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

![image](https://user-images.githubusercontent.com/55913475/158985537-f6ac425b-bbe8-4131-bdc8-197f56093040.png)

**Chặn truy cập IP VPS tự động redirect về website trên VPS**

Theo mặc định thì khi truy cập IP của VPS hoặc khi trỏ một tên miền về VPS mà tên miền này không được cấu hình vhost thì bạn sẽ được redirect tới một website bất kỳ trên VPS, điều này là không nên và để hạn chế điều này các bạn mở file **/etc/httpd/conf/httpd.conf**

`nano /etc/httpd/conf/httpd.conf`

Thêm phía trên dòng **IncludeOptional conf.d/*.conf** rules sau:

```
<VirtualHost *:80>
	DocumentRoot /var/www/html
	ServerName www.example.com
	<Directory "/var/www/html">
		AllowOverride All
                Options None
                Require method GET POST OPTIONS
	</Directory>
</VirtualHost>
```

![image](https://user-images.githubusercontent.com/55913475/158986474-abe95ebc-1321-4929-9121-362206b0b34c.png)

**Tạo virtual host (vhost) cho website**

Virtual Host là file cấu hình trong Apache để cho phép nhiều domain cùng chạy trên một máy chủ. Có một khái niệm khác được đề cập tới trong Nginx cũng có chức năng tương tự như Virtual Host được gọi là Server Block.

Tất cả các file vhost sẽ nằm trong thư mục /etc/httpd/conf.d/. Để tiện quản lý mỗi website nên có một vhost riêng, ví dụ: 123.com.conf

Trong ví dụ này sẽ tạo website 123.com với vhost tương ứng là /etc/httpd/conf.d/123.com.conf

nano /etc/httpd/conf.d/123.com.conf

Dán nội dung sau vào

```
<VirtualHost *:80>
	ServerName www.123.com
	ServerAlias 123.com
	DocumentRoot /home/123.com/public_html
	ErrorLog /home/123.com/logs/error_log
	CustomLog /home/123.com/logs/access_log combined
</VirtualHost>
```
Tiếp theo các bạn cần tạo thư mục chứa mã nguồn website và thư mục chứa file log bằng các lệnh sau

```
mkdir -p /home/123.com/public_html
mkdir -p /home/123.com/logs
chown -R apache:apache /home/123.com
```

Reload lại Apache để cập nhật cấu hình

`systemctl reload httpd`

Sau khi cấu hình hoàn tất các bạn trỏ tên miền về vps sau đó tạo file **/home/123.com/public_html/index.html**

`nano /home/123.com/public_html/index.html`

Dán nội dung sau vào

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>123.com</title>
</head>
<body>
	<p><center>123.com - Uy tín</center></p>
</body>
</html>
```

Truy cập tên miền của bạn bằng trình duyệt để kiểm tra
