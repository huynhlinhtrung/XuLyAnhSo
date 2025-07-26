Xử lý Ảnh Số – Tuần 4

Notebook tuan4.ipynb tập trung vào phân tích tín hiệu và lọc tần số trong miền Fourier

Cấu trúc thư mục
Exercise4 chứa các file ảnh freq1.jpg và freq2.png
Kết quả lọc sẽ tạo thêm thư mục lowpass, highpass, bandstop

Yêu cầu phần mềm
opencv-python
numpy
matplotlib
scipy

Bài tập 1 biến đổi Fourier
  Đọc ảnh, chuyển sang miền tần số bằng FFT2
  Tính phổ biên độ, hiển thị ảnh phổ với log scale

Bài tập 2 lọc tần số thấp
  Thiết kế filter lý tưởng low-pass (cắt bỏ tần số cao trên cutoff)
  Áp dụng vào phổ, thực hiện inverse FFT
  Lưu ảnh gộp vào Exercise4/lowpass

Bài tập 3 lọc tần số cao
  Thiết kế filter high-pass (loại bỏ tần số thấp dưới cutoff)
  Áp dụng tương tự, lưu vào Exercise4/highpass

Bài tập 4 lọc band-stop
  Xác định dải tần trung bình cần loại bỏ
  Áp dụng band-stop filter, lưu vào Exercise4/bandstop

Lưu ý thực nghiệm với các cutoff khác nhau để quan sát kết quả
