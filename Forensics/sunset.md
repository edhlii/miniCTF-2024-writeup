# Mô tả
Điểm cuối cùng của hoàng hôn là gì ?<br>
[sunset.jpg](https://minictf.infosecptit.club/files/ab178fd8610b7777257c8379bb2738ee/sunset.jpg?token=eyJ1c2VyX2lkIjo2OCwidGVhbV9pZCI6bnVsbCwiZmlsZV9pZCI6NDJ9.ZuKe2A.h5pkkqVU63jCjlL3efZjdIxH-Q4)
# Cách giải
Khi mở ra thì ta chỉ thấy một bức ảnh hoàng hôn bình thường.<br>
Sử dụng ```binwalk```, ta nhận thấy trong bức ảnh chứa một file rar<br>
![binwalk file](https://i.imgur.com/wYa67hJ.png)<br> <br>
Thực hiện extract file rar trong bức ảnh bằng ```binwalk```, đồng thời đổi tên cho file được extract có đuôi ```.rar``` <br>
![binwalk extract](https://i.imgur.com/xHBZFEW.png)<br> <br>
Ta nhận được thêm file ```sun2.jpg```, điều đặc biệt là file này cũng chứa một file ```rar``` trong đó
![sun2 binwalk](https://i.imgur.com/Ak6k9nx.png)<br> <br>
Tiếp tục extract file rar trong bức ảnh, và làm tương tự như trên, ta thu được ```sun3.jpg```. Tiếp tục làm tương<br>
tự như với 2 file trên với file ```sun3.jpg```, lần này ta sẽ thấy file ```flag.txt```
![flag.txt](https://i.imgur.com/li1d1mz.png)<br> <br>
Flag: ```miniCTF{I_LOVE_PTIT}```
