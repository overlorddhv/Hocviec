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
**Bước 1:** Đầu tiên bạn hãy vào trang web Gihub.com. Sau đó nhập đầy đủ thông tin tài khoản của bạn và nhấn Sign up for Github.
![image](https://user-images.githubusercontent.com/48250210/157359636-73f86daa-5030-4ceb-8311-53327cf80102.png)

**Bước 2:** Lúc này bạn hãy vào Email để kích hoạt tài khoản của mình.
![image](https://user-images.githubusercontent.com/48250210/157359773-3640695c-a702-487e-ae9e-8f646f6934a7.png)
