 # **Mô hình OSI (Open System Interconnection)**
Mô hình OSI (Open System Interconnection): là mô hình được tổ chức ISO đề xuất từ 1977 và công bố lần đầu vào 1984. Để các máy tính và các thiết bị mạng có thể truyền thông với nhau phải có những qui tắc giao tiếp được các bên chấp nhận. Mô hình OSI là một khuôn mẫu giúp chúng ta hiểu dữ liệu đi xuyên qua mạng như thế nào đồng thời cũng giúp chúng ta hiểu được các chức năng mạng diễn ra tại mỗi lớp.

Mô hình tham chiếu OSI được chia thành bảy lớp với các chức năng sau: Application Layer (lớp ứng dụng): giao diện giữa ứng dụng và mạng.

Presentation Layer (lớp trình bày): thoả thuận khuôn dạng trao đổi dữ liệu. Session Layer (lớp phiên): cho phép người dùng thiết lập các kết nối.

Transport Layer (lớp vận chuyển): đảm bảo truyền thông giữa hai hệ thống. Network Layer (lớp mạng): định hướng dữ liệu truyền trong môi trường liên mạng. Data link Layer (lớp liên kết dữ liệu): xác định việc truy xuất đến các thiết bị.

Physical Layer (lớp vật lý): chuyển đổi dữ liệu thành các bit và truyền đi.

![image](https://user-images.githubusercontent.com/65167293/157796467-e9ff007a-0c7a-49af-ad8d-838e8ee5c724.png)


*Hình 1. 1 Mô hình tham chiếu OSI*

##
## **Chức năng chung của các lớp trong mô hình**
- Lớp ứng dụng (Application Layer): là giao diện giữa các chương trình ứng dụng của người dùng và mạng. Lớp Application xử lý truy nhập mạng chung, kiểm soát luồng và phục hồi lỗi. Lớp này không cung cấp các dịch vụ cho lớp nào mà nó cung cấp dịch vụ cho các ứng dụng như: truyền file, gởi nhận E-mail, Telnet, HTTP, FTP, SMTP…

- Lớp trình bày (Presentation Layer): lớp này chịu trách nhiệm thương lượng và xác lập dạng thức dữ liệu được trao đổi. Nó đảm bảo thông tin mà lớp ứng dụng của một hệ thống đầu cuối gởi đi, lớp ứng dụng của hệ thống khác có thể đọc được. Lớp trình bày thông dịch giữa nhiều dạng dữ liệu khác nhau thông qua một dạng chung, đồng thời nó cũng nén và giải nén dữ liệu. Thứ tự byte, bit bên gởi và bên nhận qui ước qui tắc gởi nhận một chuỗi byte, bit từ trái qua phải hay từ phải qua trái. Nếu hai bên không thống nhất thì sẽ có sự chuyển đổi thứ tự các byte bit vào trước hoặc sau khi truyền. Lớp presentation cũng quản lý các cấp độ nén dữ liệu nhằm giảm số bit cần truyền. Ví dụ: JPEG, ASCCI, EBCDIC....

- Lớp phiên (Session Layer): lớp này có chức năng thiết lập, quản lý, và kết thúc các phiên thông tin giữa hai thiết bị truyền nhận. Lớp phiên cung cấp các dịch vụ cho lớp trình bày. Lớp Session cung cấp sự đồng bộ hóa giữa các tác vụ người dùng bằng cách đặt những điểm kiểm tra vào luồng dữ liệu. Bằng cách này, nếu mạng không hoạt động thì chỉ có dữ liệu truyền sau điểm kiểm tra cuối cùng mới phải truyền lại. Lớp này cũng thi hành kiểm soát hội thoại giữa các quá trình giao tiếp, điều chỉnh bên nào truyền, khi nào, trong bao lâu. Ví dụ như: RPC, NFS,. Lớp này kết nối theo ba cách: Haft-duplex, Simplex, Full- duplex.

- Lớp vận chuyển (Transport Layer): lớp vận chuyển phân đoạn dữ liệu từ hệ thống máy truyền và tái thiết lập dữ liệu vào một luồng dữ liệu tại hệ thống máy nhận đảm bảo rằng việc bàn giao các thông điệp giữa các thiết bị đáng tin cậy. Dữ liệu tại lớp này gọi là segment. Lớp này thiết lập, duy trì và kết thúc các mạch ảo đảm bảo cung cấp các dịch vụ sau:

- Xếp thứ tự các phân đoạn: khi một thông điệp lớn được tách thành nhiều phân đoạn nhỏ để bàn giao, lớp vận chuyển sẽ sắp xếp thứ tự các phân đoạn trước khi ráp nối các phân đoạn thành thông điệp ban đầu.

- Kiểm soát lỗi: khi có phân đoạn bị thất bại, sai hoặc trùng lắp, lớp vận chuyển sẽ yêu cầu truyền lại.

- Kiểm soát luồng: lớp vận chuyển dùng các tín hiệu báo nhận để xác nhận. Bên gửi sẽ không truyền đi phân đoạn dữ liệu kế tiếp nếu bên nhận chưa gởi tín hiệu xác nhận rằng đã nhận được phân đoạn dữ liệu trước đó đầy đủ.

- Lớp mạng (Network Layer): lớp mạng chịu trách nhiệm lập địa chỉ các thông điệp, diễn dịch địa chỉ và tên logic thành địa chỉ vật lý đồng thời nó cũng chịu trách nhiệm gởi packet từ mạng nguồn đến mạng đích. Lớp này quyết định đường đi từ máy tính nguồn đến máy tính đích. Nó quyết định dữ liệu sẽ truyền trên đường nào dựa vào tình trạng, ưu tiên dịch vụ và các yếu tố khác. Nó cũng quản lý lưu lượng trên mạng chẳng hạn như chuyển đổi gói, định tuyến, và kiểm soát sự tắc nghẽn dữ liệu. Nếu bộ thích ứng mạng trên bộ định tuyến (router) không thể truyền đủ đoạn dữ liệu mà máy tính nguồn gởi đi, lớp Network trên bộ định tuyến sẽ chia dữ liệu thành những đơn vị nhỏ hơn, nói cách khác, nếu máy tính nguồn gửi đi các gói tin có kích thước là 20Kb, trong khi Router chỉ cho phép các gói tin có kích thước là 10Kb đi qua, thì lúc đó lớp Network của Router sẽ chia gói tin ra làm 2, mỗi gói tin có kích thước là 10Kb. Ở đầu nhận, lớp Network ráp nối lại dữ liệu. Ví dụ: một số giao thức lớp này: IP, IPX,...Dữ liệu ở lớp này gọi packet hoặc datagram.

- Lớp liên kết dữ liệu (Data link Layer): cung cấp khả năng chuyển dữ liệu tin cậy xuyên qua một liên kết vật lý. Lớp này liên quan đến:
  - Địa chỉ vật lý.
  - Mô hình mạng.
  - Cơ chế truy cập đường truyền.
  - Thông báo lỗi.
  - Thứ tự phân phối frame.
  - Điều khiển dòng.

Tại lớp data link, các bít đến từ lớp vật lý được chuyển thành các frame dữ liệu bằng cách dùng một số nghi thức tại lớp này. Lớp data link được chia thành hai lớp con:

- Lớp con LLC (logical link control).
- Lớp con MAC (media access control).

Lớp con LLC là phần trên so với các giao thức truy cập đường truyền khác, nó cung cấp sự mềm dẻo về giao tiếp. Bởi vì lớp con LLC hoạt động độc lập với các giao thức truy cập đường truyền, cho nên các giao thức lớp trên hơn (ví dụ như IP ở lớp mạng) có thể hoạt động mà không phụ thuộc vào loại phương tiện LAN. Lớp con LLC có thể lệ thuộc vào các lớp thấp hơn trong việc cung cấp truy cập đường truyền.

Lớp con MAC cung cấp tính thứ tự truy cập vào môi trường LAN. Khi nhiều trạm cùng truy cập chia sẻ môi trường truyền, để định danh mỗi trạm, lớp cho MAC định nghĩa một trường địa chỉ phần cứng, gọi là địa chỉ MAC address. Địa chỉ MAC là một con số đơn nhất đối với mỗi giao tiếp LAN (card mạng).

- Lớp vật lý (Physical Layer): định nghĩa các qui cách về điện, cơ, thủ tục và các đặc tả chức năng để kích hoạt, duy trì và dừng một liên kết vật lý giữa các hệ thống đầu cuối. Một số các đặc điểm trong lớpvật lý này bao gồm:
- Mức điện thế.
  - Khoảng thời gian thay đổi điện thế.
- Tốc độ dữ liệu vật lý.
  - Khoảng đường truyền tối đa.
- Các u nối vật lý

   ***Quá trình xử lí và vận chuyển của một gói dữ liệu***

![image](https://user-images.githubusercontent.com/65167293/157796516-0c52e988-ce90-4e6b-a934-ff677e6be696.png)

*Hình 1. 2    Quá trình xử lí và vận chuyển của 1 gói dữ liệu*

 ***Quá trình đóng gói dữ liệu***
 
![image](https://user-images.githubusercontent.com/65167293/157796566-9ce5aeb8-a062-477b-a8e0-feca29254c04.png)

*Hình 1. 3   Tên gọi dữ liệu ở các tầng trong mô hình OSI*

Đóng gói dữ liệu là quá trình đặt dữ liệu nhận được vào sau header (và trước trailer) trên mỗi lớp. Lớp Physical không đóng gói dữ liệu vì nó không dùng header và trailer. Việc đóng gói dữ liệu không nhất thiết phải xảy ra trong mỗi lần truyền dữ liệu của trình ứng dụng. Các lớp 5, 6, 7 sử dụng header trong quá trình khởi động, nhưng trong phần lớn các lần truyền thì không có header của lớp 5, 6, 7 lý do là không có thông tin mới để trao đổi.

***Quá trình truyền dữ liệu từ máy gửi đến máy nhận***

Bước 1: Trình ứng dụng (trên máy gửi) tạo ra dữ liệu và các chương trình phần cứng, phần mềm cài đặt mỗi lớp sẽ bổ sung vào header và trailer (quá trình đóng gói dữ liệu tại máy gửi).

Bước 2: Lớp Physical (trên máy gửi) phát sinh tín hiệu lên môi trường truyền tải để truyền dữ liệu.

Bước 3: Lớp Physical (trên máy nhận) nhận dữ liệu.

Bước 4: Các chương trình phần cứng, phần mềm (trên máy nhận) gỡ bỏ header và trailer và xử lý phần dữ liệu (quá trình xử lý dữ liệu tại máy nhận).

Giữa bước 1 và bước 2 là quá trình tìm đường đi của gói tin. Thông thường, máy gửi đã biết địa chỉ IP của máy nhận. Vì thế, sau khi xác định được địa chỉ IP của máy nhận thì lớp Network của máy gửi sẽ so sánh địa chỉ IP của máy nhận và địa chỉ IP của chính nó:

- Nếu cùng địa chỉ mạng thì máy gửi sẽ tìm trong bảng MAC Table của mình để có được địa chỉ MAC của máy nhận. Trong trường hợp không có được địa chỉ MAC tương ứng, nó sẽ thực hiện giao thức ARP để truy tìm địa chỉ MAC. Sau khi tìm được địa chỉ MAC, nó sẽ lưu địa chỉ MAC này vào trong bảng MAC Table để lớp Datalink sử dụng ở các lần gửi sau. Sau khi có địa chỉ MAC thì máy gửi sẽ gởi gói tin đi (giao thức ARP sẽ được nói thêm trong các chương tiếp theo).
- Nếu khác địa chỉ mạng thì máy gửi sẽ kiểm tra xem máy có được khai báo Default Gateway hay không.

\+ Nếu có khai báo Default Gateway thì máy gửi sẽ gởi gói tin thông qua Default Gateway.

\+ Nếu không có khai báo Default Gateway thì máy gởi sẽ loại bỏ gói tin và thông báo "Destination host Unreachable"

***Chi tiết quá trình xử lí tại máy nhận***

Bước 1: Lớp Physical kiểm tra quá trình đồng bộ bit và đặt chuỗi bit nhận được vào vùng đệm. Sau đó thông báo cho lớp Data Link dữ liệu đã được nhận.

Bước 2: Lớp Data Link kiểm lỗi frame bằng cách kiểm tra FCS trong trailer. Nếu có lỗi thì frame bị bỏ. Sau đó kiểm tra địa chỉ lớp Data Link (địa chỉ MAC) xem có trùng với địa chỉ máy nhận hay không. Nếu đúng thì phần dữ liệu sau khi loại header và trailer sẽ được chuyển lên cho lớp Network.

Bước 3: Địa chỉ lớp Network được kiểm tra xem có phải là địa chỉ máy nhận hay không (địa chỉ IP). Nếu đúng thì dữ liệu được chuyển lên cho lớp Transport xử lý.

Bước 4: Nếu giao thức lớp Transport có hỗ trợ việc phục hồi lỗi thì số định danh phân đoạn được xử lý. Các thông tin ACK, NAK (gói tin ACK, NAK dùng để phản hồi về việc các gói tin đã được gởi đến máy nhận chưa) cũng được xử lý ở lớp này. Sau quá trình phục hồi lỗi và sắp thứ tự các phân đoạn, dữ liệu được đưa lên lớp Session.

Bước 5: Lớp Session đảm bảo một chuỗi các thông điệp đã trọn vẹn. Sau khi các luồng đã hoàn tất, lớp Session chuyển dữ liệu sau header lớp 5 lên cho lớp Presentation xử lý.

Bước 6: Dữ liệu sẽ được lớp Presentation xử lý bằng cách chuyển đổi dạng thức dữ liệu. Sau đó kết quả chuyển lên cho lớp Application.

Bước 7: Lớp Application xử lý header cuối cùng. Header này chứa các tham số thoả thuận giữa hai trình ứng dụng. Do vậy tham số này thường chỉ được trao đổi lúc khởi động quá trình truyền thông giữa hai trình ứng dụng.
# **Mô hình TCP/IP**

***Vai trò của mô hình tham chiếu TCP/IP***

Các bộ phận, văn phòng của Chính phủ Hoa Kỳ đã nhận thức được sự quan trọng và tiềm năng của kĩ thuật Internet từ nhiều năm trước, cũng như đã cung cấp tài chánh cho việc nghiên cứu, để thực sự có được một mạng Internet toàn cầu. Sự hình thành kĩ thuật Internet là kết quả nghiên cứu dưới sự tài trợ của Defense/Advanced Research Projects Agency (ARPA/DARPA). Kĩ thuật ARPA bao gồm một tập hợp của các chuẩn mạng, đặc tả chi tiết cách thức mà các máy tính thông tin liên lạc với nhau, cũng như các quy ước cho các mạng interconnecting và định tuyến giao thông. Tên chính thức là TCP/IP Internet Protocol Suite và thường được gọi là TCP/IP, có thể dùng để thông tin liên lạc qua tập hợp bất kỳ các mạng interconnected. Nó có thể dùng để liên kết mạng trong một công ty, không nhất thiết phải nối kết với các mạng khác bên ngoài.

***Các lớp của mô hình tham chiếu TCP/IP***

![image](https://user-images.githubusercontent.com/65167293/157796766-6dd4dc44-9643-49bb-a76b-796bb7691b2d.png)

*Hình 1. 4   Mô hình tham chiếu TCP/IP*

Mô hình tham chiếu TCP/IP tương tự như kiến trúc OSI, sau đây là một số tính chất của các lớp trong mô hình tham chiếu TCP/IP:

- Lớp Application: quản lý các giao thức, như hỗ trợ việc trình bày, mã hóa, và quản lý cuộc gọi. Lớp Application cũng hỗ trợ nhiều ứng dụng, như: FTP (File Transfer Protocol), HTTP (Hypertext Transfer Protocol), SMTP (Simple Mail Transfer Protocol), DNS (Domain Name System), TFTP (Trivial File Transfer Protocol).
- Lớp Transport: đảm nhiệm việc vận chuyển từ nguồn đến đích. Tầng Transport đảm nhiệm việc truyền dữ liệu thông qua hai nghi thức: TCP (Transmission Control Protocol) và UDP (User Datagram Protocol).
- Lớp Internet: đảm nhiệm việc chọn lựa đường đi tốt nhất cho các gói tin. Nghi thức được sử dụng chính ở tầng này là nghi thức IP (Internet Protocol).
- Lớp Network Interface: có tính chất tương tự như hai lớp Data Link và Physical của kiến trúc OSI.


***Các bước đống gói dữ liệu trong mô hình TCP/IP***

![image](https://user-images.githubusercontent.com/65167293/157796802-301a9a8c-e80f-46a3-b0a8-2073f45e39e4.png)

*Hình 1. 5  Các bước đóng gói dữ liệu trong mô hình TCP/IP*

# **So sánh mô hình OSI và TCP/IP**

**Các điểm giống nhau:**

- Cả hai đều có kiến trúc phân lớp.

\+ Đều có lớp Application, mặc dù các dịch vụ ở mỗi lớp khác nhau.

\+ Đều có các lớp Transport và Network.

- Sử dụng kĩ thuật chuyển packet (packet-switched).
- Các nhà quản trị mạng chuyên nghiệp cần phải biết rõ hai mô hình trên. 

 **Các điểm khác nhau:**
 
- Mô hình TCP/IP kết hợp lớp Presentation và lớp Session vào trong lớp Application
- Mô hình TCP/IP kết hợp lớp Data Link và lớp Physical vào trong một lớp.
- Mô hình TCP/IP đơn giản hơn bởi vì có ít lớp hơn.
- Giao thức TCP/IP được chuẩn hóa và sử dụng phổ biến trên toàn thế giới

