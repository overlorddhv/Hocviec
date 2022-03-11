# Cách tạo một GitHub Repository

Repository là một không gian để lưu trữ dự án của bạn. Do tính chất phân tán của Git, nên có thể hiểu repository là nơi lưu trữ mã nguồn ở cả local và server.

Bạn có thể lưu trữ file code, text, hình ảnh hoặc bất kỳ loại tệp nào trong repository.

Để tạo một repository trên Github bạn làm như sau:

- Vào Github, đăng ký một tài khoản bằng cách click vào “Sign up for Github”.

(Xem hướng dẫn tạo tài khoản ở file: https://github.com/thongngoduc/Hocviec/blob/main/Ng%C3%B4%20%C4%90%E1%BB%A9c%20Th%C3%B4ng/Bu%E1%BB%95i%202/C%C3%A1ch%20t%E1%BA%A1o%20m%E1%BB%99t%20GitHub%20Repository.md)

- Sau khi đăng ký và kích hoạt thành công. Bạn bắt đầu tạo mới một project với “Start a new project”.
Bạn có thể xem hình bên dưới cho rõ thêm nhé:

![image](https://user-images.githubusercontent.com/65167293/157231192-c7a25cc2-b0ac-4c9e-b565-9fc64a376062.png)

- Nhập tên Repositoty và nhấn nút “Create Repository”. Ngoài ra, bạn cũng có thể thêm mô tả cho repo ( Cái này chỉ là lựa chọn, không bắt buộc phải có).

![image](https://user-images.githubusercontent.com/65167293/157231382-d15ad9ca-1dce-4782-a56a-660fe2bfff6c.png)

Trong đó, bạn lưu ý 2 options sau:

- Theo mặc định thì repository để là public. Tức là ai cũng có thể xem được repo này của bạn. Nếu dự án của bạn chưa muốn công khai mà chỉ muốn quản lý nội bộ thì chọn Private.
- Bạn có thêm một README file để giới thiệu repo kèm với một file .gitignore. Github đã có sẵn template .gitignore cho bạn, cứ chọn một template phù hợp với mã nguồn dự án là được.
Khi tạo xong, repo sẽ như sau:

![image](https://user-images.githubusercontent.com/65167293/157231520-82ab80de-86ae-4424-916b-925e4e9acc6f.png)

Khi đã có repository, bạn có thể clone, pull, push… source code của mình lên đó rồi.

Phần tiếp theo của bài viết, chúng ta sẽ tìm hiểu về branch trên Github.

# Tạo branch trên Github
Branch giúp bạn làm việc trên các phiên bản khác nhau của cùng một repository. Mình lấy ví dụ: Bạn muốn phát triển thêm một tính năng mới cho dự án. Nhưng bạn lại phần sửa đổi đó lại ảnh hưởng tới dự án chính. Lúc này branch ra đời.

Branch cho phép bạn chuyển đổi qua lại giữa các trạng thái và phiên bản khác nhau của dự án.

Với kịch bản ví dụ ở trên, bạn có thể tạo mới một branch và phát triển tính năng mới trên đó mà không ảnh hưởng tới master branch. Sau khi đã implement xong, test kỹ càng thì có thể merge vào master branch.

![image](https://user-images.githubusercontent.com/65167293/157231769-d15841ce-5177-4247-bf8e-6f33d61372db.png)

Để tạo một branch trên Github, bạn làm như sau:

- Click vào dropdown branch: Branch: master
- Khi danh sách branch xổ ra, bạn có thể tạo thêm một branch mới tại đây

![image](https://user-images.githubusercontent.com/65167293/157231851-382517bd-f4b6-40d6-9536-46aec9eedc01.png)

# Hướng dẫn sử dụng Github chi tiết
Github có đầy đủ những command của git. Nhưng do bài viết này quá dài nên mình sẽ không liệt kê hết tất cả chúng ở đây. Mình sẽ tập trung hướng dẫn những command cơ bản nhất, hay dùng trên Github.

# 1. Commit Command
Commit command cho phép bạn lưu lại những thay đổi của file. Khi bạn commit, nên viết mô tả rõ ràng trong commit message. Điều này sẽ giúp cho quản lý dự án tốt hơn, có thể theo dõi, review những thay đổi source code sau này.
Để tạo commit, bạn làm như sau:

- Chọn file muốn sửa
- Chọn “Edit” để sửa file.
- Sau khi sửa xong thì điền thông tin message và nhấn Commit.

![image](https://user-images.githubusercontent.com/65167293/157231987-b42911f8-4ba2-4ea9-9975-1a053a140b58.png)

2. Pull Command
Lệnh PULL request là lệnh quan trọng  nhất trên Github. Nó cho biết những thay đổi trong source code, và yêu cầu owner của source code xem xét nó và merge nó vào master branch.

Một khi commit xong, bất kể ai cũng có thể update sự thay đổi và thảo luận về sự thay đổi đó.

Tính năng này rất hay cho các dự án mã nguồn mở. Khi mà bất kì cũng có thể đóng góp công sức cho dự án. Tất nhiên, mọi sự thay đổi đều phải được sự đồng ý của owner dự án.

Ở đây, mình cần làm rõ hơn với các bạn đỡ nhầm lẫn về lệnh Pull:

- Lệnh pull request : Là lệnh yêu cầu chủ owner dự án xem xét một thay đổi nào đó trước khi merge vào master branch.
- Lệnh Pull: đây là lệnh của git, đơn thuần có thể hiểu là lệnh update source code từ server về local. Nếu có bất kì sự xung đột code nào (conflict) thì bạn cần phải resolve nó.

![image](https://user-images.githubusercontent.com/65167293/157232093-3c664e57-6df2-4d3b-a988-28834297603e.png)

![image](https://user-images.githubusercontent.com/65167293/157232166-2cdb90bb-58e1-4417-ae0f-f305127fc2c9.png)

![image](https://user-images.githubusercontent.com/65167293/157232188-7449f7d9-08eb-4895-a007-7a9a014a88fc.png)

# 3. Merge command
Lệnh cơ bản cuối cùng mà mình muốn nhắc đến là merge. Lệnh merge này cho phép bạn hợp nhất những thay đổi vào một branch.

- Click vào “Merge pull request” để hợp nhất những thay đổi vào master branch.
- Click vào “Confirm merge”.
Bạn có thể tham khảo hình bên dưới:

![image](https://user-images.githubusercontent.com/65167293/157232305-b63c71b9-12c1-4406-aa7f-889728a9abb1.png)

# Cloning dự án từ Github
Tiếp tục hướng dẫn sử dụng Github. Đây có lẽ là thao tác bạn hay dùng nhất khi tìm kiếm mã nguồn mở trên mạng. Khi bạn thấy một dự án nào đó hay ho và có thể ứng dụng được cho dự án của mình, bạn muốn download dự án này về máy tính để tham khảo.

Có 2 cách để tải dự án từ Github:

- Một là bạn chọn Zip toàn bộ dự án và tải về

![image](https://user-images.githubusercontent.com/65167293/157232431-9b97fb24-7f23-4400-a84b-f1b4b1d662aa.png)

Hai là bạn có thể clone dự án về bằng lệnh git. Bạn cũng click vào “Clone or Download”. Sau đó copy đường dẫn và gõ trong cửa sổ terminal trên máy tính như sau

      git clone git@github.com:vntalking/demo-create-repro.git
      
 # Tạm kết
Trên đây, mình đã hoàn thành hướng dẫn cách sử dụng Github cơ bản. Tất cả các thao tác đều thực hiện trên web.
Mình sẽ tiếp tục gửi tới các bạn nhiều cách để tương tác với GitHub để các bạn có thể tham khảo thêm.

# Tham Khảo
 1. https://vntalking.com/
