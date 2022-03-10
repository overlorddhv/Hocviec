# 1. DNS là gì?

DNS viết tắt của Domain Name System có nghĩa là hệ thống phân giải tên miền. DNS là hệ thống cho phép thiết lập tương ứng giữa địa chỉ IP và tên miền trên Internet. DNS được phát minh vào năm 1984 cho Internet và đây là một trong số các chuẩn công nghiệp của các cổng bao gồm cả TCP/IP. Hệ thống phân giải tên miền chính là chìa khóa chủ chốt của nhiều dịch vụ mạng hiện nay như Internet, Mail server, Web server… Mỗi máy tính khi kết nối vào Internet sẽ được gán cho 1 địa chỉ IP riêng biệt và không trùng lẫn với bất kỳ máy tính nào khác trên thế giới. Cũng giống như vậy đối với website cũng có địa chỉ IP riêng biệt của website đó. Nói cách khác, DNS cũng giống như một danh bạ điện thoại dành riêng cho Internet. Nếu bạn biết tên của một người nhưng không biết số điện thoại hay ngược lại, bạn có thể tham khảo trong sổ danh bạ dễ dàng.

# 2. Cách thức hoạt động của DNS

DNS hoạt động theo từng bước theo cấu trúc của DNS. Bước đầu tiên gọi là DNS query, một truy vấn để lấy thông tin. Sử dụng tình huống tìm kiếm website bằng cách gõ tên miền vào trong web browser (ví dụ, www.google.com). Đầu tiên, DNS server sẽ tìm thông tin phân giải trong filehosts – một file text trong hệ điều hành chịu trách nhiệm chuyển hostname thành địa chỉ IP. Nếu không thấy thông tin, nó sẽ tìm trọng cache – bộ nhớ tạm của phần cứng hay phần mềm. Nơi phổ biến nhất lưu thông tin cache này là  bộ nhớ tạm của trình duyệt và bộ nhớ tạm của Internet Service Providers (ISP). Nếu không nhận được thông tin, bạn sẽ thấy mã lỗi hiện lên. Tổng cộng có khoảng 4 loại server tham gia vào trong hệ thống phân giải tên miền:
  # DNS Recursor
DNS recursor là server đóng vai trò liên lạc với các server khác để thay nó làm nhiệm vụ phản hồi cho client (trình duyệt người dùng). Nó như một nhân viên cần mẫn nhận nhiệm vụ lấy và trả thông tin cho client (trình duyệt) để tìm đúng thông tin chúng cần. Để lấy được thông tin, DNS recursor có thể sẽ cần gọi đến Root DNS Server để trợ giúp.
  # Root Nameserver
Root DNS Server, cũng thường được gọi là nameserver, là server quan trọng nhất trong hệ thống cấp bậc của DNS. Nó không có tên cụ thể. Bạn có thể hiểu nó là một thư viện để định hướng tìm kiếm giúp bạn. Trên thực tế, DNS recursive resolver sẽ chuyển yêu cầu tới Root Nameserver. Sau đó, server này sẽ phản hồi rằng nó cần tìm trong các top-level domain name servers (TLD nameserver) cụ thể nào.
  # TLD Nameserver
Khi bạn muốn truy cập Google hay Facebook, thường phần mở rộng của bạn sẽ dùng là .com. Nó là một trong các top-level domain. Server cho loại top-level domain này gọi là TLD nameserver. Nó chịu trách nhiệm quản lý toàn bộ thông tin của một phần mở rộng tên miền chung. Ví dụ như khi bạn gõ www.google.com trên trình duyệt, TLD .com sẽ phản hồi từ một DNS resolver để giới thiệu cho nó một Authoritative DNS server. Authoritative Name Server là nơi chính thức chứa nguồn dữ liệu của tên miền đó.
  # Authoritative Nameserver
Khi một DNS resolver tìm thấy một authoritative nameserver, đây là việc phân giải tên miền diễn ra. Authoritative nameserver có chứa thông tin tên miền gắn với địa chỉ nào. Nó sẽ đưa cho recursive resolver địa chỉ IP cần thiết tìm thấy trong danh mục các bản ghi của nó.

# 3. Các loại DNS bản ghi DNS thường sử dụng
 
 - CNAME Record: Là một bản ghi tên quy chuẩn (Canonical Name Record). Đây là một dạng bản ghi tài nguyên trong hệ thống tên miền.
 - A Record: Dùng để trỏ tên miền website tới một địa chỉ IP cụ thể. Đây được xem là bản ghi DNS đơn giản nhất.
 - MX Record: Bản ghi này bạn có thể sử dụng để trỏ tên miền đến mail server. MX Record chỉ định server nào quản lý các dịch vụ Email của tên miền đó.
 - AAAA Record: Dùng để trỏ tên miền đến địa chỉ IPv6 và cho phép thêm host mới, TTL và IPv6.
 - TXT Record: Ngoài ra, có thể thêm giá trị TXT, Host mới, TTL và Point To để chứa các thông tin định dạng văn bản domain.
 - SRV Record: Đây là bản ghi DNS đặc biệt, dùng để xác định chính xác dịch vụ nào đang chạy Port nào. Và thông qua bản ghi này bạn có thể thêm Priority, Port, Weight, TTL, Point to.
 - NS Record: Bản ghi này có thể chỉ định Name Server cho từng tên miền phụ và bên cạnh đó có thể tạo tên Name Server, TTL hay host mới.

# 4. Các loại DNS Server
  
  - Root Name Server
Root Name Server là một dịch vụ phân giải tên miền gốc và trên thế giới có khoảng 12 DNS root Server. DNS root Server quản lý tất cả các tên miền Top-level. Khi có yêu cầu phân giải một Domain Name thành một địa chỉ IP, client sẽ gửi yêu cầu đến DNS gần nhất (DNS ISP). DNS ISP sẽ kết nối tới DNS root Server để hỏi địa chỉ của Domain Name. DNS root Server sẽ căn cứ và dựa vào các Top Level của tên miền và từ đó có những tài liệu hướng dẫn phù hợp để chuyển hướng cho khách hàng đến đúng địa chỉ cần truy vấn.
 - Local Name Server
DNS Server này dùng để chứa thông tin để truy xuất và tìm kiếm máy chủ tên miền. Và thường được duy trì và phát triển bởi các doanh nghiệp hay các nhà cung cấp dịch vụ Internet.

# 5. Các loại truy vấn DNS

Trong một truy vấn DNS thông thường, ba loại truy vấn xảy ra. Bằng cách sử dụng kết hợp các truy vấn này. Một quy trình được tối ưu hóa cho quá trình phân giải DNS có thể giúp giảm khoảng cách di chuyển. Trong một tình huống lý tưởng, dữ liệu bản ghi được lưu trong bộ nhớ cache sẽ khả dụng, cho phép máy chủ định danh DNS trả về truy vấn không đệ quy.

3 loại truy vấn DNS:

  - Recursive query: DNS client yêu cầu máy chủ DNS (thường là recursive DNS resolver). Sẽ trả lời máy khách bằng bản ghi tài nguyên được yêu cầu. Hoặc thông báo lỗi nếu resolver không thể tìm thấy bản ghi.
  - Iterative query: Trong tình huống này, DNS client sẽ cho phép máy chủ DNS trả về câu trả lời tốt nhất có thể. Nếu máy chủ DNS được truy vấn không có kết quả trùng khớp với tên truy vấn. Nó sẽ trả về một giới thiệu đến máy chủ DNS có thẩm quyền cho mức thấp hơn. DNS client sau đó sẽ thực hiện một truy vấn đến địa chỉ được giới thiệu. Quá trình này tiếp tục với các máy chủ DNS bổ sung trong chuỗi truy vấn cho đến khi xảy ra lỗi hoặc hết thời gian.
  - Non-recursive query: Thông thường điều này sẽ xảy ra khi DNS resolver client truy vấn máy chủ DNS một record mà server có quyền truy cập hoặc bản ghi tồn tại bên trong bộ đệm của server. Thông thường, một máy chủ DNS sẽ lưu các bản ghi DNS để ngăn chặn việc tiêu thụ thêm băng thông và giảm tải cho các máy chủ DNS khác.

# 6. Nguyên nhân DNS dễ bị tấn công?

Vì hệ thống tên miền khá phức tạp và người tấn công có thể tận dụng điểm yếu trong DNS để tấn công với nhiều phương thức khác nhau. Đa số các cuộc tấn công đều tập trung vào việc lạm dụng DNS để ngăn người dùng không thể truy cập vào Internet. Bên cạnh đó, DNS cũng có thể bị tấn công bằng phướng pháp tận dụng giao thức DNS để chuyển hướng người dùng truy cập vào các trang web độc hại nhằm đánh cắp dữ liệu nhạy cảm của cá nhân, doanh nghiệp. Ngoài ra, việc sử dụng server đệ quy sẽ lưu phản hồi vào bộ nhớ tạm để tăng tốc độ của các truy vấn tiếp theo. Nhằm giảm số lượng request thông tin, nhưng khá nguy hiểm và dễ bị tấn công bởi Man-In-The-Middle. Những kẻ tấn công có thể truy cập vào Over IP (VoIP) để đánh cắp thông tin, mạo danh, trích xuất dữ liệu, thông tin,….
