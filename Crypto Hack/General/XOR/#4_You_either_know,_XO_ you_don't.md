# You either know, XOR you don't
![image](https://user-images.githubusercontent.com/128831586/231473882-1b080930-4baf-4d01-a624-03ca2ea891c3.png)
- Ở challenge này sẻ giúp bạn trau dồi và năng cao khả năng làm việc với XOR của bạn
- Đề cho ta 1 đoạn mã Hex: 0e0b213f26041e480b26217f27342e175d0e070a3c5b103e2526217f27342e175d0e077e263451150104
- Ta sẻ đổi mã Hex này thành mã nhị phân
- Sau đó thay vì phải ép nó vào mảng để XOR thì ta có thể dùng hàm xor trong thư viện pwn
- Ta thấy "I've encrypted the flag with my secret key, you'll never be able to guess it." nên ta có flag=data^key <--> key=data^flag
- Vì cờ chắc chắn sẻ có "crypto{" nên ta gán flag="crypto"
- Sau đó đem flag xor với data ta đc: b'myXORke+y_Q\x0bHOMe$~seG8bGURN\x04DFWg)a|\x1dTM!an\x7f'
- Nên ta doán key=myXORkey
- Sau đó xor key với data ta sẻ tìm đc đáp án
# code mẫu
- Tìm key
    from pwn import xor

    data = bytes.fromhex('0e0b213f26041e480b26217f27342e175d0e070a3c5b103e2526217f27342e175d0e077e263451150104')
    flag=b'crypto{'
    key=xor(flag,data)
    print(key)
- Sau khi xong đoạn code này ta sẻ có đoạn:b'myXORke+y_Q\x0bHOMe$~seG8bGURN\x04DFWg)a|\x1dTM!an\x7f'
- Sau đó ta gán key=myXORkey

    from pwn import xor

    data = bytes.fromhex('0e0b213f26041e480b26217f27342e175d0e070a3c5b103e2526217f27342e175d0e077e263451150104')

    key=b'myXORkey'
    flag=xor(key,data)
    print(flag)
- Cờ là: ***crypto{1f_y0u_Kn0w_En0uGH_y0u_Kn0w_1t_4ll}***
