# Endcoding
![image](https://user-images.githubusercontent.com/128831586/232316356-abc6ebde-67fa-4ea7-a041-eb27ad55316d.png)
- Đây là challenge đầu tiên của Shark_CTF_Crypto do team Shark tổ chức cụ thể là Trần Anh Nhật Việt bao sân, tạo ra các bài CTF để kiểm tra khả năng của tụi chơi Crypto như tụi mình.
- Challenge này nhằm kiểm tra khả năng giải endcoding của tụi mình.
- Đề như sau
    #Chall này dựa vào kiến thức General và tạo acc Cryptohack

        from Crypto.Util.number import*
        from base64 import*
        flag='shark{????????????????????????????}'
        #Giữa các f_block sẽ có dấu '_'
        f_block_1 = 418547722601
        f_block_4 = 'YmlnSW50ZXJnZXI='
        f_block_3 = 626173653634
        f_block_2 = 'rohknomswkv'
    
- Đề cho ta 4 block, flag sẻ là kết hợp của 4 block đó.
- Ta được gợi ý là "Chall này dựa vào kiến thức General và tạo acc Cryptohack nên ta nghĩ ngay đến:
    +   Dùng Cipher
    +   Kiến thức phần endcoding
    +   kiến thức phần Xor
-   Nhưng vì đề bài cho toàn dữ liệu nên ta có thể loại bỏ trường hợp dùng kiến thức phần Xor.
  
-   Với f_block_1 ta thấy nó là 1 số lớn nên ta sẻ dùng long_to_bytes() để giải nó:
   
        f_block_1 = 418547722601
        block1=long_to_bytes(f_block_1).decode()
        
-  Với đoạn code này chúng ta sẻ tìm được block1 là: ***ascii***
  
-  Với f_block_2 ta thấy đoạn block này khá giống với lúc ta tạo tài khoản Cryptohack nên ta sẻ thử dùng cipher.
-  Và block2 là: ***hexadecimal***

-  Với f_block_3 ta cũng thấy nó giống với số lớn nên ta thử dùng long_to_byte nhưng khi ta làm thì nó lại bị lỗi nên ta nghĩ sang cách khác đó chính là dùng hàm bytes.fromhex().

        f_block_3 = '626173653634'
        block3=bytes.fromhex(f_block_3).decode()
        
-   Với đoạn code này chúng ta sẻ tìm được block3 là: ***base64***

-   Với f_block_4 thì đề cho 1 đoạn khá giốn với base64 nên thử dùng base64.

        block4=base64.b64decode(f_block_4).decode()

Với đoạn code này ta sẻ có đc block4 là: ***bigInterger***

# Code mẩu

#Chall này dựa vào kiến thức General và tạo acc Cryptohack

        from Crypto.Util.number import*
        import base64
        flag='shark{????????????????????????????}'
        #Giữa các f_block sẽ có dấu '_'
        f_block_1 = 418547722601
        f_block_4 = 'YmlnSW50ZXJnZXI='
        f_block_3 = '626173653634'
        f_block_2 = 'rohknomswkv'

        block1=long_to_bytes(f_block_1).decode()
        block2='hexadecimal'
        block3=bytes.fromhex(f_block_3).decode()
        block4=base64.b64decode(f_block_4).decode()

        flag= 'Shark{'+ str(block1)+'_'+str(block2)+'_'+str(block3)+'_'+str(block4)+'}'

        print(flag)
-   Và cờ của bài này là: ***Shark{ascii_hexadecimal_base64_bigInterger}***
