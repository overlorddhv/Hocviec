**1. SMTP là gì?**

SMTP là viết tắt của Simple Mail Transfer Protocol – giao thức truyền tải thư tín đơn giản) là hệ thống giao thức có nhiệm vụ nhận, truyền tải dữ liệu trong email của người dùng. Hệ thống chỉ nhận và gửi thư điện tử email thông qua thiết bị có kết nối mạng Internet.

Hiện nay, các ứng dụng thư điện tử thường sử dụng SMTP chỉ để gửi thư điện tử được chuyển tiếp, gửi email đến đến máy chủ thư trên cổng 587 hoặc 465 theo RFC 8314.

Giao thức SMTP dùng nền văn bản (ASCII) và tương đối đơn giản. Trước khi gửi một thông điệp, bạn có thể định vị một hoặc nhiều địa chỉ nhận thông thiệp. Những địa chỉ này thường sẽ được kiểm tra về sự tồn tại của chúng. SMTP vốn dùng cổng 25 của giao thức TCP. SMTP sẽ xác định cấu trúc của các địa chỉ, yêu cầu tên miền và bất cứ điều gì liên quan đến email. SMTP cũng xác định các yêu cầu cho Post Office Protocol (POP) và truy cập Internet Message Protocol (IMAP) máy chủ, do đó email được gửi đúng cách.

Máy chủ SMTP (SMTP server) là máy chủ sử dụng phương thức SMTP để hỗ trợ người dùng gửi email của mình. Với SMTP server, email sau khi gửi sẽ được lưu trữ và được chuyển tiếp theo những địa chỉ mà người dùng mong muốn.

Máy chủ SMTP sẽ giúp người dùng có thể gửi email đến với một số lượng lớn người nhận mong muốn với chi phí thấp. Cùng với đó là khả năng đính kèm tập tin và lưu trữ với dung lượng cao. Khi gửi mail, người dùng sẽ được thông báo những trạng thái của từng mail để dễ dàng theo dõi, cập nhật. Sử dụng SMTP Server, những mail sau khi gửi sẽ ít có khả năng rơi vào hộp thư rác của người nhận.

SMTP Server hoạt động liên tục 24/24  để phục vụ cho việc cung cấp thông tin trực tuyến. Vị trí đặt máy chủ cũng vô cùng quan trọng nhằm đảm bảo sự toàn vẹn của dữ liệu, chất lượng và tốc độ lưu chuyển dữ liệu từ Server đến máy tính gửi/nhận thư.

**2. Hệ thống hoạt động của SMTP**

Khi gửi một email nào đó, hệ thống SMTP sẽ tự động dựa vào tên địa chỉ email đó và chuyển thông báo tới cho máy chủ SMTP. Sau khi SMTP server nhận được tín hiệu, tín hiệu sẽ được trao đổi giữa máy chủ SMTP và máy chủ DNS để tìm ra tên miền gốc trong máy chủ SMTP.

Sau những bước trên, máy chủ thực hiện bước kiểm tra liệu thông tin người dùng với thông tin email có trùng khớp hay không. Nếu trùng khớp thì doanh nghiệp sẽ nhận hay gửi dữ liệu có dung lượng lớn thông qua email và nhận các thư điện tử bằng phần mềm.

Để đề phòng trường hợp máy chủ SMTP và máy chủ DNS có thể không trao đổi với nhau thì những tín hiệu không được phản hồi ấy sẽ gửi tới server trung gian. Server trung gian vẫn nhận được tín hiệu gốc và bắt đầu truyền qua nhiều máy chủ khác nhau cho tới khi gửi tới Server gốc. Hệ thống phụ sẽ chạy hết công suất cùng thời gian tối đa trước khi tín hiệu bị thông báo là hết hạn và không sử dụng được nữa.

Hiện nay, các email client như outlook, thunderbird, webmail đều sử dụng giao thức SMTP để nhận thư (nó thường được gọi là: SMTP gmail)

**3. Gửi email bằng SMTP**

![image](https://user-images.githubusercontent.com/48250210/158012737-43917427-f0cd-4afc-8d0d-104f8f6fc86d.png)

SMTP cung cấp bộ mã đơn giản hóa việc truyền thông điệp giữa các máy chủ email. SMTP sẽ cung cấp các mã đó và phần mềm máy chủ của email được thiết kế để hiểu nghĩa của chúng. Mỗi thông điệp khi chuyển đến đích thường sẽ đi qua một số máy tính. Như vậy, nó được lưu trữ trong một khoảng thời gian ngắn trước khi nó chuyển sang máy tính tiếp theo trong đường dẫn.

Bạn có thể thiết lập máy chủ SMTP hoặc có thể kết nối ứng dụng email của mình với một trong các nhà cung cấp máy chủ SMTP  và cấp quyền gửi email trực tiếp.

Nhiều người cho rằng việc thiết lập máy chủ SMTP riêng của mình để tiết kiệm chi phí. Tuy nhiên, mỗi máy chủ chuyển tiếp SMTP sẽ có một số giới hạn về số lượng email mà nó có thể phân phối trên nhiều ISP khác nhau. Nếu bạn viết mã để gửi hàng triệu email, thì các ISP đôi khi sẽ bắt đầu chặn những email này vì chúng là thư rác vì một lượng lớn email được gửi bởi một người gửi cùng một lúc.

**4. SMTP Server là gì? Có giống một máy chủ bình thường?**

Một máy chủ SMTP sẽ có một địa chỉ (hoặc nhiều địa chỉ) có thể được thiết lập bởi các mail client hoặc ứng dụng mà bạn đang sử dụng. Và thường được định dạng như smtp.serveraddress.com. (Ví dụ, địa chỉ máy chủ SMTP của Gmail là smtp.gmail.com. Của Twilio SendGrid là smtp.sendgrid.com. Hay của Amazon SES là amazonses.com) .

Về mặt kỹ thuật thì SMTP server giống như các máy chủ thông thường khác. Điểm khác ở đây là khả năng gửi email số lượng lớn không giới hạn.

Ví dụ, Gmail là máy chủ gửi email miễn phí của Google. Nhưng đặt ra hạn chế là bạn chỉ gửi được tối đa 500 email/ngày. Không được phép gửi nhiều hơn. Ngoài ra, Gmail phục vụ mục đích liên quan đến công việc, cá nhân, các thông tin liên lạc, giao dịch…. Không sử dụng cho mục đích gửi quảng cáo, tiếp thị, marketing.

Còn với SMTP server nó là các máy chủ chuyên dụng để gửi email số lượng lớn. Với mục đích gửi thông tin quảng cáo, marketing hoặc chăm sóc khách hàng. Và bạn sẽ cần trả phí gửi cho các smtp server này.

Ngoài ra, một máy chủ SMTP đóng nhiệm vụ quan trọng trong việc xác thực email gửi đi có phải là tài khoản đang hoạt động không. Đây là vai trò đầu tiên trong việc bảo vệ hộp thư đến của bạn từ email bất hợp pháp. Nó cũng sẽ gửi email trở lại người gửi nếu nó không thể được chuyển thành công. Điều này thông báo cho người gửi rằng họ có địa chỉ email không đúng hoặc email của họ đang bị chặn bởi máy chủ nhận.
