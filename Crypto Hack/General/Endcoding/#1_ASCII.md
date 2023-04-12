# ASCII
![image](https://user-images.githubusercontent.com/128831586/231408181-07256863-6a41-462e-add6-ffea4ba25114.png)
- Challenge này sẻ giúp chúng ta hiểu rỏ hơn về bảng mã ASCII.
![image](https://user-images.githubusercontent.com/128831586/231409740-007de9a3-36e8-40f4-a084-342590b4d567.png)
- Bảng mã ASCII (tên đầy đủ: American Standard Code for Information Interchange - Chuẩn mã trao đổi thông tin Hoa Kỳ), thường được phát âm là át-xơ-ki, là bộ ký tự và bộ mã ký tự dựa trên bảng chữ cái La Tinh được dùng trong tiếng Anh hiện đại và các ngôn ngữ Tây Âu khác.
- Để giải được challenge này thì như đề đã gợi ý, thì ta phải đổi tấp cả các con số này từ hệ thập phân về ký tự.
![image](https://user-images.githubusercontent.com/128831586/231410814-ea7ab599-e318-4718-b9a7-9853f9a7363d.png)
- Các công cụ để đổi của Python:
  + chr(): Chuyển từ Decimal sang ASCII
  + ord(): Chuyển từ ASCII sang decimal
## Code mẩu
'''
	data=[99, 114, 121, 112, 116, 111, 123, 65, 83, 67, 73, 73, 95, 112, 114, 49, 110, 116, 52, 98, 108, 51, 125]
	flag=""
	for i in data:
			flag=flag+chr(i)
	print(flag)
'''
	
