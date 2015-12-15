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

#III
