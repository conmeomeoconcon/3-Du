# Greatest Common Divisor
![image](https://user-images.githubusercontent.com/128831586/231485429-0be83dd7-cdb0-4747-b280-57c014f3e8d6.png)
-	Ở bài này ta sẻ nhắc lại một bài toàn đơn giản lớp 6, tìm ước chung lớn nhất
-	Trước hết ta sẻ đi vào các tìm ước chung lớn nhất
	+	Cho 2 số a, b
	+	Ta sẻ lấy số lớn hơn trừ số nhở hơn
	+	Ví dụ:
	+	a = 14, b = 8
	+	14 -8 = 6
	+	Sau đó ta thay số kết quả vào số lớn
	+	Ví dụ:
	+	a = 6, b = 8
	+	Sau đó ta lại lấy số lớn hơn trừ số nhỏ hơn
	+	Ví dụ:
	+	8 -6 = 2
	+	Sau đó ta lặp lại các bước trên cho đến khi số kết quả bằng 0 thì dừng lại
	+	ước chung nhỏ nhất sẻ là số a hoặc số b
	+Ví dụ:
	+6 - 2 = 4
	+4 - 2 = 2
	+2 - 2 = 0
	+vậy khi a = 14 và b = 8 thì ước chung lớn nhất của chúng sẻ là 2
	# Code mẫu

		a = int(66528)
		b = int(52920)

		while a%b!=0:
				if a>b:
						a=a-b
				else:
						b=b-a

		print(a)  
- Cờ là: ***1512***
