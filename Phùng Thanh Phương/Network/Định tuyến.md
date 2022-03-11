**1. Khái niệm về định tuyến**

Định tuyến là quá trình xác định đường đi tốt nhất trên một mạng máy tính để gói tin tới được đích theo một số thủ tục nhất định nào đó thông qua các nút trung gian là các bộ định tuyến router. Thông tin về những con đường này có thể được cập nhật tự động từ các router khác hoặc là do người quản trị mạng chỉ định cho router. Sau khi Router nhận gói tin, thì Router sẽ gỡ bỏ phần header lớp 2 để tìm địa chỉ đích thuộc lớp 3. Sau khi đọc xong địa chỉ đích lớp 3 nó tìm kiếm trong Routing Table cho mạng chứa địa chỉ đích.

Giả sử mạng đó có trong Routing Table, Router sẽ xác định địa chỉ của router hàng xóm (router chia sẻ chung kết nối). Sau đó gói tin sẽ được đẩy ra bộ đệm của cổng truyền đi tương ứng, router sẽ khám phá loại đóng gói lớp 2 nào được sử dụng trên kết nối giữa 2 router. Gói tin được đóng gửi xuống lớp 2 và đưa xuống môi trường truyền dẫn dưới dạng bit và được truyền đi bằng tín hiệu điện, quang hoặc sóng điện từ. Quá trình sẽ tiếp tục cho tới khi gói tin được đưa đến đích thì thôi.

Để làm được việc này thì các router cần phải được cấu hình một bảng định tuyến (Routing Table) và giao thức định tuyến (Routing Protocol). Bảng định tuyến là bảng chứa tất cả những đường đi tốt nhất đến một đích nào đó tính từ router. Khi cần chuyển tiếp một gói tin, router sẽ xem địa chỉ đích của gói tin, sau đó tra bảng định tuyến và chuyển gói tin đi theo đường tốt nhất tìm được trong bảng. Trong bảng định tuyến có thể bao gồm một tuyến mặc định, được biểu diễn bằng địa chỉ 0.0.0.0 0.0.0.0.

Bảng định tuyến của mỗi giao thức định tuyến là khác nhau, nhưng có thể bao gồm những thông tin sau:

- Địa chỉ đích của mạng, mạng con hoặc hệ thống.

- Địa chỉ IP của router chặng kế tiếp phải đến.

- Giao tiếp vật lí phải sử dụng để đi đến Router kế tiếp.

- Subnet mask của địa chỉ đích.

- Khoảng cách đến đích (ví dụ: số lượng chặng để đến đích).

- Thời gian (tính theo giây) từ khi Router cập nhật lần cuối.

Giao thức định tuyến là ngôn ngữ giao tiếp giữa các router. Một giao thức định tuyến cho phép các router chia sẻ thông tin về các network, router sử dụng các thông tin này để xây dựng và duy trì bảng định tuyến.
