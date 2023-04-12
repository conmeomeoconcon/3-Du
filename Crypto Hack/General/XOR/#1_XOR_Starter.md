# XOR
![image](https://user-images.githubusercontent.com/128831586/231427648-da0b4397-3723-41ef-af13-70e26702f3bf.png)
-	Challenge đầu tiên này sẻ giới thiệu với ta về XOR và cách nó hoạt động.
-	Các toán tử thao tác bit (tiếng Anh: bitwise operator) là các toán tử được sử dụng chung với một hoặc hai số nhị phân để tạo ra một phép toán thao tác bit. Hầu hết các toán tử thao tác bit đều là các toán tử một hoặc hai ngôi.
-	Để giải challenge này thi ta chỉ cần dùng phép XOR của Python
## Code mẫu

		data='label'
		flag=""
		for i in data:
				flag=flag+chr(ord(i)^13)
		print(flag)
		
-	Cờ là: ***crypto{aloha}***

