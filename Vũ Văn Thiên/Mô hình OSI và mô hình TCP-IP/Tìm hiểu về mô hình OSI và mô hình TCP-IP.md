# Mô hình OSI là gì?

Mô hình OSI (Open system interconnection – Mô hình kết nối các hệ thống mở) là một thiết kế dựa vào nguyên lý tầng cấp, lý giải một cách trừu tượng kỹ thuật kết nối truyền thông giữa các máy vi tính và thiết kế giao thức mạng giữa chúng. Mô hình này được phát triển thành một phần trong kế hoạch OSI (Open Systems Interconnection) do ISO và IUT-T khởi xướng. Nó còn được gọi là Mô hình bảy tầng của OSI.

**Mô hình OSI dùng để làm gì?**

Mô hình OSI được tạo ra với mục đích là cho phép sự tương giao (interoperability) giữa các hệ máy (platform) đa dạng được cung cấp bởi các nhà sản xuất khác nhau. Mô hình cho phép tất cả các thành phần của mạng hoạt động hòa đồng, bất kể thành phần ấy do ai tạo dựng. Vào những năm cuối thập niên 1980, ISO đã tiến cử việc thực thi mô hình OSI như một tiêu chuẩn mạng.

## Các giao thức trong mô hình OSI

Trong mô hình OSI có hai loại giao thức được sử dụng: giao thức hướng liên kết (Connection – Oriented) và giao thức không liên kết (Connectionless).

**Giao thức hướng liên kết**

Trước khi truyền dữ liệu, các thực thể đồng tầng trong hai hệ thống cần phải thiết lập một liên kết logic. Chúng thương lượng với nhau về tập các tham số sẽ sử dụng trong giai đoạn truyền dữ liệu, cắt/hợp dữ liệu, liên kết sẽ được hủy bỏ. Thiết lập liên kết logic sẽ nâng cao độ tin cậy và an toàn trong quá trình trao đổi dữ liệu.

**Giao thức không liên kết**

Dữ liệu được truyền độc lập trên các tuyến khác nhau. Với các giao thức không liên kết chỉ có giai đoạn duy nhất truyền dữ liệu


## Vai trò và chức năng chủ yếu các tầng

**Vai trò và chức năng tầng ứng dụng (Application Layer)**

Tầng ứng dụng là tầng gần với người sử dụng nhất. Nó cung cấp phương tiện cho người dùng truy nhập các thông tin và dữ liệu trên mạng thông qua chương trình ứng dụng. Tầng này là giao diện chính để người dùng tương tác với chương trình ứng dụng, và qua đó với mạng.

**Vai trò và chức năng tầng trình bày (Presentation Layer)**

Lớp trình diễn hoạt động như tầng dữ liệu trên mạng. lớp này trên máy tính truyền dữ liệu làm nhiệm vụ dịch dữ liệu được gửi từ tầng Application sang dạng Fomat chung. Và tại máy tính nhận, lớp này lại chuyển từ Fomat chung sang định dạng của tầng Application

- Lớp thể hiện thực hiện các chức năng sau:
  - Dịch các mã kí tự từ ASCII sang EBCDIC.
  - Chuyển đổi dữ liệu. 
  - Nén dữ liệu để giảm lượng dữ liệu truyền trên mạng. 
  - Mã hoá và giải mã dữ liệu để đảm bảo sự bảo mật trên mạng.

**Vai trò và chức năng tầng phiên (Session Layer)**

Tầng Session kiểm soát các (phiên) hội thoại giữa các máy tính. Tầng này thiết lập, quản lý và kết thúc các kết nối giữa trình ứng dụng địa phương và trình ứng dụng ở xa

Hỗ trợ hoạt động song công (duplex) hoặc bán song công (half-duplex) hoặc đơn công (Single) và thiết lập các qui trình đánh dấu điểm hoàn thành (checkpointing) – giúp việc phục hồi truyền thông nhanh hơn khi có lỗi xảy ra, vì điểm đã hoàn thành đã được đánh dấu – trì hoãn (adjournment), kết thúc (termination) và khởi động lại (restart).

Mô hình OSI uỷ nhiệm cho tầng này trách nhiệm “ngắt mạch nhẹ nhàng” (graceful close) các phiên giao dịch (một tính chất của giao thức kiểm soát giao vận TCP) và trách nhiệm kiểm tra và phục hồi phiên, đây là phần thường không được dùng đến trong bộ giao thức TCP/IP.

**Vai trò và chức năng tầng vận chuyển (Transport Layer)**

Lớp này thực hiện các chức năng nhận thông tin từ tầng Session chia thành các gói nhỏ hơn và truyền xuống lớp dưới, hoặc nhận thông tin từ lớp dưới chuyển lên phục hồi theo cách chia của hệ phát (Fragmentation and Reassembly).

Nhiệm vụ quan trọng nhất của lớp vận chuyển là đảm bảo chuyển số liệu chính xác giữa hai thực thể thuộc tầng Session (end–to–end control). Để làm được việc đó, ngoài chức năng kiểm tra số tuần tự phát, thu, kiểm tra và phát hiện, xử lý lỗi, lớp vận chuyển còn có chức năng điều khiển lưu lượng số liệu để đồng bộ giữa thể thu và phát và tránh tắc ngẽn số liệu khi chuyển qua lớp mạng.

Ngoài ra, nhiều thực thể lớp phiên có thể trao đổi số liệu trên cùng một kết nối lớp mạng (multIPlexing)

**Vai trò và chức năng tầng mạng (Network Layer)**

Nhiệm vụ của lớp mạng là đảm bảo chuyển chính xác số liệu giữa các thiết bị cuối trong mạng. Để làm được việc đó, phải có chiến lược đánh địa chỉ thống nhất trong toàn mạng. Mỗi thiết bị cuối và thiết bị mạng có một địa chỉ mạng xác định. Số liệu cần trao đổi giữa các thiết bị cuối được tổ chức thành các gói (Packet) có độ dài thay đổi và được gán đầy đủ địa chỉ nguồn (source address) và địa chỉ đích (destination address).

Lớp mạng đảm bảo việc tìm đường tối ưu cho các gói dữ liệu bằng các giao thức chọn đường dựa trên các thiết bị chọn đường (Router). Ngoài ra, lớp mạng có chức năng điều khiển lưu lượng số liệu trong mạng để tránh xảy ra tắc nghẽn bằng cách chọn các chiến lược tìm đường khác nhau để quyết định việc chuyển tiếp các gói số liệu.

**Vai trò và chức năng tầng liên kết dữ liệu (Data Link Layer)**

Lớp này đảm bảo việc biến đổi các tin dạng bit nhận được từ lớp dưới (vật lý) sang khung số liệu, thông báo cho hệ phát kết quả thu được sao cho các thông tin truyền lên cho tầng Network không có lỗi.

Các thông tin truyền ở tầng Physical có thể làm hỏng các thông tin khung số liệu (frame error). Phần mềm mức hai sẽ thông báo cho mức một tryền lại các thông tin bị mất/lỗi.

**Vai trò và chức năng tầng vật lý (Physical Layer)**

Là tầng thứ nhất trong bảy tầng Mô hình OSI, tầng này chịu trách nhiệm ứng đối với các đòi hỏi về dịch vụ từ Datalink Layer.

Chức năng và dịch vụ chính mà tầng vật lý giải quyết là

Thiết lập hoặc ngắt mạch kết nối điện (electrical connection) với một phương tiện truyền thông (transmission medium)

Tham gia vào quy trình mà trong đó các tài nguyên truyền thông được chia sẻ hiệu quả giữa nhiều người dùng. Chẳng hạn giải quyết tranh chấp tài nguyên (contention) và điều khiển lưu lượng

Điều biến (modulation), hoặc biến đổi giữa biểu diễn dữ liệu số (digital data) của các thiết bị người dùng và các tín hiệu tương ứng được truyền qua kênh truyền thông (communication channel)

## Phương thức hoạt động của mô hình OSI

Mỗi tầng trong mô hình OSI, có hai phương thức hoạt động chính được áp dụng đó là: phương thức hoạt động có liên kết (connection–oriented) và không có liên kết (connectionless).
Với phương thức có liên kết, trước khi truyền dữ liệu cần thiết phải thiết lập một liên kết logic giữa các thực thể cùng lớp (layer). Còn với phương thức không có liên kết, thì không cần lập liên kết logic và mỗi đơn vị dữ liệu trước hoặc sau đó.

- Phương thức có liên kết, quá trình truyền dữ liệu phải trải qua 3 giai đoạn theo thứ tự:
  - Thiết lập liên kết: hai thực thể đồng mức ở hai hệ thống thương lượng với nhau về tập các tham số sẽ được sử dụng trong giai đoạn sau.
  - Truyền dữ liệu: dữ liệu được truyền với các cơ chế kiểm soát và quản lý.
  - Hủy bỏ liên kết: giải phóng các tài nguyên hệ thống đã cấp phát cho liên kết để dùng cho các liên kết khác.

**Những ưu điểm của OSI đó là:**
- OSI phân thành nhiều tầng nhỏ và đơn giản hơn.
- OSI chuẩn hóa các thành phần mạng để phát triển dễ dàng hơn.
- OSI chuẩn hóa giao diện giữa các tầng.
- Dữ liệu được truyền nhanh chóng và dễ dàng hơn.

**Nhược điểm**
- Tầng phiên và tầng trình diễn thường không được sử dụng nhiều so với các tầng khác vì chức năng hạn hẹp của nó.
- Không hỗ trợ các giao thức, không định nghĩa bất kì giao thức nào.
- Nhiều dịch vụ trùng lặp tại các tầng, ví dụ tầng mạng và tầng liên kết dữ liệu.
- Các tầng không thể hoạt động song song, tầng dưới phải chờ dữ liệu từ tầng trên.

# Mô hình TCP/IP là gì?

TCP/ IP (Transmission Control Protocol/ Internet Protocol - Giao thức điều khiển truyền nhận/ Giao thức liên mạng), là một bộ giao thức trao đổi thông tin được sử dụng để truyền tải và kết nối các thiết bị trong mạng Internet. TCP/IP được phát triển để mạng được tin cậy hơn cùng với khả năng phục hồi tự động.
Cụ thể hơn, TCP/IP chỉ rõ cho chúng ta cách thức đóng gói thông tin (còn được gọi là gói tin ), được gửi và nhận bởi các máy tính có kết nối với nhau.

## Chức năng của các tầng trong mô hình TCP/IP

Một mô hình TCP/IP tiêu chuẩn bao gồm 4 lớp được chồng lên nhau, bắt đầu từ tầng thấp nhất là Tầng vật lý (Physical) → Tầng mạng (Network) → Tầng giao vận (Transport) và cuối cùng là Tầng ứng dụng (Application).

**Tầng 4 - Tầng Ứng dụng (Application) **

Đây là lớp giao tiếp trên cùng của mô hình. Đúng với tên gọi, tầng Ứng dụng đảm nhận vai trò giao tiếp dữ liệu giữa 2 máy khác nhau thông qua các dịch vụ mạng khác nhau (duyệt web, chat, gửi email, một số giao thức trao đổi dữ liệu: SMTP, SSH, FTP,...). Dữ liệu khi đến đây sẽ được định dạng theo kiểu Byte nối Byte, cùng với đó là các thông tin định tuyến giúp xác định đường đi đúng của một gói tin.

**Tầng 3 - Tầng Giao vận (Transport) **

Chức năng chính của tầng 3 là xử lý vấn đề giao tiếp giữa các máy chủ trong cùng một mạng hoặc khác mạng được kết nối với nhau thông qua bộ định tuyến. Tại đây dữ liệu sẽ được phân đoạn, mỗi đoạn sẽ không bằng nhau nhưng kích thước phải nhỏ hơn 64KB. Cấu trúc đầy đủ của một Segment lúc này là Header chứa thông tin điều khiển và sau đó là dữ liệu

Trong tầng này còn bao gồm 2 giao thức cốt lõi là TCP và UDP. Trong đó, TCP đảm bảo chất lượng gói tin nhưng tiêu tốn thời gian khá lâu để kiểm tra đầy đủ thông tin từ thứ tự dữ liệu cho đến việc kiểm soát vấn đề tắc nghẽn lưu lượng dữ liệu. Trái với điều đó, UDP cho thấy tốc độ truyền tải nhanh hơn nhưng lại không đảm bảo được chất lượng dữ liệu được gửi đi.

**Tầng 2 - Tầng mạng (Internet) **

Gần giống như tầng mạng của mô hình OSI. Tại đây, nó cũng được định nghĩa là một giao thức chịu trách nhiệm truyền tải dữ liệu một cách logic trong mạng. Các phân đoạn dữ liệu sẽ được đóng gói (Packets) với kích thước mỗi gói phù hợp với mạng chuyển mạch mà nó dùng để truyền dữ liệu. Lúc này, các gói tin được chèn thêm phần Header chứa thông tin của tầng mạng và tiếp tục được chuyển đến tầng tiếp theo. Các giao thức chính trong tầng là IP, ICMP và ARP.

**Tầng 1 - Tầng Vật lý (Physical) **

Là sự kết hợp giữa tầng Vật lý và tầng liên kết dữ liệu của mô hình OSI. Chịu trách nhiệm truyền dữ liệu giữa hai thiết bị trong cùng một mạng. Tại đây, các gói dữ liệu được đóng vào khung (gọi là Frame) và được định tuyến đi đến đích đã được chỉ định ban đầu.


**Ưu điểm của TCP/IP là:**

- Mô hình TCP/IP không chịu sự kiểm soát của tổ chức nào. Do đó, người dùng có thể tự do sử dụng.
- TCP/IP có khả năng tương thích với các mạng, hệ điều hành và phần cứng máy tính.
- TCP/IP có khả năng khả năng định tuyến, mở rộng và nhận định được đường dẫn tốt nhất thông qua mạng.

**Nhược điểm**
- Khó khăn trong việc thay thế các giao thức mới.
- Một tầng có nhiều chức năng nên phức tạp hơn so với mô hình OSI.
- Không có sự phân biệt dõ dàng giữa dịch vụ, giao diện và giao thức.


# So sánh giữa 2 mô hình
– Giống nhau: Mô hình OSI và TCP/IP có một số điểm chung như sau:
  - OSI và TCP/IP đều có kiến trúc phân lớp.
  - OSI và TCP/IP đều có lớp Network và lớp Transport.
  - OSI và TCP/IP cùng sử dụng kỹ thuật chuyển Packet.

- Khác nhau: 

|  | Mô hình OSI | Mô hình TCP/IP| 
|--------------|-------|------|
| Độ tin cậy phổ biến | Nhiều người cho rằng đây là mô hình cũ, chỉ để tham khảo, số người sử dụng hạn chế hơn so với TCP/IP | Được chuẩn hóa, nhiều người tin cậy và sử dụng phổ biến trên toàn cầu |
| Phương pháp tiếp cận | Tiếp cận theo chiều dọc | Tiếp cận theo chiều ngang | 
|Sự kết hợp giữa các tầng|Mỗi tầng khác nhau sẽ thực hiện một nhiệm vụ khác nhau, không có sự kết hợp giữa bất cứ tầng nào|Trong tầng ứng dụng có tầng trình diễn và tầng phiên được kết hợp với nhau|
|Thiết kế |Phát triển mô hình trước sau đó sẽ phát triển giao thức|	Các giao thức được thiết kế trước sau đó phát triển mô hình|
|Số lớp (tầng)|7|4|
|Truyền thông|Hỗ trợ cả kết nối định tuyến và không dây|Hỗ trợ truyền thông không kết nối từ tầng mạng|
|Tính phục thuộc|Giao thức độc lập|Phụ thuộc vào giao thức|


