# Challenge
23tmln đã tìm thấy một kho báu,mở ra thì thấy tờ giấy viết một đoạn mã kì lạ,nội dung của nó là gì nhỉ?<br>
[sixtifor.txt](https://minictf.infosecptit.club/files/8d24eb26c6cda7b2ad3fb2372b2be5f7/sixtifor.txt?token=eyJ1c2VyX2lkIjo2OCwidGVhbV9pZCI6bnVsbCwiZmlsZV9pZCI6NDR9.ZuE2Rw.VdW9z1Bq1hsPyc8-zbMUQ4vn5Mg)
# Solution
Tên của file đã gợi ý rằng file đã được mã hóa base64, ta sử dụng CyberChef để giải mã base64.<br>
Tuy nhiên, sau khi giải mã lần đầu tiên, ta vẫn thu được chuỗi ngẫu nhiên thiếu ý nghĩa, ta cần<br>
lấy output và tiếp tục giải mã base64 tiếp. Sau 10 lần, ta sẽ thu được flag.<br>
![sixtifor decrypt](https://i.imgur.com/neAn9py.png)<br>
Flag: ```miniCTF{!_l0v3_cryp10_f0r3v3r}```
