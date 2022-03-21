# Network File System

## NFS (Network File System) là gì?

NFS (Network File System) là một hệ thống giao thức chia sẻ file phát triển bởi Sun Microsystems từ năm 1984, cho phép một người dùng trên một máy tính khách truy cập tới hệ thống file chia sẻ thông qua một mạng máy tính giống như truy cập trực tiếp trên ổ cứng.

## Những tính năng của NFS là gì?

- NFS cho phép truy cập cục bộ đến các tệp từ xa, cho phép nhiều máy tính sử dụng cùng một tệp để mọi người trên mạng có thể truy cập vào cùng một dữ liệu

- Với sự trợ giúp của NFS, chúng ta có thể cấu hình các giải pháp lưu trữ tập trung.

- Giảm chi phí lưu trữ bằng cách để các máy tính chia sẻ ứng dụng thay vì cần dung lượng ổ đĩa cục bộ cho mỗi ứng dụng của người dùng

- Giảm chi phí quản lý hệ thống và minh bạch hệ thống tập tin

- Cung cấp tính nhất quán và độ tin cậy của dữ liệu vì tất cả người dùng đều có thể đọc cùng một bộ tệp

- Có thể bảo mật với Firewalls và Kerberos
## Cài đặt và cấu hình NFS trên server Linux


### Setup NFS Server và Client trên CentOS 7.x để chia sẻ dữ liệu

Bước 1: Cấu hình Firewall

Sử dụng firewall mặc định của Centos 7

` yum -y install firewalld`


![image](https://user-images.githubusercontent.com/62273292/159374296-12bc8e36-d1e2-4b95-abb1-89c54a249e94.png)

![image](https://user-images.githubusercontent.com/62273292/159374421-4fadb424-35ee-43b9-8cc2-7ef397830aa2.png)


Khởi động và đặt chế độ khởi động mặc định

`systemctl start firewalld.service`

`systemctl enable firewalld.service`

![image](https://user-images.githubusercontent.com/62273292/159374558-badbebb1-1588-4b2f-b91f-40f04f0acf13.png)


Mở các port SSH và NFS

```
firewall-cmd --permanent --zone=public --add-service=ssh
firewall-cmd --permanent --zone=public --add-service=nfs
firewall-cmd --reload
```

![image](https://user-images.githubusercontent.com/62273292/159374686-65d7cea7-fe8e-41d7-8434-24383a427bd6.png)

Bước 2: Cài đặt NFS

Trên server, ta chạy lệnh:

`yum -y install nfs-utils`

![image](https://user-images.githubusercontent.com/62273292/159374818-63f2e5dc-4fb0-4ac1-a16f-8f92ca4f7a51.png)


Sau đó khởi động nfs server service

```
systemctl enable nfs-server.service
systemctl start nfs-server.service
```
![image](https://user-images.githubusercontent.com/62273292/159374919-37af0605-2857-4a31-bf6a-f2679640e099.png)


Bước 3: Tạo thư mục chia sẻ trên Server

```
mkdir /var/vthien
chown nfsnobody:nfsnobody /var/vthien
chmod 755 /var/vthien
```

![image](https://user-images.githubusercontent.com/62273292/159376325-ab0dbeaf-b226-4377-bca3-5cf04028dfd5.png)


Sử dụng export để khai báo phân vùng sử dụng NFS share

`vi /etc/exports`

![image](https://user-images.githubusercontent.com/62273292/159376577-51364634-115a-44ef-b178-923c91b90d8c.png)


Sau đó thêm vào:

```
/home           192.168.1.101(rw,sync,no_root_squash,no_subtree_check)
/var/nfs        192.168.1.101(rw,sync,no_subtree_check)
```

Tùy chọn no_root_squash để /home được access bởi root. Sau đó chạy lệnh:

`exportfs -a`

![image](https://user-images.githubusercontent.com/62273292/159376786-18f0de0c-6d6e-446b-96eb-2bc2307fbc43.png)

Bước 4: Mount NFS Shares trên Client

![image](https://user-images.githubusercontent.com/62273292/159376939-aa19766f-fae2-4a3a-bf30-d1e6ce8ab314.png)


## Cấu hình trên Windows Server 2019

Mở Server manage lên và chọn Add role and features

![image](https://user-images.githubusercontent.com/62273292/159377166-d743ab48-6dfb-4c73-90db-37e03fb5b937.png)

Chọn Next

![image](https://user-images.githubusercontent.com/62273292/159377186-edb00f3c-9111-4478-b5ad-a884d59d4f4a.png)


Chọn Next

![image](https://user-images.githubusercontent.com/62273292/159377199-036859ec-e9cb-4da9-8118-6d5179c6efb6.png)


Chọn Next

![image](https://user-images.githubusercontent.com/62273292/159377227-364ef36a-2e57-431d-af97-236dc89f67e6.png)

Chọn Client for NFS rồi chọn Next

![image](https://user-images.githubusercontent.com/62273292/159377244-580c713a-5bfc-4fc1-b045-8c63991ee715.png)


Chọn Install để tiến hành cài đặt

![image](https://user-images.githubusercontent.com/62273292/159377262-e5fa80c4-95fd-4e68-9cce-f68d3cb546a0.png)


![image](https://user-images.githubusercontent.com/62273292/159377276-56245914-905a-4140-a9e7-2dce630fa1c2.png)


  Xử Lý Bị Lỗi

![image](https://user-images.githubusercontent.com/62273292/159377454-2637b5f6-2049-46ef-b141-bcf75fdb8f75.png)























