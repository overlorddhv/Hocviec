
# Tổng quan

   **1.1  Tổng quan về công nghệ ảo hóa**
   
Với sự phát triển nhanh chóng của ngành công nghệ thông tin, các công nghệ cũ dần dần đã thể hiện nhiều mặt hạn chế và không phù hợp với nhu cầu thực tiễn nữa, đặc biệt là đối với nhu cầu ngày càng cao và phúc tạp của các doanh nghiệp như quản lý tập trung cơ sở dữ liệu, giảm thiểu chi phí về cơ sở hạ tầng công nghệ,hiệu năng sử dụng,... Do đó sự ra đời của công nghệ ảo hóa là tất yếu và là giải pháp.

Công nghệ ảo hóa đang làm thay đổi bộ mặt của thế giới điện toán bằng các công cụ có khả năng được triển khai và quản lý đơn giản, hiệu quả. Bằng việc tối ưu sử dụng các nguồn tài nguyên hệ thống, và chi phí triển khai ban đầu thấp, ảo hóa đem lại cho các doanh nghiệp nhiều khả năng và nguồn lợi to lớn.

Sức mạnh của công nghệ ảo hóa là tận dụng hiệu suất làm việc của các máy chủ bằng cách cho phép cài đặt nhiều máy chủ ứng dụng trên một máy chủ vật lý. Và việc quản lý cũng trở nên dễ dàng và tập trung hơn trên một máy chủ duy nhất.

**1.1.1 Khái niệm về công nghệ ảo hóa**

Ảo hóa là một công nghệ phần mềm khai thác triệt để khả năng làm việc của các phần cứng trong một hệ thống máy chủ. Nó hoạt động như một tầng trung gian giữa hệ thống phần cứng máy tính và phần mềm chạy trên nó, nó thay đổi nhanh chóng toàn cảnh của lĩnh vực Công nghệ Thông tin (CNTT) và cách tính toán của con người. Máy chủ trong các hệ thống CNTT ngày nay thường được thiết kế để chạy một hệ điều hành và một ứng dụng. Điều này không khai thác triệt để hiệu năng của hầu hết các máy chủ rất lớn. Ảo hóa cho phép vận hành nhiều máy chủ ảo trên cùng một máy chủ vật lý, dùng chung các tài nguyên của một máy chủ vật lý qua nhiều môi trường khác nhau. Các máy chủ ảo khác nhau có thể vận hành nhiều hệ điều hành và ứng dụng khác nhau trên cùng một máy chủ vật lý.

![image](https://user-images.githubusercontent.com/65167293/157791176-24a7d227-9930-4def-8713-8f22a20c2894.png)

Hình 1.1.1 : Một server vật lý trong hệ thống ảo hóa

**1.1.2 Thành phần của một hệ thống ảo hóa**

**1.1.2.1 Tài nguyên vật lý (host machine / host hadware)**

Các tài nguyên vật lý trong môi trường ảo hóa cung cấp tài nguyên mà các máy ảo sẻ sử dụng tới.một môi trường tài nguyên lớn có thể cung cấp được cho nhiều máy ảo chạy trên nó và hiệu quả làm việc của các máy ảo cao hơn. Các tài nguyên vật lý thông thường như là ổ đĩa cứng, Ram, card mạng, CPU,….

**1.1.2.2 Các phần mềm ảo hóa (virtual software)**

Lớp phần mềm ảo hóa này cung cấp sự truy cập cho mỗi máy ảo đến tài nguyên hệ thống. Nó cũng chịu trách nhiệm lập kế hoạch và phân chia tài nguyên vật lý cho các máy ảo. Phần mềm ảo hóa là nền tản của môi trường ảo hóa. Nó cho phép tạo ra các máy ảo cho người sử dụng, quản lý các tài nguyên và cung cấp các tài nguyên này đến các máy ảo. Kế hoạch quản lý sử dụng tài nguyên khi có sự tranh chấp một tài nguyên đặc biệt của các máy ảo, điều này dẫn tới sự hiệu quả làm việc của các máy ảo. Ngoài ra phần mềm ảo hóa còn cung cấp giao diện quản lý và cấu hình cho các máy ảo. 

**1.1.2.3 Máy ảo (virtual machine)**

Thuật ngữ máy ảo được dùng chung khi miêu tả cả máy ảo (lớp 3) và hệ điều hành ảo (lớp 4). Máy ảo thực chất là một phần cứng ảo trên một môi trường hay một phân vùng trên ổ đĩa. Trong môi trường này có đầy đũ thiết bị phần cứng như một máy thật . Đây là một kiểu phần  mềm ảo hóa dựa trên phần cứng vật lý. Các hệ điều hành khách mà chúng ta cài trên các máy ảo này không biết phần cứng mà nó nhìn thấy là phần cứng ảo. 

**1.1.2.4 Hệ điều hành khách(Guest operating system)**

Hệ điều hành khách được xem như một phần mềm (lớp 4) được cài đặt trên một máy ảo (lớp 3) giúp ta có thể sử dụng dễ dàng và xử lý các sự cố trong môi trường ảo hóa, Nó giúp người dùng có những thao tác giống như là đang thao tác trên một lớp phần cứng vật lý thực sự.

**1.2.3 Ưu điểm của công nghệ ảo hóa**

\-	Khai thác và quản lý triệt để các tài nguyên hiện hữu về cơ sở hạ tầng**,** giúp hệ thống hoạt động với sự linh hoạt cao, tận dụng khả năng phần cứng tối đa.

\-	Giảm thiểu các chi phí bằng cách giảm hạ tầng vật lý và cải thiện máy chủ, giúp quản lý tốt hơn cũng như giảm các yêu cầu về nhân sự.

\-	Tăng cường tính sẵn sàng của phần cứng và ứng dụng để cải thiện tính liên tục kinh doanh. Sao lưu dự phòng và di trú toàn bộ môi trường ảo hóa an toàn mà không cần ngưng phục vụ. 

\-	Hạn chế thời gian chết (downtime) và khôi phục ngay lập tức khi phát sinh sự cố bằng các công nghệ hỗ trợ có sẵn như High Availability, Load balancing, Vmmonitor, Raid, công nghệ lưu trữ mạng SAN…..

\-	Đạt được tính linh động trong quá trình vận hành: Đáp ứng các thay đổi kinh doanh với sự quản lý tài nguyên động, cung cấp máy chủ nhanh hơn và cải thiện triển khai destop và ứng dụng.

\-	Cải thiện khả năng quản lý và bảo mật desktop: Triển khai, quản lý và giám sát các môi trường desktop an toàn mà các người dùng có thể truy cập cục bộ hay từ xa, có hoặc không có kết nối mạng, trên hầu hết bất kỳ chuẩn desktop, laptop hay tablet PC nào.

**1.1.4 Nhược điểm**

Vấn đề khó khăn của công nghệ này chính là về bảo mật. Bảo mật cho môi trường ảo hóa vẫn gặp nhiều khó khăn khi thiếu công cụ cần thiết vì môi trường ảo có những yêu cầu riêng, khác biệt so với môi trường thực tế.

Vấn đề tương thích giữa hệ điều hành máy ảo với hệ điều hành máy chủ và hệ điều hành máy chủ với phần cứng.

**1.2 Nội dung báo cáo**

Nghiên cứu về công nghệ ảo hóa nói chung và công nghệ ảo hóa của VMWare nói riêng để hiểu và ứng dụng vào việc xây dựng mô hình ứng dụng ảo hóa trong thực tế cho doanh nghiệp.

**1.3 Cấu trúc báo cáo**

Chương 1: Tổng Quan.

Nêu tổng quan về công nghệ ảo hóa, các ưu và nhược điểm khi triển khai công nghệ này; Các khái niệm trong công nghệ ảo hóa,…

Chương 2: Nền tảng công nghệ Ảo Hóa.

- `   `Giới thiệu về các nền tảng công nghệ ảo hóa và phân loại công nghệ ảo hóa
- `   `Giới thiệu các công nghệ hỗ trợ công nghệ ảo hóa
- Nghiên cứu công nghệ ảo hóa của VMWare với ESX server và các tính năng cao cấp của nó.

Chương 3 : Triển khai và quản trị trên hệ thống của ESX server

Triển khai xây dựng mô hình thực tế trên hệ thống ảo của ESX server, từ đó thấy được ưu nhược điểm của hệ thống đối với việc ứng dụng vào thực tế.

Chương 4: Kết Luận 

Trình bày kết quả đạt được, những hạn chế và hướng phát triển của đề tài.

# Nền tảng công nghệ ảo hóa

   **2.1 Các kiến trúc công nghệ ảo hóa**
   
   **2.1.1 Công nghệ ảo hóa VMWare** 
      
Đây là công nghệ ảo hóa cực kỳ mạnh mẽ của công ty VMware. Công nghệ ảo hóa của VMWare  cho phép doanh nghiệp và các nhà cung cấp dịch vụ biến trung tâm dữ liệu của họ thành những trung tâm dữ liệu được ảo hóa. Công nghệ ảo hóa này mang đến cho người sử dụng những nhu cầu thiết yếu là tính sẵn dùng, sự quản lý đồng bộ và khả năng bảo mật. Công nghệ ảo hóa của VMWare cho phép ảo hóa các hệ thống  máy chủ vật lý một cách mạnh mẽ và hiêu quả nhờ các tính năng cao cấp được hỗ trợ trong các phiên bản ESX server và trong phiên bản mới nhất VMWare vSphere Hypervisor. VMware cũng cung cấp đầy đủ các ứng dụng ảo hóa quan trọng cho doanh nghiệp, cụ thể là chức năng trình chịu lỗi, quản lý khả năng khôi phục dữ liệu, quản lý tài nguyên phần cứng được tập trung, …

![image](https://user-images.githubusercontent.com/65167293/157791262-e347ec5a-41b2-4317-a0a3-fdf8587b252a.png)

Hình 2.1.1: Mô hình ảo hóa VMWare

**2.1.2 Công nghệ ảo hóa Hyper\_V** 

Hyper-V chính là công nghệ ảo hóa thế hệ kế tiếp dựa trên hypervisor của Microsoft, hyper-v khai thác phần cứng server 64-bit thế hệ mới (Hyper-V chỉ chạy trên nền HĐH server 64-bit và CPU có hỗ trợ 64-bit có tính năng ảo hoá) và có nhiều cải tiến quan trọng, là thành phần quan trọng trong Windows Server 2008 x64 và tích hợp với các công cụ quản lý server quen thuộc trên Windows. 

![image](https://user-images.githubusercontent.com/65167293/157791300-b3abe81f-6fbe-4b5e-997e-ade97c8ab4af.png)

Hình 2.1.2: Mô hình ảo hóa Hyper\_V

Với Hyper-V, Microsoft cung cấp một nền tảng ảo hóa mạnh và linh hoạt, có thể đáp ứng nhu cầu ảo hóa mọi cấp độ cho môi trường doanh nghiệp. Với kiến trúc hoạt động mới của Hyper-V giúp xây dựng hệ thống Server bảo mật và khai thác tối ưu hiệu suất của Server trong hệ thống mạng. Trong cấu trúc của Hyper-V gồm 3 phần chính: phân vùng cha(parent) là phân vùng chứa hệ điều hành máy chủ vật lý, các phân vùng con(child) là phân vùng của các hệ điều hành máy ảo, cuối cùng là lớp hypervisor. Windows Hypervisor là một bộ giao tiếp bằng phần mềm, nó nằm giữa lớp phần cứng vật lý và một hay nhiều hệ điều hành. Hypervisor điều khiển việc truy cập đến phần nhân của phần cứng và định nghĩa ra các môi trường hoạt động độc lập tách rời gọi là partition. Nhiệm vụ chính của lớp Windows Hypervisor là đảm bảo sự tách rời giữa các phân vùng và giám sát việc sử dụng tài nguyên phần cứng giữa các phân vùng, bảo đảm cô lập để bảo mật giữa các phân vùng hệ điều hành máy ảo. Windows Hypervisor điều khiển phần cứng vật lý giống như advanced programmable interrupt controllers (APICs) trong việc ngắt quãng định tuyến, bộ xử lý vật lý để lên kế hoạch xử lý một cách logic việc truy cập của máy ảo, hàng chờ, không gian bộ nhớ vật lý để điều khiển các truy xuất đến Ram và bộ nhớ thiết bị và các phần cứng khác. Phân vùng cha quản lý việc phân phối Ram, bộ xử lý và quản lý nguồn, Pci bus, các thiết bi truy xuất thông qua các trình điều khiển thiết bị.

**2.1.3 Công nghệ ảo hóa OpenVZ**

OpenVZ là một nhánh mã nguồn mở của Virtuozzo do SWsoft cung cấp. Đây là một giải pháp ảo hóa thương mại ở cấp độ hệ điều hành (OS-level virtuallization) dựa trên nhân Linux. OpenVZ cho phép một máy chủ vật lý có thể chạy nhiều hệ điều hành một cách độc lập và được coi như một máy chủ riêng ảo (VPSS) hoặc môi trường ảo (VES), đảm bảo các ứng dụng không bị xung đột. Lợi thế của OpenVZ là đạt được hiệu suất rất cao so với việc triển khai các máy chủ độc lập. Tuy nhiên OpenVZ có một hạn chế là đòi hỏi cả máy chủ và hệ điều hành khách đều phải sử dụng các hệ thống mã nguồn mở của Linux. OpenVZ được chia thành 2 cấp độ: mức tùy chỉnh nhân kernel và mức người sử dụng ở mức công cụ.

![image](https://user-images.githubusercontent.com/65167293/157791342-f2e24b3b-d2a6-4b7c-a269-7b8d56e92886.png)

Hình 2.1.3: Mô hình ảo hóa OpenVZ

**2.2 Phân loại ảo hóa**

   **2.2.1 Ảo hóa máy chủ (Server virtualization)**
   
![image](https://user-images.githubusercontent.com/65167293/157791379-b92e8226-ad1d-443c-a527-047c53438384.png)


Mục đích chính của việc ảo hóa máy chủ chính là tách rời mối liên hệ luồng công việc của máy chủ từ máy chủ vật lý để mà chúng ta có khả năng phân thành nhiều luồng công việc hơn đem đền sự hiệu quả đáng kể trong doanh nghiệp. Ví dụ trung bình với một máy vật lý dùng làm DHCP chỉ sử dung hết 3/10 khả năng của máy vật lý. Với ảo hóa máy chủ cho phép dùng hết 10/10 khả năng máy vật lý, lúc này máy vật lý sẽ kiêm nhiều nhiệm vụ hơn như DNS, FTP… tăng cao tính hiệu quả. Các công nghệ ảo hóa máy chủ hiện tại đang sử dụng công nghệ hypervisor giúp cho khả năng chạy nhiều hệ điều hành máy khách thường gọi là Partition (phân vùng) trên một máy chủ đơn lẻ. Khả năng phân luồng công việc máy chủ trở thành hiện thực. Bên cạnh đó công nghệ này cũng đem đến những cải thiện đáng kể cho máy chủ, nâng cao tính sẵn sàng cho hệ thống và khả năng mở rộng hạ tầng, đơn giản hóa việc sao lưu và phục hồi, và giảm chi phí điều hành.

**2.2.2 Ảo hóa ứng dụng (Application virtualization)**

![image](https://user-images.githubusercontent.com/65167293/157791412-18d3d833-1185-47fe-8efa-7167e66ec489.png)


Ảo hóa ứng dụng là một dạng công nghệ ảo hóa khác cho phép chúng ta tách rời mối liên kết giữa ứng dụng và hệ điều hành và cho phép phân phối lại ứng dụng phù hợp với nhu cầu user. Bằng cách chạy các ứng dụng một cách tập trung thay vì cài đặt lên mỗi máy trạm, quản lý việc cập nhật phần mềm trở nên dễ dàng hơn, giải quyết vấn đề tương thích giữa các ứng dụng và việc thử nghiệm sự tương thích của chúng cũng trở nên dễ dàng hơn.

**2.2.3 Ảo hóa máy khách (Desktop Virtualization)**

![image](https://user-images.githubusercontent.com/65167293/157791437-34905c5d-7cc6-4e77-b030-e3796b1d4841.png)


Đây là nhóm công nghệ mới mục tiêu chính là tạo nên một môi trường cô lập hoàn toàn trên máy tính. Việc triển khai công nghệ này có thể giúp chúng ta hỗ trợ các ứng dụng cũ chạy trên hệ điều hành hiện tại và giải quyết được vấn đề tương thích đang gây khó khăn khi muốn nâng cấp hệ thống, cho phép các doanh nghiệp tiếp cận các hệ điều hành mới nhất dễ dàng hơn và đạt đươc nhiều lợi ích hơn từ những tính năng mới.

**2.2.4 Ảo hóa trình diễn (Presentation virtualization)**

![image](https://user-images.githubusercontent.com/65167293/157791482-fb1d2cf1-d2c8-4eaf-8b02-c2f94c9f809a.png)


Ảo hóa trình diễn đòi hỏi sự tách rời giữa việc xử lý và việc lưu trữ dữ liệu từ máy trạm. Khóa chính của giải pháp này chính là Terminal Services, là một trong những công nghệ ảo hóa sẵn sàng trên mọi phiên bản Windows Server 2008. Việc dùng Terminal Services đem đến cho chúng ta khả năng chạy một ứng dụng ở mọi nơi trong khi có thể dùng nó ở một nơi khác. Loại trừ đi được quá trình cài đặt các ứng dụng một cách cục bộ trên mỗi máy tính, từ giờ chúng ta có thể cài đặt và quản lý chúng một cách tập trung trong phòng quản lý hoặc data center. Terminal Services làm cho mỗi user cảm giác mình đang làm việc với các ứng dụng tại local với các thao tác được hiển thị trên màn hình, trong khi đó mọi thông tin thao tác thật sự đều gởi đến server xử lý.

**2.2.5 Ảo hóa hồ sơ (Profile virtualization)**

![image](https://user-images.githubusercontent.com/65167293/157791499-3fc857cd-876b-4ed4-aed8-58cf4926d05b.png)


Bao gồm việc ảo hóa các tính năng thông dụng trên máy chủ: Folder Redirect, Roaming User Profile, và Offline Files với đặc tính chung là sự tách rời phần dữ liệu và thông tin người dùng về hệ thống với máy trạm.

User profiles, là một cấu trúc hệ thống file (thư mục và file) gồm có thông tin trạng thái cho mỗi người dùng trên một máy tính. Một số thư mục và file trong user profile thường bị ẩn để tránh cho người dùng nhầm lẫn với các nội dung của họ.

**2.3 Cơ chế hoạt động của công nghệ ảo hóa**

Ảo hóa được xây dựng dựa trên giải pháp chia một máy vật lý thành nhiều máy con. Giải pháp này được biết đến với cái tên là Virtual Machine Monitor (VMM) sau này gọi là Hypervisor. Hypervisor cho phép tạo tách rời các máy ảo và điều phối truy cập của các máy ảo này đến tài nguyên phần cứng.

Hypervisor hoạt động như là một lớp phần mềm nằm ngay trên phần cứng hoặc bên dưới một hoặc nhiều hệ điều hành khách. Mục đích chính của nó là cung cấp các môi trường  làm việc cho các máy ảo. Cho phép các máy ảo hoạt động trên một phần của phần cứng được gọi là phân vùng (partition). Các hệ điều hành của máy ảo được cài đặt trên phân vùng này. Mỗi phân vùng sẽ được cung cấp tập hợp các tài nguyên phần cứng riêng của nó chẳng hạn như bộ nhớ, các chu kỳ CPU và thiết bị. Hypervisor có trách nhiệm điều khiển và phân phối các luồng truy cập đến các tài nguyên phần cứng

Khi một hệ điều hành thực hiện truy xuất hoặc tương tác tài nguyên phần cứng trên hệ điều hành chủ thì công việc của một Hypervisor sẽ là:

- Hypervisor mô phỏng phần cứng, nó làm cho các hệ điều hành tưởng rằng mình đang sử dụng tài nguyên vật lý của hệ thống thật.
- Hypervisor liên lạc với các trình điều khiển thiết bị
- Các trình điều khiển thiết bị phần cứng liên lạc trực tiếp đến phần cứng vật lý.

![image](https://user-images.githubusercontent.com/65167293/157791528-ee726c4e-4258-4514-b3f4-7639366021bf.png)

Hình 2.3 : vị trí của lớp ảo hóa Hypervisor

Trong mô hình này trình điều khiển phần cứng liên lạc trực tiếp với các thiết bị phần cứng mà không phải qua bất kì trung gian nào nên nó mang lại một hiệu suất cao nhất về sử dụng tài nguyên phần cứng. Một vài sản phẩm đang sử dụng dạng này là Microsoft Hyper-V, Citrix Xenserver, Vmware ESX server. 

**2.4 Các công nghệ hỗ trợ hệ thống ảo hóa**

   **2.4.1 Công Nghệ Máy ảo (Virtual Machine)**
   
Máy ảo là một máy tính được cài trên một hệ điều hành khác hay một máy tính khác. Một máy ảo cũng bao gồm phần cứng, các ứng dụng phần mềm và hệ điều hành. Điều khác biệt ở đây là lớp phần cứng của máy ảo không phải là các thiết bị thường mà chỉ là một môi trường hay phân vùng mà ở đó nó được cấp phát một số tài nguyên như là chu kì cpu, bộ nhớ, ỗ đĩa….Công nghệ máy ảo cho phép cài và chạy nhiều máy ảo trên một máy tính vật lý. Mỗi máy ảo có một hệ điều hành máy khách riêng lẻ và được phân bố tài nguyên, ổ cứng, card mạng và các tài nguyên phần cứng khác một cách hợp lý. Việc phân bố tài nguyên này phụ thuộc vào nhu cầu của từng máy ảo ứng dụng và cũng tùy thuộc vào phương pháp ảo hóa được dùng. Đặc biệt khi máy ảo cần truy  xuất tài nguyên phần cứng thì nó hoạt động giống như một máy thật hoàn chỉnh. Vì chỉ là một tập tin được phân vùng trên ổ đĩa nên việc di chuyển các máy ảo từ máy chủ này sang máy chủ khác là rất dễ dàng và không cần quan tâm đến vấn đề tương thích phần cứng hay ảnh hưởng tới máy chủ.

![image](https://user-images.githubusercontent.com/65167293/157791556-5a20532e-a22c-411b-967a-b96de19eea11.png)

Hình 2.4.1 : Mô hình các lớp tương tác trong hệ thống

Trong kiến trúc của một bộ xử lý ảo hóa được chia thành 4 lớp . Lớp 0 là lớp có quyền cao nhất có thể truy cập và can thiệp sâu nhất đến tài nguyên phần cứng. Lớp 0 thường là các hệ điều hành chủ được cài trên chính máy chủ. Lớp 1 là lớp ảo hóa Hypervisor. Lớp này dùng đề quản lý và phân phối tài nguyên đến các máy ảo. Lớp 2 là các hệ điều hành khách chạy trên các máy ảo. Để truy cập tài nguyên phần cứng nó phải liên lạc với lớp ảo hóa và phải qua hệ điều hành máy chủ . Lớp có quyền can thiệp thấp nhất đến tài nguyên là lớp 3 là các ứng dụng hoạt động trên các máy ảo.

Trong các hệ thống máy tính lớn dùng để xử lý các ứng dụng thương mại và khoa học( mainframe), hệ điều hành chạy trên phần cứng máy thực ở chế độ ưu tiên vì chỉ có hệ điều hành chủ mới được phép sửa đổi và can thiệp vào phần cứng bên dưới nó. Còn máy ảo làm việc ở chế độ giới hạn vì phần cứng mà nó nhìn thấy chỉ là các thiết bị ảo . Khi máy ảo yêu cầu các lệnh  hoặc tiến trình thông thường thì hệ điều hành chủ  sẽ chuyển tiếp chúng đến bô xử lý để thực thi trực tiếp, còn đối với  các lệnh hoặc các tiến trình  đặc biệt nhạy cảm can thiệp sâu đến phần cứng bên dưới sẽ bị chặn lại vì có thể làm ảnh hưởng tới hệ thống và máy ảo còn lại. Hệ điều hành chủ  sẽ thực thi lệnh  với bộ xử lý trên máy thực rồi sau đó mô phỏng kết quả rồi trả về cho máy ảo. Đây là cơ chế nhằm cách ly máy ảo với máy thực để đảm bảo an toàn hệ thống. 

**2.4.2 Công nghệ cân bằng tải (Load Balancing)**

Trong xu hướng công nghệ, máy chủ là trái tim của của mạng máy tính, nếu máy chủ mạng hỏng, hoạt động của hệ thống sẽ bị ngưng trệ. Do vậy, vấn đề đặt ra là cần có một giải pháp để đảm bảo cho hệ thống vẫn hoạt động tốt ngay cả khi có sự cố xảy ra đối với máy chủ mạng. Giải pháp hiệu quả được đưa ra là sử dụng một nhóm server cùng thực hiện một chức nǎng dưới sự điều khiển của một công cụ phân phối tải - Giải pháp cân bằng tải. Có rất nhiều hãng đưa ra giải pháp cân bằng tải như Cisco, Coyote Point, Sun Microsystems... với rất nhiều tính nǎng phong phú.

Load Balancing là một công nghệ có khả năng chia tải và nâng cao khả năng chịu lỗi của hệ thống. Load Balancing không chỉ làm nhiệm vụ phân phối tải cho các server mà còn còn cung cấp cơ chế đảm bảo hệ thống server luôn khả dụng trước các client và nhu cầu truy cập từ internet.

Hiện nay có 2 loại cân bằng tải được áp dụng:

\-	Cân bằng tải sử dụng phần cứng: sử dụng các mođun cắm thêm trên các thiết bị chuyên dụng như Bộ định tuyến (Router) hay hay bộ chuyển mạch (Switch) để chia tải theo luồng, thường hoạt động từ layer 4 trở xuống. Vì sử dụng thiết bị chuyên dụng nên có hiệu năng cao, tính ổn định cao, khả năng mở rộng tốt hơn nhưng khó phát triển được tính năng bảo mật phức tạp. Thường sử dụng các thiết bị của Cisco, F5, Citrix,…

\-	Cân bằng tải sử dụng phần mềm: Sử dụng phần mềm cài trên server để kết hợp nhiều server một cách chặt chẽ tạo thành một server ảo (virtual server). Cách này có ưu điểm là có thể chia sẻ được nhiều tài nguyên trong hệ thống, theo dõi được trạng thái của các máy chủ trong nhóm để chia tải hợp lý. Tuy nhiên, do sử dụng phần mềm trên server, tính phức tạp cao nên khả năng mở rộng của giải pháp này bị hạn chế, phức tạp khi triển khai cũng như khắc phục khi xảy ra sự cố, có rào cản về tính tương thích, khó có được những tính năng tăng tốc và bảo mật cho ứng dụng. Thường sử dụng các giải pháp Proxy, DNS load balancing, Round Robin NDS,…

**2.4.2.1 Công nghệ cân bằng tải mạng (Network Load Balancing (NLB))**

Load Balancing là một công nghệ có khả năng chia tải và nâng cao khả năng chịu lỗi của hệ thống. Được dùng cho các ứng dụng Stateless applications (các ứng dụng hoạt động mang tính nhất thời) như Web, File Tranfer Protocol (FTP), Virtual Private Network (VPN)… Trong hệ thống NLB sẽ bao gồm các cụm server được cấu hình tương tự nhau (có thể được đặt rải rác ở nhiều nơi) cùng hoạt động để phân phối khối lượng công việc giữa các máy chủ trong hệ thống, giúp hệ thống giảm bớt gánh nặng khi phân bố tải.

Nhược  điểm của NLB là mỗi cụm server phải dùng riêng một nơi lưu trữ cục bộ (Local Storage) cho nên cần phải có quá trình đồng bộ hóa dữ liệu ở mỗi nơi lưu trữ, số lượng cụm server càng nhiều thì thời gian cho việc đồng bộ hóa càng lâu, chính vì điều này nên ta không nên triển khai các ứng dụng Stateful applications (các ứng dụng hoạt động thường xuyên trong thời gian dài) như các database server: Microsoft SQL Server, Microsoft Exchange Server, File and Print Server… trên kỹ thuật NLB này nhằm đảm bảo tính chính xác của dữ liệu.

**2.4.2.2 Công nghệ cân bằng tải Clustering**

Đây là công nghệ được dùng rộng rãi cho các hệ thống cần độ sẵn sàng phục vụ cao, đây là giải pháp được đặc biệt quan tâm do tính kinh tế, đa dạng và khả nǎng dịch vụ cao. Công nghệ này có thể sử dụng phần cứng chuyên dụng để cung cấp một môi trường với độ tin cậy cao đảm bảo cho các dịch vụ có thể hoạt động trơn tru mà không bị dừng bởi một vài lỗi nhỏ; hoặc cũng có thể được thiết kế để chạy trên các phần cứng thông dụng mà vẫn đạt được các yêu cầu:

\-   Tăng cường khả năng mở rộng.
\-   Nâng cao hiệu suất.
\-   Tính sẵn sàng cao và khắc phục sự cố.

![image](https://user-images.githubusercontent.com/65167293/157791599-bde1a326-476f-4161-adf2-274af1363d39.png)

Hình 2.4.2.1: Mô hình cân bằng tải Clustering

Với hệ thống sử dụng công nghệ clustering, trong quá trình khởi tạo cấu hình của hệ thống sẽ bao gồm một hệ thống với các nút chính chủ động (active primary node) và một hệ thống với các nút phụ bị động sao lưu (passive backup node). Trong hệ thống này các nút chủ động và bị động cần có cùng cấu hình và được sử dụng công nghệ lưu trữ SAN hoặc Raid (Raid 1).

Nút đang hoạt động (active node) sẽ đáp lại các yêu cầu về dịch vụ thông qua một địa chỉ IP ảo (Virtual IP hay VIP). Địa chỉ VIP là một địa chỉ IP và nó chỉ khác so với địa chỉ IP thông thường của một nút đang hoạt động.

Hệ thống bị động (gồm các nút không hoạt động) sẽ không trực tiếp chạy dịch vụ, thay vào đó nó quản lí các dịch vụ của nút chủ động đang hoạt động, và đảm bảo chắc chắn là nút đang hoạt động vẫn phải đang còn hoạt động. Nếu nút không hoạt động phát hiện ra 1 vấn đề nào đó với hoặc là nút hoạt động hoặc dịch vụ đang chạy trên nó, thì một thông báo lỗi sẽ được khởi tạo.Khi có lỗi, hệ thống clustering sẽ thực hiện các bước sau:

\-   Nút đang hoạt động sẽ trực tiếp ngắt hết các dịch vụ đang chạy và các kết nối.

\-   Nút không hoạt động sẽ khởi động các dịch vụ tương đương với các dịch vụ của máy chủ động.

\-   Nút đang hoạt động sẽ ngắt không sử dụng địa chỉ VIP

\-   Nút không hoạt động bây giờ lại chuyển thành nút đang hoạt động, và ở chế độ sử dụng địa chỉ VIP.

\-   Nếu nó vẫn đang hoạt động và đang duy trì kết nối mạng, nút trước kia là chủ động thì bây giờ trở thành nút bị động, bắt đầu giám sát các dịch vụ của nút chủ động.

**2.4.3 Công nghệ lưu trữ SAN**

SAN là một hệ thống mạng lưu trữ chuyên dụng kết nối nhiều Server và nhiều thiết bị lưu trữ, với mục  đích chính là truyền tải dữ liệu giữa hệ thống máy tính và phần tử lưu trữ và giữa các phần tử lưu trữ với nhau.

![image](https://user-images.githubusercontent.com/65167293/157791626-9a678764-b7f4-4e57-a8bd-c1ef16cba466.png)

Trong ảo hóa công nghệ lưu trữ mạng được dùng làm trung tâm của dữ liệu và cũng có thể làm nơi chứa các máy ảo khi cần thiết. Nó hỗ trợ các máy chủ có thể lấy dữ liệu từ nó để khởi động.

Lợi ích của SAN  

\-  Lưu trữ tập trung dữ liệu trên một hệ thống đơn nhất.  

\-  Cho phép truy cập dữ liệu với tốc  độ rất cao (2Gb/s; 4Gb/s tương lai lên tới 10Gb/s).  

\-  Tính ổn định liên tục của thiết bị rất cao (99,999%).  

\-  Dễ dàng nâng cấp, mở rộng trong tương lại (tăng thêm số lượng máy chủ, hay mở rộng dung lượng lưu trữ lên rất lớn và uyển chuyển): bảo vệ sự đầu tư thông qua khả năng tương thích ngược với các switch thế hệ cũ hơn, và khả năng nâng cấp firmware của thiết bị mà không phải dừng hoạt động hệ thống, đảm bảo mọi dịch vụ đều được duy trì liên tục 100%.  

\-  Có khả năng sao lưu dữ liệu trong nội bộ hệ thống SAN, mà không phải dừng dịch vụ của máy chủ để sao lưu như các hệ thống lưu trữ khác, đồng thời không hề ảnh hưởng băng thông của mạng LAN khi thực hiện các thao tác backup.  

\-  Bảo mật tốt: xác thực, xác quyền, điều khiển truy xuất và khả năng quản lý theo vùng tăng thêm mức bảo mật mạng.  

\-  Hỗ trợ nhiều hệ điều hành và môi trường cluster, cho phép thiết kế linh động và bảo vệ sự đầu tư.  

\-  Uyển chuyển trong khoảng cách, kết nối và hiệu suất, với khả năng hỗ trợ nhiều hơn 3000 port. Hỗ trợ cơ sở hạ tầng đa giao thức gồm FC, iSCSI, và FCIP. 

**2.4.4 Công nghệ Raid**

RAID (Redundant Array of Independent Disks) có ngĩa là sự tận dụng các phần dư trong các ổ cứng độc lập. Ban đầu, RAID được sử dụng như một giải pháp phòng hộ vì nó cho phép ghi dữ liệu lên nhiều đĩa cứng cùng lúc. RAID chính là sự kết hợp giữa các đĩa cứng vật lý bẳng cách sử dụng một trình điều khiển đặc biệt RAID có thể sử dụng như là một phần cứng lẫn phần mềm.

`	`Hệ thống RAID được dùng trong việc đảm bảo an toàn dữ liệu  khi có ổ đĩa bị lỗi và phục hồi lại các dữ liệu , có thể thay nóng ổ đĩa đối với một số loại RAID và cũng còn tùy thuộc vào máy chủ. RAID ngày càng trở nên cần thiết cho các hệ thống máy tính 

Vì RAID mang tính toàn vẹn dữ liệu cao , phục hồi nhanh chóng nên RAID chủ yếu được ứng dụng vào các máy máy chủ, không phải là các máy bàn không thể dùng Raid được mà là do chi phí đầu tư khá tốn kém nên chỉ ở các hệ thống lớn đòi hỏi độ an toàn cho dữ liệu phải cao mới sử dụng.

**Striping (Song Hành):** 

Là một trong những chuẩn RAID có hiệu năng cao nhất , nó giúp ta tăng tốc độ truy cập lên tối đa bằng cách ghi song song dữ liệu lên các ổ đĩa này . Kỹ thuật này sẽ chia các tệp dự liệu ra và ghi đồng thời lên ổ đĩa cứng trong cùng một thời gian . Và khi đọc thì cũng đọc cùng lúc trên tất cả các ổ đĩa làm cho tốc độ đọc và hiệu suất cao.

Ở cấp độ byte Striping chia ra thành từng gói nhỏ có kích thước một byte và bộ điều khiển sẽ ghi byte này lên ổ đĩa , trong cấp độ Block thì tập tin cũng bị chia nhỏ , lúc này chia nhỏ như thế nào thì tùy theo kích thước của Block nó như thế nào , tập tin sẽ được lưu và phân bổ trên các Block này.

![image](https://user-images.githubusercontent.com/65167293/157791708-abaa64cd-0613-4ab3-a364-e40e85563214.png)

**Duplexing (Ghép Đôi) :**

Đây là chuẩn mở rộng của Mirroring . Dữ liệu cũng được ghi trên hai ổ cứng nhưng phải có 2 bộ điều khiển RAID kết nối với 2 đĩa cứng . Từ đây ta đã thấy chuẩn này khá tốn kém . Nhưng có một đặc tính là Duplexing mang tính bảo mật cao hơn Mirroing vì ở đây nó dùng tới 2 card điêu khiển RAID

![image](https://user-images.githubusercontent.com/65167293/157791733-81681f1f-1470-4d97-8636-d95f0c867cc9.png)

**Parity RAID:**

Đây là phương pháp bảo vệ an toàn cho dữ liệu , sử dụng các thông tin mang tính chẵn lẻ bằng cách lưu giữ một con số nhị phân 0 hoặc 1 cho biết tổng các bit trong gói tin là chẵn hay lẻ . Nếu dùng chuẩn này thì lợi ích lớn nhất của nó là không yêu cầu hệ thống RAID bớt đi một phần dung lượng để lưu trữ dữ liệu . Nhưng cũng có khuyết điểm của nó là phải yêu cầu hệt thống có một phần cứng thật mạnh .

**JBOD:** 

Được viết tắt từ “Just a Bunch of Disks” và không phải là hệ thống RAID chính thống, nó không có mục đích cải thiện hiệu suất của ổ cứng hay độ tin cậy. Nó dùng để ghép những ổ cứng có dung lượng khác nhau thành một dung lượng lưu trữ duy nhất.

Từ các chuẩn Raid trên cho ra đời các loại Raid như Raid 0, Raid 1, Raid 2, Raid 3, Raid 4, Raid 5, Raid 6, Raid 0+1, Raid 10,…là các ứng dụng dựa trên các công nghệ của những chuẩn RAID.

**2.5 Các tính năng của VMWare EXSi server**

   **2.5.1 Virtual Machine File System (VMFS)**
   
- VMFS của VMware chỉ được tạo dành cho ảo hóa VMware. Vì vậy nó là hệ thống file hiệu suất cao nhất có sẵn để sử dụng trong việc ảo hóa doanh nghiệp. Tuy được gộp vào phiên bản nào đó hoặc gói ESX Server hay VI bạn chọn nhưng VMFS vẫn được đưa ra như một sản phẩm riêng bởi Vmware. Điều này là vì nó cũng khá độc nhất.
- Đây là một hệ thống file cluster hiệu suất cao cho phép nhiều hệ thống có thể truy cập vào hệ thống file tại cùng một thời điểm. VMFS là những gì mang đến cho bạn một nền tảng vững chắc để thực hiện VMotion và VMHA. Với nó bạn có thể tăng phân vùng một cách linh hoạt, hỗ trợ việc ghi nhật ký và bổ sung thêm đĩa ảo cho hệ thống. Thêm hoặc xóa một Server ESX từ một khối lượng VMware VMFS mà không phá vỡ khác ESX Server hosts.
  
  **2.5.2  Virtual symmetric multi-processing (Virtual SMP)**
  
- Virtual SMP của VMware (hay VSMP) là một tính năng cho phép VMware ESX Server có thể tận dụng đến 4 bộ vi xử lý vật lý trên hệ thống đồng thời. Thêm vào đó, với VSMP, việc xử lý các nhiệm vụ sẽ được cân bằng giữa các CPU. 

  **2.5.3Công nghệ độ sẵn sàng cao (High Availability)**
  
High Availability  được cung cấp bởi nhà sản suất VMware . Đây là một tiện ích hoàn hảo được thiết kế cho hệ thống máy chủ ESX  và VMware Infrastructure .Mục đích của công nghệ này là di chuyển các máy ảo từ máy chủ này sang một máy chủ khác khi sảy ra sự cố về hỏng hóc máy chủ vật lý hay mất kết nối mạng.Công nghệ này giúp các máy ảo ứng dụng có thể được phục hồi và hoạt động ngay khi chuyển sang máy chủ mới mà không có lo lằng gì về vấn đề tương thích với máy chủ vật lý.

`	`Đây là một tính năng rất mạnh vì bất cứ hệ thống hoặc thiết bị phần cứng nào cũng đều có thể bị rủi ro và hư hỏng,và các vấn đề trục trặc này khó có thể đoán trước được .Vì vậy để đảm bảo an toàn dữ liệu và các máy chủ ứng dụng có thể hoạt động trực tuyến ngay lập tức khi bị sự cố thì giải pháp chính là  cấu hình cho hệ thống hoạt động tính năng High Availability.

![image](https://user-images.githubusercontent.com/65167293/157791776-5275b81e-129d-4ff7-8e19-79ee04fa21fb.png)

Hình 2.5.3 : Sơ đồ hoạt động của VMware High Availability

Yêu cầu của VMware High Availability:

- Công nghệ High Availability chỉ hỗ trợ cho một số phần Phần mềm ảo hóa do VMware cung cấp như là VMware Infrastructure hoặc VMware ESX Server.
- Để cấu hình tính năng này phải có ít nhất là hai hệ thống máy chủ sử dụng ảo hóa. 
- Phải có ít nhất một thiết bị lưu trữ mạng SAN để kết nối hai hệ thống.
- Yêu cầu phải có tương thích về hoạt động của các hệ thống máy chủ.

Ưu điểm:

- Cung cấp độ an toàn cao cho các máy ảo,nhờ đó các máy ảo có thể hoạt động được ngay khi đươc di chuyển sang hệ thống máy chủ mới.
- Không phân loại hệ điều hành,High Availability có thể di chuyển bất cứ hệ điều hành nào được cài trên máy ảo.
- Cấu hình dễ dàng và triển khai nhanh chóng.
- Có thể kết hợp với các công nghệ khác như bộ phân phối tài nguyên nguyên (Distributed Resource *Scheduler*) và VMonitor để các máy ảo di chuyển sang hệ thống khác mà không gây mất kết nối đối với người dùng.

Hạn chế:

- Các CPU trên mỗi máy chủ phải tương thích với nhau.
- Các máy ảo nằm trên hệ thống máy chủ gặp trục trặc cần phải khởi động lại.
- Không đảm bảo an toàn cho các ứng dụng khi máy tự động khởi động lại sau khi chuyển qua máy chủ mới.


  **2.5.4 VMotion & Storage Vmotion**
  
![image](https://user-images.githubusercontent.com/65167293/157791800-e31eb31b-90a2-4458-8b18-da06cad25038.png)

- Với VMotion, khi ta thiết lập lưu trữ datacenter (không có thì không sử dụng được tính năng này), các máy khách ảo VM có thể được chuyển quyền điều khiển từ một máy esx server này sang một máy esx server khác mà không gây ra thời gian chết đối với người dùng
- Storage VMotion (hay SVMotion) cũng tương tự như Vmotion trong vấn đề có liên quan tới VM, được chuyển và không có thời gian chết đối với máy khách VM và người dùng. Với SVMotion, các máy khách VM nằm trên máy chủ nó cư trú thì đĩa ảo cho VM chính là những gì chuyển đổi. Nó giúp bạn có thể chuyển đổi các đĩa ảo của máy khách VM từ một kho dữ liệu nội bộ trên máy chủ ESX này sang kho lưu trữ SAN (sang datacenter) chia mà không gây ra thời gian chết đối với người dùng


  **2.5.5 VMware Consolidated Backup (VCB)**
  
![image](https://user-images.githubusercontent.com/65167293/157791834-ca5825a4-262b-4ceb-ab12-6a8fd03313d0.png)

- VBC là một nhóm các tiện ích dòng lệnh của Windows, được cài đặt trên hệ thống Windows, có kết nối SAN đến hệ thống file ESX Server VMFS. Với VCB, bạn có thể thực hiện các backup mức file và mức image, khôi phục các máy khách VM, quay trở về máy chủ VCB. Nhiều hãng backup đã tích hợp VCB để có thể thực hiện dễ dàng hơn. 
- Người ta thường sử dụng vSphere Data Recovery để thay thế vì nó có giao diện đồ họa dễ sử dụng.


  **2.5.6 Trung tâm quản lý nâng cấp (Vcenter update Manager)**
  
- Quản lý nâng cấp (Update Manager) là một tính năng mới đi kèm với Virtual Center & ESX Server. Với Update Manager có thể thực hiện các nâng cấp ESX Server, các nâng cấp của hệ điều hành Windows và Linux đối với máy khách VM. Để thực hiện các nâng cấp ESX Server, có thể sử dụng Vmotion và nâng cấp ESX Server mà không hề gây ra thời gian chết đối với các máy khách VM đang chạy trên nó. Ngoài ra, Update Manager dùng để vá các hệ thống khách và chủ để ngăn chặn các lỗ hổng bảo mật đang bị khai thác.


  **2.5.7 Phân phối tài nguyên theo lịch trình (Distributed resource scheduler( DRS))**
  
![image](https://user-images.githubusercontent.com/65167293/157791864-5fa8bd21-7186-4c40-b285-7a0961ef1cbd.png)

- Phân phối tài nguyên theo lịch trình là một trong những tính năng tiên tiến khác của ESX Server và VI Suite. DRS về cơ bản là một hệ thống lập lịch trình tài nguyên và cân bằng tải của các máy chủ ESX. Nếu được thiết lập hoàn toàn tự động thì DRS có thể nhận ra vị trí tài nguyên có lợi nhất trên tất cả các máy chủ ESX và chuyển linh hoạt các máy khách VM từ một máy chủ ESX này sang máy chủ khác bằng Vmotion, không mất thời gian chết của máy đối với người dùng. Nó có thể được sử dụng cho việc sắp đặt ban đầu của các máy khách VM và cho tối ưu liên tục (khi VMware gọi đến nó). Thêm vào đó, nó còn có thể được sử dụng cho việc duy trì máy chủ ESX.

  **2.5.8 Quản lý phân phối điện năng (Distributed Power Manager (DPM))**
  
- DPM là một phần của Distributed Resource Scheduler (DRS) được tích hợp trong VMWare.
- Cũng như chức năng tối ưu hóa quá trình tải tài nguyên qua nhiều máy chủ lưu trữ ESX của DRS, DPM cũng có thể góp phần thực hiện chức năng này bằng cách di chuyển các máy ảo khách khỏi những máy chủ không sử dụng và tắt những máy chủ này.
- Trong VMWare, DPM được mô tả như sau: VMWare DRS tích hợp tính năng quản lý điện năng phân phối (DPM) thử nghiệm. Khi DPM được kích hoạt hệ thống sẽ đối chiếu công suất cấp độ máy chủ và cluster với yêu cấu của những máy ảo đang vận hành trong cluster đó. Dựa trên kết quả so sánh, DPM sẽ đề cuất (hay tự động triển khai) các biện pháp giúp giảm tiêu thụ điện năng của cluster.


  **2.5.9 Virtual Center (VC) & Infrastructure Client (VI Client)**
  
![image](https://user-images.githubusercontent.com/65167293/157791918-c38a1ad4-9c9b-4b61-b4c3-97edde85b628.png)


` 	`VMware Infrastructure client và Virtual Center cũng là một tính năng tiên tiến của ESX Server & VI Suite. Virtual Center là một phần trong nhiều tính năng máy chủ ESX. Nó có nhiều tính năng tiên tiến bên trong. Khi đi kèm với VC, VI Client thực sự là một giao diện cho quản trị viên VMware sử dụng để cấu hình, tối ưu và quản trị tất cả các hệ thống máy chủ ESX.

- Với VI Client, bạn có thể tăng được các vấn đề như hiệu suất, quản trị role, bảo mật, và các tính năng dựa trên mẫu của các máy khách VM mới cho toàn bộ cơ sở hạ tầng ảo hóa. Nếu có nhiều ESX Server, thì bạn cần phải có VMware Virtual Center.


  **2.5.10 Quản lý khôi phục site (Site Recovery Manager (SRM))**
  
` 	`Quản lý khôi phục site là một tính năng khôi phục thảm họa tuyệt vời. Nếu bạn có hai trung tâm dữ liệu (một chính và được bảo vệ còn một phụ và được dùng để khôi phục - primary/protected - secondary/recovery), các máy chủ ESX của VMware và SRM được hỗ trợ SAN tại mỗi site thì bạn có thể sử dụng SRM để lập kế hoạch, kiểm tra và khôi phục toàn bộ cơ sở hạ tầng ảo hóa VMware của mình. 

**2.5.11 Khôi phục dữ liệu (VMware vShere Data Recovery)**

![image](https://user-images.githubusercontent.com/65167293/157791964-fb5f7b9f-2ab2-4d4d-bd72-f58d3f085113.png)

Một trong những tính năng mới trong vSphere là Data Recovery, trong cụm giải pháp “Essentials Plus” hoặc phiên bản vSphere Advanced. Tính năng mới này được cung cấp như một máy ảo bên trong môi trường vSphere và tích hợp với máy chủ vCenter nhằm cung cấp cách thức quản lý tập trung đối với các backup. vSphere Data Recovery sử dụng giao diện quản lý GUI khá hoàn chỉnh với một loạt các wizard hỗ trợ cài đặt và quản lý tất các công việc backup lẫn khôi phục.

**Các tính năng chính:**

- Backup dự phòng và hoàn chỉnh của các image máy ảo (VM) và backup/restore mức file cho các máy ảo Windows.
- Hỗ trợ VSS cho các máy ảo Windows để có được các backup tin cậy hơn
- Tránh nhân bản dữ liệu nhằm giảm không gian lưu trữ cho các backup
- Giao diện quản lý vCenter cho quản lý GUI tập trung và sử dụng nhiều wizard để đơn giản hóa các hoạt động.
- Lưu trữ đĩa bằng cách sử dụng một loạt các giao thức kết nối chuẩn - iSCSI, FC, NAS hay lưu trữ nội bộ
- vSphere được tích hợp đầy đủ và có nhiều cải tiến, tiếp tục backup các máy ảo khi chúng bị chuyển sang một host khác.
- 
 **2.5.12*** **Chuyển đổi máy ảo (vCenter Convert)**
 
![image](https://user-images.githubusercontent.com/65167293/157792000-a531d9a1-c206-49cd-b392-5ba7da442e61.png)

Tính năng này cho phép convert máy vật lý đang chạy (bao gồm cả hệ điều hành và dữ liệu trên máy vật lý tùy bạn muốn) thành máy ảo chạy trong VMware ESX Server (cả windows và linux). Tính năng này miễn phí

Lưu ý rằng Virtual Center được yêu cầu cho một số tính năng tiên tiến hơn và nó được mua riêng. Bên cạnh đó cũng có một số mức khác nhau trong việc hỗ trợ khả năng sẵn có cho các sản phẩm này. 

  # Triển khai và quản trị trên hệ thống VMWare
  
   **3.1 Mô hình ứng dụng** 
   
   **3.1.1 Mục tiêu triển khai hệ thống** 
   
- Ảo hóa toàn bộ hệ thống máy chủ và các ứng dụng để loại trừ:
  - Thời gian trì trệ đầu tư thiết bị máy chủ mới khi triển khai ứng dụng mới.
  - Thời gian chết (downtime) khi bảo trì hay nâng cấp hệ thống máy chủ.
- Tiết kiệm chi phí đầu từ hệ thống máy chủ, tiết giảm không gian của phòng máy chủ, độ phức tạp của hệ thống cáp kết nối và chi phí hàng ngày cho hệ thống điện và làm mát.
- Khai thác triệt để hiệu năng cũng như công năng của công nghệ và sức mạnh phần cứng máy chủ hiện nay.
- Quản lý tập trung tại một điểm duy nhất và giảm thiểu các thao tác quản trị.
- 
  **3.1.2 Mô hình** 


![image](https://user-images.githubusercontent.com/65167293/157792033-e7e18ba0-3be9-41e4-bf90-46f91fdc8d27.png)



Yêu cầu hệ thống:

|STT|Thành phần|Mô tả kỹ thuật|
| :-: | :- | :- |
|1|*CPU*|Chủng loại bộ vi xử lý ≥ Quad-Core. Tốc độ xung xử lý ≥ 3.0GHz|
|2|*RAM*|Phụ thuộc vào số lượng máy ảo/Host. *Khuyến cáo:* tối thiểu 1GB/VM|
|3|*HDD*|Dung lượng lưu trữ ≥ 160GB |
|4|*RAID Controller*|Hỗ trợ chuẩn RAID-1 (Mirror)|
|5|*Network Interface*|Gigabit Ethernet|
|6|*Một số phần mềm hỗ trợ*|<p>- ESX server; VMWare vSphere client</p><p>- Window server 2003; win XP,</p><p>- Mail MDeamon server; các component để triển khai domain,web server,…</p>|


  **3.1.3 Cài đặt VMWare EXS sever**
(Chưa làm được và sẽ bổ sung sau)

##

## **	
# Kết luận

   **Kết quả đạt được**

Về lý thuyết:

Thấy được lợi ích của công nghệ ảo hóa khi ứng dụng vào thực tế đề giảm chi phí đầu tư, tăng hiệu suất hoạt động, tận dụng được cơ sở hạ tầng, nâng cao hiệu quả quản lý,…

Nắm được các kiến thức của công nghệ ảo hóa nói chung và công nghệ ảo hóa VMWare nói riêng .

Hiểu được các cấu trúc, tính năng của hệ thống ảo hóa sử dụng VMWare ESX server.

Tìm hiểu được các công nghệ hỗ trợ cho công nghệ ảo hóa như công nghệ cân bằng tải, Raid, công nghệ lưu trữ mạng SAN,...

Về thực nghiệm:

Chưa triển khai được hệ thống mạng sử dụng công nghệ ảo hóa của VMWare và xây dựng được các server ứng dụng trên hệ thống ảo hóa này

**Hạn chế**

Do bị giới hạn về cơ sở vật chất nên chưa triển khai hết được các tính năng của VMWare (đòi hỏi về bản quyền, cấu hình máy chủ,…)

**Hướng phát triển**

Do bị hạn chế về vật chất, thời gian và khả năng của bản thân nên đề tài còn nhiều thiếu sót. Nếu có điều kiện, đề tài sẽ triển khai thêm các nội dung sau:

- Triển khai đầy đủ các tính năng của ESX Server.
- Triển khai mô hình doanh nghiệp đầy đủ và quy mô hơn.**	


**Tài liệu tham khảo**

[1] John Kelbley, Mike Sterling, Allen Stewart (2009) *Sybex - Windows Server 2008 Hyper-V*. Wiley Publishing, Inc

[2] ScottLowe (2009 )*Mastering VMware vSphere 4*. Wiley Publishing

[3] Bernard Golden (2009) *Virtualization for Dummies*. Wiley Publishing

[4]  Chandra Kopparapu (2002)*Load Balancing Servers, Firewalls, and Caches.* Wiley Computer Publishing

[5]  Anil Desai (2007) *The Definitive Guide to Virtual Platform Management*. Realtime Publishing

[6] Palo Alto (2008) *VMware Infrastructure Brochure*. VMware Publishing

[7] WHITE PAPER (2010)*VMware\_Virtual\_Hardware*. VMware Publishing

[8] <Http://diendanmaychu.net>	

` `[10] <http://vmware.com>	

` `[12] <http://quantrimang.com>	


