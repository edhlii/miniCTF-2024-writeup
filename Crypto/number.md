# Mô tả
Bạn có thể giải mã thông điệp này không ?<br>
[ciphertext.txt](https://minictf.infosecptit.club/files/df68f38930ad9b88f54b25ee5cc950ce/ciphertext.txt?token=eyJ1c2VyX2lkIjo2OCwidGVhbV9pZCI6bnVsbCwiZmlsZV9pZCI6NTN9.ZuE82g.Q450i2m34kiRht_jgjRmKye4aGk)
# Cách giải
Sử dụng CyberChef, chuyển đổi từ Decimal, ta được: ```oJyhnHAHEagWH1OsD2k1La0=```<br>
Nhận thấy đây là phương pháp mã hóa base64.<br>
Tiếp tục chuyển đổi đoạn mã vừa nhận từ base64, ta thu được flag.<br>
![number decrypt](https://i.imgur.com/PHmEVG9.png)
Flag: ```miniCTF{ISP_Club}```
