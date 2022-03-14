# 1. Công nghệ ảo hóa

- Ảo hóa là công nghệ cho phép khai thác triệt để khả năng hoạt động của các phần cứng trong hệ thống máy chủ bằng cách chạy đồng thời nhiều OS trên cùng lớp vật lý.
Cùng chia sẻ tài nguyên phần cứng và được quản lý bởi lớp ảo hóa (Hypervisor).
- Lớp ảo hóa nằm giữa như một tầng trung gian giữa phần cứng (hardware) và phần mềm hệ điều hành (OS) giúp quản lý, phân phát tài nguyên phần cứng cho lớp OS ảo hoạt động ở trên.

Nó hoạt động như một tầng trung gian giữa phần cứng máy tính và phần mềm chạy trên nó. Ý tưởng của công nghệ máy chủ ảo hóa là từ một máy PC đơn lẻ có thể tạo thành nhiều máy ảo riêng biệt. Ảo hóa cho phép tạo nhiều máy ảo trên một máy chủ vật lý, mỗi một máy ảo cũng được cấp phát tài nguyên phần cứng như máy thật gồm có Ram, CPU, ổ cứng, Card mạng, các tài nguyên khác và hệ điều hành riêng. Khi chạy ứng dụng, người sử dụng không nhận biết được ứng dụng đó chạy trên lớp phần cứng ảo.

![image](https://user-images.githubusercontent.com/55913475/158132692-e04a9a8a-e353-4f05-a598-0e2fc3ea298d.png)

# 2. Các thành phần của hệ thống ảo hóa

![image](https://user-images.githubusercontent.com/55913475/158132920-a8a99d64-7077-4898-b7ee-a282f5c305de.png)

- Tài nguyên vật lý chính (Host machine / Host hardwave): Máy chủ vật lý, CPU, RAM, ổ đĩa cứng, card mạng… Nhiệm vụ là chia tài nguyên cấp cho các máy ảo.
- Phần mềm ảo hóa (Hypervisor): cung cấp truy cập cho mỗi máy chủ ảo đến tài nguyên của máy chủ vật lý, lập kế hoạch và phân chia tài nguyên vật lý cho các máy chủ ảo, cung cấp giao diện quản lý cho các máy chủ ảo
- Hệ điều hành khách (Guest Operating System): được cài đặt trên một máy chủ ảo, thao tác như ở trên hệ điều hành thông thường.
- Mảy ảo (Virtual Machine): nó hoạt động như một máy chủ vật lý thông thường với tài nguyên riêng, giao diện riêng, hệ điều hành riêng.

Một hệ thống ảo hóa bắt buộc phải có đầy đủ các thành phần: tài nguyên vật lý, phần mềm ảo hóa, máy chủ ảo và hệ điều hành khách. Khi có đầy đủ 4 thành phần của hệ thống ảo hóa, người dùng có thể dễ dàng xây dựng cho mình một hệ thống ứng dụng ảo hóa hoàn chỉnh.

# 3. Hoạt động của ảo hóa

Ảo hóa được xây dựng dựa trên giải pháp chia một máy vật lý thành nhiều máy con. Giải pháp này được biết đến với cái tên là Virtual Machine Monitor (VMM) hay thường được gọi là Hypervisor. VMM cho phép tạo tách rời các máy ảo và điều phối truy cập của các máy ảo này đến tài nguyên phần cứng và cấp phát tài nguyên tự động theo nhu cầu sử dụng. Cấu trúc này giúp cân bằng khả năng điện toán để mang lại:

- Nhiều ứng dụng chạy trên cùng một server, mỗi máy ảo được lập trình trên máy chủ, do đó nhiều ứng dụng và các hệ điều hành có thể cùng lúc chạy trên một host.
- Tối đa hóa công suất sử dụng và tối thiếu hóa server: Mỗi máy chủ vật lý được sử dụng với đầy đủ công suất, cho phép giảm đáng kể chi phí nhờ sử dụng tối đa server.
- Cấp phát tài nguyên và ứng dụng nhanh chóng, dễ dàng. Máy ảo được triển khai từ một file chứa đầy đủ phần mềm với cơ chế đơn giản là copy và Điều này mang đến sự đơn giản, nhanh chóng và linh hoạt chưa từng cócho việc quản lý và cung cấp hạ tầng Công nghệ thông tin. Máy ảo thậm chí cóthể di chuyển sang một server vật lý khác trong khi vẫn đang chạy, hoạt động bình thường. Doanh nghiệp có thể ảo hóa những ứng dụng quan trọng của doanh nghiệp để nâng cao hiệu suất, sự ổn định, khả năng mở rộng và giảm thiểu chi phí.

# 4. Mục tiêu của ảo hóa

Ảo hóa xoay quanh 4 mục tiêu chính: Availability, Scalability, Optimization, Management.

- Availability: giúp các ứng dụng hoạt động liên tục bằng cách giảm thiểu (bỏ qua) thời gian chết (downtime) khi phần cứng gặp sự cố, khi nâng cấp hoặc di chuyển.
- Scalability:  khả năng tùy biến, thu hẹp hay mở rộng mô hình server dễ dàng mà không làm gián đoạn ứng dụng.
- Optimization: sử dụng triệt để nguồn tài nguyên phần cứng và tránh lãng phí bằng cách giảm số lượng thiết bị vật lý cần thiết (giảm số lượng server, switch, cáp, v.v. )
- Management: khả năng quản lý tập trung, giúp việc quản lý trở nên dễ dàng hơn bao giờ hết.

# 5. Lợi ích và nhược điểm của ảo hóa

**Lợi ích của ảo hóa**

Ngày nay xu hướng ảo hóa máy chủ đã trở thành xu hướng chung của hầu hết các doanh nghiệp trên toàn thế giới. Những khó khăn trong thời kỳ khủng hoảng khiến cho các doanh nghiệp phải tìm mọi cách để giảm thiểu chi phí. Ảo hóa được coi là một công nghệ giúp các doanh nghiệp cắt giảm chi tiêu hiệu quả với khả năng tận dụng tối đa năng suất của các thiết bị phần cứng. Việc áp dụng công nghệ ảo hóa máy chủ đem lại những lợi ích như:

- Tiết kiệm năng lượng tiêu thụ, giảm chi phí duy trì server (tiền điện để chạy và làm mát server)
- Giảm số lượng thiết bị vật lý cần thiết (giảm số lượng server, switch, cáp, phí gia công)
- Tận dụng tối đa nguồn tài nguyên, tránh lãng phí.
- Quản lý tập trung, liên tục, nâng cao hiệu quả làm việc của quản trị viên.
- Khả năng mở rộng dể dàng
**Nhược điểm**

- Thông thường, mỗi máy ảo chỉ sử dụng một file VMDK (file này có thể được chia nhỏ tùy theo cách cài đặt) để lưu lại toàn bộ dữ liệu trong máy ảo và một số file nhỏ khác để lưu cấu hình máy ảo. Do đó, nếu một trong số những tệp tin bị lỗi hoặc bị mất mà chưa được backup thì có thể xem như máy ảo đã bị hư hoàn toàn và không thể phục hồi.
- Ngoài ra nếu máy chủ có cấu hình phần cứng thấp nhưng lại có một máy ảo sử dụng quá nhiều tài nguyên hoặc chạy quá nhiều máy ảo sẽ làm chậm toàn bộ hệ thống bao gồm các máy ảo và các ứng dụng chạy trên máy ảo. Đồng thời do một hoặc vài máy chủ phải đảm nhận nhiều máy ảo chạy trên nó nên máy chủ gặp trục trặc, sự cố thì các máy ảo cũng sẽ bị ảnh hưởng theo.
- Còn ở góc độ bảo mật, nếu hacker nắm quyền điều khiển một máy chủ vật lý chứa các máy ảo thì hacker có thể kiểm soát được tất cả các máy ảo trong nó.

# 6. Các mức độ ảo hóa

  **Ảo hóa toàn phần(full virtualization)
  
  Đây là loại ảo hóa mà ta không cần chỉnh sửa hệ điều hành khách (guest OS) cũng như các phần mềm đã được cài đặt trên nó để chạy trong môi trường hệ điều hành chủ (host OS). Khi một phần mềm chạy trên guest OS, các đoạn code của nó không bị biến đổi mà chạy trực tiếp trên host OS và phần mềm đó như đang được chạy trên một hệ thống thực sự. Bên cạnh đó, ảo hóa toàn phần có thể gặp một số vấn đề về hiệu năng và hiệu quả trong sử dụng tài nguyên hệ thống. Trình điều khiển máy ảo phải cung cấp cho máy ảo một “ảnh” của toàn bộ hệ thống, bao gồm BIOS ảo, không gian bộ nhớ ảo, và các thiết bị ảo. Trình điều khiển máy ảo cũng phải tạo và duy trì cấu trúc dữ liệu cho các thành phần ảo (đặc biệt là bộ nhớ), và cấu trúc này phải luôn được cập nhật cho mỗi một truy cập tương ứng được thực hiện bởi máy ảo.
  
  **Ảo hóa song song(Paravirtualization)
  
  Là một phương pháp ảo hóa máy chủ mà trong đó, thay vì mô phỏng một môi trường phần cứng hoàn chỉnh, phần mềm ảo hóa này là một lớp mỏng dồn các truy cập các hệ điều hành máy chủ vào tài nguyên máy vật lý cơ sở, sử dụng môt kernel đơn để quản lý các Server ảo và cho phép chúng chạy cùng một lúc (có thể ngầm hiểu, một Server chính là giao diện người dùng được sử dụng để tương tác với hệ điều hành). Ảo hóa song song đem lại tốc độ cao hơn so với ảo hóa toàn phần và hiệu quả sử dụng các nguồn tài nguyên cũng cao hơn. Nhưng nó yêu cầu các hệ điều hành khách chạy trên máy áo phải được chỉnh sửa. Điều này có nghĩa là không phải bất cứ hệ điều hành nào cũng có thể chạy ảo hóa song song được (trái với Ảo hóa toàn phần). XP Mode của Windows 7 là một ví dụ điển hình về ảo hóa song song.
  Phương pháp ảo hóa này có hai ưu điểm. Thứ nhất, giảm chi phí hoạt động do số lượng mã rất ít. Lớp phần mềm của ảo hóa song song hoạt động giống một cảnh sát giao thông , nó cho phép một hệ điều hành chủ truy cập các tài nguyên vật lý của phần cứng, đồng thời ngăn không cho các hệ điều hành chủ khác truy cập các nguồn tài nguyên đó. Ưu điểm thứ hai của ảo hóa song song song là nó không giới hạn các trình điều khiển thiết bị trong phần mềm ảo hóa; thực tế là ảo hóa song song không hề có các trình điều khiển thiết bị. Thay vào đó, nó sử dụng các trình điều khiển thiết bị có trong một hệ điều hành chủ, gọi là máy chủ đặc quyền. Nó cho phép các công ty tận dụng hiệu suất phần cứng các máy chủ, chứ không bị giới hạn phần cứng mà các trình điều khiển phải sẵn có trong phần mềm ảo hóa này như trong ảo hóa mô phỏng phần cứng.

Tuy nhiên, phương pháp ảo hóa này cũng có một nhược điểm lớn: Do ít quan trọng và dồn truy cập vào một phần cứng cơ sở, ảo hóa song song yêu cầu các hệ điều hành chủ phải được thay đổi để tương tác với giao diện của nó. Công việc này chỉ có thể được thực hiện khi truy cập mã nguồn của hệ điều hành. Do đó, nhược điểm này sẽ được giảm thiểu khi sử dụng các máy chủ có các con chip mới trong cơ sở hạ tầng sản xuất.

  **Ảo hóa hệ điều hành**

Một hệ điều hành được vận hành ngay trên một hệ điều hành chủ đã tồn tại và có khả năng cung cấp một tập hợp các thư viện tương tác với các ứng dụng, khiến cho mỗi ứng dụng truy xuất tài nguyên phần cứng cảm thấy như truy xuất trực tiếp máy chủ vật lý. Từ phối cảnh của ứng dụng, nó được nhận thấy và tương tác với các ứng dụng chạy trên hệ điều hành ảo, và tương tác với hệ điều hành ảo mặc dù nó kiểm soát tài nguyên hệ điều hành ảo. Nói chung, không thể thấy các ứng dụng này hoặc các tài nguyên hệ điều hành đặt trong hệ điều hành ảo khác. Phương pháp ảo hóa này đặc biệt hữu dụng nếu nhà cung cấp muốn mang lại cho cộng đồng người sử dụng khác nhau các chức năng khác nhau của hệ thống trên một một máy chủ duy nhất. Đây là một phương pháp lý tưởng cho các công ty máy chủ Web: Họ sử dụng ảo hóa container (OS ảo) để khiến cho một trang Web chủ “tin rằng” trang web này kiểm soát toàn bộ máy chủ Tuy nhiên, trên thực tế mỗi trang Web chủ chia sẻ cùng một máy với các trang Web khác, mỗi trang Web này lại có một container riêng. Ảo hóa hệ điều hành yêu cầu rất ít tài nguyên hệ thống, do đó bảo đảm hầu hết tài nguyên máy sẵn có cho các ứng dụng chạy trên container. Tuy nhiên, ảo hóa hệ điều hành vẫn có một số nhược điểm. Nhược điểm đầu tiên và lớn nhất là phương pháp này thường giới hạn sự lựa chọn hệ điều hành. Sự container hóa nghĩa là các container cung cấp một hệ điều hành tương tự như hệ điều hành chủ và thậm chí thống nhất về phiên bản và các bản vá lỗi.

Như chúng ta có thể tưởng tượng, có thể xảy ra vấn đề nếu nhà cung cấp muốn chạy các ứng dụng khác nhau trên các container, do các ứng dụng thường được chứng thực cho một phiên bản hệ điều hành và các bản vá lỗi. Do đó, ảo hóa hệ điều hành thích hợp nhất với cấu hình thuần nhất, trong các tình huống này ảo hóa hệ điều hành là sự lựa chọn hoàn hảo.

  **Ảo hóa ứng dụng**

Thông thường, khi muốn sử dụng một phần mềm nào đó như office, design, người dùng hay có suy nghĩ rằng cần phải tốn thời gian cài đặt phần mềm đó lên trên máy tính, cụ thể hơn là lên hệ điều hành đang sử dụng. Điều này tốn khá nhiều thời gian, nhất là nếu áp dụng trên những doanh nghiệp lớn, có cả ngàn máy tính, và đồng thời vấn đề quản lý các phần mềm này như ai truy xuất, thời gian truy xuất cho phép ra sao trở thành một thách thức thật sự.

Do đó, khái niệm ảo hóa ứng dụng ra đời. Một ứng dụng được ảo hóa sẽ không được cài đặt lên máy tính một cách thông thường, mặc dù ở góc độ người sử dụng, ứng dụng vẫn hoạt động một cách bình thường. Ảo hóa ứng dụng sẽ giúp tách rời sự phụ thuộc giữa nền tảng phần cứng, hệ điều hành và ứng dụng với nhau.

# 7. Các công nghệ hỗ trợ ảo hóa hệ thống

  **Công nghệ máy ảo(Virtual Machine)
  
  ![image](https://user-images.githubusercontent.com/55913475/158134884-47feabac-c63e-47d5-9139-eb2a89e56bfc.png)
  
  Máy ảo là một máy tính được cài trên mộ hệ điều hành khác hay một áy tính khác. Một máy ảo cũng bao gồm phần cứng, các ứng dụng phần mềm về hệ điều hành. Điều khác biệt ở đây là lớp phần cứng của máy ảo không phải là các thiết bị thường mà chỉ là một môi trường hay phân vùng mà ở đó nó được cấp phát một số tài nguyên như cpu, bộ nhớ, ổ đĩa…Công nghệ máy ảo cho phép cài và chạy nhiều máy ảo trên một máy tính vật lý. Mỗi máy ảo có một hệ điều hành riêng lẻ và được phân bố tài nguyên hợp lý, nó phụ thuộc vào nhu cầu của máy ảo và phương pháp ảo hóa được dùng. Khi máy ảo truy xuất tài nguyên phần cứng thì nó hoạt động như một máy tính bình thường.
  
  **Công nghệ lưu trữ SAN (Storage Aera networking)**
  
  SAN hay còn gọi là mạng lưu trữ là một mạng chuyên dụng, hoàn toàn tách biệt với các mạng LAN và WAN. Nói chung mạng SAN sẽ nối kết tất cả các tài nguyên liên quan đến lưu trữ trong mạng lại với nhau. Đặc điểm nổi bật trong cấu trúc SAN là nó thường cho tốc độ kết nối dữ liệu cao (Gigabit/sec) giữa các thiết bị lưu trữ ngoại vi, đồng thời cho khả năng mở rộng cao. Mặc dù thường được đề cập đến phần cứng nhiều hơn, SAN còn bao gồm những phần mềm chuyên biệt dùng cho quản lý, giám sát và cấu hình mạng.

SANs cung cấp nhiều lợi điểm. Quản lí và khai thác thiết bị lưu trữ ở dạng tập trung là một trong những mục tiêu phát triển chính của SAN. Đối với quản trị viên thì việc quản lý tất cả các nguồn tài nguyên lưu trữ trong môi trường luôn phát triển và đòi hỏi cao là một việc không dễ dàng, chi phí đắt. Còn đối với SANs thì chi phí quản lý cũng như độ phức tạp được giảm đáng kể trong khi vẫn cung cấp đầy đủ các tính năng kỹ thuật quan trọng.

  **Công nghệ cân bằng tải Clustering**
  
  Đây là công nghệ được dùng rộng rãi do tính kinh tế, đa dạng và khả năng dịch vụ cao. Công nghệ này có thể sử dụng phần cứng chuyên dụng để cung cấp một môi trường với độ tin cậy cao đảm bảo cho các dịch vụ có thể hoạt động trơn tru, luôn luôn sẵn sàng mà không bị dừng bởi một vài lỗi nhỏ, hoặc cũng có thể được thiết kế để chạy trên các phần cứng thông dụng mà vẫn đạt được các yêu cầu:

- Tăng cường khả năng mở rộng.
- Tính sẵn sàng cao và khắc phục sự cố.
- Nâng cao hiệu suất.

Hệ thống sử dụng công nghệ clustering gồm có các nút chủ động (active primary node) và các nút thụ động (passive backup node). Khi hệ thống hoạt động các nút chính sẽ thực hiện các dịch vụ còn các nút phụ sẽ không trực tiếp chạy dịch vụ, thay vào đó nó quản lí các dịch vụ của nút chủ động đang hoạt động, và đảm bảo chắc chắn là nít đang hoạt động vẫn phải đang còn hoạt động. Nếu nút không hoạt động phát hiện ra 1 vấn đề trên nút chính thì sẽ có một thông báo lỗi được khởi tạo. Khi có lỗi, hệ thống clusting sẽ thực thiện:

- Nút đang hoạt động sẽ trực tiếp ngắt hết các dịch vụ đang chạy và các kết nối.
- Nút không hoạt động sẽ khởi tạo các dịch vụ tương đương với dịch vụ của máy chủ động
- Nút không hoạt động bây giờ chuyển thành nút chủ động.

Và nút còn lại sau khi được khắc phục lỗi nó sẽ trở thành nút bị động.Và còn một số công nghệ khác hỗ trợ cho hệ thống ảo hóa như: công nghệ RAID, Network Load Balangcing (NLB),….
