# SSH: Secure Socker Shell

**1. SSH là gì?**

SSH là một chương trình tương tác giữa máy chủ và máy khách có sử dụng cơ chế mã hoá đủ mạnh nhằm ngăn chặn các hiện tượng nghe trộm, đánh cắp thông tin trên đường truyền. Các chương trình trước đây: telnet, rlogin không sử dụng phương pháp mã hoá. Vì thế bất cứ ai cũng có thể nghe trộm thậm chí đọc được toàn bộ nội dung của phiên làm việc bằng cách sử dụng một số công cụ đơn giản. Sử dụng SSH là biện pháp hữu hiệu bảo mật dữ liệu trên đường truyền từ hệ thống này đến hệ thống khác.

SSH bao gồm cả giao thức mạng lẫn một bộ tiện ích để triển khai giao thức đó. SSH sử dụng mô hình client-server, kết nối một ứng dụng Secure Shell client (nơi session được hiển thị) với một SSH server (nơi session chạy). Triển khai SSH thường hỗ trợ cả các giao thức ứng dụng, dùng cho giả lập terminal hay truyền file. Ngoài ra, SSH cũng có thể được dùng để tạo các tunnel bảo mật cho nhiều giao thức ứng dụng. Chẳng hạn như để chạy các phiên đồ họa X Windows System từ xa. Một SSH server theo mặc định sẽ nghe trên cổng TCP 22.

![image](https://user-images.githubusercontent.com/48250210/158010704-5ef5112c-3c17-4b2b-bae3-b64c630d4d9e.png)

**2. Giao thức SSH hoạt động như thế nào?**

Secure Shell được tạo ra để thay thế các chương tình giả lập terminal hoặc chương trình đăng nhập không an toàn như Telnet, rlogin (remote login) hay rsh (remote shell). Bên cạnh đó, SSH cũng hỗ trợ các chức năng tương tự như đăng nhập và chạy các terminal session trên hệ thống ở xa. SSH cũng thay thế các chương trình truyền file như FTP (File Transfer Protocol) hay rcp (remote copy).

Chức năng đơn giản nhất của SSH là kết nối đến một host ở xa cho một phiên terminal, bằng lệnh như sau:

    ssh server.example.org
    
Qua lệnh này, client sẽ kết nối đến một server có tên server.example.com bằng user ID là UserName. Nếu đây là lần kết nối đầu tiên giữa host và server, người dùng sẽ được thông báo về public key fingerprint của host ở xa và nhắc người dùng kết nối:


    The authenticity of host 'sample.ssh.com' cannot be established.

    DSA key fingerprint is 
    01:23:45:67:89:ab:cd:ef:ff:fe:dc:ba:98:76:54:32:10.

    Are you sure you want to continue connecting (yes/no)?

Nếu chọn yes, phiên sẽ được tiếp tục và host key được lưu trữ trong file known_hosts của hệ thống cục bộ. Đây là một file ẩn và được lưu trữ mặc định trong một directory ẩn tên là /.ssh/known_hosts, trong home directory của người dùng. Sau đó, client có thể kết nối trực tiếp đến server đó lần nữa mà không cần phê duyệt; host key sẽ xác thực kết nối.

**3. Chức năng của giao thức SSH**

Sau khi biết được giao thức SSH là gì và hoạt động như thế nào? Chắc hẳn bạn đang thắc mắc về các chức năng của SSH key. Thì, SSH hỗ trợ các chức năng sau đây:

* Truy cập từ xa an toàn vào các hệ thống hay thiết bị mạng có hỗ trợ SSH cho người dùng và các quá trình tự động khác.
* Hỗ trợ phiên chuyển file an toàn
* Tự động truyền file an toàn.
* Thực thi lệnh an toàn trên các máy hay hệ thống từ xa.
* Quản lý an toàn các thành phần cơ sở hạ tầng mạng.

SSH có thể được sử dụng để enable các terminal session và nên được dùng thay thế cho các chương trình Telnet có độ bảo mật kém hơn. Ngoài ra, SSH cũng thường được dùng trong các script và nhiều phần mềm khác để cho phép các chương trình, hệ thống truy cập an toàn từ xa vào các tài nguyên khác.

**4. Ứng dụng của SSH là gì?**

* SSH có mặt trong mọi datacenter và được đi kèm mặc định trong mọi server Unix, Linux và Mac. Các kết nối SSH hiện đang được ứng dụng để bảo mật nhiều loại giao tiếp khác nhau giữa một máy cục bộ và một host từ xa. Trong đó bao gồm cả quyền truy cập an toàn từ xa vào các tài nguyên, thực thi lệnh từ xa hay chuyển các bản patch, bản cập nhật phần mềm,… Bên cạnh khả năng tạo ra các kênh an toàn cho máy cục bộ và máy ở xa, SSH cũng dùng để quản lý router, phần cứng của server, các nền tảng ảo hóa, hệ điều hành, và có trong các ứng dụng quản lý và truyền file,…
* Secure Shell được dùng để kết nối đến các server, thực hiện các thay đổi, upload,… bằng các công cụ hay thông qua terminal. Bên cạnh đó, các SSH key cũng được dùng để tự động truy cập vào server, chủ yếu được ứng dụng trong các script, hệ thống backup hay các công cụ quản lý cấu hình,…
* SSH được thiết kế với mục đích đề cao sự thuận tiện và khả năng làm việc xuyên ranh giới giữ các tổ chức, do đó SSH key cung cấp một single sign-on (SSO – đăng nhập một lần) để người dùng có thể nhanh chóng chuyển qua lại giữa các tài khoản mà không cần tốn thời gian nhập password.
* Hơn nữa, SSH không chỉ xác thực qua một kết nối được mã hóa, mà mọi SSH traffic đều được mã hóa; cho dù người dùng đang truyền file, duyệt web hay chạy lệnh, mọi tác vụ của họ đều được bảo mật tuyệt đối.
* Ta có thể sử dụng SSH với một user ID thông thường và password làm thông tin xác thực, tuy nhiên SSH chủ yếu dựa vào các public key pair để xác thực các host với nhau. Người dùng cá nhân vẫn phải sử dụng user ID và password – hoặc các phương pháp xác thực khác – để có thể kết nối đến host từ xa, tuy nhiên máy cục bộ và máy từ xa sẽ xác thực riêng biệt với nhau. Việc này được thực hiện bằng cách tạo một public key pair duy nhất cho từng host trong quá tình giao tiếp. Mỗi session yêu cầu có hai public key pair: một key pair dùng để xác thực máy từ xa với máy cục bộ, và bộ key pair có nhiệm vụ ngược lại.

**5.Ưu điểm của SSH**

SSH cho phép mã hóa dữ liệu để những kẻ tấn công không thể đánh cắp thông tin người dùng và mật khẩu của bạn. SSH cũng cho phép tạo các giao thức truyền dữ liệu khác như FTP. Dưới đây là danh sách những điều cụ thể mà SSH bảo vệ bạn.

* IP source routing
* Giả mạo DNS
* Nghe lén dữ liệu được truyền
* Giả mạo địa chỉ IP
* Thao túng dữ liệu trên routers

**Các kỹ thuật mã hóa khác**

Ưu điểm của SSH so với các giao thức cũ là khả năng mã hóa và truyền tải dữ liệu một cách an toàn giữa host và client.
Có 3 cách để mã hóa khi sử dụng SSH

* Symmetrical encryption.
* Asymmetrical encrytion.
* Hashing.
