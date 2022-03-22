
# Web Server là gì? Tìm hiểu cơ chế vận hành của web server

![image](https://user-images.githubusercontent.com/62273292/158772287-95bee322-4f7b-4750-b3c1-1707c46b2e62.png)


## Web server là gì?

Web server hay còn gọi là máy chủ web, trong đó được kết nối và liên kết mạng máy tính mở rộng. Máy chủ web được cài đặt các chương trình để phục vụ ứng dụng web, chứa toàn bộ dữ liệu và nắm quyền quản lý. Web server có thể lấy thông tin requess từ phía trình duyệt web và gửi phần hồi tới máy khách thông qua HTTP hoặc giao thức khác.

Web server là gì? 
Web server hay còn gọi là máy chủ web, trong đó được kết nối và liên kết mạng máy tính mở rộng. Máy chủ web được cài đặt các chương trình để phục vụ ứng dụng web, chứa toàn bộ dữ liệu và nắm quyền quản lý. Web server có thể lấy thông tin requess từ phía trình duyệt web và gửi phần hồi tới máy khách thông qua HTTP hoặc giao thức khác.

Những web server được sử dụng nhiều nhất hiện nay: Apache, Nginx, IIs...

![image](https://user-images.githubusercontent.com/62273292/158772500-76749286-0deb-404b-a204-fa67da032418.png)


## Về mặt phần cứng

Web server là một máy tính lưu trữ các file thành phần tạo nên một website (ví dụ: HTML, images, CSS, và file javacript...) và truyền chúng tới người dùng cuối. 

Web server được kết nối đến internet và truy cập thông qua một domain giống như mozilla.org. 

## Về mặt phần mềm

Web server bao gồm một số phần kiểm soát người dùng web truy cập đến file host tại tối thiểu một HTTP server. Một HTTP server là một phần của phần mềm nó hiểu là URLs(web address) và HTTP (là phương thức để trình duyệt của bạn hiển thị trang web) Ở mức cơ bản nhất, bất cứ một trình duyệt nào cần một file host trên một web server, trình duyệt đó sẽ request file đó thông qua HTTP. Khi một yêu cầu được gửi đến địa chỉ web server đúng thì HTTP server gửi trở lại một yêu cầu thông qua HTTP. 

## Để công khai một trang web

![image](https://user-images.githubusercontent.com/62273292/158772673-49af1c7d-a843-45d3-893b-abbb34858280.png)


Chúng ta cần một web server tĩnh hoặc một web server động. 

Một web server tĩnh hay bao gồm một máy tính với một HTTP server. Chúng ta gọi đó là web server tĩnh vì web server gửi cái file không hề thay đổi của nó đến trình duyệt của người dùng. 


Một web server động bao gồm một web server tĩnh cùng với các phần mềm mở rộng của chúng, nhìn chung nhất đó là các application server và databases. Chúng ta gọi nó là web động vì application server update các host file trước khi gửi nó về trình duyệt của người dùng thông qua HTTP server. 


Ví dụ để tạo ra trang web cuối cùng bạn nhìn thấy trên trình duyệt, application server sẽ điền đầy đủ vào các HTLM tempate với nội dung được lấy ra từ databases. Ví dụ như MDN và Wikipedia có hàng nghìn trang web. Nhưng chúng không phải là tài liệu HTTM thực. Chỉ một khuân mẫu HTML và một database rất lớn. Cài đặt này làm cho nó dễ dàng và nhanh hơn cho việc quản lý và truyền nội dung. 

**Cách trả lại response của web server**

Để truy nhập vào một trang web, trình duyệt của bạn gửi một yêu cầu đến server. Web server sẽ xử lý và tìm kiếm file được yêu cầu đó trong bộ nhớ của web server. Trong việc tìm file, Server sẽ đọc file đó xử lý nó nếu cần rồi gửi nó về cho trình duyệt.

## Hosting files (Web server lưu trữ các file)

Thứ nhất, web server phải lưu trữ các file của website nó là tất cả các file HTML và các file liên quan đến nó nó như css và javascript, fonts và các video ...

Về mặt kỹ thuật thì bạn có thể lưu trữ tất cả các file đó trên máy tính của mình, nhưng để thuận tiện hơn thì chúng ta nên lưu trữ dữ liệu đó trên các web server riêng rẽ có các đặc tính sau:

Luôn chạy và hoạt động liên tục.

Luôn luôn kết nối với internet.

Luôn có trung một địa chỉ IP. 

Được bảo trì bởi một bên cung cấp thứ 3. 


Vì tất cả các lý do trên việc tìm một nhà cung cấp host tốt là một phần quan trọng trong việc phát triên websites. Hiện có rất nhiều công ty cung cấp các giải pháp hosting cho việc phát triển web bạn chỉ cần chọn một trang web tốt phù hợp với ngân sách của bạn. 

## Giao tiếp thông qua HTTP

Thứ hai, một web server cung cấp các dịch vụ hỗi trợ HTTP (Hypertext Transfer Protocol). Cũng như cái tên của nó, HTTP chỉ ra cách truyền siêu văn bản giữa hai máy tính. Giao thức là tập hợp các quy tắc để truyền thông giữa hai máy tính. HTTP là một giao thức nguyên bản, vô cấp.


- Textual: tất cả các lệnh là văn bản thuần túy mà còn con người có thể đọc.
- Stateless: Cả máy chủ và khách đều không nhớ rõ các thao tác trước đó.

HTTP cung cấp một luật rất rõ ràng cho người dùng và server giao tiếp trao đổi với nhau. Bạn cần lưu ý những điều sau:

 - Chỉ có khách được phép gửi request tới server và chỉ có server mới có quyền trả lời các request của khách.
 - Khi yêu cầu một file thông qua HTTP, khách phải cung cấp url của file.
 - Wed server phải trả lời mọi yêu cầu HTTP, ít nhất với thông báo lỗi.

Trên web server, máy chủ HTTP có trách nhiệm xử lý và trả lời các yêu cầu đến:

- Khi nhận yêu cầu, máy chủ HTTP đầu tiên sẽ kiểm tra xem URL yêu cầu có khớp với tệp hiện có hay không.  
- Nếu vậy, máy chủ web gửi nội dung tệp tin về trình duyệt. 
- Nếu không, máy chủ ứng dụng sẽ tạo tệp cần thiết. Nếu không thể xử lý được, máy chủ web trả lại thông báo lỗi cho trình duyệt, thông thường là "404 Not Found" NGINX

## Web server hoạt động như thế nào?

Bất cứ khi nào bạn xem một trang web trên internet, có nghĩa là bạn đang yêu cầu trang đó từ một web server.

Khi bạn nhập URL trên trình duyệt của mình (ví dụ: https://nhanhoa.com), trình duyệt của bạn yêu cầu trang từ web server và web server sẽ gửi lại trang.

![image](https://user-images.githubusercontent.com/62273292/158773561-a7163bab-790e-47e4-b87e-b71f869c1453.png)



# Tìm hiểu về Nginx

## 1, Tổng quan

Nginx là 1 máy chủ reverse proxy mã nguồn mở cho các giao thức HTTP, HTTPS, SMTP, POP3 và IMAP, cũng như là 1 máy chủ cân bằng tải (load balancer), HTTP cache và web. Dự án Nginx được bắt đầu với việc tập trung vào tính đồng thời cao, hiệu năng cao và sử dụng tài nguyên thấp và được phát triển bởi Igor Sysoev vào nằm 2002, được phân phối ra công chúng lần đầu vào nằm 2004.

Không giống với các máy chủ web truyền thống, Nginx không dựa trên luồn (thread) để xử lý yêu cầu. Thay vào đó, nó sử dụng 1 kiến trúc bất đồng bộ hướng sự kiện linh hoạt . Kiến trúc này sử dụng ít, nhưng quan trọng hợn, là lượng bộ nhớ có thể dự đoán khi hoạt động. Đây chính là điểm mấu chốt khiến Nginx là 1 trong số ít những máy chủ được viết để giải quyết vấn đề C10K

Nói đến đây một số bạn sẽ tò mò là vấn đề C10K là gì ? Hiểu đơn giản thì do các máy chủ web truyền thống xử lý các yêu cầu dựa trên luồn (thread), tức là mỗi khi máy chủ web nhận được 1 yêu cầu mới, nó sẽ tạo ra 1 luồng mới để xử lý cho yêu cầu này, và cứ thế khi số lượng các yêu cầu gửi đến máy chủ web ngày càng nhiều thì số lượng các luồn xử lý này trong máy chủ sẽ ngày càng tăng. Và điều này dẫn đến việc thiếu hụt tài nguyên cấp cho các luồn xử lý trên ... (Các bạn có thể tìm hiểu rõ hơn tại đây)

Hiện nay, có khoảng 14,72 % (hơn 137 triệu) các website trên Internet đang sử dụng Nginx là máy chủ web.

![image](https://user-images.githubusercontent.com/62273292/159424417-9835e07c-bb53-423e-a285-d42e29f0a5e7.png)


## 2, Kiến trúc của Nginx

Khi được khởi chạy service, nginx khởi tạo mọt tiến trình chủ và cũng là tiến trình duy nhất tồn tại trong bộ nhớ Master Process. Tiến trình này không chịu trách nhiệm tự xử lý bất kỳ request nào từ phía client mà thay vào đó nó sinh ra các tiến trình con gọi là Worker Process để xử lý các request này.

![image](https://user-images.githubusercontent.com/62273292/159424748-dd3f3a3a-8fad-4054-a4c1-14f2e07751fe.png)

Để định nghĩa cho các Worker Process này, chúng ta cần sử dụng tệp tin cấu hình để xác định số tiến trình, số lượng kết nối , tài khoản và nhóm tài khoản mà mỗi Worker Process chạy

## Cấu hình Http trong Nginx

1, Giới thiệu module Http trong Nginx

Module HTTP Core là thành phần chứa tất cả các khối, chỉ thị và các biến cơ bản của máy chủ HTTP. Mặc định module này được cài đặt trong khi biên dịch, nhưng không được bật lên khi Nginx chạy, việc sử dụng module này là không bắt buộc

Module này là 1 trong những module tiêu chuẩn lớn nhất của Nginx – nó cung cấp 1 số lượng lớn các chỉ thị và biến. Để có thể hiểu được tất cả các yếu tố này và vai trò của chúng, chúng ta sẽ bắt tay vào tìm hiểu 3 khối chỉ thị chính – `http`, `server` và `location`.

`http` : được khai báo ở phần đầu của tập tin cấu hình. Nó cho phép chúng ta định nghĩa các chỉ thị và các khối từ tất cả các module liên quan đến khía cạnh HTTP của Nginx. Khối chỉ thị này có thể được khai báo nhiều lần trong tập tin cấu hình, và các giá trị chỉ thị được chèn trong khối http sau sẽ ghi đè lên các chỉ thị nằm trong khối http trước đó

`server` : khối này cho phép chúng ta khai báo 1 website. Nói cách khác, 1 website cụ thể (được nhận diện bởi 1 hoặc nhiều hostname) được thừa nhận bới Nginx và nhận cấu hình của chính nó. Khối này chỉ có thể được dùng bên trong khối http.

`location` : cho phép chúng ta định nghĩa 1 nhóm các thiết lập được áp dụng cho 1 vị trí cụ thể trên website (thể hiện qua URL của website đó). Khối location có thể được dùng bên trong 1 khối server hoặc nằm chồng bên trong 1 khối location khác.

![image](https://user-images.githubusercontent.com/62273292/159425472-19733e1a-177a-4666-9ee8-0294127dc0d1.png)















