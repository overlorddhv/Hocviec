**1. Giao thức POP**

Giao thức POP là viết tắt của Post Office Protocol. Như chúng ta biết rằng SMTP được sử dụng như một tác nhân truyền thông điệp. Khi tin nhắn được gửi đi, SMPT được sử dụng để gửi tin nhắn từ máy khách đến máy chủ và sau đó đến máy chủ người nhận. Nhưng thông báo được gửi từ máy chủ người nhận đến máy chủ thực tế với sự trợ giúp của Tác nhân truy cập thông báo. Tác nhân truy cập thông báo chứa hai loại giao thức, tức là, POP3 và IMAP.

**2. Thư được truyền đi như thế nào?**

![image](https://user-images.githubusercontent.com/65167293/157800139-7dc5fb97-a81e-4a8f-9584-e0faa572f647.png)

Giả sử người gửi muốn gửi thư cho người nhận. Thư đầu tiên được truyền đến máy chủ thư của người gửi. Sau đó, thư được truyền từ máy chủ thư của người gửi đến máy chủ thư của người nhận qua internet. Khi nhận thư tại máy chủ thư của người nhận, thư sau đó sẽ được gửi đến người dùng. Toàn bộ quá trình được thực hiện với sự trợ giúp của các giao thức Email. Việc truyền thư từ người gửi đến máy chủ thư của người gửi và sau đó đến máy chủ thư của người nhận được thực hiện với sự trợ giúp của giao thức SMTP. Tại máy chủ thư của người nhận, giao thức POP hoặc IMAP lấy dữ liệu và truyền đến người dùng thực tế.

Vì SMTP là một giao thức đẩy nên nó sẽ đẩy thông điệp từ máy khách đến máy chủ. Như chúng ta có thể quan sát trong hình trên rằng SMTP đẩy thư từ máy khách đến máy chủ thư của người nhận. Giai đoạn thứ ba của giao tiếp email yêu cầu một giao thức kéo và POP là một giao thức kéo. Khi thư được truyền từ máy chủ thư của người nhận đến máy khách có nghĩa là máy khách đang kéo thư từ máy chủ.

**3. POP3 là gì?**

POP3 là một giao thức đơn giản và có chức năng rất hạn chế. Trong trường hợp của giao thức POP3, máy khách POP3 được cài đặt trên hệ thống người nhận trong khi máy chủ POP3 được cài đặt trên máy chủ thư của người nhận.

**4. Lịch sử của giao thức POP3**

Phiên bản đầu tiên của giao thức bưu điện được giới thiệu lần đầu tiên vào năm 1984 với tên gọi RFC 918 trên Internet

lực lượng công binh. Các nhà phát triển đã phát triển một giao thức email đơn giản và hiệu quả được gọi là giao thức POP3, được sử dụng để truy xuất email từ máy chủ. Điều này cung cấp cơ sở để truy cập thư ngoại tuyến thay vì truy cập hộp thư ngoại tuyến.

Năm 1985, giao thức bưu điện phiên bản 2 được giới thiệu trong RFC 937, nhưng nó đã được thay thế bằng giao thức bưu điện phiên bản 3 vào năm 1988 với việc xuất bản RFC 1081. Sau đó, POP3 đã được sửa đổi trong 10 năm tiếp theo trước khi nó được xuất bản. Sau khi được hoàn thiện, nó được xuất bản vào năm 1996.

Mặc dù giao thức POP3 đã trải qua nhiều cải tiến khác nhau, các nhà phát triển vẫn duy trì một nguyên tắc cơ bản rằng nó tuân theo quy trình ba giai đoạn tại thời điểm truy xuất thư giữa máy khách và máy chủ. Họ đã cố gắng làm cho giao thức này rất đơn giản, và sự đơn giản này làm cho giao thức này trở nên rất phổ biến ngày nay.

Hãy hiểu hoạt động của giao thức POP3 qua sơ đồ sau:

![image](https://user-images.githubusercontent.com/65167293/157800232-1522e7cb-8561-4fcb-9b58-698bf3a11316.png)

Để thiết lập kết nối giữa máy chủ POP3 và máy khách POP3, máy chủ POP3 yêu cầu tên người dùng cho máy khách POP3. Nếu tên người dùng được tìm thấy trong máy chủ POP3, thì nó sẽ gửi thông báo ok. Sau đó, nó yêu cầu mật khẩu từ máy khách POP3; sau đó máy khách POP3 gửi mật khẩu đến máy chủ POP3. Nếu mật khẩu được khớp, thì máy chủ POP3 sẽ gửi thông báo OK và kết nối được thiết lập. Sau khi thiết lập kết nối, khách hàng có thể xem danh sách các thư trên máy chủ thư POP3. Trong danh sách các thư, người dùng sẽ nhận được số lượng và kích thước email từ máy chủ. Ngoài danh sách này, người dùng có thể bắt đầu truy xuất thư.

Sau khi máy khách truy xuất tất cả các email từ máy chủ, tất cả các email từ máy chủ sẽ bị xóa. Do đó, chúng ta có thể nói rằng các email được giới hạn cho một máy cụ thể, vì vậy sẽ không thể truy cập vào các email giống nhau trên một máy khác. Tình trạng này có thể được khắc phục bằng cách định cấu hình cài đặt email để để lại một bản sao của thư trên máy chủ thư.

**5. Ưu nhược điểm của giao thức POP3**

***Sau đây là những ưu điểm của giao thức POP3:***

- Nó cho phép người dùng đọc email ngoại tuyến. Nó chỉ yêu cầu kết nối internet tại thời điểm tải email từ máy chủ. Sau khi các thư được tải xuống từ máy chủ, tất cả các thư đã tải xuống sẽ nằm trên PC hoặc đĩa cứng của máy tính của chúng tôi, có thể được truy cập mà không cần internet. Do đó, chúng ta có thể nói rằng giao thức POP3 không yêu cầu kết nối internet vĩnh viễn.
- Nó cung cấp khả năng truy cập dễ dàng và nhanh chóng vào các email vì chúng đã được lưu trữ trên PC của chúng tôi.
- Không có giới hạn về kích thước của email mà chúng tôi nhận hoặc gửi.
- Nó yêu cầu ít không gian lưu trữ máy chủ hơn vì tất cả các thư được lưu trữ trên máy cục bộ.
- Có kích thước tối đa trên hộp thư, nhưng nó bị giới hạn bởi kích thước của đĩa cứng.
- Nó là một giao thức đơn giản nên nó là một trong những giao thức phổ biến nhất được sử dụng hiện nay.
- Nó rất dễ dàng để cấu hình và sử dụng.


***Nhược điểm của giao thức POP3***

Sau đây là những ưu điểm của giao thức POP3:

Nếu các email được tải xuống từ máy chủ, thì tất cả các email sẽ bị xóa khỏi máy chủ theo mặc định. Vì vậy, không thể truy cập thư từ các máy khác trừ khi chúng được cấu hình để để lại bản sao của thư trên máy chủ.

Chuyển thư mục thư từ máy cục bộ sang máy khác có thể khó khăn.

Vì tất cả các tệp đính kèm được lưu trữ trên máy cục bộ của bạn, nên có nhiều nguy cơ bị vi-rút tấn công nếu trình quét vi-rút không quét chúng. Cuộc tấn công của virus có thể gây hại cho máy tính.

Thư mục email được tải xuống từ máy chủ thư cũng có thể bị hỏng.

Các thư được lưu trữ trên máy cục bộ, vì vậy bất kỳ ai ngồi trên máy của bạn đều có thể truy cập vào thư mục email.
