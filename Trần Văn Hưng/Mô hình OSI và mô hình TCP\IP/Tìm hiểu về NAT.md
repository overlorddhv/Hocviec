# 1. NAT là gì?

NAT (Network Address Translation) là một kỹ thuật cho phép chuyển đổi từ một địa chỉ IP này thành một địa chỉ IP khác. Thông thường, NAT được dùng phổ biến trong mạng sử dụng địa chỉ cục bộ, cần truy cập đến mạng công cộng (Internet). Vị trí thực hiện NAT là router biên kết nối giữa hai mạng.

# 2. Cơ chế hoạt động của NAT

NAT sử dụng IP của chính nó làm IP công cộng cho mỗi máy con (client) với IP riêng. Khi một máy con thực hiện kết nối hoặc gửi dữ liệu tới một máy tính nào đó trên internet, dữ liệu sẽ được gửi tới NAT, sau đó NAT sẽ thay thế địa chỉ IP gốc của máy con đó rồi gửi gói dữ liệu đi với địa chỉ IP của NAT. Máy tính từ xa hoặc máy tính nào đó trên internet khi nhận được tín hiệu sẽ gửi gói tin trở về cho NAT computer bởi vì chúng nghĩ rằng NAT computer là máy đã gửi những gói dữ liệu đi. NAT ghi lại bảng thông tin của những máy tính đã gửi những gói tin đi ra ngoài trên mỗi cổng dịch vụ và gửi những gói tin nhận được về đúng máy tính đó (client).

# 3. Các loại NAT

**Static NAT(NAT tĩnh)**

NAT tĩnh hay còn gọi là Static NAT là phương thức NAT một đổi một. Nghĩa là một địa chỉ IP cố định trong LAN sẽ được ánh xạ ra một địa chỉ IP Public cố định trước khi gói tin đi ra Internet. Phương pháp này không nhằm tiết kiệm địa chỉ IP mà chỉ có mục đích ánh xạ một IP trong LAN ra một IP Public để ẩn IP nguồn trước khi đi ra Internet làm giảm nguy cơ bị tấn công trên mạng.

***Cấu hình Static NAT***

- Thiết lập mối quan hệ chuyển đổi giữa địa chỉ nội bộ bên trong và địa chỉ đại điện bên ngoài.

  `Router (config) # ip nat inside source static [local ip] [global ip]`

- Xác định các cổng kết nối vào mạng bên trong và thực hiện lệnh.

  `Router (config-if) # ip nat inside`

-Xác định các cổng kết nối ra mạng công cộng bên ngoài thực hiện lệnh.

  `Router (config-if) # ip nat outside.`

**Dynamic NAT(NAT động)**

Nat động (Dynamic NAT) là một giải pháp tiết kiệm IP Public cho NAT tĩnh. Thay vì ánh xạ từng IP cố định trong LAN ra từng IP Public cố định. LAN động cho phép NAT cả dải IP trong LAN ra một dải IP Public cố định ra bên ngoài.

***Cấu hình Dynamic NAT***

- Xác định dải địa chỉ đại diện bên ngoài (public):các địa chỉ NAT.

  `Router (config) # ip nat pool [name start ip] [name end ip] netmask [netmask]/prefix-lenght [prefix-lenght]`

- Thiết lập ACL cho phép những địa chỉ nội bộ bên trong nào được chuyển đổi: các địa chỉ được NAT.

  `Router (config) # access-list [access-list-number-permit] source [source-wildcard]`

- Thiết lập mối quan hệ giữa địa chỉ nguồn đã được xác định trong ACL với dải địa chỉ đại diện ra bên ngoài.

  `Router (config) # ip nat inside source list <acl-number> pool <name>`

- Xác định các cổng kết nối vào mạng nội bộ.

  `Router (config-if) # ip nat inside`

- Xác định các cổng kết nối ra bên ngoài.

  `Router (config-if) # ip nat outside`

**NAT Overload**

NAT Overload là một dạng của Dynamic NAT, nó thực hiện ánh xạ nhiều địa chỉ IP thành một địa chỉ (many – to – one) và sử dụng các địa chỉ số cổng khác nhau để phân biệt cho từng chuyển đổi. NAT Overload còn có tên gọi là PAT (Port Address Translation). Chỉ số cổng được mã hóa 16 bit, do đó có tới 65536 địa chỉ nội bộ có thể được chuyển đổi sang một địa chỉ công cộng.

***Cấu hình Overload***

- Xác định dãy địa chỉ bên trong cần chuyển dịch ra ngoài (private ip addresses range)

  `Router (config) # access-list <ACL-number> permit <source> <wildcard>`

- Cấu hình chuyển đổi địa chỉ IP sang cổng nối ra ngoài

  `Router (config) # ip nat inside source list <ACL-number> interface <interface> overload`

- Xác định các cổng nối vào mạng bên trong và nối ra mạng bên ngoài

Đối với các cổng nối vào mạng bên trong:
  
  `Router (config-if) # ip nat inside`

Đối với nối ra mạng bên ngoài:

  `Router (config-if) # ip nat outside`
  
# 4. Chức năng của NAT

- Ban đầu, NAT được đưa ra nhằm giải quyết vấn đề thiếu hụt địa chỉ của IPv4 .
- NAT giúp chia sẻ kết nối Internet (hay 1 mạng khác) với nhiều máy trong LAN chỉ với 1 IP duy nhất.
- NAT che giấu IP bên trong LAN
- NAT giúp quản trị mạng lọc các gói tin được gửi đến hay gửi từ một địa chỉ IP và cho phép hay cấm truy cập đến một port cụ thể.

# 5. Các vấn đề an ninh và quản trị mạng

Dynamic NAT (NAT động) tự động tạo ra một bức tường lửa giữa mạng nội bộ và mạng bên ngoài, hoặc giữa các mạng nội bộ của bạn và Internet. NAT chỉ cho phép các kết nối có nguồn gốc bên trong Stub Domain. Về cơ bản, điều này có nghĩa là một máy tính nằm ở mạng ngoài không thể kết nối với máy tính của bạn, trừ khi máy tính của bạn đã kết nối với máy tính đó trước. Bạn có thể duyệt Internet và kết nối đến một trang web, hoặc thậm chí là download một file tin; nhưng người khác không thể sử dụng các địa chỉ IP của bạn để kết nối tới một Port (cổng) trên máy tính của bạn.

Trong những trường hợp cụ thể, Static NAT (NAT tĩnh) cũng cho phép các thiết bị bên ngoài khởi tạo kết nối đến các máy tính trên Stub Domain. Một số NAT Router cung cấp bộ lọc và traffic logging. Bộ lọc cho phép công ty của bạn kiểm soát những trang mà nhân viên truy cập vào trên trang Web để ngăn chặn họ xem được những tài liệu quan trọng. Bạn có thể sử dụng traffic logging để tạo ra một tập tin nhật ký những trang web được truy cập và tạo ra các báo cáo khác nhau.

NAT đôi khi bị nhầm lẫn với các máy chủ proxy, nhưng giữa NAT và máy chủ proxy có sự khác biệt nhất định. NAT không thể nhầm lẫn được với các máy tính nguồn và máy tính đích, NAT giống như một thiết bị thứ ba. Còn một máy chủ proxy có thể bị nhầm lẫn. Máy tính nguồn biết rằng nó thực hiện một yêu cầu đến máy chủ proxy và phải được cấu hình để thực hiện yêu cầu đó. Máy tính đích sẽ hiểu rằng các máy chủ proxy là máy tính nguồn, và giao dịch với nó trực tiếp.

Ngoài ra, máy chủ proxy thường làm việc ở tầng 4 (Transport) trong mô hình OSI Reference Model hoặc cao hơn, trong khi NAT làm việc ở tầng 3 giao thức liên mạng (Network protocol). Khi làm việc tại một tầng cao hơn khiến các máy chủ proxy hoạt động chậm hơn so với các thiết bị NAT. Lợi ích lớn nhất của NAT đó là quản trị mạng (Network Administation) một cách rõ ràng. Ví dụ, bạn có thể di chuyển máy chủ Web của bạn hoặc máy chủ FTP tới máy tính chủ khác mà không cần phải lo lắng các liên kết bị hỏng. Đơn giản chỉ cần thay đổi, sử dụng Inbound Route Map để phản hồi máy chủ mới. Bạn cũng có thể thay đổi mạng nội bộ (Internal Network) một cách dễ dàng, bởi vì chỉ có địa chỉ IP bên ngoài hoặc địa chỉ IP của Router hoặc địa chỉ IP trong nhóm địa chỉ Global Address.

NAT và DHCP (dynamic host configuration protocol - giao thức cấu hình Host động). Bạn có thể chọn một loạt các địa chỉ IP Private trên Stub Domain và có máy chủ DHCP phát những địa chỉ IP này khi cần thiết.
