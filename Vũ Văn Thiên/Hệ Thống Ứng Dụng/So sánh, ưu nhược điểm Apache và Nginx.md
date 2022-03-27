# Tìm hiểu về Apache (Apache HTTP Server)

## Apache là gì?

Apache có tên đầy đủ là Apache HTTP Server. Đây là một web server mã nguồn mở miễn phí và được sử dụng phổ biến hiện nay. Nếu sử dụng Apache, bạn chỉ cần thao tác đơn giản là nhập URL hoặc IP và nhấn Enter thì Server sẽ tiếp nhận URL hay địa chỉ IP mà bạn đã nhập.

![image](https://user-images.githubusercontent.com/62273292/160291044-07b42020-d526-4a43-a0c1-4ec92d9bbe8e.png)

Apache chạy được trên các hệ điều hành tương tự như Unix, Windows, Novell Netware và các hệ điều hành khác. Chính vì vậy, hiện nay nó được sử dụng khá rộng rãi.

**Ưu và nhược điểm của Apache**

Ưu điểm 

– Apache là phần mềm miễn phí mã nguồn mở, có độ ổn định và đáng tin cậy.

– Cấu hình đơn giản và thân thiện dù bạn là những người mới bắt đầu làm quen với ứng dụng này

– Phần mềm được cập nhật thường xuyên, phát hiện và báo lỗi liên tục nhằm giúp người dùng ngăn chặn kịp thời, không để thông tin bị đánh cắp.

– Các thể thức cấu trúc Module linh hoạt, Apache hoạt động hiệu quả và nhanh nhạy hơn với WordPress sites.

– Cộng đồng sử dụng Apache lớn nên có thể tương trợ và giải đáp thắc mắc của bạn bất kỳ lúc nào

Nhược điểm

– Thỉnh thoảng chậm hay gặp trục trặc trong quá trình truy vấn bởi có rất nhiều người truy cập Apache cùng một lúc.

– Khả năng bảo mật đôi khi còn chưa hiệu quả do tính miễn phí nên người dùng có thể chọn nhiều cách thiết lập khác nhau.



# Tìm hiểu về NGINX

## Web Server NGINX là gì?

NGINX là web server mã nguồn mở. NGINX ban đầu được dùng để phục vụ web HTTP. Nhưng hiện nay được dùng để làm Reverse Proxy, Email Proxy (IMAP, POP3, SMTP) và một trình cân bằng tải (load balancer) và proxy ngược (reverse proxy) cho các máy chủ HTTP, TCP và UDP.

![image](https://user-images.githubusercontent.com/62273292/160291147-578ee4b2-074b-4318-aaea-3f5d2b858fe5.png)

Khả năng xử lý cao, cùng một lúc hơn 10.000 kết nối với bộ nhớ thấp.

Phục vụ Static Files và lập chỉ mục cho tập tin.

Dùng bộ nhớ đệm cache để tăng tốc proxy ngược, cân bằng tải đơn giản và khả năng chịu lỗi.

Hỗ trợ tăng tốc với bộ nhớ đệm của WSGI, SCGI, FastCGI và các máy chủ Memcached.

Có cấu hình linh hoạt và khả năng lưu lại nhật ký truy vấn.

Chuyển hướng lỗi 3XX – 5XX.

Sử dụng Regular Expressions để Rewrite URL.

Hạn chế tỷ lệ đáp ứng truy vấn.

Giới hạn truy vấn từ một địa chỉ hoặc số kết nối đồng thời.

Có khả năng nhúng mã PERL.

Tương thích và hỗ trợ Ipv6.

Hỗ trợ WebSockets.

Hỗ trợ truyền tải file MP4 và FLV.

Rewrite URL,…


# So sánh Apache và NGINX

![image](https://user-images.githubusercontent.com/62273292/160291244-051adf1e-889d-4f8e-a25f-2ea31726cfac.png)


## Hệ điều hành hỗ trợ

Hiện nay, Apache hoạt động trên tất cả các loại hệ thống Unix-like (Linux hoặc BSD) và hỗ trợ đầy đủ cho Microsoft Windows.

Và với NGINX thì nó cũng chạy trên một vài hệ thống trong số chúng. Bên cạnh đó cũng hỗ trợ Windows nhưng hiệu suất thì không được mạnh bằng.

### Hiệu suất

**Đối với web tĩnh**

Dựa trên một thử nghiệm kiểm chuẩn chạy tới 1000 kết nối đồng thời thì NGINX nhanh hơn 2,5 lần Apache.

![image](https://user-images.githubusercontent.com/62273292/160291299-22fe70b1-d4fd-4c7e-9013-9121aeefa4e9.png)


Một thử nghiệm khác với 512 kết nối đồng thời, NGINX nhanh hơn khoảng 2 lần và tiêu thụ ít bộ nhớ hơn (4%).

Như vậy, đối với web tĩnh thì NGINX rõ ràng vượt trội hơn. Nên nếu cần xử lý nhiều nội dung tĩnh thì NGINX là sự lựa chọn hoàn hảo dành cho bạn.

**Đối với web động**

Bạn có thể cân nhắc sử dụng NGINX hay Apache nếu đã có một trang web động bằng WordPress, Joomla, Drupal,… Nội dung tĩnh trong các tình huống này ít hơn rất nhiều so với nội dung động.

Khi bạn xem xét các bài test điểm chuẩn của Speedemy và kết quả hoàn toàn giống nhau. Trong trường hợp này không có sự vượt trội nào so với NGINX. Bởi hầu hết các request đang xử lý trong PHP runtime environment khá giống nhau cho cả hai web server.

**Tính linh hoạt**

Một máy chủ web phải đủ linh hoạt để cho phép các tùy chỉnh. Apache làm điều đó khá tốt thông qua việc sử dụng các công cụ .htaccess, trong khi đó NGINX lại không hỗ trợ. Nó cho phép phân cấp nhiệm vụ admin. Admin bên thứ ba và admin cấp hai có thể bị ngăn truy cập vào máy chủ chính. Hơn nữa, Apache hỗ trợ hơn 60 module, giúp nó có khả năng mở rộng cao. Đây cũng chính là nguyên nhân vì sao Apache lại phổ biến hơn với các nhà cung cấp dịch vụ hosting.

**Bảo mật**

Cả Apache và NGINX đều rất coi trọng tính bảo mật trên trang web của mình. Không có hệ thống mạnh mẽ nào mà lại không có những biện pháp đối phó với các cuộc tấn công DDoS, phần mềm độc hại và phishing. Cả hai máy chủ này đều định kỳ phát hành báo cáo bảo mật và những tư vấn, đảm bảo rằng khía cạnh bảo mật được tăng cường ở mọi cấp độ.

**Hỗ trợ và tài liệu**

Apache sở hữu mạng lưới hỗ trợ cộng đồng lớn thông qua mailing lists, IRC và Stack Overflow. Ngoài ra, còn có tùy chọn hỗ trợ bên thứ ba từ OpenLogic.

Tương tự, NGINX cũng có hỗ trợ thông qua mailing lists, IRC và Stack Overflow. Nginx còn có một số sản phẩm có tên NGINX + có hỗ trợ riêng của Google bao gồm nhiều tính năng hơn.

Cả NGINX và Apache đều cung cấp tài liệu, bao gồm hầu hết mọi chủ đề và tính năng cần thiết. Tài liệu này bao gồm release notes, user guides, tutorials,… thậm chí còn có cả wiki riêng.

# Apache và Nginx, nên chọn loại máy chủ nào cho trang web?

NGINX và Apache đều có những ưu và nhược điểm riêng. Đây cũng là những lựa chọn sáng giá trong các lĩnh vực khác nhau. Nếu NGINX thích hợp với các nội dung tĩnh thì đối với nội dung động lại không tạo ra sự khác biệt thực sự giữa các máy chủ web.

![image](https://user-images.githubusercontent.com/62273292/160291460-6b98a7fd-51f4-4a72-95e8-dfa70c369e7b.png)


Hiện nay, trong hầu hết các lĩnh vực thì cả hai máy chủ này đều cạnh tranh với nhau. Nhưng với những lợi thế riêng biệt, Apache đi kèm với tài liệu lớn hơn và hỗ trợ tốt hơn để tải các module động khác nhau. Trong khi NGINX có thể phục vụ nhiều nguồn nội dung và phương tiện tĩnh cho các trang web có lưu lượng truy cập cao.

Bên cạnh đó, bạn cũng cần xem xét thêm các tính năng ở trên của NGINX và Apache để đưa ra quyết định cuối cùng. Giả sử nếu bạn đang chạy một trang web có lưu lượng truy cập cao với nhiều nội dung tĩnh thì bạn có thể chọn NGINX. Nhưng nếu bạn coi trọng sự giàu có của tài nguyên và cộng đồng hỗ trợ thì Apache sẽ là phương án tốt hơn.

**Đánh giá Apache vs NGINX, webserver nào tốt hơn**

Cả hai webserver hiện nay, đều có thể cạnh tranh với nhau trong hầu hết các tiêu chí.

Đối với nội dung tĩnh NGINX là vua, nhưng đối với nội dung động nó kém hơn một chút.

NGINX nổi bật với một số tính năng cao cấp của nó (media streaming, reverse proxying for non-HTTP protocols)

Người dùng shared hositng có thể thích sự tiện lợi của file .htaccess Apache.

Và Apache có khá nhiều dynamic module (NGINX mới chỉ bắt đầu thêm dynamic module)

NGINX được sử dụng chủ yếu cho VPS hosting, dedicated hosting, hoặc container cluster.

Với các website có lượt truy cập cao có nhu cầu phục vụ rất nhiều nội dung tĩnh và / hoặc streaming media sẽ hướng tới NGINX.

Nhưng đa phần cả 2 sẽ hoạt động tốt trong hầu hết mọi trường hợp

Bất kể với web server nào, hãy chọn một nhà cung cấp hosting tốt nhất trên nền tảng Linux.

Với VPS tôi khuyên bạn nên dùng Vultr, còn với Shared hosting Bluehost, HawkHost đều đáng sử dụng.















