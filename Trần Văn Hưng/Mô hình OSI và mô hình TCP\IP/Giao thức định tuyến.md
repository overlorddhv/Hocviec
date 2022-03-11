# Định tuyến là gì?

Định tuyến là quá trình xác định đường đi tốt nhất trên một mạng máy tính để gói tin tới được đích theo một số thủ tục nhất định nào đó thông qua các nút trung gian là các bộ định tuyến router. Thông tin về những con đường này có thể được cập nhật tự động từ các router khác hoặc là do người quản trị mạng chỉ định cho router. Sau khi Router nhận gói tin, thì Router sẽ gỡ bỏ phần header lớp 2 để tìm địa chỉ đích thuộc lớp 3. Sau khi đọc xong địa chỉ đích lớp 3 nó tìm kiếm trong Routing Table cho mạng chứa địa chỉ đích. Để truyền được gói tin đến đích thì các router cần phải được cấu hình một bảng định tuyến (Routing Table) và giao thức định tuyến (Routing Protocol). Bảng định tuyến là bảng chứa tất cả những đường đi tốt nhất đến một đích nào đó tính từ router. Khi cần chuyển tiếp một gói tin, router sẽ xem địa chỉ đích của gói tin, sau đó tra bảng định tuyến và chuyển gói tin đi theo đường tốt nhất tìm được trong bảng. Trong bảng định tuyến có thể bao gồm một tuyến mặc định, được biểu diễn bằng địa chỉ 0.0.0.0 0.0.0.0.

Bảng định tuyến của mỗi giao thức định tuyến là khác nhau, nhưng có thể bao gồm những thông tin sau:

- Địa chỉ đích của mạng, mạng con hoặc hệ thống.

- Địa chỉ IP của router chặng kế tiếp phải đến.

- Giao tiếp vật lí phải sử dụng để đi đến Router kế tiếp.

- Subnet mask của địa chỉ đích.

- Khoảng cách đến đích (ví dụ: số lượng chặng để đến đích).

- Thời gian (tính theo giây) từ khi Router cập nhật lần cuối.

Giao thức định tuyến là ngôn ngữ giao tiếp giữa các router. Một giao thức định tuyến cho phép các router chia sẻ thông tin về các network, router sử dụng các thông tin này để xây dựng và duy trì bảng định tuyến.

# Phân loại định tuyến

Có nhiều tiêu chí để phân loại các giao thức định tuyến khác nhau. Định tuyến được phân chia thành 2 loại cơ bản:

- Định tuyến tĩnh: Việc xây dựng bảng định tuyến của router được thực hiện bằng tay bởi người quản trị.

- Định tuyến động: Việc xây dựng và duy trì trạng thái của bảng định tuyến được thực hiện tự động bởi router.

Việc chọn đường đi được tuân thủ theo 2 thuật toán cơ bản:

+ Distance vector: Chọn đường đi theo hướng và khoảng cách tới đích.

+ Link State: Chọn đường đi ngắn nhất dựa vào cấu trúc của toàn bộ mạng theo trạng thái của các đường liên kết mạng.

![image](https://user-images.githubusercontent.com/55913475/157820356-e28d7b1e-82cc-48c1-9cfc-111782e21081.png)

Khi chọn lựa một giao thức định tuyến động cần cân nhắc một số yếu tố như: độ lớn của hệ thống mạng, băng thông các đường truyền, khả năng của router, loại router và phiên bản router, các giao thức đang chạy trong hệ thống mạng.

# Các giao thức định tuyến

**RIP (Routing Information Protocol)**
- RIP là một giao thức IGP để phân phối thông tin định tuyến giữa các router bên trong một AS
- RIP là một giao thức định tuyến vecto khoảng cách
- Mỗi router khởi tạo bảng định tuyến với một danh sách các kết nối trực tiếp với các router gần nhất.
- Mỗi router sẽ flood bảng định tuyến của nó trên toàn AS
- Khi một router nhận được một thông tin từ router khác, nó sẽ update bảng định tuyến của mình để cuối cùng nó đảm bảo rằng có thể biết được tất cả các router khác.
- Trong bảng định tuyến của router, mỗi đích đến có một thuộc tính gọi là metric cost, đó là khoảng cách vecto từ router đến đích.
- Nếu một router có thể chọn nhiều hop để gửi data tới đích, nó sẽ quyết định chọn một hop dựa vào so sánh các metric phải trả khi gửi data.

**IGRP (Interior Gateway Routing Protocol)**
IGRP là giao thức định tuyến dạng classful, nghĩa là không chứa subnet mask trong các thông tin cập nhật định tuyến (routing update). Do không có khả năng mang các thông tin update nên dẫn đến có một vài hạn chế trong các thiết kế mạng dùng giao thức này. Các giao thức nhóm classful gồm RIPv1 và IGRP. Các đặc điểm của một giao thức classful gồm
- Thực hiện quá trình summary ở ranh giới các mạng
- Các routes được trao đổi giữa các mạng được summary theo địa chỉ của IANA.
- Bên trong một network, các lớp mạng con trao đổi với nhau bởi router mà không cần giá trị mask. Do đó giá trị subnet mask phải có cùng giá trị cho tất cả các interface trong cùng mạng.
Nếu có một entry trong bảng định tuyến cho một subnet cụ thể, gói IP sẽ được chuyển về địa chỉ đích đó. Nếu địa chỉ đích là không biết, datagram sẽ bị drop. Nếu ta có cấu hình default-network cho router, default network sẽ được dùng. Tuy nhiên default-network chỉ được dùng trong classful routing nếu router không có kiến thức về mạng đíc ở bất kỳ mức nào. Như vậy nếu major network là biết, gói IP sẽ bị drop cho dù có một mạng default network.
Ở chế độ mặc định, IGRP tính toán metric dựa trên các thông số băng thông (bandwidth) và độ trễ (delay). IGRP có thời gian cập nhật dài hơn RIP, có khả năng hỗ trợ cân bằng tải với metric không bằng nhau. IGRP không hỗ trợ discontiguous network, VLSM.

**EIGRP (Enhanced Interior Gateway Routing Protocol)**
EIGRP là giao thức định tuyến dạng lai giữa distance vector và link state. EIGRP là một phát triển riêng của Cisco nhằm khắc phục các nhược điểm của RIP/IGRP và có những ưu điểm như dễ cấu hình, độ hội tụ nhanh, tiết kiệm tài nguyên mạng khi trao đổi thông tin, sử dụng địa chỉ multicast để liên lạc, khả năng sử dụng hiệu quả băng thông, hỗ trợ VLSM và vấn đề mạng không liên tục (discontiguous network).
Các giao thức định tuyến nhóm classless được thiết kế để khắc phục các hạn chế của định tuyến classful, trong đó bao gồm các đặc điểm sau:
- Không gian địa chỉ được sử dụng hiệu quả
- Hỗ trợ VLSM. Các cổng của router trong cùng một network có thể có các giá trị subnet mask khác nhau
- Hỗ trợ cho việc sử dụng CIDR
- Các route có thể được summary.
EIGRP và IGRP có cùng cách tính metric, tuy nhiên metric của EIGRP bằng metric của IGRP nhân với 256 do IGRP có trường metric là 24 bit trong khi EIGRP có trường metric là 32 bit:
EIGRP Metric = IGRP Metric * 256

**OSPF (Open Shortest Path First)**
- OSPF là giao thức IGP để phân phối các thông tin định tuyến bên trong một mạng AS. OSPF là một giao thức định tuyến trạng thái liên kết.
- Thông tin của topo mạng sẽ được các router tính toán chọn đường đi tốt nhất để gửi data đến đích, thường dựa vào thuật toán Dijkstra.
- Thuận lợi chính của giao thức trạng thái liên kết là các router biết được các thông tin về topo mạng, nên nó có thể tính toán được đường đi tốt nhất mà thõa mãn các yêu cầu đặc biệt.
- Bất lợi của nó là nếu có thêm các router của mạng thì sẽ làm tăng lên số lượng và tần số của bảng tin update và cũng kéo dài thời gian tính toán chọn đường.

**BGP (Border Gateway Protocol)**
- BGP là một giao thức EGP được thiết kết để phân phối thông tin định tuyến giữa các AS.
- BGP là một giao thức định tuyến vecto khoảng cách.
- Bảng định tuyến chứa tất cả các đích mà router biết và địa chỉ hop tiếp theo mà router phải gửi để đến đích cũng như metric cost của con đường đó.
- Nếu một router có thể chọn nhiều hop để gửi data tới đích, nó sẽ quyết định chọn một hop dựa vào so sánh các metric phải trả khi gửi data.

# Lệnh cấu hình các giao thức định tuyến cơ bản

**1. RIP v2**

`router(config)#router rip`

 `router (config-router)#ver 2`
 
 `router (config-router)#net ip-add (major network)`
 
 `router (config-router)#no auto-summary`
 
 **2.OSPF**
 
 Note: Tất cả những router có cùng area phải cấu hình giống nhau tất cả các thông số thì khu vực đó mới hoạt động đúng chức năng được.

- Cấu hình cơ bản

`Router(config)#router ospf process ID (difference)`

`Router(config-router)#network ip-add Wildcard-mask area-ID`

- Cấu hình priority ở các interface để bầu DR và BDR

Priority càng lớn thì khả năng được bầu làm DR càng cao, ngược với bầu Root brige của Switch, càng nhỏ thì lại càng được bầu.

`Router(config)#interface fastethernet 0/0`

`Router(config-if)#ip ospf priority 55`

Sau khi cấu hình xong priority có thể kiểm tra bằng lệnh.

`Router# show ip ospf interface f0/0`

- Chỉnh sửa lại OSPF cost metric trong mỗi interface

Cost càng nhỏ thì tuyến đó càng được coi là best path

`Router(config-if)#ip ospf cost 1`

- Các lệnh show dùng để kiểm tra cấu hình OSPF

`show ip protocol`

`show ip route`

`show ip ospf`

`show ip ospf interface`

`show ip ospf database`

`show ip ospf neighbor detail`

`clear ip route *`

`debug ip ospf events`

`debug ip ospf ad`

**3. EIGRP**

- Cấu hình cơ bản.

`Router(config)#router eigrp As_id`

`Router(config-router)#network network number`

`Router(config-router)#no auto-summary`

- Thay đổi băng thông và tự tổng hợp tuyến trong interface

`Router(config-if)#bandwidth kilobits`

`Router(config-if)#ip summary-address protocol AS network number subnet mask`

- Cân bằng tải trong EIGRP

`Router(config-router)#variance number`

- Quảng bá default route

Cách 1:

`Router(config)#ip route 0.0.0.0 0.0.0.0 [interface/nexthop]`

`Router(config)#redistribute static`

Cách 2:

`Router(config)#ip default-network network number`

Cách 3:

`Router(config-if)#ip summary-network eigrp AS number 0.0.0.0 0.0.0.0`

- Quảng bá các tuyến khác trong EIGRP (không phải là default)

`Router(config-router)#redistribute protocol process ID metrics k1 k2 k3 k4 k5`

Ex: `Router(config-router)#redistribute ospf metrics 100 100 100 100 100`

- Chia sẻ traffic trong EIGRP

`Router(config-router)#traffic share {balanced/min}`

- Các lệnh kiểm tra cấu hình EIGRP

`show ip eigrp neighbor`

`show ip eigrp interface`

`show ip eigrp topology`

`show ip eigrp traffic`

`debug eigrp packet`

