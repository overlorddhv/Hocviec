# 1. SSH là gì?

SSH, hay Secure (Socket) Shell, là một giao thức mạng cung cấp cho người dùng (đặc biệt là các QTV mạng) cách truy cập an toàn vào một máy tính qua một mạng không được bảo mật. Bên cạnh đó, SSH cũng cung cấp nhiều bộ tiện ích để triển khai giao thức SSH. Secure Shell là một giao thức cung cấp khả năng xác thực password mạnh mẽ, cùng với khả năng giao tiếp dữ liệu được mã hóa giữa hai máy tính kết nối với nhau qua một mạng mở như Internet. Bên cạnh đó, SSH cũng được sử dụng phổ biến bởi các QTV mạng để quản lý hệ thống và ứng dụng từ xa. Từ đó cho phép đăng nhập vào các máy tính khác qua mạng và thực hiện các tác vụ cơ bản như thực thi lệnh, di chuyển file,… SSH bao gồm cả giao thức mạng lẫn một bộ tiện ích để triển khai giao thức đó. SSH sử dụng mô hình client-server, kết nối một ứng dụng Secure Shell client (nơi session được hiển thị) với một SSH server (nơi session chạy). Triển khai SSH thường hỗ trợ cả các giao thức ứng dụng, dùng cho giả lập terminal hay truyền file. Ngoài ra, SSH cũng có thể được dùng để tạo các tunnel bảo mật cho nhiều giao thức ứng dụng. Chẳng hạn như để chạy các phiên đồ họa X Windows System từ xa. Một SSH server theo mặc định sẽ nghe trên cổng TCP 22.

# 2. Chức năng

SSH hỗ trợ các chức năng sau đây:

   - Truy cập từ xa an toàn vào các hệ thống hay thiết bị mạng có hỗ trợ SSH cho người dùng và các quá trình tự động khác.
   - Hỗ trợ phiên chuyển file an toàn
   - Tự động truyền file an toàn.
   - Thực thi lệnh an toàn trên các máy hay hệ thống từ xa.
   - Quản lý an toàn các thành phần cơ sở hạ tầng mạng.
  
  SSH có thể được sử dụng để enable các terminal session và nên được dùng thay thế cho các chương trình Telnet có độ bảo mật kém hơn. Ngoài ra, SSH cũng thường được dùng trong các script và nhiều phần mềm khác để cho phép các chương trình, hệ thống truy cập an toàn từ xa vào các tài nguyên khác.
  
# 3. Kỹ thuật mã hóa qua SSH

Lợi điểm khiến SSH hơn hẵn những giao thức cũ là khả năng mã hóa và truyền tải dữ liệu an toàn giữa host và client. Host đại diện cho máy chủ  từ xa bạn muốn kết nối tới và client là máy tính của bạn dùng để truy cập tới host. Có 3 cách khác nhau để mã hóa qua SSH:

  - Symmetrical encryption.
  - Asymmetrical encryption.
  - Hashing.
    
   **Symmetric Encryption**
   
  Symmetric encryption là một dạng mã hóa sử dụng secret key ở cả 2 chiều mã hóa và giải mã tin nhắnb bởi cả host và client. Có nghĩa là ai nắm được khóa đều có thể giải mã tin nhắn trong quá trình chuyền. Symmetrical encryption thường được gọi là shared key hoặc shared secret encryption. Vì có một khóa được sử dụng, hoặc một cặp khóa (pair key) mà một khóa có thể được tính ra từ khóa kia. Symmetric keys được sử dụng để mã hóa toàn bộ liên lạc trong phiên giao dịch SSH. Cả client và server tạo chung một key bí mật như là một phương thức thỏa thuận, và key đó không được tiết lộ cho bên thứ ba. Quá trình tạo symmetric key được thực hiện bởi key exchange algorithm. Điều khiến cho thuật toán an toàn là vì key không được truyền giữa client và host. Thay vào đó, cả 2 máy tính chia sẽ thông tin chung và sau đó sử dụng chúng để tính ra khóa bí mật.Kể cả có máy khác bắt được thông tin chung, nó cũng không thể tính ra key bí mật vì không biết được thuật toán tạo key. Cũng phải lưu ý rằng, tuy nhiên secret token được sử dụng cho một phiên SSH nhất định, và được tạo bởi chứng thực của client. Khi key đã được tạo, tất cả packets truyền giữa 2 máy phải được mã hóa bởi private key. Việc này bao gồm cả mật khẩu điền vào bởi user, vì vậy mật khẩu cũng có thể được bảo vệ khỏi những “lính bắn tỉa packet” trên mạng. Một số loại symmetrical encryption ciphers đã tồn tại, bao gồm, những không giới hạn AES (Advanced Encryption Standard), CAST128, Blowfish etc. Trước khi thiết lập kết nối an toàn client và host sẽ đồng ý loại cipher nào được sử dụng, bằng cách xuất bản danh sách cyphers được hỗ trợ để tham khảo. Cypher thích hợp nhất ở phía client sẽ hiển thị trong danh sách của host như là một bidirectional cypher.
  
  **Asymmetric Encryption**
  
  Không giống với symmetrical encryption, asymmetrical encryption sử dụng 2 khóa khác nhau để mã hóa và giải mã. 2 khóa này được gọi là public key và private key. Cả 2 hình thành nên một cặp khóa là public-private key pair. Khóa public, như tên gọi của nó sẽ được công khai cho tất cả các bên liên quan. Mặc dù nó liên quan mật thiết đến private key về chức năng, nhưng private key không thể được tính toán ra từ một public key. Sự liên quan này rất phức tạp: thư được mã hóa bởi public key của một máy, và chỉ có thể được giải mã bởi private key của chính máy đó. Sự liên quan một chiều này có nghĩa là public key không thể giải mã chính thư của nó, hoặc không thể giải mã bất kỳ thứ gì được mã hóa bằng private key. Private key phải luôn luôn được đảm bảo an toàn, ví dụ, kết nối an toàn, không có bên thứ 3 biết. Sức mạnh của cả chu trình kết nối phụ thuộc vào việc private key có bị tiết lộ hay không, vì chỉ có nó mới có khả năng giải mã thư được truyền đi mà được mã hóa bởi public key. Vì vậy, bất kỳ bên nào có thể giải mã thư được ký bởi public key có nghĩa là bên đó đang sở hữu private key tương ứng. Không giống với quan niệm thông thường, asymmetrical encryption không được dùng để mã hóa toàn bộ phiên SSH. Thay vào đó, nó chỉ được sử dụng trong quá trình trao đổi thuật toán của khóa của symmetric encryption. trước khi bắt đầu một phiên giao dịch an toàn, cả 2 đồng ý tạo ra một cặp public-private key tạm, chia sẽ private keys để tạo một khóa secret key chung. Khi kết nối symmetrict an toàn đã được thiết lập, server sử dụng public key của client để tạo và challenge và truyền nó tới client để chứng thực. Nếu client có thể giải mã tin nhắn, có nghĩa là nó đang giữa đúng private key cần thiết cho kết nối. Phiên giao dịch SSH bắt đầu.
  
  **Hashing**
  
  Hashing một chiều là một dạng mã hóa khác sử dụng trong Secure Shell Connections. Hash một chiều khác với cả 2 phương thức mã hóa trên ở chỗ nó không được sinh ra để giải mã. Chúng tạo ra một giá trị duy nhất với độ dài nhất định cho mỗi lần nhập liệu mà không có hướng nào khác để khai thác. Điều này khiến nó dường như không thể quay ngược lại giải mã. Rất dễ để tạo một cryptographic hash từ một lần input, nhưng không thể tạo ra lần input đó từ một hash. Có nghĩa là nếu client giữ đúng input đó, client có thể tạo ra một crypto-graphic hash giống như vậy và so sánh nó với giá trị ở đầu bên kia để xác định cả 2 bên nhập giống input. SSH sử dụng hashes để xác nhận tính xác thực của tin nhắn. Nó được thực hiện bởi HMACs, hoặc Hash-based Message Authentication Codes. Việc này đảm bảo lệnh không bị giả mạo bởi bất kỳ phương thức nào. Trong khi thuật toán symmetrical encryption được chọn, một thuật toán xác thực tin nhắn phù hợp cũng được chọn. Nó hoạt động tương tự việc cipher được chọn như thế nào, như bên trên mình đã giải thích trong phần symmetric encryption. Mỗi tin nhắn được truyền đi phải chứa MAC, được tính bởi symmetric key, packet sequence number, và nội dung tin nhắn. Nó truyền ra ngoài một gói dữ liệu được mã hóa symmetric như là một phần của communication packet.
  
