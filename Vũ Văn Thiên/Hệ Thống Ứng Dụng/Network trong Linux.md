# Network trong Linux

## Các lệnh cơ bản về network trong linux

Xác định địa chỉ ip và các network interface

![image](https://user-images.githubusercontent.com/62273292/159157603-a57e4720-502f-41b8-bde6-a80536288458.png)


Để xem những thiết bị được kết nối vào computer từ IRQ 1 - IRQ 15 :

![image](https://user-images.githubusercontent.com/62273292/159157666-9ced74c5-a647-4210-890b-644c064bab6c.png)


Thiết lập địa chỉ ip cho một card mạng ta dùng command sau :

[root@bigboy tmp]# ifconfig eth0 192.168.1.5 netmask 255.255.255.0 up

Thiết lập cấu hình có định cho card mạng tao vào edit files cho card mang eth0 tại /etc/sysconfig/network-scripts/ifcfg-eth0 với nội dung như sau:

Fixed IP Address

[root@bigboy tmp]# cd /etc/sysconfig/network-scripts

[root@bigboy network-scripts]# vi ifcfg-eth0

Sau khi cấu hình xong ta dùng command sau để cho card mạng nhận được cấu hình mới :

Thiết lập cấu hình có định cho card mạng tao vào edit files cho card mang eth0 tại /etc/sysconfig/network-scripts/ifcfg-eth0 với nội dung như sau:

![image](https://user-images.githubusercontent.com/62273292/159157748-46cdd9a3-a22e-4e02-b4f1-af066a315639.png)


![image](https://user-images.githubusercontent.com/62273292/159157758-ef921bed-f5f4-4ff5-a40f-77e6aa719748.png)


![image](https://user-images.githubusercontent.com/62273292/159157775-bbaaf1ff-deb4-4eb4-aba4-6b44c1c9ee97.png)


