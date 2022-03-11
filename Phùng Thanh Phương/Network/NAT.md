# NAT (Network Address Translation)

**1. NAT (Network Address Translation) là gì?**

![image](https://user-images.githubusercontent.com/48250210/157799108-3f9812aa-fad1-44b4-82d3-4a44b70d71f8.png)

NAT là từ viết tắt của Network Address Translation. Đây là kỹ thuật để chuyển đổi từ địa chỉ IP này sang địa chỉ IP khác. 

NAT được sử dụng phổ biến trong các mạng dùng địa chỉ cục bộ để truy cập đến mạng công cộng (tức là Internet). Để nối kết 2 mạng này với nhau, router biên đóng vai trò là vị trí thực hiện NAT.

**2. Nhiệm vụ của NAT**

NAT giống như một Router, chuyển tiếp các gói tin giữa những lớp mạng khác nhau trên một mạng lớn. NAT dịch hay thay đổi một hoặc cả hai địa chỉ bên trong một gói tin khi gói tin đó đi qua một Router, hay một số thiết bị khác. Thông thường NAT thường thay đổi địa chỉ thường là địa chỉ riêng (IP Private) của một kết nối mạng thành địa chỉ công cộng (IP Public).

NAT cũng có thể coi như một Firewall (tường lửa) cơ bản. NAT duy trì một bảng thông tin về mỗi gói tin được gửi qua. Khi một máy tính trên mạng kết nối đến 1 website trên Internet header của địa chỉ IP nguồn được thay thế bằng địa chỉ Public đã được cấu hình sẵn trên NAT sever, sau khi có gói tin trở về NAT dựa vào bảng record mà nó đã lưu về các gói tin, thay đổi địa chỉ IP đích thành địa chỉ của PC trong mạng và chuyển tiếp đi. Thông qua cơ chế đó quản trị mạng có khả năng lọc các gói tin được gửi đến hay gửi từ một địa chỉ IP và cho phép hay ngăn truy cập đến một port cụ thể.
 
NAT Port giúp các dữ liệu dễ dàng đi qua các thiết bị mạng (router, moderm…) mà không bị tường lửa chặn. Điều này giúp đảm bảo tốc độ truy cập dữ liệu (download và upload), đáp ứng nhu cầu cho các ứng dụng game online, xem camera, utorrent, acestream...

**3. Ưu điểm của NAT**

NAT mang đến cho người dùng các ưu điểm sau:

* Tiết kiệm địa chỉ IPv4: Nguy cơ thiếu địa chỉ IPv4 càng tăng cao do lượng người dùng internet ngày càng nhiều. Vì thế, kỹ thuật NAT ra đời chính là giải pháp giúp giảm đáng kể số lượng IPv4 cần dùng. 
* Có khả năng che giấu địa chỉ IP trong mạng LAN
* Cách thức hoạt động của NAT là chia sẻ kết nối internet với nhiều thiết bị truy cập (máy tính, điện thoại di động) trong cùng một mạng LAN với duy nhất một địa chỉ IP public.

Nhờ thế, NAT cho phép quản trị viên có thể lọc tất cả các gói tin đến, đồng thời cấp quyền truy cập cho IP mạng công cộng đến một cổng bất kỳ. 

**4. Nhược điểm của NAT**

Song song với ưu điểm, NAT vẫn tồn tại một vài hạn chế như: 

* CPU tốn thời gian kiểm tra và đổi địa chỉ IP khi nó sử dụng kỹ thuật NAT. Do đó, quá trình switching sẽ bị tăng độ trễ và ảnh hưởng đến tốc độ truyền của mạng internet.
* Các kỹ thuật viên khó khăn trong việc kiểm tra nguồn gốc địa chỉ IP do NAT đã che giấu chúng. Thậm chí, họ cũng gặp không ít trở ngại khi tìm dấu viết của các gói tin.
* Vì khả năng giấu địa chỉ IP của NAT nên ngăn cản hoạt động của một số ứng dụng bắt buộc phải dùng IP.

**5. Phân loại NAT**

**5.1. Static NAT**

Đây là kỹ thuật được dùng để thay đổi, biến địa chỉ IP này thành địa chỉ IP khác, thông qua việc dùng một phương pháp cụ thể và cố định từ IP cục bộ sang IP Public. Tất cả quá trình này sẽ được thực hiện thủ công.

Static NAT cực kỳ hiệu quả nếu sử dụng các thiết bị có IP cố định để truy cập internet bên ngoài.

Cách cấu hình NAT như sau:

- Bước 1: Bạn thiết lập mối quan hệ để thực hiện chuyển đổi địa chỉ IP cục bộ và IP Public theo cú pháp:

Router (config) # ip nat inside source static [local ip] [global ip]

- Bước 2: Bạn tiến hành thiết lập cổng kết nối mạng nội bộ theo cú pháp:

Router (config-if) # ip nat inside

- Bước 3: Bạn thực hiện thiết lập cổng kết nối mạng bên ngoài theo cú pháp:

Router (config-if) # ip nat outside

**5.2. Dynamic NAT**

Kỹ thuật này được dùng để thực hiện ánh xạ tự động một địa chỉ IP sang địa chỉ IP khác (còn được gọi là (one to one)). Thông thường, nó sẽ chuyển IP mạng cục bộ sang IP đã được đăng ký hợp lệ.

Cách cấu hình NAT như sau:

- Bước 1: Bạn thiết lập IP của mạng bên ngoài theo cú pháp:

Router (config) # ip nat pool [name start ip] [name end ip] netmask [netmask]/prefix-lenght [prefix-lenght]

- Bước 2: Tiến hành tạo ACL để thiết lập danh sách địa chỉ IP mạng cục bộ có thể được chuyển đổi IP theo cú pháp:

Router (config) # access-list [access-list-number-permit] source [source-wildcard]

- Bước 3: Bạn xây dựng mối quan hệ của địa chỉ nguồn (đã thiết lập trong ACL) với IP hợp lệ của mạng bên ngoài theo cú pháp:

Router (config) # ip nat inside source list <acl-number> pool <name>

- Bước 4: Bạn thiết lập cổng kết nối mạng nội bộ theo cú pháp:

Router (config-if) # ip nat inside

- Bước 5: Bạn tiếp tục thiết lập cổng kết nối mạng bên ngoài theo cú pháp:

Router (config-if) # ip nat outside

**5.3. NAT Overload**

NAT Overload hay còn gọi là PAT (Port Address Translation). Nó chính là một dạng biến thể của Dynamic NAT. Vì thế, NAT Overload có khả năng thực hiện chuyển đổi địa chỉ IP tự động nhưng là chuyển đổi nhiều địa chỉ IP thành một IP, tức là dạng many to one. Đồng thời, nó sử dụng nhiều chỉ số port để phân biệt từng chuyển đổi.  

Cách cấu hình NAT Overload:

- Bước 1: Bạn xác định những địa chỉ IP mạng nội bộ cần ánh xạ theo cú pháp:

Router (config) # access-list <ACL-number> permit <source> <wildcard>

- Bước 2: Bạn thực hiện cấu hình để chuyển IP đến cổng kết nối mạng bên ngoài theo cú pháp:

Router (config) # ip nat inside source list <ACL-number> interface <interface> overload

- Bước 3: Bạn thiết lập các cổng kết nối mạng bên trong theo cú pháp:

Router (config-if) # ip nat inside

- Bước 4: Bạn thiết lập các cổng kết nối mạng bên ngoài theo cú pháp:

Router (config-if) # ip nat outside
