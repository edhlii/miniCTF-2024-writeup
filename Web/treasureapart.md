# Mô tả
Kho báu hay thứ mà các người gọi là flag, bị ta giấu ở đâu đó trong cái web này, dễ thôi, đừng ấn vào link lạ nhé....<br>
http://msw2.kesug.com/
# Cách giải
Ta thực hiện Inspect trang web, nhìn vào đoạn code HTML, dòng số 39, ta được phần cuối của flag<br>
```html
<!-- Html is neat. But the flag is somewhere else, just 1 part here : hjdd3n_4p4rt}, try to find others! (>.o)-->
```
Tiếp theo ta xem xét code javascript của trang web, ở dòng cuối ta nhận được phần 2 của flag<br>
```js
/* Javascript is like treasure's owner. Anyways the second part of the treasure is here: r3_m4ps_4r3_ */
```
Cuối cùng ta xem code CSS của trang web, ta sẽ thu thập được phần đầu của flag<br>
```css
/* You need CSS to draw pretty maps. Here's first part of the treasure: miniCTF{tr34su */
```
Như vậy, ghép 3 phần tìm được, ta sẽ có flag<br>
Flag: ```miniCTF{tr34sur3_m4ps_4r3_hjdd3n_4p4rt}```
