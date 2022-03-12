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

Root Name Servers là gì?
Đây là máy chủ tên miền chứa các thông tin, để tìm kiếm các máy chủ tên miền lưu trữ (authority) cho các tên miền thuộc mức cao nhất (top-level-domain).

Máy chủ ROOT có thể đưa ra các truy vấn (query) để tìm kiếm tối thiểu các thông tin về địa chỉ của các máy chủ tên miền authority thuộc lớp top-level-domain chứa tên miền muốn tìm.

Sau đó, các máy chủ tên miền ở mức top-level-domain có thể cung cấp các thông tin về địa chỉ của máy chủ authority cho tên miền ở mức second-level-domain chứa tên miền muốn tìm. Quá trình tìm kiếm tiếp tục cho đến khi chỉ ra được máy chủ tên miền authority cho tên miền muốn tìm. Theo cơ chế hoạt động này thì bạn có thể tìm kiếm một tên miền bất kỳ trên không gian tên miền.

Một điểm đáng chú ý khác, quá trình tìm kiếm tên miền luôn được bắt đầu bằng các truy vấn gửi cho máy chủ ROOT. Nếu như các máy chủ tên miền ở mức ROOT không hoạt động, quá trình tìm kiếm này sẽ không được thực hiện.

Để tránh điều này xảy ra, trên mạng Internet hiện tại có 13 hệ thống máy chủ tên miền ở mức ROOT. Các máy chủ tên miền này nói chung và ngay trong cùng một hệ thống nói riêng đều được đặt tại nhiều vị trí khác nhau trên mạng Internet.
