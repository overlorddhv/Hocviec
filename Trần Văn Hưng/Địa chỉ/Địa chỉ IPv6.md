# Địa chỉ IPv6 là gì?

IPv6 (Internet Protocol version 6) là phiên bản mới nhất của Giao thức Internet (IP), giao thức truyền thông cung cấp một hệ thống định vị vị trí cho các máy tính trên mạng và định tuyến lưu lượng trên Internet. Trong thời đại Internet bùng nổ và trở nên phổ biến, lượng địa chỉ IPv4 ngày càng cạn kiệt, bộc lộ các hạn chế đối với việc phát triển các loại hình dịch vụ hiện đại trên Internet, không đáp ứng đủ nhu cầu người dùng. Được IETF tạo ra để thay thế và khắc phục những lỗi của IPv4,  IPv6  ra đời.

# Phân loại địa chỉ IPv6

Một địa chỉ IPv6 có thể được phân thành 1 trong 3 loại như sau:
- Unicast
Một địa chỉ unicast được định nghĩa duy nhất trên một cổng của một node IPv6. Một gói tin được gởi đến một địa chỉ unicast được đưa đến cổng được định nghĩa bởi địa chỉ đó.
- Multicast
Một địa chỉ multicast định nghĩa một nhóm các cổng IPv6. Một gói tin gởi đến địa chỉ multicast được xử lý bởi tất cả những thành viên của nhóm multicast.
- Anycast
Một địa chỉ anycast được đăng kí cho nhiều cổng (trên nhiều node). Một gói tin được gởi đến một địa chỉ anycast là được chuyển đến chỉ một trong số các cổng này.

# Cấu trúc của địa chỉ IPv6

Vẫn giữ đặc trưng là một chuỗi tập hợp của các con số có giới hạn, được sắp xếp thành 1 dãy số có quy luật, địa chỉ IPv6  có chiều dài ấn tượng:128bit. Địa chỉ IPv6 được biểu diễn dưới dạng các cụm số hexa được ngăn thành 8 phần, mỗi phần có chiều dài 16bit và được ngăn bởi dấu “:”. Với 128 bit chiều dài, không gian địa chỉ IPv6 gồm 2128 địa chỉ, cung cấp một lượng địa chỉ khổng lồ cho hoạt động Internet.

# Ưu điểm của địa chỉ IPv6

- Không gian địa chỉ lớn hơn và dễ dàng quản lý hơn: Tăng từ 32bit lên 128bit.
- Header của giao thức được cải tiến: Cải thiện hiệu suất chuyển tiếp gói tin.. Khôi phục lại nguyên lý kết nối đầu cuối-đầu cuối của Internet và loại bỏ hoàn toàn công nghệ NAT
- Quản trị TCP/IP dễ dàng hơn:  IPv6 được thiết kế với khả năng tự động cấu hình mà không cần sử dụng máy chủ DHCP, hỗ trợ nhiều trong việc giảm cấu hình thủ công.
- Cấu trúc định tuyến tốt hơn: Định tuyến IPv6 được thiết kế hoàn toàn phân cấp. Khả năng QoS (Quality of service) giúp đánh dấu QoS cho các gói tin và dán nhãn để giúp xác định những traffic cần được ưu tiên.
- Hỗ trợ tốt hơn Multicast: Tăng cường sử dụng truyền thông một chiều hiệu quả.
- Hỗ trợ bảo mật tốt hơn: Mã hóa và xác thực truyền thông.
- Tính di động: Dễ dàng hơn khi xử lý với thiết bị di động hay chuyển vùng
- Jumbograms: Hỗ trợ các packet payload cực lớn cho hiệu quả cao hơn.
- Anycast: Dịch vụ dự phòng sử dụng những địa chỉ không có cấu trúc đặc biệt.

# Sự khác biệt giữa địa chỉ IPv4 và địa chỉ IPv6

- IPv6 có triển khai IP Security (IPSec) để tăng bảo mật. Nhưng công nghệ này cũng có triển khai và tích hợp hoàn toàn vào IPv4 tùy thuộc vào đơn vị IPS.
- Về địa chỉ: IPv4 32Bit trong khi IPv6 có đến 128Bit.
- Địa chỉ IPv4 chỉ đánh số, trong khi đó, IPv6 có cả chữ và số
- IPv4 tách nhị phân bằng dấu chấm (.), IPv6 lại tách bằng dấu 2 chấm (:)
- Header của IPv4 là 12 trường còn của IPv6 chỉ 8 trường
- IPv4 sử dụng ARP (Address Resolution Protocol) để ánh xạ đến địa chỉ MAC, trong khi IPv6 sử dụng NDP (Neighbour Discovery Protocol) để ánh xạ đến MAC.

