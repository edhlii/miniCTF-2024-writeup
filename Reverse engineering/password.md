# Mô tả
File treasure.exe được tạo ra dựa trên file chall2.py. Bạn<br>
có thể tìm được mật khẩu của kho báu ở bên trong file<br>
chall2.py. Good luck!<br>
[password.zip](https://minictf.infosecptit.club/files/3c21c2983d6f2dd8965b49caf6a102a7/password.zip?token=eyJ1c2VyX2lkIjo2OCwidGVhbV9pZCI6bnVsbCwiZmlsZV9pZCI6Mzl9.ZuBXHA._3q8IdxGYQNXpzm7znol7q66Q44)
# Cách giải
Mở file source code ```chall2.py```, tại đây ta sẽ biết cách để tìm được mật khẩu để chạy file ```treasure.exe```.<br>
```python
import time


pw = ["I", "S", "P"]
flag = open('file.txt')

print("Hãy nhập mật khẩu để mở kho báu!\n    (Mật khẩu gồm 6 chữ số)\n")
inp = input("Mật khẩu của bạn là: ")
while (len(inp) < 6 or len(inp) > 6):
    inp = input("Mật khẩu có 6 chữ số, hãy nhập lại: ")

count = 0
for i in range(3):
    if (int(inp[ 2 * i : 2 * i + 2 ]) == ord(pw[i])):
        count += 1

if (count == 3):
    print(flag.read())
else:
    print("LOADING!");
    time.sleep(5)
    print("Wait a minute!")
    time.sleep(5)
    print("Mật khẩu sai!!!")

flag.close()
input("\nẤn Enter để thoát!")
```
List ```pw``` được khởi tạo với 3 phần tử là các chữ cái I, S, P. Và mật khẩu có 6 kí tự.<br>
Nhìn vào dòng 12 đến 15. Ta cần nhập mật khẩu để biến ```count``` đếm tới 3 để in ra flag.<br>
Trong vòng lặp ```for```, điều kiện để biến ```count``` tăng là cứ 2 chữ số một sẽ phải bằng<br>
giá trị ASCII của từng phần tử trong list ```pw```, lần lượt ta có ```I = 73, S = 83, P = 80```, như vậy mật khẩu là ```738380```.<br>
Nhập mật khẩu này khi chạy ```treasure.exe```, ta sẽ có được flag.<br>

Flag: ```miniCTF{d4y_L4_kH0_l34u_cU4_Chl3c_Ru0n5_N4y}```
