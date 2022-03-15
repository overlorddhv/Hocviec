# Giao thức IMAP
  
## 1. Giao Thức IMAP là gì?
  
IMAP là chữ viết tắt của Internet Message Access Protocol là một giao thức được ra đời vào năm 1986 cho phép bạn truy cập email của mình mọi lúc mọi nơi, từ bất kỳ thiết bị.

Khi bạn đọc email bằng cách dùng IMAP, bạn thực sự không phải tải xuống hoặc lưu trữ nó trên máy tính của mình. Thay vào đó, bạn đang đọc nó từ dịch vụ email. Nhờ đó, bạn có thể kiểm tra email bạn từ thiết bị khác nhau như điện thoại, máy tính,... ở bất kỳ đâu trên thế giới.

IMAP chỉ tải xuống thư khi bạn bấm vào nó và phần đính kèm không tự động được tải xuống. Cách này giúp bạn có thể kiểm tra thư của bạn nhanh chóng nhiều hơn POP.

![image](https://user-images.githubusercontent.com/62273292/158334853-69c1fcb7-a9e6-4e55-9bcd-f1b3998eca95.png)


## 2. Cách thức hoạt động

Kết nối đến server
Lấy nội dung được người dùng yêu cầu và lưu vào bộ nhớ đệm trên thiết bị cục bộ. VD: danh sách các email mới, danh sách email theo một truy vấn tìm kiếm...
Hiển thị các nội dung đã lấy trên phần mềm của người dùng, xử lý các biên tập thêm/xóa/sửa của người dùng lên các email.
Ngắt kết nối.
Các bước làm việc của IMAP phức tạp hơn so với POP. Về cơ bản, email vẫn được lưu trên server, người dùng chỉ copy một bản lưu tạm trên thiết bị cá nhân (Một số phần mềm cho phép tải một hoặc nhiều email được chỉ định hoàn toàn về thiết bị).

## 3. Ưu điểm IMAP và lý do điện thoại nên sử dụng IMAP

Mail được lưu trữ trên server, có thể truy cập từ nhiều thiết bị và địa điểm khác nhau (điện thoại, máy tính…)
Xem nhanh hơn do chỉ cần tải trước danh sách email với các tiêu đề với các yêu cầu rõ ràng thay vì phải đồng bộ toàn bộ như POP.
Tiết kiệm không gian lưu trữ trên thiết bị cục bộ đặc biệt là điện thoại
Vẫn cho phép lưu trữ email cục bộ (cài đặt trên phần mềm).
Việc sử dụng IMAP trên điện thoại sẽ làm cho việc đồng bộ dữ liệu dễ dàng giữa điện thoại máy tính và server.
Sử dụng POP3 trên điện thoại sẽ có nguy cơ bị mất dữ liệu cao hơn, vì điện thoại có thể bị mất hoặc bị hư bất cứ lúc nào. Và việc đồng bộ dữ liệu có thể không đảm bảo vì khi email tải về thì sẽ tự động xóa trên server.

## 4. Nhược điểm của IMAP:

Vì IMAP lưu các email trên mail server, nên dung lượng hòm thư của bạn sẽ bị giới hạn bởi các nhà cung cấp dịch vụ mail. Nếu bạn có một lượng lớn email cần lưu trữ, bạn sẽ gặp nhiều vấn đề khi gửi nhận mail khi hòm thư bị đầy. Nhiều người giải quyết vấn đề này bằng cách tạo một bản sao copy của các email đó thông qua mail client, sau đó xóa bỏ email gốc trên server. Ngoài ra nếu bạn sử dụng Gmail theo tên miền và vượt quá giới hạn dung lượng mặc định là 15GB/tài khoản, bạn có thể mua thêm dung lượng tài khoản với giá từ 700k / năm.

Ngoài ra, nếu sử dụng IMAP thì bạn cần phải có kết nối Internet nếu muốn truy cập email (IMAP chỉ kéo email headers về, nội dung email vẫn còn trên server).

