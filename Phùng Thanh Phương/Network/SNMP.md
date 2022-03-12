# Simple Network Management Protocol

**1. SNMP là gì?**

SNMP (Simple Network Management Protocol) là giao thức tầng ứng dụng được sử dụng để quản lý và giám sát các thiết bị mạng cũng như chức năng của chúng. SNMP cung cấp ngôn ngữ chung cho các thiết bị mạng để chuyển tiếp thông tin quản lý trong cả môi trường single-vendor và multi-vendor trong mạng cục bộ (LAN) hoặc mạng diện rộng (WAN). Phiên bản gần đây nhất của SNMP, version 3, bao gồm các cải tiến bảo mật để xác thực và mã hóa tin nhắn SNMP cũng như bảo vệ các gói trong khi truyền.

Một trong những giao thức được sử dụng rộng rãi nhất, SNMP được hỗ trợ trên một loạt các loại phần cứng – từ các thiết bị mạng thông thường như bộ định tuyến (router), bộ chuyển mạch (switch) và điểm truy cập không dây (wireless access point) đến các điểm cuối như máy in, scanner và thiết bị IoT (Internet of Things). Ngoài phần cứng, SNMP có thể được sử dụng để giám sát các dịch vụ như Dynamic Host Configuration Protocol (DHCP). Các software agent trên các thiết bị và dịch vụ này giao tiếp với hệ thống quản lý mạng (NMS), còn được gọi là trình quản lý SNMP, thông qua SNMP để chuyển tiếp thông tin trạng thái và thay đổi cấu hình.

Mặc dù SNMP có thể được sử dụng trong một mạng có quy mô bất kỳ, nhưng giá trị lớn nhất của nó là rõ ràng là trong các mạng rộng lớn. Đăng nhập thủ công và riêng lẻ vào hàng trăm hoặc hàng nghìn node sẽ cực kỳ mất thời gian và tốn nhiều tài nguyên. Trong khi đó, sử dụng SNMP với một NMS cho phép người quản trị mạng quản lý và theo dõi tất cả những node từ một giao diện duy nhất, mà thường có thể hỗ trợ hàng loạt các lệnh và cảnh báo tự động.

**2. Các thành phần của SNMP**

![image](https://user-images.githubusercontent.com/48250210/158012332-2079197b-3878-49fc-9245-cd39a59ff604.png)

Có bốn thành phần chính trong mạng do SNMP quản lý:

* SNMP Agent: Chương trình này chạy trên phần cứng hoặc dịch vụ đang được giám sát, thu thập dữ liệu về các số liệu khác nhau như tình trạng sử dụng băng thông hoặc dung lượng ổ đĩa. Khi được người quản lý SNMP truy vấn, agent sẽ gửi thông tin này lại cho trình quản lý. Một agent cũng có thể chủ động thông báo cho NMS nếu xảy ra lỗi. Hầu hết các thiết bị đi kèm với một SNMP Agent được cài đặt sẵn; Thông thường nó chỉ cần được bật lên và cấu hình.
* Các thiết bị và tài nguyên do SNMP quản lý: Đây là các node mà một agent chạy trên đó.
* Trình quản lý SNMP (còn gọi là NMS): Nền tảng phần mềm này hoạt động như một bảng điều khiển tập trung mà các agent cung cấp thông tin. Nó sẽ chủ động yêu cầu các agent gửi thông tin cập nhật qua SNMP theo định kỳ. Những gì người quản lý mạng có thể làm với thông tin đó phụ thuộc rất nhiều vào số lượng tính năng của NMS. Có một số trình quản lý SNMP miễn phí đang được cung cấp, nhưng chúng thường bị giới hạn về khả năng hoặc số lượng node mà chúng có thể hỗ trợ. Ở mức độ cao hơn, các nền tảng cấp doanh nghiệp cung cấp các tính năng nâng cao cho các mạng phức tạp hơn, với một số sản phẩm hỗ trợ lên đến hàng chục nghìn node.
* Cơ sở thông tin quản lý (Management information base – MIB): Cơ sở dữ liệu này là một file văn bản (.mib) phân loại và mô tả tất cả các đối tượng được sử dụng bởi một thiết bị cụ thể có thể được truy vấn hoặc kiểm soát bằng SNMP. Cơ sở dữ liệu này phải được tải vào NMS để có thể xác định và theo dõi trạng thái của các thuộc tính này. Mỗi mục MIB được gán một định danh đối tượng (OID).

**3. SNMP hoạt động như thế nào?**

SNMP thực hiện vô số chức năng, dựa trên sự pha trộn giữa truyền tin push-and-pull giữa các thiết bị mạng và hệ thống quản lý. Nó có thể ra lệnh đọc hoặc ghi, chẳng hạn như đặt lại mật khẩu hoặc thay đổi cài đặt cấu hình. Nó có thể báo cáo lại mức độ sử dụng băng thông, CPU và bộ nhớ, với một số trình quản lý SNMP tự động gửi cho người quản trị một email hoặc thông báo tin nhắn văn bản nếu vượt quá ngưỡng xác định trước.

Trong hầu hết các trường hợp, SNMP hoạt động trong một mô hình đồng bộ, với giao tiếp được khởi tạo bởi người quản lý SNMP và tác nhân gửi phản hồi. Các lệnh và thông báo này, thường được vận chuyển qua giao thức UDP hoặc TCP/IP, được gọi là đơn vị dữ liệu giao thức (PDU):

* GET: Được tạo bởi trình quản lý SNMP và được gửi đến một agent để lấy giá trị của một biến số nào đó, được xác định bởi OID của nó, trong một MIB .
* RESPONSE: Được gửi bởi agent cho người quản lý SNMP, được phát đi để trả lời yêu cầu GET. Chứa các giá trị của các biến được yêu cầu.
* GETNEXT: Được gửi bởi người quản lý SNMP đến agent để lấy các giá trị của OID tiếp theo trong hệ thống phân cấp của MIB.
* GETBULK: Được gửi bởi người quản lý SNMP cho agent để có được các bảng dữ liệu lớn bằng cách thực hiện nhiều lệnh GETNEXT.
* SET: Được gửi bởi người quản lý SNMP cho agent để đưa ra các cấu hình hoặc lệnh.
* TRAP: Một cảnh báo không đồng bộ được gửi bởi agent đến trình quản lý SNMP để chỉ ra một sự kiện quan trọng, chẳng hạn như lỗi hoặc sự cố, đã xảy ra.

**4. Cấu trúc của SNMP**

![image](https://user-images.githubusercontent.com/48250210/158012436-75729391-1de1-413e-ae5f-2ff34c8cd4cd.png)

Để gửi thông tin, SNMP sử dụng mô hình truyền thông phân lớp.

* Layer 1 – Lớp ứng dụng (SNMP)
* Layer 2 – Lớp vận chuyển (UDP)
* Layer 3 – Lớp Internet (IP)
* Layer 4 – Lớp Network interface

Mặc dù mô hình nhiều lớp này có vẻ hơi khó hiểu, nhưng nó rất hiệu quả trong việc tách biệt các nhiệm vụ giao tiếp và hỗ trợ thiết kế, triển khai mạng.

**5. Lợi ích của SNMP**

Sử dụng SNMP cho phép bạn quản lý các asset mạng không có hệ điều hành, nhưng là các thành phần quan trọng của cơ sở hạ tầng. 

Nó đơn giản hóa nhiệm vụ và giúp bạn có thể tập trung mạng. Nó còn cho phép kiểm soát hiệu quả hơn, ngay cả đối với thiết bị không có hệ điều hành như máy in.

Một ưu điểm khác của SNMP là nó có một ngôn ngữ duy nhất cho phép người dùng tương tác với tất cả các thiết bị từ các nhà sản xuất khác nhau.

Vì vậy, nó tương thích với hầu hết mọi asset và dịch vụ mạng, chẳng hạn như Windows, Linux, Mac và máy ảo Java.

SNMP không chỉ hữu ích để cung cấp hỗ trợ chủ động mà còn để cải thiện trải nghiệm khách hàng, cho phép bạn dự đoán nhu cầu.

* Các lợi ích chính khác của SNMP:

  * Ưu điểm chính của việc sử dụng SNMP là thiết kế đơn giản. Dễ dàng triển khai nó trên mạng, vì nó không yêu cầu cấu hình lâu.
  * Hơn nữa, SNMP rất phổ biến ngày nay. Hầu hết tất cả các nhà sản xuất thiết bị phần cứng liên mạng lớn, như switch hoặc router, đều triển khai hỗ trợ SNMP trong các sản phẩm của họ.
  * Mở rộng là một ưu thế khác của SNMP. Do thiết kế đơn giản, dễ dàng cập nhật giao thức để đáp ứng nhu cầu của user trong tương lai.
  * SNMP dựa trên giao thức truyền tải UDP, yêu cầu ít tài nguyên hơn và kết nối đồng thời hơn với TCP.
