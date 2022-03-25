# Nginx cùng php và mysql trên ubuntu

Bước 1 – Cài đặt Nginx

Nginx hoặc engine x là một máy chủ proxy và proxy hiệu suất cao với mức tiêu thụ bộ nhớ thấp. Hầu hết các trang web quy mô lớn như Netflix, Pinterest, CloudFlare, GitHub đều sử dụng Nginx.

Trong bước này, chúng tôi sẽ cài đặt máy chủ web Nginx từ kho lưu trữ Ubuntu.

Chạy lệnh dưới đây.

`sudo apt install nginx -y`

Sau khi cài đặt hoàn tất, hãy khởi động dịch vụ Nginx và cho phép nó khởi chạy mỗi khi khởi động hệ thống.

`systemctl start nginx`

`systemctl enable nginx`

Quá trình cài đặt Nginx đã hoàn tất.

Cấu hình tường lửa

Bạn nên bật tường lửa trên máy chủ.

Thêm cổng dịch vụ SSH và HTTP vào cấu hình tường lửa.

Chạy lệnh UFW bên dưới.

`ufw allow ssh`

`ufw allow http`

Bây giờ hãy khởi động tường lửa UFW và cho phép nó khởi chạy mọi lúc khi khởi động hệ thống.

`ufw enable`

Máy chủ web Nginx đang hoạt động và chạy dưới tường lửa UFW.



Bước 2 – Cài đặt MySQL

MySQL là Hệ thống quản lý cơ sở dữ liệu quan hệ mã nguồn mở (RDBMS) phổ biến nhất được tạo bởi Oracle Corporation. Đây là thành phần trung tâm của LEMP Stack và chúng tôi sẽ cài đặt phiên bản MySQL mới nhất từ ​​kho lưu trữ Ubuntu.

Cài đặt MySQL bằng lệnh apt bên dưới.

`sudo apt install mysql-server mysql-client -y`

Sau khi cài đặt MySQL hoàn tất, hãy khởi động dịch vụ MySQL và cho phép nó khởi chạy mọi lúc khi khởi động hệ thống.

`systemctl start mysql`

`systemctl enable mysql`


Và chúng tôi đã cài đặt MySQL 5.7 trên máy chủ Ubuntu 18.04.

Bước 3 – Cài đặt PHP-FPM

PHP-FPM hoặc FastCGI Process Manager là một thay thế cho PHP FastCGI cũ hơn, cung cấp các tính năng bổ sung và cải thiện tốc độ. Nó phù hợp với các trang web nhỏ đến lớn dựa trên ngôn ngữ lập trình PHP.

Trong bước này, chúng tôi sẽ cài đặt PHP7.2-FPM với một số phần mở rộng bổ sung theo yêu cầu của phpmyadmin.

Cài đặt PHP-FPM bằng lệnh bên dưới.

`sudo apt install php7.2 php7.2-fpm php7.2-cli php7.2-curl php7.2-mysql php7.2-curl php7.2-gd php7.2-mbstring php-pear -y`

Bây giờ bắt đầu dịch vụ PHP-FPM và cho phép nó khởi chạy mỗi khi khởi động hệ thống sau khi hoàn tất cài đặt.

`systemctl start php7.2-fpm`

`systemctl enable php7.2-fpm`

PHP7.2-FPM đã khởi động và chạy trên Ubuntu 18.04 trong tệp sock, kiểm tra nó bằng lệnh netstat.

`netstat -pl | grep php`


Bước 4 – Định cấu hình Nginx và PHP-FPM

Trong bước này, chúng tôi sẽ cấu hình máy chủ web Nginx và PHP-FPM.

Cấu hình Nginx

Chuyển đến thư mục cấu hình ‘/ etc / nginx’ và chỉnh sửa tệp ‘nginx.conf’ bằng vim hoặc nano.

`cd /etc/nginx/`

`vim nginx.conf`

Bỏ ghi chú các dòng sau.

```
keepalive_timeout 2;
server_tokens off;
```

Lưu tập tin cấu hình và thoát khỏi trình soạn thảo.

Bây giờ chỉnh sửa tệp máy chủ ảo Nginx mặc định.

`vim sites-available/default`

Bỏ ghi chú dòng PHP hiển thị bên dưới và thay đổi dòng tệp sock.

```
       location ~ \.php$ {
 include snippets/fastcgi-php.conf;
 #
 # # With php-fpm (or other unix sockets):
 fastcgi_pass unix:/var/run/php/php7.2-fpm.sock;
 # # With php-cgi (or other tcp sockets):
 # fastcgi_pass 127.2.0.1:9000;
 }
 
 ```
Lưu và thoát.

Kiểm tra cấu hình Nginx và đảm bảo không có lỗi, sau đó khởi động lại dịch vụ.

`nginx -t`

`systemctl reload nginx`


Cấu hình PHP-FPM

Chuyển đến thư mục `‘/etc/php/7.2’` và chỉnh sửa tệp `‘php.ini’`.

`cd /etc/php/7.2/`

`vim fpm/php.ini`

Bỏ ghi chú dòng `‘cgi.fix_patinfo’` và thay đổi giá trị thành `‘0’`.

`cgi.fix_pathinfo=0`

Lưu và thoát.

Tải lại dịch vụ PHP-FPM.

`systemctl reload php7.2-fpm`

Và chúng tôi đã hoàn thành cấu hình máy chủ web Nginx và PHP-FPM.

Bước 5 – Cài đặt PhpMyAdmin

PhpMyAdmin là một ứng dụng dựa trên PHP để quản lý cơ sở dữ liệu MySQL hoặc MariaDB từ trình duyệt web.

Trong bước này, chúng tôi sẽ cài đặt và định cấu hình phpmyadmin trong ngăn xếp LEMP (Linux, Nginx, MySQL và PHP-FPM).

Cài đặt PHPMyAdmin bằng lệnh apt bên dưới.

`sudo apt install phpmyadmin -y`

Trong quá trình cài đặt, nó sẽ hỏi bạn về cấu hình máy chủ web cho phpmyadmin.



Chọn không có tùy chọn và di chuyển con trỏ đến ‘OK’.

Đối với cấu hình cơ sở dữ liệu phpmyadmin, chọn ‘Có’.



Và nhập quản trị viên phpmyadmin mới ‘MẠNH’, chẳng hạn như ‘Hakaselabs001@#’.



Lặp lại mật khẩu 

Và quá trình cài đặt phpmyadmin đã hoàn tất.

Bước 6 – Cấu hình PhpMyAdmin

Sau khi cài đặt phpmyadmin, chúng ta cần cấu hình phpmyadmin để chạy dưới máy chủ web Nginx và định cấu hình truy cập phpmyadmin của người dùng MySQL.

Định cấu hình PhpMyAdmin với Nginx

Để chạy phpmyadmin dưới máy chủ web Nginx, chúng ta cần thêm cấu hình vào tệp cấu hình máy chủ ảo.

Chuyển đến thư mục cấu hình ‘/ etc / nginx’ và chỉnh sửa tệp máy chủ ảo mặc định.

`cd /etc/nginx/`

`vim sites-available/default`

Dán cấu hình Nginx sau cho phpmyadmin bên trong khung ‘server {…}’.

```
location /phpmyadmin {
 root /usr/share/;
 index index.php;
 try_files $uri $uri/ =404;

location ~ ^/phpmyadmin/(doc|sql|setup)/ {
 deny all;
 }

location ~ /phpmyadmin/(.+\.php)$ {
 fastcgi_pass unix:/var/run/php/php7.2-fpm.sock;
 fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
 include fastcgi_params;
 include snippets/fastcgi-php.conf;
 }
}
```

Lưu và thoát.

Kiểm tra cấu hình nginx và khởi động lại dịch vụ nginx.

`nginx -t`

`systemctl reload nginx`

Và chúng tôi đã thêm cấu hình Nginx cho phpmyadmin.

Định cấu hình người dùng MySQL cho PhpMyAdmin

Trong hướng dẫn này, chúng tôi sẽ sử dụng người dùng MySQL không root cho phpmyadmin. Chúng tôi sẽ tạo một người dùng mới và cấp tất cả các đặc quyền của cơ sở dữ liệu bên trong máy chủ cho người dùng.

Đăng nhập vào vỏ MySQL.

`mysql -u root -p`

Bây giờ tạo một người dùng mới bằng cách sử dụng các truy vấn MySQL bên dưới.

```
create user hakase@'localhost' identified by 'Hakaselabs001@#';
grant all privileges on *.* to hakase@'localhost' identified by 'Hakaselabs001@#';
flush privileges;
exit;
```

Và chúng tôi đã tạo một người dùng mới để truy cập phpmyadmin.



Bước 7 – Kiểm tra

Kiểm tra tệp PHP

Chuyển đến thư mục gốc web ‘/ var / www / html’ và tạo tệp phpinfo mới.

`cd /var/www/html/`

`vim info.php`

Dán đoạn mã phpinfo bên dưới.

```
<?php
phpinfo ();
?>
```
Lưu và thoát.


Bây giờ hãy mở trình duyệt web và nhập địa chỉ IP của máy chủ như hình bên dưới. Thay thế IP bằng ip máy chủ của bạn.

`http://192.168.33.10/info.php`

Và dưới đây là tất cả thông tin về cấu hình máy chủ PHP.



Kiểm tra đăng nhập PhpMyAdmin

Trên trình duyệt web, nhập URL phpmyadmin sau (thay thế IP bằng IP máy chủ của bạn).

`http://192.168.33.10/phpmyadmin/`

Trên trang đăng nhập phpmyadmin, nhập người dùng ‘hakase’ bằng mật khẩu ‘ Hakaselabs001@#’ và nhấp vào nút ‘Go’.



Bây giờ chúng ta sẽ thấy bảng điều khiển phpmyadmin như dưới đây.

