# Git là gì?

Git là một phần mềm kiểm soát phiên bản nguồn mở, miễn phí. Nó được tạo bởi Linus Torvalds vào năm 2005. Công cụ trong cộng đồng IT này là một hệ thống kiểm soát phiên bản ban đầu được phát triển để làm việc với một số nhà phát triển trên nhân Linux.

![image](https://user-images.githubusercontent.com/62273292/158340507-a578dfb0-902f-4683-93c6-621e805a2bf5.png)

Điều này về cơ bản có nghĩa là Git là một trình theo dõi nội dung. Vì vậy, Git có thể được sử dụng để lưu trữ nội dung – và nó chủ yếu được sử dụng để lưu trữ code vì các tính năng khác mà nó cung cấp.

Các dự án thực tế thường có nhiều nhà phát triển làm việc song song. Vì vậy, họ cần một hệ thống kiểm soát phiên bản như Git để đảm bảo rằng không có xung đột code giữa chúng.

Ngoài ra, các yêu cầu trong dự án như vậy thay đổi thường xuyên. Vì vậy, một hệ thống kiểm soát phiên bản cho phép các nhà phát triển quay lại phiên bản cũ hơn của code của họ.

Hệ thống chi nhánh trong Git cho phép các nhà phát triển làm việc riêng lẻ trên một tác vụ (Ví dụ: Một nhánh -> Một tác vụ HOẶC Một nhánh -> Một nhà phát triển). Về cơ bản, hãy nghĩ về Git như một ứng dụng phần mềm nhỏ kiểm soát cơ sở code của bạn, nếu bạn là nhà phát triển.
![image](https://user-images.githubusercontent.com/62273292/158340588-c10ff495-2dad-423e-9b7c-a20c0448d032.png)


## Tại sao nên sử dụng Git?

Có rất nhiều lợi thế để bạn nên sử dụng Git trong việc lập trình ngay từ hôm nay, bất kể là lập trình cái gì đi chăng nữa.

 - Git dễ sử dụng, an toàn và nhanh chóng.
 - Có thể giúp quy trình làm việc code theo nhóm đơn giản hơn rất nhiều bằng việc kết hợp các phân nhánh (branch).
 - Bạn có thể làm việc ở bất cứ đâu vì chỉ cần clone mã nguồn từ kho chứa hoặc clone một phiên bản thay đổi nào đó từ kho chứa, hoặc một nhánh nào đó từ kho chứa.
 - Dễ dàng trong việc deployment sản phẩm.
 Và nhiều hơn thế nữa.
Nếu bạn là một lập trình viên thì Git là một hệ thống bạn cần phải biết cách sử dụng, ít nhất là ngay từ bây giờ.

Và bắt đầu sử dụng Git thế nào thì ở bài sau chúng ta sẽ tìm hiểu tới.

## Cách Git hoạt động

Nếu chúng ta muốn bắt đầu sử dụng Git, chúng ta cần biết nơi lưu trữ các repository của mình.

Một kho lưu trữ (hay gọi tắt là Repo) là một dự án chứa nhiều tệp. Trong trường hợp của chúng ta, một kho lưu trữ sẽ chứa các tệp dựa trên code.

Có hai cách bạn có thể lưu trữ kho của bạn. Một là trực tuyến (trên đám mây) và thứ hai là ngoại tuyến (tự cài đặt trên máy chủ của bạn).

Có ba dịch vụ lưu trữ Git phổ biến: GitHub (thuộc sở hữu của Microsoft), GitLab (thuộc sở hữu của GitLab) và BitBucket. Chúng ta sẽ sử dụng GitHub trong bài này.

## Git giúp dễ dàng đóng góp cho các dự án nguồn mở

Gần như mọi dự án nguồn mở đều sử dụng GitHub để quản lý các dự án của họ. Sử dụng GitHub là miễn phí nếu dự án của bạn là nguồn mở và nó bao gồm wiki và trình theo dõi vấn đề giúp dễ dàng đưa vào tài liệu chuyên sâu hơn và nhận phản hồi về dự án của bạn.

Nếu bạn muốn đóng góp, bạn chỉ cần rẽ nhánh (lấy một bản sao) của một dự án, thực hiện các thay đổi của bạn và sau đó gửi pull request dự án bằng giao diện web của GitHub. Pull request này là cách bạn nói với dự án là bạn đã sẵn sàng để họ xem xét các thay đổi của bạn.

## Tài liệu

Bằng cách sử dụng GitHub, bạn sẽ dễ dàng có được tài liệu tuyệt vời. Phần trợ giúp và hướng dẫn của họ có bài viết cho gần như bất kỳ chủ đề nào liên quan đến Git mà bạn có thể nghĩ đến.

## Tùy chọn tích hợp

GitHub có thể tích hợp với các nền tảng phổ biến như Amazon và Google Cloud, với các dịch vụ như Code Climate để theo dõi phản hồi của bạn và có thể đánh dấu cú pháp trong hơn 200 ngôn ngữ lập trình khác nhau.

## Theo dõi các thay đổi trong code của bạn qua các phiên bản

Khi nhiều người cùng hợp tác trong một dự án, thật khó để theo dõi các sửa đổi – ai đã thay đổi những gì, khi nào và nơi các tệp đó được lưu trữ.

GitHub xử lý vấn đề này bằng cách theo dõi tất cả các thay đổi đã được đẩy vào kho lưu trữ.

Giống như sử dụng Microsoft Word hoặc Google Drive, bạn có thể có lịch sử phiên bản code của mình để các phiên bản trước không bị mất. Thật dễ dàng để trở lại phiên bản trước và đóng góp công việc của bạn.

## Trưng bày công việc của bạn

Bạn có phải là nhà phát triển muốn thu hút nhà tuyển dụng? GitHub là công cụ tốt nhất bạn có thể dựa vào cho việc này.

Ngày nay, khi tìm kiếm tân binh cho các dự án của họ, hầu hết các công ty đều nhìn vào hồ sơ GitHub. Nếu hồ sơ của bạn có sẵn, bạn sẽ có cơ hội được tuyển dụng cao hơn ngay cả khi bạn không đến từ một trường đại học hoặc cao đẳng lớn.

