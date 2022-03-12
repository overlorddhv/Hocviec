# I. Giao thức HTTP

**1.1. HTTP là gì?**

HTTP (HyperText Transfer Protocol – Giao thức truyền tải siêu văn bản) là một trong các giao thức chuẩn về mạng Internet, được dùng để liên hệ thông tin giữa Máy cung cấp dịch vụ (Web server) và Máy sử dụng dịch vụ (Web client), là giao thức Client/Server dùng cho World Wide Web – WWW

Giao thức HTTP là một giao thức tầng ứng dụng của bộ giao thức TCP/IP (các giao thức nền tảng cho Internet).

![image](https://user-images.githubusercontent.com/48250210/157997896-d9e2ed66-ac59-447e-b5ed-9024accca4e9.png)

** Cách hoạt động 

Giao thức HTTP hoạt động dựa trên mô hình Client – Server. Thông thường khi các bạn lướt web, các máy tính của người dùng sẽ đóng vai trò làm máy khách (Client). Sau một thao tác nào đó của người dùng, các máy khách sẽ gửi yêu cầu đến máy chủ (Server) và chờ đợi câu trả lời từ những máy chủ này.

![image](https://user-images.githubusercontent.com/48250210/157997977-5a6f3a08-a9f4-4f30-b876-f196f6b5a324.png)

Ngoài ra, khi các hệ thống trao đổi dữ liệu với nhau, chúng cũng sử dụng giao thức này nhưng 2 bên đều là server.

**1.2. HTTP - Requests**

Một HTTP client (máy khách) gửi một HTTP request (yêu cầu) lên server (máy chủ) nhờ một thông điệp có định dạng như sau:

    <method> <request-URL> <http-serverion>
    <headers>
    <body>
   
Ví dụ về một HTTP Requests

![image](https://user-images.githubusercontent.com/48250210/157998226-58ebd156-fd72-4c5c-85db-9aced77efa56.png)

**1.2.1. Request Line**

Bắt đầu của HTTP Request sẽ là dòng Request-Line bao gồm 3 thông tin:

**a. Method**

Báo cho Server rằng hành động sẽ phải sử lý với thông tin được gửi từ client lên.

Phương thức GET
* Câu truy vấn sẽ được đính kèm vào đường dẫn HTTP request. Ví dụ: /?username=”tinohost”&pass=”tenmien”
* GET request có thể được cached, bookmark và lưu trong lịch sử của trình duyệt mà bị giới hạn về chiều dài (chiều dài của URL là có hạn).
Lưu ý: Bạn không nên dùng GET request với dữ liệu quan trọng mà chỉ dùng để nhận dữ liệu, không có tính bảo mật.

Phương thức POST
* Câu truy vấn sẽ được gửi trong phần message body của HTTP request.
* POST không thể, cached, bookmark hay lưu trong lịch sử trình duyệt và cũng không bị giới hạn về độ dài.

Các phương thức khác

* HEAD: tương tự như GET nhưng chỉ gửi về HTTP header.
* PUT: tải lên một mô tả về URL định trước.
* DELETE: xóa một tài nguyên định trước.
* OPTIONS: trả về phương thức HTTP mà server hỗ trợ.
* CONNECT: chuyển kết nối của HTTP request thành một kết nối HTTP tunnel.

**b. Request URL**

Một URL (Uniform Resource Locator) được sử dụng để xác định duy nhất một tài nguyên trên Web. Một URL có cấu trúc như sau:

    protocol://hostname:port/path-and-file-name

Trong một URL có 4 thành phần:

* Protocol: giao thức tầng ứng dụng được sử dụng bởi client và server
* Hostname: tên DNS domain
* Port: Cổng TCP để server lắng nghe request từ client
* Path-and-file-name: Tên và vị trí của tài nguyên yêu cầu.

**c. HTTP version**

HTTP version là Phiên bản giao thức HTTP đang sử dụng.

**1.2.2. Request header**

Tiếp theo dòng Request-Line là các trường Request-header, cho phép client gửi thêm các thông tin bổ sung về thông điệp HTTP request và về chính client. Một số trường thông dụng như:

* Accept loại nội dung có thể nhận được từ thông điệp response. Ví dụ: text/plain, text/html…
* Accept-Encoding: các kiểu nén được chấp nhận. Ví dụ: gzip, deflate, xz, exi…
* Connection: tùy chọn điều khiển cho kết nối hiện thời. Ví dụ: keepalive,Upgrade…
* Cookie: thông tin HTTP Cookie từ server
* User-Agent: thông tin về user agent của người dùng.

**1.2.3. Request Body**

Body là dữ liệu mà Client sẽ gửi lên Server,

Một request body có thể là một đoạn text thuần túy, HTML, XML, JSON, Javascript, hoặc một tập các cặp key-value dạng form-data.

Khi bạn mở một web, trình duyệt sẽ nhận payload dạng HTML, nó chính là giao diện mà chúng ta quan sát được trên trình duyệt đó.

Thông thường khi làm việc với các HTTP APIs chúng ta sẽ gửi và nhận các payload dạng JSON hoặc XML.

Không phải tất cả các message HTTP đều phải có payload: POST và PUT có thể có, còn với GET và DELETE thì có thể không có payload.

Sau khi request server sẽ xử lý và phản hổi (response) tới client theo 1 trong 3 phương pháp:

* Server phân tích request nhận được, maps yêu cầu với tập tin trong tập tài liệu của server, và trả lại tập tin yêu cầu cho client.
* Server phân tích request nhận được, maps yêu cầu vào một chương trình trên server, thực thi chương trình và trả lại kết quả của chương trình đó.
* Request từ client không thể đáp ứng, server trả lại thông báo lỗi.

**1.3. HTTP – Responses

HTTP response là bản tin trả về từ server sang client, trong đó sẽ có các trường thông tin mà request yêu câu.

Định dạng gói tin HTTP response cũng gồm 3 phần chính là: Status line, Header và Body.

![image](https://user-images.githubusercontent.com/48250210/157998906-bb30b1c7-d50a-4974-9ee0-cb54e75df358.png)

**1.3.1. Response Status**
Gồm 3 trường là phiên bản giao thức (HTTP version), mã trạng thái (Status code) và mô tả  trạng thái (Status text):

* Phiên bản giao thức (HTTP version): phiên bản của giao thức HTTP mà server hỗ trợ, thường là HTTP/1.0 hoặc HTTP/1.1
* Mã trạng thái (Status code): mô tả trạng thái kết nối dưới dạng số, mỗi trạng thái sẽ được biểu thị bởi một số nguyên. Ví dụ: 200, 404, 302,…
* Mô tả trạng thái (Status text): mô tả trạng thái kết nối dưới dạng văn bản một cách ngắn gọn, giúp người dùng dễ hiểu hơn so với mã trạng thái. Ví du: 200 OK, 404 Not Found, 403 Forbiden,…

Một số loại thông dụng mà server trả về cho client như sau:

**1xx: information Message**

Các status code này chỉ có tính chất tạm thời, client có thể không quan tâm.

**2xx Successful**

Khi đã xử lý thành công request của client, server trả về status dạng này:

* 200 OK: request thành công.
* 202 Accepted: request đã được nhận, nhưng không có kết quả nào trả về, thông báo cho client tiếp tục chờ đợi.
* 204 No Content: request đã được xử lý nhưng không có thành phần nào được trả về.
* 205 Reset: giống như 204 nhưng mã này còn yêu câu client reset lại document view.
* 206 Partial Content: server chỉ gửi về một phần dữ liệu, phụ thuộc vào giá trị range header của client đã gửi.

**3xx Redirection**

Server thông báo cho client phải thực hiện thêm thao tác để hoàn tất request:

* 301 Moved Permanently: tài nguyên đã được chuyển hoàn toàn tới địa chỉ Location trong HTTP response.
* 303 See other: tài nguyên đã được chuyển tạm thời tới địa chỉ Location trong HTTP response.
* 304 Not Modified: tài nguyên không thay đổi từ lần cuối client request, nên client có thể sử dụng đã lưu trong cache.

**4xx Client error**

Lỗi của client:

* 400 Bad Request: request không đúng dạng, cú pháp.
* 401 Unauthorized: client chưa xác thực.
* 403 Forbidden: client không có quyền truy cập.
* 404 Not Found: không tìm thấy tài nguyên.
* 405 Method Not Allowed: phương thức không được server hỗ trợ.

**5xx Server Error**

Lỗi của server:

* 500 Internal Server Error: có lỗi trong quá trình xử lý của server.
* 501 Not Implemented: server không hỗ trợ chức năng client yêu cầu.
* 503 Service Unavailable: Server bị quá tải, hoặc bị lỗi xử lý.

**1.3.2. Response Header**

Header của gói tin response có chức năng tương tựn như gói tin request, giúp server có thể truyền thêm các thông tin bổ sung đến client dưới dạng các cặp “Name:Value”.

**1.3.3. Response Body**

Là nơi đóng gói dữ liệu để trả về cho client, thông thường trong duyệt web thì dữ liệu trả về sẽ ở dưới dạng một trang HTML để trình duyệt có thể thông dịch được và hiển thị ra cho người dùng.

Hoặc trả về dạng JSON, XML khi giao tiếp bằng API.

**1.4. Công cụ kiểm tra API với giao thức HTTTP**

Để kiểm tra giao thức HTTP và làm việc với các API chúng ta có thể sử dụng công cụ như:

**Postman**

Postman là một công cụ cho phép chúng ta thao tác với API, phổ biến nhất là REST. Postman hiện là một trong những công cụ phổ biến nhất được sử dụng trong thử nghiệm các API. Với Postman, ta có thể gọi Rest API mà không cần viết dòng code nào.

Postman hỗ trợ tất cả các phương thức HTTP (GET, POST, PUT, PATCH, DELETE, …). Bên cạnh đó, nó còn cho phép lưu lại lịch sử các lần request, rất tiện cho việc sử dụng lại khi cần.

**Soap UI**

Soap UI là công cụ phổ biến để kiểm tra API Nó cho phép bạn kiểm tra APU Rest và Soap một cách dễ dàng. Công cụ này tạo ra các thử nghiệm nhanh chóng với các thao tác đơn giản, dễ thực hiện.

# II. Giao thức HTTPS

**2.1. HTTPS là gì?**

HTTPS viết tắt của Hyper Text Transfer Protocol Secure (giao thức truyền tải siêu văn bản bảo mật) là phiên bản an toàn của HTTP, giao thức mà nhờ đó dữ liệu được gửi giữa trình duyệt và trang web bạn đang kết nối. Chữ ‘S’ ở cuối HTTPS là viết tắt của “Secure” (Bảo mật)

HTTPS cũng có những hoạt động giống như HTTP. Tuy nhiên, chúng được bổ sung SSL và TSL. Giao thức này đảm bảo không có bên thứ 3 đăng nhập được và đánh cắp thông tin. Dù cho bạn đang tìm kiếm thông tin bằng máy tính công cộng hay máy cá nhân thì HTTPS cũng sẽ đảm bảo thông tin liên lạc của bạn với máy chủ được bảo mật.

![image](https://user-images.githubusercontent.com/48250210/157999276-240b42e1-ffd9-44fa-aec1-d99febbd3334.png)

Bảo mật PKI –  Public Key Infrastructure
Cả hai giao thức TLS và SSL đều sử dụng hệ thống PKI (Public Key Infrastructure, hạ tầng khóa công khai) không đối xứng. Một hệ thống không đối xứng sử dụng hai “khóa” để mã hóa thông tin liên lạc, khóa “công khai” và khóa “riêng”. Bất cứ thứ gì được mã hóa bằng khoá công khai (public key) chỉ có thể được giải mã bởi khóa riêng (private key) và ngược lại.

Một hệ thống PKI hoàn chỉnh bao gồm các thành phần sau:

* Khóa công khai – Public Key
* Khóa bí mật – Privte Key
* Ủy quyền thẻ chứng thực – Certification Authority (CA)
* Ủy quyền thẻ đăng ký – Registration Authority (RA)
* Ủy quyền xác nhận hợp lệ – Validation Authority (VA)
* Thẻ chứng thực số – Digital certificates (DC)
* Thẻ chứng thực bị CA thu hồi – Certificate revocation list (CRL)
* Hệ thống phân phối thẻ – Certificate Distribution System (CDS)

Khi yêu cầu kết nối giao thức HTTPS với trang web, đầu tiên trang web sẽ gửi chứng chỉ SSL tới trình duyệt của bạn. Chứng chỉ này chứa khóa công khai cần thiết để bắt đầu phiên bảo mật. Dựa trên trao đổi ban đầu này, trình duyệt và trang web sẽ bắt đầu giao thức SSL handshake (giao thức bắt tay). Giao thức SSL handshake liên quan đến việc tạo bí mật chia sẻ để thiết lập kết nối an toàn duy nhất giữa bạn và trang web.

Khi sử dụng chứng chỉ SSL đáng tin cậy trong quá trình kết nối HTTPS, người dùng sẽ thấy biểu tượng ổ khóa trong thanh địa chỉ của trình duyệt. Khi một chứng chỉ Extended Validation Certificate được cài đặt trên một trang web, thanh địa chỉ sẽ chuyển sang màu xanh lá cây.

**2.2. Có nên sử dụng HTTPS không?**

Thời gian trước, HTTPS chỉ sử dụng cho website lớn như ngân hàng, tài chính, thương mại điện tử để bảo mật thông tin tối đa. Tuy nhiên, vì tính bảo mật tiêu chuẩn của nó mà hầu hết các website của doanh nghiệp hiện nay đều cần sử dụng. Bởi vì:

* HTTPS giúp bảo mật thông tin người dùng
HTTPS có phương thức mã hóa đảm bảo các thông điệp giữa máy khách và máy chủ không cung cấp được cho bên thứ 3 (hacker). Khi bạn truy cập vào website không cài đặt HTTPS thì sẽ phải đối diện với nguy cơ bị tấn công dữ liệu. Hacker có thể đánh cắp các dữ liệu mà bạn gửi đi như: email. Password, thẻ tín dụng,…. Thậm chí, mọi theo tác của bạn đều bị theo dõi thậm chí ghi lại.

Khi được thiết lập HTTPS thì người dùng hoàn toàn yên tâm khi các dữ liệ trao đổi tới máy chủ luôn được an toàn, không sai lệch và không bị mất dữ liệu.

![image](https://user-images.githubusercontent.com/48250210/157999618-b8d382b8-216c-4f34-916d-774810635a5f.png)

* Tránh bị website giả mạo lừa đảo

Nếu bạn để ý sẽ thấy được bất kỳ server nào cũng có thể giả dạng server của bạn để đánh cắp thông tin người dùng hay lừa đảo kiểu Phishing. Khi cài HTTPS, trước khi dữ liệu được mã hóa để tiếp tục trao đôi thì trên trình duyệt máy khách sẽ có yêu cầu kiểm tra SSL từ máy chủ để đảm bảo rằng người dùng đang truyền thông tin đến đúng đối tượng mong muốn. Chứng chỉ TSL/SS trên HTTPS sẽ giúp xác minh website chính thức của doanh nghiệp.

* Tăng uy tín của Website

Các trình duyệt web như Google, Chrome, Firefox ,… thì đều hiển thị cảnh báo về những website HTTP (không bảo mật). Đây là hành động giúp bảo vệ dữ liệu cho người dùng tránh bị đánh cắp những thông tin quan trọng.

Bảo vệ người dùng chính là bảo vệ website của bạn bởi nếu website không được người dùng tin tưởng thì bạn sẽ mất đi user có sẵn. Chính vì thế cần dùng HTTPS để bảo mật và gìn giữ uy tín cho bạn.

![image](https://user-images.githubusercontent.com/48250210/157999644-62941641-9ae4-444f-9f93-086e7e6f48b5.png)

# 3. Kết luận

Ta có thể phân biệt HTTP và HTTPS qua những tiêu chí sau:

![image](https://user-images.githubusercontent.com/48250210/157999709-64358473-e72c-4e56-83c8-ae93ab947654.png)

HTTP kết nối sẽ đơn giản hơn HTTPS nhưng phần bảo mật sẽ không được đảm bảo, dễ bị tấn công.
