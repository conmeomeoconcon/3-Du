# Favourite byte
![image](https://user-images.githubusercontent.com/128831586/231459602-781346ed-efeb-466a-8e46-95d7bfb7fea4.png)
-	Challenge này sẻ giúp bạn có cái nhìn khác về XOR, khiến bạn thoát ra khỏi khuôn khổ phải XOR 1 với 1.
-	Đề cho ta một đoạn Hex: '73626960647f6b206821204f21254f7d694f7624662065622127234f726927756d'.
-	Ta đưa đoạn này về thành bytes bằng bytes.fromhex().
-	Sau đó ta bỏ nó vào mảng rồi tiến hành XOR.
-	Ta thấy câu "I've hidden some data using XOR with a single byte" nghĩa là bạn phải XOR với đúng cái bytes mà đề đang dấu trong 256 bytes nên ta sẻ cho chạy trong khoảng [0:255].
-	Vì flag chắc chắn sẻ có "crypto", nên ta sẻ cho nó chạy đến khí đến khi thấy chứ "crypto" trong đó thì in ra.
# code mẫu
		data = bytes.fromhex('73626960647f6b206821204f21254f7d694f7624662065622127234f726927756d')
		data2=[]

		for i in data:
				data2.append(i)

		for i in range(256):
				a=""
				for j in data2:
						a=a+chr(j^i)
				if "crypto" in a:
						print(a)
-	Cờ là: ***crypto{0x10_15_my_f4v0ur173_by7e}***
