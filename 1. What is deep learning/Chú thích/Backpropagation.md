Backpropagation là một thuật ngữ trong machine learning và neural networks, <span style="color:rgb(66, 255, 242)">được sử dụng để huấn luyện mạng neural</span>. Nó là viết tắt của cụm từ "backward propagation of errors" (lan truyền ngược của lỗi). Thuật toán này được sử dụng để <span style="color:rgb(66, 255, 242)">điều chỉnh các trọng số của mạng neural dựa trên độ lỗi giữa giá trị đầu ra dự đoán và giá trị đầu ra thực tế</span> đã biết từ dữ liệu huấn luyện.

Cụ thể, quá trình backpropagation <span style="color:rgb(66, 255, 242)">bắt đầu từ đầu ra của mạng neural</span> và <span style="color:rgb(66, 255, 242)">lan truyền ngược lại các lớp trước</span> đó để <span style="color:rgb(66, 255, 242)">tính toán độ lỗi ở mỗi lớp</span> và <span style="color:rgb(66, 255, 242)">điều chỉnh các trọng số</span> sao cho độ lỗi này giảm dần. Thuật toán này giúp mạng neural học được cách tối ưu hóa đầu ra dự đoán một cách chính xác hơn qua từng lần lặp.

Thuật toán này hoạt động theo hai giai đoạn chính:

1. **Lan truyền tiến (Forward Propagation):** Dữ liệu được đưa qua mạng neural từ lớp vào đến lớp ra để tính toán đầu ra dự đoán.
    
2. **Lan truyền ngược (Backward Propagation):** Sau khi tính được đầu ra, thuật toán tính toán gradient của hàm mất mát theo từng tham số của mô hình, bắt đầu từ lớp cuối cùng trở về lớp đầu tiên. Quá trình này dựa trên chain rule để truyền gradient ngược từ lớp ra về lớp vào.