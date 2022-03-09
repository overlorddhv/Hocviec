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
