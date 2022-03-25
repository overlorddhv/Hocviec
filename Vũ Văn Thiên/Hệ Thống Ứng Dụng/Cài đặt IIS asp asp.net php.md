# Cài đặt IIS trên Windows Server 2019

1. Chạy Powershell với quyền admin và cài đặt IIS.

![image](https://user-images.githubusercontent.com/62273292/158933745-3b19dfdf-94a3-4174-b40f-6eed4250731f.png)


2. Chạy Server Manager và nhấp vào Add roles and features.

![image](https://user-images.githubusercontent.com/62273292/158933760-7b52d094-f73e-464c-af9a-93107c241686.png)


3. Nhấp vào nút Next.

![image](https://user-images.githubusercontent.com/62273292/158933777-34fe646e-274a-4640-807b-611b3d3d9235.png)


4. Chọn Role-based or feature-based installation.

![image](https://user-images.githubusercontent.com/62273292/158933795-c6c6476e-a6ef-4034-904a-4cdd840f8281.png)


5. Chọn host bạn muốn thêm các service.

![image](https://user-images.githubusercontent.com/62273292/158933808-a83ec4dc-b843-4b4f-a963-951d2cb9a999.png)


6. Tích vào hộp Web Server (IIS).

![image](https://user-images.githubusercontent.com/62273292/158933833-bf5a1e9a-6bc9-41a6-b29d-ca47a10f6c28.png)


7. Các tính năng bổ sung được yêu cầu để thêm IIS Server. Nhấp vào nút Add Features > Next.

![image](https://user-images.githubusercontent.com/62273292/158933855-04a5e530-933d-4c42-a5e3-2bfbd5d83424.png)


8. Nhấp vào nút Next.

![image](https://user-images.githubusercontent.com/62273292/158933873-e5cb9915-a818-46ce-9e5b-18a4d72b2103.png)


9. Nhấp vào nút Next.

![image](https://user-images.githubusercontent.com/62273292/158933884-88f0f708-ec0e-41c0-b4a4-b847ad825498.png)


10. Đây là phần chọn các tính năng của Web Server. Hãy chọn những tính năng mà bạn muốn thêm. Trong ví dụ này, các tùy chọn mặc định được giữ nguyên. Tất nhiên, bạn có thể thêm các tính năng này sau khi cài đặt IIS.

![image](https://user-images.githubusercontent.com/62273292/158933903-289fa707-e06c-4f25-b009-3567a755ab81.png)


11. Nhấp vào nút Install.

![image](https://user-images.githubusercontent.com/62273292/158933920-c5b6dbf5-5a4d-4068-be25-4d54142c3dbc.png)


12. Sau khi kết thúc cài đặt, nhấp vào nút Close.

![image](https://user-images.githubusercontent.com/62273292/158933941-7c655fd2-637d-450f-94f1-e72ea2d68b3d.png)


13. Chạy trình duyệt web và truy cập vào localhost, sau đó bạn có thể xác minh IIS có đang chạy bình thường không.

![image](https://user-images.githubusercontent.com/62273292/158933959-6bf3577b-d982-4dab-8f8d-7ca764d4b1bb.png)





# IIS với ASP Classic và ASP.net

![image](https://user-images.githubusercontent.com/62273292/160034648-6a5993a1-62f5-46a4-890a-750419c8b98d.png)

Chuột phải vào Site-> Add Website

![image](https://user-images.githubusercontent.com/62273292/160034679-aff86192-ab91-4b7d-bbf4-97ec415fc31c.png)


 Tiến hành cấu hình:
 
 Đặt tên site name, chọn đến Application Pool, ở đây mình chọn .NET v4.5, sau đó OK
(Ở đây các bạn có thể tạo Application pool, hướng dẫn tạo Application pool tại đây)

![image](https://user-images.githubusercontent.com/62273292/160034722-897dafef-60d9-45af-9354-b361274331ca.png)


Tiếp đến Physical Path: chọn đến đường dẫn thư mục có chứa file web config

Sau đó chọn Connect as => Specific user => Set tài khoản Microsoft bạn đang sử dụng trên máy, điền Username & Password => OK

![image](https://user-images.githubusercontent.com/62273292/160034768-435991d9-f666-422e-8a1d-fd52f5275c6c.png)

 Tiếp đến ô IP Address gõ đúng cái địa chỉ IP của localhost (ở đây là 127.0.0.1), Port 80 là mặc định, Host name: tùy ý. Sau đó nhấn OK
 
 ![image](https://user-images.githubusercontent.com/62273292/160034785-9ff6b55f-98ea-4c34-9af6-87c7658b4a47.png)


 Lúc này đã tạo thành công Site
 
 ![image](https://user-images.githubusercontent.com/62273292/160034819-73df15ee-51f4-4117-b089-db630f051c9b.png)


Lúc này vẫn chưa chạy được, chúng ta phải tiến hành chỉnh sửa file host:

Vào đường dẫn: C:\Windows\System32\drivers\etc, mở file hosts lên và làm như sau: Thêm dòng bôi vàng trong hình vào 127.0.0.1 test.lv.com (127.0.0.1: IP localhost, test.lv.com: Host name chúng ta đã thêm trong quá trình tạo Site), Lưu lại là OK

![image](https://user-images.githubusercontent.com/62273292/160034878-8530b6b6-8e95-4bcd-97cd-750298de8559.png)


 Mở trình duyệt gõ Host name chúng ta đã tạo, thì sẽ chạy được project Web của chùng ta mà không cần mở code lên chạy thủ công nữa.
 
 ![image](https://user-images.githubusercontent.com/62273292/160034915-e61a40ef-43df-4628-8225-6dcc91c43609.png)







## Hoàn Tất

![image](https://user-images.githubusercontent.com/62273292/160034951-2ffd19c5-d017-4836-81e4-66e05cf26c96.png)

## ASP 

![image](https://user-images.githubusercontent.com/62273292/160043972-b70a311e-0fb0-4c33-946f-c90fca9b7038.png)

![image](https://user-images.githubusercontent.com/62273292/160044043-30564283-1362-4e7f-b014-d5aacd7cb7c9.png)

## ASP.NET

![image](https://user-images.githubusercontent.com/62273292/160035053-33f1b508-5fd6-4edc-9f12-43b530e0764e.png)


![image](https://user-images.githubusercontent.com/62273292/160035083-44b7bb5a-b0ae-4f63-9966-500953db8d0e.png)







# IIS với php

Cài đặt PHP Manager

PHP Manager được sử dụng để quản lý các phiên bản PHP trên hệ thống, cũng như đơn giản hoá việc sử dụng PHP. Khi sử dụng PHP manager, chỉ cần vài thao tác chuột là đã có thể add thêm 1 phiên bản PHP sử dụng cũng như tuỳ biến các extension PHP.

Để cài đặt PHP Manager, trước hết cần cài đặt Dotnet 3.5

Tại Server Manager > Features > Add Features

![image](https://user-images.githubusercontent.com/62273292/160040625-37aaf410-71f8-4015-8cad-8e225be5ada7.png)


Chọn Dotnet FrameworkFramework 3.5.1 Features > Next

![image](https://user-images.githubusercontent.com/62273292/160040647-805c75c8-a457-44c2-943e-8986a54192d9.png)


Chọn Install và chờ hệ thống cài đặt hoàn tất

![image](https://user-images.githubusercontent.com/62273292/160040664-3b08f337-80a5-4ace-b8a5-5c04ee2c7ab0.png)


Tiến hành cài đặt PHP Manager theo các bước hướng dẫn của phần mềm.

Sau khi cài đặt xong PHP Manager, tiến hành khởi động lại hệ thống VPS/Server

Sau khi hệ thống đã khởi động lại, truy cập vào IIS và kiểm tra trạng thái của PHP Manager

![image](https://user-images.githubusercontent.com/62273292/160040709-f53a734b-17c4-4bb2-bedb-e4bd65a86812.png)


PHP Manager đã được cài đặt hoàn tất

![image](https://user-images.githubusercontent.com/62273292/160040729-66f616f9-056d-4825-ab29-3063b6aec528.png)


Truy cập vào PHP Manager và chọn Register New PHP version

![image](https://user-images.githubusercontent.com/62273292/160040753-82583cf7-8d37-4eba-b060-42f752441272.png)


Chọn tới file php-cgi.exe trong thư mục php56 vừa giải nén

![image](https://user-images.githubusercontent.com/62273292/160040772-f52602df-a448-4243-a235-c5352631344a.png)


Chọn OK

![image](https://user-images.githubusercontent.com/62273292/160040779-3bd1003e-bd33-4fa8-9bfd-9242e84a4838.png)


Như vậy ta đã add thành công PHP 5.6 vào IIS, trong trường hợp muốn add các phiên bản khác, chỉ cần lặp lại các thao tác add PHP như trên (Lưu ý: Cài đặt thêm Visual C++ theo yêu cầu của mỗi bản PHP).

![image](https://user-images.githubusercontent.com/62273292/160040801-5fe5688f-6e43-4171-a5b5-c549fd603c61.png)


Restart lại IIS

![image](https://user-images.githubusercontent.com/62273292/160040821-90e6e46b-6bc9-420e-9fef-0f9b06b127b8.png)


Tiến hành Kiểm tra phiên bản PHP đã được hoạt động chưa bằng cách vào PHP Manager > Check phpinfo()

![image](https://user-images.githubusercontent.com/62273292/160040843-1a78ee47-da32-4a48-9ed2-bc701046a79d.png)


Chọn Site là Url để test, ví dụ:

![image](https://user-images.githubusercontent.com/62273292/160040861-a2dfa6cd-f16c-4951-a9cd-110bc8f5b457.png)


Như vậy PHP đã được cài đặt hoàn tất

## KẾT QUẢ


![image](https://user-images.githubusercontent.com/62273292/160040927-7986c53b-1de2-41fb-9f5b-f802e169cbac.png)

![image](https://user-images.githubusercontent.com/62273292/160041017-7750a048-dcdf-40c9-a9c7-9c0d49d1bf3f.png)

![image](https://user-images.githubusercontent.com/62273292/160041065-842e173c-66cf-4f8e-acc0-5ca916029cb3.png)







