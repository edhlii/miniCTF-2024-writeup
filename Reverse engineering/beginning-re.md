# Mô tả
Đây là bước khởi đầu trong công cuộc dịch ngược, bạn hãy thử xem.<br>
[chall1.cpp](https://minictf.infosecptit.club/files/5c40d799760b9402c15210359e85b8d2/chall1.cpp?token=eyJ1c2VyX2lkIjo2OCwidGVhbV9pZCI6bnVsbCwiZmlsZV9pZCI6Mzh9.ZuBVMQ.7-iUw-ILPy9eCDmu5QYwNrUtNKk)
# Cách giải
Đọc source code, ta nhận thấy string ```flag``` đã bị xáo trộn trong câu lệnh điều kiện:
```cpp
if (flag.size() == 35 &&
        flag[1] == 'i' &&
        flag[10] == 'v' &&
        flag[12] == 'r' &&
        flag[32] == 'g' &&
        flag[14] == '3' &&
        flag[16] == '1' &&
        flag[22] == 'y' &&
        flag[31] == '_' &&
        flag[17] == 's' &&
        flag[9] == '3' &&
        flag[15] == '_' &&
        flag[33] == '0' &&
        flag[11] == 'e' &&
        flag[8] == 'R' &&
        flag[34] == '}' &&
        flag[27] == '3' &&
        flag[24] == 'h' &&
        flag[21] == 's' &&
        flag[0] == 'm' &&
        flag[29] == 'w' &&
        flag[4] == 'C' &&
        flag[3] == 'i' &&
        flag[23] == '_' &&
        flag[30] == '3' &&
        flag[19] == 'e' &&
        flag[13] == 's' &&
        flag[2] == 'n' &&
        flag[7] == '{' &&
        flag[28] == '_' &&
        flag[20] == '4' &&
        flag[18] == '_' &&
        flag[6] == 'F' &&
        flag[5] == 'T' &&
        flag[25] == '3' &&
        flag[26] == 'r')
```
Sắp xếp lại theo đúng thứ tự, ta nhận được flag.<br>
Flag: ```miniCTF{R3vers3_1s_e4sy_h3r3_w3_g0}```
