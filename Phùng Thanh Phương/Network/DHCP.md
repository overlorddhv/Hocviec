**1. DHCP là gì?**

DHCP (Dynamic Host Configuration Protocol) hay DHCP còn gọi là giao thức cấu hình động máy chủ. DHCP có bản chất là một máy chủ mạng. Nó tự động cung cấp, gán địa chỉ IP, cổng mặc định và các thông số mạng khác cho các thiết bị client và các cấu hình liên quan khác như subnet mask và gateway mặc định.

DHCP cung cấp một database trung tâm để theo dõi tất cả các máy tính trong hệ thống mạng với mục đích quan trọng là tránh xảy ra trường hợp hai máy tính khác nhau lại có cùng địa chỉ IP. Một máy chủ DHCP tự động gửi các thông số mạng cần thiết đến khách hàng để có thể giao tiếp chính xác trên mạng.

Nếu không có DHCP, các máy tính có thể cấu hình IP thủ công (cấu hình IP tĩnh). Ngoài việc cung cấp IP, thì DHCP còn cung cấp các thông tin cụ thể như DNS. Hiện nay thì DHCP có 2 phiên bản là IPv4 và IPv6.

Một số thuật ngữ bạn cần biết khi tìm hiểu về DHCP:

* DHCP Client (Máy trạm DHCP): Là một thiết bị nối vào mạng và sử dụng DHCP để lấy các thông tin cấu hình như là địa chỉ mạng, địa chỉ máy chủ DNS.
* DHCP server (Máy chủ DHCP): Là một thiết bị nối vào mạng có chức năng trả về các thông tin cần thiết cho máy trạm DHCP khi có yêu cầu.
* Binding (kết nối): Là tập hợp các thông tin cấu hình trong đó có ít nhất một địa chỉ IP, được sử dụng bởi một DHCP Client và các kết nối được quản lý bởi DHCP.
* BOOTP relay agents (Thiết bị chuyển tiếp BOOTP): Là một máy trạm hoặc router có khả năng chuyển các thông điệp DHCP giữa DHCP server và DHCP Client.
* DHCP Lease: Là khoảng thời gian giữ nguyên địa chỉ IP trước khi nó thay đổi. Mỗi địa chỉ IP sẽ có một vòng đời nhất định và khi hết thời hạn nó sẽ được cấp một địa chỉ IP mới.

**2. Cách thức hoạt động của DHCP**

Đối với cách thức hoạt động của DHCP thì khá dễ hiểu, khi một thiết bị truy cập mạng yêu cầu địa chỉ IP từ một router thì ngay sau đó router sẽ gán cho một địa chỉ IP khả dụng cho phép thiết bị có thể giao tiếp trên mạng dễ dàng.

Trong đó, router hoạt động như một máy chủ DHCP đối với các mô hình nhỏ hay hộ gia đình. Còn đối với các mạng lớn hơn thì router không thể quản lý được nên đóng vai trò là một máy chủ chuyên dụng để cấp địa chỉ IP.

Cách thức hoạt động còn có thể hiểu theo một khía cạnh khác, khi một thiết bị muốn kết nối mạng thì nó sẽ gửi một yêu cầu đến máy chủ (gọi là DHCP DISCOVER). Sau khi có yêu cầu đến máy chủ thì ngay tại đó máy chủ sẽ tìm một địa chỉ IP khả dụng với thiết bị đó và cung cấp địa chỉ IP và gói DHCP OFFER.

Ngay sau khi nhận được địa chỉ IP, thiết bị đó sẽ phản hồi lại máy chủ với gói tin DHCP REQUEST. Và đây là lúc chấp nhận yêu cầu thì máy chủ sẽ gửi tin báo nhận (ACK) để xác nhận rằng thiết bị đó đã có điạ chỉ IP và xác định được thời gian sử dụng địa chỉ IP vừa đucợ cấp đến khi có địa chỉ IP mới.

**3. Ưu điểm và nhược điểm của DHCP là gì?**

* Ưu điểm của DHCP

  * DHCP cho phép bạn cấu hình tự động giúp cho các thiết bị như máy tính, điện thoại và các thiết bị thông minh khác,… kết nối mạng một cách nhanh chóng và dễ dàng hơn,
  * Cách thức hoạt động của DHCP là gán địa chỉ IP cho từng thiết bị, nên khó có thể trùng địa chỉ IP. Với cách làm này giúp cho hệ thống hoạt động một cách ổn định và đơn giản.
  * Với việc DHCP cho phép cài đặt mặc định và thiết lập tự động lấy IP giúp cho mọi thiết bị muốn kết nối đều nhận được địa chỉ IP và kết nối để giao tiếp với mạng.
  * Bên cạnh đó, DHCP có thể vừa quản lý địa chỉ IP và các tham số của TCP/IP trên một giao diện giúp cho việc quản lý và theo dõi dễ dàng.
  * Người quản lý có thể thay đổi cấu hình và các thông số giúp cho việc update hệ thống hiệu quả hơn.
  * Ưu điểm cuối cùng có thể nói đến ở đây là các thiết bị có thể di chuyển tự do từ mạng này sang mạng khác và có thể nhận một địa chỉ IP tự động khác (bởi vì các thiết bị có thể tự nhận địa chỉ IP).
  * 
Ngoài ra, các máy chủ DHCP cung cấp các giao diện quản lý và ghi nhật ký. Điều này giúp các quản trị viên có thể quản lý các địa chỉ IP vi phạm. Máy chủ DHCP có thể cung cấp khả năng dự phòng và tính khả dụng cao. Khi một máy chủ DHCP xảy ra lỗi, client sẽ được bảo toàn địa chỉ IP hiện tại mà không gây ra gián đoạn cho các node cuối.

Một số tổ chức muốn di chuyển DHCP cho IPv6 ra khỏi phạm vi các router/switch. Đồng thời đặt chúng trên một cơ sở hạ tầng máy chủ DHCP mạnh mẽ. Việc này thường xảy ra ở các tổ chức đang bắt đầu triển khai IPv6. Mục đích của thay đổi này thường là để có DHCP hoạt động tương tự nhau cho cả hai giao thức. Các tổ chức doanh nghiệp sẽ muốn tận dụng máy chủ DHCP giao thức kép tập trung để cung cấp địa chỉ IPv6 và IPv6 cho các thiết bị client.

* Nhược điểm của DHCP

  * DHCP sử dụng IP động đôi khi không phù hợp với thiết bị cố định như máy in, server file.
  * Đối với các máy in hộ gia đinh hay văn phòng thì việc gán địa chỉ IP liên tục không mang lại hiệu suất cao. Vì mỗi khi kết nối với một máy tính khác nhau thì máy in đó phải cập nhật cài đặt để có thể kết nối được với máy tính.

**4. Các thông điệp giao tiếp giữa DHCP server và DHCP Client**

![image](https://user-images.githubusercontent.com/48250210/158011610-5cf51ee9-f326-4eeb-aaf8-7e598278c539.png)

* DHCP Discover: Đây là một gói tin được gửi đến DHCP server khi có một thiết bị yêu cầu cung cấp địa chỉ IP để truy cập vào mạng.
* DHCP Offer: Được máy chủ DHCP gửi phản hồi cho Client sau khi nhận DHCP Discover. Đây là gói chứa địa chỉ IP, cấu hình TCP/IP bổ sung.
* DHCP Request: Đây là gói tin được DHCP Client phản hồi với server về sự chấp nhận địa chỉ IP sau khi nhận DHCP Offer.
* DHCP Acknowleadge: Đây là gói tin mà máy chủ DHCP phản hồi lại với Client nhằm xác minh rằng đã chấp nhận địa chỉ IP DHCP Request đồng thời định hướng các tham số tùy chọn để thực hiện việc cho phép Client truy cập magnj TCP/IP cũng như hoàn tất quá trình khởi động.
* DHCP Nak: Nếu Client không còn sử dugnj địa chỉ IP do nó đã hết hạn hoặc đã chuyển sang một người dung mới. Thì lúc này DHCP sẽ gửi một gói tin DHCP Nak. Và nó chính là gói tin được gửi từ DHCP server đến Client khi nó nhận được yêu cầu từ một địa chỉ IP không có giá trị theo các Scope mà nó đucợ định cấu hình.
* DHCP Decline: Trường hợp DHCP Client quyết định tham số thông tin được đề nghị nào không có giá trị nó sẽ gửi một gói DHCP Decline đến các server và client phải bắt đầu quá trình thuê bao lại.
* DHCP Release: Đây là một gói tin được DHCP Client gửi đến một server để giải phóng địa chỉ IP và có thể xóa bất kỳ IP đang còn tồn tại
