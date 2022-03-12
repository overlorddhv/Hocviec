# I. Tổng quan về FTP(File Transfer Protocol)

**1.1. FTP là gì?**

FTP – File Transfer Protocol (Giao thức truyền tải tập tin) được dùng trong việc trao đổi dữ liệu trong mạng thông qua giao thức TCP/IP, thường hoạt động trên 2 cổng là 20 và 21. Với giao thức này, các máy client trong mạng có thể truy cập đến máy chủ FTP để gửi hoặc lấy dữ liệu. Điểm nổi bật là người dùng có thể truy cập vào máy chủ FTP để truyền và nhận dữ liệu dù đang ở xa.

**1.2. Mục đích sử dụng**

* Được sử dụng để trao đổi tập tin qua mạng lưới truyền thông sử dụng TCP/IP (internet, mạng nội bộ, …)
* Sử dụng để tải xuống máy tính các file từ máy chủ.
* Tại sao nên dùng FTP: Mặc dù việc truyền file từ hệ thống này sang hệ thống khác rất đơn giản và dễ hiểu, nhưng đôi khi xảy ra những vấn đề khác nhau. Ví dụ, 2 hệ thống có thể có các quy ước tập tin khác nhau, 2 hệ thống có các cách khác nhau để thể hiện văn bản và dữ liệu hay 2 hệ thống có cấu trúc thư mục khác nhau, … Giao thức FTP khắc phục những vấn đề này bằng cách thiết lập 2 kết nối giữa các máy chủ. Một kết nối để sử dụng truyền dữ liệu, 1 kết nối còn lại được sử dụng để điều khiển kết nối.

# II. Mô hình và nguyên lí hoạt động của FTP

**2.1. Mô hình cơ bản FTP**

**2.1.1. Kết nối TCP trong FTP**

![image](https://user-images.githubusercontent.com/48250210/158003559-e7a8cec1-53e0-4467-ba7c-b0246efbb4df.png)

Giống như hầu hết các giao thức TCP/IP, FTP dựa trên mô hình Client – Server. Tuy nhiên, khác với các ứng dụng khác chạy trên nền TCP/IP, FTP cần tới 2 kết nối TCP:

* Control connection (sử dụng port 21 – trên server): Đây là kết nối TCP logic chính được tạo ra khi phiên làm việc được thiết lập. Nó được thực hiện giữa các quá trình điều khiển. Nó được duy trì trong suốt phiên làm việc và chỉ cho các thông tin điều khiển đi qua như lệnh hay response(phản hồi)
* Data connection (sử dụng port 20 – trên server): Kết nối này sử dụng các quy tắc rất phức tạp vì các loại dữ liệu có thể khác nhau. Nó được thực hiện giữa các quá trình truyền dữ liệu. Kết nối này mở khi có lệnh chuyển tệp và đóng khi tệp truyền xong.

**2.1.2. Mô hình FTP**

Sơ đồ minh họa

![image](https://user-images.githubusercontent.com/48250210/158003581-143a8aaa-b8f0-4641-a394-8fd3e722b61a.png)

Do chức năng điều khiển và dữ liệu được truyền tải bằng cách sử dụng các kênh riêng biệt nên mô hình FTP chia mỗi thiết bị thành 2 phần giao thức logic chịu trách nhiệm cho mỗi kết nối ở trên:

* Protocol interpreter (PI): Là thành phần quản lý kênh điều khiển, phát và nhận lệnh và trả lời.
* Data transfer process (DTP): chịu trách nhiệm gửi và nhận dữ liệu giữa client và server.

**2.1.3. Chức năng từng phần trong mô hình FTP**

* Phía Server

  * Server Protocol Interpreter (Server-PI) : Chịu trách nhiệm quản lí Control Connection trên Server. Nó lắng nghe yêu cầu kết nối hướng từ User trên cổng 21. Khi kết nối được thiết lập, nó nhận lệnh từ User-PI, gửi phản hồi và quản lí tiến trình truyền dữ liệu trên Server.
  * Server Data Transfer Process (Server-DTP) : chịu trách nhiệm nhận và gửi file từ User-DTP. Server-DTP vừa làm nhiệm vụ thiết lập Data Connection và lắng nghe Data Connection của User thông qua cổng 20. Nó tương tác với Server File System trên hệ thống cục bộ để đọc và chép file.

* Phía Client

  * User Interface: Đây là chương trình được chạy trên máy tính, nó cung cấp giao diện xử lí cho người dùng, chỉ có trên phía Client. Nó cho phép người dùng sử dụng những lệnh đơn giản để điều khiển các session FTP, từ đó có thể theo dõi được các thông tin và kết quả xảy ra trong quá trình.
  * User Protocol Interpreter (User-PI): Chịu trách nhiệm quản lí Control Connection phía Client. Nó khởi tạo phiên kết nối FTP bằng việc phát hiện ra Request tới Server-PI. Sau khi kết nối được thiết lập, nó xử lí các lệnh nhận được trên User Interface, gửi chúng tới Server-PI rồi đợi nhận Response trở lại. Nó cũng quản lí các tiến trình trên Client.
  * User Data Transfer Process (User-DTP): Có nhiệm vụ gửi hoặc nhận dữ liệu từ Server-DTP. User-DTP có thể thiết lập hoặc lắng nghe DataConnection từ Server thông qua cổng 20. Nó tương tác với Client File System trên Client để lưu trữ file.

**2.2.2. Nguyên lí hoạt động của FTP**

Cần có 2 kết nối TCP trong phiên làm việc của FTP: TCP Data connection trên cổng 20, TCP Control connection trên cổng 21.

* Control connection : luôn được mở ở mọi thời điểm khi dữ liệu hoặc lệnh được gửi.
* Data connection : chỉ được mở khi có trao đổi dữ liệu thực.

Trình tự chung của FTP hoạt động như sau:

1. FTP Client mở Control connection đến FTP server (trên port 21) và chỉ định 1 cổng trên Client để Server gửi lại phản hồi. Đường kết nối này dùng để truyền lệnh và không phải là dữ liệu. Control connection sẽ mở trong suốt thời gian của phiên làm việc (telnet giữa 2 hệ thống)
2. Client chuyển tiếp thông tin như username, password tới Server để thực hiện xác thực (authentication). Server sẽ trả lời bằng mã chấp nhận hay từ chối của các request.
3. Client gửi thêm các lệnh với tên tệp, kiểu dữ liệu, … để vận chuyển, thêm luồng dữ liệu(tức là chuyển tập tin từ máy khách đến máy chủ hoặc ngược lại). Server sẽ phản hồi với mã (reply code) chấp nhận hoặc từ chối.
4. Khi dữ liệu đã sẵn sàng, 2 bên sẽ mở kết nối TCP trên cổng 20.
5. Dữ liệu có thể được vận chuyển giữa Client và Server trên cổng 20. Dữ liệu vận chuyển được mã hóa theo 1 số định dạng bao gồm NVT-ASCII hoặc nhị phân(binary)
6. Khi quá trình vận chuyển dữ liệu được hoàn thành, phiên làm việc của FTP Server sẽ đóng lại Data Connection trên cổng 20. Nhưng vẫn giữ Control Connection trên công 21.
7. Control connection có thể được sử dụng để thiết lập truyền dữ liệu khác hoặc đóng liên kết.

**2.3. Một số lệnh command sử dụng trên FTP**

![image](https://user-images.githubusercontent.com/48250210/158003786-0b13e794-1a19-4433-9d35-54e88fc964e5.png)

**2.4. FTP Reply**

Mỗi lần User-PI gửi lệnh đến Server-PI qua Control connection, server sẽ gửi lại phản hồi dưới dạng các code. Code reply nhằm các mục đích sau:

* Xác nhận máy chủ đã nhận được lệnh.
* Cho biết lệnh từ phía người dùng có được chấp nhận hay không, nếu xảy ra lỗi thì đó là lỗi gì.
* Cho biết nhiều thông tin khác nhau cho người dùng về phiên, ví dụ như là: tình trạng truyền file, …

Cấu trúc của FTP reply code : Xyz.

* Ý nghĩa của X trong FTP reply code

![image](https://user-images.githubusercontent.com/48250210/158003874-ced46d10-e235-4eff-a1a0-dbe5795580d0.png)

* Tham số y cung cấp thêm thông tin như bảng dưới. z cũng cung cấp thêm thông tin nhưng ý nghĩa chính xác có thể khác nhau giữa các cài đặt.

![image](https://user-images.githubusercontent.com/48250210/158003889-b5ade01d-0a56-401d-9c76-6e85bb660070.png)

**Chú ý:** Điều quan trọng cần lưu ý trong FTP, các Request không nhất thiết phải được thực hiện theo cùng 1 trình tự khi đã gửi, các giao dịch (transactions) và trả lời (reply) có thể được xen kẽ.

**2.5. Tính bảo mật của FTP**

Giống như phần lớn các giao thức cũ, phương pháp đăng nhập đơn giản của FTP là một sự kế thừa từ những giao thức ở thời kì đầu của Internet. Ngày nay, nó không còn đảm bảo tính an toàn cần thiết trên môi trường Internet toàn cầu vì username và password được gửi qua kênh kết nối điều khiển dưới dạng clear text(không mã hóa).

Điều này làm cho bảo mật FTP đã định ra thêm nhiều tùy chọn chứng thực và mã hóa phức tạp cho những ai muốn tăng thêm mức độ an toàn vào trong phần mềm FTP của họ.

# III. Kênh dữ liệu trong FTP
Kênh điều khiển được tạo ra giữa Server-PI và User-PI, sử dụng quá trình thiết lập kết nối và chứng thực được duy trì trong suốt phiên kết nối FTP. Các lệnh và các hồi đáp được trao đổi giữa bộ phận PI (Protocol Interpreter) qua kênh điều khiển, những dữ liệu thì không.

Mỗi khi cần phải truyền dữ liệu giữa các server và client, một kênh dữ liệu cần phải được tạo ra. Kênh dữ liệu kết nối bộ phận User-DTP và Server-DTP. Kết nối này cần thiết cho cả hoạt động truyền file trực tiếp (gửi hoặc nhận một file) cũng như đối với việc truyền dữ liệu ngầm, như là yêu cầu một danh sách file trong thư mục nào đó trên server.

Để tạo ra kênh dữ liệu, FTP sử dụng 2 phương thức khác nhau: Normal (Active) Data Connections (mặc định) và Passive Data Connections.

Khác biệt giữa 2 phương thức này là phía Client hay bên Server đưa ra yêu cầu khởi tạo kết nối.

**3.1. Normal (Active) Data Connections**

Phương thức tạo kết nối dữ liệu bình thường hay còn gọi là Kết nối kênh dữ liệu ở dạng chủ động.

Phía Server-DTP tạo kênh dữ liệu bằng cách mở một cổng kết nối tới User-DTP. Server sử dụng cổng đặc biệt được dành riêng cho kết nối dữ liệu là cổng số 20. Trên máy Client, cổng mặc định được sử dụng chính là cổng được sử dụng để kết nối điều khiển, nhưng Server sẽ thường chọn mỗi cổng khác nhau cho mỗi chuyển giao.

**3.2. Passive Data Connections**

Phương thức tạo kết nối bị động.

* Server sẽ chấp nhận 1 yêu cầu kết nối dữ liệu được khởi tạo từ Client.
* Server sẽ trả lời lại phía Client với địa chỉ IP cũng như địa chỉ cổng mà Server sẽ sử dụng.
* Sau đó phía Server-DTP lắng nghe trên cổng này một kết nối TCP đến từ User-DTP.
* Theo mặc định, phía Client sẽ sử dụng cùng cổng mà nó sử dụng cho Control Connection như trong trường hợp chủ động. Tuy nhiên, trong phương pháp này, Client cũng có thể chọn sử dụng một cổng khác cho Data Connection nếu cần thiết.

# IV. Các phương thức truyền dữ liệu trong FTP
Khi Client-DTP và Server-DTP thiết lập xong kênh dữ liệu, dữ liệu sẽ được truyền trực tiếp từ phía Client tới phía Server, hoặc ngược lại, tùy theo các lệnh được sử dụng. Do thông tin điều khiển được gửi đi trên kênh điều khiển, nên toàn bộ kênh dữ liệu có thể được sử dụng để truyền dữ liệu. FTP có ba phương thức truyền dữ liệu, đó là: stream mode, block mode, và compressed mode.

**4.1. Stream mode**

* Dữ liệu truyền đi liên tiếp dưới dạng các byte không cấu trúc.
* Thiết bị gửi chỉ đơn thuần đẩy luồng dữ liệu qua kết nối TCP tới phía nhận.
* Không có trường tiêu đề nhất định
* Không có cấu trúc dạng Header, nên việc báo hiệu kết thúc file sẽ đơn giản được thực hiện khi thiết bị gửi ngắt kênh kết nối dữ liệu khi đã truyền dữ liệu xong.
* Được sử dụng nhiều nhất trong 3 phương thức trong triển khai FTP thực tế. Do:
 * Là phương thức mặc định và đơn giản nhất.
 * Là phương thức phổ biến nhất, vì nó xử lí các file chỉ đơn thuần là xử lí dòng byte, mà không cần để ý tới nội dung.
 * Không tốn 1 lượng byte “overload” nào để thông báo Header.

**4.2. Block mode**

* Phương thức truyền dữ liệu mang tính quy chuẩn hơn.
* Dữ liệu được chia thành nhiều khối nhỏ và đóng gói thành các FTP block.
* Mỗi block có 1 trường Header 3 byte: báo hiệu độ dài, và chứa thông tin về các khối dữ liệu đang được gửi.
* Một thuật toán đặc biệt được sử dụng để kiểm tra các dữ liệu đã truyền đi. Và để phát hiện, khởi tạo lại đối với 1 phiên truyền dữ liệu đã bị ngắt kết nối.

**4.3. Compressed mode (Chế độ nén)**

* Phương thức truyền dữ liệu sử dụng 1 kỹ thuật nén đơn giản, là “run-lenght encoding (mã hóa chiều dài)” – có tác dụng phát hiện và xử lí các đoạn lặp trong dữ liệu được truyền đi để giảm chiều dài của toàn bộ thông điệp.
* Thông tin sau khi được nén, sẽ được xử lí như Block mode, với trường Header.
* Trong thực tế, việc nén dữ liệu thường được thực hiện ở chỗ khác, làm cho phương thức Compressed mode trở nên không cần thiết.
