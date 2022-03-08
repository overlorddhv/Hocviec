# 1. Tải git về và cài đặt.
Download git tại trang chủ: https://git-scm.com/downloads

Sau khi down xong thì các bạn cài đặt ra, cứ next – next như cài các phần mềm bình thường.

Sau khi cài đặt xong các bạn sẽ thấy có 2 icon cho git được xuất hiện đó là git GUI và git Bash.

Chúng ta chỉ sử dụng git bash.

# 2. Cấu Hình và kết nối với server git hub.
Các bạn bật git bash lên và thực hiện cấu hình địa chỉ email và tài khoản cho nó với 2 câu lệnh sau.

      git config –global user.name “tên account”                     

      git config –global user.email “Email của bạn”

 (note: 2 dấu – ko cách)
 
 ![image](https://user-images.githubusercontent.com/65167293/157194951-55b35781-1992-474d-bae1-22ec088b54f9.png)

Sau khi cấu hình xong, chúng ta cần kết nối local với server.

 # a. Tạo SSH Key.

SSH Key là mã chìa khóa để server và local có thể kết nối được với nhau.

Và khi đi làm dự án của công ty. Bạn muốn tham gia vào project, thì sếp sẽ tạo một ssh key trên máy bạn, và sau đó lấy mã key đó add vào server github.

Như vậy server git hub sẽ quản lý được có bao nhiêu máy local đang kết nối với nó,

và nó cho phép clone code về các máy local.

Tóm lại SSH Key như một chìa khóa trung gian giao dịch giữa server và local.

– Đánh command:

        ssh-keygen -t rsa 

Một thông báo hiện ra yêu cầu bạn nhập đường dẫn cho ssh key y như mô tả (tức là bạn đánh lại dòng nó show cho bạn)

      c:/users/your_computer_name/.ssh/id_rsa      
// lưu ý your_computer_name tên máy tính của bạn.

Nó sẽ yêu cầu bạn nhập password 2 lần.

Lưu ý:  nó sẽ không hiển thị ký tự * hay ký gì đó đại diện cho passowrd, bạn có thể tưởng nhầm là mình đánh nhưng nó chưa nhận, nên có sai hay nhầm thì ấn phí backspace rồi nhập lại bình thường.

Nhập 2 lần chính xác.

Bạn phải nhớ password này vì nó là pass sau này bạn lấy code về hay đẩy code lên server sẽ dùng đến nó.

Sau khi nhập pass thành công, thì nó thông báo, ssh key của bạn được tạo trong file *pub.

Bạn tìm và mở file .pub đó lên và coppy toàn bộ nội dung của nó. Đó chính là mã ssh key của bạn.

b. Add SSH Key vào server git hub

Bây giờ bạn vào trang git hub, bạn đăng nhập vào rồi vào mục account chọn setting

![image](https://user-images.githubusercontent.com/65167293/157196342-c6928c25-0eef-4503-83cf-2b4c6d3e04ef.png)

Bạn nhấn chọn vào SSH and GPG keys

![image](https://user-images.githubusercontent.com/65167293/157196631-ae0a10ed-d782-4b31-a1d3-1cac715f4223.png)

Tại đây bạn có thể thấy hiện có bao nhiêu máy local được kết nối với server của bạn, bạn có thể thêm hoặc remove các tài khoản.

Bạn chọn New SSH Key để add key của bạn vào.

![image](https://user-images.githubusercontent.com/65167293/157196954-2a18e305-7ef9-454b-92a8-5af49ab3023a.png)

– Tiêu đề nên chọn tên của người code. Ví dụ bạn làm việc theo team, bạn nên để tên của các thành viên để dễ quản lý.

– Sau đó paste đoạn key mà bạn copy trong file *pub từ máy local vào mục key, sau đó ấn vào button Add ssh key.

Ok. Việc add key đã hoàn tất.
