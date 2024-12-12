[Bitcoin Whitepaper](bitcoin.pdf)

## Introduction

#### The disadvantage of old system.
Commerce on Internet often face disputes and need a trusted third party to mediate. It brings some disadvantage problem, such as added expense of financial institutions to resolve conflicts and the result of disputes rely on these financial insituations. Disputes can make reversal transactions, so both parties need be vigilant, especially merchants must be wary of their customer to avoid defraud.
#### Solution 
+ Using an electronic payment system based in cryptographic proof instead of trust, helping us don't need to depend on a trusted third party. This system make all transactions can't reverse.
+ Using keys pair with a hash function to make a chain of digital signatures to prove all transaction is confirmed.
#### Transaction

![[Pasted image 20241212222730.png]]

Private key is used to sign new signature for the owner. With the previous owner signature and current owner's public key and a hash function(which rely on previous transactions), we can make new transaction. This transaction can verify by previous owner's public key.

#### [[Double-spending]]

In traditional solution, all transaction can be verified by the mint to avoid double-spent. But there is a disadvantage in this way that we depend on the company running the mint.
So, to accomplish all transactions without a trusted party, all transactions must be public announced and we need an system for participants to agree on a only history. That system will agree the first time the coin is changed and the payee needs proof that at the time of each transaction, the majority of nodes agreed it was the first received.

#### [[Timestamp]]

Using a timestamp server to public the time that the transaction is created.
1. A block includes:
    +  The information of itselft.
    +  The time the block was created.
    +  A hash of the previous block.
2. When a new block is created:
    +  This block based on the time this block is created and a hash of the previous block.
    +  The hash of this new block is broadcasted to all nodes.

#### [[Proof-of-work]]

Nếu sử dụng cơ chế biểu quyết theo số đông thì kẻ tấn công có thể kiểm soát hệ thống nếu nó giữ > 50% số node trên mạng. Để tránh khỏi nhược điểm này, cơ chế Proof-of-work được sinh ra.

##### Ưu điểm
Kẻ tấn công khi muốn thay đổi thông tin của 1 nodes nào đó thì cũng phải tạo lại tất cả các nodes đứng sau đó để thỏa mãn điều kiện mã hóa.
Để chống lại điều này, chúng ta sẽ xây dựng 1 hệ thống tạo các node nhanh đến mức không 1 kẻ tấn công nào có thể đuổi kịp được ==> Tin vào 1 hệ thống có tốc độ và sức mạnh phần cứng lớn nhất. Nếu phần lớn các node của hệ thống có sức mạnh phần cứng và các node đó tuân thủ quy tắc thì chuỗi block đó sẽ chuỗi nhanh nhất và vượt xa tốc độ của những kẻ tấn công. Để kiểm soát tốc độ của mỗi khối được tạo ra, ta sẽ phải đặt ra 1 bài toán chung và tất cả mọi người đều có quyền tham gia giải chúng. Khi giải được bài toán đó thì ta sẽ tìm được địa chỉ để có thể tạo được block tiếp theo.
Bài toán đặt ra đó là phải tìm 1 số nonce thỏa mãn những điều kiện mã hóa. Chỉ có 1 cách giải cho bài toán này là đi thử tất cả các trường hợp có thể xảy ra. Điều này chứng tỏ rằng node nào giải được bài toán này nhanh nhất thì node đó nhiều khả năng chính là node có sức mạnh phần cứng và tốc độ tính toán cao nhất.

Sau khi node nhanh nhất tìm được số nonce và tạo ra 1 block mới thì các node còn lại sẽ đồng thuận hóa bằng cách thay số nonce này vào hệ thống của chính node đó.

=> Proof of work là cơ chế dựa trên phần cứng mạnh nhất để tối đa tốc độ tạo ra các block mới, khiến cho những kẻ tấn công không thể đuổi kịp để thay đổi.

##### Nhược điểm
+ Khi các node đua nhau tăng sức mạnh phần cứng để có thể giải được bài toán nhanh nhất, thì sẽ lãng phí tài nguyên của các node cố gắng giải nhưng không phải nhanh nhất.
+ (Cái này em không chắc) Có thể càng về sau, bài toán sẽ càng khó và tốc độ để tạo ra 1 block mới ngày càng giảm.

#### Network

Hệ thống sẽ vận hành theo quy trình
+ Các giao dịch sẽ được gửi tới tất cả các node.
+ Mỗi node gom các giao dịch đó lại và tìm cách tạo ra 1 block mới.
+ Các node phải giải bài toán của proof-of-work để có thể nối block đó vào trong hệ thống
+ Node đầu tiên giải được bài toán đó, nó sẽ phát tán cho tất cả các node còn lại
+ Các node còn lại chấp nhận block mới vào chuỗi nếu tất cả các transaction trong block đó hợp lệ.