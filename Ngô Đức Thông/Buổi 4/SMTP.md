Bạn là chủ một doanh nghiệp nhưng không biết SMTP là gì? Đây là một vấn đề bạn cần lưu ý. Cùng tìm hiểu về máy chủ SMTP trong bài viết này.

Mỗi công ty đều có mỗi địa chỉ email riêng biệt giúp gửi tài liệu hoặc hợp đồng cho đối tác trong và ngoài nước. Để làm được điều ấy, tất cả doanh nghiệp đều phải thông qua hệ thống SMTP giúp gửi, nhận email đơn giản hơn. Vậy giao thức SMTP là gì? Có chức năng ra sao?

**1. Định nghĩa giao thức SMTP**

Simple Mail Transfer Protocol (viết tắt là SMTP) là hệ thống giao thức có nhiệm vụ nhận hay truyền tải dữ liệu trong email của người dùng. Hệ thống chỉ nhận và gửi thư điện tử email thông qua thiết bị có kết nối mạng Internet. Những thiết bị nhận và gửi email được gọi là máy chủ SMTP, mỗi máy chủ đều liên kết tới cổng mạng Internet 25 – cổng TCP.

Đã có nhiều khách hàng nói rằng không cần biết máy chủ SMTP là gì, sử dụng như thế nào vẫn có thể gửi, nhận email thì đúng vậy, người dùng không xài SMTP vẫn sử dụng email bình thường. Tuy nhiên, đối với những email có chứa file hay video dung lượng lớn thì khó gửi được hoặc có khi không cho phép gửi, người dùng cần SMTP giúp giảm thời gian chuyển dữ liệu và cấp quyền gửi dữ liệu dung lượng lớn.

![image](https://user-images.githubusercontent.com/65167293/157799843-f43e933d-b41d-42d8-8605-c8afda7fab20.png)

**2.  Hệ thống hoạt động của SMTP**

Khi doanh nghiệp gửi một email nào đó, hệ thống SMTP sẽ tự động dựa vào tên địa chỉ email đó và chuyển thông báo tới cho máy chủ SMTP. Sau khi SMTP server nhận được tín hiệu, tín hiệu sẽ được trao đổi giữa máy chủ SMTP và máy chủ DNS để tìm ra tên miền gốc tại Hostname trong máy chủ SMTP.

Sau các bước trên, máy chủ thực hiện bước kiểm tra liệu thông tin người dùng với thông tin email có trùng khớp hay không, nếu trùng khớp thì doanh nghiệp sẽ nhận hay gửi dữ liệu có dung lượng lớn thông qua email và nhận các thư điện tử bằng phần mềm.

Nhằm đề phòng trường hợp máy chủ SMTP và máy chủ DNS có thể không trao đổi với nhau, những tín hiệu không được phản hồi ấy sẽ gửi tới server trung gian. Server trung gian vẫn nhận được tín hiệu gốc và bắt đầu truyền qua nhiều máy chủ khác cho tới khi gửi tới Server gốc. Hệ thống phụ sẽ chạy hết công suất cùng thời gian tối đa trước khi tín hiệu bị thông báo là hết hạn và không sử dụng được nữa.

Hầu hết Email client (outlook, thunderbird, app trên điện thoại, webmail...) đều sử dụng giao thức SMTP để gửi và nhận thư.

![image](https://user-images.githubusercontent.com/65167293/157799927-2b594cbf-83e7-4642-b7fe-ddd8cdc0d121.png)

**3.  Thông tin khác về SMTP cho mọi doanh nghiệp**

Vào đầu năm 1980, giao thức SMTP bắt đầu được mọi doanh nghiệp sử dụng rộng rãi. Tuy nhiên vào thời gian đầu, hệ thống SMTP đơn giản chỉ là ứng dụng trong hệ thống UUCP (hệ thống sao chép dữ liệu của máy Unix sang máy Unix khác) giúp hệ thống này trao đổi thư từ điện tử dễ dàng hơn so với các thiết bị đương thời khác. Hiện nay, SMTP đã là một giao thức độc lập và hoạt động rất tốt nếu thiết bị gửi hoặc nhận email có kết nối Internet liên tục.

SMTP có thể xem là khái niệm hoàn hảo nhất gần giống với email. Tất cả những công việc của SMTP đều cần thông qua email và liên quan mật thiết tới email. Ngoài ra, giao thức SMTP bao gồm 25 cổng giao thức hệ thống TCP giúp truyền tải thư điện tử trên trang web đơn giản và hiệu quả.

![image](https://user-images.githubusercontent.com/65167293/157799972-627bd6d0-2672-4f2d-86d4-8ca3607f2167.png)
