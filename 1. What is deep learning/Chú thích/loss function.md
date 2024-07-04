[bài viết về loss function](https://khanh-personal.gitbook.io/ml-book-vn/chapter1/ham-mat-mat)
**Loss function** kí hiệu là L, là thành phần cốt lõi của [[evaluation function]] và [[objective function]]. Cụ thể, trong công thức thường gặp:
![[Pasted image 20240704003224.png]]
Loss function trả về một số thực không âm thể hiện sự chênh lệch giữa hai đại lượng: �^y^​, label được dự đoán và �y, label đúng. Loss function giống như một hình thức để bắt model đóng phạt mỗi lần nó dự đoán sai, và số mức phạt tỉ lệ thuận với độ trầm trọng của sai sót. Trong mọi bài toán supervised learning, mục tiêu của ta luôn bao gồm giảm thiểu tổng mức phạt phải đóng. Trong trường hợp lý tưởng �^=�y^​=y, loss function sẽ trả về giá trị cực tiểu bằng 0.
