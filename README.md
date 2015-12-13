#VMware Workstation - ubuntu 15.10
<a href="http://imgur.com/lIPGbTW"><img src="http://i.imgur.com/lIPGbTW.png" title="source: imgur.com" /></a>
#Cách sử dụng trình soạn thảo Vi
VI có 2 chế độ là command và insert :

**>>>>>>>>>>>> CHÚ Ý: PHÂN BIỆT CHỮ THƯỜNG VÀ CHỮ IN HOA <<<<<<<<<<<<<**
##Để chuyển sang chế độ command (đang ở chế độ insert) : ấn phím ESC
- Để hiển thị số dòng gõ lệnh **:set nu**
- **<SHIFT> + J** : để gộp 2 dòng
- **<CTRL> + D** : để xuống nửa trang
- **<CTRL> + U** : để lên nửa trang
- **<CTRL> + F** : để xuống 1 trang
- **<CTRL> + B** : để lên 1 trang
###Các lệnh với con trỏ
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

###Các lệnh xóa kí tự
- **x**    : để xóa kí tự hiện tại
- **X**    : để xóa kí tự phía trước
- **dw**   : để xóa 1 từ
- **dd**   : để xóa 1 dòng
- **cw**   : để xóa 1 từ đồng thời chuyển sang chế độ *Insert*
- **cc**   : để xóa 1 dòng đồng thời chuyển sang chế độ *Insert*
- **d^**   : để xóa kí tự từ bên trái con trỏ đến đầu dòng
- **d$**   : để xóa kí tự từ bên phải con trỏ đến cuối dòng
- **nx**   : để xóa  kí tự hiện tại và n-1 kí tự bên phải kí tự hiện tại

    VD : **2x** : xóa 2 kí tự
- **ndd*** : để xóa dòng hiện tại và n-1 dòng bên dưới dòng hiện tại
 
    VD: **2đ** : xóa 2 dòng
- **v** bắt đầu bôi đen

##Để chuyển sang chế độ insert (đang ở chế độ command) : ấn các phím:
  + **a** : con trỏ xuất hiện sau kí tự hiện tại
  + **A** : con trỏ xuất hiện cuối dòng
  + **i** : con trỏ xuất hiện trước kí tự hiện tại
  + **I** : con trỏ xuất hiện đầu dòng
  + **o** : thêm một dòng bên dưới và cho phép nhập kí tự vào
  + **O** : thêm một dòng bên trên và cho phép nhập kí tự vào

