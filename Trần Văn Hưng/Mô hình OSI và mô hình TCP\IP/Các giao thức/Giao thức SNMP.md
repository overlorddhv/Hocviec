# 1. SNMP là gì?
  
  SNMP (Simple Network Management Protocol) là một giao thức tầng ứng dụng được Hội đồng Kiến trúc Internet (IAB) xác định trong RFC1157 để trao đổi thông tin quản lý giữa các thiết bị mạng. Nó là một phần của Transmission Control Protocol/Internet Protocol (TCP/IP). Giao thức SNMP là một trong những giao thức mạng được chấp nhận rộng rãi để quản lý và giám sát các phần tử mạng. Hầu hết các thiết bị mạng được cung cấp đi kèm với SNMP agent. Các agent này phải được kích hoạt và cấu hình để giao tiếp với các công cụ giám sát mạng hoặc hệ thống quản lý mạng (NMS).
  
# 2. Các thành phần của SNMP

  **SNMP Manager**
  
  Trình quản lý hoặc hệ thống quản lý là một thực thể riêng biệt có trách nhiệm giao tiếp với các thiết bị mạng được triển khai SNMP agent. Đây thường là một máy tính được sử dụng để chạy một hoặc nhiều hệ thống quản lý mạng.

  Các chức năng chính của SNMP manager:

   - Agent truy vấn
   - Nhận response từ các agent
   - Đặt các biến trong agent
   - Xác nhận các sự kiện không đồng bộ từ các agent
    
  **SNMP Manager Device**
    
   Thiết bị được quản lý hoặc phần tử mạng là một phần của mạng yêu cầu một số hình thức giám sát và quản lý, ví dụ: router, switches, server, máy trạm, máy in, UPS, v.v.
    
  **SNMP Agent**
  
  Agent là một chương trình được đóng gói trong các thiết bị mạng. Việc kích hoạt agent cho phép nó thu thập cơ sở dữ liệu thông tin quản lý từ thiết bị cục bộ và cung cấp nó cho SNMP manager khi được truy vấn. Các agent này có thể là tiêu chuẩn (ví dụ: Net-SNMP) hoặc cụ thể cho một nhà cung cấp (ví dụ: HP insight agent).

  Các chức năng chính của SNMP agent:

   - Thu thập thông tin quản lý về các chỉ số hoạt động cuả thiết bị
   - Lưu trữ và truy xuất thông tin quản lý như được định nghĩa trong MIB.
   - Báo hiệu sự kiện cho trình quản lý.
   - Hoạt động như một proxy cho một số nút mạng không quản lý được – SNMP.
    
# 3. Cách thức hoạt động của SNMP

  ![image](https://user-images.githubusercontent.com/55913475/157618603-f00d2dcf-209f-4f23-b0ca-5dadef6d95bb.png)
  
  SNMP sử dụng một số command cơ bản để giao tiếp giữa manager và agent.
    
   - GET: Yêu cầu thông tin bất cứ lúc nào
  
  Để nhận thông tin trạng thái từ agent, manager có thể đưa ra message Get và GetNext để yêu cầu thông tin cho một biến cụ thể. Sau khi nhận được message Get hoặc GetNext, agent sẽ gửi message GetResponse cho manager. Nó sẽ chứa thông tin được yêu cầu hoặc lỗi giải thích tại sao không thể xử lý request.
    
   - SET: Điều khiển thiết bị từ xa 
  
  Message SET cho phép manager yêu cầu thực hiện thay đổi đối với đối tượng được quản lý (tức là rơle điều khiển). Sau đó, agent sẽ trả lời bằng message Set-response nếu thay đổi đã được thực hiện hoặc lỗi giải thích tại sao không thể thực hiện thay đổi.
    
   - TRAP: SNMP message phổ biến nhất
 
 Message TRAP được khởi xướng bởi agent và gửi đến manager khi một sự kiện quan trọng xảy ra. Trap dùng để cảnh báo cho manager – thay vì đợi request trạng thái từ manager khi cần thăm dò ý kiến của agent.
    
   - INFORM: Một loại message có giá trị khác
  
  Message INFORM rất giống với TRAP, nhưng chúng đáng tin cậy hơn. Các message INFORM được khởi tạo bởi agent và khi manager nhận được nó, nó sẽ gửi response đến agent cho biết message đã được nhận. Nếu agent không nhận được response từ manager thì agent sẽ gửi lại message INFORM.
    
   - SNMPWALK: Nhận tất cả dữ liệu
  
  SNMPWALK sử dụng nhiều request Get-Next để truy xuất toàn bộ cây dữ liệu mạng từ một đối tượng được quản lý. Công cụ iReasoning MIB Browser sẽ rất hữu ích để xem tất cả các OID mà một agent cung cấp.
  
# 4. Cấu trúc của SNMP

  ![image](https://user-images.githubusercontent.com/55913475/157618699-3f0b76aa-fdbf-43e8-a814-867e5d161069.png)

  Để gửi thông tin, SNMP sử dụng mô hình truyền thông phân lớp.

   - Layer 1 – Lớp ứng dụng (SNMP)
   - Layer 2 – Lớp vận chuyển (UDP)
   - Layer 3 – Lớp Internet (IP)
   - Layer 4 – Lớp Network interface
  
  Mặc dù mô hình nhiều lớp này có vẻ hơi khó hiểu, nhưng nó rất hiệu quả trong việc tách biệt các nhiệm vụ giao tiếp và hỗ trợ thiết kế, triển khai mạng.
  
# 5. Lợi ích của SNMP

  - Sử dụng SNMP cho phép bạn quản lý các asset mạng không có hệ điều hành, nhưng là các thành phần quan trọng của cơ sở hạ tầng. 
  - Đơn giản hóa nhiệm vụ và giúp bạn có thể tập trung mạng. Nó còn cho phép kiểm soát hiệu quả hơn, ngay cả đối với thiết bị không có hệ điều hành như máy in.
  - Có một ngôn ngữ duy nhất cho phép người dùng tương tác với tất cả các thiết bị từ các nhà sản xuất khác nhau.
  - Tương thích với hầu hết mọi asset và dịch vụ mạng, chẳng hạn như Windows, Linux, Mac và máy ảo Java.
  - Thiết kế đơn giản, dễ dàng triển khai nó trên mạng, vì nó không yêu cầu cấu hình lâu.
  - Hầu hết tất cả các nhà sản xuất thiết bị phần cứng liên mạng lớn, như switch hoặc router, đều triển khai hỗ trợ SNMP trong các sản phẩm của họ.
  - Dễ dàng cập nhật giao thức để đáp ứng nhu cầu của user trong tương lai.
  - SNMP dựa trên giao thức truyền tải UDP, yêu cầu ít tài nguyên hơn và kết nối đồng thời hơn với TCP.
