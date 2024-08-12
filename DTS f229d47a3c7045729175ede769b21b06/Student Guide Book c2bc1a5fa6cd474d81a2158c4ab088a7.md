# Student Guide Book

# Module 1: Building a Simple Network

## Lession 1: Exploring the Functions of the Networks

*Network* có nghĩa là kết nối một lượng lớn các thiết bị lại với nhau.

*Computer network* là kết nối các thiết bị PCs, servers, phones, cameras, printers, … để chúng có thể giao tiếp với nhau.

![Untitled](Student%20Guide%20Book%20c2bc1a5fa6cd474d81a2158c4ab088a7/Untitled.png)

*Main Office —> Branch Office —> Home office —> Mobile Users*

### Các thành phần vật lý của Network

![Untitled](Student%20Guide%20Book%20c2bc1a5fa6cd474d81a2158c4ab088a7/Untitled%201.png)

**Endpoints**

**Interconnections:**

NICs: dịch dữ liệu máy tính sang định dạng có thể truyền qua mạng. NIC là thiết bị để cắm cáp mạng vào
Network media

Connectors provide

Switches:

💬 Kết nối các thiết bị trong cùng mạng để có thể giao tiếp với nhau.

Router: 

💬 Kết nối các mạng khác nhau lại và chọn đường dẫn tốt nhất giữa các mạng một cách thông minh.
Định tuyến lưu lượng truy cập từ mạng này sang mạng khác.

WLAN: wireless decives 

Access Points or APs: Cho phép những thiết bị không dây kết nốt đến một mạng có dây

WLAN Controllers: quản lý các APs

Firewalls: Kiểm soát và giám sát lưu lượng mạng truy cập dựa trên các quy tắc bảo mật được xác định trước.

Topology

![Untitled](Student%20Guide%20Book%20c2bc1a5fa6cd474d81a2158c4ab088a7/Untitled%202.png)

![Untitled](Student%20Guide%20Book%20c2bc1a5fa6cd474d81a2158c4ab088a7/Untitled%203.png)

Physical topology: Là topo kết nối các thành phần vật lý của network ⇒ Có thể chẩn đoán được lỗi ở network. ⇒ Dễ dàng fix lỗi và phải cập nhật duy trì liên tục, hàng ngày hàng tháng, ..vv

_ Phải có server lưu các thông tin truy cập về mạng —> Thêm bảo mật để không phải ai cũng có thể truy cập mạng.

_ làm quản trị về phần cứng

⇒ Không phản ánh được dữ liệu đang chạy trong mạng như nào.

Logical topology: 

_ VLAN này qua VLAN kia là phải qua định tuyến

_ Cho phép xem đc traffic flow trong các thiết bị mạng, giúp tìm lỗi sâu hơn trong dịch vụ.

💣 

Tốc độ access: tốc độ thiết bị truy cập vào 1 điểm

Là tốc độ từ máy tính đến router là 10MB

Tốc độ cam kết ra ngoài internet ?? ⇒ 

Tốc độ dịch vụ end to end

Cost: chi phí xây dựng lên network đấy chi phí mua bla bla,
Chi phí vận hành và bảo dưỡng.

Bảo mật truy cập vào network.

Bảo mật về mặt truyền tải từ điểm A đến điểm B. 

IPSec: Ip Sercurity , IpSec Framework

Tính khả dụng của mạng (availability): tính ổn định, khả năng sẵn sàng của mạng

Đo trong 1 năm thì khoảng thời gian uptime/downtime là bao lâu?

HA: High availability: 99,999 % uptime được gọi là mạng HA

ReEndency: router switch, firewall, server, …

Luôn có 1 cặp firewall chạy cùng với nhau, loadbacing, …

switch trong kiến trúc 3 lớp luôn có 1 cặp để giải quyết vấn đề reEndcy

Dự phòng về nguồn. —> Thiết bị cao cấp

Dự phòng về module xử lý chính RP rout processor

Nhà cũng cấp dịch vụ → nhà cung cấp nào lỗi thì chuyển sang nhà cung cấp khác.

Nếu 1 nhà cung cấp dịch vụ thì thuê 2 link

device, process, link

⇒ HA

Sercurity

 

QoS:

Máy - Máy

Người - Máy

Người - Người

Sắp xếp theo độ trễ giảm dần.

Với người với người cần đảm bảo:

Delay

Package loss

Sự khác biệt về delay - Rister Độ trượt: độ delay cho từng gói tin.

## Lession 2: Understanding the Host-to-Host Communications Moel

![Untitled](Student%20Guide%20Book%20c2bc1a5fa6cd474d81a2158c4ab088a7/Untitled%204.png)

End Device = Host

OSI, TCP/IP 

![Untitled](Student%20Guide%20Book%20c2bc1a5fa6cd474d81a2158c4ab088a7/Untitled%205.png)

OSI 7 layers

![Untitled](Student%20Guide%20Book%20c2bc1a5fa6cd474d81a2158c4ab088a7/Untitled%206.png)

TCP/IP 

![Untitled](Student%20Guide%20Book%20c2bc1a5fa6cd474d81a2158c4ab088a7/Untitled%207.png)

### Protocol

ARP: Address Resolution Protocol

IP: Network Layer
Mac: Data Link Layer

IP-Mac đi với nhau (IP-MAC)

ARP broadcast MAC: ff:ff:ff … 48 bit - 12 chữ f

RARP: phản hồi gửi lại ARP có địa chỉ mac

DHCP:

Cung cấp IP động

Cấp các trường dhcp option —> TFTP server ở đâu, …

Default gateway:

Mạng LAN thì không cần gateway

Đi ra ngoài internet —> cấu hình ip gateway

DNS server

Bit

Frame

Package

## Subnets

Single broadcast domain

Việc mở rộng nhiều thiết bị —> bản tin arp làm tắc nghẽn đường truyền

⇒ Có vấn đề cho việc mở rộng

Subnet work: Class A dành cho mạng lướn

class B dành cho mạng vừa

class C dành cho người dùng

Chia network thành các subnet work —> kết nối các subnetwork bằng router

⇒ Có các miền broadcast domain ứng với các subnetnetwork

### Đặc điểm subnet mark:

255.255.0.1 or /16  

16 bit 1 và 16 bit sau = 0

local là cùng 1 mạng → dùng phương thức local

remote là thông qua router → cần thông qua router 

Làm sao biết ip address là local or remote?

10.1.1.1/24  —> 10.1.0.2

VLSM:

# 11/7/2024 - buổi

Static NAT và PAT

NAT dynamic không còn được dùng nhiều nữa

Khi khai báo cổng trunk thường phải khai báo cấu hình native VLAN

Native VLAN:

Thêm trường thông tin chỗ môi frame khi gửi qua switcb —> đường trunking

Chuẩn để thêm các trường tên vào là chuẩn 802.1Q

![Untitled](Student%20Guide%20Book%20c2bc1a5fa6cd474d81a2158c4ab088a7/Untitled%208.png)

Native Vlan là khi gửi qua trunk thì nó ẩn tag

Native VLAN là VLAN1

Do máy chủ quản lý không đọc được tag nên VLAN1 cần không tag, và khi truy cập vào VLAN1 là có thể truy cập vào mọi VLAN khác.

Dynamic Trunk Protocol

Giao thức trunk động

![Untitled](Student%20Guide%20Book%20c2bc1a5fa6cd474d81a2158c4ab088a7/Untitled%209.png)

VLAN Trungking Protocol: 

Guari các link, các game,

VTP domains