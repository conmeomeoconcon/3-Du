# Bytes and Big Integers
![image](https://user-images.githubusercontent.com/128831586/231423101-2cfc4ced-29b0-4d91-b2aa-e4ce6cd25ed7.png)
- Challenge này sẻ giúp chúng ta làm quen với 2 hàm long_to_bytes() và bytes_to_long().
    + long_to_bytes(): Chuyển từ integer về bytes
    + bytes_to_long(): Chuyển từ bytes sang integer
- 11515195063862318899931685488813747395775516287289682636499965282714637259206269
- Đề cho ta 1 chuỗi số nguyên, để giải bài này ta chỉ cần dùng hàm long_to_bytes()
## Code mẫu
    from Crypto.Util.number import*

    data=11515195063862318899931685488813747395775516287289682636499965282714637259206269
    flag=long_to_bytes(data).decode()
    print(flag)
- Cờ là: ***crypto{3nc0d1n6_4ll_7h3_w4y_d0wn}***
