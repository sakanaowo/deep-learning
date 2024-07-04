[Tensor operations](https://theneuralblog.com/basic-operations-on-tensors/)

Một số thao tác tensor cơ bản thường gặp:
**1. Khởi tạo tensor:**

- Sử dụng hàm `empty` để tạo tensor chưa được khởi tạo giá trị.
- Sử dụng hàm `zeros` để tạo tensor với các phần tử đều bằng 0.
- Sử dụng hàm `ones` để tạo tensor với các phần tử đều bằng 1.
- Sử dụng hàm `full` để tạo tensor với các phần tử đều bằng một giá trị cụ thể.
- Sử dụng hàm `arange` để tạo tensor với các phần tử được sắp xếp theo dãy số.
- Sử dụng hàm `linspace` để tạo tensor với các phần tử được lấy mẫu đều đặn trong một khoảng.
- Sử dụng hàm `eye` để tạo ma trận đơn vị.
- Sử dụng hàm `from_numpy` để chuyển đổi mảng NumPy thành tensor.

**Ví dụ:**

Python

```
import torch

# Khởi tạo tensor 3x3 với các phần tử đều bằng 0
x = torch.zeros((3, 3))

# Khởi tạo tensor 2x4 với các phần tử đều bằng 5
y = torch.full((2, 4), 5)

# Khởi tạo tensor với các phần tử được sắp xếp theo dãy số từ 0 đến 9
z = torch.arange(10)
```

**2. Truy cập phần tử tensor:**

- Sử dụng dấu ngoặc vuông để truy cập phần tử theo vị trí.
- Sử dụng lát cắt để truy cập một tập con của tensor.
- Sử dụng hàm `index_select` để truy cập phần tử theo chỉ mục.

**Ví dụ:**

Python

```
# Truy cập phần tử ở vị trí (1, 2) của tensor x
x[1, 2]

# Truy cập hai hàng đầu tiên của tensor x
x[:2, :]

# Truy cập các cột 1 và 3 của tensor x
x[:, [1, 3]]

# Truy cập các phần tử chẵn của tensor z
z[::2]
```

**3. Thao tác toán học:**

- Có thể thực hiện các phép toán số học cơ bản như cộng, trừ, nhân, chia trên tensor.
- Hỗ trợ các phép toán so sánh như lớn hơn, nhỏ hơn, bằng nhau, v.v.
- Có thể thực hiện các phép toán ma trận như nhân ma trận, lấy nghịch đảo, v.v.

**Ví dụ:**

Python

```
# Cộng tensor x và y
x + y

# Nhân tensor x với 5
x * 5

# Lấy nghịch đảo của tensor x
torch.inverse(x)

# Kiểm tra xem tất cả các phần tử của tensor z đều lớn hơn 0
torch.all(z > 0)
```

**4. Thay đổi hình dạng tensor:**

- Sử dụng hàm `reshape` để thay đổi hình dạng của tensor.
- Sử dụng hàm `transpose` để hoán đổi vị trí các chiều của tensor.
- Sử dụng hàm `view` để thay đổi hình dạng tensor mà không cần tạo bản sao mới.

**Ví dụ:**

Python

```
# Thay đổi hình dạng tensor x thành (9, 1)
x.reshape((9, 1))

# Hoán đổi vị trí chiều 0 và chiều 1 của tensor x
x.transpose(0, 1)

# Thay đổi hình dạng tensor x thành (9, 1) mà không cần tạo bản sao mới
x.view((9, 1))
```

**5. Gộp tensor:**

- Sử dụng hàm `cat` để gộp các tensor theo một chiều cụ thể.
- Sử dụng hàm `stack` để gộp các tensor thành một tensor mới với một chiều bổ sung.

**Ví dụ:**

Python

```
# Gộp các tensor x và y theo chiều 0
torch.cat((x, y), 0)

# Gộp các tensor x, y và z thành một tensor mới với chiều thứ 4
torch.stack((x, y, z), 3)
```

