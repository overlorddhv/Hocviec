# Giao thức SMTP

## SMTP là gì?

SMTP là 3 chữ cái đầu viết tắt của Simple Mail Transfer Protocol dịch ra có nghĩa là giao thức truyền tải thư tín đơn giản hóa. Và giao thức này thực hiện nhiệm vụ chính là gửi mail còn việc nhận mail hay truy xuất dữ liệu mail server sẽ có giao thức IMAP hay POP3 đảm nhiệm.

SMTP Server (server dùng để gửi mail) là một dịch vụ cho phép gửi email với số lượng lớn, tốc độ nhanh mà không bị giới hạn như các hòm mail miễn phí của Gmail hoặc mail đi kèm hosting. Nói cách khác các máy chỉ chủ giúp bạn thao tác gửi thư người ta thường gọi là SMTP server chúng thực hiện gửi thư qua giao thức TCP hoặc IP.

Thường thì SMTP thực hiện để hoạt động qua cổng Internet 25 (TCP) nhưng tại châu âu có một phương thức thay thế cho SMTP của gmail được sử dụng rộng rãi gọi là X.400. Song Song với đó có nhiều máy chủ thư điện tử giờ đây đã hỗ trợ giao thức chuyển thư đơn giản mở rộng còn gọi là (ESMTP), giao thức này cho phép các tệp đa phương tiện được gửi dưới dạng e-mail.

Hệ thống mail hay đơn giản chỉ là một Email muốn chuyên nghiệp thì cần phải tìm hiểu về các giao thức mà nó sẽ hỗ trợ vì khi làm việc lâu dài nó sẽ giúp nâng cao hiệu suất công việc nhờ khả năng gửi nhận thư nhanh chóng, nhưng bạn cũng cần phải lưu ý là khả năng đính kèm tập tin và lưu trữ với dung lượng cao sẽ giúp bạn có thêm nhiều lợi thế trong việc sử dụng lâu dài, tiết kiệm thời gian chuyển đổi doanh nghiệp,…

Ngoài giao thức SMTP trong thư điện tử thì những giao thức khác cũng rất quan trọng như IMAP hay POP3 cgiúp bạn có một hệ thống gói email doanh nghiệp toàn diện nhất, chuyên nghiệp tính năng cao.


## Giao thức SMTP hoạt động như thế nào?

![image](https://user-images.githubusercontent.com/62273292/158330084-97449f51-c0f4-4e4b-b3f4-d8b677a09af5.png)

Việc gửi thông báo được thực hiện bắt đầu bằng việc chuyển thông báo đến một SMTP Server chỉ định. Dựa vào tên miền của địa chỉ e-mail nhận (ví dụ, ‘tenemail.com’), SMTP Server bắt đầu trao đổi liên lạc với một DNS Server mà sẽ tìm kiếm và trả về host name của SMTP Server đích (ví dụ ‘mail.ten-email.com’) cho tên miền đó. Sau cùng SMTP Server đầu tiên trao đổi thông tin trực tiếp với SMTP Server đích thông qua cổng 25 của TCP/IP.

Nếu tên người dùng của địa chỉ e-mail nhận trùng khớp với một trong những tài khoản người dùng được phép trong máy chủ đích. Thì thông báo e-mail gốc cuối cùng sẽ được đưa đến máy chủ này, rồi chỉ chờ người nhận lấy thông báo thông qua một chương trình gửi nhận mail như mail server Outlook chẳng hạn.

Trong trường hợp SMTP Server đầu tiên không thể liên lạc và trao đổi thông tin trực tiếp với máy chủ đích, thì giao thức SMTP có cung cấp các cơ chế để chuyển các thông báo thông qua một hay nhiều SMTP Server chuyển tiếp trung gian. Một máy chủ trung gian sẽ nhận thông báo gốc và sau đó sẽ gửi nó tới máy chủ đích hoặc cũng có thể gửi nó một lần nữa tới một máy chủ trung gian khác. Quá trình này sẽ được thao tác nhiều lần cho đến khi thông báo được chuyển đi hoặc thời gian lưu giữ thông báo hết hạ

