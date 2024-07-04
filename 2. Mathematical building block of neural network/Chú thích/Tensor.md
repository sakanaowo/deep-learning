[tensorFlow](https://www.facebook.com/legacy/notes/1625331727576436)
Tensor là một khái niệm cơ bản trong toán học và vật lý, được sử dụng rộng rãi trong lĩnh vực học máy và học sâu. Nó là một<span style="color:rgb(66, 255, 242)"> cấu trúc dữ liệu tổng quát có thể biểu diễn các đại lượng toán học với nhiều chiều khác nhau.</span> Dưới đây là một số điểm cơ bản về tensor:

1. **Định nghĩa**: Một tensor là <span style="color:rgb(66, 255, 242)">một mảng n-chiều của các số</span>. Nó có thể là một số <span style="color:rgb(66, 255, 242)">vô hướng </span>(scalar), <span style="color:rgb(66, 255, 242)">vector</span> (mảng một chiều), <span style="color:rgb(66, 255, 242)">ma trận</span> (mảng hai chiều), hoặc các mảng có nhiều chiều hơn.

2. **Cấp bậc (Rank)**: Cấp bậc của một tensor đề cập đến số chiều của nó:
   - Tensor bậc 0: Một số vô hướng, ví dụ: \(3\)
   - Tensor bậc 1: Một vector, ví dụ: \([1, 2, 3]\)
   - Tensor bậc 2: Một ma trận
   - Tensor bậc n: Một mảng n-chiều

3. **Ứng dụng trong học máy**:
   - Trong học máy, đặc biệt là học sâu, tensor được sử dụng để biểu diễn dữ liệu và trọng số của các mạng neural.
   - Ví dụ, một hình ảnh màu có thể được biểu diễn như một tensor bậc 3 với kích thước (chiều cao, chiều rộng, số lượng kênh màu).
   - ![[Pasted image 20240704104731.png]]

4. **[[Thao tác của tensor]]**:
   - Các thư viện học máy như TensorFlow và PyTorch cung cấp các công cụ mạnh mẽ để làm việc với tensor, bao gồm các phép toán số học, phép biến đổi và tối ưu hóa.
   - Các phép toán này thường được thực hiện trên GPU để tăng tốc độ xử lý.

5. **Ký hiệu**:
   - Tensor thường được ký hiệu bằng các chữ cái viết hoa, ví dụ: \(T\).
   - Cách ký hiệu cũng phụ thuộc vào ngữ cảnh và lĩnh vực sử dụng.

6. **Ứng dụng trong học sâu**:
   - Khi huấn luyện một mạng neural, dữ liệu đầu vào (chẳng hạn hình ảnh, văn bản) và trọng số của các lớp mạng được biểu diễn dưới dạng tensor.
   - Các phép biến đổi, tính toán trong quá trình huấn luyện và dự đoán cũng được thực hiện trên các tensor này.
