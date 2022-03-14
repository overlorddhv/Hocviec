# Hướng dẫn cài đặt IIS lên window server

Theo Microsoft, Web Server (IIS) trong Windows Server 2019 cung cấp một nền tảng bảo mật, dễ quản lý, theo kiểu mô-đun và có thể mở rộng để lưu trữ các trang web, service và ứng dụng một cách đáng tin cậy. Bản phát hành Windows Server 2019 mới của Microsoft đi kèm với phiên bản IIS 10. Hướng dẫn này sẽ cho biết cách cài đặt cài đặt và sử dụng IIS trên Windows Server 2019.

# Chuẩn bị
**Windows server 2019 (Các bạn có thể tham khảo link cài đặt: )  

1. Sau khi khởi động xong Windows server 2019, các bạn sẽ thấy xuất hiện hộp thoại Server Mânger

Nhấn chọn **Add roles and features**

![image](https://user-images.githubusercontent.com/65167293/158219636-e06a9df6-a3fb-4442-aa3c-abb8e18d8836.png)

2. Nhấn chọn **Next**.

![image](https://user-images.githubusercontent.com/65167293/158219851-0b2ce9a6-e68c-4a87-8a9a-338ffe65c495.png)

3. Chọn **Role-based or feature-based installation**.

![image](https://user-images.githubusercontent.com/65167293/158219935-96aee623-6086-4dfe-b24e-b65a0bac92e0.png)

4. Chọn host bạn muốn thêm các service.

![image](https://user-images.githubusercontent.com/65167293/158220050-da77563f-9b6c-4ab1-9867-ea977c480aad.png)

5. Tích vào hộp **Web Server (IIS)**.

![image](https://user-images.githubusercontent.com/65167293/158220156-d90cb5b4-7691-4c76-809b-7c57e4e6e1b9.png)

6. Các tính năng bổ sung được yêu cầu để thêm IIS Server. Nhấp vào nút **Add Features > Next**.

![image](https://user-images.githubusercontent.com/65167293/158220300-cd972fa9-3099-451a-9f50-d9c3832f5d9b.png)

7. Nhấp vào nút **Next**.

![image](https://user-images.githubusercontent.com/65167293/158220402-d9b1308e-c53d-4bcc-846c-eab85944cfb0.png)

8. Nhấp vào nút **Next**.

![image](https://user-images.githubusercontent.com/65167293/158220521-0468d8cc-2e5f-4434-b012-c5a9a171691d.png)

9. Đây là phần chọn các tính năng của Web Server. Hãy chọn những tính năng mà bạn muốn thêm. Trong ví dụ này, các tùy chọn mặc định được giữ nguyên. Tất nhiên, bạn có thể thêm các tính năng này sau khi cài đặt IIS.

![image](https://user-images.githubusercontent.com/65167293/158220645-94c58ebe-79e1-469f-a8b9-9ad4b63f2df9.png)

10. Nhấp vào nút **Install**.

![image](https://user-images.githubusercontent.com/65167293/158220751-7f3f7923-5f17-4ea6-a339-c8a5377bcc53.png)

11. Sau khi kết thúc cài đặt, nhấp vào nút **Close**.

![image](https://user-images.githubusercontent.com/65167293/158220837-49db8cd7-36ae-4191-90ac-05bc13f7085b.png)

12. Chạy trình duyệt web và truy cập vào **localhost**, sau đó bạn có thể xác minh IIS có đang chạy bình thường không.

 ![image](https://user-images.githubusercontent.com/65167293/158221691-dada598d-96e6-40d9-8b7e-eb76572d4801.png)

13. Truy cập theo đường link này để mở file hosts

![sửa file host](https://user-images.githubusercontent.com/65167293/158224572-07009409-2f15-4d2e-b868-b036ed79931c.png)

14. Sửa file hosts như hình dưới

![sửa file host 2](https://user-images.githubusercontent.com/65167293/158224729-f701817f-8b07-4378-94a2-3ac2fc1875c3.png)

15. Tạo file index.html với nội dung *"Hello windows"* theo đường dẫn như hình dưới

![thêm file html hello windows](https://user-images.githubusercontent.com/65167293/158225068-be423733-78e1-4dd3-96bc-ec552b92663b.png)


# Sử dụng IIS trên Windows Server 2019

1. Chạy Powershell với quyền admin và cấu hình như sau:

        Windows PowerShell
        Copyright (C) Microsoft Corporation. All rights reserved.

        # show Sites list : [Default Web Site] is only set
        PS C:\Users\Administrator> Get-Website 

        Name             ID   State      Physical Path                  Bindings
        ----             --   -----      -------------                  --------
        Default Web Site 1    Started    %SystemDrive%\inetpub\wwwroot  http *:80:

        # [Physical Path] is the Document Root
        PS C:\Users\Administrator> Get-ChildItem C:\inetpub\wwwroot 

            Directory: C:\inetpub\wwwroot

        Mode                LastWriteTime         Length Name
        ----                -------------         ------ ----
        -a----        8/27/2019   6:57 PM            703 iisstart.htm
        -a----        8/27/2019   6:57 PM          99710 iisstart.png

        # verify accesses : [iisstart.htm] responds
        PS C:\Users\Administrator> Invoke-WebRequest localhost 

        StatusCode        : 200
        StatusDescription : OK
        Content           : <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
        .....
        .....
        ParsedHtml        : System.__ComObject
        RawContentLength  : 703

        # confirm default documents
        PS C:\Users\Administrator> Get-WebConfigurationProperty -Filter "//defaultDocument/files/add" -PSPath "IIS:\Sites\Default Web Site" -Name "value" | select value 

        Value
        -----
        Default.htm
        Default.asp
        index.htm
        index.html
        iisstart.htm

        # create a test page under the Document Root and verify working
        # [Write-Output] generates with UTF-16, so specify encoding explicitly with [Out-File]
        PS C:\Users\Administrator> Write-Output "IIS Default Start Page" | Out-File C:\inetpub\wwwroot\Default.htm -Encoding Default 

        # verify accesses
        # for [curl.exe], specify extension ⇒ if not specify extension, [curl] is an Alias from [Invoke-WebRequest]
        PS C:\Users\Administrator> curl.exe localhost 
        IIS Default Start Page
 
  
 2. Chạy **Start** > **Server Manager** và nhấp vào **Tools** > **Internet Information Services (IIS) Manager**.

![image](https://user-images.githubusercontent.com/65167293/158222523-da369bf6-1710-4d66-a2ac-d4f081b3c20b.png)

3. Mở các mục ở bảng điều khiển bên trái, **Default Web Site** được cấu hình.

![image](https://user-images.githubusercontent.com/65167293/158222627-84215613-c1c3-4a55-9b58-796d0d82cbc7.png)

4. Tạo file 123web.com như hình mô tả

![3](https://user-images.githubusercontent.com/65167293/158223242-c9a961a5-ff30-447e-bfc6-e244c37c07e5.png)

5. Bấm chọn **WIN-FF485GJMCR6** rồi sau đó nhấn **restart**

![4](https://user-images.githubusercontent.com/65167293/158223523-f76ce676-2d7e-4d79-8f4f-ed86b901be34.png)

6. Chọn vào **123web.com** vừa mới tạo được vào sau đó nhấn **Browse 123web,com**

Như vậy các bạn đã thực hiện xong việc cài đặt 

