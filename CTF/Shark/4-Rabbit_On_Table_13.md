# Rabbit_On_Table_13
![image](https://user-images.githubusercontent.com/128831586/232324485-111271c7-e919-4821-9ec1-844af51dbbca.png)
- Ở challenge này sẻ kiểm tra chúng ta cách đưa dữ liệu về ascii và khả năng phân tích đề của chúng ta
- Đề cho 1 đoạn lst, sau khi ta nhìn vào đoàn đó thì ta nghĩ ngay đến việc decode nó về ascii.

    lst=[121, 114, 103, 95, 122, 114, 95, 113, 98, 106, 97, 95, 102, 121, 98, 106, 121, 108]

    s=[]
    for i in lst:
        s.append(chr(i))

    s="".join(s)
    print(s)

- Sau khi decode về ascii thì nhìn vào đề ta thấy đề là Rabbit_On_Table13 và đoạn gợi ý là "#Con số mà nhiều người coi là không tốt thường được bỏ qua trong các khu vực đếm số, vì nó được cho là mang lại điều không may và rủi ro." nên ta phân tích thành ROT13 từ đó ta tìm thử tool rot13 và nó gợi ý cho ta tool rot13 cipher
- Sau khi sử dụng tool rot13 thì ta thu được "let_me_down_slowly" suy ra flag là: ***Shark{let_me_down_slowly}***
