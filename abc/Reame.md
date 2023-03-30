# Cryptography
  Cryptography hay mật mã học là hoạt động nghiên cứu về các kỹ thuật truyền thông an toàn, chỉ cho phép người nhận và người gửi có thể đọc được nội dung bên trong thông điệp đó.
  Cryptography có 4 loại thường gặp:
 - Symmetric Encryption – Mã hóa đối xứng
 - Asymmetric Encryption – Mã hóa bất đối xứng
 - Hashing functions – Hàm băm
 - Digital signatures – Chữ ký số
## Symmetric Encryption – Mã hóa đối xứng
  Symmetric Encryption hay Mã hóa đối xứng là một trong những dạng mã hóa phổ biến và dễ thực hiện nhất, trong đó:

  -Encryption: là quá trình mã hóa nội dung một thông điệp, khiến người không có key không thể hiểu được nội dung của thông điệp.
  -Decryption: là quá trình giải mã, thông thường sẽ dùng key do người thực hiện mã hóa cung cấp để giải mã và đọc được nội dung thông điệp.
 ## Asymmetric Encryption – Mã hóa bất đối xứng
  Nếu bạn sử dụng Symmetric Encryption trên mạng Internet vốn dĩ không an toàn, đồng nghĩa với việc key lẫn thông điệp bạn gửi đi đều sẽ có thể bị đọc trộm. Vì thế, Asymmetric Encryption – Mã hóa bất đối xứng được sinh ra.

  Với Asymmetric Encryption, chúng ta sẽ có 2 key, 1 key riêng tư do chúng ta giữ và một key công khai sẽ được gửi đến đối tác. Cả 2 key này sẽ được dùng để xác nhận 2 bên và tạo ra một kết nối an toàn hơn.
  ## Hashing functions – Hàm băm
  Trong thực tế, Asymmetric Encryption vẫn có thể dễ dàng bị phá khi khóa công khai bị làm giả. Một phương án khác được thực hiện đó chính là Hashing functions (hay Hàm băm) được ra đời và Hashing functions là hàm 1 chiều không thể khôi phục lại 100% nội dung thông điệp ban đầu. Điều này sẽ vô cùng lý tưởng cho việc xác thực dữ liệu.
 ## Sử dụng encoding/decoreding
  Encoding là quá trình chuyển đổi chuỗi các ký tự như là chữ cái, chữ số và các ký tự đặc biệt thành một dạng format khác theo quy chuẩn nhất định (ví dụ như theo bảng mã ASCII) để truyền dẫn một cách hiệu quả.
  Decoding là quá trình chuyển đổi chuỗi ký tự đã bị encoding về lại trạng thái ban đầu. Quá trình này hoàn toàn khác với mã hóa - Encryption mà chúng ta vẫn hay lầm tưởng.
  Encoding và Decoding thường được xử dụng trong quá trình trao đổi thông tin và lưu trữ thông tin. Tuy nhiên trong trường hợp cần trao đổi những thông tin nhạy cảm, mang tính bảo mật cao thì encoding không được khuyến khích sử dụng.
 ## URL Encoding
  URLs chỉ có thể được gửi đi thông qua Internet bằng việc sử dụng bảng mã ASCII và cũng có những trường hợp khi URL chứa các ký tự đặc biệt ngoài các ký tự trong bảng mã ASCII, nó cần được mã hóa.
  ## ASCII Encoding
  ASCII là viết tắt của American Standard Code for Information Interchange. Máy tính chỉ có thể hiểu được các con số, vì vậy bảng mã ASCII biểu diễn các ký tự dưới dạng các con số. Mục đích của những mã hiệu này là nhằm tiết kiệm phí tổn trong quá trình truyền tải data trên băng thông. Trình duyệt (phía máy khách) sẽ mã hóa đầu vào theo bộ ký tự được sử dụng trong trang web và bộ ký tự mặc định trong HTML5 là UTF-8.
## Hashing functions lý tưởng sẽ cần phải thỏa được 2 điều:

- 1 input đưa vào chỉ có duy nhất 1 output được tạo ra và không được trùng lặp với bất kỳ output nào đã tồn tại.
- 1 input sẽ có kết quả output giống nhau dù cho thực hiện bao nhiêu lần.
  Vì thế, Hashing functions được áp dụng tốt nhất vào việc bảo mật mật khẩu. Server chỉ lưu lại kết quả output và so sánh kết quả output khi người dùng nhập mật khẩu.
## Digital signatures – Chữ ký số
  Digital signatures sẽ sử dụng kết hợp cả Hashing functions và asymmetric encryption để mã hóa thông điệp giúp đạt được 2 mục đích: bảo vệ tính toàn vẹn, bảo mật của dữ liệu và có thể xác nhận được danh tính trong quá trình gửi đi.
# Cryptanalysis
  Cryptanalysis là ngành học nghiên cứu các phương thức để thu được ý nghĩa của thông tin đã được mã hóa. Điều này liên quan đến việc tìm khóa bí mật.
  
  Cryptanalysis cũng được dùng để ám chỉ tới bất kỳ cố gắng để phá vỡ sự bảo mật của các giải thuật mật mã và giao thức khác nói chung. Tuy nhiên, cryptanalysis thường không bao gồm các phương thức tấn công mà không nhắm vào đích chính là những nhược điểm của các cách viết mật mã hiện nay, như bribery, physical coercion, burglary, keystroke logging, và social enginerring.
## Các kiểu tấn công
  Về cơ bản, điều quan trong thực tế cần cho một cuộc tấn công dựa vào việc trả lời 3 câu hỏi sau:

1. Kiến thức và khả năng nào là điều kiện tiên quyết?
2. Có bao nhiêu thông tin bí mật được suy luận ra?
3. Đòi hỏi bao nhiêu nỗ lực? (Bản chất phức tạp của tính toán là gì?)

• Total break — Kẻ tấn công tìm ra khóa bí mật.
• Global deduction — Kẻ tấn công tìm ra giải thuật tương đương cho sự mã hóa và giải mã nhưng không học về key.
• Instance (local) deduction — kẻ tấn công tìm ra khối plaintext (hoặc ciphertext) mà không được biết trước.
• Information deduction — Kẻ tấn công thu được một vài thông tin Shanon ve plaintext (hoặc ciphertext) không được biết trước.
• Distinguishing algorithm — Kẻ tấn công có thể nhận biết được khối từ một sự hoán vị ngẫu nhiên.
• Time — số "phép tính chính" được mô tả. Cái này không chặt chẽ, phép tính chính có thể là các chỉ dẫn máy tính cơ bản như cộng, XOR, luân phiên…,hoặc hoàn toàn là các phương thức mã hóa. Such as addition, XOR, shift, and so forth, or entire encryption methods.
• Memory —Sô lưu trữ đòi hỏi để mô tả tấn công the amount of storage required to perform the attack.
• Data — chất lượng của plaintext và ciphertext đòi hỏi.

# Block Cipher and Stream Cipher
## stream Cipher
  Mật mã dòng (Stream cipher) thuộc mật mã khoá bí mật, đối xứng. Ý tưởng của thuật toán mã hoá theo dòng là bản nguồn sẽ được phân rã thành các bit; từng bit này sẽ được mã hoá bằng mỗi bit khoá để cho kết quả là một bit mã. Việc mã hoá bit được thực hiện bằng hàm logic XOR.
  
  Một số thuật toán:
- Stream key(dòng khóa)
- Thuật toán A5(tạo khóa tuyến tính)
- Máy chạy và dừng luân phiên
- Thuật toán RC4(Rivest Cipher 4)
- One-time pad(OTP)
## Block Cipher
  Block Cipher là phương pháp mã hóa dữ liệu trong Block nhằm tạo ra các bản mã dựa vào các thuật toán và khóa mật mã. Khác với Stream Cipher chỉ có thể mã hóa dữ liệu từng bit một, Block Cipher giúp xử lý các Block có kích thước cố định cùng một lúc và thường là 64 hoặc 128 bit.
  
 Các chế độ của block cipher:
- Chế độ Electronic Codebook (ECB)
- Chế độ Cipher Block Chaining (CBC)
- Chế độ Ciphertext Feedback (CFB)
- Chế độ Output Feedback (OFB)
- Chế độ Counter (CTR)
