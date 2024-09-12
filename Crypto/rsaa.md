# Challenge
Chúng tôi có một siêu máy tính đang hoạt động, vì vậy tôi mã hóa thông tin của mình bằng cách chọn những con số lớn!<br>
[output.txt](https://minictf.infosecptit.club/files/ba54ba30d4102d91f15535f9e9b51588/output.txt?token=eyJ1c2VyX2lkIjo2OCwidGVhbV9pZCI6bnVsbCwiZmlsZV9pZCI6NDZ9.ZuIoiQ.QM2_1H8YPOhNnRNbhLYGQWMh0Qc)
[source.py](https://minictf.infosecptit.club/files/f429594675a78d7e51ee8a84fddd5b74/source.py?token=eyJ1c2VyX2lkIjo2OCwidGVhbV9pZCI6bnVsbCwiZmlsZV9pZCI6NDd9.ZuIoiQ.BsZMlXAEIzuo0X4CYDuzulNydh8)
# Solution
Mở file ```source.py```, ta thấy đoạn mã python mã hóa flag bằng phương pháp [RSA](https://vi.wikipedia.org/wiki/RSA_(m%C3%A3_h%C3%B3a))<br>
Mở file ```output.txt```, ta nhận được thông tin về các biến số ```n```, ```e```, ```c``` dùng để mã hóa.<br>
<br>
Để phục hồi flag ban đầu từ các giá trị ```n```, ```c```, ```e```, ta cần tìm ```private key d```.<br>
Ta lần lượt làm theo các bước để decrypt flag.<br>
### Bước 1: Tìm ước số p, q của n
Ta cần tìm ước số ```p``` và ```q``` đã được sử dụng để sinh ra ```n```.<br>
Sử dụng [factordb](factordb.com), ta dễ dàng tìm ra giá trị ```p```, ```q```.<br>
![factors of n](https://i.imgur.com/6dE0aAH.png)<br>
### Bước 2: Decrypt flag
Sử dụng [RSA Cipher](https://www.dcode.fr/rsa-cipher), nhập các thông số về ```n```, ```c```, ```e```, ```p```, ```q``` đã biết để decrypt flag.<br>
![flag](https://i.imgur.com/Q0up00i.png)
<br><br>
Flag: ```miniCTF{f3rm47_w45_4_g3n1u5}```
