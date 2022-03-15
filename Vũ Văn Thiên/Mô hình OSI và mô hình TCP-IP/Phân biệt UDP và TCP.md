## UDP và TCP là hai giao thức truyền dẫn qua internet phổ biến nhất hiện nay. Vậy sự khác nhau giữa UDP và TCP là gì?

## Phân biệt UDP và TCP

Như chúng ta biết rằng, cả TCP (Transmission Control Protocol) và UDP (User Datagram Protocol) là những giao thức Internet được sử dụng rộng rãi nhất.
Trong đó, TCP là giao thức định hướng kết nối. Tức là, một khi kết nối được thiết lập, dữ liệu có thể được gửi theo hai chiều. Trong khi đó, UDP là một giao thức Internet không kết nối đơn giản hơn. Nhiều tin nhắn được gửi dưới dạng packet in chunks sử dụng UDP. Trên cơ sở các đặc điểm, thuộc tính của hai giao thức, chúng ta có thể phân biệt giữa UDP và TCP.

![image](https://user-images.githubusercontent.com/62273292/158342231-9cab12a9-be07-4841-8940-e0ecad6f2387.png)

Sau đây, là những điểm khác biệt quan trọng giữa UDP và TCP

|Đặc điểm| TCP (Transmission Control Protocol)|UDP (User Datagram Protocol)|
|---------|-----------|------------------------|
|Định nghĩa|Là một giao thức truyền thông tin, sử dụng dữ liệu được truyền giữa các hệ thống qua mạng. Trong đó, dữ liệu được truyền dưới dạng packet.Nó bao gồm kiểm tra lỗi, đảm bảo việc phân phối và duy trì thứ tự của các packet|Giống với giao thức TCP. Nhưng không đảm bảo việc kiểm tra lỗi và khôi phục dữ liệu. Nếu bạn sử dụng giao thức này, dữ liệu sẽ được gửi liên tục, không phân biệt vấn đề ở đầu nhận.|
|Thiết kế|TCP là một giao thức định hướng kết nối (connection oriented).|UDP là một giao thức ít kết nối hơn (connectionless).|
|	Độ tin cậy|Vì TCP cung cấp hỗ trợ kiểm tra lỗi và cũng đảm bảo cung cấp dữ liệu đến đích. Điều này làm cho nó đáng tin cậy hơn so với UDP.|Mặt khác, UDP chỉ cung cấp hỗ trợ kiểm tra lỗi cơ bản bằng cách sử dụng checksum. Vì vậy việc phân phối dữ liệu đến đích không thể được đảm bảo trong UDP so với TCP.|
|Truyền dữ liệu|Trong TCP, dữ liệu được truyền theo một trình tự cụ thể. Có nghĩa là các packet đến người nhận theo thứ tự.|Trong UDP không có trình tự dữ liệu. Để thực hiện việc sắp xếp thứ tự nó phải được quản lý bởi lớp ứng dụng.|
|Hiệu năng|TCP chậm hơn và kém hiệu quả hơn về hiệu suất so với UDP. Ngoài ra TCP cũng nặng hơn so với UDP.|UDP nhanh hơn và hiệu quả hơn TCP.|
|Truyền lại|Có thể truyền lại packet trong TCP trong trường hợp gói bị mất hoặc cần gửi lại.|	Không thể truyền lại các packet trong UDP.|

## kết luận

Cả TCP và UDP đều có những ưu điểm và nhược điểm. UDP nhanh hơn, đơn giản và hiệu quả hơn và do đó thường được sử dụng để gửi các tệp âm thanh, video và TCP, mặt khác, mạnh mẽ, đáng tin cậy và đảm bảo phân phối các gói theo cùng một thứ tự.
Do đó, chúng tôi kết luận rằng cả TCP và UDP đều cần thiết cho việc truyền dữ liệu


