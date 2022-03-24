# Cài đặt Lighttpd trên Ubuntu 20.04

Lighttpd là một giải pháp thay thế rất phổ biến cho các máy chủ web phổ biến trên hệ điều hành họ Unix. Nhờ đó, Chúng tôi có thể tìm thấy nó có sẵn thông qua các kho lưu trữ Ubuntu 20.04 chính. Do đó, để cài đặt nó trong Ubuntu 20.04, chúng tôi sẽ chỉ phải mở một thiết bị đầu cuối (Ctrl + Alt + T) và thực hiện lệnh:

`sudo apt install lighttpd`

![image](https://user-images.githubusercontent.com/62273292/159820895-08069241-3aba-492d-8f22-f1a2b688eda2.png)


Lighttpd được quản lý như một dịch vụ hệ thống, và do đó chúng tôi sẽ có thể bắt đầu nó bằng cách nhập vào thiết bị đầu cuối:

`sudo systemctl start lighttpd`

Và chúng tôi có thể dừng nó lại với lệnh khác này:

`sudo systemctl stop lighttpd`

Nó cũng sẽ cung cấp cho chúng tôi khả năng biết tình trạng của dịch vụ gõ vào thiết bị đầu cuối:

![image](https://user-images.githubusercontent.com/62273292/159820985-8d59cac7-121f-4997-b149-d7b52ec36ee7.png)


`sudo systemctl status lighttpd`

Mở trình duyệt và truy cập vào địa chỉ ip của mình

![image](https://user-images.githubusercontent.com/62273292/159821151-3a1832de-39b8-48d5-9fbc-9d602b735bb7.png)


## Thêm hỗ trợ PHP vào Lighttpd

Phải nói rằng chúng tôi sẽ cần cài đặt PHP để các trang web động có thể được thông dịch, vì theo mặc định thì không. Với điều này, chúng tôi đảm bảo rằng một phần tốt các ứng dụng được tạo bằng ngôn ngữ này có thể được sử dụng trên máy chủ của chúng tôi. Chúng tôi sẽ có thể cài đặt PHP bằng lệnh sau:

`sudo apt install php7.4 php7.4-fpm php7.4-mysql php7.4-cli php7.4-curl php7.4-xml`

![image](https://user-images.githubusercontent.com/62273292/159821309-c8647375-c6dd-4fd4-a4b6-121040326bfb.png)

Khi quá trình cài đặt PHP hoàn tất, cần thực hiện một số thay đổi nhỏ để Lighttpd có thể hoạt động với PHP và thông dịch các trang web. Điều đầu tiên sẽ là mở một trong những tệp cấu hình với trình soạn thảo yêu thích của chúng tôi:

`sudo vim /etc/php/7.4/fpm/pool.d/www.conf`

Y bên trong tệp thay đổi giá trị của 'nghe' a:

![image](https://user-images.githubusercontent.com/62273292/159821357-f5837a4d-5902-424e-acbf-dd285df50535.png)

`listen = 127.0.0.1:9000`

Sau đó, chúng tôi lưu các thay đổi và đóng tệp. Bước tiếp theo sẽ là thực hiện nhiều thay đổi hơn đối với tệp cấu hình khác. Vì vậy, hãy mở nó:

	
`sudo vim /etc/lighttpd/conf-available/15-fastcgi-php.conf`

Và bên trong chúng ta sẽ thay đổi những dòng sau:

```
"bin-path" => "/usr/bin/php-cgi",
"socket" => "/var/run/lighttpd/php.socket",
```

![image](https://user-images.githubusercontent.com/62273292/159821469-5e01ca6c-8bbd-4bc8-86f3-c815b40114dc.png)


```
"host" => "127.0.0.1",
"port" => "9000",
```

Khi hoàn tất, chúng tôi lưu các thay đổi và đóng tệp

Tại thời điểm này, bạn chỉ cần chạy các lệnh sau để kích hoạt các mô-đun giúp Lighttpd hoạt động với PHP:

![image](https://user-images.githubusercontent.com/62273292/159821525-bf3ec72d-a905-4f68-9ff0-60d9ec3ec8e8.png)


```
sudo lighty-enable-mod fastcgi
 
sudo lighty-enable-mod fastcgi-php
```

Đã kết thúc khởi động lại các dịch vụ Lighttpd và php-fpm:

`sudo systemctl restart lighttpd php7.4-fpm`

Kiểm tra xem PHP đã được kích hoạt chưa

Để kiểm tra xem mọi thứ chúng tôi đã làm có hoạt động không, chúng ta sẽ viết một tệp PHP trong thư mục gốc của Lighttpd, và sau đó mở nó bằng trình duyệt.

Chúng ta sẽ tạo tệp này bằng lệnh:

`sudo vim /var/www/html/test.php`

Bên trong tệp, chúng tôi sẽ dán văn bản sau. Sau đó, chúng tôi lưu và đóng tệp.

<?php phpinfo();?>

Đã trả lại tại nhà ga, chúng tôi sẽ phải thay đổi quyền của thư mục và đặt Lighttpd làm chủ sở hữu của nó. Chúng tôi sẽ thực hiện điều này bằng cách thực hiện các lệnh:

![image](https://user-images.githubusercontent.com/62273292/159821644-66c05e4a-6f32-4548-8637-ca36e4e7a8f5.png)


```
sudo chown -R www-data:www-data /var/www/html/
 
sudo chown -R 755 /var/www/html/
```

Khởi động trình duyệt chạy Localhost/test.php

![image](https://user-images.githubusercontent.com/62273292/159821756-9c73d3b0-e8ee-416a-8c63-b0a06e8cdf32.png)







