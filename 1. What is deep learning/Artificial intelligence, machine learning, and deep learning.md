![[1.1 AI, machine learning and deep learning.png]]

### <span style="color:rgb(0, 176, 240)">1. Artificial Intelligence</span>
- Một cách chính xác: AI được mô tả là _<span style="color:rgb(221, 95, 217)">nỗ lực tự động hóa các nhiệm vụ trí tuệ thường được thực hiện bởi con người</span>_
	>AI là một lĩnh vực chung bao gồm học máy và học sâu, nhưng cũng bao gồm nhiều cách tiếp cận khác có thể không liên quan đến bất kỳ việc học nào.
### <span style="color:rgb(0, 176, 240)">2. Machine Learning</span> 
- [Machine learning là gì](https://topdev.vn/blog/machine-learning-la-gi/)
- machine learning workflow:
	- data collection -> preproccessing -> training model -> evaluating model -> Improve
- Phân loại:
	- [Supervisor learning](obsidian://open?vault=deep%20learning&file=1.%20What%20is%20deep%20learning%2FCh%C3%BA%20th%C3%ADch%2FSupervised%20learning) học có giám sát
	- [Unsupervised learning](obsidian://open?vault=deep%20learning&file=1.%20What%20is%20deep%20learning%2FCh%C3%BA%20th%C3%ADch%2FUnsupervised%20learning): học không có giám sát
- Mô hình ML:
![[Pasted image 20240702220127.png]]

### <span style="color:rgb(0, 176, 240)">3. Learning rules and representations from data</span>
Để định nghĩa deep learning và hiểu sự khác biệt giữa deep learning với các phương pháp học máy khác, thì đầu tiên cần một số ý tưởng về chức năng của thuật toán chức năng của học máy(ML)
Ở trên, chúng ta đã thấy rằng ML tìm ra quy luật để thực hiện tác vụ xử lý data. Vì thế, để học máy, chúng ta cần 3 thứ:
- Nhập [data point](obsidian://open?vault=deep%20learning&file=1.%20What%20is%20deep%20learning%2FCh%C3%BA%20th%C3%ADch%2Fdata%20points): ví dụ, trong tác vụ xử lý giọng nói,thì data point có thể là bản ghi âm do con người tạo ra. Trong xử lý ảnh thì có thể là hình ảnh
- Ví dụ về output dự kiến: trong xử lý giọng nói thì output dự kiến có thể là giọng con người. Trong xử lý ảnh thì output dự kiến có thể là 'chó' hoặc 'mèo'
- Cách để đánh giá thuật toán có hoạt động tốt hay không: Điều này là cần thiết để <span style="color:rgb(66, 255, 242)">xác định khoảng cách giữa output hiện tại và output dự kiến</span> của thuật toán. Phép đo được sử dụng là tạo tín hiệu feedback để hiệu chỉnh cách thuật toán hoạt động -> <span style="color:rgb(221, 95, 217)">bước chỉnh sửa</span> được gọi là <span style="color:rgb(221, 95, 217)">learning</span>.
Một model ML <span style="color:rgb(221, 95, 217)">biến đổi dữ liệu đầu vào</span> thành những<span style="color:rgb(221, 95, 217)"> dữ liệu có nghĩa</span> - quá trình 'học' từ sơ khai đến hiểu rõ. Vì thế, <span style="color:rgb(221, 95, 217)">vấn đề cốt lõi</span> của ML và deep learning là <span style="color:rgb(221, 95, 217)">chuyển đổi dữ liệu một cách có nghĩa</span>, hay nói cách khác, học cách <span style="color:rgb(221, 95, 217)">biểu diễn dữ liệu đầu vào hiệu quả</span> để tiến tới output dự kiến.
Vậy thì nên biểu diễn như thế nào? Ví dụ: Một hình ảnh có thể được mã hóa dạng RGB hoặc HSV(hue-saturation-value). Trong 1 số trường hợp thì một tác vụ có thể gặp khó khăn với định dạng RGB nhưng với HSV thì ngược lại như tăng độ bão hòa của ảnh,... Các model ML đều nhằm tìm kiếm các cách biểu diễn phù hợp cho dữ liệu đầu vào để xử lý tác vụ 
Ví dụ cụ thể:
- Xác định tọa độ của 1 điểm và dự đoán điểm này màu đen hay trắng
![[Pasted image 20240703000901.png]]
Ở đây:
- Đầu vào là tọa độ các điểm
- Đầu ra dự kiến là màu sắc của các điểm
Thứ chúng ta cần là 1 cách mới để biểu diễn dữ liệu sao cho các điểm trắng và đen tách biệt nhau, ví dụ như đổi trục tọa độ:![[Pasted image 20240703003020.png]]
Vấn đề phân loại đen/trắng có thể được diễn đạt thành một quy tắc đơn giản: "Các điểm đen là những điểm có x > 0," hoặc "Các điểm trắng là những điểm có x < 0."
Các <span style="color:rgb(221, 95, 217)">thuật toán học máy thường không sáng tạo</span> trong việc tìm kiếm các phép biến đổi này; chúng chỉ <span style="color:rgb(221, 95, 217)">đơn giản là tìm kiếm qua một tập hợp các thao tác được xác định trước, gọi là không gian giả thuyết</span>. Ví dụ, không gian của tất cả các phép thay đổi tọa độ có thể có sẽ là không gian giả thuyết của chúng ta trong ví dụ phân loại tọa độ 2D.
Vậy <span style="color:rgb(221, 95, 217)">học máy</span> là gì,1 cách ngắn gọn: <span style="color:rgb(221, 95, 217)">tìm kiếm các biểu diễn và quy tắc hữu ích trên một số dữ liệu đầu vào, trong một không gian khả năng được xác định trước, sử dụng sự hướng dẫn từ một tín hiệu phản hồi</span>. Ý tưởng đơn giản này cho phép giải quyết một loạt các tác vụ cần trí tuệ, từ nhận dạng giọng nói đến lái xe tự hành.

### <span style="color:rgb(0, 176, 240)">4."Deep" in Deep learning</span>
- <span style="color:rgb(221, 95, 217)">Học sâu</span> là một <span style="color:rgb(221, 95, 217)">lĩnh vực của học máy</span>, tập trung vào việc học các lớp biểu diễn có nghĩa từ dữ liệu. 
- Từ "<span style="color:rgb(221, 95, 217)">sâu</span>" chỉ sự độ sâu của các lớp, không phải là sự sâu sắc. Độ sâu của mô hình là số lượng lớp biểu diễn. 
- Các lớp được học thông qua [mạng neuron](obsidian://open?vault=deep%20learning&file=1.%20What%20is%20deep%20learning%2FCh%C3%BA%20th%C3%ADch%2Fm%E1%BA%A1ng%20neuron) (neural network) 
- Về mặt kĩ thuật: Deep learning là cách học các biểu diễn dữ liệu qua nhiều giai đoạn
### <span style="color:rgb(0, 176, 240)">5.Understanding how deep learning works, in three figures</span> 
Các <span style="color:rgb(221, 95, 217)">trọng số của một lớp</span> trong mạng neural <span style="color:rgb(221, 95, 217)">lưu trữ cách mà lớp đó xử lý dữ liệu đầu vào</span>. Học(learning) trong ngữ cảnh này có nghĩa là <span style="color:rgb(66, 255, 242)">tìm ra các giá trị cho các trọng số của tất cả các lớp trong mạng để mạng có thể ánh xạ chính xác các đầu vào với mục tiêu liên quan</span>. 
Một mạng neuron có thể chứa hàng chục triệu tham số, và việc tìm ra các giá trị chính xác cho tất cả chúng là một nhiệm vụ phức tạp vì thay đổi một tham số sẽ ảnh hưởng đến hành vi của tất cả các tham số khác.
![[Pasted image 20240704002332.png]]

Để kiểm soát đầu ra của một mạng neural, trước tiên cần đo lường được khoảng cách giữa đầu ra dự đoán của mạng và kết quả mục tiêu mong đợi. Việc này được thực hiện thông qua [loss function](obsidian://open?vault=deep%20learning&file=1.%20What%20is%20deep%20learning%2FCh%C3%BA%20th%C3%ADch%2Floss%20function) của mạng, còn được gọi là hàm mục tiêu hoặc hàm chi phí. Loss function nhận các dự đoán của mạng và kết quả thực tế, sau đó tính ra _loss score_, cho biết mạng đã hoạt động như thế nào đối với ví dụ cụ thể đó.
![[Pasted image 20240704003607.png]]

Trick cơ bản trong học sâu là sử dụng _loss score_ để điều chỉnh giá trị của các trọng số, nhằm giảm hao hụt cho từng ví dụ cụ thể. Quá trình điều chỉnh này do [[optimizer]] (bộ tối ưu hóa) thực hiện, triển khai thuật toán[[ Backpropagation ]] (truyền ngược của sai số), thuật toán cốt lõi của học sâu.
![[Pasted image 20240704004416.png]]
