# 1. Mô hình OSI

Mô hình OSI hay Open Systems Interconnection có nhiệm vụ thiết lập kết nối giữa các thiết bị giao tiếp trên toàn cầu. OSI được coi là mã nguồn mở vì khả năng phù hợp với mọi hệ thống mạng của nó.

Mô hình cung cấp một tiêu chuẩn dưới dạng kiến trúc phân tầng cho phép các hệ thống khác nhau có thể giao tiếp được với nhau, trong đó gồm có 7 tầng với những cấu trúc và chức năng riêng đã được định nghĩa sẵn.

Mỗi tầng có một chức năng riêng và chỉ giao tiếp với các tầng tiếp giáp với nó, mọi sự thay đổi về vị trí các tầng trong kiến trúc trên đều không được chấp nhận:

+ Tầng ứng dụng (Application Layer)

Là tầng duy nhất tương tác trực tiếp với tiến trình ứng dụng, có trách nhiệm cung cấp giao diện cũng như các thao tác dữ liệu giúp người dùng và phần mềm ứng dụng tương tác với nhau

Một số giao thức có trong tầng ứng dụng như: HTTP, FTP, POP, DHCP,…

+ Tầng trình diễn (Presentation Layer)

Là tầng ngay dưới tầng ứng dụng, nó đáp ứng các nhu cầu của tầng ứng dụng như phiên dịch, mã hóa, giải mã, nén dữ liệu

Phiên dịch dữ liệu theo cú pháp mà ứng dụng có thể hiểu, mã hóa dữ liệu gửi đi cũng như giải mã dữ liệu nhận, nén dữ liệu trước khi truyền xuống tầng phiên

+ Tầng phiên (Session Layer) 

Là tầng ngay dưới tầng trình diễn, cung cấp các nhu cầu dịch vụ cho tầng trình diễn. Tầng phiên chịu trách nhiệm đóng và mở luồng giao tiếp giữa hai thiết bị, thời gian giữa mở và đóng được gọi là phiên. Nó đảm bảo phiên mở đủ lâu để dữ liệu có thể gửi đi và đóng đủ nhanh để tránh lãng phí tài nguyên

Ngoài ra, tầng phiên cung cấp dịch vụ đánh dấu điểm hoàn thành. Ví dụ khi bạn truyền một file dung lượng 10 GB, cứ sau mỗi 1GB lại đánh dấu điểm hoàn thành 1 lần thì khi bị mất kết nối hoặc tạm ngừng ở điểm 6GB rồi truyền lại thì chỉ cần truyền 4GB phần dữ liệu còn lại chưa được truyền

+ Tầng giao vận (Transport Layer) 

Là tầng ngay dưới tầng phiên, nó đáp ứng các nhu cầu của tầng phiên. Tầng giao vận chịu trách nhiệm thiết lập kết nối giữa hai thiết bị, nó nhận dữ liệu từ tầng phiên rồi xử lý để gửi xuống tầng dưới cũng như nhận dữ liệu từ tầng dưới xử lý để chuyển lên tầng phiên

Tầng giao vận có thể cung cấp dịch vụ kiểm soát luồng và kiểm soát lỗi để đảm bảo dữ liệu được chuyển đi được chính xác và không quá tải bên nhận

+ Tầng mạng (Network Layer) 

Đáp ứng các nhu cầu của tầng giao vận, chịu trách nhiệm giúp dữ liệu có thể truyền giữa các thiết bị ở các mạng khác nhau, nếu 2 thiết bị cùng trong một mạng thì ta không cần thiết phải có tầng này

Tầng mạng còn cung cấp các thuật toán dò đường cho các bộ định tuyến để xác định đường truyền vật lý tốt nhất cho dữ liệu

+ Tầng liên kết dữ liệu (Data Link Layer) 

Đáp ứng các nhu cầu của tầng mạng, về cơ bản tầng này giống với tầng mạng nhưng nó hỗ trợ dữ liệu có thể được truyền đi giữa các thiết bị trong cùng một mạng

+ Tầng vật lý (Physical Layer) 

Bao gồm các thiết bị phần cứng giúp truyền tải dữ liệu như cáp, bộ định tuyến,…. Ở tầng này dữ liệu được truyền tải dưới dạng bit 0 và 1

![image](https://user-images.githubusercontent.com/48250210/157418903-7049b632-7685-415c-9428-cd459f9fc5ac.png)

    - Ưu điểm của mô hình OSI 
      + Mỗi tầng có 1 cấu trúc và chức năng riêng nên dễ dàng xây dựng và sửa chữa
      + Có thể tích hợp trong nhiều mạng lưới khác nhau
      + Hỗ trợ kết nối có liên kết và kết nối phi liên kết

    - Nhược điểm của mô hình OSI
      + Tầng phiên và tầng trình diễn thường không được sử dụng nhiều so với các tầng khác vì chức năng hạn hẹp của nó
      + Không hỗ trợ các giao thức, không định nghĩa bất kì giao thức nào
      + Nhiều dịch vụ trùng lặp tại các tầng, ví dụ tầng mạng và tầng liên kết dữ liệu
      + Các tầng không thể hoạt động song song, tầng dưới phải chờ dữ liệu từ tầng trên

# 2. Mô hình TCP/IP

TCP/IP là viết tắt của Transmission Control Protocol/Internet Protocol. Đây là một bộ các giao thức truyền thông được sử dụng để kết nối các thiết bị mạng với nhau trên Internet. 

TCP/IP cũng có thể được sử dụng như một giao thức truyền thông trong mạng máy tính riêng (mạng nội bộ).

Trong đó, bộ Giao thức internet - một tập hợp các quy tắc và thủ tục - thường gọi là TCP/IP. Trong đó, TCP và IP là hai giao thức chính bên cạnh những giao thức khác trong bộ. 

Bộ giao thức TCP/IP hoạt động như một lớp trừu tượng giữa các ứng dụng internet và hạ tầng router/switch.

Cũng vậy, TCP/IP chỉ định cách dữ liệu được trao đổi qua internet. Nó thực hiện bằng cách cung cấp thông tin liên lạc đầu cuối. Từ đó xác định cách nó được chia thành các packet, xác định địa chỉ, truyền dẫn, định tuyến và nhận dữ liệu. 

TCP/IP được thiết kế để đảm bảo độ tin cậy, nó có khả năng khôi phục tự động khi gặp sự cố trong quá trình truyền dữ liệu.

Giao thức TCP/IP được chia thành 4 tầng mạng:

+ Tầng ứng dụng
 
Đảm nhận vai trò giao tiếp dữ liệu giữa 2 máy khác nhau thông qua các dịch vụ mạng khác nhau (duyệt web, chay hay các giao thức trao đổi dữ liệu SMTP, SSH, FTP…)

Dữ liệu khi đến được tầng này sẽ được định dạng để kết nối theo kiểu Byte nối Byte. Các thông tin định tuyến tại đây sẽ giúp xác định đường đi đúng của một gói tin

+ Tầng mạng

Đảm nhận việc truyền tải dữ liệu một cách hợp lý. Nhiệm vụ của tầng Internet là xử lý các gói tin, sau đó kết nối với các mạng độc lập để vận chuyển các gói dữ liệu đã được mã hóa qua các ranh giới mạng. Tầng Internet cũng bao gồm nhiều giao thức như giao thức IP, ICMP

+ Tầng giao vận 

Tầng dữ liệu hoạt động thông qua hai giao thức chính là TCP (Transmission Control Protocol) và UDP (User Datagram Protocol)

Nhiệm vụ của tầng giao vận là duy trì liên lạc đầu cuối trên toàn mạng. Ở tầng này, TCP và UDP sẽ hỗ trợ nhau phân luồng dữ liệu. Trong nhiều trường hợp giao thức UDP sẽ được thay thế TCP

+ Tầng vật lý 

Tầng vật lý (còn được gọi là tầng liên kết dữ liệu) là tầng thấp nhất trong mô hình TCP/IP. Tầng này chịu trách nhiệm truyền dữ liệu giữa hai thiết bị trong cùng một mạng 

Tại đây, các gói dữ liệu được đóng vào khung (gọi là Frame) và được định tuyến đi đến đích đã được chỉ định ban đầu

![image](https://user-images.githubusercontent.com/48250210/157420600-68cdd72e-f7a3-4cd3-8b29-3cfcf266849b.png)

    - Ưu điểm của mô hình TCP/IP
        + Thiết lập kết nối giữa các loại máy tính khác nhau
        + Hoạt động độc lập với hệ điều hành
        + Hỗ trợ nhiều giao thức định tuyến
        + Kiến trúc client - server, khả năng mở rộng cao
        + Có thể hoạt động độc lập
        + Hỗ trợ nhiều giao thức định tuyến
        + Nhẹ, không gây nhiều áp lực với máy tính hay mạng

    - Nhược điểm của mô hình TCP/IP
        + Việc cài đặt khá phức tạp, khó để quản lý
        + Tầng transport không đảm bảo việc phân phối các gói tin
        + Các giao thức trong TCP/IP không dễ để có thể thay thế
        + Không tách biệt rõ ràng các khái niệm về dịch vụ, giao diện và giao thức. Do đó nó không hiệu quả để mô tả các công nghệ mới trong mạng mới
        + Dễ bị tấn công SYN  - một kiểu tấn công từ chối dịch vụ

# 3. So sánh mô hình OSI và TCP/IP

**3.1 Điểm tương đồng giữa mô hình OSI và TCP/IP**

+ Chia sẻ kiến trúc chung

Cả 2 mô hình đều là mô hình logic và có kiến trúc tương tự vì cả 2 mô hình đều được xây dựng dựa trên các lớp

+ Xác định tiêu chuẩn 

Cả 2 lớp đều có các tiêu chuẩn xác định và chúng cũng cung cấp khuôn khổ được sử dụng để thực hiện các tiêu chuẩn và thiết bị

+ Quy trình khắc phục sự cố được đơn giản hóa

Cả 2 mô hình đã đơn giản hóa quá trình khắc phục sự cố bằng cách chia nhỏ chức năng phức tạp thành các thành phần đơn giản hơn

+ Các tiêu chuẩn được xác định trước

Các tiêu chuẩn và giao thức đã được xác định trước, những mô hình này không xác định lại chúng, chỉ tham khảo hoặc sử dụng lại chúng. Ví dụ, các tiêu chuẩn Ethernet đã được IEEE xác định trước khi phát triển các mô hình 

+ Cả 2 đều có chức năng tương tự của các lớp Transport và Network

Chức năng được thực hiện giữa lớp Presentation và lớp Network tương tự như chức năng được thực hiện ở lớp Transport

**3.2. Sự khác biệt giữa mô hình OSI và TCP/IP**

![image](https://user-images.githubusercontent.com/48250210/157420223-26e2517f-5b9d-41e1-976d-512f04d82637.png)

# 4. Kết luận

Chúng ta có thể kết luận rằng mô hình TCP/IP đáng tin cậy đối với mô hình OSI, TCP/IP được sử dụng cho kết nối đầu cuối để truyền dữ liệu qua Internet. TCP/IP mạnh mẽ, linh hoạt, hữu hình và cũng gợi ý cách dữ liệu nên được gửi qua web. Lớp vận chuyển của Mô hình TCP/IP kiểm tra xem dữ liệu đã đến theo thứ tự chưa, nó có lỗi hay không, các gói bị mất có được gửi hay không, xác nhận có được nhận hay không, v.v…
