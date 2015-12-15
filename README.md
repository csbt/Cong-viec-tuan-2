#I. VMware Workstation - ubuntu 15.10
<a href="http://imgur.com/lIPGbTW"><img src="http://i.imgur.com/lIPGbTW.png" title="source: imgur.com" /></a>
#II. Cách sử dụng trình soạn thảo Vi
VI có 2 chế độ là command và insert :

**>>>>>>>>>>>> CHÚ Ý: PHÂN BIỆT CHỮ THƯỜNG VÀ CHỮ IN HOA <<<<<<<<<<<<<**
##1. Để chuyển sang chế độ command (đang ở chế độ insert) : ấn phím ESC
- Để hiển thị số dòng gõ lệnh **:set nu**
- **<SHIFT> + J** : để gộp 2 dòng
- **<CTRL> + D** : để xuống nửa trang
- **<CTRL> + U** : để lên nửa trang
- **<CTRL> + F** : để xuống 1 trang
- **<CTRL> + B** : để lên 1 trang

###1.1 Các lệnh với con trỏ
Di chuyển con trỏ bằng phím mũi tên hoặc các phím:
  + **h** : sang trái 1 kí tự
  + **l** : sang phải 1 kí tự
  + **w** : sang phải 1 từ
  + **b** : sang trái 1 từ
  + **k** : lên 1 dòng
  + **j** : xuống 1 dòng
  + **:số dòng** : để chuyển con trỏ về đầu dòng đó.

      VD:   **:20** con trỏ sẽ xuất hiện ở đầu dòng 20
  + **0 ( phím số 0)** : để đưa con trỏ về đầu dòng
  + **$ ( SHIFT + 4**  : để đưa con trỏ về cuối dòng
  + **H** : đưa con trỏ về kí tự đầu tiên của dòng đầu tiên trong màn hình hiện tại
  + **L** : đưa con trỏ về kí tự đầu tiên của dòng cuối cùng trong màn hình hiện tại
  + **M** : đưa con trỏ về kí tự đầu tiên của dòng giữa trong màn hình hiện tại

###1.2 Các lệnh xóa kí tự
- **x**   : để xóa kí tự hiện tại
- **X**   : để xóa kí tự phía trước
- **dw**  : để xóa 1 từ
- **dd**  : để xóa 1 dòng
- **cw**  : để xóa 1 từ đồng thời chuyển sang chế độ *Insert*
- **cc**  : để xóa 1 dòng đồng thời chuyển sang chế độ *Insert*
- **d^**  : để xóa kí tự từ bên trái con trỏ đến đầu dòng
- **d$**  : để xóa kí tự từ bên phải con trỏ đến cuối dòng
- **nx**  : để xóa  kí tự hiện tại và n-1 kí tự bên phải kí tự hiện tại

    VD : **2x** : xóa 2 kí tự
- **ndd** : để xóa dòng hiện tại và n-1 dòng bên dưới dòng hiện tại
 
    VD : **2dd** : xóa 2 dòng

###1.3 Các lệnh tìm kiếm
- **?** : tìm ngược trở lên
- **/** : tìm xuôi

###1.4 Các lệnh thay thế
- **:ab abcd lenh thay the** : thay thế *abcd* bằng *lenh thay the* khi ở chế độ Insert 
- **:s/text1/text2/g** :  thay thế text1 bằng text2 : :%s/text/text2/g
- 

###1.5 Một số lệnh khác
- **v** : để bắt đầu bôi đen
- **.** : tiếp tục thực hiện lệnh trước đó
- **u** : undo
- **y** : để coppy
- **yy** or **Y* : để coppy 1 dòng
- **p** : để paste
- **nyy** or **nY** : để coppy dòng hiện tại và n-1 dòng bên dưới dòng hiện tại

   VD : **2yy** coppy 2 dòng
- gõ lệnh **:1,4t 9** : để coppy từ dòng 1 đến dòng 4 và paste vào dòng 9

###1.6 Thao tác với tập tin
- **:w** :  lưu văn bản với tên mặc định
- **:w newfile.txt** : để save nội dung của file hiện tại vào một file mới là newfile.txt ( tựa “save as” bên Win Word )
- **:x** : lưu và thoát khỏi chế độ soạn thảo
- **:q!** : thoát không lưu
- Nếu dùng vi để mở nhiều file ( vi file1 file2 file3 )
  + **:n#** : để nhảy đến file tiếp theo
  + **:n vi2** : để nhảy tới file 'vi2'
  + **:rew** : để nhảy ngược lại

##2. Để chuyển sang chế độ insert (đang ở chế độ command) : ấn các phím:
  + **a** : con trỏ xuất hiện sau kí tự hiện tại
  + **A** : con trỏ xuất hiện cuối dòng
  + **i** : con trỏ xuất hiện trước kí tự hiện tại
  + **I** : con trỏ xuất hiện đầu dòng
  + **o** : thêm một dòng bên dưới và cho phép nhập kí tự vào
  + **O** : thêm một dòng bên trên và cho phép nhập kí tự vào

#III. Các chế độ của card mạng trên máy ảo:

* **Chế độ Bridge**: ở chế độ này thì card mạng trên máy ảo sẽ được gắn vào VMnet0 và VMnet0 này liên kết trực tiếp với card mạng vật lý. Ở chế độ này máy ảo sẽ kết nối internet thông qua lớp card mạng vật lý và có chung lớp mạng với card mạng vật lý.

* **Chế độ NAT**: ở chế độ này thì card mạng của máy ảo kết nối với VMnet8, VNnet8 cho phép máy ảo đi internet thông qua cơ chế NAT (NAT device).

	Lúc này lớp mạng bên trong máy ảo khác hoàn toàn với lớp mạng của card vật lý bên ngoài. IP của card mạng sẽ được cấp bởi DHCP VMnet8 cấp, trong trường hợp bạn muốn thiết lập IP tĩnh cho card mạng máy ảo bạn phải đảm bảo chung lớp mạng với VNnet8 thì máy ảo mới có thể đi internet.

* **Cơ chế Host-only**: ở cơ chế này máy ảo được kết nối với VMnet có tính có tính năng Host-only, trong trường hợp này là VMnet1 (bạn có thể add nhiều VMnet Host-only). VMnet Host-only kết nối ra một card mạng ảo tương ứng ngoài máy thật.

	Ở chế độ này máy ảo không có kết nối internet. IP của máy ảo được cấp bởi DHCP của VMnet tương ứng.Trong nhiều trường hợp đặc biệt cần cấu hình riêng, ta có thể tắt DHCP trên VMnet và cấu hình IP bằng tay cho máy ảo.

#IV. Một số lệnh cấu hình Network trên Ubuntu

##1. Các câu lệnh kiểm tra thông tin mạng trong Ubuntu

- **ifconfig -a** : Kiểm tra cấu hình các card mạng

- **hostname** :  xem hostname 

- **grep eth & ifconfig** : Xem thông tin cấu hình các card mạng (MAC, địa chỉ IP, gateway..)  của tất cả các card mạng trong máy (tương tự lệnh ipconfig của Windows)
  
- **route -n** :Kiểm tra đường đi của gói tin (tương tự lệnh route trong Windows).
 
##2. Các câu lệnh cấu hình mạng trong Ubuntu

- **/etc/init.d/networking restart** : Restart Network Interface
- **vi /etc/network/interfaces** : Thiết lập file cấu hình mạng trong Ubuntu
- **route add default gw 192.168.1.1** : Đặt địa chỉ IP 192.168.1.1 làm default gateway trong Ubuntu.
- **route delete default gw 192.168.1.1** : Xóa địa chỉ default gateway 192.168.1.1
- **route add -net 192.168.5.0 mask 255.255.255.0 dev eth0** : Để add một routing tĩnh đến mạng (cho card mạng eth0). Ngược lại với add ta dùng lệnh delete.

#V. Phân tích gói tin IP datagram
<a href="http://imgur.com/ssKaKx6"><img src="http://i.imgur.com/ssKaKx6.png" title="source: imgur.com" /></a>

- **Version** (4 bit): chỉ phiên bản (version) hiện hành của IP được cài đặt.
- **IHL**: Internet header length (4 bit): chỉ độ dài phần header tính theo đơn vị từ (word - 32 bit).
- **Type of Service** (8 bit): đặc tả tham số về yêu cầu dịch vụ: Thông tin về loại dịch vụ và mức ưu tiên của gói IP.
	+ **Precedence** (3 bits): chỉ thị về quyền ưu tiên gửi datagram:
		. 111 Network Control (cao nhất)

		. 011- flash
		
		. 110 Internetwork Control
		
		. 010 Immediate
		
		. 101 CRITIC/ECP
		
		. 001 Priority
		
		. 100 Flas Override
		
		. 000 Routine (thấp nhất)
	+ **D (delay)** (1 bit) : chỉ độ trễ yêu cầu

		. D = 0 độ trễ bình thường
		
		. D = 1 độ trễ thấp
	  
