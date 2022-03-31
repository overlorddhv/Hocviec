# Tìm hiểu về MariaDB

## MariaDB là gì?

**MariaDB là hệ quản trị cơ sở dữ liệu miễn phí được phát triển từ hệ quản trị cơ sở dữ liệu mã nguồn mở MySQL**. MariaDB được phát triển nhằm thay thế công nghệ cơ sở dữ liệu MySQL, vì thế nó tương thích và cho một hiệu suất cao hơn so với MySQL. Ưu điểm khi sử dụng MariaDB là gì?

![image](https://user-images.githubusercontent.com/62273292/160368019-16268d64-3641-4592-9a6f-8276fad69269.png)

MariaDB được Michael “Monty” Widenius, developer hàng đầu của MySQL dẫn dắt và phát triển. Ưu điểm lớn nhất của hệ quản trị này là tương thích với nhiều hệ điều hành, bao gồm Linux CentOS, Ubuntu và Window với các gói cài đặt tar, zip, MSI, rpm cho cả 32bit và 64bit với hiệu suất cao hơn so với MySQL. 

Vì thế, MariaDB đang ngày càng được đông đảo các nhà phát triển sử dụng, trong đó có wikipedia, Fullstack-Station,… MariaDB đang có xu hướng thay thế cho MySQL – hệ quản trị cơ sở dữ liệu mã nguồn mở lâu đời nhất được sử dụng từ trước đến nay.

Nền móng cơ sở đầu tiên của MariaDB được phát triển bởi “trụ cột” của MySQL AB là Michael “Monty” Widenius. Năm 2008, sau khi Sun mua lại MySQL AB, Michael “Monty” Widenius rời khỏi MySQL AB và tiếp tục phát triển một hệ cơ sở quản trị mới của mình.

Đầu năm 2009, Michael cùng với 1 vài đồng nghiệp khác bắt đầu tiến hành dự án chuyên sâu về công cụ lưu trữ MySQL, sau này trở thành MariaDB. Tên gọi MariaDB được đặt tên theo tên con gái út của Widenius – Maria. Sau nhiều lần nâng cấp và phát triển, hiện tại MariaDB đã ra mắt phiên bản mới nhất là MariaDB 10.1.

MariaDB được hình thành dựa trên nền tảng của MySQL, vì thế nó kế thừa được hầu hết các chức năng cơ bản cần thiết của MySQL. Bên cạnh đó, MariaDB cũng phát triển thêm nhiều tính năng mới và có sự nâng cấp hơn về cơ chế lưu trữ, tối ưu máy chủ.

MariaDB có 2 bản trả phí và không cần trả phí. Tuy nhiên, với phiên bản không trả phí, người dùng vẫn có thể sử dụng đầy đủ các tính năng mà không ảnh hưởng đến việc chạy hệ thống.

## Ưu điểm của MariaDB là gì?

![image](https://user-images.githubusercontent.com/62273292/160370307-7db726e3-f787-4740-8602-15ec130768db.png)


Không phải ngẫu nhiên mà MariaDB được nhiều người yêu thích và sử dụng đến vậy. Những ưu điểm lớn nhất của hệ quản trị này phải kể đến bao gồm:

-Hoàn toàn miễn phí

-Khắc phục những hạn chế của MySQL

-Bổ sung thêm nhiều Engine hơn

-Kết hợp cả SQL và NoSQL

-Hỗ trợ tiếng Việt

**Hoàn toàn miễn phí**

Đây là một hệ quản trị sử dụng mã nguồn mở hoàn toàn miễn phí. Do đó, người dùng không cần phải bỏ tiền mua bản quyền và vẫn có thể sử dụng đầy đủ những tính năng của phần mềm này.

**Khắc phục những hạn chế của MySQL**

MariaDB được phát triển từ MySQL, do đó nó kế thừa những đặc điểm chủ yếu của hệ quản trị này từ phiên bản 5.1 -> 5.5. Do đó, người dùng có thể chuyển từ MySQL sang MariaDB mà không ảnh hưởng đến hệ thống. 

Đặc biệt, những hạn chế của MySQL, khi chuyển qua MariaDB đều sẽ được khắc phục một cách triệt để nhất, thậm chí có thể tăng tốc độ hơn so với MySQL từ 3-5%. Ngoài ra, hệ quản trị này còn cải thiện hiệu năng và có thêm nhiều chức năng mới hơn so với MySQL.

**Bổ sung thêm nhiều Engine hơn**

Ngoài các storage engines cơ bản như MyISAM, BLACKHOLE, CSV, MEMORY, ARCHIVE, MERGE; MariaDB còn phát triển thêm các storage engines khác bao gồm: Aria, XtraDB, FederatedX, OQGRAPH, SphinxSE, IBM DB2I, Spider, PBXT,…

**Kết hợp cả SQL và NoSQL**

MariaDB là sự kết hợp của cả 2 loại cơ sở dữ liệu là SQL và NoSQL. Việc kết hợp sẽ giúp hệ thống này có thể tích hợp được tất cả ưu điểm của cả 2 cơ sở dữ liệu này là Dynamic Column và Cassandra Storage Engine.

**Hỗ trợ tiếng Việt**

Một ưu điểm tuyệt vời của MariaDB là đã có bản tiếng Việt. Mặc dù bản dịch chưa thật sự hoàn hảo nhưng vẫn có thể hỗ trợ nhiều cho người dùng.



## So sánh giữa MySQL và MariaDB

**Điểm khác biệt giữa MySQL và MariaDB là gì? **

Cả MySQL và MariaDB đều là những hệ quản trị cơ sở dữ liệu phổ biến và được nhiều chuyên gia đánh giá cao. Tuy nhiên, giữa 2 hệ thống này cũng có những điểm khác biệt như sau:

- Về cơ sở hình thành

- Ngôn ngữ lập trình hỗ trợ

- Công cụ lưu trữ

**Về cơ sở hình thành**

Sự khác biệt trong cơ sở hình thành với MariaDB là gì? MySQL được hình thành từ năm 1995 dựa trên cơ sở của C / C ++, và hiện tại được duy trì và phát triển bởi đội ngũ Oracle.

Phiên bản đầu tiên của MariaDB ra mắt vào năm 2009, được phát triển trên nền tảng MySQL và thừa kế những ưu điểm của MySQL.

Theo số liệu thống kê, trong số các hệ thống quản trị cơ sở dữ liệu, MySQL xếp ở vị trí thứ 2 trong khi MariaDB xếp ở vị trí thứ 9.

**Khác biệt giữa mã nguồn MYSQL và MariaDB là gì?**


-MySQL: Mã nguồn đóng

-MariaDB: Mã nguồn mở

**Ngôn ngữ lập trình hỗ trợ**

- MySQL: Ada, C, C#, C++, D, Delphi, Eiffel, Erlang, Haskell, Java, JavaScript (Node.js), Objective-C, OCaml, Perl, PHP, Python, Ruby, Scheme, Tcl

- MariaDB: Cũng tương tự MySQL nhưng không hỗ trợ Delphi

**Công cụ lưu trữ**

- MySQL sẽ bao gồm các công cụ lưu trữ sau: InnoDB, MyISAM, BLACKHOLE, CSV, MEMORY, ARCHIVE, MERGE.

- MariaDB bao gồm: InnoDB, MyISAM, BLACKHOLE, CSV, MEMORY, ARCHIVE, MERGE, ColumnStore, MyRocks, Aria, SphinxSE, TokuDB, CONNECT, SEQUENCE, Spider, Cassandra.















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

Đã tạo thành công database.

![image](https://user-images.githubusercontent.com/62273292/160353030-0f8456f5-0aaa-46fd-835f-8ba62e1f2351.png)


##  Export database (xuất dữ liệu)

Tạo 1 thư mục để lưu file khi xuất dữ liệu

`mkdir dbbackup`

![image](https://user-images.githubusercontent.com/62273292/160971401-d14f3751-dd2d-43fe-b23b-80b2afc5b7f4.png)


Di chuyển đến mục vừa tạo

`cd dbbackup`

![image](https://user-images.githubusercontent.com/62273292/160971458-f637e195-0fc5-4a86-830f-fbc24d1389f6.png)

 Xuất dữ liệu
 
 `mysqldump -u vanthienn -p thiendatabase > hihi.sql`


![image](https://user-images.githubusercontent.com/62273292/160971350-367eefa6-02be-4a74-a6b2-a237e731e29a.png)

## Import database (nhập dữ liệu)

Xóa cơ sở dữ liệu trước khi import dữ liệu

![image](https://user-images.githubusercontent.com/62273292/160972773-f3269114-9c7e-4005-8a76-cafc8399e735.png)

Tạo database mới

![image](https://user-images.githubusercontent.com/62273292/160972904-90b85353-107c-4a51-a181-d7d15b8765af.png)

Di chuyển đến mục lưu trữ file đã lưu,

`cd dbbackup`

Bắt đầu import file đã lưu

`mysql -u vanthienn -p thiendatabase < hihi.sql`

![image](https://user-images.githubusercontent.com/62273292/160974147-261fa92c-1403-414d-95dc-4a825f2f20e6.png)

Vào Mysql, sử dụng tên database và kiểm tra bảng đã có chưa, kiểm tra dữ liệu và hoàn tất


![image](https://user-images.githubusercontent.com/62273292/160974264-e47b904b-8efe-4655-bfc1-ade100669fab.png)

























