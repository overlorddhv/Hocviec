**1. Khái niệm về định tuyến**

Định tuyến là quá trình xác định đường đi tốt nhất trên một mạng máy tính để gói tin tới được đích theo một số thủ tục nhất định nào đó thông qua các nút trung gian là các bộ định tuyến router. Thông tin về những con đường này có thể được cập nhật tự động từ các router khác hoặc là do người quản trị mạng chỉ định cho router. Sau khi Router nhận gói tin, thì Router sẽ gỡ bỏ phần header lớp 2 để tìm địa chỉ đích thuộc lớp 3. Sau khi đọc xong địa chỉ đích lớp 3 nó tìm kiếm trong Routing Table cho mạng chứa địa chỉ đích.

Giả sử mạng đó có trong Routing Table, Router sẽ xác định địa chỉ của router hàng xóm (router chia sẻ chung kết nối). Sau đó gói tin sẽ được đẩy ra bộ đệm của cổng truyền đi tương ứng, router sẽ khám phá loại đóng gói lớp 2 nào được sử dụng trên kết nối giữa 2 router. Gói tin được đóng gửi xuống lớp 2 và đưa xuống môi trường truyền dẫn dưới dạng bit và được truyền đi bằng tín hiệu điện, quang hoặc sóng điện từ. Quá trình sẽ tiếp tục cho tới khi gói tin được đưa đến đích thì thôi.

Để làm được việc này thì các router cần phải được cấu hình một bảng định tuyến (Routing Table) và giao thức định tuyến (Routing Protocol). Bảng định tuyến của mỗi giao thức định tuyến là khác nhau, nhưng có thể bao gồm những thông tin sau:

- Địa chỉ đích của mạng, mạng con hoặc hệ thống.

- Địa chỉ IP của router chặng kế tiếp phải đến.

- Giao tiếp vật lí phải sử dụng để đi đến Router kế tiếp.

- Subnet mask của địa chỉ đích.

- Khoảng cách đến đích (ví dụ: số lượng chặng để đến đích).

- Thời gian (tính theo giây) từ khi Router cập nhật lần cuối.

Giao thức định tuyến là ngôn ngữ giao tiếp giữa các router. Một giao thức định tuyến cho phép các router chia sẻ thông tin về các network, router sử dụng các thông tin này để xây dựng và duy trì bảng định tuyến.

Giao thức định tuyến (Routing Protocol) : là một tập hợp các quy tắc mô tả một giao thức lớp 3 sẽ gửi cập nhật cho nhau về các mạng hiện có. Nếu có nhiều đường đi đến một mạng cùng tồn tại, giao thức định tuyến cũng sẽ xác định đường đi tốt nhất được dùng. Khi các thiết bị có chung một hiểu biết về mạng đó, các thiết bị sẽ bắt đầu chuyển tiếp các gói tin trên đường đi tốt nhất

Vùng tự trị (Autonomous System – AS): Internet được chia thành các vùng nhỏ hơn gọi là các vùng tự trị. AS bao gồm tập hợp các mạng con được kết nối với nhau bởi Router. Một hệ thống AS thông thường thuộc quyền sở hữu của một công ty hay của một nhà cung cấp dịch vụ Internet(ISP) và các AS được kết nối với nhau. Nhà quản lí phải đăng kí với cơ quan quản trị mạng trên Internet (Inter NIC) để lấy được một số nhận dạng AS cho riêng mình. Bên trong mỗi AS, nhà quản lí có quyền quyết định loại Router cũng như giao thức cho hệ thống định tuyến của mình.

Bảng định tuyến (routing table): một Router phải xem xét bảng định tuyến của mình trước khi chuyển gói tin đến địa chỉ ở xa. Bảng này chứa các thông tin về mạng đích mà Router cần biết để truyền gói tin một cách chính xác. Thông tin có thể bao gồm các địa chỉ mạng, mạng con, các hệ thống độc lập. Trong bảng định tuyến có thể bao gồm một tuyến mặc định, được biểu diễn bằng địa chỉ 0.0.0.0 0.0.0.0.
Bảng định tuyến của mỗi giao thức định tuyến là khác nhau, nhưng có thể bao gồm những thông tin sau:
* Địa chỉ đích của mạng, mạng con hoặc hệ thống.
* Địa chỉ IP của Router chặng kế tiếp phải đến.
* Giao tiếp vật lí phải sử dụng để đi đến Router kế tiếp.
* Mặt nạ mạng của Địa chỉ đích.Khoảng cách đến đích (VD: số lượng chặng để đến đích).
* Thời gian (tính theo giây) từ khi Router cập nhật lần cuối

Khoảng cách quản trị (Administrative Distance) : được sử dụng để đánh giá độ tin cậy của thông tin định tuyến mà Router nhận từ router hàng xóm. AD là một số nguyên nhận giá trị từ 0 đến 255 (0: tương ứng với độ tin cậy cao nhất; 255: không có lưu lượng đi qua tuyến này hay tuyến này không được sử dụng để vận chuyển thông tin của người sử dụng). Thông tin định tuyến được đánh giá dựa vào AD, AD càng thấp thì tuyến đó càng tin cậy.

Metric
