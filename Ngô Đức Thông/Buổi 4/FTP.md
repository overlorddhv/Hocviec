Thuật ngữ FTP rất ít người nghe đến, nhưng với những cá nhân làm website thì khái niệm FTP đã quá quen thuộc. Bởi FPT rất quan trọng trong việc quản lý các tập tin lên host và nhiều tính năng khác. Vậy bản chất của FTP là gì? Chúng ta cùng tìm hiểu điều này trong bài viết dưới đây nhé!
 # **FTP là gì?**
FTP viết tắt từ File Transfer Protocol, là một giao thức truyền tải tập tin từ máy tính này đến máy tính khác thông qua một mạng TCP hoặc qua mạng Internet. Nhờ vào giao thức này nên người sử dụng có thể tải dữ liệu như hình ảnh, văn bản, các tập tin nhạc, video... từ máy tính của mình lên máy chủ đang đặt ở một nơi khác hoặc tải các tập tin đã có trên máy chủ về máy tính cá nhân của mình một cách dễ dàng. FTP cũng là giao thức dùng để truyền tải dữ liệu web lên máy chủ web cho dù máy chủ đặt rất xa.

Giao thức FTP được sử dụng nhiều nhất vào mục đích truyền tải dữ liệu, rút gọn thời gian cũng như đáp ứng nhu cầu của việc tải và truyền đi của các dữ liệu dung lượng lớn một cách nhanh chóng. Bạn có thể gửi đi và nhận những tệp tin có dung lượng lên đến vài trăm MB mà không phải lo lắng nó không được chuyển đi. Điều quan trọng là bạn có thể cùng lúc thực hiện việc upload/download nhiều tập tin để tiết kiệm thời gian mà không hề gặp phải vấn đề gì.

# **Mô hình hoạt động của giao thức FTP**

![image](https://user-images.githubusercontent.com/65167293/157799296-6b9cd483-f00d-43f4-b9b7-1c186606dd98.png)

Hình thức hoạt động của giao thức FTP dựa trên hai tiến trình cơ bản là kiểm soát kết nối và kết nối dữ liệu. Điều này xảy ra giữa client FTP và server FTP, hay còn gọi là Control Connection và Data Connection.

- Control connection (kiểm soát kết nối): Khi phiên làm việc bắt đầu thì trong suốt quá trình diễn ra công việc thì tiến trình này sẽ kiểm soát kết nối và chỉ thực hiện nhiệm vụ các thông tin điều khiển đi qua trong suốt quá trình truyền dữ liệu.
- Data connection (kết nối dữ liệu): Khác với Control connection thì đây là tiến trình nhằm thực hiện các kết nối chứ không còn kiểm soát nữa. Nó sẽ kết nối các dữ liệu khi dữ liệu được gửi từ server tới client hoặc ngược lại. Tiến trình này thực hiện xuyên suốt quá trình đến khi việc truyền dữ liệu hoàn tất thì nó cũng ngừng lại.


# **Các phương thức truyền dữ liệu trong giao thức FTP**

Như chúng tôi đã nhắc phía trên thì FTP là một giao thức truyền tải tập tin từ một máy tính đến máy tính khác thông qua một mạng TCP hoặc qua mạng Internet. Và việc truyền tải này được thực hiện theo 3 phương thức khác nhau là: Stream mode, Block mode, và Compressed mode. Cụ thể từng phương thức như sau:

- **Stream mode:** Là phương thức truyền tập tin không có cấu trúc dạng header. Dựa vào tính tin cậy trong việc truyền dữ liệu và thông qua kết nối TCP tới phía nhận nên chỉ ngắt kết nối là dữ liệu cũng kết thúc.
- **Block mode:** Các dữ liệu truyền được chia làm nhiều đoạn nhỏ sau đó được đóng gói lại thành các FTP blocks, mỗi gói đều chứa thông tin dữ liệu và điều này sẽ là việc truyền nhận dữ liệu an toàn, đúng chuẩn hơn.
- **Compressed mode**: Phương thức thứ 3 mà giao thức FTP thực hiện, phương thức này sẽ giúp các tệp tin, dữ liệu truyền đi nếu gặp phải trường hợp quá nặng thì chúng sẽ giúp xử lý đoạn tập tin đó bằng cách nén chúng lại và chuyển đi một cách đơn giản. Tuy nhiên hiện nay các tệp tin truyền đi đều được nén sẵn cho phù hợp nên Block mode có sẽ không cần thiết.
**


# **FTP client là gì?**

![image](https://user-images.githubusercontent.com/65167293/157799401-31fa1b21-8538-4ac6-8882-5b75290a0a41.png)

*Hình 1  Một số FTP client đi kèm với các tùy chọn bổ sung*

Một số FTP client đi kèm với các tùy chọn bổ sung, chẳng hạn như giao diện dòng lệnh cho các lệnh nâng cao, trình chỉnh sửa văn bản tích hợp (để tinh chỉnh các file dựa trên văn bản) và so sánh thư mục (cho phép bạn so sánh nội dung của hai thư mục).

Có một số FTP client tốt miễn phí có sẵn cho Windows. Hơn nữa, bạn có thể sử dụng Windows File Explorer như một FTP client, truy cập các file từ xa dưới dạng bộ nhớ đính kèm.

# **FTP trong trình duyệt**

Như đã đề cập ở trên, bạn có thể sử dụng FTP từ trình duyệt của mình. Bạn cần địa chỉ của FTP server. Địa chỉ sẽ hơi khác so với địa chỉ trang web thông thường, thay đổi https:// thành ftp://. Kết quả sẽ giống như sau:

    ftp://site.name.com

Khi nhập URL để truy cập vào FTP server, bạn sẽ phải nhập thông tin đăng nhập, chẳng hạn như tên người dùng hoặc địa chỉ email và mật khẩu. Một số FTP server cho phép truy cập trực tiếp với việc bao gồm tên người dùng và mật khẩu trong URL. Trong trường hợp này, URL sẽ trông giống như sau:

    ftp://ftp\_username:ftp\_password@site.name.com

Khi bạn đăng nhập vào FTP server trong trình duyệt của mình, bạn có thể truy cập các file tương tự như một FTP client. Tuy nhiên, các trình duyệt thường cung cấp ít tùy chọn bảo mật hơn, vì vậy bạn nên xem xét các FTP server mà bạn truy cập và nội dung bạn tải xuống.

# **Bạn có cần FTP server không?**

Đó là một câu hỏi thú vị. Nếu bạn thường xuyên gửi file cho mọi người, FTP server có thể phù hợp với bạn. FTP server cho phép bạn sắp xếp các file của mình như cách bạn làm trong File Explorer trên desktop, cung cấp quyền truy cập cho những người dùng khác để tải xuống file từ xa và đặt các quyền cụ thể đối với những gì người dùng có thể và không thể làm đối với file của bạn.

Ví dụ, bạn muốn cung cấp liên kết cố định cho album ảnh gia đình của mình trực tuyến, đồng thời cũng muốn cho gia đình mình quyền truy cập để upload ảnh của họ lên. FTP server riêng (yêu cầu mật khẩu mạnh và duy nhất) cung cấp một file hosting server mà gia đình bạn có thể truy cập để tải xuống và upload lên các album ảnh gia đình, tất cả ở cùng một nơi.

Album ảnh gia đình của bạn sau đó dễ quản lý hơn và có sẵn cho tất cả các thành viên trong gia đình. FTP server cũng không hạn chế dung lượng file lớn, trừ khi bạn chỉ định. Hơn hết, album ảnh gia đình được sao lưu, bảo vệ trước mọi sự cố không lường trước được.

Album ảnh gia đình là một ví dụ cơ bản về cách bạn có thể sử dụng FTP server. Còn vô số những ứng dụng khác, nhưng tóm lại, FTP chỉ xoay quanh một điều. Đó là giúp việc quản lý và chia sẻ file giữa các máy tính dễ dàng hơn.

# **Bạn có thể tạo FTP Server trên máy tính của mình**

Bạn có thể tạo FTP Server trên máy tính của mình? Điều này nghe có vẻ lạ nhưng thực tế bạn có thể làm được chỉ bằng một router có tích hợp tính năng FTP và kết nối bộ nhớ ngoài với Router là có thể tạo một máy chủ FTP tại nhà dễ dàng. Điều này giúp hạn chế và giảm các chi phí khi sử dụng.

Tầm quan trọng của FTP là rất lớn trong đời sống của con người. Các bạn có thể tìm mua các thiết bị Router có tích hợp tính năng FTP tại TOTOLINK Việt Nam. Những sản phẩm tiên tiến hiện đại này sẽ giúp bạn trong công việc được tốt hơn.

# **Kết luận**

Hy vọng bài viết sẽ giúp bạn hiểu hơn về giao thức FTP, ở đây mình chỉ nêu ra những kiến thức cơ bản, các bạn có thể tìm hiểu thêm và chia sẽ cho mình nhé.
