# Tìm hiểu về Process (tiến trình) trong linux

## Process là gì?

Process (tiến trình) là trạng thái tức thời của một chương trình đang chạy trên máy tính. Nó bao gồm bộ nhớ cần thiết để chạy chương trình (không gian địa chỉ của quá trình) và khả năng kiểm soát hiện trạng của bộ xử lý trong quá trình thực thi chương trình (tiến trình điều khiển của quá trình)

## Một process hoạt động thế nào?

Khi hệ thống khởi động, kernel sẽ khởi tạo một vài hành vi của riêng nó dưới một process và khởi động một chương trình gọi là `init`. `init` theo đó sẽ khởi chạy một loạt các shell script (nằm ở /`etc`) được gọi là init script, sẽ khởi động tất cả các service hệ thống.

Rất nhiều service này được implement dưới dạng daemon program, chương trình chạy background mà không can thiệp tới giao diện người dùng. Vì thế kể cả khi chúng ta không đăng nhập thì hệ thống cũng ở trạng thái busy một lúc để khởi chạy

Chương trình có thể khởi chạy một chương trình khác được diễn giải trong cơ chế process gọi là process cha sinh ra process con.

Kernel sẽ duy trì thông tin về mỗi một process. Ví dụ: mỗi process được gán cho một giá trị là PID (process ID). PID được gán theo thứ tự tăng dần và init luôn có PID là 1. Kernel cũng theo dõi thông tin bộ nhớ gán cho mỗi process, cũng như tính sẵn sàng của process để có thể tiếp tục thực thi.

Cũng như file thì process cũng có owner và user ID, ...

## Theo dõi process

Câu lệnh phổ biến để theo dõi các process là `ps`. `ps` có rất nhiều tùy chọn, cách dùng cơ bản nhất là:


```
➜  ~ ps
  PID TTY          TIME CMD
 4486 pts/1    00:00:00 zsh
 4845 pts/1    00:00:00 ps
```

![image](https://user-images.githubusercontent.com/62273292/159156013-716db6e9-cecc-4577-b26d-ecdb681aa6d1.png)


Chúng ta có thể thấy là mặc định thì `ps` sẽ không show quá nhiều thông tin, chỉ show thông tin của terminal session hiện tại.

Kết quả list ra 2 processes cùng với thông tin PID.

TTY là viết tắt của teletype, để chỉ terminal đang chạy process đó.

TIME đế chỉ thời gian chiếm CPU của process tương ứng.

Với thêm options x, chúng ta sẽ nhìn thấy tất cả các tiến trình bất kể terminal nào

![image](https://user-images.githubusercontent.com/62273292/159156141-2b9c1a3d-24b2-4a1d-b61d-42e82147f722.png)


Chúng ta có thể thấy cột STAT mới xuất hiện, viết tắt của state để chỉ trạng thái của process tương ứng, chúng ta có các dạng state sau:

![image](https://user-images.githubusercontent.com/62273292/159156188-f0fa45fb-dcea-4d01-92ea-96e9b7b2f16a.png)


Một set option phổ biến khác là `aux`

![image](https://user-images.githubusercontent.com/62273292/159156273-13dfc887-2a71-494c-a95c-4fbed56b4a42.png)

Khi chạy ps với option này sẽ hiển thị process thuộc về mọi user.

Theo dõi process với `top`

![image](https://user-images.githubusercontent.com/62273292/159156451-0e3e5d1d-650f-46f7-bd1d-cc7917f2e0a9.png)


Sau đây là bảng giải thích ý nghĩa output của lệnh `top`:

|Dòng|Trường|Ý nghĩa|
|--|--|--|
|1|top|tên của chương trình|
||21:55:13|thời gian hiện tại|
||up 6:30|	uptime. Thời gian hệ thống bắt đầu chạy|
||1 users|Có 1 user đã log in|
||load average:|Chỉ ra con số ở trạng thái có thể chạy và đang share CPU. Giá trị dưới 1.0 chỉ ra là hệ thống đang không busy|
|2|Tasks:|Tổng kết số lương process và số lương process theo trạng thái|
|3|	Cpu(s):|Dòng này miêu tả đặc điểm của những tác vụ CPU đang thực thi|
||0,9 us|0,9% CPU đang được dùng cho user process|
||1,0 us|1,0% CPU đang được dùng cho system process|
||0,0 ni|0,0% CPU đang được dùng cho process có độ ưu tiên thấp|
||97,8 id|97,8% của CPU đang nhàn rỗi|
||0,0 wa|	97,8% của CPU đang chờ I/O|
|4|Mem:|Chỉ ra có bao nhiêu RAM đang được dùng|
|5|Swap:|	Chỉ ra có bao nhiêu Swap space đang được dùng|


## Kiểm soát process

Khi chúng ta gõ một lệnh và chạy nó, terminal sẽ ở trạng thái không dùng được cho đến chương trình chạy xong, chắc hẳn chúng ta đã quá quen thuộc với việc sử dụng ctrl-c để kết thúc một chương trình đang được thực thi, trong phần này chúng ta sẽ tìm hiểu về các cách để kiểm soát một process như vây.

Trong phần này chúng ta sẽ lấy ví dụ với chương trình xlogo thực thi một việc đơn giản đó là show ra cửa sổ có hình logo hệ thống. Đặc điểm của chương trình này là nó sẽ chiếm terminal cho đến khi chúng ta tắt cửa sổ logo đó đi.

Vậy làm sao để chạy một chương trình mà nó không chiếm terminal của chúng ta, chúng ta có thể thêm & vào cuối câu lệnh muốn chạy. Việc làm này gọi là chạy background job.

![image](https://user-images.githubusercontent.com/62273292/159156772-08c63610-53ab-4aa5-85ad-356ffa61669c.png)


Sau khi chạy lệnh trên, terminal thông báo cho chúng ta biết là chúng ta đã bắt đầu chạy background job đầu tiên với PID là 52933. Chúng ta có thể kiểm tra lại bằng lệnh ps như trên.

Ngoài ra còn một lệnh khác cũng có thể list các background job đó là `jobs`

![image](https://user-images.githubusercontent.com/62273292/159156833-66a39cb2-f457-43dd-bb41-2b2c41e8b050.png)


Để trả một process đang chạy background về foreground thì chúng ta có thể sử dụng lệnh `fg` là viết tắt của foreground.

![image](https://user-images.githubusercontent.com/62273292/159156863-d8cfb64d-9bca-4235-a845-f740968ebdb2.png)


Chúng ta truyền vào lệnh `fg` số thứ tự của jobs, chương trình sẽ lại chiếm terminal như khi chúng ta chạy nó bình thường.

Để stop một process (khác với terminate process sử dụng ctrl-c) ta sử dụng ctrl-z

![image](https://user-images.githubusercontent.com/62273292/159157020-40670ecb-dc14-4156-a822-905686eee84f.png)


khi đó, đối với xlogo chúng ta không thể resize cửa sổ chương trình được. Để tiếp tục thực thi chương trình, chúng ta có thể sử dụng lệnh fg như trên với tham số là số hiệu của jobs. Hoặc chúng ta cũng có thể sử dụng lệnh bg, tiếp tục chạy chương trình ở background

![image](https://user-images.githubusercontent.com/62273292/159157029-af4e7c09-fc09-4dd8-9a48-84d4f1d2cb09.png)


## Signals

Chúng ta  có thể sử dụng lệnh `kill` để dường process

![image](https://user-images.githubusercontent.com/62273292/159157143-e8ee18bf-c58d-4c8a-8ed9-f50cce02af1a.png)


Thực ra lệnh kill không thực sự kill process mà nó gửi đến process một signal. Signals là cách mà OS giao tiếp với chương trình. Việc chúng ta sử dụng ctrl-c và ctrl-z cũng chính là gửi tín hiệu INT và TSTP đến cho chương trình.

Để gửi signal đến một chương trình, chúng ta có thể sửa dụng lệnh kill kết hợp với số/tên của signal. Sau đây là một số signal phổ biến:

![image](https://user-images.githubusercontent.com/62273292/159157201-a102227b-ac44-4118-8465-9bc396aca700.png)


```
➜  ~ kill -STOP 8525 
[1]  + 8525 suspended (signal)  xlogo                                                                    
➜  ~ kill -CONT 8525
➜  ~ ps
  PID TTY          TIME CMD
 4486 pts/1    00:00:00 zsh
 8525 pts/1    00:00:00 xlogo
 8551 pts/1    00:00:00 ps
➜  ~ kill -INT 8525
[1]  + 8525 interrupt  xlogo
```

Ngoài ra chúng ta có thể chạy lệnh kill -l để list ra các signal khả dụng của hệ thống

```
➜  ~ kill -l
HUP INT QUIT ILL TRAP ABRT BUS FPE KILL USR1 SEGV USR2 PIPE ALRM TERM STKFLT CHLD CONT STOP TSTP TTIN TTOU URG XCPU XFSZ VTALRM PROF WINCH POLL PWR SYS
```

Ngoài ra chúng ta có thể gửi kill signal đến nhiều tiến trình chạy cùng một chương trình bằng cách sử dụng killall

```
➜  ~ xlogo &
[1] 8906
➜  ~ xlogo &
[2] 8914
➜  ~ xlogo &
[3] 8939
➜  ~ ps
  PID TTY          TIME CMD
 4486 pts/1    00:00:00 zsh
 8906 pts/1    00:00:00 xlogo
 8914 pts/1    00:00:00 xlogo
 8939 pts/1    00:00:00 xlogo
 8951 pts/1    00:00:00 ps
➜  ~ killall xlogo
[1]    8906 terminated  xlogo                                                                       
[3]  + 8939 terminated  xlogo
[2]  + 8914 terminated  xlogo
➜  ~ ps
  PID TTY          TIME CMD
 4486 pts/1    00:00:00 zsh
 8962 pts/1    00:00:00 ps
```


















