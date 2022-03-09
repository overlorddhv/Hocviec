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
* LAN

Mạng LAN là viết tắt của từ tiếng Anh Local Area Network được tạm dịch là mạng máy tính nội bộ, giao tiếp này cho phép các thiết bị kết nối với nhau để cùng làm việc và chia sẻ dữ liệu. Kết nối này được thực hiện thông qua sợi cáp LAN hay Wifi (không dây) trong không gian hẹp, chính vì thế nó chỉ dùng được ở một phạm vi giới hạn như phòng làm việc, trong nhà, trường học…

![image](https://user-images.githubusercontent.com/48250210/157400600-4c75bc6b-c68b-49ca-b9e3-49e00a353786.png)

Ưu điểm của mạng LAN: Tốc độ truyền tải cao, hỗ trợ kết nối được nhiều thiết bị nhanh chóng. Tuy bị giới hạn về phạm vi kết nối nhưng chi phí, sử dụng dây ít, dễ dàng quản trị.

* MAN

 Mạng MAN (Metropolitan Area Network) hay còn gọi là mạng đô thị liên kết từ nhiều mạng LAN qua dây cáp, các phương tiện truyền dẫn khác,... Khả năng kết nối trong phạm vi lớn như trong một thị trấn, thành phố, tỉnh.

Mô hình mạng MAN thường được dùng chủ yếu cho đối tượng là tổ chức, doanh nghiệp nhiều chi nhánh, nhiều bộ phận kết nối với nhau.

![image](https://user-images.githubusercontent.com/48250210/157401135-4a63442b-1a08-4fe8-a242-57a15387ab55.png)

Mạng Man thường được sử dụng cho doanh nghiệp vì mô hình này này cung cấp nhiều loại dịch vụ như kết nối đường truyền qua voice (thoại), data (dữ liệu), video(hình ảnh), triển khai các ứng dụng dễ dàng.

Ưu điểm của mạng MAN: Phạm vi kết nối lớn giúp tương tác giữa các bộ phận doanh nghiệp dễ dàng, hiệu quả,chi phí thấp, tốc độ truyền tải ổn định, bảo mật thông tin, quản lý đơn giản.

* WAN

Mạng WAN ((Wide Area Network) hay còn gọi là mạng diện rộng được kết hợp giữa các mạng đô thị bao gồm cả mạng MAN và mạng LAN thông qua thiết bị vệ tinh, cáp quang, cáp dây điện.

![image](https://user-images.githubusercontent.com/48250210/157401988-10236dbf-be36-44cc-9fa2-5bbbac9b10c0.png)

Mạng diện rộng được tạo ra nhằm kết nối trên một diện lớn có quy mô trên quốc gia. Giao thức sử dụng trong mạng WAN là TCP/IP, đường truyền băng thông thay đổi tùy vào vị trí lắp đặt.

Ưu điểm của mạng WAN: Khả năng kết nối rộng lớn, không bị giới hạn tín hiệu, dễ dàng chia sẻ thông tin, lưu trữ dữ liệu. Tốc độ truyền tải tương đối tùy vào mỗi khu vực hoặc thiết bị truyền dẫn khác nhau.

=> có thể so sánh qua bảng sau:

![image](https://user-images.githubusercontent.com/48250210/157402459-6b6db3c1-e9c9-48c0-8157-4429af59c5d6.png)

Ngoài ra còn có các loại mạng khác như:
* PAN (Personal Area Network): hay còn gọi là mạng cá nhân khả năng kết nối phạm vi nhỏ thường được dùng thông qua các thiết bị định tuyến. Khả năng định tuyến này giúp truyền dẫn dữ liệu trên thiết bị đến đích.
* SAN (Storage Area Networking): hay còn gọi là mạng lưu trữ, thường được dùng để kết nối các tài nguyên, dữ liệu giữa các thiết bị với nhau trong cùng một mạng, tốc độ truyền tải rất cao nhanh hơn so với mạng LAN thông thường.
* Mạng VPN (Virtual Private Network) hay thường gọi là mạng riêng ảo giúp người dùng kết nối mạng an toàn khi tham gia vào mạng cộng đồng. Mô hình mạng này cho phép người dùng kết nối nhiều site khác nhau tương tự như mô hình mạng WAN.

**4. Các mô hình mạng**
