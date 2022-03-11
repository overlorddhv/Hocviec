**1. Giao thức IMAP**

IMAP là viết tắt của Internet Message Access Protocol . Nó là một giao thức lớp ứng dụng được sử dụng để nhận email từ máy chủ thư. Đây là giao thức được sử dụng phổ biến nhất như POP3 để lấy email.

Nó cũng tuân theo mô hình máy khách / máy chủ. Ở một phía, chúng tôi có một ứng dụng khách IMAP, là một quy trình chạy trên máy tính. Ở phía bên kia, chúng tôi có một máy chủ IMAP, cũng là một quá trình chạy trên một máy tính khác. Cả hai máy tính được kết nối thông qua một mạng.

![image](https://user-images.githubusercontent.com/65167293/157800739-55fe255c-ba3e-48ef-8133-9b4b6c7c954b.png)

Giao thức IMAP nằm trên lớp truyền tảiTCP / IP có nghĩa là nó sử dụng ngầm định độ tin cậy của giao thức. Khi kết nối TCP được thiết lập giữa máy khách IMAP và máy chủ IMAP, máy chủ IMAP sẽ lắng nghe cổng 143 theo mặc định, nhưng số cổng này cũng có thể được thay đổi.

Theo mặc định, có hai cổng được IMAP sử dụng:

- Cổng 143: Đây là một cổng IMAP không được mã hóa.
- Cổng 993: Cổng này được sử dụng khi ứng dụng khách IMAP muốn kết nối qua IMAP một cách an toàn.
**2.  Tại sao chúng ta nên sử dụng IMAP thay vì giao thức POP3?**

POP3 đang trở thành giao thức phổ biến nhất để truy cập hộp thư TCP / IP. Nó thực hiện mô hình truy cập thư ngoại tuyến, có nghĩa là các thư được truy xuất từ ​​máy chủ thư trên máy cục bộ, sau đó bị xóa khỏi máy chủ thư. Ngày nay, hàng triệu người dùng sử dụng giao thức POP3 để truy cập các thư đến. Do mô hình truy cập thư ngoại tuyến, nó không thể được sử dụng nhiều. Mô hình trực tuyến mà chúng tôi muốn trong thế giới lý tưởng. Trong mô hình trực tuyến, chúng ta cần phải luôn kết nối với internet. Vấn đề lớn nhất với việc truy cập ngoại tuyến bằng POP3 là các thư bị xóa vĩnh viễn khỏi máy chủ, vì vậy nhiều máy tính không thể truy cập vào thư. Giải pháp cho vấn đề này là lưu trữ các thư tại máy chủ từ xa thay vì trên máy chủ cục bộ. POP3 cũng phải đối mặt với một vấn đề khác, đó là bảo mật và an toàn dữ liệu. Giải pháp cho vấn đề này là sử dụng mô hình truy cập ngắt kết nối, mô hình này cung cấp các lợi ích của cả truy cập trực tuyến và ngoại tuyến. Trong mô hình truy cập ngắt kết nối, người dùng có thể lấy thư để sử dụng cục bộ như trong giao thức POP3 và người dùng không cần phải kết nối internet liên tục. Tuy nhiên, những thay đổi được thực hiện đối với hộp thư được đồng bộ hóa giữa máy khách và máy chủ. Thư vẫn còn trên máy chủ để các ứng dụng khác nhau trong tương lai có thể truy cập. Khi các nhà phát triển nhận ra những lợi ích này, họ đã thực hiện một số nỗ lực để triển khai mô hình truy cập không kết nối. Điều này được thực hiện bằng cách sử dụng các lệnh POP3 cung cấp tùy chọn để lại các thư trên máy chủ. Điều này có hiệu quả, nhưng chỉ ở một mức độ hạn chế, chẳng hạn, việc theo dõi thư nào mới hay cũ sẽ trở thành một vấn đề khi cả hai đều được truy xuất và để lại trên máy chủ. Vì vậy, POP3 thiếu một số tính năng cần thiết cho mô hình truy cập bị ngắt kết nối thích hợp. Khi các nhà phát triển nhận ra những lợi ích này, họ đã thực hiện một số nỗ lực để triển khai mô hình truy cập không kết nối. Điều này được thực hiện bằng cách sử dụng các lệnh POP3 cung cấp tùy chọn để lại các thư trên máy chủ. Điều này có hiệu quả, nhưng chỉ ở một mức độ hạn chế, chẳng hạn, việc theo dõi thư nào mới hay cũ sẽ trở thành một vấn đề khi cả hai đều được truy xuất và để lại trên máy chủ. Vì vậy, POP3 thiếu một số tính năng cần thiết cho mô hình truy cập bị ngắt kết nối thích hợp. Khi các nhà phát triển nhận ra những lợi ích này, họ đã thực hiện một số nỗ lực để triển khai mô hình truy cập không kết nối. Điều này được thực hiện bằng cách sử dụng các lệnh POP3 cung cấp tùy chọn để lại các thư trên máy chủ. Điều này có hiệu quả, nhưng chỉ ở một mức độ hạn chế, chẳng hạn, việc theo dõi thư nào mới hay cũ sẽ trở thành một vấn đề khi cả hai đều được truy xuất và để lại trên máy chủ. Vì vậy, POP3 thiếu một số tính năng cần thiết cho mô hình truy cập bị ngắt kết nối thích hợp.

Vào giữa những năm 1980, sự phát triển bắt đầu tại Đại học Stanford trên một giao thức mới cung cấp một cách thức có khả năng hơn để truy cập vào hộp thư của người dùng. Kết quả là sự phát triển của giao thức truy cập thư tương tác, sau này được đổi tên thành Giao thức truy cập thư qua Internet .

**3.  Lịch sử và tiêu chuẩn IMAP**

Phiên bản đầu tiên của IMAP được chính thức ghi nhận như một tiêu chuẩn internet là IMAP phiên bản 2, và trong RFC 1064, và được xuất bản vào tháng 7 năm 1988. Nó được cập nhật trong RFC 1176, tháng 8 năm 1990, vẫn giữ nguyên phiên bản cũ. Vì vậy, họ đã tạo ra một tài liệu mới của phiên bản 3 được gọi là IMAP3. Trong RFC 1203, được xuất bản vào tháng 2 năm 1991. Tuy nhiên, IMAP3 không bao giờ được thị trường chấp nhận, vì vậy mọi người tiếp tục sử dụng IMAP2. Phần mở rộng cho giao thức sau đó được tạo ra có tên là IMAPbis, bổ sung hỗ trợ cho Phần mở rộng Thư Internet Đa năng (MIME) cho IMAP. Đây là một sự phát triển rất quan trọng do tính hữu ích của MIME. Mặc dù vậy, IMAPbis chưa bao giờ được xuất bản dưới dạng RFC. Điều này có thể do các sự cố liên quan đến IMAP3. Vào tháng 12 năm 1994, IMAP phiên bản 4, tức là IMAP4 được xuất bản trong hai RFC, tức là, RFC 1730 mô tả giao thức chính và RFC 1731 mô tả cơ chế xác thực cho IMAP 4. IMAP 4 là phiên bản hiện tại của IMAP, được sử dụng rộng rãi ngày nay. Nó tiếp tục được cải tiến và phiên bản mới nhất của nó thực sự được gọi là IMAP4rev1 và được định nghĩa trong RFC 2060. Nó được cập nhật gần đây nhất trong RFC 3501.

**4.  Tính năng IMAP**

IMAP được thiết kế cho một mục đích cụ thể cung cấp một cách linh hoạt hơn về cách người dùng truy cập hộp thư. Nó có thể hoạt động ở bất kỳ chế độ nào trong ba chế độ, tức là chế độ trực tuyến, ngoại tuyến và ngắt kết nối. Trong số này, các chế độ ngoại tuyến và ngắt kết nối được hầu hết người dùng giao thức quan tâm.

***Sau đây là các tính năng của giao thức IMAP:***

- Truy cập và lấy thư từ máy chủ từ xa: Người dùng có thể truy cập thư từ máy chủ từ xa trong khi vẫn giữ lại các thư trong máy chủ từ xa.
- Đặt cờ thông báo: Cờ thông báo được đặt để người dùng có thể theo dõi thông báo mà họ đã xem.
- Quản lý nhiều hộp thư: Người dùng có thể quản lý nhiều hộp thư và chuyển thư từ hộp thư này sang hộp thư khác. Người dùng có thể sắp xếp chúng thành các danh mục khác nhau cho những người đang làm việc trong các dự án khác nhau.
- Xác định thông tin trước khi tải xuống: Nó quyết định có truy xuất hay không trước khi tải thư từ máy chủ thư.
- Tải xuống một phần của tin nhắn: Nó cho phép bạn tải xuống một phần của tin nhắn, chẳng hạn như một phần nội dung từ phần kịch câm. Điều này có thể hữu ích khi có các tệp đa phương tiện lớn trong phần tử văn bản ngắn của tin nhắn.
- Sắp xếp thư trên máy chủ: Trong trường hợp POP3, người dùng không được phép quản lý thư trên máy chủ. Mặt khác, người dùng có thể sắp xếp các thư trên máy chủ theo yêu cầu của họ như họ có thể tạo, xóa hoặc đổi tên hộp thư trên máy chủ.
- Tìm kiếm: Người dùng có thể tìm kiếm nội dung của email.
- Kiểm tra tiêu đề email: Người dùng cũng có thể kiểm tra tiêu đề email trước khi tải xuống.
- Tạo hệ thống phân cấp: Người dùng cũng có thể tạo các thư mục để sắp xếp các thư theo một hệ thống phân cấp.
**


1. **Hoạt động chung của IMAP**

![image](https://user-images.githubusercontent.com/65167293/157800812-a353389c-75c0-4002-aed3-5eb5a651407f.png)

- IMAP là một giao thức khách-máy chủ giống như POP3 và hầu hết các giao thức ứng dụng TCP / IP khác. Giao thức IMAP4 chỉ hoạt động khi IMAP4 phải nằm trên máy chủ nơi đặt các hộp thư của người dùng. Trong c POP3 không nhất thiết phải yêu cầu cùng một máy chủ vật lý cung cấp các dịch vụ SMTP. Do đó, trong trường hợp của giao thức IMAP, hộp thư phải có thể truy cập được đối với cả SMTP cho các thư đến và IMAP để truy xuất và sửa đổi.
- IMAP sử dụng Giao thức điều khiển truyền (TCP) để liên lạc nhằm đảm bảo việc phân phối dữ liệu và cũng được nhận theo đơn đặt hàng.
- IMAP4 lắng nghe trên một cổng nổi tiếng, tức là cổng số 143, đối với một yêu cầu kết nối đến từ máy khách IMAP4.

Chúng ta hãy hiểu giao thức IMAP qua một ví dụ đơn giản.

![image](https://user-images.githubusercontent.com/65167293/157800831-afd0a9b0-cdde-493c-8a83-9f111c1db3b2.png)

Giao thức IMAP đồng bộ hóa tất cả các thiết bị với máy chủ chính. Giả sử chúng ta có ba thiết bị máy tính để bàn, điện thoại di động và máy tính xách tay như trong hình trên. Nếu tất cả các thiết bị này đang truy cập vào cùng một hộp thư, thì nó sẽ được đồng bộ hóa với tất cả các thiết bị. Ở đây, đồng bộ hóa có nghĩa là khi thư được mở bởi một thiết bị, thì nó sẽ được đánh dấu là đã mở trên tất cả các thiết bị khác, nếu chúng ta xóa thư, thì thư cũng sẽ bị xóa khỏi tất cả các thiết bị khác. Vì vậy, chúng tôi có đồng bộ hóa giữa tất cả các thiết bị. Trong IMAP, chúng tôi có thể thấy tất cả các thư mục như thư rác, hộp thư đến, đã gửi, v.v. Chúng tôi cũng có thể tạo thư mục của riêng mình được gọi là thư mục tùy chỉnh sẽ hiển thị trong tất cả các thiết bị khác.

