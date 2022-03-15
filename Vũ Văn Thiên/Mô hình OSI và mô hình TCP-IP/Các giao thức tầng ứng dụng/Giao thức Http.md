
## Giao thức HTTP là gì?

HTTP là từ viết tắt của Hyper Text Transfer Protocol nghĩa là Giao thức Truyền tải Siêu Văn Bản được sử dụng trong www. HTTP là 1 giao thức cho phép tìm nạp tài nguyên, chẳng hạn như HTML doc.

Nó là nền tảng của bất kỳ sự trao đổi dữ liệu nào trên Web và cũng là giao thức giữa client (thường là các trình duyệt hay bất kỳ loại thiết bị, chương trình nào) và server (thường là các máy tính trên đám mây). 1 doc hoàn chỉnh được tái tạo từ các doc con khác nhau được fetch – tìm nạp, chẳng hạn như văn bản, mô tả layout, hình ảnh, video, script v..v..

Được thiết kế lần đầu từ những năm 90, HTTP là 1 giao thức có thể mở rộng vốn đã phát triển dần theo thời gian. 1 giao thức lớp ứng dụng được gửi thông qua nền tảng TCP/IP , hay qua 1 kết nối TCP được mã hóa TLS. Mặc dù về mặt lý thuyết, bất kỳ giao thức truyền tải đáng tin cậy nào cũng có thể được sử dụng.

Nhờ vào khả năng mở rộng của nó, HTTP được sử dụng để không chỉ tìm nạp các tài liệu siêu văn bản mà còn cả hình ảnh và video hoặc để đăng tải nội dung lên server, giống như với các kết quả form HTML. HTTP cũng có thể được sử dụng để tìm nạp các phần của các doc nhằm cập nhật các trang web theo yêu cầu.

## Khía cạnh cơ bản của HTTP?

HTTP là gì? HTTP là 1 giao thức tuy đơn giản nhưng khá mạnh mẽ nhờ vào các đặc trưng cơ bản sau đây.

**HTTP đơn giản:**

HTTP thường được thiết kế để trở nên đơn giản và thân thiện để con người có thể đọc được, ngay cả khi có thêm sự phức tạp được giới thiệu trong HTTP/2 bằng cách đóng gói các HTTP message thành các frame. Với các HTTP message, chúng ta có thể được đọc và hiểu được, cung cấp khả năng testing hơn cho các dev và giảm thiểu độ phức tạp cho bất cứ người mới nào.

**HTTP có thể mở rộng:**

Được giới thiệu trong HTTP/1.0, các header HTTP làm cho giao thức này dễ dàng mở rộng và thử nghiệm hơn nữa. Chức năng mới thậm chí có thể được giới thiệu bằng 1 thỏa thuận đơn giản giữa 1 client và 1 máy chủ về ngữ nghĩa của 1 header mới.

**HTTP là stateless, nhưng không sessionless:**

Không có liên kết giữa 2 yêu cầu được thực hiện liên tiếp trên cùng 1 kết nối. Điều này ngay lập tức có khả năng trở thành vấn để với người dùng cố gắng tương tác với các trang nhất định 1 cách mạch lạc, chẳng hạn như sử dụng shopping cart trên các trang e-commerce, tức thương mại điện tử.

Nhưng trong khi cốt lõi bản thân HTTP là stateless, các cookie HTTP cho phép sử dụng các session trạng thái. Sử dụng khả năng mở rộng header, các cookie HTTP được thêm vào quy trình vận hành, cho phép tạo các session trên mỗi yêu cầu HTTP để chia sẻ cùng 1 ngữ cảnh hay cùng 1 trạng thái.

## Cấu trúc cơ bản của HTTP

Qua sơ đồ bên dưới, các bạn sẽ thấy được cấu trúc khá đơn giản của 1 ứng dụng web và miêu tả cụ thể vị trí của HTTP là gì:
![alt text]()
