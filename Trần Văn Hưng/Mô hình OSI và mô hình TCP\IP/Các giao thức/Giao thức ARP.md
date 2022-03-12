# 1. ARP là gì?

– ARP là phương thức phân giải địa chỉ động giữa địa chỉ lớp network và địa chỉ lớp datalink. Quá trình thực hiện bằng cách: một thiết bị IP trong mạng gửi một gói tin local broadcast đến toàn mạng yêu cầu thiết bị khác gửi trả lại địa chỉ phần cứng ( địa chỉ lớp datalink ) hay còn gọi là Mac Address của mình.

– ARP là giao thức lớp 2 – Data link layer trong mô hình OSI và là giao thức lớp Link layer trong mô hình TCP/IP.

– Ban đầu ARP chỉ được sử dụng trong mạng Ethernet để phân giải địa chỉ IP và địa chỉ MAC. Nhưng ngày nay ARP đã được ứng dụng rộng rãi và dùng trong các công nghệ khác dựa trên lớp hai.

# 2. Hoạt động của ARP trong mạng LAN

   - Bước 1: Máy gửi kiểm tra cache của mình. Nếu đã có thông tin về sự ánh xạ giữa địa chỉ IP và địa chỉ MAC thì chuyển sang Bước 7.

   - Bước 2: Máy gửi khởi tạo gói tin ARP request với địa chỉ SHA và SPA là địa chỉ của nó, và địa chỉ TPA là địa chỉ IP của máy cần biết MAC. (Trường THA để giá trị toàn 0 để biểu hiện là chưa tìm được địa chỉ MAC)

   - Bước 3: Gửi quảng bá gói tin ARP trên toàn mạng (Địa chỉ MAC đích của gói tin Ethernet II là địa chỉ MAC quảng bá ff:ff:ff:ff:ff:ff).

   - Bước 4: Các thiết bị trong mạng đều nhận được gói tin ARP request. Gói tin được xử lý bằng cách các thiết bị đều nhìn vào trường địa chỉ Target Protocol Address.

  Thiết bị với IP trùng với IP trong trường Target Protocol Address sẽ bắt đầu quá trình khởi tạo gói tin ARP Reply bằng cách lấy các trường Sender Hardware Address và Sender Protocol Address trong gói tin ARP nhận được đưa vào làm Target trong gói tin gửi đi. Đồng thời thiết bị sẽ lấy địa chỉ MAC của mình để đưa vào trường Sender Hardware Address. Đồng thời cập nhất giá trị ánh xạ địa chỉ IP và MAC của máy gửi vào bảng ARP cache của mình để giảm thời gian xử lý cho các lần sau.

  - Bước 5: Thiết bị đích bắt đầu gửi gói tin Reply đã được khởi tạo đến thiết bị nguồn vừa gửi bản tin ARP request. Gói tin reply là gói tin gửi unicast.

  - Bước 6: Thiết bị nguồn nhận được gói tin reply và xử lý bằng cách lưu trường Sender Hardware Address trong gói reply như địa chỉ phần cứng của thiết bị đích cần tìm.

  - Bước 7: Thiết bị nguồn update vào ARP cache của mình giá trị tương ứng giữa địa chỉ IP và địa chỉ MAC của thiết bị đích. Lần sau sẽ không còn cần tới ARP request.

# 3. Hoạt động của ARP trong môi trường liên mạng

  Hoạt động của ARP trong một môi trường phức tạp hơn đó là hai hệ thống mạng gắn với nhau thông qua một Router.

Do các broadcast lớp MAC không thể truyền qua Router nên khi đó máy A sẽ xem Router C như một cầu nối hay một trung gian (Agent) để truyền dữ liệu. Trước đó, máy A sẽ biết được địa chỉ IP của Router C (địa chỉ Gateway) và biết được rằng để truyền gói tin tới B phải đi qua C.

Để tới được router C thì máy A phải gửi gói tin tới port X của router C (là gateway trong LAN A). Quy trình truyền dữ liệu được mô tả như sau:
   
   Máy A gửi ARP request để tìm MAC của port X.

   Router C trả lời, cung cấp cho A địa chỉ MAC của port X.

   Máy A truyền gói tin tới port X của router C (với địa chỉ MAC đích là MAC của port X, IP đích là IP máy B).

   Router C nhận được gói tin của A, forward ra port Y. Trong gói tin có chứa địa chỉ IP máy B, router C sẽ gửi ARP request để tìm MAC của máy B.

  Trên thực tế ngoài dạng bảng định tuyến này người ta còn dùng phương pháp proxy ARP (sẽ tìm hiểu phần sau), trong đó có một thiết bị đảm nhận nhiệm vụ phân giải địa chỉ cho tất cả các thiết bị khác. Theo đó các máy trạm không cần giữ bảng định tuyến nữa Router C sẽ có nhiệm vụ thực hiện, trả lời tất cả các ARP request của tất cả các máy.

# 4. Các bản tin ARP
    
   - ARP probe: Đây là loại bản tin ARP dùng để máy thăm dò xem địa chỉ mà máy được cấp phát (cấu hình manual hoặc DHCP, …) có bị trùng với địa chỉ IP của máy nào trong cùng mạng hay không. Khi mới ban đầu, các máy đều thực hiện broadcast bản tin ARP này.

   - Bản tin này có cấu trúc địa chi IP của máy gửi là 0.0.0.0 (thể hiện máy gửi bản tin này chưa xác định IP, đồng thời cũng là để các máy khác trong mạng không cập nhật MAC của máy vào ARP caching – vì nó chưa được gán IP cụ thể nào)

   - Địa chỉ MAC đích là 00:00:00:00:00:00

   - Địa chỉ IP đích là địa chỉ IP mà máy gửi được cấp phát.

   - Thông thường bản tin ARP request này sẽ không có reply.

   - ARP announcements: ARP cũng sử dụng một cách đơn giản để thông báo tới các máy trong mạng khi địa chỉ IP hoặc địa chỉ MAC của nó thay đổi. Đó chính là bản tin gratuitous ARP

   - Bản tin Gratuitous ARP được gửi broadcast request trong mạng với địa chỉ MAC và IP máy gửi là địa chỉ sau khi thay đổi.

   - Địa chỉ MAC đích là 00.00.00.00.00.00. Địa chỉ IP đích là chính nó. Điều này đảm bảo các máy trong mạng khi nhận được bản tin này sẽ chỉ cập nhật địa chỉ MAC và IP của máy gửi vào trong ARP caching của mình => không có bản tin reply cho bản tin này.

   - ARP request: Là bản tin ARP request mà máy gửi gửi broadcast để tìm địa chỉ MAC của máy nhận.

   - Địa chỉ MAC và IP gửi là địa chỉ của máy gửi.

   - Địa chỉ MAC nhận được set là 0 hết.

   - Địa chỉ IP nhận là địa chỉ IP của máy cần tìm.

   - ARP reply: Là bản tin mà máy nhận sau khi nhận được ARP request sẽ đóng gói lại MAC của mình và gửi bản tin reply về cho máy gửi.

   - Nó sẽ đóng gói là địa chỉ IP và MAC của mình vào địa chỉ SHA và PHA.

   - Địa chỉ mà máy gửi gửi tới nó sẽ được đóng gói và phần địa chỉ THA và TPA.

   - Gửi bản tin unicast.
    
 # 5. ARP Caching
  
  ARP là một giao thức phân giải địa chỉ động. Quá trình gửi gói tin Request và Reply sẽ tiêu tốn băng thông mạng. Chính vì vậy càng hạn chế tối đa việc gửi gói tin Request và Reply sẽ càng góp phần làm tăng khả năng họat động của mạng. Từ đó sinh ra nhu cầu của ARP Caching. ARP Cache có dạng giống như một bảng tương ứng giữa địa chỉ hardware và địa chỉ IP.
(Trong Window: dùng câu lệnh arp -a trong Command Prompt để show ra ARP cache trong máy)
