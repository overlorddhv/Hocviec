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
