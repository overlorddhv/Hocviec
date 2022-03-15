# Giao thức POP

## POP là gì?

Post Office Protocol (POP) là giao thức tiêu chuẩn được sử dụng bởi các mail client để truy xuất email từ xa từ mail server qua kết nối TCP/IP. Kể từ khi phiên bản đầu tiên được tạo ra vào năm 1984, Post Office Protocol (hiện tại là Phiên bản 3) đã trở thành một trong những giao thức phổ biến nhất và được sử dụng bởi hầu hết mọi ứng dụng email cho đến nay. Sự phổ biến của nó là có lý do: sự đơn giản trong việc cấu hình, vận hành và bảo trì.

Định kỳ, những người đăng ký sẽ sử dụng ứng dụng email để kiểm tra hộp thư của họ trên máy chủ từ xa và tải xuống bất kỳ email nào được gửi đến họ.

Khi ứng dụng email đã tải xuống các mail, chúng thường bị xóa khỏi máy chủ. Tuy nhiên vẫn có một số ứng dụng email cho phép người dùng chỉ định các thư được sao chép hoặc lưu trên máy chủ trong một khoảng thời gian nhất định.

Các ứng dụng email thường sử dụng port 110 TCP để kết nối với máy chủ POP3. Nếu giao tiếp được mã hóa được hỗ trợ trên máy chủ POP3, người dùng có thể tùy chọn kết nối bằng cách sử dụng STLS, hoặc POP3S sử dụng Transport Layer Security (TLS) hoặc Secure Sockets Layer (SSL) trên TCP port 995 để kết nối với máy chủ).

## Lịch sử của Post Office Protocol

Phiên bản đầu tiên của Post Office Protocol được xuất bản lần đầu trong Request for Comments in 1984 với tên RFC 918 của IETF (Internet Engineering Task Force). Trước đó, các nhà phát triển nhận ra sự cần thiết phải thiết kế một phương pháp lấy email đơn giản và hiệu quả từ máy chủ. Họ thấy được các lợi thế của việc đọc email ngoại tuyến thay vì truy cập hộp thư trực tuyến.

Năm 1985, Post Office Protocol phiên bản 2 xuất bản trong RFC 937, được thay thế bằng Phiên bản 3 vào năm 1988 với ấn phẩm RFC 1081. POP3 đã được sửa đổi nhiều lần trong 10 năm tiếp theo, trước khi nó được tinh chỉnh để đạt được thông số kỹ thuật như hiện hành (xuất bản năm 1996 - RFC 1939).

Mặc dù POP3 đã trải qua khá nhiều cải tiến, nhưng các nhà phát triển vẫn duy trì nguyên tắc cơ bản của giao thức có ba giai đoạn trong quá trình truy xuất thư giữa client và server. Sự đơn giản là điều khiến POP3 trở thành một trong những phương thức lấy thư phổ biến nhất được sử dụng hiện nay.

## Cách thức hoạt động của Post Office Protocol

Khi người dùng kiểm tra email mới, client sẽ kết nối với máy chủ POP3. Sau đó, ứng dụng email sẽ cung cấp tên người dùng và mật khẩu của mình cho máy chủ để xác thực. Sau khi kết nối, client đưa ra một loạt các lệnh dựa trên văn bản để truy xuất tất cả các email. Sau đó, nó lưu trữ các thưđã tải xuống này trên hệ thống cục bộ của người dùng, xóa các bản sao trên máy chủ và ngắt kết nối khỏi máy chủ.

Theo mặc định, các mail trên server sẽ bị xóa sau khi chúng được lấy xong. Do đó, các email luôn gắn liền với một máy cụ thể đó, không thể truy cập các email đó từ một ứng dụng email trên máy khác. Người dùng có thể khắc phục vấn đề này bằng cách cấu hình cài đặt ứng dụng email để lại một bản sao của các email trên máy chủ.

POP giải phóng không gian mailbox trên máy chủ vì email và tệp đính kèm được tải xuống và xóa ở server bất cứ khi nào mail client kiểm tra thư mới. Email ngoại tuyến được lưu trữ trong máy tính của người dùng không có giới hạn kích thước hộp thư, ngoại trừ dung lượng lưu trữ ổ cứng của PC. Một nhược điểm của tài khoản thư POP3 là người dùng khó truy xuất thư nếu họ quyết định chuyển đổi chương trình email hoặc hệ thống máy tính.

## Ưu điểm của POP3

- Email được tải xuống máy tính người dùng do đó có thể được đọc khi người dùng ngoại tuyến.

- Mở tệp đính kèm rất nhanh chóng và dễ dàng vì chúng đã được tải xuống.

- Cần ít không gian lưu trữ trên máy chủ bởi tất cả các email được lưu trữ trên máy cục bộ.

- Dung lượng lưu trữ của email bị giới hạn bởi kích thước của đĩa cứng của bạn.

- Rất phổ biến, dễ cấu hình và sử dụng.

## Nhược điểm của POP3

- Email không thể được truy cập từ các máy khác (trừ khi được cấu hình để làm như vậy).

- Khó khăn trong việc xuất folder lưu trữ mail cục bộ sang mail client hoặc máy vật lý khác.

- Thư mục email có thể bị hỏng, có khả năng mất toàn bộ hộp thư cùng một lúc.

- Tệp đính kèm email có thể chứa vi-rút , khiến người dùng PC bị tổn hại nếu trình quét vi-rút không thể phát hiện ra.

## So sánh POP và IMAP

IMAP có các đặc điểm sau:

- Kết nối đến server.

- Lấy nội dung được yêu cầu từ người dùng và lưu đệm cục bộ.

- Xử lý các biên tập từ người dùng, ví dụ như đánh dấu email là mail để đọc hay xóa…

- Ngắt kết nối.

Như ta thấy, thủ tục làm việc của IMAP phức tạp hơn một chút so với POP. Về cơ bản, cấu trúc thư mục và email được lưu trên server và chỉ có bản sao được lưu cục bộ, tức chúng được lưu tạm. Tuy nhiên, người dùng cũng có thể lưu lại cố định mail.

Rõ ràng là, còn tùy thuộc vào nhu cầu người dùng để quyết định đâu là giao thức mail phù hợp nhất. 

**Chọn POP nếu:*

- Bạn muốn truy cập mail chỉ từ một thiết bị.

- Bạn cần truy cập email thường xuyên dù có kết nối Internet hay không.

- Không gian lưu trữ trên server hạn chế.

**Chọn IMAP nếu:**

- Bạn muốn truy cập email từ nhiều thiết bị khác nhau.

- Bạn có một kết nối Internet thường xuyên và tin cậy.

- Bạn muốn xem nhanh các email mới hoặc những email trên server.

- Không gian lưu trữ cục bộ hạn chế.

- Bạn lo lắng về vấn đề dự phòng dữ liệu.

IMAP là giao thức hiện đại hơn, mang lại tính linh hoạt. Và email người dùng cũng tự động được lưu dự phòng trên server trong khi không gian lưu trữ khả dụng của server thường không còn là vấn đề hiện nay và bạn vẫn có thể lưu cục bộ những email quan trọng.

## Kết Luận

Mặc dù POP3 đã xuất hiện từ những năm 1980, nhưng nó vẫn là một trong những giao thức email phổ biến. Bằng cách lưu trữ thư trên máy tính client, nó cho phép người dùng đọc thư ngoại tuyến và không có giới hạn kích thước trên dung lượng lưu trữ của máy chủ. Tuy nhiên, người dùng cần phải cẩn thận với vi-rút trong tệp đính kèm vì chúng có thể gây ra mối đe dọa bảo mật cho máy khách.
