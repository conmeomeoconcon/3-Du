# Sor
![image](https://user-images.githubusercontent.com/128831586/232324977-e8f9dc79-5997-4673-ba60-0719a196cc47.png)
- Ở challenge này chúng ta có thể thấy nó khá giống với challenge "XOR Properties" của Cryptohack nên ta sẻ làm giống như vậy.

## Code mẫu

    #Tìm flag và bạn sẽ thấy ai là người đẹp trai nhất

    #key2 = key1^flag
    #key1 = key4^key3
    #key2 = key5^key6
    from pwn import xor


    key3 = b'7\xdc\xb2\x92\x03\x0f\xaa\x90\xd0~\xec\x17\xe3\xb1\xc6\xd8\xda\xf9L5\xd4\xc9\x19\x1a^\x1e'
    key4 = b'\x91\x14\x04\xe1?\x94\x88N\xab\xbe\xc9%\x85\x12@\xa5/\xa3\x81\xdd\xb7\x97\x00\xddm\r'
    key5 = b'\x04\xee\x98U \x8a,\xd5\x90\x91\xd0Gg\xaeG\x961p\xd1f\r\xf7\xf5o_\xaf'
    key6 = b'\xd1NOTwjzy\x8a?\xaa\x14oe\x9e\x85\xacKh\xd1\x18\xc0\x89\xdc3\xd8\xc7VqRnpgT\x9a$\x94\x08'

    key1 = xor(key4,key3)
    key2 = xor(key5,key6)
    flag = xor(key1,key2).decode()

    print(flag)
    
- Và flag là: ***shark{tran_anh_nhat_viet_dep_trai_qua}***
