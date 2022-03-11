# Địa chỉ Ipv4 là gì?

Ipv4 viết tắt cho Internet Protocol Version 4, dịch ra có nghĩa là giao thức Internet phiên bản thứ 4. Ipv4 đã được bộ quốc phòng Hoa Kỳ chuẩn hóa trong bản MIL-STD-1777. Giao thức Internet IP đã trải qua nhiều phiên bản khác nhau và phiên bản Ipv4 là phiên bản đầu tiên được sử dụng rộng rãi trên toàn thế giới và hiện vẫn còn đang là nòng cốt của Internet trên toàn thế giới. Ipv4 là giao thức mang tính hướng dữ liệu và được sử dụng cho hệ thống chuyển mạch gói. Ipv4 không quan tâm đến thứ tự truyền gói tin, cũng không đảm bảo gói tin sẽ đến đích hay là có xảy ra tình trạng lặp gói tin ở đích đến hay không. Nó chỉ có cơ chế đảm bảo tính toàn vẹn dữ liệu bằng việc sử dụng những gói kiểm tra được thiết lập đi kèm với nó. Địa chỉ Ipv4 là 1 địa chỉ đơn nhất đang được sử dụng bởi các thiết bị điện tử hiện nay để nhận diện và liên lạc với nhau trên Internet. Để đánh địa chỉ, Ipv4 sử dụng 32bit và chia ra làm 4 octet (mỗi octet có 8 bit = 1 byte). Dấu chấm được sử dụng để ngăn các octet với nhau.

# Các lớp của địa chỉ IPv4

Ban đầu, 1 địa chỉ Ipv4 được chia ra làm 2 phần là địa chỉ của mạng (Network ID) và địa chỉ của máy (Host ID). Địa chỉ của mạng (Network ID) được xác lập bởi octet đầu tiên và địa chỉ của máy (Host ID) được xác lập cho 3 octet còn lại. Với cách chia này thì địa chỉ của network bị giới hạn ở con số 256. Đây là con số quá ít so với nhu cầu sử dụng thực tế. Vì vậy người ta đã định nghĩa phân lớp mạng để vượt qua giới hạn này và tập hợp thành 1 lớp mạng đầy đủ còn được gọi là classful.

Địa chỉ IP được phân ra thành 5 lớp khác nhau: lớp A, lớp B, lớp C, lớp D,lớp E. Với cách phân loại này sẽ tạo được vô số địa chỉ IPv4 khác nhau.
- Lớp A: Như đã đề cập ở phần trên, địa chỉ Ipv4 được chia ra làm 4 octet. Lớp A của địa chỉ Ipv4 sử dụng octet đầu làm network và 3 Octet sau làm host. Bit đầu tiên của địa chỉ lớp A luôn được chọn là 0. Dải địa chỉ mạng lớp A chạy từ 1.0.0.0 đến 126.0.0.0. Vì vậy lớp A sẽ có tổng cộng 126 mạng. Trong khi đó mạng Loopback là 127.0.0.0. Phần host của lớp A có tất cả 24 bit. Do đó, mỗi lớp A có (224 – 2) host.
![image](https://user-images.githubusercontent.com/55913475/157800373-fc18a3e1-2379-44e4-8a32-ddab71931d23.png)
- Lớp B: Lớp B của địa chỉ Ipv4 sử dụng 2 obtet đầu làm phần mạng và 2 obtet sau làm phần host. Hai bit đầu tiên của lớp B luôn là 1 và 0. Dải địa chỉ mạng lớp B chạy từ 128.0.0.0 đến 191.255.0.0. Như vậy lớp B sẽ có tổng cộng 214 mạng. Vì phần host dài 16 bit nên mạng lớp B có (216 – 2) host.
![image](https://user-images.githubusercontent.com/55913475/157800438-822aaaee-413d-442a-a268-45ea524c1e3c.png)
- Lớp C: Lớp C của địa chỉ Ipv4 dùng 3 octet đầu làm phần mạng và 1 octet sau làm phần host. Địa chỉ lớp C luôn có 3 bit đầu là 1 1 0. Dải mạng lớp C chạy từ 192.0.0.0 -> 223.255.255.0. Như vậy sẽ có 221 mạng trong lớp C. Đối với phần host gồm 1 octet sau cùng nên dài 8 bit và sẽ có (28 – 2) host trong lớp C.
![image](https://user-images.githubusercontent.com/55913475/157800512-52e31f85-bf1c-43da-8e86-a2d8d5740d6c.png)
- Lớp D: Lớp D được sử dụng làm các địa chỉ multicast và dải địa chỉ lớp D từ 224.0.0.0 -> 239.255.255.255.
- Lớp E: Lớp E gồm các giải số từ 240.0.0.0 trở đi và được sử dụng cho mục đích dự phòng.

# Lưu ý của IPv4

- Các địa chỉ của lớp A, lớp B, lớp C của Ipv4 thường được dùng để đặt cho các host.
- Nên quan sát octet đầu tiên của địa chỉ Ipv4 để xác định địa chỉ IP thuộc lớp nào. Nếu octet đầu tiên từ 1 đến 126 thì địa chỉ thuộc lớp A. Nếu octet đầu tiên từ 128 đến 191 thì địa chỉ thuộc lớp B. Nếu octet đầu tiên từ 192 đến 223 thì địa chỉ thuộc lớp C. Nếu octet đầu tiên từ 224 đến 239 thì địa chỉ thuộc lớp D. Cuối cùng, nếu octet đầu tiên từ 240 đến 255 thì địa chỉ thuộc lớp E.

# Hạn chế của IPv4

Hạn chế lớn nhất của Ipv4 là cấu trúc thiết kế của nó không có bất cứ cách thức bảo mật nào cả. Ipv4 cũng hoàn toàn không có phương tiện mã hóa dữ liệu. Vì vậy, lưu lượng truyền tải dữ liệu giữa các host với nhau sẽ không được bảo mật, chỉ được bảo mật phổ biến ở mức ứng dụng mà thôi. Nếu áp dụng phương thức bảo mật phổ biến IPSec tại tầng IP thì mô hình bảo mật chủ yếu là bảo mật lưu lượng giữa các mạng còn việc bảo mật đầu cuối thường sử dụng rất hạn chế. Việc thiếu hụt không gian địa chỉ cũng là 1 trong những hạn chế rất lớn của Ipv4. Để đánh địa chỉ, phiên bản Ipv4 chỉ sử dụng 32bit, do đó không gian của nó chỉ có khoảng 236 địa chỉ. Sự bùng nổ Internet đến thời điểm hiện tại khiến cho tài nguyên Ipv4 được sử dụng gần như là cạn kiện. Vì thế phiên bản này không đủ đáp ứng so với nhu cầu hiện nay. 
