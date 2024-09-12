# Mô tả
Có lẽ định dạng file đã bị đổi, hãy đi tìm định dạng file gốc. Good luck!<br>
[kho_bau.exe](https://minictf.infosecptit.club/files/19921e6e216888305fa27a432c09b6c4/kho_bau.exe?token=eyJ1c2VyX2lkIjo2OCwidGVhbV9pZCI6bnVsbCwiZmlsZV9pZCI6NDB9.ZuJCBg.PNwxsbMg8n_r4WyMd16xpVqOSQw)
# Cách giải
Sử dụng lệnh ```file``` trên linux:
```console
$ file kho_bau.exe
```
Ta sẽ thấy định dạng ban đầu của file.
```console
kho_bau.exe: JPEG image data, JFIF standard 1.01, aspect ratio, density 1x1, segment length 16, baseline, precision 8, 4000x2666, components 3
```
Ta thực hiện chuyển đuôi file từ ```.exe``` sang ```jpeg```, mở hình ảnh lên và ta sẽ thấy flag:
![flag](https://i.imgur.com/wdOBwZy.jpeg)
Flag: ```miniCTF{hop_kho_bau_tri_thuc}```
