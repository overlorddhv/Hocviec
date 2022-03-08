# Tìm hiểu về git và git hub.
1. Một số khái niệm

   GitHub là một dịch vụ nổi tiếng cung cấp kho lưu trữ mã nguồn Git cho các dự án phần mềm. Github có đầy đủ những tính năng của Git, ngoài ra nó còn bổ sung những tính năng về social để các developer tương tác với nhau.
   
*Vài thông tin về GIT:

- Là công cụ giúp quản lý source code tổ chức theo dạng dữ liệu phân tán.
- Giúp đồng bộ source code của team lên 1 server.
- Hỗ trợ các thao tác kiểm tra source code trong quá trình làm việc (diff, check modifications, show history, merge source, …)

  GitHub có 2 phiên bản: miễn phí và trả phí. Với phiên bản có phí thường được các doanh nghiệp sử dụng để tăng khả năng quản lý team cũng như phân quyền bảo mật dự án.
  Còn lại thì phần lớn chúng ta đều sử dụng Github với tài khoản miễn phí để lưu trữ source code.

  Github cung cấp các tính năng social networking như feeds, followers, và network graph để các developer học hỏi kinh nghiệm của nhau thông qua lịch sử commit.

  Nếu một comment để mô tả và giải thích một đoạn code. Thì với Github, commit message chính là phần mô tả hành động mà bạn thực hiện trên source code.

  Github trở thành một yếu tố có sức ảnh hưởng lớn trong cộng động nguồn mở. Cùng với Linkedin, Github được coi là một sự thay thế cho CV của bạn. Các nhà tuyển dụng cũng rất hay tham khảo Github profile để hiểu về năng lực coding của ứng viên.

  Giờ đây, kỹ năng sử dụng git và Github từ chỗ ưu thích sang bắt buộc phải có đối với các ứng viên đi xin việc.

2. Tính năng của GitHub

  GitHub được coi là một mạng xã hội dành cho lập trình viên lớn nhất và dễ dùng nhất với các tính năng cốt lõi như:

- Wiki, issue, thống kê, đổi tên project, project được đặt vào namespace là user.
- Watch project: theo dõi hoạt động của project của người khác. Xem quá trình người ta phát triển phầm mềm thế nào, project phát triển ra sao.
- Follow user: theo dõi hoạt động của người khác.

	Có 2 cách tiếp cận GitHub: Tạo project của riêng mình Contribute cho project có sẵn: fork project có sẵn của người khác, sửa đổi, sau đó đề nghị họ cập nhật sửa đổi của mình (tạo pull request).

3. Các thuật ngữ liên quan cần nắm

- git: là prefix của các lệnh được sử dụng dưới CLI
- branch: được hiểu như là nhánh, thể hiện sự phân chia các version khi 2 version đó có sự sai khác nhất định và 2 version đều có sự khác nhau.
- commit: là một điểm trên cây công việc (Work Tree ) hay gọi là cây phát triển công việc
- clone: được gọi là nhân bản, hay thực hiện nhân bản. Sử dụng để clone các project, repository trên các hệ thống chạy trên cơ sở là git, ví dụ như: bitbucket, github, gitlab, cor(1 sản phẩm mã nguồn mở cho phép người dùng tự tạo git server cho riêng mình trên vps, server),… Việc clone này sẽ sao chép repository tại commit mình mong muốn, dùng để tiếp tục phát triển. Thao tác này sẽ tải toàn bộ mã nguồn, dữ liệu về máy tính của bạn.
- folk: Folk là thao tác thực hiện sao chép repository của chủ sở hữu khác về git account của mình. sử dụng và đối xử như 1 repository do mình tạo ra.
- repository: Kho quản lý dữ liệu, là nơi lưu trữ các dữ liệu, mã nguồn của project.
- tag: sử dụng để đánh dấu một commit khi bạn có quá nhiều commit tới mức không thể kiểm soát được.
- remote: sử dụng để điều khiển các nhánh từ một repository trên git server, đối xử với các nhánh trên remote tương tự như đối xử với các nhánh trên local
- diff: So sánh sự sai khác giữa phiên bản hiện tại với phiên bản muốn so sánh, nó sẽ thể hiện các sự khác nhau
- .gitignore: file mặc định của git sử dụng để loại bỏ (ignore) các thư mục, file mà mình không muốn push lên git server

4. Lịch sử của GiHub

  GitHub được viết bằng Ruby on Rails và Erlang do Tom Preston-Werner, Chris Wanstrath, và PJ Hyett phát triển trang web được đưa ra và chạy chính thức vào tháng 4 năm 2008.

  Tính đến thời điểm tháng 3 năm 2018 Github đang là dịch vụ máy chủ lưu trữ các mã nguồn lập trình lớn nhất thế giới. Với hơn 25 triệu người dùng và hơn 80 triệu mã nguồn dự án, Github đã trở thành một phần không thể thiêu đối với cộng đồng phát triển mã nguồn mở và cộng đồng lập trình viên trên toàn thế giới.

5. Tại sao lập trình viên nên chọn GitHub

- Quản lý source code dễ dàng

  Khi bạn tạo một repo, toàn bộ source code của repo đó được lưu trên GitHub. Tại đây, bạn có thể coi lại quá trình mình đã làm việc thông qua các comment sau mỗi lần commit. Và cái hay ở đây, là nhiều người có thể cùng làm một repo.

  Lợi ích đầu tiên, chính là bạn biết được ai đã commit và commit cái gì. Tiếp theo, source của bạn có thể phát triển theo nhiều nhánh. Nguyên tắc làm việc với các nhánh như thế này: Bạn có thể rẽ nhiều nhánh để phát triển project. Nhưng cuối cùng, bạn phải merge lại vào nhánh MASTER để ra được project hoàn chỉnh.
	
6. Tracking sự thay đổi qua các version

	Khi có nhiều member cùng thực hiện một dự án thì khá là phức tạp để theo dõi revisons – ai thay đổi cái gì, lúc nào và mấy cái files đó được stored ở đâu. Đừng lo vì GitHub đã tính đến chuyện này giúp bạn, bằng cách luôn lưu lại những thay đổi bạn đã push lên repository. Cũng tương tự với Microsoft Word hay Google Drive, bạn có một lịch sử phiên bản để phòng trường hợp các phiên bản trước đó bị mất hay không được lưu.
	
7. Markdown

	Markdown là một cách định dạng text trên web. Bạn có thể chỉnh sửa cách hiển thị của document, format từ như định dạng in đậm hay in nghiêng, thêm hình và tạo list những thứ bạn có thể làm với Markdown. Hầu hết, Markdown chỉ là đoạn text đơn thuần với những ký tự đặc biệt chèn vào, như (#) hay (*) Trong GitHub thì bạn có thể sử dụng Mardown ở những nơi: Git, Comments tại Issues và Pull Requests, các file có đuôi .md hay .markdown extension

8. GitHup chứng tỏ bạn là ai

	Chẳng thể phủ nhận những lời hay ý đẹp bạn viết trong CV là cần thiết. Nhưng Source code luôn là minh chứng tốt nhất để thể hiện bạn là developer thực thụ. Có thể nói, 1 phần GitHub “nho nhỏ” trong CV có thể đánh bóng vị trí của bạn, nổi bật hơn những ứng cử viên khác. Đối với nhà tuyển dụng, GitHub cũng giống như một chiếc máy liar-detech – phân biệt real developer với những kẻ “faker”.

	Hãy đầu tư cho mình một tài khoản Github thật ấn tượng và đưa đường dẫn vào trong CV, chẳng nhà tuyển dụng nào lại dại dột mà bỏ qua bạn đâu.

	Có rất nhiều công ty lớn trên thế giới xem đây là một yêu cầu trong quy trình tuyển dụng của họ. Nếu bạn có nhiều đóng góp cho cộng đồng hoặc có nhiều sản phẩm trên Github, sẽ là một lợi thế rất lớn so với các ứng viên khác. Vì bằng cách đăng tải các project của mình lên đây, bạn đã tạo cho mình một profile cá nhân vô cùng đáng tin cậy.

	Vì khi nhìn vào đó, nhà tuyển dụng sẽ biết được ngay thế mạnh của bạn là gì, và khả năng coding của bạn thế nào.

9. Github giúp cải thiện kỹ năng code, thậm chí là tracking bug

	Có hàng ngàn hàng vạn cách để học, học trên Github sẽ là một ý kiến không tồi trong thời đại này. Với hàng vạn open source projects, hàng trăm ngàn contributors, hàng tỉ commit mỗi ngày thì chỉ bằng việc xem. So sánh, học tập từ những thay đổi đó đã đem lại cho bạn hàng tá điều hay để cải thiện kỹ năng code của bản thân mình.

	“Bug tracking” là một tính năng được GitHub tích hợp vào để đơn giản hóa quá trình “tìm và diệt bọ”. Để hiểu được quy trình thì những gì bạn cần làm là mở dashboard của từng project lên và filter các thông tin. Sau đó, các câu hỏi sẽ được hệ thống, sắp xếp theo mức độ phổ biến, thời gian update hay tương tại. Phần mềm này cũng có giao diện khá mượt nên luôn được xếp hạng cao trong cộng đồng IT dev.
	
10. Github là một kho tài nguyên tuyệt vời

	Với chức năng Explore, bạn có thể theo dõi, tìm kiếm những open source projects theo đúng technology pattern mà bạn ưa thích. Github hỗ trợ code search không kể nó ở dưới dạng một project riêng biệt hay là website. Ngoài ra, nền tảng này cũng có SEO khá tốt nên người dùng có thể tìm kiếm bất kỳ code string nào được chia sẻ public.
	
11. Github Action

	Trên server của Github có những workflow scripts chạy tự động. Dev có thể dùng chúng để phản hồi các events trên repositories hoặc thực hiện vài action. Ví dụ như tôi có viết một cái tiện ích nho nhỏ, Autotagger – GitHub Marketplace, sẽ tự động tạo git tafs khi mà số phiên bản của package.json thay đổi. Nhìn thì đây chỉ là hành động nhỏ nhưng sẽ có tác động rất lớn khi phải truy tìm code ngược về bản phát hành, và bớt đi một cơn “nhức đầu” cho các project maintainers đó chứ.
	
	![image](https://user-images.githubusercontent.com/65167293/157165156-50d5c44e-6c6f-4223-ad1a-312d3aa49f48.png)

12. Github Package Registry

	Cái package registry này cho phép lập trình viên duy trì distribution registries của họ, bao gồm npm, docker, maven, nuget và Ruby gems.
	![image](https://user-images.githubusercontent.com/65167293/157165273-f1d6303e-c42f-4719-9dcb-ff53a6ae9646.png)

	Đừng ngần ngại mà không tạo ngay cho mình một tài khoản Github. Tạo những project của riêng mình và chia sẻ với mọi người, hoặc bạn có thể thoải mái fork một project của một open source nào đó. Tạo pull request hoặc issues nếu như tìm được lỗi, cần support.
	
13. Mở rộng mối quan hệ

- Gặp gỡ những dev mới
	Vài ngàn developer toàn cầu đang tham gia mạng lưới rộng lớn của GitHub để chia sẻ kinh nghiệm của họ cũng như những ý tưởng rất đỉnh.

- Chia sẻ kinh nghiệm bản thân
	Git cho phép user share code, text fragments hay bất kỳ thông tin nào với các dev khác. Do đó bạn có thể dùng nó để trao đổi text, hay gists work như git repositories, từ đó tách ra và update các phiên bản đó.

# Tham Khảo
1. https://topdev.vn/blog/github-la-gi/#mot-vai-khai-niem-cua-git-ban-can-nam
2. https://phattrienphanmem123az.com/
