# Tổng quan về GitHub
Trước khi tìm hiểu GitHub là gì, chúng ta cần phải biết về Git. Git là gì? Git là một hệ quản trị phiên bản được phát triển bởi Linus Torvalds. Có thể hiểu nôm na là Git giống như trái tim của GitHub. Nếu Git là trái tim thì Hub cũng được ví như phần hồn của GitHub. Hub trong GitHub là nơi biến những dòng lệnh, Git, thành một mạng xã hội khổng lồ cho lập trình viên.

Như vậy tóm lại GitHub là sự kết hợp giữa 2 từ, Git là hệ thống quản lý dự án và phiên bản code, còn Hub là một mạng xã hội cho lập trình viên. Nó sử dụng để hợp tác nhiều người lại với nhau, từ mọi nơi trên thế giới, lên kế hoạch, theo dõi và làm chung một dự án.

GitHub cũng là một nền tảng lưu trữ online lớn nhất trên thế giới về các dự án nhiều người làm.

Github cung cấp các tính năng social networking như feeds, followers, và network graph để các developer học hỏi kinh nghiệm của nhau thông qua lịch sử commit.

**Một số thuật ngữ cơ bản**
* Repository

Nơi lưu trữ program và file ở trong hệ thống quản lý Version. Trên Git chia repository thành 2 loại là Local repository và Remote repository.

* Local repository

Repository đang thao tác hiện tại, trong trường hợp thao tác chủ yếu trên máy tính cá nhân hoặc server phát triển gọi là local repository. Ngoài ra, có thể sao chép repository từ remote repository và xây dựng môi trường trên máy tính cá nhân hoặc server

* Remote repository

Repository nằm ngoài, có thể thao tác thông qua local repository. Có thể sử dụng trong trường hợp nhiều người thao tác, public trên internet

* Working tree

Nơi người dùng edit, tạo file mới

* Index

Nơi bảo trì trạng thái sau khi edit trên working tree là đối tượng tiếp theo trước khi commit lên repository

* Branch

Dùng để phân nhánh và ghi chép lịch sử. Nhánh đã chia không bị ảnh hưởng của nhánh khác nên có thể cùng có nhiều thay đổi trong repository giống nhau

Trên Git có 3 loại local branch, remote branch, remote tracking branch

Local branch: Branch có thể quản lý trong local repository

Remote branch: Branch ở trong remote repository

Remote tracking branch: Branch để local repository tracking (theo dõi) remote branch. Ví dụ origin/master biểu thị cho việc đang tracking branch master có ở remote repository gọi là origin

* Check out

Triển khai branch ở repository lên working tree

Trên Git không chỉ branch mà tag, Specific commit, branch của remote repository cũng có thể check out

* Tag

Tên được gắn vào để có thể dễ dàng tham chiếu commit

* Commit

Message gắn vào khi thay đổi file
# 1. Cách tạo tài khoản GitHub
**Bước 1.** Đầu tiên bạn hãy vào trang web Gihub.com. Sau đó nhập đầy đủ thông tin tài khoản của bạn và nhấn Create Account.
![image](https://user-images.githubusercontent.com/48250210/157361736-97afa9eb-3d8a-4f89-9887-c175cdd6c0c8.png)
![image](https://user-images.githubusercontent.com/48250210/157361142-f76379dc-fd80-4829-85a4-fb36860e4ec5.png)
![image](https://user-images.githubusercontent.com/48250210/157361304-644a4a74-88dc-4f18-82e7-26c1bda6eb8c.png)

**Bước 2.** Lúc này bạn hãy vào Email để kích hoạt tài khoản của mình.
![image](https://user-images.githubusercontent.com/48250210/157359773-3640695c-a702-487e-ae9e-8f646f6934a7.png)

# 2. Cách tải và cài đặt GitHub
**Bước 1.** Vào trang web "https://desktop.github.com" và chọn Dowload for Windows (64Bit).
![image](https://user-images.githubusercontent.com/48250210/157362129-55c32b55-8580-4393-b86a-0ff90a505c4c.png)

**Bước 2.** Click đúp vào file vừa tải về. Lúc này ứng dụng sẽ tự động cài đặt vào máy.
![image](https://user-images.githubusercontent.com/48250210/157362250-1bc4fa12-5a45-4459-b66a-9bf8a5715cfc.png)

**Bước 3.** Sau khi cài đặt thành công bạn có thể đăng nhập tài khoản mình vừa tạo ở phía trên để sử dụng bằng cách chọn Sign in to GitHub.com
![image](https://user-images.githubusercontent.com/48250210/157362324-73129141-eafb-4514-9eda-cd7fcf5f4163.png)

**Bước 4.** Bạn nhập tên đăng nhập và mật khẩu, sau đó chọn Sign in. 
![image](https://user-images.githubusercontent.com/48250210/157362584-06d2844a-331f-4dfa-ae05-c82e85a9fb16.png)

**Bước 5.** Bạn nhập tên và email để hiển thị trong GitHub, sau đó nhấn Continue.
![image](https://user-images.githubusercontent.com/48250210/157362825-a2e0744d-2f36-48ba-9df5-65d362211839.png)

**Bước 6.** Nhấn Finish.\
![image](https://user-images.githubusercontent.com/48250210/157362919-54940cfe-a06e-487b-9559-f1ccd60682e8.png)
