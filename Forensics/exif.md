# Mô tả
Chiếc rương kho báu này ẩn chứa điều gì cơ?<br>
[ggwp.jpg](https://minictf.infosecptit.club/files/e056a2c3302d465b1d703cce5a20f7c6/ggwp.jpg?token=eyJ1c2VyX2lkIjo2OCwidGVhbV9pZCI6bnVsbCwiZmlsZV9pZCI6NTF9.ZuKc_Q.KCRTyvFBXIXninPoh5wX1xJ6PsI)
# Cách giải
Sử dụng tool ```exiftool``` trên linux terminal.<br>
```console
$ exiftool ggwp.jpg
```
Output trả ra như sau:
![output](https://i.imgur.com/8T6kSVt.png)
Flag đã được tìm thấy ở ```XP Comment``` và ```Comment```<br><br>
Flag: ```miniCTF{G00d_game_w3ll_play3r}```
