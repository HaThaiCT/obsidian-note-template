[Double-spending - Wikipedia](https://en.wikipedia.org/wiki/Double-spending)
[[Bitcoin]]

**Double-spending** là hành động chi tiêu cùng một đơn vị tiền (cả tiền kỹ thuật số hoặc tiền giấy) nhiều hơn một lần một cách trái phép. Đây là vấn đề phổ biến trong hệ thống tài chính kỹ thuật số, nơi không có sự quản lý vật lý đối với đồng tiền, dẫn đến rủi ro bị sao chép hoặc gian lận.

#### Bản chất của vấn đề:

- Trong các giao dịch tiền mặt, double-spending không xảy ra vì một tờ tiền vật lý chỉ có thể được trao đổi một lần tại một thời điểm.
- Trong môi trường kỹ thuật số, do thông tin (bao gồm tiền kỹ thuật số) có thể sao chép dễ dàng, một kẻ gian có thể sử dụng cùng một token hoặc đồng tiền số trong nhiều giao dịch, nếu không có cơ chế ngăn chặn hiệu quả.

---

### Ví dụ trực quan về **Double-Spending**

**Tình huống:**  
Giả sử bạn có 1 token kỹ thuật số trị giá 100.000 VNĐ (không phải blockchain hoặc có cơ chế kiểm tra trung tâm yếu).

1. **Giao dịch đầu tiên:**  
    Bạn gửi token đó cho người bán hàng trực tuyến A để mua một món đồ giá 100.000 VNĐ. Người bán nhận được token, nhưng hệ thống chưa kiểm tra xem token đã được sử dụng trước đó hay chưa.
    
2. **Giao dịch thứ hai:**  
    Trong cùng thời gian, bạn sao chép token đó và sử dụng nó để mua một món đồ khác từ người bán B.
    

Nếu hệ thống không ngăn chặn hoặc phát hiện kịp thời, cả hai người bán đều nghĩ rằng họ nhận được token hợp lệ, nhưng thực chất chỉ có một đơn vị tiền tồn tại.

---

### Ngăn chặn Double-Spending trong các hệ thống khác nhau

1. **Trong hệ thống tập trung:**
    
    - Một cơ quan trung tâm (như ngân hàng hoặc hệ thống thanh toán) sẽ kiểm tra giao dịch để đảm bảo rằng token đó chưa được chi tiêu trước đó.
    - Ví dụ: Khi bạn quẹt thẻ tín dụng, ngân hàng xác minh tài khoản của bạn để đảm bảo rằng bạn có đủ số dư trước khi thực hiện giao dịch.
2. **Trong hệ thống phi tập trung (như blockchain):**
    
    - Blockchain giải quyết vấn đề này bằng cách ghi lại mọi giao dịch trong một sổ cái phân tán. Mỗi token chỉ có thể được chi tiêu khi đã được xác nhận bởi các nút trong mạng thông qua cơ chế đồng thuận, ví dụ như **proof-of-work** hoặc **proof-of-stake**.

---

### Một ví dụ thực tế sử dụng Blockchain để ngăn chặn Double-Spending

- Khi bạn gửi Bitcoin cho một người, giao dịch của bạn được truyền đi trên toàn mạng lưới. Các nút xác minh giao dịch bằng cách đảm bảo rằng bạn thực sự sở hữu số Bitcoin đó và chưa sử dụng chúng trước đây.
- Sau khi giao dịch được xác nhận, nó sẽ được thêm vào blockchain. Mọi giao dịch sau đó đều dựa vào bản ghi này, làm cho việc sử dụng lại Bitcoin đó trong một giao dịch khác là không thể.