# Giao thức Https

## Giao thức Https là gì?

Https là phiên bản an toàn của http (viết tắt của Hyper Text Transfer Protocol Secure - giao thức truyền tải siêu văn bản bảo mật), giao thức mà qua đó dữ liệu được gửi giữa trình duyệt và trang web bạn đang kết nối.

## HTTPS hoạt động như thế nào?

Các trang HTTPS thường sử dụng một trong hai giao thức bảo mật để mã hóa thông tin liên lạc - SSL (Secure Sockets Layer, tầng ổ bảo mật) hoặc TLS (Transport Layer Security, bảo mật tầng truyền tải). Cả hai giao thức TLS và SSL đều sử dụng hệ thống PKI (Public Key Infrastructure, hạ tầng khóa công khai) không đối xứng. Một hệ thống không đối xứng sử dụng hai “khóa” để mã hóa thông tin liên lạc, khóa “công khai” và khóa “riêng”. Bất cứ thứ gì được mã hóa bằng khoá công khai (public key) chỉ có thể được giải mã bởi khóa riêng (private key) và ngược lại.

Như tên cho thấy, khóa “riêng” cần được bảo vệ nghiêm ngặt và chỉ truy cập được bởi chủ nhân của khóa riêng. Trong trường hợp một trang web, khóa riêng được giữ kín trên máy chủ web. Ngược lại, khóa công khai được phân phối cho bất kỳ ai và tất cả mọi người cần để có thể giải mã thông tin đã được mã hoá bằng khóa riêng.


## Chứng chỉ HTTPS là gì?

Khi yêu cầu kết nối HTTPS với trang web, đầu tiên trang web sẽ gửi chứng chỉ SSL tới trình duyệt của bạn. Chứng chỉ này chứa khóa công khai cần thiết để bắt đầu phiên bảo mật. Dựa trên trao đổi ban đầu này, trình duyệt và trang web sẽ bắt đầu giao thức SSL handshake (giao thức bắt tay). Giao thức SSL handshake liên quan đến việc tạo bí mật chia sẻ để thiết lập kết nối an toàn duy nhất giữa bạn và trang web

Khi sử dụng chứng chỉ SSL đáng tin cậy trong quá trình kết nối HTTPS, người dùng sẽ thấy biểu tượng ổ khóa trong thanh địa chỉ của trình duyệt. Khi một chứng chỉ Extended Validation Certificate được cài đặt trên một trang web, thanh địa chỉ sẽ chuyển sang màu xanh lá cây

## Lợi ích của giao thức HTTPS

Lợi ích chính của chứng chỉ HTTPS là:
- Thông tin khách hàng, như số thẻ tín dụng, được mã hóa.
- Khách truy cập có thể xác minh bạn là một doanh nghiệp đã đăng ký và bạn sở hữu tên miền.
- Nhận được niềm tin của khách hàng và hoàn tất việc mua hàng từ các trang web sử dụng HTTPS.
