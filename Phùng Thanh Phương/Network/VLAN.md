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

**4.1. Cách thức tạo lập VLAN**

Mỗi một cổng trên switch có thể chia cho một VLAN. Những cổng được chia sẻ cho cùng một VLAN thì chia sẻ broadcast. Cổng nào không thuộc VLAN thì sẽ không chia sẻ broadcast. Những cải tiến của VLAN là làm giảm bớt broadcast và sự lãng phí băng thông.

Có 2 phương thức để tạo lập VLAN:
- VLAN tĩnh (static VLAN)
- VLAN động (dynamic VLAN)

**4.1.1. Static VLAN**

Phương thức này được ám chỉ như là port-base membership. Việc gán các cổng switch vào một VLAN là đã tạo một static VLAN. Giống như một thiết bị được kết nối  vào mạng, nó tự động thừa nhận VLAN của cổng đó. Nếu user thay đổi các cổng và cần truy cập vào cùng một VLAN thì người quản trị mạng cần phải khai báo cổng tới VLAN cho kết nối tới.

**4.1.2. Dynamic VLAN**

VLAN được tạo thông qua việc sử dụng các phần mềm như Ciscowork 2000. Với một VMMPS (VLAN Management Policy Server) có thể đăng ký các cổng của switch vào các VLAN một cách tự động dựa trên địa chỉ MAC nguồn của thiết bị được nối vào cổng. Dynamic VLAN hiện thời tính đến thành viên của nó dựa trên địa chỉ MAC của thiết bị. Như một thiết bị trong mạng, nó truy vấn một cơ sở dữ liệu trên VMPS của các VLAN thành viên.

Trên switch cổng được gán cho một VLAN cụ thể thì độc lập với user hoặc hệ thống gắn với cổng đó. CÓ nghĩa là tất cả các user nằm trên các cổng nên là thành viên của cùng 1 VLAN. Một workstation hay một hub có thể kết nối vào một cổng VLAN. người quản trị mạng thực hiện gán các VLAN. Cổng mà được cấu hình là static thì không thể thay đổi  một cách tự động tới VLAN khác khu mà cấu hình lại switch.

Khi các user gắn với cùng một phân đoạn mạng chia sẻ, tất cả các user đó cùng chia sẻ băng thông của phân đoạn mạng. Mỗi một user được gắn vào môi trường chia sẻ, tất cả các user đó cùng chia sẻ băng thông của phân đoạn mạng. Mỗi một user được gắn vào môi trường chia sẻ, thì sẽ có ít băng thông sẵn có cho mỗi user, bởi tất cả các user đều nằm trên một miền xung đột. Nếu chia sẻ trở nên quá lớn, xung đột có thể xảy rả quá mức và các trình ứng dụng có thể bị mất chất lượng.

Các switch làm giảm xung đột bằng cách cung cấp băng thông giữa các thiết bị sử dụng Micro segmentation (vi phân đoạn), tuy nhiên các switch chỉ chuyển các gói tịn dạng ARP ( Address Resolution Protocol - Giao thức độ phân giải địa chỉ). VLAN đưa ra nhiều băng thông hơn cho user trong một mạng chia sẻ bằng cách hạn chế miền quảng bá cụ thể.

VLAN mặc định cho tất cả các cổng trên switch là VLAN1 hoặc management VLAN. VLAN mặc định không thể xóa, tuy nhiên các VLAN thêm vào có thể tạo ra và các cổng có thể gán lại tới các VLAN xen kẽ. Mỗi một cổng giao diện trên switch giống như cổng của bridge và switch đơn giản là một bridge nhiều cổng. Các bridge lọc tải mạng mà không cần quan tâm đến phân đoạn mạng nguồn mà chỉ cần quan tâm đến phân đoạn mạng đích. Nếu một frame cần chuyển qua bridge, và địa chỉ MAC đích là biết được, thì bridge sẽ chuyển frame tới cổng giao diện chính xác. Nếu bridge hoặc switch không biết đích đến, nó sẽ chuyển gói tin qua tất cả các cổng trong vùng quảng bá (VLAN) trừ cổng nguồn. Mỗi một VLAN nên có một địa chỉ lớp 3 duy nhất hoặc địa chỉ subnet được đăng ký. Điều đó giúp router chuyển mạch gói giữa các VLAN. Các VLAN có thể tồn tại như các mạng end-to-end

**4.2. End-to-End VLAN (VLAN đầu cuối)**

Các End-to-End VLAN cho phép các thiết bị trong một nhóm sử dụng chung tài nguyên. Bao gồm các thông số như server lưu trữ, nhóm dự án và các phòng ban. Mục đích của các End-to-End VLAN là duy trì 80% thông lượng trên VLAN hiện thời. Một End-to-End VLAN có các đặc điểm sau:
* Các user được nhóm vào các VLAN độc lập về vị trí vật lý nhưng lại phụ thuộc vào nhóm chức năng hoặc đặc thù công việc.
* Tất cả các user trong một VLAN nên có cùng kiểu truyền dữ liệu 80/20 (80% băng thông cho VLAN và 20% băng thông cho các truy cập từ xa).
* Như một user di chuyển trong một khuôn viên mạng, VLAN dành cho user đó không nên thay đổi.
* Mỗi VLAN có những bảo mật riêng cho từng thành viên. 

Như vật, trong End-to-End VLAN, các user sẽ được nhóm vào thành những nhóm dựa trên chức năng, theo nhóm dự án hoặc theo cách mà những người dùng đó sử dụng tài nguyên mạng

**4.3. Geographic VLANs ( các VLAN cục bộ)**

Nhiều hệ thống mạng mà cần có sự di chuyển tới những nơi tập trung tài nguyên, End-to-End VLAN trở nên khó duy trì. Những user yêu cầu sử dụng nhiều nguồn tài nguyên khác nhau, nhiều trong số đó không còn ở trong VLAN của chúng nữa. Bởi sự thay đổi về địa điểm và cách sử dụng tài nguyên. Các VLAN được tạo ra xung quanh các giới hạn địa lý hơn là giới hạn thông thường.

Vị trí địa lý có thể rộng như toàn bộ một tòa nhà, hoặc cũng có thể nhỏ như một switch trong một wiring closet (tủ dây điện). Trong một số cấu trúc VLAN cục bộ, đó là một cách để tìm ra nguyên tắc 20/80 trong hiệu quả với 80% của thông lượng truy cập từ xa và 20% thông lượng hiện thời tới user. Điều này trái ngược với End-to-End VLAN. Mặc dù hình thái mạng này user phải đi qua thiết bị lớp 3 để đạt được 80% tài nguyên khai thác. Thiết kế này cho phép cung cấp cho một dự định, một phương thức chắc chắn của việc xác nhận tài nguyên.

**4.4. Nhận dạng VLAN Frame**

![image](https://user-images.githubusercontent.com/48250210/157790183-0d08cdc8-3a92-455d-b1ef-e0efe1e68822.png)

Với các VLAN sử dụng nhiều switch, frame header được đóng gói hoặc sử dụng lại để phản hồi một VLAN Id trước khi Frame được gửi đi vào nốt kết giữa các switch. Trước khi chuyển gói tin đến điểm cuối, Frame header được thay đổi trở lại với định dạng ban đầu. VLAN nhận dạng bằng cách: gói tin nào thì thuộc VLAN đó. Phương thức đa mạch nối (Multiple trunking) tồn tại, bao gồm IEEE 802.1q, ISL, 802.10 và LANE.

**4.4.1. IEEE 802.1q: Frame tagging**

Giao thức này như là một phương thức chuẩn của IEEE để dành cho việc nhận dạng các VLAN bằng cách thêm vào Frame header đặc điểm của một VLAN. Phương thức này còn được gọi là gắn thẻ cho Frame (Frame tagging).

![image](https://user-images.githubusercontent.com/48250210/157791043-2eb28dc8-d728-4470-ac8a-104614621633.png)

Trong hình minh họa một định dạng Frame 802.1q với VLAN Id. mỗi một cổng 802.1q được gán cho một đường trunk và tất cả các cổng trên đường trunk để ở trong một Native VLAN. Mỗi cổng 802.1q được gán một giá trị nhận dạng đó là native VLAN Id (mặc định là VLAN 1). Tất cả các frame không được gắn thẻ được gán vào trong LAN cái mà theo lý thuyết là nằm trong tham số Id. Một đường trunk 802.1q được kết hợp các cổng trunk có một giá trị Native VLAN. Tuy nhiên các trạm làm việc thông thường có thể đọc được các Native Frame không gắn thẻ nhưng lại đọc được các Frame được gắn thẻ. IEEE 802.1q Frame tagging đã đưa ra một phương truyền thông VLAN giữa các switch.

**4.4.2. Inter-Switch Link Protocol**

ISL là một giao thức đóng gói của Cisco. Giao thức này dùng để đa liên kết các hệ thống đa switch, nó được hỗ trợ, tương thích trên switch cũng tốt như router.

![image](https://user-images.githubusercontent.com/48250210/157794971-6927cd95-ce87-4dce-b591-70d2a6378dcb.png)

Dòng switch Castalyst sử dụng ISL frame tagging là một kỹ thuật có độ trễ thấp, dùng cho việc dồn kênh từ nhiều VLAN trên một đường dây vật lý. ISL được thực thi cho kết nối giữa switch, router và NIC sử dụng trên các node như server. Để hỗ trợ chức năng ISL, các thiết bị kết nối phải được cấu hình ISL.

**4.5. Các kiểu VLAN**

* VLAN 1

Mặc định, các thiết bị lớp 2 sẽ sử dụng một VLAN mặc định để đưa tất cả các cổng của thiết bị đó vào. Thêm vào nữa là có rất nhiều giao thức lớp 2 như CDP, PAgP, và VTP cần phải được gửi tới một VLAN xác định trên các đường trunk. Chính vì các mục đích đó mà VLAN mặc định được chọn là VLAN 1.

CDP, PagP, VTP, và DTP luôn luôn được truyền qua VLAN 1 và mặc định này không thể thay đổi được. Các khuyến cáo của Cisco chỉ ra rằng VLAN 1 chỉ nên dành cho các giao thức kể trên.

* Default VLAN

VLAN 1 còn được gọi là default VLAN. Chính vì vậy, mặc định, native VLAN, management VLAN và user VLAN sẽ là thành viên của VLAN 1.

Tất cả các giao diện Ethernet trên switch Catalyst mặc định thuộc VLAN 1. Các thiết bị gắn với các giao diện đó sẽ là thành viên của VLAN 1, trừ khi các giao diện đó được cấu hình sang các VLAN khác.

* User VLANs

Hiểu đơn giản User VLAN là một VLAN được tạo ra nhằm tạo ra một nhóm người sử dụng mà không phụ thuộc vào vị trí địa lý hay logic và tách biệt với phần còn lại của mạng ban đầu. Câu lệnh switchport access vlan được dùng để chỉ định các giao diện vào các VLAN khác nhau.

* Native VLAN

Một chủ đề hay gây nhầm lẫn là Native VLAN. Native VLAN là một VLAN có các cổng được cấu hình trunk. Khi một cổng của switch được cấu hình trunk, trong phần tag của frame đi qua cổng đó sẽ được thêm một số hiệu VLAN thích hợp. Tất cả các frames thuộc các VLAN khi đi qua đường trunk sẽ được gắn thêm các tag của giao thức 802.1q và ISL, ngoại trừ các frame của VLAN 1. Như vậy, theo mặc định các frames của VLAN 1 khi đi qua đường trunk sẽ không được gắn tag.
Khả năng này cho phép các cổng hiểu 802.1Q giao tiếp được với các cổng cũ không hiểu 802.1Q bằng cách gửi và nhận trực tiếp các luồng dữ liệu không được gắn tag. Tuy nhiên, trong tất cả các trường hợp khác, điều này lại gây bất lợi, bởi vì các gói tin liên quan đến native VLAN sẽ bị mất tag.

Native VLAN được chuyển thành VLAN khác bằng câu lệnh: **Switch(config-if)#switchport trunk native vlan vlan-id**

* Management VLAN

Hiện nay, đa số các thiết bị như router, switch có thể truy cập từ xa bằng cách telnet đến địa chỉ IP của thiết bị. Đối với các thiết bị mà cho phép truy cập từ xa thì chúng ta nên đặt vào trong một VLAN, được gọi là Management VLAN. VLAN này độc lập với các VLAN khác như user VLAN, native VLAN. Do đó khi mạng có vấn đề như : hội tụ với STP, broadcast storms, thì một Management VLAN cho phép nhà quản trị vẫn có thể truy cập được vào các thiết bị và giải quyết các vấn đề đó.

Một yếu tố khác để tạo ra một Management VLAN độc lập với user VLAN là việc tách các thiết bị đáng tin cậy với các thiết bị không tin cậy. Do đó làm giảm đi khả năng các user khác đạt được quyền truy cập vào các thiết bị đó.

**5. Cách cấu hình VLAN**

**5.1. Tạo VLAN**

**Bước 1.** Đăng nhập vào tiện ích trên web và chọn đến phần VLAN Management > VLAN Settings.

**Bước 2.** Trong khu vực VLAN Table, bấm chuột vào Add để tạo một VLAN mới. Một cửa sổ sẽ xuất hiện.

**Bước 3.** VLAN có thể được thực hiện thêm vào theo hai phương thức khác nhau như được hiển thị bởi những tùy chọn bên dưới. Sau đó bạn hãy lựa chọn phương thức mong muốn.

**Bước 4.** Nếu bạn đã chọn VLAN ở bước 3 thì hãy nhập VLAN ID vào trường VLAN ID. Chú ý, phạm vi phải nằm trong khoảng từ 2 đến 4094.

**Bước 5.** Trong trường VLAN Name, bạn cần phải nhập tên cho VLAN. Ví dụ như: VLAN Name sẽ là Accounting, có tối đa 32 ký tự có thể được sử dụng.

**Bước 6.** Bạn tiếp tục chọn hộp kiểm VLAN Interface State để thực hiện kích hoạt trạng thái interface VLAN. Nó đã được tự động lựa chọn theo mặc định. Nếu không, mạng VLAN sẽ bị tắt và không có gì có thể được truyền hay nhận thông qua VLAN.

**Bước 7.** Tích chuột vào hộp kiểm Link Status SNMP Traps nếu như bạn muốn kích hoạt việc tạo SNMP trap.

**Bước 8.** Nếu bạn chọn Range ở trong bước 3, hãy nhập phạm vi cho các VLAN ở trong trường VLAN Range. Phạm vi đã có sẵn là 2 – 4094. Trong ví dụ này, VLAN Range sẽ là từ 3 đến 52.

**Lưu ý:** Có thể tạo được tối đa 100 VLAN cùng một lúc.

**Bước 9.** Bạn nhấn vào Apply để hoàn tất.

**5.2. Chỉnh sửa VLAN**

**Bước 1.** Đăng nhập vào tiện ích dựa trên trình duyệt web và lựa chọn VLAN Management > VLAN. Bạn hãy tìm đến trang VLAN thì mục Settings sẽ mở ra.

**Bước 2.** Chọn hộp kiểm bên cạnh VLAN nơi mà bạn muốn chỉnh sửa.

**Bước 3.** Nhấn Edit để thực hiện chỉnh sửa VLAN đã chọn. Cửa sổ Edit VLAN được xuất hiện.

**Bước 4.** Bạn có thể thay đổi VLAN hiện tại bằng cách dùng danh sách drop-down VLAN ID. Điều này được sử dụng để có thể nhanh chóng chuyển đổi giữa các VLAN bạn muốn cấu hình, mà không phải thực hiện quay lại trang VLAN Settings.

**Bước 5.** Chỉnh sửa tên của VLAN vào trong trường VLAN Name. Tên này sẽ không ảnh hưởng đến hiệu suất của VLAN và còn được sử dụng để nhận dạng dễ dàng.

**Bước 6.** Đánh dấu vào phần hộp kiểm VLAN Interface State để có thể kích hoạt trạng thái interface của VLAN. Nếu không thì VLAN sẽ bị tắt và không có gì có thể được truyền hoặc thực hiện nhận thông qua VLAN.

**Bước 7.** Tích chuột vào hộp kiểm Enable Link Status SNMP Traps để cho phép tạo SNMP trap với thông tin ở trạng thái liên kết. Hộp này sẽ được chọn theo mặc định.

**Bước 8.** Nhấn vào Apply để hoàn tất.

**5.3. Xóa cấu hình mạng VLAN**

**Bước 1.** Bạn hãy đăng nhập vào tiện ích dựa trên web và lựa chọn VLAN Management > VLAN Settings.

**Bước 2.** Chọn hộp kiểm bên cạnh VLAN mà bạn muốn xóa.

**Bước 3.** Nhấn Delete để thực hiện xóa VLAN đã chọn.

**6. Các giao thức trong VLAN**

**6.1. VLAN Trunking Protocol – Giao thức mạch nối các VLAN**

VTP (Vlan Trunking Protocol) là giao thức hoạt động ở tầng liên kết dữ liệu trong mô hình OSI. VTP giúp cho việc cấu hình VLAN luôn đồng nhất khi thêm, xóa, sửa thông tin về VLAN trong hệ thống mạng.

VTP gửi thông điệp quảng bá qua “VTP domain” mỗi 5 phút một lần, hoặc khi có sự thay đổi xảy ra trong quá trình cấu hình VLAN. Một thông điệp VTP bao gồm “rivision-number”, tên VLAN (VLAN name), số hiệu VLAN. Bằng sự cấu hình VTP Server và việc quảng bá thông tin VTP tất cả các switch đều đồng bộ về tên VLAN và số liệu VLAN của tất cả các VLAN.

Một trong những thành phần quan trọng trong các thông tin quảng bá VTP là tham số “revision-number”.  Mỗi thành phần VTP server điều chỉnh thông tin VLAN, nó tăng “revision-number” lên 1, rồi sau đó VTP Server mới gửi thông tin quảng bá VTP đi. Khi một switch nhận một thông điệp VTP với “revision-number” lớn hơn, nó sẽ cập nhật cấu hình VLAN.

![image](https://user-images.githubusercontent.com/48250210/157797779-ebe31d42-6176-4305-a7bd-91e4f2d39c0d.png)

VTP hoạt động ở một trong 3 cơ chế sau:
* Server
* Client
* Transparent

![image](https://user-images.githubusercontent.com/48250210/157797871-381a7917-8cd2-49fc-8c95-c671d5e3f8af.png)

Switch ở chế độ VTP Server có thể tạo, chỉnh sử và xóa VLAN. VTP server lưu cấu hình VLAN trong NVRAM của nó. VTP Server gửi thông điệp ra tất cả các cổng” trunk”.

Switch ở chế độ VTP client không tạo, sửa và xóa thông tin VLAN. VTP Client có chức năng đáp ứng theo mọi sự thay đổi của VLAN từ Server và gửi thông điệp ra tất cả các cổng “trunk” của nó. VTP Client đồng bộ cấu hình VLAN trong hệ thống.

Switch ở chế độ transparent sẽ nhận và chuyển tiếp các thông điệp quảng bá VTP do các switch khác gửi đến mà không quan tâm đến nội dung của các thông điệp này. Nếu “transparent switch” nhận thông tin cập nhật VTP nó cũng không cập nhật vào cơ sở dữ liệu của nó; đồng thời nếu cấu hình VLAN của nó có gì thay đổi, nó cũng không gửi thông tin cập nhật cho các switch khác. Trên “transparent switch” chỉ có một việc duy nhất là chuyển tiếp thông điệp VTP. Switch hoạt động ở “transparent-mode” chỉ có thể tạo ra các VLAN cục bộ. Các VLAN này sẽ không được quảng bá đến các switch khác.

**6.2. Inter VLAN Routing**

**6.2.1. Inter-VLAN**

Mỗi mạng có nhu cầu riêng của nó, tuy nhiên cho dù đó là một mạng lưới rộng lớn hay nhỏ, định tuyến nội bộ, trong hầu hết các trường hợp, là điều cần thiết. Khả năng để phân chia mạng bằng cách tạo ra VLANs, do đó giảm broadcasts mạng và tính bảo mật ngày càng tăng. Các thiết lập phổ biến bao gồm một broadcast domain riêng biệt cho các dịch vụ quan trọng ngày càng nhiều.

Vấn đề ở đây là làm thế nào có thể từ một trong những người sử dụng VLAN ( thuộc về 1 broadcast domain), sử dụng được các dịch vụ được cung cấp bởi một VLAN khác? Do vậy giải pháp định tuyến trên VLAN đã được đề cập đến.

Inter-VLAN là phương pháp được thiết lập có hiệu quả nhất bằng cách cung cấp một liên kết trunk duy nhất giữa Switch và Router mà có thể mang lưu lượng truy cập của nhiều VLAN và trong đó các lưu lượng ấy lần lượt có thể được định tuyến bởi Router.

Với Inter-VLAN Routing, Router nhận frame từ Switch với gói tin xuất phát từ một VLAN đã được tag. Nó liên kết các frame với các subinterface thích hợp và sau đó giải mã nội dung của frame (phần IP packet). Router sau đó thực hiện chức năng của Layer 3 dựa trên địa chỉ mạng đích có trong gói tin IP để xác định subinterface cần chuyển tiếp gói IP. Các IP packet bây giờ được đóng gói thành frame theo chuẩn dot1Q (hoặc ISL) để nhận dạng VLAN của subinterface chuyển tiếp và truyền đi trên đường trunk vào Switch.

**6.2.3. Cấu hình Inter-VLAN

a. Trên Switch

SW0(config)#vlan 10

SW0(config-vlan)#name IT

SW0(config-vlan)#vlan 20

SW0(config-vlan)#name sale

SW0(config-vlan)#exit

SW0(config)#interface range f0/1-10

SW0(config-if-range)#switchport access vlan 10

SW0(config-if-range)#exit

SW0(config)#interface range f0/11-20

SW0(config-if-range)#switchport access vlan 20

SW0(config-if-range)#exit

SW0(config)#interface range g1/1-2

SW0(config-if-range)#switchport mode trunk

SW0(config)#interface vlan 1

SW0(config)#no shutdown

SW0(config-if)#ip add 10.0.0.101 255.255.255.0

SW0(config-if)#end

SW0#write

b. Cấu hình định tuyến VLAN trên Router

R1(config)#int f0/0

R1(config-if)#no shut

R1(config)#int f0/0.10

R1(config-subif)#encapsulation dot1Q 10

R1(config-subif)#ip add 192.168.1.1 255.255.255.0

R1(config-subif)#exit

R1(config)#int f0/0.20

R1(config-subif)#encapsulation dot1Q 20

R1(config-subif)#ip add 192.168.2.1 255.255.255.0

R1(config-subif)#exit
