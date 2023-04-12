# Lemur XOR
![image](https://user-images.githubusercontent.com/128831586/231481869-fb1e990f-0915-4df2-ba45-6b3c3c1ca5e6.png)
-	ở bài này chúng ta sẻ làm quen với một ứng dụng của XOR.
-	Đề bài cho ta 2 bức hình như thế này:
-	lemur.png.
![image](https://user-images.githubusercontent.com/128831586/231482273-3d8e0b2f-2ef4-4485-8941-1bb0672e5001.png)
-	flag.png.
![image](https://user-images.githubusercontent.com/128831586/231482490-1d36378c-b8b1-46fe-95e0-504386ffa40e.png)
- Bài này chúng ta chỉ cần chuyển hình về nhị phân sau đó xor với nhau rồi chuyển lại thành hình.
# Code mẫu

		from binascii import unhexlify

		with open("lemur.png", mode='rb') as fl:
				lemur = fl.read()


		with open("flag.png", mode='rb') as ff:
				flag = ff.read()

		d = b''
		for b1, b2 in zip(lemur, flag):
				d += bytes([b1^b2])

		with open("new.png", mode='wb') as fn:
				fn.write(d)	
-	ta có ảnh:
![image](https://user-images.githubusercontent.com/128831586/231484315-2d71385b-f16d-489a-9837-09f3ffd8b058.png)
-	Cờ là :***crypto{X0Rly_n0t!}***

    
