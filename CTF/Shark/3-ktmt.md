# ktmt
![image](https://user-images.githubusercontent.com/128831586/232323670-7042b82a-20a3-40da-8d5b-78a6be1d5adb.png)
- Chúng ta có thể thấy bài này khá giống với bài Favourite byte trên Cryptohack nên ta làm y chang như vậy

- Đầu tiên chúng ta Xor key với output, vì ta biết flag sẻ có dạng là 'Shark{' nên ta gán flag là b'Shark{' và xor với output

#HVC là gì, bối rối quá trời lunnnnn

    def xor(a: bytes, b: bytes):
        return bytes([a[i%len(a)] ^ b[i%len(b)] for i in range(max(len(a), len(b)))])

    flag = b'shark'
    key = b'\x10\x1a\x18\x02\x1f\x14\x1b\x1d\x0b/<\x0e<$\x18\x1e+,\x16\x0f'

    print(xor(flag, key).decode())
    #output=\x10\x1a\x18\x02\x1f\x14\x1b\x1d\x0b/<\x0e<$\x18\x1e+,\x16\x0f

- Sau khi xor xong thì ta thu được đoạn dữ liệu là "b'cryptohuj]WuOLyl@Weg" tùe đó ta đoán key là 'crypto' nên ta gán flag bằng b'crypto' và xor với output

    #HVC là gì, bối rối quá trời lunnnnn

    def xor(a: bytes, b: bytes):
        return bytes([a[i%len(a)] ^ b[i%len(b)] for i in range(max(len(a), len(b)))])

    flag = b'\x10\x1a\x18\x02\x1f\x14\x1b\x1d\x0b/<\x0e<$\x18\x1e+,\x16\x0f'
    key = b'crypto'

    print(xor(flag, key).decode())
    #output=\x10\x1a\x18\x02\x1f\x14\x1b\x1d\x0b/<\x0e<$\x18\x1e+,\x16\x0f

- Và flag là: ***Shark{xor_Ha_Van_Cu}***
