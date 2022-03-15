# Mô hình OSI là gì?

Mô hình OSI (Open system interconnection – Mô hình kết nối các hệ thống mở) là một thiết kế dựa vào nguyên lý tầng cấp, lý giải một cách trừu tượng kỹ thuật kết nối truyền thông giữa các máy vi tính và thiết kế giao thức mạng giữa chúng. Mô hình này được phát triển thành một phần trong kế hoạch OSI (Open Systems Interconnection) do ISO và IUT-T khởi xướng. Nó còn được gọi là Mô hình bảy tầng của OSI.

**Mô hình OSI dùng để làm gì?**

Mô hình OSI được tạo ra với mục đích là cho phép sự tương giao (interoperability) giữa các hệ máy (platform) đa dạng được cung cấp bởi các nhà sản xuất khác nhau. Mô hình cho phép tất cả các thành phần của mạng hoạt động hòa đồng, bất kể thành phần ấy do ai tạo dựng. Vào những năm cuối thập niên 1980, ISO đã tiến cử việc thực thi mô hình OSI như một tiêu chuẩn mạng.

**Những ưu điểm của OSI đó là:**
- OSI phân thành nhiều tầng nhỏ và đơn giản hơn.
- OSI chuẩn hóa các thành phần mạng để phát triển dễ dàng hơn.
- OSI chuẩn hóa giao diện giữa các tầng.
- Dữ liệu được truyền nhanh chóng và dễ dàng hơn.

**Nhược điểm**
- Tầng phiên và tầng trình diễn thường không được sử dụng nhiều so với các tầng khác vì chức năng hạn hẹp của nó.
- Không hỗ trợ các giao thức, không định nghĩa bất kì giao thức nào.
- Nhiều dịch vụ trùng lặp tại các tầng, ví dụ tầng mạng và tầng liên kết dữ liệu.
- Các tầng không thể hoạt động song song, tầng dưới phải chờ dữ liệu từ tầng trên.

# Mô hình TCP/IP là gì?

TCP/ IP (Transmission Control Protocol/ Internet Protocol - Giao thức điều khiển truyền nhận/ Giao thức liên mạng), là một bộ giao thức trao đổi thông tin được sử dụng để truyền tải và kết nối các thiết bị trong mạng Internet. TCP/IP được phát triển để mạng được tin cậy hơn cùng với khả năng phục hồi tự động.
Cụ thể hơn, TCP/IP chỉ rõ cho chúng ta cách thức đóng gói thông tin (còn được gọi là gói tin ), được gửi và nhận bởi các máy tính có kết nối với nhau.

**Ưu điểm của TCP/IP là:**

- Mô hình TCP/IP không chịu sự kiểm soát của tổ chức nào. Do đó, người dùng có thể tự do sử dụng.
- TCP/IP có khả năng tương thích với các mạng, hệ điều hành và phần cứng máy tính.
- TCP/IP có khả năng khả năng định tuyến, mở rộng và nhận định được đường dẫn tốt nhất thông qua mạng.

**Nhược điểm**
- Khó khăn trong việc thay thế các giao thức mới.
- Một tầng có nhiều chức năng nên phức tạp hơn so với mô hình OSI.
- Không có sự phân biệt dõ dàng giữa dịch vụ, giao diện và giao thức.


# So sánh giữa 2 mô hình
– Giống nhau: Mô hình OSI và TCP/IP có một số điểm chung như sau:
  - OSI và TCP/IP đều có kiến trúc phân lớp.
  - OSI và TCP/IP đều có lớp Network và lớp Transport.
  - OSI và TCP/IP cùng sử dụng kỹ thuật chuyển Packet.

- Khác nhau: 

|  | Mô hình OSI | Mô hình TCP/IP| 
|--------------|-------|------|
| Độ tin cậy phổ biến | Nhiều người cho rằng đây là mô hình cũ, chỉ để tham khảo, số người sử dụng hạn chế hơn so với TCP/IP | Được chuẩn hóa, nhiều người tin cậy và sử dụng phổ biến trên toàn cầu |
| Phương pháp tiếp cận | Tiếp cận theo chiều dọc | Tiếp cận theo chiều ngang | 
|Sự kết hợp giữa các tầng|Mỗi tầng khác nhau sẽ thực hiện một nhiệm vụ khác nhau, không có sự kết hợp giữa bất cứ tầng nào|Trong tầng ứng dụng có tầng trình diễn và tầng phiên được kết hợp với nhau|
|Thiết kế |Phát triển mô hình trước sau đó sẽ phát triển giao thức|	Các giao thức được thiết kế trước sau đó phát triển mô hình|
|Số lớp (tầng)|7|4|
|Truyền thông|Hỗ trợ cả kết nối định tuyến và không dây|Hỗ trợ truyền thông không kết nối từ tầng mạng|
|Tính phục thuộc|Giao thức độc lập|Phụ thuộc vào giao thức|


