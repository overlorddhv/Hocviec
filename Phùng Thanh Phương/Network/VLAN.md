**1. VLAN là gì?**

VLAN là viết tắt của Virtual Local Area Network hoặc Virtual LAN, có nghĩa là Mạng cục bộ ảo” hoặc “Mạng LAN ảo”. VLAN là một mạng tùy chỉnh được tạo từ một hoặc nhiều mạng LAN hiện có. Nó cho phép các nhóm thiết bị từ nhiều mạng (cả có dây và không dây ) được kết hợp thành một mạng logic duy nhất. Kết quả là một mạng LAN ảo có thể được quản lý giống như một mạng cục bộ vật lý. Việc tạo lập nhiều mạng LAN ảo trong cùng một mạng cục bộ ( giữa các khoa trong một trường học, giữa các cục trong một công ty,...) giúp giảm thiểu vùng quảng bá (broadcast domain) cũng như tạo thuận lợi cho việc quản lý một mạng cục bộ rộng lớn.

Với mạng LAN thông thường, các máy tính trong cùng một địa điểm (cùng phòng,..) có thể được kết nối với nhau thành một mạng LAN., chỉ sử dụng một thiết bị tập trung như hub hay switch. Có nhiều mạng LAN khác nhau cần rất nhiều bộ hub, swtich. Tuy nhiên thực tế số lượng máy tính trong một LAN thường không nhiều, ngoài ra nhiều máy tính cùng một địa điểm (cùng phòng) có thể thuộc nhiều LAN khác nhau vì vậy càng tốn nhiều bộ hub, switch khác nhau. Do đó vừa tốn tài nguyên số lượng hub, switch và lãng phí số lượng port Ethernet.

Với nhu cầu tiết kiệm tài nguyên đồng thời đáp ứng nhu cầu sử dụng nhiều LAN trong cùng một địa điểm, giải pháp đưa ra là nhóm các máy tính thuộc các LAN khác nhau vào cùng một bộ tập trung switch. Giải pháp này gọi là mạng LAN ảo hay VLAN.

![image](https://user-images.githubusercontent.com/48250210/157635234-009f04a5-1d14-4d94-8084-f55beb043638.png)

Hiện nay, VLAN đóng một vai trò rất quan trọng trong công nghệ mạng LAN. Để thấy rõ được lợi ích của VLAN, chúng ta hãy xét trường hợp sau:

Giả sử, một công ty có 3 bộ phận là: Engineering, Marketing, Accounting, mỗi bộ phận trên lại trải ra trên 3 tầng. Để kết nối các máy tính trong một bộ phận với nhau thì ta có thể lắp đặt cho mỗi tầng một switch. Điều đó có nghĩa là mỗi tầng phải dùng 3 switch cho 3 bộ phận, nên để kết nối 3 tầng trong công ty cần phải sử dụng 9 switch => rất tốn kém và không thể tận dụng hết số port vốn có của 1 switch. Vì vậy, giải pháp VLAN ra đời nhằm giải quyết vấn đề trên một cách đơn giản và vẫn tiết kiệm được tài nguyên.

![image](https://user-images.githubusercontent.com/48250210/157639138-8e653ae5-8ef3-4d65-be42-82f865e67383.png)

Như hình vẽ ta thấy, mỗi tầng của công ty chỉ cần dùng 1 switch, và switch này được chia VLAN. Các máy tính ở bộ phận Engineering thì sẽ được gán vào VLAN Engineering, các PC ở bộ phận khác cũng được gán vào các VLAN tương ứng là Marketing và Accounting. Cách làm trên giúp ta có thể tiết kiệm tối đa số switch phải sử dụng đồng thời tận dụng được hết số cổng sẵn có của switch.

**2. Phân loại**

Có 3 loại VLAN, bao gồm:
* VLAN dựa trên cổng (port based VLAN): mỗi cổng (ethernet hoặc Fast ethernet) được gắn vợi một VLAN xác định. Do đó mỗi máy tính/thiết bị host kết nối với một cổng của switch đều thuộc một VLAN nào đó. Đây là cách cấu hình VLAN đơn giản và phổ biến nhất.
* VLAN dựa trên địa chỉ vật lý MAC (MAC address based VLAN): mỗi địa chỉ MAC được gắn tới một VLAN nhất định. Cách cấu hình này rất phức tạp và khó quản lý. 
* VLAN dựa trên giao thức (protocol based VLAN): tương tự với VLAN dựa trên địa chỉ MAC nhưng sử dụng địa chỉ IP thay cho địa chỉ MAC. Cách cấu hình này không được thông dụng

**3. Ưu điểm của VLAN**

* Tiết kiệm băng thông của hệ thống mạng: VLAN chia mạng LAN thành nhiều đoạn (segment) nhỏ, mỗi đoạn đó là một vùng quảng bá (broadcast domain). Khi có gói tin quảng bá (broadcast), nó sẽ được truyền duy nhất trong VLAN tương ứng. Do đó việc chia VLAN giúp tiết kiệm băng thông của hệ thống.
* Tăng khả năng bảo mật: do các thiết bị ở các VLAN khác nhau không thể truy nhập vào nhau (trừ khi sử dụng router nối giữa các VLAN). Như trong ví dụ trên, các máy tính trong VLAN Accounting chỉ có thể liên lạc được với nhau. máy ở VLAN Accounting không thể kết nối được với máy tính ở VLAN Engineering.
* Dễ dàng thêm/bớt máy tính vào VLAN: việc thêm một máy tính vào  VLAN rất đơn giản, chỉ cần cấu hình cổng cho máy đó vào VLAN mong muốn
* Giúp mạng có tính linh động cao: VLAN có thể dễ dàng di chuyển thiết bị. Giả sử trong ví dụ trên, sau một thời gian sử dụng, công ty quyết định để mỗi bộ phận một tầng riêng biệt. Với VLAN, ta chỉ cần cấu hình lại các cổng switch rồi đặt chúng vào VLAN theo yêu cầu. 
VLAN có thể được cấu hình tĩnh hay động. Trong cấu hình tĩnh, người quản trị mạng phải cấu hình cho từng cổng của mỗi switch. Sau đó, gán cho nó vào một VLAN nào đó. Trong cấu hình động, mỗi cổng của switch có thể tự cấu hình VLAN cho mình dựa trên địa chỉ MAC của thiết bị đã kết nối vào.

**4. Cấu trúc hoạt động của VLAN**

Cấu trúc của một mạng các VLAN gồm 3 tầng thiết bị như sau
* Tầng 1: là router làm nhiệm vụ định tuyến giữa các VLAN
* Tầng 2: là các switch. trên các cổng của mỗi switch chia thành các VLAN
* Tầng 3: là các workstation

Ký hiệu T: là đường Trunk

![image](https://user-images.githubusercontent.com/48250210/157784138-93b8f570-38e3-4c4e-a226-d0c4432aee1a.png)

**4.1. Cách thức tạo lập VLAN

Mỗi một cổng trên switch có thể chia cho một VLAN. Những cổng được chia sẻ cho cùng một VLAN thì chia sẻ broadcast. Cổng nào không thuộc VLAN thì sẽ không chia sẻ broadcast. Những cải tiến của VLAN là làm giảm bớt broadcast và sự lãng phí băng thông.

Có 2 phương thức để tạo lập VLAN:
- VLAN tĩnh (static VLAN)
- VLAN động (dynamic VLAN)

**4.1.1. Static VLAN

Phương thức này được ám chỉ như là port-base membership. Việc gán các cổng switch vào một VLAN là đã tạo một static VLAN. Giống như một thiết bị được kết nối  vào mạng, nó tự động thừa nhận VLAN của cổng đó. Nếu user thay đổi các cổng và cần truy cập vào cùng một VLAN thì người quản trị mạng cần phải khai báo cổng tới VLAN cho kết nối tới.

**4.1.2. Dynamic VLAN

VLAN được tạo thông qua việc sử dụng các phần mềm như Ciscowork 2000. Với một VMMPS (VLAN Management Policy Server) có thể đăng ký các cổng của switch vào các VLAN một cách tự động dựa trên địa chỉ MAC nguồn của thiết bị được nối vào cổng. Dynamic VLAN hiện thời tính đến thành viên của nó dựa trên địa chỉ MAC của thiết bị. Như một thiết bị trong mạng, nó truy vấn một cơ sở dữ liệu trên VMPS của các VLAN thành viên.

Trên switch cổng được gán cho một VLAN cụ thể thì độc lập với user hoặc hệ thống gắn với cổng đó. CÓ nghĩa là tất cả các user nằm trên các cổng nên là thành viên của cùng 1 VLAN. Một workstation hay một hub có thể kết nối vào một cổng VLAN. người quản trị mạng thực hiện gán các VLAN. Cổng mà được cấu hình là static thì không thể thay đổi  một cách tự động tới VLAN khác khu mà cấu hình lại switch.

Khi các user gắn với cùng một phân đoạn mạng chia sẻ, tất cả các user đó cùng chia sẻ băng thông của phân đoạn mạng. Mỗi một user được gắn vào môi trường chia sẻ, tất cả các user đó cùng chia sẻ băng thông của phân đoạn mạng. Mỗi một user được gắn vào môi trường chia sẻ, thì sẽ có ít băng thông sẵn có cho mỗi user, bởi tất cả các user đều nằm trên một miền xung đột. Nếu chia sẻ trở nên quá lớn, xung đột có thể xảy rả quá mức và các trình ứng dụng có thể bị mất chất lượng.

Các switch làm giảm xung đột bằng cách cung cấp băng thông giữa các thiết bị sử dụng Micro segmentation (vi phân đoạn), tuy nhiên các switch chỉ chuyển các gói tịn dạng ARP ( Address Resolution Protocol - Giao thức độ phân giải địa chỉ
