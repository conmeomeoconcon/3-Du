# Hese
![image](https://user-images.githubusercontent.com/128831586/232325385-463b896a-2011-4e60-9be5-0ddb09a784f3.png)
- Ở challenge này chúng ta sẻ phải đối mặt với không chỉ 1 mà là rất nhiều base64
- Ta có gợi ý là "#Bạn có bối rối trước quá nhiều Base64 hăm" nên ta sẻ nghĩ đến việc decode cái này nhiều lần
## code mẩu

    import base64
    from Crypto.Util.number import*

    r='NGUgNDcgNTUgNjcgNGUgNDQgNTEgNjcgNGUgNmEgNjMgNjcgNGUgNmEgNjMgNjcgNGUgNDcgNTEgNjcgNGUgMzIgNDUgNjcgNGUgNDcgNTEgNjcgNGUgNmEgNjMgNjcgNGUgNDcgNTEgNjcgNGUgMzIgNDUgNjcgNGUgNDQgNTUgNjcgNGUgNmEgNjMgNjcgNGUgNDcgNTEgNjcgNGUgMzIgNDUgNjcgNGUgNDQgNTUgNjcgNGUgNmEgNjMgNjcgNGUgNDcgNTEgNjcgNGUgMzIgNDUgNjcgNGUgNDQgNDUgNjcgNGUgNmEgNjMgNjcgNGUgNDcgNTUgNjcgNGUgNTQgNjMgNjcgNGUgNTQgNmIgNjcgNGUgNmEgNjMgNjcgNGUgNDcgNTUgNjcgNGUgNDQgNjMgNjcgNGUgNTQgNDUgNjcgNGUgNmEgNjMgNjcgNGUgNDcgNTUgNjcgNGUgNTQgNTEgNjcgNGUgNmQgNDkgNjcgNGUgNmEgNjMgNjcgNGUgNDcgNTUgNjcgNGUgNTQgNjMgNjcgNGUgNTQgNmIgNjcgNGUgNmEgNjMgNjcgNGUgNDcgNTUgNjcgNGUgNDQgNTEgNjcgNGUgNTQgNmIgNjcgNGUgNmEgNjMgNjcgNGUgNDcgNTUgNjcgNGUgMzIgNDUgNjcgNGUgNDQgNmIgNjcgNGUgNmEgNjMgNjcgNGUgNDcgNTEgNjcgNGUgMzIgNDUgNjcgNGUgNDQgNTUgNjcgNGUgNmEgNjMgNjcgNGUgNDcgNTEgNjcgNGUgMzIgNDUgNjcgNGUgNDcgNTEgNjcgNGUgNmEgNjMgNjcgNGUgNDcgNTUgNjcgNGUgNDQgNjMgNjcgNGUgNTQgNTUgNjcgNGUgNmEgNjMgNjcgNGUgNDcgNTUgNjcgNGUgNDQgNTEgNjcgNGUgNTQgNDUgNjcgNGQgMzIgNTEgM2Q='

    r=base64.b64decode(r).decode()
    r=bytes.fromhex(r).decode()

    r=base64.b64decode(r).decode()
    r=bytes.fromhex(r).decode()

    r=base64.b64decode(r).decode()
    r=bytes.fromhex(r).decode()

    flag='Shark{'+str(r)+'}'

    print(flag)

- Sau khi decode 3 lần thì thấy được flag là: ***Shark{H3110_MY_Fr13ND}***
