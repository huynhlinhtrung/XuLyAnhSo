

pip install opencv-python numpy matplotlib

Xử lý Ảnh Số – Tuần 2

Notebook tuan2.ipynb gồm 4 bài tập thực hành về xử lý ảnh số: khử nhiễu, phát hiện biên, và thay đổi màu sắc ảnh.

1. Cấu trúc thư mục

.
tuan2.ipynb                (Notebook chính)
Exercise/                  (Thư mục chứa ảnh đầu vào)
filtered_mean/             (Ảnh sau lọc trung bình - mean)
filtered_gaussian/         (Ảnh sau lọc Gaussian)
filtered_median/           (Ảnh sau lọc median)
edge_detected_images/      (Ảnh sau phát hiện biên)
random_rgb/                (Ảnh đổi màu RGB ngẫu nhiên)
random_hsv/                (Ảnh đổi màu HSV ngẫu nhiên)

2. Cài đặt môi trường

Cài các thư viện Python cần thiết:

pip install opencv-python numpy matplotlib

3. Hướng dẫn thực hiện các bài tập

Bài 1: Khử nhiễu và so sánh bộ lọc
  Đọc tất cả ảnh trong thư mục Exercise/.
  Áp dụng lần lượt 3 bộ lọc: mean, Gaussian, median cho từng ảnh.
  Lưu kết quả vào các thư mục tương ứng: filtered_mean/, filtered_gaussian/, filtered_median/.
  So sánh hiệu quả các bộ lọc bằng cách quan sát trực quan.

Bài 2: Phát hiện biên
  Sử dụng ảnh đã khử nhiễu (chọn bộ lọc tốt nhất từ Bài 1).
  Áp dụng các phương pháp phát hiện biên: Sobel và Canny.
  Lưu ảnh kết quả vào thư mục edge_detected_images/.

Bài 3: Đổi màu RGB ngẫu nhiên
  Sử dụng ảnh đã khử nhiễu.
  Thay đổi giá trị RGB của từng pixel bằng một giá trị ngẫu nhiên (giữ nguyên cấu trúc ảnh).
  Lưu ảnh kết quả vào thư mục random_rgb/.

Bài 4: Đổi màu HSV ngẫu nhiên
  Sử dụng ảnh đã khử nhiễu.
  Chuyển ảnh sang không gian màu HSV.
  Thay đổi ngẫu nhiên giá trị của một trong ba kênh H, S hoặc V (không trùng kênh cho mỗi ảnh).
  Chuyển lại sang RGB và lưu vào thư mục random_hsv/.


