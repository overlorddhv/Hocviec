# Cài đặt centos 7 trên VMware

## Cài Đặt centos 7

Sau khi cài đặt VMware xong chúng ta tiến hành cài đặt centos 7 như sau:

Bước 1: Khởi động máy ảo VMware > File > New Virtual Machine.

![image](https://user-images.githubusercontent.com/62273292/158609712-bdd9d99c-e1c2-4933-ba55-ca9751365faf.png)

Bước 2: Chọn Custom > Next.

![image](https://user-images.githubusercontent.com/62273292/158609812-8821a362-17af-4539-b941-f7aa42fb387f.png)

Bước 3:  check vào ô I will install the operating system later. > Next

![image](https://user-images.githubusercontent.com/62273292/158609886-8ae0894a-aac2-4818-970b-1666a94c1170.png)

Bước 4:  Chọn Linux > Version: Centos 7 64-bit (ở đây, máy của mình là 64bit nên mình sẽ chọn là centos 7 64-bit).

![image](https://user-images.githubusercontent.com/62273292/158609937-5da44557-46f8-4399-97d5-b5758e65659d.png)

Bước 5:  Đặt tên và chọn nơi lưu file (đây là file đĩa ảo, file này khá nặng nên lưu ở ổ đĩa nào còn trống nhiều dung lượng để tránh gặp lỗi khi cài đặt).

![image](https://user-images.githubusercontent.com/62273292/158609970-2bacd1a9-5fd9-4d3f-9c26-ad51f5c872e7.png)

Bước 6: Chọn tốc độ xử lý của máy ảo.

![image](https://user-images.githubusercontent.com/62273292/158610048-d0ba907f-4711-4077-ac67-399a7b80875d.png)

Bước 7: Chọn RAM,  nếu ram bạn nhiều thì có thể để lên cao hơn nữa.

![image](https://user-images.githubusercontent.com/62273292/158610111-999dc4f2-cc2d-43a8-973d-f97c3a5c220e.png)

Bước 8: Thiết lập card mạng cho máy ảo ( bạn có thể chọn card nat hoặc bried)

![image](https://user-images.githubusercontent.com/62273292/158610179-83a13a91-5ed2-4cfb-8468-8a29fbd8b0e9.png)

Bước 9:  Thiết lập chế độ nhập xuất

![image](https://user-images.githubusercontent.com/62273292/158610227-594ea79a-9409-4062-8921-3780da9ca91f.png)

Bước 10: tiếp click Next

![image](https://user-images.githubusercontent.com/62273292/158610266-e8b04e76-fe24-4c1d-ad0d-9e716089e843.png)

Bước 11:  Tạo một ổ đĩa ảo mới. Chọn Create a new virtual disk > Next

![image](https://user-images.githubusercontent.com/62273292/158610308-e5d3c5bf-715f-4158-8dae-c3333dd4c449.png)

Bước 12: Chọn dung lượng cho ổ đĩa đó, mình để mặc định là 40GB. NHỚ CHỌN Store virtual disk as a single file

![image](https://user-images.githubusercontent.com/62273292/158610350-897a3530-5453-4982-9402-373452adf84d.png)


Bước 13: Chọn đường dẫn lưu file ổ đĩa ảo, sau này có thể copy và chuyển qua máy tính khác mã vẫn dùng được máy ảo.

![image](https://user-images.githubusercontent.com/62273292/158610396-e8f7fe37-6a56-42ac-a61b-a4946e292a7f.png)


Bước 14: Chọn Customize Hardware để kiếm tra lại các thiếp lập.

![image](https://user-images.githubusercontent.com/62273292/158610450-267f04bd-2712-424d-bab3-e193f7149fda.png)


Bước 15:  New CD/DVD  (IDE) > Use ISO image file và chọn đến đường dẫn file ISO centos 7 đã tải về ở trên. Sau đó ấn Close.

![image](https://user-images.githubusercontent.com/62273292/158610506-aa74df6d-9a3c-4a18-ae6c-d8a0f0742f96.png)


Bước 16: Chọn Finish

![image](https://user-images.githubusercontent.com/62273292/158610560-1ac92039-130a-4027-8d97-59e39bdec680.png)


Bước 17: Khởi động centos bằng Power on this virtual machine

![image](https://user-images.githubusercontent.com/62273292/158610590-2323c4b5-3406-410f-aa24-634d5cdc80cc.png)


Bước 18: Chọn Install centos 7

![image](https://user-images.githubusercontent.com/62273292/158610790-ccc5202a-dbd5-4afe-b6c7-ce085a4b1ea6.png)

Bước 19: Thiết lập ngôn ngữ > Continue (english khuyến cáo).

![image](https://user-images.githubusercontent.com/62273292/158610836-67345321-5733-4433-8201-ee167ab1940a.png)

Bước 20: Thiết lập ngày, giờ. DATE & TIME > Done (set giờ việt nam nhé, cứ trỏ chuột vào bản đồ việt nam)

![image](https://user-images.githubusercontent.com/62273292/158610892-d0878df0-ca92-4007-be06-d2ff9307dfc4.png)

Bước 21: Ở mục SOFTWATE SELECTION, chọn giao diện đồ hoạ (GUI) để dễ dàng thao tác:

Server with GUI > KDE > Done

![image](https://user-images.githubusercontent.com/62273292/158610977-3ce685c7-1598-45cb-ad82-c00e04b62118.png)

Bước 22: Mục INSTALLATION DESTINATION, chọn ổ đĩa ảo 40GB mình đã tạo lúc nãy > Done

![image](https://user-images.githubusercontent.com/62273292/158611072-6584d370-98e1-4543-b22f-247d384f3531.png)

Bước 23: Mục NETWORK & HOST NAME, chọn ON > Done

![image](https://user-images.githubusercontent.com/62273292/158611129-150d71e6-e44b-4afb-91c9-0c85e0443bd6.png)

Bước 24: Chọn Begin Installation

![image](https://user-images.githubusercontent.com/62273292/158611186-8f33b658-696f-4f59-9193-f81700ab43b1.png)

Bước 25: Thiết lập tài khoản ROOT, tài khoản này rất quan trọng nên cần phải ghi nhớ mật khẩu

![image](https://user-images.githubusercontent.com/62273292/158611245-c650a008-6445-46c4-aaa1-6d0dd44b183d.png)

Bước 26:  Chờ máy tự động cài đặt, bạn chờ khoảng 3 đến 5 phút tuỳ vào cấu hình của máy tính. Click Reboot

![image](https://user-images.githubusercontent.com/62273292/158611317-f6257829-57d5-4347-8ab2-c89039e3856a.png)

Bước 27: Tick chọn I accept the license agreement

![image](https://user-images.githubusercontent.com/62273292/158611380-8e008600-fa30-4061-92d0-c05112496a86.png)

Bước 28: Tạo tài khoản mới để đăng nhập vào hệ thống.

![image](https://user-images.githubusercontent.com/62273292/158611437-e27de2f4-6ea0-440f-9a86-2d865173fdf1.png)

Bước 29: Set mật khẩu cho tài khoản của bạn vừa tạo lúc nãy. LƯU Ý 2 MẬT KHẨU ROOT VÀ USER KHÁC NHAU

![image](https://user-images.githubusercontent.com/62273292/158611521-a1ba2150-73c5-4ab5-bc07-502b0887b501.png)

Bước 30: Giờ ta đã có thể chạy được Centos trên máy ảo VMware.

![image](https://user-images.githubusercontent.com/62273292/158611675-1758dfe6-5d68-4410-b2ee-d3d37208bced.png)








