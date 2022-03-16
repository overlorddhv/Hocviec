# VMware

## VMware là gì?

VMware là phần mềm máy chủ ảo, đây là một môi trường ảo có chức năng như một hệ thống máy tính ảo với CPU, bộ nhớ, mạng và bộ lưu trữ riêng. Chúng được tạo trên một hệ thống phần cứng vật lý. Phần mềm được gọi là hypervisor chia các tài nguyên của máy khỏi phần cứng và cung cấp một cách thích hợp để VM có thể sử dụng.

![image](https://user-images.githubusercontent.com/62273292/158516665-e3f6d9eb-6237-43e6-8f16-b16ad94f2d8f.png)

VMware được phát triển bởi công ty VMware Inc ở California. Phần mềm đầu tiên là phần mềm ảo hóa sau đó đến phần mềm VMWare Workstation ra mắt vào tháng 5 năm 1999. Tiếp đó là các sản phẩm máy chủ VMWare GSX Server và VMWare ESX trên thị trường vào năm 2001.

Các máy chủ vật lý, được trang bị hypervisor như KVM được gọi là host. Nhiều máy ảo sử dụng tài nguyên của nó gọi là guest. Hypervisor xử lý các tài nguyên CPU, RAM và Disk như một nhóm tài nguyên. Có thể dễ dàng được di chuyển giữa các máy ảo hiện có hoặc sang các máy ảo mới.

Các máy ảo được cách ly với phần còn lại của hệ thống và nhiều máy ảo có thể tồn tại trên một phần cứng, như một máy chủ. Chúng có thể được di chuyển giữa các máy chủ lưu trữ. Tùy theo nhu cầu hoặc để sử dụng tài nguyên hiệu quả hơn.

Máy ảo cho phép nhiều hệ điều hành khác nhau chạy đồng thời trên một máy tính. Ví dụ như bản Linux® chạy trên trên máy tính xách tay MacOS. Mỗi hệ điều hành hoạt động giống như cách nó chạy trên một phần cứng máy chủ vật lý.

## VMware hoạt động như thế nào?

Khi máy ảo đang chạy và người dùng hoặc chương trình đưa ra lệnh yêu cầu tài nguyên bổ sung từ môi trường vật lý, hypervisor gửi yêu cầu tới tài nguyên của hệ thống vật lý để hệ điều hành và ứng dụng của máy ảo có thể truy cập nhóm tài nguyên vật lý được chia sẻ.

Máy ảo chạy như một tiến trình trong cửa sổ ứng dụng, tương tự như bất kỳ ứng dụng nào khác, trên hệ điều hành của máy vật lý. Các tệp chính tạo nên một máy ảo bao gồm tệp nhật ký, tệp cài đặt NVRAM, tệp đĩa ảo và tệp cấu hình.

![image](https://user-images.githubusercontent.com/62273292/158517520-d4992e9b-8889-48ad-b8a3-a775b3141986.png)

## Phầm mềm VMware dùng để làm gì?

VMware Workstation là sản phẩm được phát hành bởi công ty VMware. Đây là phần mềm cho phép người dùng tạo và sử dụng máy ảo trực tiếp trên laptop hoặc PC. Ngoài việc cài đặt nhiều phiên bản điều hành khác nhau mà còn có thể dễ dàng chuyển đổi máy ảo cùng một lúc.

![image](https://user-images.githubusercontent.com/62273292/158517592-4d34d2f7-195d-4608-9f5a-39052654c1cc.png)


Ngoài ra, VMWare Workstation còn được xem là cầu nối giữa máy chủ và máy ảo cho tất cả các tài nguyên phần cứng. Tất cả các trình điều khiển thiết bị hiện nay được cài đặt thông qua máy chủ.

VMware Server là phần mềm ảo hóa máy chủ miễn phí. Cho phép sử dụng nhiều máy ảo trên cùng một máy chủ vật lý. VMware Server cũng tương thích với Windows, Linux, Solaris,…

VMware vSpere là bộ sản phẩm ảo hóa máy chủ của VMware bảo gồm phần mềm quản lý ESXi hypervisor và vCenter. Hiện nay, sản phẩm đã có những sự phát triển mạnh và được tích hợp thêm nhiều tính năng mới.

## Lợi ích khi sử dụng VMware

Phần mềm ảo hóa có thể giải quyết được các tính huống cấp bách về mảng CNTT, từ đó giảm được các chi phí bảo trì khi mở rộng hoặc nâng cấp cơ sở hạ tầng. Những lợi ích tiêu biểu khi sử dụng VMware như:

- Giảm nguy cơ mấy dữ liệu, nhiều tùy chọn sao lưu và bảo mật dữ liệu.
- Tăng tính linh hoạt của hệ thống trung tâm dữ liệu.
- Giảm chi phí vận hành.
- Loại bỏ hoặc hạn chế được các công việc hành chính cho các nhân viên IT.

## Các loại hypervisors của VMware?

Có 2 loại hypervisors khác nhau có thể được sử dụng để ảo hóa.

**Loại 1**

 Hypervisor loại 1 là trên bare metal. Tài nguyên VM được lên lịch trực tiếp tới phần cứng bởi hypervisor. KVM là một ví dụ về hypervisor loại 1. KVM đã được hợp nhất vào Linux Kernel vào năm 2007. Vì vậy nếu bạn đang sử dụng phiên bản Linux hiện đại, bạn đã có quyền truy cập vào KVM.
 
**Loại 2 **

Hypervisor loại 2 là Host – Tài nguyên VMware được lập lịch dựa trên hệ điều hành chủ, sau đó được thực thi dựa trên phần cứng. VMware Workstation và Oracle VirtualBox là những ví dụ về Hypervisor loại 2

## Ưu điểm khi dùng máy ảo Vmware

Máy ảo dễ quản lý và bảo trì, đồng thời chúng mang lại một số lợi thế so với máy vật lý:

  - Máy ảo có thể chạy nhiều môi trường hệ điều hành trên một máy tính vật lý duy nhất, tiết kiệm không gian vật lý, thời gian và chi phí quản lý.
  - Máy ảo hỗ trợ các ứng dụng cũ, giảm chi phí chuyển sang hệ điều hành mới. Ví dụ: một máy ảo Linux chạy bản phân phối Linux làm hệ điều hành khách có thể tồn tại trên máy chủ lưu trữ đang chạy hệ điều hành không phải Linux, chẳng hạn như Windows.
  - Máy ảo cũng có thể cung cấp khả năng khôi phục ổ đĩa tích hợp và các tùy chọn cung cấp ứng dụng.

## Nhược điểm khi dùng máy ảo Vmware

Mặc dù máy ảo có một số lợi thế so với máy vật lý, nhưng cũng có một số nhược điểm tiềm ẩn:

  - Chạy nhiều máy ảo trên một máy vật lý có thể dẫn đến hiệu suất không ổn định nếu các yêu cầu về cơ sở hạ tầng không được đáp ứng.
  - Máy ảo kém hiệu quả hơn và chạy chậm hơn một  máy tính vật lý đầy đủ. Hầu hết các doanh nghiệp sử dụng kết hợp cơ sở hạ tầng vật lý và cơ sở hạ tầng ảo để cân bằng các ưu và nhược điểm tương ứng.

## Các tính năng của máy ảo VMware

Máy ảo (VM) cho phép một doanh nghiệp chạy hệ điều hành hoạt động như một máy tính hoàn toàn riêng biệt trong cửa sổ ứng dụng trên máy tính để bàn. Máy ảo có thể được triển khai để đáp ứng các nhu cầu về năng lượng xử lý ở các mức độ khác nhau, để chạy phần mềm yêu cầu hệ điều hành khác hoặc để kiểm tra các ứng dụng trong môi trường an toàn.


![image](https://user-images.githubusercontent.com/62273292/158519041-39faef5e-7221-4684-b4d1-297b745d5023.png)


Máy ảo đã từng được sử dụng để ảo hóa máy chủ, cho phép các nhóm CNTT hợp nhất tài nguyên máy tính của họ và nâng cao hiệu quả. Ngoài ra, máy ảo có thể thực hiện các tác vụ cụ thể được coi là quá rủi ro để thực hiện trong môi trường máy chủ, chẳng hạn như truy cập dữ liệu bị nhiễm vi-rút hoặc kiểm tra hệ điều hành. Vì máy ảo được tách biệt với phần còn lại của hệ thống nên phần mềm bên trong máy ảo không thể giả mạo máy tính chủ.

## Có những loại máy ảo VMware nào

Người dùng có thể chọn từ hai loại máy ảo khác nhau – máy ảo quy trình và máy ảo hệ thống:

Máy ảo quy trình cho phép một quy trình duy nhất chạy như một ứng dụng trên máy chủ, cung cấp một môi trường lập trình độc lập với nền tảng bằng cách che thông tin của phần cứng hoặc hệ điều hành cơ bản. Một ví dụ về máy ảo quy trình là Máy ảo Java, cho phép bất kỳ hệ điều hành nào chạy các ứng dụng Java như thể chúng có nguồn gốc từ hệ thống đó.

![image](https://user-images.githubusercontent.com/62273292/158519731-03975925-1a03-44bd-a271-6954f3197469.png)


Một máy ảo hệ thống được ảo hóa hoàn toàn để thay thế cho một máy vật lý. Nền tảng hệ thống hỗ trợ việc chia sẻ tài nguyên vật lý của máy tính chủ giữa nhiều máy ảo, mỗi máy chạy bản sao hệ điều hành của riêng nó. Quá trình ảo hóa này dựa vào một hypervisor, có thể chạy trên phần cứng trống, chẳng hạn như VMware ESXi hoặc trên một hệ điều hành.





