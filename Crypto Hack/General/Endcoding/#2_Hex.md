# Hex
![image](https://user-images.githubusercontent.com/128831586/231415699-86c087be-22c4-48ca-a552-0ff8063c5d95.png)
-	Challenge này sẻ giúp chúng ta hiểu rỏ hơn về Hex
-	Hex hay còn được biết đến là hệ thập lục phân
-	Trong toán học và trong khoa học điện toán, hệ thập lục phân (hay hệ đếm cơ số 16, tiếng Anh: hexadecimal), hoặc chỉ đơn thuần gọi là thập lục, là một hệ đếm có 16 ký tự, từ 0 đến 9 và A đến F (chữ hoa và chữ thường như nhau).
-	Để giải challenge này thì ta phải chuyển dãy này về Bytes
-	63727970746f7b596f755f77696c6c5f62655f776f726b696e675f776974685f6865785f737472696e67735f615f6c6f747d
-	Để chuyển về thì ta được gợi ý sử dụng các hàm:
    + bytes.fromhex(): Chuyển từ hex sang bytes
    + bytes.hex() : Chuyển từ bytes sang hex
## code mẫu

    data='63727970746f7b596f755f77696c6c5f62655f776f726b696e675f776974685f6865785f737472696e67735f615f6c6f747d'
    flag=bytes.fromhex(data).decode()
    print(flag)  
    
- Cờ là: ***crypto{You_will_be_working_with_hex_strings_a_lot}***
- bạn có thể tham khảo thêm:
  + https://www.rapidtables.com/code/text/ascii-table.html
  + https://en.wikipedia.org/wiki/Hexadecimal
