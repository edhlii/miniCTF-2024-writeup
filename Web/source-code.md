# Mô tả
Một flag bí mật đang ẩn nấp đâu đó trong trang web này, và nhiệm vụ của bạn là lùng sục mã nguồn để tìm nó!<br>
[Trang web của tôi](http://www.minictf.kesug.com/index.html?i=2)
# Cách giải
Inspect trang web, xem đoạn code HTML, ta sẽ tìm thấy flag ở dòng 106:
```html
<p>Cờ của bạn là: miniCTF{this_is_a_secret_flag}</p>
```
Flag: ```miniCTF{this_is_a_secret_flag}```
