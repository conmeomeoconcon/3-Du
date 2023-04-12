# XOR Properties
![image](https://user-images.githubusercontent.com/128831586/231449686-f7fead19-80b6-4518-aade-19ebf31dfbb5.png)
-	Ở challenge này sẻ giúp các bạn làm rỏ hơn về tính chất của XOR.
-	Có bốn tính chất chính mà chúng ta nên xem xét khi giải quyết các thách thức bằng cách sử dụng toán tử XOR
		+	Tính giao hoán: A^B=B^A
		+	Tính kết hợp: A^(B^C)=(A^B)^C
		+	tính đơn vị: A^0=A
		+	Tính bù trừ: A^A=0
KEY1 = a6c8b6733c9b22de7bc0253266a3867df55acde8635e19c73313
KEY2 ^ KEY1 = 37dcb292030faa90d07eec17e3b1c6d8daf94c35d4c9191a5e1e
KEY2 ^ KEY3 = c1545756687e7573db23aa1c3452a098b71a7fbf0fddddde5fc1
FLAG ^ KEY1 ^ KEY3 ^ KEY2 = 04ee9855208a2cd59091d04767ae47963170d1660df7f56f5faf
- Ở bài này sau khi ta chuyển hết dữ liệu về Decimal thì ta có thể tìm KEY2 từ việc XOR dòng 2 với KEY1, KEY3 bằng cách XOR KEY2 mới tìm được với dòng 2, và tương tự như vậy để tìm ra flag. Ví dụ:KEY3 = KEY2^'c1545756687e7573db23aa1c3452a098b71a7fbf0fddddde5fc1'
## Code mẫu
		from Crypto.Util.number import*

		key1=int('a6c8b6733c9b22de7bc0253266a3867df55acde8635e19c73313',16)
		k2=int('37dcb292030faa90d07eec17e3b1c6d8daf94c35d4c9191a5e1e',16)
		k3=int('c1545756687e7573db23aa1c3452a098b71a7fbf0fddddde5fc1',16)
		k4=int('04ee9855208a2cd59091d04767ae47963170d1660df7f56f5faf',16)

		key2=key1^k2
		key3=key2^k3
		flag=hex(key1^key2^key3^k4)

		flag=flag[2:]
		flag=bytes.fromhex(flag).decode()

		print(flag)
***Lưu ý***: Sau khi XOR KEY ra FLAG xong thì trong FLAG sẻ có 2 kí tự đầu là ox là kí tự định dạng cho bytes, nên khi ta đổi FLAG về Hex thì phải bỏ nó ra
-Cờ là: ***crypto{x0r_i5_ass0c1at1v3}***
