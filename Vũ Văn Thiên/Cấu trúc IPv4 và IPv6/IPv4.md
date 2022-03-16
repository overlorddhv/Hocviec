# Cấu trúc phân loại cách chia địa chỉ IPv4

## Địa chỉ Ipv4 là gì?

Ipv4 viết tắt cho Internet Protocol Version 4, dịch ra có nghĩa là giao thức Internet phiên bản thứ 4. Ipv4 đã được bộ quốc phòng Hoa Kỳ chuẩn hóa trong bản MIL-STD-1777. Giao thức Internet IP đã trải qua nhiều phiên bản khác nhau và phiên bản Ipv4 là phiên bản đầu tiên được sử dụng rộng rãi trên toàn thế giới và hiện vẫn còn đang là nòng cốt của Internet trên toàn thế giới.

Ipv4 là giao thức mang tính hướng dữ liệu và được sử dụng cho hệ thống chuyển mạch gói. Ipv4 không quan tâm đến thứ tự truyền gói tin, cũng không đảm bảo gói tin sẽ đến đích hay là có xảy ra tình trạng lặp gói tin ở đích đến hay không. Nó chỉ có cơ chế đảm bảo tính toàn vẹn dữ liệu bằng việc sử dụng những gói kiểm tra được thiết lập đi kèm với nó.

Địa chỉ Ipv4 là 1 địa chỉ đơn nhất đang được sử dụng bởi các thiết bị điện tử hiện nay để nhận diện và liên lạc với nhau trên Internet. Để đánh địa chỉ, Ipv4 sử dụng 32bit và chia ra làm 4 octet (mỗi octet có 8 bit = 1 byte). Dấu chấm được sử dụng để ngăn các octet với nhau.

Để hiểu địa chỉ Ipv4 là gì có thể lấy ví dụ như sau: Giả sử ta có 1 dải số như sau: 172.16.254.1. Dải số này có thể được dùng để đặt tên cho 1 địa chỉ Ipv4 nào đó. Có thể thấy địa chỉ Ipv4 có tổng cộng 4 số và mỗi số phải nằm trong giới hạn từ 0-255. Xem hình minh họa.

![image](https://user-images.githubusercontent.com/62273292/158498718-19dd6fcd-9d8c-4a06-b302-3ad549d98124.png)

Các loại địa chỉ Ipv4: unicast, broadcast, multicast. Trong đó unicast là địa chỉ IP cho phép thiết bị gửi dữ liệu đến 1 nơi nhận duy nhất. Địa chỉ IP broadcast lại cho phép gửi dữ liệu đến các host trong 1 mạng con. Còn địa chỉ IP multicast cho phép thiết bị gửi dữ liệu đến 1 tập xác định trước các host.

## Địa chỉ Ipv4 có bao nhiêu lớp?

Ban đầu, 1 địa chỉ Ipv4 được chia ra làm 2 phần là địa chỉ của mạng (Network ID) và địa chỉ của máy (Host ID). Địa chỉ của mạng (Network ID) được xác lập bởi octet đầu tiên và địa chỉ của máy (Host ID) được xác lập cho 3 octet còn lại. Với cách chia này thì địa chỉ của network bị giới hạn ở con số 256. Đây là con số quá ít so với nhu cầu sử dụng thực tế. Vì vậy người ta đã định nghĩa phân lớp mạng để vượt qua giới hạn này và tập hợp thành 1 lớp mạng đầy đủ còn được gọi là classful.

Địa chỉ IP được phân ra thành 5 lớp khác nhau: lớp A, lớp B, lớp C, lớp D,lớp E. Với cách phân loại này sẽ tạo được vô số địa chỉ IPv4 khác nhau. Đặc điểm của các lớp IPv4 này là gì? Hãy cùng tìm hiểu tiếp nhé.



## Lớp A

