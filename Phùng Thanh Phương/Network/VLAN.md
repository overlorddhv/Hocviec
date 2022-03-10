**1. VLAN là gì?**

VLAN là viết tắt của Virtual Local Area Network hoặc Virtual LAN, có nghĩa là Mạng cục bộ ảo” hoặc “Mạng LAN ảo”. VLAN là một mạng tùy chỉnh được tạo từ một hoặc nhiều mạng LAN hiện có. Nó cho phép các nhóm thiết bị từ nhiều mạng (cả có dây và không dây ) được kết hợp thành một mạng logic duy nhất. Kết quả là một mạng LAN ảo có thể được quản lý giống như một mạng cục bộ vật lý. Việc tạo lập nhiều mạng LAN ảo trong cùng một mạng cục bộ ( giữa các khoa trong một trường học, giữa các cục trong một công ty,...) giúp giảm thiểu vùng quảng bá (broadcast domain) cũng như tạo thuận lợi cho việc quản lý một mạng cục bộ rộng lớn.

Với mạng LAN thông thường, các máy tính trong cùng một địa điểm (cùng phòng,..) có thể được kết nối với nhau thành một mạng LAN., chỉ sử dụng một thiết bị tập trung như hub hay switch. Có nhiều mạng LAN khác nhau cần rất nhiều bộ hub, swtich. Tuy nhiên thực tế số lượng máy tính trong một LAN thường không nhiều, ngoài ra nhiều máy tính cùng một địa điểm (cùng phòng) có thể thuộc nhiều LAN khác nhau vì vậy càng tốn nhiều bộ hub, switch khác nhau. Do đó vừa tốn tài nguyên số lượng hub, switch và lãng phí số lượng port Ethernet.

Với nhu cầu tiết kiệm tài nguyên đồng thời đáp ứng nhu cầu sử dụng nhiều LAN trong cùng một địa điểm, giải pháp đưa ra là nhóm các máy tính thuộc các LAN khác nhau vào cùng một bộ tập trung switch. Giải pháp này gọi là mạng LAN ảo hay VLAN.

![image](https://user-images.githubusercontent.com/48250210/157635234-009f04a5-1d14-4d94-8084-f55beb043638.png)
