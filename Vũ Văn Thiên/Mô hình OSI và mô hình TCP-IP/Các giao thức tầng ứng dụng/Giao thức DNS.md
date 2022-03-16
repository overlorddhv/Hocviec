# Giao thức DNS

# DNS Là gì?

DNS là viết tắt của cụm từ Domain Name System, mang ý nghĩa đầy đủ là hệ thống phân giải tên miền. DNS được phát minh vào năm 1984 cho Internet, chỉ một hệ thống cho phép thiết lập tương ứng giữa địa chỉ IP và tên miền.Hiểu một cách ngắn gọn nhất, DNS cơ bản là một hệ thống chuyển đổi các tên miền website mà chúng ta đang sử dụng, ở dạng www.tenmien.com sang một địa chỉ IP dạng số tương ứng với tên miền đó và ngược lại.

Thao tác này của DNS giúp liên kết các thiết bị mạng với nhau nhằm mục đích định vị và gán một địa chỉ cụ thể cho các thông tin trên internet.

![image](https://user-images.githubusercontent.com/62273292/158499514-ba89d9ff-f804-4b18-a997-3efdceedf76b.png)

## Chức năng của DNS là gì?

Về chức năng, DNS có thể được hiểu như một “người phiên dịch” và “truyền đạt thông tin”. DNS sẽ làm công việc dịch tên miền thành một địa chỉ IP gồm 4 nhóm số khác nhau. Ví dụ như www.tenmien.com thành 421.64.874.899 hoặc ngược lại dịch một địa chỉ IP thành tên miền.

Khi “dịch” như thế, trình duyệt sẽ hiểu và đăng nhập vào được. Và khi người dùng đăng nhập vào một website, thay vì phải nhớ và nhập một dãy số địa chỉ IP của hosting, thì chỉ cần nhập tên website là trình duyệt tự động nhận diện.

Mỗi máy tính trên Internet đều có một địa chỉ IP duy nhất. Địa chỉ IP này được dùng để thiết lập kết nối giữa server và máy khách để khởi đầu một kết nối. Bất kỳ khi nào, bạn truy cập vào một website tùy ý hoặc gửi một email, thì DNS đóng vai trò rất quan trọng trong trường hợp này.

ngoài ra thì mỗi DNS còn có chức năng ghi nhớ những tên miền mà nó đã phân giải và trong những lần truy cập tới, nó sẽ ưu tiên sử dụng. Đó là lý do mà bạn sử dụng nhiều dịch vụ mạng như research thông tin, xem phim, chơi game giải trí,… nhanh chóng và dễ dàng hơn.

![image](https://user-images.githubusercontent.com/62273292/158499816-0df8df53-fea1-4bd5-990b-6bb36dd0115e.png)

## Cách hoạt động của DNS

DNS hoạt động từng bước theo cấu trúc của nó. Bước đầu là một truy vấn để lấy thông tin được gọi là “DNS query” .

Lại quay về với ví dụ tìm kiếm website www.google.com trong web browser nhé!

→ Đầu tiên, DNS server sẽ tìm thông tin phân giải trong file hosts – tức file text trong hệ điều hành, chịu trách nhiệm chuyển hostname thành IP.

Nếu không thấy thông tin, nó sẽ quay về tìm trong cache – bộ nhớ tạm của phần cứng hay phần mềm. Nơi phổ biến nhất thường lưu thông tin này chính là bộ nhớ tạm của trình duyệt và bộ nhớ tạm ISP (Internet Service Providers.
Nếu không nhận được thông tin, bạn sẽ thấy mã bị lỗi hiện lên.

## Sử dụng DNS như thế nào?

Các Domain name system có tốc độ biên dịch khác nhau, bởi vậy, người dùng có thể tự lựa chọn DNS Server để sử dụng. Hoặc bạn có thể sử dụng DNS mặc định của nhà cung cấp dịch vụ Internet, hoặc dùng Domain Name Server miễn phí hoặc trả phí khác, đều được. Nhưng có một lưu ý là khi sử dụng các DNS Server khác, bắt buộc bạn phải thay đổi trong máy tính của mình.

Các bước thay đổi DNS trong máy tính
  - 1: Chọn Start – Setting – Network Connection
  - 2: Double click vào Local Area Connection, chọn Properties – Internet Protocol (TCP/IP) – Properties
  - 3: Điền thông số DNS Server bạn muốn vào 2 ô “Preferred DNS Server” & “Alternate DNS Server”.
Lưu ý

Các Hacker có thể thông qua DNS để đánh cắp những thông tin cá nhân của bạn. Vậy nên, hãy kiểm tra rõ tên truy cập của các Website, tránh truy cập vào các website giả mạo, các phần mềm không rõ nguồn gốc.


## Các loại bản ghi DNS

CNAME Record (Bản ghi CNAME): Cho phép bạn tạo một tên mới, điều chỉnh trỏ tới tên gốc và đặt TTL. Tóm lại, tên miền chính muốn đặt một hoặc nhiều tên khác thì cần có bản ghi này. 

A Record: Bản ghi này được sử dụng phổ biến để trỏ tên Website tới một địa chỉ IP cụ thể. Đây là bản ghi DNS đơn giản nhất, cho phép bạn thêm Time to Live (thời gian tự động tái lại bản ghi), một tên mới và Points To ( Trỏ tới IP nào).

MX Record: Với bản ghi này, bạn có thể trỏ Domain đến Mail Server, đặt TTL, mức độ ưu tiên (Priority). MX Record chỉ định Server nào quản lý các dịch vụ Email của tên miền đó.

AAAA Record: Để trỏ tên miền đến một địa chỉ IPV6 Address, bạn sẽ cần sử dụng AAA Record. Nod cho phép bạn thêm Host mới, TTL,IPv6.

TXT Record: Bạn cũng có thể thêm giá trị TXT, Host mới, Points To, TTL. Để chứa các thông tin định dạng văn bản của Domain, bạn sẽ cần đến bản ghi này.

SRV Record: Là bản ghi dùng để xác định chính xác dịch vụ nào chạy Port nào. Đay là Record đặc biệt trong DNS. Thông qua nó, bạn có thể thêm Name, Priority, Port, Weight, Points to, TTL.

NS Record: Với bản ghi này, bạn có thể chỉ định Name Server cho từng Domain phụ. Bạn có thể tạo tên Name Server, Host mới, TTL


## Tại sao DNS dễ bị tấn công?

Quá trình tên miền được dịch thành địa chỉ IP, được gọi là phân giải DNS

Khi ai đó nhập một tên miền nào đó, chẳng hạn www.google.com vào Web Browser, thì trình duyệt lập tức liên hệ với 1 máy chủ tên, để lấy địa chỉ IP tương ứng. Có 2 loại máy chủ tên:

Máy chủ tên có thẩm quyền: Nơi lưu trữ thông tin đầy đủ về một vùng

Máy chủ tên đệ quy: Nơi trả lời các truy vấn DNS cho người dùng Internet, đồng thời lưu trữ kết quả phản hồi của DNS trong một khoảng thời gian.

Thông quan các màn battle “ngoài sáng trong tối” này, tội phạm mạng sẽ có thể:

  - Cướp Email
  - Can thiệp Voice Over IP ( VoIP )
  - Mạo danh các trang web
  - Đánh cắp thông tin đăng nhập và mật khẩu
  - Trích xuất dữ liệu thẻ tín dụng và một số thông tin mật khác

![image](https://user-images.githubusercontent.com/62273292/158502357-e5ee707a-444f-4eca-93fe-a9d3eb42b075.png)



