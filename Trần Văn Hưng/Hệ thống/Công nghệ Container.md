# 1. Containers là gì?

Containers là công nghệ ảo hóa hệ điều hành được sử dụng để gói applications và các phụ thuộc của chúng (dependencies), chạy trong các môi trường cô lập. Chúng cung cấp phương pháp nhẹ nhàng để gói và triển khai applications theo cách tiêu chuẩn hóa trên nhiều loại hạ tầng khác nhau.

Những mục tiêu này khiến container trở thành lựa chọn hấp dẫn cho cả developers và chuyên gia vận hành. Containers chạy ổn định trên bất kỳ máy chủ nào có khả năng chứa container, vì vậy developers có thể kiểm tra cùng một software cục bộ mà sau này sẽ triển khai đến các môi trường sản xuất đầy đủ. Định dạng container cũng đảm bảo rằng các phụ thuộc của application được đưa vào image, đơn giản hóa quá trình xử lý và giải phóng. Bởi vì các máy chủ và nền tảng chạy container là chung, quản lý hạ tầng cho các hệ thống dựa trên container có thể được tiêu chuẩn hóa.

Containers được tạo từ container images : các nhóm đại diện cho hệ thống, ứng dụng và môi trường của container. container images hoạt động như là các mẫu tạo ra containers cụ thể và cùng một image có thể sinh ra bất kỳ số lượng container đang chạy nào.

Điều này tương tự như cách classes và instances hoạt động trong lập trình hướng đối tượng (object-oriented programming); một class duy nhất có thể tạo bất kỳ số lượng instances nào giống như container image duy nhất có thể tạo bất kỳ số lượng container nào. Sự tương tự này cũng đúng với sự kế thừa vì container images có thể đóng vai trò là nguồn gốc cho những container images tùy chỉnh hơn. Users có thể tải xuống container dựng sẵn từ các nguồn bên ngoài hoặc xây dựng images tùy chỉnh theo nhu cầu.

# 2. Docker là gì?

Mặc dù Linux containers là công nghệ hơi chung chung có thể được triển khai và quản lý theo một số cách khác nhau, nhưng cho đến nay Docker vẫn là cách phổ biến nhất để chạy building và chạy containers. Docker là bộ công cụ cho phép users tạo container images, đẩy hoặc kéo images từ các registries bên ngoài, chạy và quản lý containers trong nhiều môi trường khác nhau. Sự gia tăng về mức độ phổ biến của containers trên Linux có thể được quy trực tiếp cho những nỗ lực của Docker sau khi phát hành vào năm 2013.

Công cụ dòng lệnh docker đóng nhiều vai trò. Nó chạy và quản lý container, hoạt động như một trình quản lý quy trình cho container workloads. Nó có thể tạo container images mới bằng cách đọc và thực thi các lệnh từ Dockerfile hoặc chụp nhanh các container đang chạy. Lệnh cũng có thể tương tác với Docker Hub , container image registry, để kéo xuống container images mới hoặc đẩy local images lên để lưu hoặc công khai chúng.

Mặc dù Docker chỉ cung cấp một trong nhiều triển khai container trên Linux, nhưng nó có điểm khác biệt là entry point phổ biến nhất trong thế giới của containers và là giải pháp được triển khai phổ biến nhất. Mặc dù các tiêu chuẩn mở đã được phát triển cho container để đảm bảo khả năng tương tác, hầu hết các nền tảng và công cụ liên quan đến container đều coi Docker là mục tiêu chính khi thử nghiệm và phát hành software. Docker không hẳn là giải pháp hiệu quả nhất cho một môi trường nhất định, nhưng nó là một trong những lựa chọn được thử nghiệm nhiều nhất.

Nói một cách thực tế, trong khi có các lựa chọn thay thế cho containers trên Linux, thì việc tìm hiểu Docker trước rất có ích vì tính phổ biến và ảnh hưởng của nó đối với thuật ngữ, tiêu chuẩn và công cụ của hệ sinh thái.

# 3. Hoạt động của Container

**Virtual Machines và Container**

Virtual Machines, hay VMs, là công nghệ ảo hóa hardware cho phép ảo hóa hoàn toàn hardware và tài nguyên của máy tính. Một hệ điều hành khách riêng biệt quản lý virtual machine, tách biệt hoàn toàn với hệ điều hành chạy trên hệ thống máy chủ. Trên hệ thống máy chủ, một phần software được gọi là hypanneror chịu trách nhiệm khởi động, dừng và quản lý virtual machines.

Do VMs được vận hành như máy tính hoàn toàn khác biệt, trong điều kiện hoạt động bình thường, không ảnh hưởng đến hệ thống máy chủ hoặc các VMs khác, virtual machines cung cấp sự cô lập và bảo mật tuyệt vời. Tuy nhiên có một số nhược điểm. Ví dụ, ảo hóa toàn bộ máy tính yêu cầu VMs sử dụng lượng tài nguyên đáng kể. Do virtual machine được vận hành bởi hệ điều hành khách hoàn chỉnh, nên thời gian cung cấp và khởi động virtual machine có thể khá chậm. Tương tự, vì VMs hoạt động như machine độc lập, quản trị viên cần áp dụng công cụ và quy trình quản lý giống như hạ tầng để cập nhật và chạy các môi trường riêng lẻ.

Nói chung, virtual machines cho phép chia tài nguyên của machine thành các máy tính riêng lẻ, nhỏ hơn, nhưng kết quả cuối cùng không khác biệt đáng kể so với việc quản lý một nhóm máy tính vật lý. Việc mở rộng thành viên và trách nhiệm của mỗi máy chủ có thể tập trung hơn, nhưng các công cụ, chiến lược và quy trình sử dụng và khả năng của hệ thống có thể sẽ không thay đổi đáng kể.

Containers có nhiều cách tiếp cận khác nhau. Container ảo hóa hệ điều hành một cách trực tiếp thay vì ảo hóa toàn bộ máy tính. Chúng chạy như quy trình chuyên biệt được quản lý bởi kernel của hệ điều hành máy chủ, nhưng với một cảnh nhìn bị ràng buộc và bị điều khiển nặng nề về quy trình, tài nguyên và môi trường của hệ thống. Containers không biết rằng chúng tồn tại trên một hệ thống dùng chung và hoạt động như thể chúng có toàn quyền kiểm soát máy tính.

Thay vì xử lý containers như thể chúng là máy tính đầy đủ như máy ảo, thì việc quản lý containers tương tự như applications là phổ biến hơn. Chẳng hạn, tuy có thể gắn SSH server vào một container nhưng nó không phải là mô hình được đề xuất. Thay vào đó, việc gỡ lỗi thường được thực hiện thông qua giao diện ghi nhật ký, các cập nhật được áp dụng bằng cách cuộn các images mới và quản lý service được nhấn mạnh để ưu tiên quản lý toàn bộ container.

Những đặc điểm này có nghĩa là containers chiếm một không gian ở đâu đó giữa các máy ảo được cô lập và quản lý riêng của các quy trình thông thường. Containers cung cấp khả năng phân vùng và ảo hóa tập trung vào quá trình, cung cấp sự cân bằng tốt về sự giới hạn, tính linh hoạt và tốc độ.

**Linux cgroups và Namespaces**

Linux kernel có một vài tính năng giúp thực hiện việc này. Linux control groups, hay còn gọi là cgroups, là tính năng kernel cho phép quy trình và tài nguyên của chúng được nhóm lại, cô lập và được quản lý như một unit. cgroups kết hợp các quy trình lại với nhau, xác định tài nguyên nào có thể truy cập và cung cấp cơ chế quản lý và giám sát hành vi. Chúng tuân theo hệ thống phân cấp cho phép tiến trình con kế thừa các điều kiện gốc và có khả năng áp dụng các ràng buộc hơn nữa. cgroups cung cấp chức năng cần thiết gắn các quy trình lại với nhau thành một nhóm và giới hạn tài nguyên có thể truy cập.

Tính năng kernel chính khác mà containers dựa vào là Linux namespaces. Namespaces giới hạn những gì quá trình có thể thấy về phần còn lại của hệ thống. Các quy trình chạy bên trong namespaces không nhận thức được bất cứ thứ gì chạy bên ngoài namespace của chúng. Vì các namespaces xác định một ngữ cảnh riêng biệt tách biệt với phần còn lại của hệ thống, nên process tree của namespace cần phản ánh ngữ cảnh đó. Bên trong namespace, quy trình chính trở thành PID 1 (tiến trình ID 1), quy trình PID truyền thống dành riêng cho hệ thống init của hệ điều hành. Process tree ảo bị điều khiển này được xây dựng trong namespace cho phép tiến trình chạy trong containers vận hành như thể chúng đang hoạt động trong môi trường bình thường, không bị hạn chế.

# 4. Lợi ích của việc container hóa

***Ảo hóa nhẹ***

So với ảo hóa hardware với máy ảo, container cực kỳ nhẹ. Thay vì ảo hóa tất cả tài nguyên hardware và chạy hệ điều hành hoàn toàn độc lập trong môi trường đó, containers sử dụng kernel của hệ thống máy chủ và chạy như các quy trình được ngăn cách trong HĐH đó. Từ quan điểm của máy chủ lưu trữ, containers chạy như bất kỳ quy trình nào khác, có nghĩa là chúng nhanh chóng khởi động và dừng lại, sử dụng lượng tài nguyên hạn chế. Container chỉ có thể xem và truy cập tập hợp con của không gian xử lý và tài nguyên của máy chủ, nhưng có thể hoạt động như thể nó là hệ điều hành hoàn toàn độc lập trong hầu hết các trường hợp. Bản thân container images cũng có thể rất nhỏ. Kích thước image tối thiểu cho phép workflows dựa trên việc kéo xuống image mới nhất trong thời gian chạy mà không gây ra sự chậm trễ đáng kể. Đây là yêu cầu cho nhiều hệ thống phân tán chịu lỗi, tự phục hồi.

***Sự cô lập môi trường***

Bằng cách sử dụng các tính năng Linux kernel như cgroups và namespaces, containers được cô lập khỏi môi trường máy chủ và các containers khác. Điều này cung cấp mức độ kiểm soát chức năng giúp ngăn chặn môi trường container can thiệp lẫn nhau. Mặc dù không đủ mạnh để coi là sandboxing bảo mật đầy đủ, nhưng sự cô lập này vẫn có có lợi thế. Sự phụ thuộc và xung đột library dễ tránh hơn vì máy chủ và mỗi container duy trì software trong filesystems riêng biệt. Vì các môi trường networking có thể được tách ra, nên applications trong container có thể liên kết với các cổng gốc của chúng mà không cần lo lắng về xung đột với software trên hệ thống máy chủ hoặc trong các containers khác. Sau đó, quản trị viên có thể chọn cách diễn dịch networking của container tới các networks máy chủ theo yêu cầu của họ.

***Định dạng Packaging được chuẩn hóa và mục tiêu về Runtime***

Một trong những lợi ích hấp dẫn nhất của container là khả năng thống nhất và đơn giản hóa quy trình đóng gói và triển khai software. Container images cho phép gộp applications và tất cả yêu cầu runtime của chúng vào một unit có thể triển khai trên nhiều cơ sở hạ tầng khác nhau. Bên trong các container, developers có thể cài đặt và sử dụng bất kỳ libraries nào mà applications yêu cầu mà không sợ can thiệp vào các thư viện hệ thống máy chủ. Các phụ thuộc là phiên bản bị khóa khi image được tạo. Vì runtime của container hoạt động như nền tảng tiêu chuẩn, triển khai ổn định, nên developers không cần biết nhiều về machines cụ thể nơi các container sẽ chạy. Miễn là container runtime hoạt động và có sẵn tài nguyên hệ thống đầy đủ, container sẽ chạy giống như trong môi trường development. Tương tự, từ góc độ hoạt động, container hóa giúp chuẩn hóa các yêu cầu của môi trường deployment. Thay vì phải cung cấp và duy trì môi trường duy nhất dựa trên ngôn ngữ application, runtime và các phụ thuộc, thì quản trị viên có thể tập trung vào việc duy trì các máy chủ chung có chức năng như nền tảng container và phân bổ nhóm tài nguyên mà machines có thể truy cập. Việc kết hợp tất cả đặc điểm riêng của application trong container sẽ tạo ra một ranh giới tự nhiên giữa các mối quan tâm của application và của nền tảng.

***Khả năng mở rộng***

Mô hình container cũng cho phép mở rộng applications bằng các cơ chế tương đối đơn giản. Kích thước image nhẹ, thời gian khởi động nhanh, khả năng tạo, kiểm tra và triển khai “golden images”, và môi trường runtime được tiêu chuẩn hóa là tất cả các tính năng có thể được sử dụng để xây dựng các hệ thống có khả năng mở rộng cao. Khả năng mở rộng của một hệ thống phụ thuộc nhiều vào kiến trúc application và cách thức container images được xây dựng. Các thiết kế hoạt động tốt với mô hình container nhận ra điểm mạnh của định dạng container để đạt sự cân bằng tốt về tốc độ, tính sẵn có và khả năng quản lý. Các kiến trúc Service-oriented , và cụ thể là microservices (kiến trúc nhiều dịch vụ nhỏ), cực kỳ phổ biến trong các môi trường container hóa bởi vì việc phân tách applications thành các thành phần riêng biệt với mục đích tập trung làm cho việc phát triển, nhân rộng và cập nhật đơn giản hơn.

# 5. Thuật ngữ Container

- Container: Trong Linux, container là công nghệ ảo hóa hệ điều hành được dùng để gộp applications và các phụ thuộc thành một gói và chạy chúng trong môi trường cô lập.

- Container Image: Container images là tệp tĩnh xác định hệ thống tệp và hành vi của các cấu hình container cụ thể. Container images được dùng làm mẫu để tạo containers.

- Container Orchestration: Orchestration là thuật ngữ được sử dụng để mô tả các quy trình và công cụ cần thiết để quản lý lượng lớn container trên nhiều máy chủ. Container orchestration thường kiểm soát tỷ lệ, khả năng chịu lỗi, phân bổ tài nguyên và lập lịch sử dụng nền tảng container.

- Container Runtime: container runtime là thành phần thực sự chạy và quản lý container trên máy chủ. Yêu cầu tối thiểu thường là cung cấp container từ một image nhất định, nhưng nhiều runtimes gộp các chức năng khác như quản lý quy trình, giám sát và quản lý image. Docker bao gồm container runtime trong lệnh docker[/B] của nó, nhưng có nhiều lựa chọn thay thế khác có sẵn cho các trường hợp sử dụng khác nhau.

- Docker: Docker là công nghệ đầu tiên truyền bá thành công ý tưởng Linux containers. Ngoài ra, hệ sinh thái công cụ của docker bao gồm docker, container runtime với các tính năng quản lý image và container rộng rãi, docker-compose, một hệ thống để xác định và chạy applications đa container và Docker Hub, đăng ký container image.

- Dockerfile: Dockerfile là tệp văn bản mô tả cách xây dựng container image. Nó xác định image cơ sở, các lệnh để chạy trong hệ thống và cách runtime sẽ khởi động và quản lý các quy trình trong container. Mặc dù không phải là tùy chọn duy nhất, nhưng Dockerfiles là định dạng phổ biến nhất để xác định container images, ngay cả khi không sử dụng chức năng xây dựng image của Docker.

- Kata Containers: Kata Containers là cách tiếp cận để quản lý máy ảo nhẹ bằng các mô hình, workflows và công cụ tái tạo trải nghiệm làm việc với containers. Các Kata containers tìm cách nắm bắt lợi ích của container trong khi cung cấp sự cô lập và bảo mật mạnh mẽ hơn.

- Kubernetes: Kubernetes là nền tảng điều phối container mạnh mẽ, quản lý clusters của container hosts và workloads chạy trên chúng. Kubernetes cung cấp công cụ và sự trừu tượng hóa để triển khai, mở rộng quy mô, giám sát và quản lý container trong môi trường sản xuất có tính sẵn sàng cao.

- Linux cgroups: Linux cgroups, hoặc các nhóm kiểm soát, là tính năng kernel kết hợp các quy trình lại với nhau và xác định quyền truy cập của chúng vào tài nguyên.Container trong Linux được triển khai bằng cgroups để quản lý tài nguyên và các quy trình riêng biệt

- Linux namespaces: Linux namespaces là tính năng kernel được thiết kế để giới hạn khả năng hiển thị cho một quá trình hoặc cgroup đối với phần còn lại của hệ thống. container trong Linux sử dụng namespaces để giúp cô lập workloads và tài nguyên của chúng khỏi các tiến trình khác đang chạy trên hệ thống.

- LXC: LXC là hình thức container hóa Linux có trước Docker và nhiều công nghệ khác trong khi dựa vào nhiều công nghệ kernel tương tự. So với Docker, LXC thường ảo hóa toàn bộ hệ điều hành thay vì chỉ các quy trình cần thiết để chạy application, và có vẻ giống với máy ảo hơn.

- Virtual Machines (Máy ảo): Máy ảo hay VM là công nghệ ảo hóa hardware mô phỏng toàn bộ máy tính. Một hệ điều hành đầy đủ được cài đặt trong máy ảo để quản lý các thành phần bên trong và truy cập tài nguyên computing của máy ảo.

- Virtualization (Ảo hóa): Ảo hóa là quá trình tạo, chạy và quản lý môi trường ảo hoặc tài nguyên máy tính. Ảo hóa là cách trừu tượng hóa tài nguyên vật lý và thường được dùng để phân đoạn một nhóm tài nguyên cho các mục đích khác nhau.

