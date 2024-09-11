# Mô tả
Luffy tìm thấy 1 trang web, do tính tò mò nên anh ta đã vào thử nhưng không thấy gì. Bạn hãy giúp Luffy tìm flag nhá<br>
[hidden](http://103.70.115.44:1234/)
# Cách giải
Khi vào trang web ta sẽ thấy một form Sign in, tại đây ta điền tài khoản và mật khẩu bất kì.<br>
![Sign in page](https://i.imgur.com/TYsWYUn.png)<br>
Sau đó ta sẽ được đưa đến một trang web toàn màu vàng, xem đoạn code HTML ta sẽ lấy được phần đầu flag<br>
ở dòng 17.<br>
```html
<i>miniCTF{N0w_</i>
```
Quay lại trang chính, ta chọn mục ```Sign up```, ta sẽ được đưa đến trang đăng ký tài khoàn.<br>
Inspect trang web, tìm tới file ```register.css```, kéo xuống dòng cuối cùng ta thấy một đoạn<br>
mã hóa base64<br>
![base4](https://i.imgur.com/StQGIZy.png)<br>
Giải mã đoạn mã, ta thu được phần 2 của flag: ```u_c4n_```<br>
Quay trở lại trang chính, lần này ta chọn vào ```Forgot password```, ta sẽ được đưa tới trang đổi mật khẩu.<br>
Đọc file ```forgotpass.css```, ở dòng cuối ta thấy một dãy số lạ:
```html
/* 2340510522183513221474498965418877 */
```
Chuyển dãy số này sang chữ bằng [kt.gy](kt.gy), ta thu được phần cuối cùng của flag: ```see_m3_h3h3h3}```<br>
Flag: ```miniCTF{N0w_u_c4n_see_m3_h3h3h3}```
