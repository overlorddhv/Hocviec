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





