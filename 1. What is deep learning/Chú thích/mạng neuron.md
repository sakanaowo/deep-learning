[link](https://nttuan8.com/bai-3-neural-network/#Neural_network_la_gi)
Mạng neuron trong deep learning là một mô hình máy tính được lấy cảm hứng từ cách hoạt động của bộ não con người. Nó được thiết kế để <span style="color:rgb(0, 176, 240)">nhận dạng các mẫu và dự đoán kết quả dựa trên dữ liệu đầu vào</span>. Dưới đây là tóm lược về mạng neuron trong deep learning:

### 1. **Neuron nhân tạo (Artificial Neuron)**:
- **Cấu trúc**: Một neuron nhân tạo mô phỏng một tế bào thần kinh trong bộ não. Nó nhận nhiều đầu vào (inputs), mỗi đầu vào có trọng số (weight) khác nhau.
- **Hoạt động**: Neuron tính toán tổng có trọng số của các đầu vào, sau đó áp dụng một hàm kích hoạt (activation function) để quyết định đầu ra (output).

### 2. **Mạng neuron đơn giản (Single Layer Perceptron)**:
- **Cấu trúc**: Gồm một lớp đầu vào, một lớp đầu ra và các kết nối trọng số giữa chúng.
- **Hạn chế**: Không thể giải quyết các vấn đề phức tạp, chỉ có thể phân loại các dữ liệu tuyến tính.

### 3. **Mạng neuron đa lớp (Multilayer Perceptron - MLP)**:
- **Cấu trúc**: Gồm nhiều lớp neuron, bao gồm lớp đầu vào, lớp ẩn (hidden layers) và lớp đầu ra.
- **Ưu điểm**: Có khả năng học và mô hình hóa các dữ liệu phi tuyến tính phức tạp.

### 4. **Hàm kích hoạt (Activation Functions)**:
- **Mục đích**: Giới thiệu tính phi tuyến vào mô hình, giúp mạng neuron học các mối quan hệ phức tạp hơn.
- **Các loại phổ biến**: Sigmoid, Tanh, ReLU (Rectified Linear Unit), Leaky ReLU.

### 5. **Huấn luyện mạng neuron (Training Neural Networks)**:
- **Phương pháp**: Sử dụng thuật toán lan truyền ngược (Backpropagation) và tối ưu hóa trọng số qua các bước học (epochs).
- **Hàm mất mát (Loss Function)**: Đo lường sự khác biệt giữa dự đoán của mô hình và giá trị thực tế, ví dụ Mean Squared Error (MSE), Cross-Entropy.
- **Tối ưu hóa**: Sử dụng các phương pháp như Gradient Descent, Adam để điều chỉnh trọng số nhằm giảm hàm mất mát.

### 6. **Deep Learning và Mạng neuron sâu (Deep Neural Networks - DNNs)**:
- **Đặc điểm**: Sử dụng nhiều lớp ẩn để tăng cường khả năng học và xử lý dữ liệu phức tạp.
- **Ứng dụng**: Nhận dạng hình ảnh, xử lý ngôn ngữ tự nhiên, nhận dạng giọng nói, và nhiều lĩnh vực khác.

### 7. **Các loại mạng neuron khác**:
- **CNN (Convolutional Neural Networks)**: Được sử dụng chủ yếu trong xử lý hình ảnh.
- **RNN (Recurrent Neural Networks)**: Được sử dụng cho dữ liệu tuần tự như chuỗi thời gian hoặc văn bản.
- **GAN (Generative Adversarial Networks)**: Được sử dụng để tạo dữ liệu mới từ dữ liệu đã có.

