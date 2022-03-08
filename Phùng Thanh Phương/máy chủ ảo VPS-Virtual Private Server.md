**1.Máy chủ ảo VPS**\
VPS là viết tắt của Virtual Private Server (máy chủ riêng ảo) là dạng máy chủ được tạo ra bằng phương pháp phân chia một máy chủ vật lý thành nhiều máy chủ khác nhau có tính năng tương tự như máy chủ riêng (dedicated server), chạy dưới dạng chia sẻ tài nguyên từ máy chủ vật lý ban đầu. Khác với Hosting sử dụng phần mềm quản lý (Hosting control panel) để khởi tạo và quản lý các gói Hosting, VPS được tạo ra nhờ công nghệ ảo hóa. Số lượng VPS luôn thấp hơn nhiều lần so với số lượng Hosting nếu cài đặt trên cùng một hệ thống Server, do đó tính ổn định và hiệu suất sử dụng tài nguyên của VPS luôn vượt trội so với Hosting. Một VPS có thể chứa hàng trăm Hosting khác nhau.

Mỗi VPS ảo đều là một hệ thống riêng, có CPU – RAM – HDD – địa chỉ IP – hệ điều hành riêng. Bất kỳ lúc nào cần thiết, người mua/thuê VPS đều có thể root hoặc restart lại hệ thống mà không ảnh hưởng đến người thuê khác.

VPS phù hợp để xây dựng các hệ thống Mail Server, Web Server, Backup/Storage Server… dùng riêng hoặc truyền tải file dữ liệu giữa các chi nhánh với nhau một cách nhanh chóng, thuận tiện và bảo mật; dễ dàng nâng cấp tài nguyên và tái tạo lại hệ điều hành khi gặp sự cố hệ thống với thời gian thực hiện rất nhanh mà không cần cài đặt lại từ đầu.

VPS như một giải pháp dung hòa giữa Hosting và máy chủ riêng (Dedicated Server) theo cả khía cạnh chi phí và cách thức vận hành. Vì vậy đây là giải pháp phù hợp cho các cá nhân hoặc doanh nghiệp muốn có một hệ thống máy chủ riêng biệt, toàn quyền quản lý với chi phí thấp.

**2. Các ưu điểm của Máy chủ ảo**
* Toàn quyền quản lý với tính năng như một máy chủ độc lập.
* Độ ổn định và bảo mật cao.
* Dễ dàng nâng cấp tài nguyên mà không làm gián đoạn dịch vụ.
* Quản trị từ xa, cài đặt các phần mềm và ứng dụng theo nhu cầu.
* Cài đặt lại hệ điều hành nhanh, chỉ từ 5-10 phút.
* Tiết kiệm được chi phí đầu tư máy chủ.

**3. Các thông số cần lưu ý**\
* RAM

Càng nhiều RAM càng tốt vì đa số các loại RAM đều giống nhau về mặt hiệu năng. Tuy nhiên, chỉ đúng với RAM vật lý, do vậy, bạn nên cân nhắc sử dụng của VPS là RAM thật (vật lý) hay là RAM ảo. Trong máy tính thì RAM là loại bộ nhớ chính, nếu máy chủ VPS của bạn càng nhiều RAM thì khả năng truy xuất dữ liệu càng tốt, bởi vì khi dùng VPS bạn sẽ cần RAM để xử lý các vấn đề như xử lý các đoạn mã PHP với phần mềm PHP, xử lý truy vấn nhập xuất của database với MySQL, các ứng dụng nhỏ đi kèm, hỗ trợ đọc ghi dữ liệu,…nên thông số này rất quan trọng.

Ngoài ra, bạn cũng nên tuỳ thuộc vào lượng truy cập website mà chọn RAM nhiều hay ít. Đối với nhu cầu sử dụng wordPress, lượng truy cập 5000/ngày và 100 user online cùng lúc, bạn cần tối thiểu 1GB RAM.

* SWAP

SWAP là bộ nhớ ảo để lưu lại các hành động xử lý cũ nếu như bộ nhớ RAM bị đầy. Bản thân SWAP là một không gian lưu trữ trên ổ cứng chứ không phải là một bộ nhớ độc lập.

Không phải VPS nào cũng hỗ trợ bộ nhớ SWAP mà chỉ có các XEN VPS mới hỗ trợ SWAP.

* Ổ cứng (Disk)

Là không lưu trữ sẽ được sử dụng để lưu các file cài đặt của hệ điều hành và các file của mã nguồn website bạn lưu trên đó.

Ổ đĩa hiện nay được chia làm 2 loại: HDD và SSD:

   * HDD (Hard Disk Drive): Là loại ổ đĩa thông dụng nhất vẫn được sử dụng trên máy tính.
   * SSD (Solid State Drive): SSD hoặc ổ cứng bán dẫn, là loại ổ cứng dùng để lưu trữ dữ liệu nhưng tốc độ truy xuất dữ liệu nhanh hơn so với HDD 300 lần. Ví dụ, test thử ổ HDD có tốc độ truy xuất chỉ khoảng 80mb/s nhưng SSD thì có tốc độ lên tới hơn 400mb/s.

Ổ cứng loại SSD thường giá sẽ đắt hơn loại ổ HDD.

* CPU Core

Đối với CPU bạn cần quan tâm đến 2 chỉ tiêu quan trọng đó chính là: số Core, tốc độ xung nhịp. Thường thì số core càng cao thì khả năng xử lý dữ liệu càng tốt. Ở các gói VPS, trung bình bạn sẽ được chọn từ 1 core đến 3 core.

* Băng thông
Băng thông cũng như 1 con đường, nếu băng thông lớn, tương tự như một con đường rộng, nhiều người có thể đi qua, tình trạng tắc nghẽn khó xảy ra và ngược lại. Các nhà cung cấp băng thông thường cung cấp lượng băng thông tối thiểu 10 – 20 Mbps.

* Thời gian Up-time
Thời gian up-time của VPS thường được ước lượng từ thời gian hoạt động của nó. Thời gian hoạt động của VPS từ 99,95 đến 99,9% thì bạn đều có thể chấp nhận mua được.

* IP
IP là viết tắt của Internet Protocol là số lượng địa chỉ IP mà nhà cung cấp dịch vụ VPS sẽ cấp cho bạn. Các dãy địa chỉ IP sẽ được nhà cung cấp chọn ngẫu nhiên.

Thông thường, nếu bạn chọn mua thêm nhiều IP khác nhau thì các dãy IP đó sẽ có chung một class A và B. Ví dụ: 192.168.1.1/192.168.1.2/192.168.1.3.

* Hệ điều hành của máy chủ ảo

Có 2 hệ điều hành phổ biến cho các máy chủ ảo là: Linux và Window. Linux thì thân thiện với người dùng tốt hơn và chi phí ít hơn, hỗ trợ ứng dụng nhiều hơn so với Window. Tuy nhiên, nếu bạn làm việc với Dot Net hoặc Visual Studio, bạn nên chọn máy chủ ảo của Window.
