
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
![Screenshot_1](https://user-images.githubusercontent.com/62273292/158309221-f8eb97a0-0d0f-4c70-aae2-f07773f8f173.png)

Giao thức HTTP là gì? HTTP còn là 1 giao thức Yêu cầu – Phản hồi dựa trên cấu trúc Client – Server. Client và Server giao tiếp với nhau bằng cách trao đổi các message độc lập (trái ngược với 1 luồng dữ liệu). Các message được gửi bởi client, thông thường là 1 trình duyệt web, được gọi là các yêu cầu và message được gửi bởi server như 1 sự trả lời, được gọi là phản hồi.

Các bạn có thể tìm hiểu thêm về các mã trạng thái HTTP – HTTP status code và hiểu rõ về danh sách các HTTP status code để biết rõ hơn về các Yêu cầu và Phản hồi tại đây nha.

## Kết nối của HTTP

1 kết nối được kiểm soát tại layer truyền tải, do đó về cơ bản nằm ngoài phạm vi của HTTP. Dù HTTP không yêu cầu giao thức truyền tải cơ bản phải dựa trên sự kết nối, vì chỉ yêu cầu nó đáng tin cậy hoặc không bị mất message (ít nhất là trình báo 1 lỗi). Trong số hai giao thức truyền tải phổ biến nhất trên Internet, TCP thì đáng tin cậy còn UDP thì không. HTTP do đó dựa vào tiêu chuẩn TCP vốn là connection-based (dựa trên sự kết nối).

![image](https://user-images.githubusercontent.com/62273292/158309790-b19c9f65-3f09-4744-96ff-2d81d97acc6f.png)

Trước khi 1 client và server có thể trao đổi 1 cặp yêu cầu – phản hồi HTTP, chúng phải thiết lập 1 kết nối TCP, 1 quá trình vốn yêu cầu 1 số vòng lặp. Hoạt động mặc định của HTTP/1.0 là mở 1 kết nối TCP riêng biệt cho từng cặp yêu cầu – phản hồi HTTP. Điều này làm nó kém hiệu quả hơn việc chia sẻ 1 kết nối TCP đơn lẻ khi nhiều yêu cầu được gửi liên tiếp.

Để giảm thiểu lỗ hỏng này, HTTP/1.1 đã giới thiệu pipelining (nhưng được chứng minh là khá khó để thực hiện) và kết nối liên tục: kết nối TCP bên dưới có thể được kiểm soát 1 phần bằng cách sử dụng tiêu đề Connection. HTTP/2 đã tiến 1 bước xa hơn bằng cách ghép các thông báo qua 1 kết nối duy nhất, giúp giữ cho kết nối ổn định và hiệu quả hơn.

Các thử nghiệm đang được tiến hành để thiết kế một giao thức truyền tải tốt hơn phù hợp hơn với HTTP. Ví dụ: Google đang thử nghiệm QUIC được xây dựng trên UDP để cung cấp giao thức truyền tải cũng đáng tin cậy và hiệu quả hơn.
