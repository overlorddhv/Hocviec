# Hướng dẫn cài đặt Apache trên Ubuntu 20.04 (cấu hình web server)

Trong bài này mình sẽ hướng dẫn các bạn cách cài đặt Apache trên Ubuntu. Apache là một trong những phần mềm web server phổ biến nhất thế giới.

Apache là một máy chủ HTTP đa nền tảng và mã nguồn mở "miễn phí", nó cung cấp năng lượng lớn cho một tỉ lệ lớn các trang web trên Internet. Apache cung cấp nhiều tính năng mạnh mẽ có thể được mở rộng thông qua các mô-đun bổ sung.

   **1. Các bước cài đặt Apache trên Ubuntu 20.04
   
Nó được tích hợp sẵn trong kho lưu trữ của Ubuntu nên việc cài đặt khá đơn giản. Trên hệ thống Linux, gói dịch vụ Apache được gọi là apache2.

Như thường lệ, trước khi cài đặt một cái gì đó trên Linux, chúng ta sẽ phải update nó đầu tiên, chạy lệnh sau :

      sudo apt update
      
Sau đó, cài đặt Apache bằng cách chạy lệnh :

      sudo apt install apache2 -y (tự động yes)

Ngay sau khi quá trình cài đặt hoàn tất, nó sẽ mặc định là được khởi động. Nhưng để cho chắc chắn, chúng ta sẽ kiểm tra trạng thái của nó xem có đang được chạy không bằng lệnh sau :

      sudo service apache2 status or sudo systemctl status apache2

Đầu ra sẽ cho chúng ta biết dịch vụ có đang chạy và được khởi động hay chưa. Ảnh sau là khởi động :

![image](https://user-images.githubusercontent.com/65167293/158227013-cbffc0e8-451a-4c34-8aa8-8b18146f8fc4.png)


Vậy là xong, chúng ta đã cài đặt thành công Apache trên hệ điều hành Ubuntu của chúng ta và có thể sử dụng được nó.

**2. Kiểm tra xem cài đặt Apache trên Ubuntu 20.04 thành công không

Để xác minh rằng mọi thứ hoạt động chính xác, hãy mở trình duyệt của bạn, nhập địa chỉa IP máy chủ của bạn như sau: http://YOUR-IP/ hoặc http://localhost và nếu nó hoạt động bạn sẽ thấy trang chào mừng của Apache mặc định như hình ảnh bên dưới:

![image](https://user-images.githubusercontent.com/65167293/158227195-45be307e-d958-4760-bcb0-ea295efa081b.png)

**3. Thiết lập server ảo trên Apache**

Server ảo là một chỉ thị cấu hình Apache cho phép bạn chạy nhiều hơn một trang web trên một server duy nhất. Thông thường, một server ảo mô tả một trang web.

Apache vận chuyển với một server ảo được bật theo mặc định. Tất cả các miền trỏ đến địa chỉ IP của server sẽ khớp với các server ảo mặc định. Nếu bạn đang lưu trữ một trang web, bạn có thể tải nội dung của nó lên browser trong file /var/www/html và chỉnh sửa cấu hình server ảo có trong file /etc/apache2/sites-enabled/000-default.conf.

Nếu bạn định lưu trữ nhiều trang web, bạn sẽ cần tạo cấu hình server ảo cho từng trang web. Trong phần này, mình sẽ thiết lập một trang web có tên miền là 'freetuts.com'. Bạn có thể thay thế nó bằng tên miền của mình.

Bước đầu tiên chúng ta cần làm là tạo thư mục gốc của tài liệu nơi các tệp trang web cho tên miền sẽ được lưu trữ và phục vụ theo yêu cầu. Chúng ta chạy lệnh sau :

        sudo mkdir -p /var/www/freetuts.com
      
Tạo thêm file index.html ở bên trong thư mục gốc của tài liệu miền :

        cd /var/www/freetuts.com
        sudo nano index.html
        
![Screenshot from 2022-03-15 00-32-18](https://user-images.githubusercontent.com/65167293/158228589-685846d7-e3a8-442b-b08b-cfd582ab53d6.png)

Lưu nó và thoát ra.

Để tránh các vấn đề về quyền, hãy thay đổi quyền sở hữu thư mục gốc của tài liệu miền thành người dùng apache (www-data):

          sudo chown -R www-data: /var/www/freetuts.com

![image](https://user-images.githubusercontent.com/65167293/158228973-868fe8ca-6bbe-4fb0-8062-1c91bb6a8b2d.png)

Sau đó thoát ra :

![image](https://user-images.githubusercontent.com/65167293/158229024-2d3178f9-bc8d-4300-a6b2-c88c986c73f5.png)

Tạo cấu hình máy chủ ảo cho miền "freetuts.com", cách tốt nhất là lưu trữ từng cấu hình vhost trong một tệp riêng biệt.

Các tệp vhosts của Apache được lưu trữ trong thư mục /etc/apache2/sites-available. Quy ước đặt tên tiêu chuẩn là đặt tên tệp theo miền.

Mở text của bạn là tạo đoạn text sau :

![image](https://user-images.githubusercontent.com/65167293/158229080-1e673d66-c012-44f6-b985-3d25d7b3f5c7.png)

Sau đó thoát ra :

![image](https://user-images.githubusercontent.com/65167293/158229159-633d2364-1573-4e69-a685-8062cfce010a.png)

Apache không đọc các tệp cấu hình được tìm thấy trong thư mục /etc/apache2/sites-available trừ khi chúng được liên kết với thư mục /etc/apache2/sites-enable.

Để kích hoạt cấu hình máy chủ ảo, hãy tọa một liên kết tượng trưng bằng tiện ích a2ensite:

            sudo a2ensite freetuts.com
Kiểm tra cấu hình xem có bất kì lỗi cú pháp nào với lệnh sau:


            sudo apachectl configtest

Nếu không có lỗi bạn sẽ thấy "Syntax OK".

![image](https://user-images.githubusercontent.com/65167293/158229301-88d883b8-cc1a-47d3-bec7-04ff73d7b48e.png)

Khởi động lại dịch vụ Apache bằng lệnh :

          sudo systemctl restart apache2 or sudo service apache2 restart
          
Kết quả đạt được

![image](https://user-images.githubusercontent.com/65167293/158229652-d2a603f5-d084-4b96-a78e-2a3e796c0f02.png)

# Cách tạo Apache Virtual Host trên Ubuntu 20.04

**1. Cấu trúc thư mục của Virtual Host Apache trên Linux**

Trên Apache Server, mỗi website sẽ có một thư mục chứa mã nguồn riêng, hay còn gọi là thư mục gốc. Nhiệm vụ của server là dựa vào domain đang request để gọi tới đúng thư mục gốc.

Ví dụ dưới đây là cấu trúc thư mục của hai website, được đặt trong /var/ww/.

            /var/www/
            ├── domain1.com
            │   └── public_html
            ├── domain2.com
            │   └── public_html
            
Như vậy, mỗi website sẽ có thư mục gốc dạng như sau:

            /var/www/<domain_name>/public_html
    
Bây giờ mình cần tạo host cho domain1.com thì các bước thực hiện như sau.

Đầu tiên hãy chạy lệnh dưới đây để tạo thư mục gốc cho domain1 bằng cách sử dụng lệnh mkdir.

              sudo mkdir -p /var/www/domain1.com/public_html

Bạn chú ý nhé, tên của thư mục phải trùng với tên của domain.

Bây giờ ta sẽ tạo một file index.html nằm trong thư mục public_html vừa tạo, để khi chạy web thì file này sẽ được chạy.

                /var/www/domain1.com/public_html/index.html

                <!DOCTYPE html>
                <html lang="en">
                  <head>
                    <meta charset="utf-8">
                    <title>Welcome to domain1.com</title>
                  </head>
                  <body>
                    <h1>Success! domain1.com home page!</h1>
                  </body>
                </html>
Giống như trong bài Nginx, vì mình sử dụng lệnh sudo để tạo các file nên nó thuộc quyền sở hữu của nhóm root. Để tránh các vấn đề rắc rối về phân quyền sau này thì hãy đổi nó sang sở hữu của Apache (www-data).

                sudo chown -R www-data: /var/www/domain1.com

2. Tạo Virual Host Apache để chạy nhiều web trên Ubuntu 20.04
Trên hệ thống của Ubuntu, file cấu hình virtual host các domain có sẵn nằm trong thư mục /etc/apache2/sites-available. Nó có thể được kích hoạt bằng cách tạo một symbolic links tới thư mục /etc/apache2/sites-enabled, và Apache sẽ đọc trong khi chạy.

Hãy sử dụng text editor bất kì để mở file /etc/apache2/sites-available/domain1.com.conf lên nhé. Mình sử dụng VI Editor, rồi nhập nội dung sau vào:

                  /etc/apache2/sites-available/domain1.com.conf

                  <VirtualHost *:80>
                      ServerName domain1.com
                      ServerAlias www.domain1.com
                      ServerAdmin webmaster@domain1.com
                      DocumentRoot /var/www/domain1.com/public_html

                      <Directory /var/www/domain1.com/public_html>
                          Options -Indexes +FollowSymLinks
                          AllowOverride All
                      </Directory>

                      ErrorLog ${APACHE_LOG_DIR}/domain1.com-error.log
                      CustomLog ${APACHE_LOG_DIR}/domain1.com-access.log combined
                  </VirtualHost>
Trong đó:

ServerName là tên của domain.

ServerAlias là danh sách sub domain hoặc domain có www.

DocumentRoot là thư mục chứa mã nguồn website.

Options: sẽ có hai sựa lựa chọn:

Indexes: Sử dụng đường link thực

FollowSymLinks: Sư dụng đường link ảo (symlink)

AllowOverride cho phép sử dụng .htaccess để ghi đè cấu hình server.

ErrorLog, CustomLog là hai file lưu log.

Bạn có thể đặt một cái tên bất kì cho file cấu hình mỗi trang web. Tuy nhiên, khuyến khích bạn đặt theo tên domain, vì khi bạn quản lý nhiều domain sẽ dễ dàng nhớ và phân biệt giữa chúng.

Để kích hoạt máy ảo thì mình sử dụng a2ensite script để hỗ trợ để tạo symbolic link từ virtual host đến thư mục sites-enabled.

            sudo a2ensite domain1.com

Và dưới đây là lệnh tạo symbolic link:

            sudo ln -s /etc/apache2/sites-available/domain1.com.conf /etc/apache2/sites-enabled/

Chạy xong tihì hãy tiếp tục thực hiện lệnh này để test nhé:

            sudo apachectl configtest

Nếu kết quả trả vè như sau là bạn đã thành công:

            Syntax OK

Khởi động lại Apache để áp dụng những thay đổi:

            sudo systemctl restart apache2

Cuối cùng, hãy truy cập vào http://domain1.com để xem thành quả mà bạn đã làm nhé.

Như vậy là mình đã hướng dẫn xong cách tạo Virtual Host Apache trên Ubuntu 20.04. Qua bài này bạn đã biết cách tạo và quản lý nhiều domain trên Ubuntu server thông qua Apache.

# Kết quả

![Screenshot from 2022-03-14 23-06-52](https://user-images.githubusercontent.com/65167293/158230882-1f18928f-fceb-43d4-9221-ba5cd65c0353.png)
