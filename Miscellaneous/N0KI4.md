# Mô tả
23tmln tải về vé đại hải trình thì thấy có thêm một bức ảnh đáng ngờ, hãy tìm thứ ẩn sau đó giúp 23tmln nhé!<br>
[im4g3.jpg](https://minictf.infosecptit.club/files/7901ee0a33dcac8e03a1086dfc8dd0ea/im4g3.jpg?token=eyJ1c2VyX2lkIjo2OCwidGVhbV9pZCI6bnVsbCwiZmlsZV9pZCI6Mzd9.ZuKrOQ.SVG_5V_vNZ8l-hxotmzGtpYE4fY)
# Cách giải
Sử dụng ```binwalk``` để khảo sát file ```im4g3.jpg```:
![im4g3.jpg binwalk](https://i.imgur.com/NxsbIBp.png)<br> <br>
Ta nhận thấy trong hình ảnh có file ```rar```.<br>
Tiếp tục sử dụng ```binwalk``` để extract file ```rar``` trong ```im4g3.jpg```:
![extract](https://i.imgur.com/0WMPxcy.png)<br> <br>
Ta thực hiện đổi đuôi file vừa extract sang ```.rar```<br>
Khi giải nén file vừa thu được, ta bị yêu cầu nhập mật khẩu giải nén:
![password to extract](https://i.imgur.com/Ig73zKL.png)<br> <br>
Sử dụng [Zip Password Recovery](https://www.lostmypass.com/file-types/zip/) của website LostMyPass, ta tìm được mật khẩu giải nén là ```123456```
![password recorvery](https://i.imgur.com/5VTsiRY.png)<br> <br>
Ta thấy một file ```flag.txt```:<br>
![flag.txt](https://i.imgur.com/hLcmBvZ.png)<br> <br>
Tuy nhiên ta vẫn chưa lấy được flag, khi mở file ta được thông điệp sau:
```text
miniCTF{#66#_666_55_444_2_#6#_666_8_#44#_2_444_#8#_2_6_#55#_44_666_66_4}
bên trong flag có vẻ không đúng lắm,hãy tìm cách giải mã xem
```
Ta có thể dễ thấy đây là cách nhấn trên bàn phím của bàn phím điện thoại Nokia (hint ở đề bài).<br>
Như vậy, ta sẽ xem với những phím được bấm này, sẽ cho ra những chữ cái nào.<br>
![nokia keypad](https://i.imgur.com/icvRIU0.png)<br> <br>
Như vậy, ta sẽ suy ra được thông điệp trong dấu ```{}``` là ```NokiaMotHaiTamKhong```<br> <br>
Flag: ```miniCTF{NokiaMotHaiTamKhong}```
