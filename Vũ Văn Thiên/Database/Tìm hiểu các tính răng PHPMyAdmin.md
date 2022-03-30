# PHPMyAdmin là gì?

PhpMyAdmin là phần mềm mã nguồn mở được viết bằng ngôn ngữ PHP giúp quản trị cở sở dữ liệu MySQL thông qua giao diện web. Tính đến nay, phpMyAdmin đã có đến hàng triệu lượt sử dụng và vẫn không ngừng tăng. Vậy tính năng hữu ích mà phpMyAdmin mang lại là gì?

![image](https://user-images.githubusercontent.com/62273292/160774293-e21c46a2-3737-45c6-855b-98c30c0e36ee.png)

*phpMyAdmin được viết bằng ngôn ngữ PHP*


## Các tính năng của phpMyAdmin là gì?

![image](https://user-images.githubusercontent.com/62273292/160774929-f549f0eb-5649-4d5e-aa60-a152f3c76740.png)

Một số tính năng chung thường được sử dụng trên phpMyAdmin:

- Quản lý user(người dùng): thêm, xóa, sửa(phân quyền).

- Quản lý cơ sở dữ liệu: tạo mới, xóa, sửa, thêm bảng, hàng, trường, tìm kiếm đối tượng.
 
- Nhập xuất dữ liệu(Import/Export): hỗ trợ các định dạng SQL, XML và CSV.

- Thực hiện các truy vấn MySQL, giám sát quá trình và theo dõi.

- Sao lưu và khôi phục(Backup/Restore): Thao tác thủ công.

Điểm yếu trong việc sao lưu dữ liệu của phpMyAdmin là gì?

 
 Dù có nhiều ưu điểm song phpMyAdmin vẫn khó tránh khỏi một vài điểm yếu cố hữu. Đặc biệt, trong việc sao lưu dữ liệu thủ công sẽ không có một vài tính năng cần thiết.

Scheduling(sao lưu tự động theo lịch đặt trước): Một tính năng khá phổ biến ở những công cụ quản trị cơ sở dữ liệu.

Storage media support(hỗ trợ lưu trữ các phương tiện truyền thông): phpMyAdmin chỉ cho phép lưu các bản sao lưu vào các local drive có sẵn trên hệ thống, qua hộp thoại Save as của trình duyệt.
 
 ## Cách sử dụng PHPMyAdmin
 
- Truy cập vào phpMyAdmin

- Quản lý cơ sở dữ liệu

- Quản lý table (bảng dữ liệu)

- Thực hiện truy vấn

- Sao lưu cơ sở dữ liệu
 
Giao diện sau khi đăng nhập
 
 ![image](https://user-images.githubusercontent.com/62273292/160780728-6b28b8aa-42f1-4db2-be8e-0edb178edb54.png)
*Giao diện sau khi đăng nhập thành công*

- Truy cập vào phpmyadmin

Nhập địa chỉ ip của hệ điều hành linux(ubuntu) với dạng như sau sẽ vào được 

`ip/phpmyadmin` 

- Quản lý cơ sở dữ liệu

Tạo cơ sỡ dữ liệu mới

![image](https://user-images.githubusercontent.com/62273292/160783571-ba9dc82e-2a8e-4ae8-9e5b-d3ce0d00cc66.png)

Quản lý table 

Tạo bảng user

![image](https://user-images.githubusercontent.com/62273292/160783877-13be70a3-c630-4c00-9c73-c632a817e6c6.png)

Nhập các trường trong bảng

![image](https://user-images.githubusercontent.com/62273292/160784468-d19c609d-c38f-443d-8731-0a4ebae31ab1.png)

- Thực hiện truy vấn


 ![image](https://user-images.githubusercontent.com/62273292/160784828-ab985f5f-d80c-42d3-9111-053852278777.png)

 Kết quả
 
 ![image](https://user-images.githubusercontent.com/62273292/160784947-13754f36-b8cd-4caa-be91-a431d50495db.png)


 - Sao lưu cơ sở dữ liệu

![image](https://user-images.githubusercontent.com/62273292/160791055-28964b19-af4f-4179-8d97-e648f27fdd2a.png)

file đã được lưu

![image](https://user-images.githubusercontent.com/62273292/160791276-ba148993-ee34-4bf2-94f8-34bb99155ed6.png)

 Phục hồi cơ sở dữ liệu
 
 Song song với sao lưu đó là chức năng phục hồi, đối với file sao lưu đã được tải ở bước trên. Các bạn tạo mới một cơ sở dữ liệu, chọn tên từ cột bên trái và truy cập tab Import, dùng thẻ Chọn tệp để tìm file sao lưu, chọn đúng kiểu file là SQL, nhấn Go.
 
 ![image](https://user-images.githubusercontent.com/62273292/160792090-71492675-2fd4-4eda-8fc8-d4d1fb7b6b77.png)

Cơ sỡ dữ liệu phục hồi thành công

 ![image](https://user-images.githubusercontent.com/62273292/160792322-a2e990ce-a5cc-469c-9ca7-a899cd4f3dd8.png)

 
 
 Ưu điểm của phpMyAdmin là gì?
 
- Tăng hiệu quả công tác quản lý cơ sở dữ liệu

-Cộng đồng hỗ trợ rộng lớn

-Đa ngôn ngữ

-Chi phí
 
 
 **Tăng hiệu quả công tác quản lý cơ sở dữ liệu**
 
 phpMyAdmin mang đến giao diện xử lý các thao tác trên cơ sở dữ liệu một cách trực quan. Từ đó, tiết kiệm thời gian, thao tác so với việc thực hiện bằng dòng lệnh trên command line.

Là công cụ đa năng có thể vừa làm việc với một đối tượng vừa xử lý lỗi hoặc các tính huống bất ngờ.

**Cộng đồng hỗ trợ rộng lớn**

phpMyAdmin có tính chất là một mã nguồn mở, được phát triển bởi rất nhiều lập trình viên trên toàn thế giới. Nhờ đó, người dùng sẽ nhận được sử hỗ trợ rất lớn từ cộng đồng.

**Đa ngôn ngữ**

Được duy trì bởi The phpMyAdmin Project hiện có sẵn đến 64 ngôn ngữ khác nhau.

**Chi phí**

Dù có nhiều ưu điểm và mang đến nhiều lợi ích vượt bậc, phpMyAdmin vẫn là công cụ hoàn toàn miễn phí.

## Nhược điểm của phpMyAdmin là gì?
 
 
 – Bảo mật
 
 Hạn chế lớn nhất của các mã nguồn mở chắc chắn là vấn đề bảo mật. Hạn chế truy cập vào URL của phpMyAdmin từ những địa chỉ IP cố định.
 
 – Sao lưu
 
 Như đã chia sẻ, thao tác sao lưu và phục hồi dữ liệu thủ công trên phpMyAdmin vẫn còn một số nhược điểm:

Không thể tự xuất database.

Chỉ có thể kết nối thông qua trình duyệt tức chỉ lưu được các bản sao lưu vào các local drive có sẵn trên hệ thống.

Định dạng file xuất bằng phpMyAdmin không được mã hóa(thiếu an toàn) và chiếm dung lượng đĩa lớn.
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
