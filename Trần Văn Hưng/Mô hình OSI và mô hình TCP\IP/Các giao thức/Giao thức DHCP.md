# 1. DHCP là gì?

DHCP (Dynamic Host Configuration Protocol hay Giao thức cấu hình host động) là một giao thức được sử dụng để cung cấp quản lý nhanh chóng, tự động và tập trung cho việc phân phối địa chỉ IP trong mạng. DHCP cũng được sử dụng để cấu hình đúng subnet mask, cổng mặc định và thông tin về DNS server trên thiết bị.

# 2. Các thành phần của DHCP

Khi làm việc với DHCP, bạn cần hiểu tất cả thành phần của nó. Dưới đây là danh sách các thành phần của DHCP.

   - DHCP server: Một thiết bị mạng chạy dịch vụ DHCP chứa địa chỉ IP và thông tin cấu hình liên quan. Đây thường là máy chủ hoặc router nhưng có thể là bất cứ thứ gì hoạt động như máy chủ chẳng hạn như thiết bị SD-WAN.
   - DHCP client: Thiết bị nhận thông tin cấu hình từ máy chủ DHCP. Đây có thể máy tính, thiết bị di động, thiết bị IoT (Internet of Things) hoặc bất cứ thiết bị gì khác yêu cầu kết nối mạng. Hầu hết các thiết bị này được cấu hình để nhận thông tin DHCP theo mặc định.
   - IP address pool: Dãy địa chỉ có sẵn cho client DHCP. Những địa chỉ này thường được truyền tuần tự từ thấp nhất đến cao nhất.
   - Subnet: Mạng IP có thể được phân thành các phân đoạn được gọi là subnet (mạng con). Mạng con giúp mạng được quản lý dễ dàng hơn.
   - Lease: Khoảng thời gian client DHCP giữ thông tin địa chỉ IP. Khi khoảng thời gian này hết hạn, client phải làm mới nó.
   - DHCP relay: Router hoặc máy chủ nghe tin nhắn được phát trên mạng đó và sau đó chuyển chúng đến một máy chủ được cấu hình. Máy chủ này sau đó phản hồi lại relay agent để truyền chúng đến client. Nó được sử dụng để tập trung máy chủ DHCP thay vì để máy chủ trên mỗi mạng con.

# 3. Nguyên lý hoạt động của DHCP

Thành phần chính của DHCP bao gồm 4 bản tin:

   - DISCOVERY
   - OFFER
   - REQUEST
   - ACK
    
Quá trình cấp phát địa chỉ IP trong giao thức DHCP bao gồm các bước sau:

![image](https://user-images.githubusercontent.com/55913475/157590268-35b0df36-748b-40e8-b9d3-e87639d35b3f.png)

Kịch bản client xin cấp DHCP từ modem

   - Bước 1: Khi muốn có địa chỉ IP để truy cập vào internet thì client sẽ tạo ra bản tin DISCOVERY để yêu cầu cấp phát địa chỉ IP
   - Bước 2: Client chưa biết địa chỉ chính xác của Server cấp phát địa chỉ cho mình do đó nó sẽ gửi bản tin này dưới dạng broadcast.
   - Bước 3: Server sẽ nhận bản tin DISCOVERY của client. Sau khi biết client muốn được cấp địa chỉ IP nó sẽ kiểm tra xem địa chỉ IP nào phù hợp để cấp cho client sử dụng
   - Bước 4: Server tạo bản tin OFFER. Gói tin này sẽ lưu trữ thông tin về IP và các thông số cấu hình khác mà client yêu cầu để có thể sử dụng để truy cập internet
   - Bước 5: Tất cả các server sẽ gửi bản OFFER dưới dạng broadcast
   - Bước 6: Client nhận gói OFFER và nó sẽ chọn ra bản OFFER đầu tiên mà nó nhận được. Nếu không nhận được OFFER nào trong một khoảng thời gian nào đó thì nó sẽ gửi lại DISCOVERY một lần nữa
   - Bước 7: Client tạo ra gói REQUEST. Và gửi dưới dạng broadcast tới tất cả các server. Server nào được nhận OFFER sẽ mang ý nghĩa là nó đồng ý nhận IP. Server nào không được nhận OFFER thì thông báo là không nhận OFFER đó
   - Bước 8: Server nhận bản tin REQEST. Các server không được nhận OFFER sẽ bỏ qua gói tin này. Gói tin nào được nhận OFFER sẽ nhận và xử lý nó. Nó sẽ kiểm tra sem IP này còn sử dụng được hay không. Nếu còn sử dụng được thì nó sẽ ghi lại thông tin và gửi lại gói tin PACK cho client. Còn nếu không thì nó sẽ gửi lại PNAK để quay lại bước 1.
    
 # 4. Ưu điểm khi sử dụng DHCP

   - Tập trung quản trị thông tin cấu hình host
   - Cấu hình động các máy
   - Cấu hình IP cho các máy một cách liền mạch.
   - Sự linh hoạt
   - Đơn giản hóa vài trò quản trị của việc cauas hình địa chỉ IP của client.
   - Sự linh hoạt
    
 # 5. Rủi ro bảo mật của DHCP
 
 Giao thức DHCP không yêu cầu xác thực để bất kỳ client nào cũng có thể tham gia mạng một cách nhanh chóng. Do đó, nó có nhiều vấn đề về bảo mật như máy chủ trái phép đưa thông tin xấu cho client, client trái phép được cấp địa chỉ IP, v.v… Bởi vì client không có cách nào để xác thực tính hợp lệ của máy chủ DHCP, do đó máy chủ có thể cung cấp thông tin mạng không chính xác. Điều này có thể gây ra các cuộc tấn công từ chối dịch vụ (denial-of-service attack) hoặc tấn công man-in-the-middle sử dụng máy chủ giả để chặn dữ liệu có thể được sử dụng với mục đích xấu. Ngược lại, bởi vì máy chủ DHCP không xác thực client, do đó nó sẽ phát thông tin địa chỉ IP đến bất cứ thiết bị nào yêu cầu. Ai đó có thể cấu hình client để liên tục thay đổi thông tin đăng nhập và nhanh chóng làm cạn kiệt địa chỉ IP có sẵn trong phạm vi, ngăn các thiết bị truy cập vào mạng. Thông số DHCP có thể giải quyết được một số vấn đề kể trên. Tùy chọn Relay Agent Information Option cho phép kỹ sư mạng gắn thẻ thông điệp DHCP khi chúng đến mạng. Thẻ này được sử dụng để kiểm soát truy cập mạng. Ngoài ra, còn có một điều khoản để xác thực thông điệp DHCP. Việc sử dụng xác thực 802.1x còn được gọi là kiểm soát truy cập mạng (NAC) được sử dụng để bảo mật DHCP. Hầu hết các nhà cung cấp mạng hàng đầu đều hỗ trợ NAC.
 
