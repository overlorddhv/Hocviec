# Giao thức HTTP

**1. HTTP là gì?**

HTTP (HyperText Transfer Protocol – Giao thức truyền tải siêu văn bản) là một trong các giao thức chuẩn về mạng Internet, được dùng để liên hệ thông tin giữa Máy cung cấp dịch vụ (Web server) và Máy sử dụng dịch vụ (Web client), là giao thức Client/Server dùng cho World Wide Web – WWW

Giao thức HTTP là một giao thức tầng ứng dụng của bộ giao thức TCP/IP (các giao thức nền tảng cho Internet).

![image](https://user-images.githubusercontent.com/48250210/157997896-d9e2ed66-ac59-447e-b5ed-9024accca4e9.png)

** Cách hoạt động 

Giao thức HTTP hoạt động dựa trên mô hình Client – Server. Thông thường khi các bạn lướt web, các máy tính của người dùng sẽ đóng vai trò làm máy khách (Client). Sau một thao tác nào đó của người dùng, các máy khách sẽ gửi yêu cầu đến máy chủ (Server) và chờ đợi câu trả lời từ những máy chủ này.

![image](https://user-images.githubusercontent.com/48250210/157997977-5a6f3a08-a9f4-4f30-b876-f196f6b5a324.png)

Ngoài ra, khi các hệ thống trao đổi dữ liệu với nhau, chúng cũng sử dụng giao thức này nhưng 2 bên đều là server.

**2. HTTP - Requests**

Một HTTP client (máy khách) gửi một HTTP request (yêu cầu) lên server (máy chủ) nhờ một thông điệp có định dạng như sau:

    <method> <request-URL> <http-serverion>
    <headers>
    <body>
   
Ví dụ về một HTTP Requests

![image](https://user-images.githubusercontent.com/48250210/157998226-58ebd156-fd72-4c5c-85db-9aced77efa56.png)

**2.1. Request Line**

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

c. HTTP version

HTTP version là Phiên bản giao thức HTTP đang sử dụng.

**2.2. Request header**

Tiếp theo dòng Request-Line là các trường Request-header, cho phép client gửi thêm các thông tin bổ sung về thông điệp HTTP request và về chính client. Một số trường thông dụng như:

* Accept loại nội dung có thể nhận được từ thông điệp response. Ví dụ: text/plain, text/html…
* Accept-Encoding: các kiểu nén được chấp nhận. Ví dụ: gzip, deflate, xz, exi…
* Connection: tùy chọn điều khiển cho kết nối hiện thời. Ví dụ: keepalive,Upgrade…
* Cookie: thông tin HTTP Cookie từ server
* User-Agent: thông tin về user agent của người dùng.

**2.3. Request Body**

Body là dữ liệu mà Client sẽ gửi lên Server,

Một request body có thể là một đoạn text thuần túy, HTML, XML, JSON, Javascript, hoặc một tập các cặp key-value dạng form-data.

Khi bạn mở một web, trình duyệt sẽ nhận payload dạng HTML, nó chính là giao diện mà chúng ta quan sát được trên trình duyệt đó.

Thông thường khi làm việc với các HTTP APIs chúng ta sẽ gửi và nhận các payload dạng JSON hoặc XML.

Không phải tất cả các message HTTP đều phải có payload: POST và PUT có thể có, còn với GET và DELETE thì có thể không có payload.

Sau khi request server sẽ xử lý và phản hổi (response) tới client theo 1 trong 3 phương pháp:

* Server phân tích request nhận được, maps yêu cầu với tập tin trong tập tài liệu của server, và trả lại tập tin yêu cầu cho client.
* Server phân tích request nhận được, maps yêu cầu vào một chương trình trên server, thực thi chương trình và trả lại kết quả của chương trình đó.
* Request từ client không thể đáp ứng, server trả lại thông báo lỗi.
