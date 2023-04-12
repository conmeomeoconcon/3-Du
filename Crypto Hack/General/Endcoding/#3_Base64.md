# Base64
![image](https://user-images.githubusercontent.com/128831586/231420024-30f6efde-55d7-4c39-ac45-3431d1887b03.png)
- Mục đích của challenge này là giúp bạn làm quen với Base64
- Base64 là phương thức convert dạng mã hóa 2 chiều từ binary sang string để có thể gửi đi được trong network một cách dễ dàng. Các binary lúc này sẽ được thể hiện bằng các ký tự mã ASCII.
- Để giải bài này ta cần phải chuyển đoạn này sang bytes rồi sang base64
- 72bca9b68fc16ac7beeb8f849dca1d8a783e8acf9679bf9269f7bf
- Đề có gợi ý cho ta sử dụng các hàm của base64
    + base64.b64encode(): Mã hóa bytes sang base64
    + base64.b64decode(): Giải mã base64 về bytes
## Code mẫu
    import base64

    data = '72bca9b68fc16ac7beeb8f849dca1d8a783e8acf9679bf9269f7bf'
    binary_data = bytes.fromhex(data)
    flag = base64.b64encode(binary_data)
    print(flag)
- Cờ là: ***crypto/Base+64+Encoding+is+Web+Safe/***
