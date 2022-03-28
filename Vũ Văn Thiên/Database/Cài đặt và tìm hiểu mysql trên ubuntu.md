# Tìm hiểu về Mysql

MySQL là một hệ thống quản trị cơ sở dữ liệu mã nguồn mở (Relational Database Management System, viết tắt là RDBMS) hoạt động theo mô hình client-server. RDBMS là một phần mềm hay dịch vụ dùng để tạo và quản lý các cơ sở dữ liệu (Database) theo hình thức quản lý các mối liên hệ giữa chúng.

MySQL là một trong số các phần mềm RDBMS. RDBMS và MySQL thường được cho là một vì độ phổ biến quá lớn của MySQL. Các ứng dụng web lớn nhất như Facebook, Twitter, YouTube, Google, và Yahoo! đều dùng MySQL cho mục đích lưu trữ dữ liệu. Kể cả khi ban đầu nó chỉ được dùng rất hạn chế nhưng giờ nó đã tương thích với nhiều hạ tầng máy tính quan trọng như Linux, macOS, Microsoft Windows, và Ubuntu.

Tới đây bạn đã thấy chúng tôi dùng khá nhiều thuật ngữ, hãy để chúng tôi giải thích các thuật ngữ đó cho bạn nhé:

## Lịch sử hình thành và phát triển của MySQL

Quá trình hình thành và phát triển của MySQL được tóm tắt như sau:

- Công ty Thuy Điển MySQL AB phát triển MySQL vào năm 1994.

- Phiên bản đầu tiên của MySQL phát hành năm 1995
- Công ty Sun Microsystems mua lại MySQL AB trong năm 2008

- Năm 2010 tập đoàn Oracle thâu tóm Sun Microsystems. Ngay lúc đó, đội ngũ phát triển của MySQL tách MySQL ra thành 1 nhánh riêng gọi là MariaDB. Oracle tiếp tục phát triển MySQL lên phiên bản 5.5.

- 2013 MySQL phát hành phiên bản 5.6

- 2015 MySQL phát hành phiên bản 5.7

- MySQL đang được phát triển lên phiên bản 8.0

MySQL hiện nay có 2 phiên bản miễn phí (MySQL Community Server) và có phí (Enterprise Server).

![image](https://user-images.githubusercontent.com/62273292/160376357-d08759c5-e50b-46c2-9702-244691cf4799.png)

*MySQL là một hệ quản trị cơ sở dữ liệu quan hệ rất phổ biến hiện nay*

## Ưu điểm và nhược điểm của MySQL

**Ưu điểm của MySQL là gì?**

**Dễ sử dụng:** MySQL là cơ sở dữ liệu tốc độ cao, ổn định, dễ sử dụng và hoạt động trên nhiều hệ điều hành cung cấp một hệ thống lớn các hàm tiện ích rất mạnh.

**Độ bảo mật cao:**  MySQL rất thích hợp cho các ứng dụng có truy cập CSDL trên Internet khi sở hữu nhiều nhiều tính năng bảo mật thậm chí là ở cấp cao.

**Đa tính năng:** MySQL hỗ trợ rất nhiều chức năng SQL được mong chờ từ một hệ quản trị cơ sở dữ liệu quan hệ cả trực tiếp lẫn gián tiếp.

**Khả năng mở rộng và mạnh mẽ:** MySQL có thể xử lý rất nhiều dữ liệu và hơn thế nữa nó có thể được mở rộng nếu cần thiết.

**Nhanh chóng:** Việc đưa ra một số tiêu chuẩn cho phép MySQL để làm việc rất hiệu quả và tiết kiệm chi phí, do đó nó làm tăng tốc độ thực thi.


## Nhược điểm của MySQL là gì?

Giới hạn: Theo thiết kế, MySQL không có ý định làm tất cả và nó đi kèm với các hạn chế về chức năng mà một vào ứng dụng có thể cần.

Độ tin cậy: Cách các chức năng cụ thể được xử lý với MySQL (ví dụ tài liệu tham khảo, các giao dịch, kiểm toán,…) làm cho nó kém tin cậy hơn so với một số hệ quản trị cơ sở dữ liệu quan hệ khác.

Dung lượng hạn chế: Nếu số bản ghi của bạn lớn dần lên thì việc truy xuất dữ liệu của bạn là khá khó khăn, khi đó chúng ta sẽ phải áp dụng nhiều biện pháp để tăng tốc độ truy xuất dữ liệu như là chia tải database này ra nhiều server, hoặc tạo cache MySQL



# Cài đặt mysql trên ubuntu

## Bước 1: Cập nhật và cài đặt

Cập nhật

`sudo apt update`

Cài đặt mysql 

`sudo apt install mysql-server`

![image](https://user-images.githubusercontent.com/62273292/160326830-56de43e5-4c3a-4939-b1bc-069bb76cbbec.png)

## Bước 2: Chạy cấu hình bảo mật

`sudo mysql_secure_installation`

![image](https://user-images.githubusercontent.com/62273292/160327094-23c50cfe-8ddf-4abf-ab18-bb01b5b86b9d.png)

Cài đặt mật khẩu

## Bước 3: Tạo người dùng MySQL chuyên dụng và cấp các đặc quyền

Tạo cơ sỡ dữ liệu

![image](https://user-images.githubusercontent.com/62273292/160340840-26d5090e-4395-4c31-b132-ca80b350e6bd.png)

Kiểm tra xem sql đã chạy chưa

![image](https://user-images.githubusercontent.com/62273292/160344832-5b5bfe95-1fca-4124-8922-c64fe88752ea.png)






























