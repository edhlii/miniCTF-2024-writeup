# Mô tả
Trên một hòn đảo hoang vu, giữa những đống vàng bạc châu báu, một tên cướp biển đã phát hiện ra một chiếc hộp bí ẩn. Chiếc hộp này không giống bất kỳ thứ gì họ từng thấy. Được chạm khắc tinh xảo với những ký tự cổ xưa và những biểu tượng kỳ lạ, chiếc hộp dường như được mã hóa một cách tinh vi.
Mỗi khi có ai đó cố gắng mở nó, các con chữ bắt đầu được phản chiếu ra từ chiếc hộp mang theo những câu hỏi, như thể chiếc hộp có suy nghĩ riêng của nó vậy. Những lời đồn đại bắt đầu lan truyền khắp tàu, rằng bên trong chiếc hộp chứa đựng một bí mật liên quan tới cái chết của chủ nhân kho báu. Nhưng để giải mã được chiếc hộp này, cần phải có trí tuệ và sự kiên trì tìm ra nguyên lí và phá giải bí ẩn này.
Hãy tự mình tìm ra chân tướng của sự việc! ___.
[Let_him_cook.cpp](https://minictf.infosecptit.club/files/4fa2ffea0941017197bfae8897c259b0/Let_him_cook.cpp?token=eyJ1c2VyX2lkIjo2OCwidGVhbV9pZCI6bnVsbCwiZmlsZV9pZCI6NDl9.ZuDP6g.pjdYwYnEt5g1GF-XqUH3vP-9dE0)
# Cách giải
Khi chạy chương trình, ta được yêu cầu nhập 3 lựa chọn 1, 2, 3 để lấy ra flag.<br>
Mở file source ```Let_him_cook.cpp```<br>
```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll long long
int Mmm = 0;
string Flag = "Z./oeS{6teFteZN:zetN'k{eznrZeee"; 
void print_Flag(string encryptedText, int key){
	string result = ""; 
	for (char c : encryptedText) {
        int charCode = int(c);
        charCode = charCode - (key % 10);
        result += char(charCode);
    }
    cout <<  "miniCTF{" << result << "}";
}

void the_truth(ll &n){
	cout << "I'll show you the truth!\n54 68 65 20 6B 65 79 20 69 73 20 61 20 70 65 72 66 65 63 74 20 6E 75 6D 62 65 72 20 6C 65 73 73 20 74 68 61 6E 20 31 36 20 62 69 74 73 2E \nConvert to text. It may help you!";
	cout << "\nYou can take a hint!"; // hint decypt tu hex sang text
	cout << "Do you want to know more? \n1. Yes  2. No" << endl;
	int t; cin >> t;
	if(t==1){
		cout << "Time Nam :)))";
		n = 0;
	} else if(t == 2){
		cout << "Choose the number 2 and the Flag is your!";
		n = 0;
	}
	Mmm++; 
}

int unlock(){
	return 1;
}

int guess_what(ll &n){
	cout << "You are wrong! Try again? \n1. Yes  2. No  3. Hmmmm\n";
	int t; cin >> t;
	if(t == 1){
		guess_what(n);
	} else if(t == 2){
		n = 0;
	} else if(t == 3){
		the_truth(n);
	}
} 

void Something_wrong(ll &n){
	cout << "Enter the password to get the Flag: ";
	ll key;
	cin >> key;
	print_Flag (Flag, key);
	if (Mmm != 0){
		cout << "Try again! Please read the information in option 3 carefully.";
	}
}
void input(){
	cout << "Choose your number: 1 2 3" << endl;
	ll n = 100000000;
	while(n > 0){
		cin >> n;
		if(n == 1){
			guess_what(n);
		} else if(n == 3){
			the_truth(n);
		} else if(n == 2){
			Something_wrong(n);
		} else {
			cout << "Invalid Value.\n" ;
		} 
		if (n == 0){
			break;
		} 
	} 
}


int main(){  
	if(unlock()) input();
	else {
		cout << "Program is locked.";
	}
	return 0;
} 
```
Ta thấy hàm ```the_truth()``` mang nhiều thông tin quan trọng. Ta sẽ thực hiện chuyển đổi<br>
mã HEX ở dòng 17 thành chữ, ta nhận được thông điệp ```The key is a perfect number less than 16 bits.```.<br>
Và ở dòng 24, 25 ta biết được rằng nhập lựa chọn 2 sẽ in ra flag.<br>
Chạy chương trình, nhập lựa chọn 2, ta được yêu cầu nhập một mật khẩu.<br>
Như hint đã được đưa ra ở trên, mật khẩu là một số hoàn hảo nhỏ hơn 16 bits.<br>
```Số hoàn hảo là số có tổng các ước số (trừ chính nó) bằng chính số đó```<br>
Như vậy ta thử điền số hoàn hảo bé nhất, số 6, và ta nhận được flag.<br>

Flag: ```miniCTF{T()i_Mu0n_@n_TH4t_nH!eu_thlT___}```
