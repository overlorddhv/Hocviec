# DNS Server

**1. Khái niệm DNS server là gì?**

DNS là viết tắt của cụm từ Domain Name System, mang ý nghĩa đầy đủ là hệ thống phân giải tên miền. Hiểu một cách ngắn gọn nhất, DNS cơ bản là một hệ thống chuyển đổi các tên miền website mà chúng ta đang sử dụng, ở dạng www.tenmien.com sang một địa chỉ IP dạng số tương ứng với tên miền đó và ngược lại.

Thao tác này của DNS giúp liên kết các thiết bị mạng với nhau nhằm mục đích định vị và gán một địa chỉ cụ thể cho các thông tin trên internet.

![image](https://user-images.githubusercontent.com/48250210/158001228-81521854-8537-42c1-8e6a-9146d7abf20a.png)

Trong hầu hết các trường hợp, hai DNS server: server phụ và server chính được cấu hình tự động trên router hoặc máy tính khi kết nối với ISP thông qua DHCP. Người dùng có thể cấu hình 2 DNS server trong trường hợp trong một số chúng bị lỗi, sau đó thiết bị sẽ dùng server phụ.

Do chỉ phụ thuộc vào thời gian thiết bị của bạn tiếp cận DNS server nên một số DNS server có thể cung cấp thời gian truy cập nhanh hơn các máy chủ khác. Chẳng hạn, nếu DNS server của ISP gần hơn DNS server của Google, thì bạn có thể thấy rằng các địa chỉ được giải quyết nhanh hơn, bằng cách sử dụng các server mặc định từ ISP của bạn chứ không phải server của bên thứ ba.

Nếu gặp phải sự cố mạng không load được website thì đó có thể là sự cố với DNS server. Nếu DNS server không thể tìm thấy địa chỉ IP chính xác được liên kết với hostname bạn nhập, trang web sẽ không thể load. Điều này cũng có nghĩa là do máy tính giao tiếp thông qua địa chỉ IP, không phải hostname.

Cài đặt DNS server gần nhất với thiết bị là những cái đặt sẽ được sử dụng. Chẳng hạn, trong khi ISP của bạn có thể sử dụng một bộ DNS server, áp dụng cho tất cả các router được liên kết với nó, thì router của bạn có thể sử dụng một bộ cài đặt DNS server khác cho tất cả các thiết bị được kết nối với router đó.

**2. Chức năng của DNS là gì?**

Về chức năng, DNS có thể được hiểu như một “người phiên dịch” và “truyền đạt thông tin”. DNS sẽ làm công việc dịch tên miền thành một địa chỉ IP gồm 4 nhóm số khác nhau. Ví dụ như www.tenmien.com thành 421.64.874.899 hoặc ngược lại dịch một địa chỉ IP thành tên miền.

Khi “dịch” như thế, trình duyệt sẽ hiểu và đăng nhập vào được. Và khi người dùng đăng nhập vào một website, thay vì phải nhớ và nhập một dãy số địa chỉ IP của hosting, thì chỉ cần nhập tên website là trình duyệt tự động nhận diện.

Mỗi máy tính trên Internet đều có một địa chỉ IP duy nhất. Địa chỉ IP này được dùng để thiết lập kết nối giữa server và máy khách để khởi đầu một kết nối. Bất kỳ khi nào, bạn truy cập vào một website tùy ý hoặc gửi một email, thì DNS đóng vai trò rất quan trọng trong trường hợp này.

Trong vô vàn trang web trên thế giới, sẽ không có ai có thể nhớ hết từng dãy số địa chỉ IP trong mỗi lần đăng nhập. Do đó, khái niệm tên miền được đưa ra, từ đó mỗi trang web sẽ được xác định với tên duy nhất.

Tuy nhiên, địa chỉ IP vẫn được sử dụng như một nền tảng kết nối bởi các thiết bị mạng. Đó là nơi DNS làm việc phân giải tên domain thành địa chỉ IP để các thiết bị mạng giao tiếp với nhau. Đồng thời, bạn cũng có thể tải một website bằng cách nhập trực tiếp địa chỉ IP thay vì nhập tên domain của website đó.

**3. Đặc điểm của DNS server**

Tốc độ của các DNS server đều khác nhau. Người dùng có thể dùng DNS server riêng bằng cách điền vào network connections hay DNS server mặc định của nhà cung cấp dịch vụ internet. Còn nếu dùng DNS server mặc định thì không cần.

Các DNS server có 2 nhiệm vụ là phản hồi các DNS server bên ngoài đang phân giải những cái tên bên trong miền quản lý và phân giải các máy bên trong miền về các địa chỉ Internet.


Mỗi nhà cung cấp dịch vụ sẽ sở hữu cho mình một DNS Server riêng với mục đích vận hành. Vì vậy, khi tra địa chỉ IP của website trong mỗi trình duyệt web thì bắt buộc gửi URL đó tới DNS Server của nhà cung cấp dịch vụ tên miền đó.

Danh sách DNS server tốt nhất

* Google Public DNS server
* OpenDNS
* Norton ConnectSafe
* Comodo Secure DNS
* Level3
* DNS Advantage
* OpenNIC
* Dyn
* Safe DNS
* DNS.Watch
* FreeDNS
* Yandex DNS
* DNS Singapore

**4. Phân loại DNS Server**

**4.1.Root Name Servers**

Đây là máy chủ tên miền chứa các thông tin, để tìm kiếm các máy chủ tên miền lưu trữ (authority) cho các tên miền thuộc mức cao nhất (top-level-domain).

Máy chủ ROOT có thể đưa ra các truy vấn (query) để tìm kiếm tối thiểu các thông tin về địa chỉ của các máy chủ tên miền authority thuộc lớp top-level-domain chứa tên miền muốn tìm.

Sau đó, các máy chủ tên miền ở mức top-level-domain có thể cung cấp các thông tin về địa chỉ của máy chủ authority cho tên miền ở mức second-level-domain chứa tên miền muốn tìm. Quá trình tìm kiếm tiếp tục cho đến khi chỉ ra được máy chủ tên miền authority cho tên miền muốn tìm. Theo cơ chế hoạt động này thì bạn có thể tìm kiếm một tên miền bất kỳ trên không gian tên miền.

Một điểm đáng chú ý khác, quá trình tìm kiếm tên miền luôn được bắt đầu bằng các truy vấn gửi cho máy chủ ROOT. Nếu như các máy chủ tên miền ở mức ROOT không hoạt động, quá trình tìm kiếm này sẽ không được thực hiện.

Để tránh điều này xảy ra, trên mạng Internet hiện tại có 13 hệ thống máy chủ tên miền ở mức ROOT. Các máy chủ tên miền này nói chung và ngay trong cùng một hệ thống nói riêng đều được đặt tại nhiều vị trí khác nhau trên mạng Internet.

**4.2. Local Name Servers**

Server này chứa thông tin, để tìm kiếm máy chủ tên miền lưu trữ cho các tên miền thấp hơn. Nó thường được duy trì bởi các doanh nghiệp, các nhà cung cấp dịch vụ Internet (ISPs)

**5. CÁCH SỬ DỤNG DNS**

Để sử dụng DNS, thì mỗi loại sẽ có những tốc độ biên khác nhau nên người dùng từ đây cũng có thể tự đưa ra lựa chọn DNS server. Theo đó, người dùng có hai sự lựa chọn cho việc sử dụng là theo DNS server khác (ở đây có thể miễn phí hoặc phải trả phí), hoặc là sự dụng DNS đã được mặc định trước từ nhà cung cấp về dịch vụ internet.

![image](https://user-images.githubusercontent.com/48250210/158002046-f73a69dd-9081-4ae3-95e9-43ab3234fbbd.png)

Nếu bạn làm thèo cách đầu tiên, sử dụng DNS server khác, thì bạn cần phải thay đổi DNS ở trong máy tính của mình với những bước cơ bản sau:

Bước 1: Chọn Start -Settings – Network Connections

Bước 2: Double-click – Local Area Connection, chọn Properties – Internet Protocol(TCP/IP) – Properties

Bước 3: Điền thông số của DNS Server mà bạn muốn vào ô “Preferred DNS Server” và ô  “Alternate DNS Server”.

**6.  Cơ chế hoạt động của DNS**

Giả sử bạn muốn truy cập vào trang có địa chỉ tenmien.com.vn

Bước 1:

Trước hết chương trình trên máy người sử dụng gửi yêu cầu tìm kiếm địa chỉ IP ứng với tên miền tenmien.com.vn tới máy chủ quản lý tên miền cục bộ thuộc mạng của nó. Máy chủ tên miền cục bộ này kiểm tra trong cơ sở dữ liệu của nó có chứa cơ sở dữ liệu chuyển đổi từ tên miền sang địa chỉ IP của tên miền mà người sử dụng yêu cầu không. Trong trường hợp máy chủ tên miền cục bộ có cơ sở dữ liệu này, nó sẽ gửi trả lại địa chỉ IP của máy có tên miền nói trên.

Trong trường hợp máy chủ tên miền cục bộ không có cơ sở dữ liệu về tên miền này nó sẽ hỏi lên các máy chủ tên miền ở mức cao nhất. Máy chủ tên miền ở mức ROOT này sẽ chỉ cho máy chủ tên miền cục bộ địa chỉ của máy chủ tên miền quản lý các tên miền có đuôi .vn.

Bước 2:

Tiếp đó, máy chủ tên miền cục bộ gửi yêu cầu đến máy chủ quản lý tên miền Việt Nam (.VN) tìm tên miền tenmien.com.vn

Máy chủ tên miền cục bộ sẽ hỏi máy chủ quản lý tên miền vnn.vn địa chỉ IP của tên miền tenmien.com.vn. Do máy chủ quản lý tên miền vnn.vn có cơ sở dữ liệu về tên miền semtek.com.vn nên địa chỉ IP của tên miền này sẽ được gửi trả lại cho máy chủ tên miền cục bộ.

Bước 3:

Cuối cùng, máy chủ tên miền cục bộ chuyển thông tin tìm được đến máy của người sử dụng.

**7. Kiến trúc DNS**

* Không gian tên miền (Domain name space)

Không gian tên miền là một kiến trúc dạng cây (hình), có chứa nhiều nốt (node). Mỗi nốt trên cây sẽ có một nhãn và có không hoặc nhiều resource record (RR), chúng giữ thông tin liên quan tới tên miền. Nốt root không có nhãn

* Tên miền (Domain name)

Tên miền được tạo thành từ các nhãn và phân cách nhau bằng dấu chấm (.), ví dụ example.com. Tên miền còn được chia theo cấp độ như tên miền top level, tên miền cấp 1, cấp 2...

* Cú pháp tên miền (Domain name syntax)

Tên miền được định nghĩa trong các RFC 1035, RFC 1123, và RFC 2181. Một tên miền bao gồm một hoặc nhiều phần, gọi là các nhãn (label), chúng cách nhau bởi dấu chấm (.), ví dụ example.com.

Hệ thống phân giải tên miền tính theo hướng từ phải sang trái. Ví dụ www.example.com thì nhãn example là một tên miền con của tên miền com, và www là tên miền con của tên miền example.com. Cây cấu trúc này có thể có tới 127 cấp.

* Tên miền quốc tế hóa (Internationalized domain names)

Do sự giới hạn của bộ ký tự ASCII trong việc diễn tả các ngôn ngữ khác nhau trên thế giới, ICANN cho phép thiết lập hệ thống IDNA (Internationalized domain names Application), dùng ký tự Unicode để biểu diễn tên miền

* Máy chủ tên miền (NS - Name Server)

Máy chủ tên miền chứa thông tin lưu trữ về một số tên miền. Hệ thống phân giải tên miền được vận hành bởi hệ thống dữ liệu phân tán, dạng Client-Server. Các node của hệ thống dữ liệu này là các máy chủ tên miền. Mỗi một tên miền sẽ có ít nhất một máy chủ tên miền chứa thông tin về tên miền đó. Các thông tin về máy chủ tên miền sẽ được lưu trữ trong các zone của tên miền. Có hai dạng Name Server là là Primary và Secondary. Một Client sẽ ưu tiên hỏi Primary trước và thử lại với Secondary nếu Primary không thể trả lời thông tin về tên miền đó trong thời gian quy định.

* Máy chủ tên miền có thẩm quyền (Authoritative name server)

Máy chủ tên miền có thẩm quyền là một máy chủ tên miền có thể trả lời các truy vấn DNS từ các dữ liệu gốc, ví dụ, tên miền quản trị hoặc phương thức DNS động.

**8. Cấu trúc gói tin DNS**

* ID: Là một trường 16 bits, chứa mã nhận dạng, nó được tạo ra bởi một chương trình để thay cho truy vấn. Gói tin hồi đáp sẽ dựa vào mã nhận dạng này để hồi đáp lại. Chính vì vậy mà truy vấn và hồi đáp có thể phù hợp với nhau.
* QR: Là một trường 1 bit. Bít này sẽ được thiết lập là 0 nếu là gói tin truy vấn, được thiết lập là một nếu là gói tin hồi đáp.
* Opcode: Là một trường 4 bits, được thiết lập là 0 cho cờ hiệu truy vấn, được thiết lập là 1 cho truy vấn ngược, và được thiết lập là 2 cho tình trạng truy vấn.
* AA: Là trường 1 bit, nếu gói tin hồi đáp được thiết lập là 1, sau đó nó sẽ đi đến một server có thẩm quyền giải quyết truy vấn.
* TC: Là trường 1 bit, trường này sẽ cho biết là gói tin có bị cắt khúc ra do kích thước gói tin vượt quá băng thông cho phép hay không.
* RD: Là trường 1 bit, trường này sẽ cho biết là truy vấn muốn server tiếp tục truy vấn một cách đệ quy.
* RA: Trường 1 bit này sẽ cho biết truy vấn đệ quy có được thực thi trên server không.
* Z: Là trường 1 bit. Đây là một trường dự trữ, và được thiết lập là 0.
* Rcode: Là trường 4 bits, gói tin hồi đáp sẽ có thể nhận các giá trị sau:
  * 0: Cho biết là không có lỗi trong quá trình truy vấn.
  * 1: Cho biết định dạng gói tin bị lỗi, server không hiểu được truy vấn.
  * 2: Server bị trục trặc, không thực hiện hồi đáp được.
  * 3: Tên bị lỗi. Chỉ có server có đủ thẩm quyền mới có thể thiết lập giá trị náy.
  * 4: Không thi hành. Server không thể thực hiện chức năng này.
  * 5: Server từ chối thực thi truy vấn.
* QDcount: Số lần truy vấn của gói tin trong một vấn đề.
* ANcount: Số lượng tài nguyên tham gia trong phần trả lời.
* NScount: Chỉ ra số lượng tài nguyên được ghi lại trong các phần có thẩm quyền của gói tin.
* ARcount: Chỉ ra số lượng tài nguyên ghi lại trong phần thêm vào của gói tin.
