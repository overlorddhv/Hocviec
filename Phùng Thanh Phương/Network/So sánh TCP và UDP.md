# 1. TCP (Transmission Control Protocol)

**1.1. Khái niệm**

TCP là giao thức truyền tải hướng kết nối (connection-oriented), nghĩa là phải thực hiện thiết lập kết nối với đầu xa trước khi thực hiện truyền dữ liệu. Tiến trình thiết lập kết nối ở TCP được gọi là tiến trình bắt tay 3 bước (threeway handshake).

Cung cấp cơ chế báo nhận (Acknowledgement) :Khi A gửi dữ liệu cho B, B nhận được thì gửi gói tin cho A xác nhận là đã nhận. Nếu không nhận được tin xác nhận thì A sẽ gửi cho đến khi B báo nhận thì thôi.

Cung cấp cơ chế đánh số thứ tự gói tin (sequencing) cho các đơn vị dữ liệu được truyền, sử dụng để ráp các gói tin chính xác ở điểm nhận và loại bỏ gói tin trùng lặp.

Có các cơ chế điều khiển luồng thích hợp (flow control) để tránh nghẽn xảy ra.

Hỗ trợ cơ chế full-duplex ( truyền và nhận dữ liệu cùng một lúc)

Phục hồi dữ liệu bị mất trên đường truyền ( A gửi B mà không thấy xác nhận sẽ gửi lại).

**1.2. Cấu trúc gói tin**

Do là giao thức tin cậy nên cấu trúc gói tin của TCP rất phức tạp

![image](https://user-images.githubusercontent.com/48250210/157802410-08de5b9b-d544-49ff-8065-b8586ae0b936.png)

* Source port và destination port (đều dài 16 bit): được sử dụng để định danh cho session của giao thức nào đó trên lớp ứng dụng đang được truyền tải trong TCP segment đang xét
* Sequence number (32 bit): dùng để đánh số thứ tự gói tin (từ số sequence nó sẽ tính ra được số byte đã được truyền).
* Acknowledge number (32 bit): : dùng để báo đã nhận được gói tin nào và mong nhận được byte mang số thứ tự nào tiếp theo.
* Header length (4 bit): cho biết toàn bộ header dài bao nhiêu tính theo đơn vị word(1 Word = 4 byte).
* Các bit reserverd (4 bit): đều được thiết lập bằng 0
* Các bit control (9 bit): các bit dùng để điều khiển cờ (flag) ACK, cờ Sequence ...
* Window size (16 bit): số lượng byte được thiết bị sẵn sàng tiếp nhận
* Checksum (16 bit): kiểm tra lỗi của toàn bộ TCP segment
* Urgent pointer (16 bit): sử dụng trong trường hợp cần ưu tiên dữ liệu
* Options (tối đa 32 bit): cho phép thêm vào TCP các tính năng khác
* Data: dữ liệu của lớp trên
