[Chữ ký số – Wikipedia tiếng Việt](https://vi.wikipedia.org/wiki/Ch%E1%BB%AF_k%C3%BD_s%E1%BB%91)
[Digital signature - Wikipedia](https://en.wikipedia.org/wiki/Digital_signature)
[[Bitcoin]]
**Digital Signature** (Chữ ký số) là một dạng chữ ký điện tử được sử dụng để đảm bảo tính xác thực và toàn vẹn của dữ liệu điện tử. Nó cung cấp sự bảo mật cho thông tin trong các giao dịch kỹ thuật số, giúp xác định rằng thông điệp hoặc tài liệu không bị thay đổi trong quá trình truyền đi. Digital Signature sử dụng công nghệ mật mã để tạo ra chữ ký, và mỗi chữ ký số là duy nhất cho một tài liệu hoặc giao dịch cụ thể.
Digital Signature hoạt động dựa trên **công nghệ mật mã** và **cặp khóa** (private và public key). Dưới đây là cách thức hoạt động chi tiết:

1. **Sử dụng cặp khóa (private-public key pair):**
    
    - **Khóa riêng (Private Key)**: Được sử dụng để tạo ra chữ ký số. Người dùng giữ bí mật cặp khóa này.
    - **Khóa công khai (Public Key)**: Được chia sẻ công khai để người nhận có thể xác minh chữ ký số.
2. **Tạo chữ ký số:**
    
    - **Tạo giá trị chữ ký**: Người gửi sử dụng khóa riêng của mình để tính toán một giá trị số (chữ ký số) từ nội dung dữ liệu cần ký. Quá trình này thường sử dụng một hàm băm mật mã (cryptographic hash function) và các phép toán mật mã.
    - Ví dụ: Nếu người gửi có dữ liệu `D` cần ký, họ sẽ tính toán chữ ký số như sau:
        - **Hàm băm mật mã (hash function)**: Tính toán giá trị băm `H(D)` từ dữ liệu `D`.
        - **Tính chữ ký**: Dùng khóa riêng để ký `H(D)`, kết quả là chữ ký số.
3. **Gửi dữ liệu và chữ ký số đi cùng nhau:**
    
    - Dữ liệu `D` và chữ ký số `S` (từ bước 2) được gửi đến người nhận.
4. **Xác minh chữ ký số:**
    
    - **Khóa công khai** của người gửi được sử dụng để xác minh tính xác thực của chữ ký.
    - Người nhận sử dụng khóa công khai của người gửi để tái tạo chữ ký số từ dữ liệu `D` và so sánh với chữ ký `S` mà họ nhận được.
    - Quá trình xác minh:
        - Tính hàm băm từ dữ liệu: `H(D)`.
        - Sử dụng khóa công khai để giải mã chữ ký `S` và tái tạo giá trị chữ ký.
        - So sánh `H(D)` với giá trị tái tạo chữ ký. Nếu chúng khớp, chữ ký số hợp lệ và dữ liệu không bị thay đổi.
        -


