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



![image](https://user-images.githubusercontent.com/62273292/161064516-fc1d56e7-ee7f-4cfc-8ad9-dc5da202c80d.png)


## Cài đặt MariaDB

![image](https://user-images.githubusercontent.com/62273292/161064749-972b663a-810b-4873-89f7-76e69aa92685.png)

`yum install MariaDB-server MariaDB-client -y`

 Đặt mật khẩu root

```
systemctl enable mariadb
systemctl start mariadb
mysql_secure_installation
```
## Cài đặt PHP-FPM và các Module cần thiết

 Cài đặt PHP-FPM
 
 Để cài đặt PHP-FPM các bạn chạy các lệnh sau

```
yum -y install yum-utils
rpm -Uvh http://rpms.remirepo.net/enterprise/remi-release-7.rpm
yum -y update

yum-config-manager --enable remi-php73
yum -y install php php-fpm php-ldap php-zip php-embedded php-cli php-mysql php-common php-gd php-xml php-mbstring php-mcrypt php-pdo php-soap php-json php-simplexml php-process php-curl php-bcmath php-snmp php-pspell php-gmp php-intl php-imap perl-LWP-Protocol-https php-pear-Net-SMTP php-enchant php-pear php-devel php-zlib php-xmlrpc php-tidy php-mysqlnd php-opcache php-cli php-pecl-zip unzip gcc

```

![image](https://user-images.githubusercontent.com/62273292/161066137-7c2fadcb-bc57-4f31-9763-6fd9914cc09a.png)

![image](https://user-images.githubusercontent.com/62273292/161066317-29642299-9f08-4f96-a35b-45e96e22187b.png)


![image](https://user-images.githubusercontent.com/62273292/161068909-b8073381-2bc8-47f6-9ee8-4cafc501295e.png)

Cấu hình php cơ bản

Tất cả cấu hình php cần thiết sẽ nằm trong file /etc/php.ini. Một số thông số cơ bản bạn có thể sửa như sau

```
;date.timezone =
expose_php = On
short_open_tag = Off
;max_input_vars = 1000
disable_functions =
```
Các bạn sửa lại thành như sau:

```
date.timezone = Asia/Ho_Chi_Minh
expose_php = Off
short_open_tag = On
max_input_vars = 3000
disable_functions = exec,system,passthru,shell_exec,proc_close,proc_open,dl,popen,show_source,posix_kill,posix_mkfifo,posix_getpwuid,posix_setpgid,posix_setsid,posix_setuid,posix_setgid,posix_seteuid,posix_setegid,posix_uname
```
Cấu hình chạy PHP-FPM

Các bạn mở file /etc/httpd/conf.d/php.conf tìm dòng SetHandler application/x-httpd-php sửa thành SetHandler “proxy:fcgi://127.0.0.1:9000”



Tiếp theo khởi động lại apache để load lại config

Khởi động PHP-FPM

```
systemctl start php-fpm
systemctl enable php-fpm
```

![image](https://user-images.githubusercontent.com/62273292/161079539-8bcbe5a7-85e4-4600-bb6c-9cd583284e70.png)

Kiểm tra

Để kiểm tra xem PHP-FPM đã hoạt  động hay chưa các bạn tạo file /home/vanthien.com/public_html/info.php với nội dung sau

```
<?php
phpinfo();
?>
```

![image](https://user-images.githubusercontent.com/62273292/161080144-915a0ca6-a958-49b1-bd38-58f94577677b.png)

## Cài đặt PhpMyAdmin

Để cài đặt PhpMyAdmin các bạn chạy lần lượt các lệnh sau

```
cd /usr/share
wget https://files.phpmyadmin.net/phpMyAdmin/5.0.2/phpMyAdmin-5.0.2-all-languages.zip
unzip phpMyAdmin-5.0.2-all-languages.zip
mv phpMyAdmin-5.0.2-all-languages phpMyAdmin
rm -rf phpMyAdmin-5.0.2-all-languages.zip
rm -rf /usr/share/phpMyAdmin/setup
```


![image](https://user-images.githubusercontent.com/62273292/161086765-5d8d2ac2-a9ce-48f0-8289-046d8a7b94fd.png)

Cấu hình phpMyAdmin

`mv /usr/share/phpMyAdmin/config.sample.inc.php /usr/share/phpMyAdmin/config.inc.php`

Tiếp theo mở file /usr/share/phpMyAdmin/config.inc.php

`nano /usr/share/phpMyAdmin/config.inc.php`

Tìm 

`$cfg['blowfish_secret'] = '';`

thêm một đoạn ký tự bất kỳ vào giữa cặp nháy đơn. Ví dụ:

`$cfg['blowfish_secret'] = 'Vanthien97';`

![image](https://user-images.githubusercontent.com/62273292/161105718-c6320f8d-4de8-4344-b0be-fd4e0e40b5da.png)


Tiếp theo thêm vào cuối file doạn code sau

$cfg['TempDir'] = '/usr/share/phpMyAdmin/tmp/';

```
mkdir -p /usr/share/phpMyAdmin/tmp
chown -R apache:apache /usr/share/phpMyAdmin/tmp
```
## Cấu hình vhost cho PhpMyAdmin

 Tạo file `/etc/httpd/conf.d/phpmyadmin.conf` với nội dung sau

```
Alias /pma /usr/share/phpMyAdmin
Alias /phpmyadmin /usr/share/phpMyAdmin
 
<Directory /usr/share/phpMyAdmin/>
    AddDefaultCharset UTF-8
    <IfModule mod_authz_core.c>
    # Apache 2.4
    <RequireAny>
        <RequireAll>
            Require all granted
        </RequireAll>
    </RequireAny>
    </IfModule>
    <IfModule !mod_authz_core.c>
        # Apache 2.2
        Order Deny,Allow
        Deny from All
        Allow from All
        Allow from ::1
    </IfModule>
</Directory>
<Directory /usr/share/phpMyAdmin/log/>
    Order Deny,Allow
    Deny from All
    Allow from None
</Directory>
<Directory /usr/share/phpMyAdmin/libraries/>
    Order Deny,Allow
    Deny from All
    Allow from None
</Directory>
<Directory /usr/share/phpMyAdmin/templates/>
    Order Deny,Allow
    Deny from All
    Allow from None
</Directory>
<Directory /usr/share/phpMyAdmin/tmp/>
    Order Deny,Allow
    Deny from All
    Allow from None
</Directory>
```


![image](https://user-images.githubusercontent.com/62273292/161105774-e476ba13-ddd6-49eb-9157-65fb125cfcc0.png)


![image](https://user-images.githubusercontent.com/62273292/161106499-8375fbfe-5a9b-4ac5-b3ce-d6deb94c4cfb.png)


Đăng nhập PhpMyadmin thành công

![Uploading image.png…]()
































