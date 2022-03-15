# Giao thức FTP

## FTP là gì?

FTP - File Transfer Protocol (Giao thức truyền tải tập tin) được dùng trong việc trao đổi dữ liệu trong mạng thông qua giao thức TCP/IP, thường hoạt động trên 2 cổng là 20 và 21. Với giao thức này, các máy client trong mạng có thể truy cập đến máy chủ FTP để gửi hoặc lấy dữ liệu. Điểm nổi bật là người dùng có thể truy cập vào máy chủ FTP để truyền và nhận dữ liệu dù đang ở xa.

## Mô hình hoạt động của giao thức FTP

Giao thức FTP hoạt động dựa trên mô hình cơ bản của việc truyền và nhận dữ liệu từ máy Client đến máy Server. Quá trình truyền nhận dữ liệu giữa máy Client và Server lại được tạo nên từ 2 tiến trình TCP logic là Control Connection và Data Connection.

![image](https://user-images.githubusercontent.com/62273292/158323595-78bdcf17-43ee-4b5c-a00b-d4e158fc96d4.png)

- Control Connection: Đây là phiên làm việc TCP logic đầu tiên được tạo ra khi quá trình truyền dữ liệu bắt đầu. Tuy nhiên, tiến trình này chỉ kiểm soát các thông tin điều khiển đi qua nó, ví dụ như các tập lệnh. Quá trình này sẽ được duy trì trong suốt quá trình phiên làm việc diễn ra.
- Data Connection: Khác với tiến trình Control Connection, Data Connection là một kết nối dữ liệu TCP được tạo ra với mục đích chuyên biệt là truyền tải dữ liệu giữa máy Client và máy Server. Kết nối sẽ tự động ngắt khi quá trình truyền tải dữ liệu hoàn tất.

## Các phương thức truyền dữ liệu trong giao thức FTP

Khi quá trình truyền dữ liệu được thiết lập, dữ liệu sẽ được truyền từ máy Client đến máy Server hoặc có thể ngược lại. Dựa trên việc truyền dữ liệu này, FTP có 3 phương thức truyền tải dữ liệu là stream mode, block mode, và compressed mode.
- Stream mode: Phương thức này hoạt động dựa vào tính tin cậy trong việc truyền dữ liệu trên giao thức TCP. Dữ liệu sẽ được truyền đi dưới dạng các byte có cấu trúc không liên tiếp. Thiết bị gửi chỉ đơn thuần đẩy luồng dữ liệu qua kết nối TCP tới phía nhận mà không có một trường tiêu đề nhất định.
- Block mode:  Là phương thức truyền dữ liệu mang tính quy chuẩn hơn. Với phương thức này, dữ liệu được chia thành nhiều khối nhỏ và được đóng gói thành các FTP blocks. Mỗi block sẽ chứa thông tin về khối dữ liệu đang được gửi.
- Compressed mode:  Phương thức truyền sử dụng kỹ thuật nén dữ liệu khá đơn giản là “run-length encoding”. Với thuật toán này, các đoạn dữ liệu bị lặp sẽ được phát hiện và loại bỏ để giảm chiều dài của toàn bộ thông điệp khi gửi đi.
![image](https://user-images.githubusercontent.com/62273292/158324568-c4fc0768-512d-4689-9192-df5657de1bd8.png)

## Cách xây dựng một máy chủ FTP đơn giản

Trước đây, việc xây dựng một máy chủ FTP khá phức tạp và tốn kém đối với mọi người. Nhất là các doanh nghiệp chưa có riêng cho mình một phòng server và những hộ gia đình có nhu cầu sử dụng nhưng ngại thực hiện vì chi phí tốn kém. Nhưng giờ đây, việc xây dựng một máy chủ FTP để truyền và nhận dữ liệu trở nên hoàn toàn dễ dàng khi được tích hợp sẵn trên các Router.

Các doanh nghiệp hay hộ gia đình chỉ cần sở hữu một thiết bị Router có tích hợp tính năng FTP. Sau đó, đầu tư thêm 1 bộ nhớ ngoài như USB hoặc ổ cứng với dung lượng thích hợp với nhu cầu cần sử dụng. Kết nối bộ nhớ với Router và cài đặt các thông số cần thiết theo hướng dẫn từ nhà sản xuất. Vậy là một máy chủ FTP đã được dựng thành công.
