# Mô tả
Trong một chuyến hành trình lênh đênh trên biển, thủy thủ đoàn đã bắt gặp một file .zip kỳ lạ trôi nổi giữa đại dương. Nhưng thật kỳ lạ, khi mở file này ra, họ phát hiện rằng nó dường như giống một bức thư hay một đoạn văn bí ẩn hơn là một file nén thông thường. Không rõ nguồn gốc hay mục đích của nó, nhưng chắc chắn bên trong chứa đựng một bí ẩn cần được giải mã. Liệu bạn có thể giúp thủy thủ đoàn khám phá bí mật ẩn giấu trong file này và tìm ra thông điệp mà nó mang theo?<br>
[findme.zip](https://minictf.infosecptit.club/files/798916a01f28f9d267f0bf226e0d08c5/findme.zip?token=eyJ1c2VyX2lkIjo2OCwidGVhbV9pZCI6bnVsbCwiZmlsZV9pZCI6MzZ9.ZuKnxQ.YuvQN7qLMV_JqWxiWwDpeqZ_2nY)
# Cách giải
Giải nén file ```findme.zip```, sau đó dùng lệnh ```grep``` để tìm string ```miniCTF``` trong toàn bộ folder.<br>
```console
$ grep -rni miniCTF *
```
Ta sẽ thấy string ```miniCTF``` được bôi đỏ:
![grep](https://i.imgur.com/wsCLvFW.png)<br> <br>
Giờ ta chỉ cần lấy các kí tự ra là có được flag.<br>
Flag: ```miniCTF{WHY_Y0U_C4N_D0_TH4T_??}```
