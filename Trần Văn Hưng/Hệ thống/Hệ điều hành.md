# 1. Hệ điều hành

Hệ điều hành trong tiếng Anh có nghĩa là Operating System, viết tắt là OS. Đây là một phần mềm để cài vào hệ thống máy tính và các thiết bị di động thông minh. Nó được dùng để quản lý, vận hành các phần cứng của thiết bị như RAM, CPU, ổ cứng cùng nhiều tài nguyên phần mềm. Chúng giữ nhiệm vụ là cầu nối giữa máy và người dùng.

# 2. Các thành phần của hệ điều hành

Hệ điều hành được cấu tạo từ các thành phần và tính năng khác nhau. Trong đó, có ba thành phần dễ dàng được xác định là:

- Kernel: Đây là phần hỗ trợ điều khiển cấp cơ bản trên các phần cứng của máy tính. Phần này giữ nhiệm vụ, đọc dữ liệu của bộ nhớ, xử lý các lệnh thực hiện. Ngoài ra, nó còn có thể xác định cách dữ liệu được nhận, gửi các phụ kiện màn hình, chuột, bàn phím và nhận định cách diễn giải dữ liệu nhận được từ mạng.
- User Interface (Giao diện người dùng): Đây là phần giúp người dùng tương tác với các thiết bị điện thoại. Họ có thể sử dụng nó thông qua các icon và một desktop hoặc một command line.
- Application Programming Interfaces (Giao diện lập trình ứng dụng): Phần này cho phép những nhà phát triển ứng dụng viết modular code.

![image](https://user-images.githubusercontent.com/55913475/158007714-f1673859-fce8-416c-8403-9db4a060c908.png)

# 3. Chức năng của hệ điều hành

Hệ điều hành là chỗ để quản lý thông tin các phần cứng. Trong đó gồm có: quản lý CPU, bộ nhớ, quản lý mạng, thiết bị cá nhân và hệ thống tập tin. Nó còn hỗ trợ người dùng có được giao diện phù hợp để sử dụng các ứng dụng trên thiết bị. Chúng sẽ cải thiện tối đa quá trình hoạt động của máy tính, gồm các công đoạn nhập liệu hoặc thao tác.

Ngoài ra, hệ điều hành còn là cầu nối giữa người dùng và thiết bị. Nó giúp chúng ta truy cập ứng dụng nhanh và xử lý các tài nguyên khác. Ngoài ra, chúng còn hỗ trợ người dùng xử lý các xung đột phần mềm hệ thống và các app khác.

# 4. Cấu trúc hệ điều hành

  **Cấu trúc đơn giản**
  
  Hệ điều hành không được chia thành những lớp(phần) rõ rệt, một lớp có thể gọi hàm thuộc bất kỳ lớp nào khác. Hệ điều hành ngày đơn giản, dễ cài đặt nhưng khó bảo vệ, khỏ mở rộng, và khó nâng cấp.
  
  **Cấu trúc phân lớp**

  Hệ điều hành được chia thành nhiều lớp, mỗi lớp được xây dựng dựa vào những lớp thấp hơn. Lớp dưới cùng là phần cứng, lớp trên cùng là lớp giao tiếp với người sử dụng. Mỗi lớp chỉ sử dụng những hàm do lớp dưới cung cấp. Hạt nhân ở lớp kế lớp phần cứng, dùng các lệnh của phần cứng để tạo các lời gọi hệ thống.

  **Cấu trúc máy ảo**

  Với hệ điều hành máy ảo, một máy được giả lập thành nhiều máy, tài nguyên cảu hệ thống như là CPU, bộ nhớ, đĩa,... được chia sẻ để tạo các máy ảo. Mỗi máy ảo được cô lập với máy ảo khác nên tài nguyên dùng chung được bảo vệ nhưng cũng dẫn đến việc không được chia sẻ tài nguyên trực tiếp.

  **Cấu trúc Client-Server

  Hệ điều hành được chia thành nhiều phần(gọi là các tiến trình server), mỗi tiến trình thực hiện một dịch vụ như là dịch vụ quản lý tập tin, quản lý tiến trình, quản lý bộ nhớ,... Các tiến trình yêu cầu(gọi là tiến trình client) sẽ gửi yêu cầu đến một tiến trình server, tiến trình server thực hiện và gửi kết quả trở lại cho tiến trình client. Hạt nhân chỉ có nhiệm vụ kiểm soát quá trình liên lác giữa các tiến trình client và server.

  ***Ưu điểm của cấu trúc Client-Server***
  
    - Hạt nhân rất nhỏ, chỉ gồm các lệnh cơ bản, nên dễ bảo vệ, dễ nâng cấp.
    - Mỗi dịch vụ của hệ điều hành do một tiến trình server đảm nhận, các tiến trình này độc lập với nhau nên khi một tiến trình server bị lỗi, hệ thống vẫn hoạt động.
    - Các tiến trình server được thực hiện ở chế độ người dùng(user-mode), không phải ở chế độ hạt nhân(kernel-mode), nên không truy xuất trực tiếp phần cứng.
    - Cấu trúc client-server rất thích hợp với mô hình hệ thống phân tán. Các tiến trình server có thể thực thi ở các máy khác nhau.
    
