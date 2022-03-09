# Mạng máy tính
**1. Định nghĩa một mạng máy tính cơ bản**
Mạng máy tính (computer network) là tập hợp của 2 hay nhiều máy tính kết hợp với nhau thông qua các phương tiện kết nối (thiết bị kết nối - Switch, hub, dây cáp, sóng vô tuyến,...) để chia sẻ các tài nguyên. Việc kết nối giữa các máy tính tuân theo các chuẩn về mạng máy tính (netwwork standard), các công nghệ mạng và các giao thức (protocol). Các máy tính trong mạng có thể gọi là nút mạng.

Việc sử dụng mạng máy tính giúp các tổ chức, danh nghiệp dễ dàng trong việc chia sẻ các tài nguyên cho người dùng. Các tài nguyên chia sẻ bao gồm các file, thư mục, máy in, kết nối Internet, các ứng dụng dùng chung.

**2. Các thành phần mạng (Netwwork Component)**

Mỗi mạng máy tính bao gồm các máy tính, thiết bị mạng, máy in,... chúng được gọi là các thành phần mạng (network component) bao gồm các thành phần chính sau:
* Máy chủ (server): Là máy tính có các tài nguyên, dịch vụ, ứng dụng chia sẻ để cho các máy tính khác truy cập tới và sử dụng. máy chủ chạy hệ điều hành máy chủ (Windows, Linux, Unix) và cài các phần mềm chuyền dụng dành cho máy chủ. Tùy thuộc vào chức năng và nhiệm vụ mà máy chủ có thể có tên gọi khác nhau như máy chủ dữ liệu (data server), máy chủ thư điện tử (mail server), máy chủ ứng dụng (application server),...
* Máy trạm (client): Là các máy tính trong mạng có thể kết nối đến các máy chủ để sử dụng các tài nguyên mà máy chủ chia sẻ. máy trạm chạy hệ thống điều hành máy trạm và các phần mềm máy trạm.
* Phương tiện truyền dẫn (media): Là các thành phần truyền dẫn vật lý giữa các máy tính như dây cáp (cable), sóng radio,...
* Tài nguyên (resource): Là các ứng dụng, dữ liệu, phần cứng chuyên dụng,... được cung cấp bởi các máy chủ trên mạng cho người dùng thông qua các máy trạm (files, máy in,...)
* Card mạng (netwwork adapter): Là một thiết bị chuyên dụng giúp các máy tính có thể gửi dữ liệu tới các máy tính thông qua phương tiện truyền dẫn
* Các thiết bị kết nối như hub, switch, router
* Giao thức mạng (netwwork protocol): là tập hợp các quy luật, quy định giúp các máy tính có thể  giao tiếp với nhau
* Topo mạng (network topology): là cấu trúc vật lý của mạng (bus, star, ring,...) nó được phân loại dựa vào loại phương tiện truyền dẫn (media type), giao thức mạng (protocol), card mạng,...

**3. Phân loại mạng máy tính**
**3.1 LAN**

Mạng LAN là viết tắt của từ tiếng Anh Local Area Network được tạm dịch là mạng máy tính nội bộ, giao tiếp này cho phép các thiết bị kết nối với nhau để cùng làm việc và chia sẻ dữ liệu. Kết nối này được thực hiện thông qua sợi cáp LAN hay Wifi (không dây) trong không gian hẹp, chính vì thế nó chỉ dùng được ở một phạm vi giới hạn như phòng làm việc, trong nhà, trường học…

![image](https://user-images.githubusercontent.com/48250210/157400600-4c75bc6b-c68b-49ca-b9e3-49e00a353786.png)

Ưu điểm của mạng LAN:
* Tốc độ truyền tải cao, hỗ trợ kết nối được nhiều thiết bị nhanh chóng. Tuy bị giới hạn về phạm vi kết nối nhưng chi phí, sử dụng dây ít, dễ dàng quản trị.

**3.2. MAN**

Mạng MAN (Metropolitan Area Network) hay còn gọi là mạng đô thị liên kết từ nhiều mạng LAN qua dây cáp, các phương tiện truyền dẫn khác,... Khả năng kết nối trong phạm vi lớn như trong một thị trấn, thành phố, tỉnh.

Mô hình mạng MAN thường được dùng chủ yếu cho đối tượng là tổ chức, doanh nghiệp nhiều chi nhánh, nhiều bộ phận kết nối với nhau.

![image](https://user-images.githubusercontent.com/48250210/157401135-4a63442b-1a08-4fe8-a242-57a15387ab55.png)

Mạng Man thường được sử dụng cho doanh nghiệp vì mô hình này này cung cấp nhiều loại dịch vụ như kết nối đường truyền qua voice (thoại), data (dữ liệu), video(hình ảnh), triển khai các ứng dụng dễ dàng.

Ưu điểm của mạng MAN:
* Phạm vi kết nối lớn giúp tương tác giữa các bộ phận doanh nghiệp dễ dàng, hiệu quả,chi phí thấp, tốc độ truyền tải ổn định, bảo mật thông tin, quản lý đơn giản.

**3.3. WAN**

Mạng WAN ((Wide Area Network) hay còn gọi là mạng diện rộng được kết hợp giữa các mạng đô thị bao gồm cả mạng MAN và mạng LAN thông qua thiết bị vệ tinh, cáp quang, cáp dây điện.

![image](https://user-images.githubusercontent.com/48250210/157401988-10236dbf-be36-44cc-9fa2-5bbbac9b10c0.png)

Mạng diện rộng được tạo ra nhằm kết nối trên một diện lớn có quy mô trên quốc gia. Giao thức sử dụng trong mạng WAN là TCP/IP, đường truyền băng thông thay đổi tùy vào vị trí lắp đặt.

Ưu điểm của mạng WAN:
* Khả năng kết nối rộng lớn, không bị giới hạn tín hiệu, dễ dàng chia sẻ thông tin, lưu trữ dữ liệu. Tốc độ truyền tải tương đối tùy vào mỗi khu vực hoặc thiết bị truyền dẫn khác nhau.

=> có thể so sánh qua bảng sau:

![image](https://user-images.githubusercontent.com/48250210/157402459-6b6db3c1-e9c9-48c0-8157-4429af59c5d6.png)

**3.4. Ngoài ra còn có các loại mạng khác**
* PAN (Personal Area Network): hay còn gọi là mạng cá nhân khả năng kết nối phạm vi nhỏ thường được dùng thông qua các thiết bị định tuyến. Khả năng định tuyến này giúp truyền dẫn dữ liệu trên thiết bị đến đích.
* SAN (Storage Area Networking): hay còn gọi là mạng lưu trữ, thường được dùng để kết nối các tài nguyên, dữ liệu giữa các thiết bị với nhau trong cùng một mạng, tốc độ truyền tải rất cao nhanh hơn so với mạng LAN thông thường.
* Mạng VPN (Virtual Private Network) hay thường gọi là mạng riêng ảo giúp người dùng kết nối mạng an toàn khi tham gia vào mạng cộng đồng. Mô hình mạng này cho phép người dùng kết nối nhiều site khác nhau tương tự như mô hình mạng WAN.

**4. Các kiểu liên kết mạng**

**4.1. Mạng dạng hình sao (Star Topology)**

Star Topology là mạnh dạng hình sao có một trung tâm và các nút thông tin. Bên trong mạng, các nút thông tin là những trạm đầu cuối. Đôi khi nút thông tin cũng chính là hệ thống các máy tính và những thiết bị khác của mạng LAN. Khu vực trung tâm mạng dạng hình sao đảm nhận nhiệm vụ điều phối mọi hoạt động bên trong hệ thống. Bộ phận này mang các chức năng cơ bản là:
* Nhận dạng những cặp địa chỉ gửi và nhận có quyền chiếm tuyến thông tin và tiến hành quá trình liên lạc với nhau.
* Phê duyệt quá trình theo dõi và xử lý khi các thiết bị trao đổi thông tin với nhau.
* Gửi đi các thông báo về trạng thái của mạng

![image](https://user-images.githubusercontent.com/48250210/157406952-802f9568-6362-4dc9-ae80-5137c40792f8.png)


Ưu điểm của mạng hình sao
* Mô hình mạng LAN dạng hình sao đảm bảo quá trình hoạt động bình thường khi có một nút thông tin bị hư hỏng. Bởi kiểu mạng LAN này hoạt động dựa trên nguyên lý song song.
* Đặc điểm cấu trúc mạng vô cùng đơn giản. Điều này giúp cho thuật toán được điều khiển một cách ổn định hơn.
* Tùy vào nhu cầu sử dụng của User, mạnh dạng hình sao có thể được mở rộng hoặc thu hẹp theo ý muốn.

Nhược điểm của mạng hình sao
* Mặc dù có khả năng mở rộng mạng, nhưng điều này hoàn toàn phụ thuộc vào khả năng hoạt động của bộ phận trung tâm. Một khi trung tâm gặp phải sự cố, toàn bộ hệ thống mạng sẽ không thể hoạt động.
* Mạnh dạng hình sao yêu cầu phải được kết nối một cách độc lập với từng thiết bị ở nút thông tin đến trung tâm. Song song đó là khoảng cách kết nối từ thiết bị đến trung tâm cũng rất hạn chế và thường chỉ đạt khoảng 100m.

Nhìn một cách tổng quan, mô hình mạng dạng hình sao giúp cho các máy tính kết nối với bộ tập trung (HUB) bằng cáp xoắn. Kiểu kết nối trên cho phép việc kết nối máy tính trực tiếp với HUB mà không cần thông qua trục BUS. Nhờ vậy mà hệ thống mạng hạn chế tối đa các yếu tố gây ngưng trệ mạng trong quá trình hoạt động.

**4.2. Mạng hình tuyến (Bus Topology)**

Bus Topology cũng là một trong các kiểu kết nối mạng được sử dụng rất phổ biến. Mô hình này giúp cho máy chủ và hệ thống máy tính hoặc các nút thông tin được kết nối cùng nhau trên một trục đường dây cáp chính. Mục đích của sự kết nối này là nhằm chuyển tải các tín hiệu thông tin.

Thông thường ở phía hai đầu của dây cáp sẽ được bịt kín bằng thiết bị terminator. Riêng các tín hiệu và gói dữ liệu di chuyển trong dây cáp sẽ mang theo địa chỉ của điểm đến.

Ưu điểm nổi bật nhất của mạnh hình tuyến chính là việc tiết kiệm chiều dài dây cáp và rất dễ lắp đặt. Nhưng mô hình mạng cũng tồn tại những khuyết điểm điển hình như dễ gây ra sự ùn tắc giao thông trong quá trình di chuyển dữ liệu số lượng lớn. Một khi có sự cố hư hỏng xảy ra ở đoạn cáp nào đó, user sẽ rất khó phát hiện. Vì vậy bạn bắt buộc phải tạm ngừng hoạt động trên đường dây và toàn bộ hệ thống để tiến hành sửa chữa.

![image](https://user-images.githubusercontent.com/48250210/157407365-59f68fee-48c5-48f1-b012-9a59b498e435.png)

**4.3. Mạnh dạng vòng (Ring Topology)**

Mô hình mạng LAN dạng vòng được bố trí theo dạng xoay vòng. Trong trường hợp này, đường dây cáp sẽ được thiết kế thành vòng tròn khép kín. Các tín hiệu chạy quanh vòng tròn sẽ di chuyển theo một chiều nào đó cố định.

Bên trong mạng dạng vòng, tại mỗi một thời điểm nhất định chỉ có một nút có khả năng truyền tín hiệu trong số hệ thống các nút thông tin. Song song đó, dữ liệu truyền đi cũng phải kèm theo địa chỉ đến tại mỗi trạm tiếp nhận.

Ưu điểm của mạng dạng vòng chính là có thể nới rộng hệ thống mạng ra xa. Số lượng dây dẫn cần thiết để sử dụng cũng ít hơn so với hai mô hình mạng kể trên. Tuy nhiên khuyết điểm lớn nhất của kiểu mạng dạng vòng chính là đường dây phi khép kín. Một khi tín hiệu bị ngắt tại một điểm nào đó, toàn bộ hệ thống cũng sẽ ngừng hoạt động.

![image](https://user-images.githubusercontent.com/48250210/157407455-a7a0aa47-2137-447e-adf0-79c1a342cf81.png)

**4.4. Mạng dạng lưới (Mesh Topology)**

Mesh Topology hay còn gọi là mạnh dạng lưới. Sản phẩm có cấu trúc dạng lưới được ứng dụng phổ biến trong các mạng nắm giữ vai trò quan trọng và không thể bị ngừng hoạt động. Điển hình như hệ thống mạng của nhà máy điện nguyên tử hoặc hệ thống mạng an ninh, quốc phòng.

Đối với mạng dạng lưới, mỗi một thiết bị máy tính sẽ được kết nối với tất cả cả các máy tính còn lại. Đó cũng là cấu trúc quen thuộc của mạng Internet.

![image](https://user-images.githubusercontent.com/48250210/157408744-e5eef765-069e-49ba-9a48-ad8720351d48.png)

**5. Các phương pháp truyền tin**

**5.1. Mạng chuyển mạch kênh (Circuit Switching Network)**

Khi có hai trạm cần trao đổi thông tin với nhau thì giữa chúng sẽ được thiết lập một "kênh" cố định và được duy trì cho đến khi một trong hai bên ngắt kết nối. Dữ liệu chỉ được truyền theo con đường cố định này. Kỹ thuật chuyển mạch kênh được sử dụng trong các kết nối ATM (Asynchronous Transfer Mode) và Dial-up ISDN (Integrated Services Digital Networks). Ví dụ về mạng chuyển mạch kênh là mạng điện thoại.

Ưu điểm là kênh truyền được dành riêng trong suốt quá trình giao tiếp do đó tốc độ truyền dữ liệu được bảo đảm. Điều này là đặc biệt quan trọng đối với các ứng dụng thời gian thực như audio và video.

Nhược điểm là phải tốn thời gian để thiết lập đường truyền cố định giữa hai trạm; hiệu suất sử dụng đường truyền không cao, vì có lúc trên kênh không có dữ liệu truyền của hai trạm kết nối, nhưng các trạm khác không được sử dụng kênh truyền này.

**5.2. Mạng chuyển mạch thông báo (Message Switching Network)**

Không giống chuyển mạch kênh, chuyển mạch thông báo không thiết lập liên kết dành riêng giữa hai trạm giao tiếp mà thay vào đó mỗi thông báo được xem như một khối độc lập bao gồm cả địa chỉ nguồn và địa chỉ đích. Mỗi thông báo sẽ được truyền qua các trạm trong mạng cho đến khi nó đến được địa chỉ đích, mỗi trạm trung gian sẽ nhận và lưu trữ thông báo cho đến khi trạm trung gian kế tiếp sẵn sàng để nhận thông báo sau đó nó chuyển tiếp thông báo đến trạm kế tiếp, chính vì lý do này mà mạng chuyển mạch thông báo còn có thể được gọi là mạng lưu và chuyển tiếp (Store and Forward Network). Một ví dụ điển hình về kỹ thuật này là dịch vụ thư điện tử (e-mail), nó được chuyển tiếp qua các trạm cho đến khi tới được đích cần đến.

Ưu điểm là cung cấp một sự quản lý hiệu quả hơn đối với sự lưu thông của mạng, bằng cách gán các thứ tự ưu tiên cho các thông báo và đảm bảo các thông báo có độ ưu tiên cao hơn sẽ được lưu chuyển thay vì bị trễ do quá trình lưu thông trên mạng; giảm sự tắc nghẽn trên mạng, các trạm trung gian có thể lưu giữ các thông báo cho đến khi kênh truyền rảnh mới gửi thông báo đi; tăng hiệu quả sử dụng kênh truyền, với kỹ thuật này các trạm có thể dùng chung kênh truyền.

Nhược điểm là độ trễ do việc lưu trữ và chuyển tiếp thông báo là không phù hợp với các ứng dụng thời gian thực, Các trạm trung gian phải có dung lượng bộ nhớ rất lớn để lưu giữ các thông báo trước khi chuyển tiếp nó tới một trạm trung gian khác (kích thước của các thông báo không bị hạn chế).

**5.3. Mạng chuyển mạch gói (Packet Switching Network)**

Kỹ thuật này được đưa ra nhằm tận dụng các ưu điểm và khắc phục những nhược điểm của hai kỹ thuật trên, đối với kỹ thuật này các thông báo được chia thành các gói tin (packet) có kích thước thay đổi, mỗi gói tin bao gồm dữ liệu, địa chỉ nguồn, địa chỉ đích và các thông tin về địa chỉ các trạm trung gian. Các gói tin riêng biệt không phải luôn luôn đi theo một con đường duy nhất, điều này được gọi là chọn đường độc lập (independent routing).

Ưu điểm là dải thông có thể được quản lý bằng cách chia nhỏ dữ liệu vào các đường khác nhau trong trường hợp kênh truyền bận; nếu một liên kết bị sự cố trong quá trình truyền thông thì các gói tin còn lại có thể được gửi đi theo các con đường khác; điểm khác nhau cơ bản giữa kỹ thuật chuyển mạch thông báo và kỹ thuật chuyển mạch gói là trong kỹ thuật chuyển mạch gói các gói tin được giới hạn về độ dài tối đa điều này cho phép các trạm chuyển mạch có thể lưu giữ các gói tin vào bộ nhớ trong mà không phải đưa ra bộ nhớ ngoài do đó giảm được thời gian truy nhập và tăng hiệu quả truyền tin.

Nhược điểm là khó khăn của phương pháp chuyển mạch gói cần giải quyết là tập hợp các gói tin tại nơi nhận để tạo lại thông báo ban đầu cũng như xử lý việc mất các gói tin.
