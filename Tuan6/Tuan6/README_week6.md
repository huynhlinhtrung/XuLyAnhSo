Xử lý Ảnh Số – Tuần 6

Notebook tuan6.ipynb thực hành template matching và cascade detection

Cấu trúc thư mục
Exercise6 gồm scene.jpg và template.png
Kết quả lưu vào tm_simple, tm_multiscale, cascade_detect

Yêu cầu phần mềm
opencv-python
numpy
matplotlib

Bài tập 1 template matching đơn giản
  Dùng cv2.matchTemplate với phương pháp TM_CCOEFF_NORMED
  Tìm vị trí khớp cao nhất, vẽ khung lên ảnh scene
  Lưu kết quả vào Exercise6/tm_simple

Bài tập 2 multi-scale matching
  Chạy matchTemplate trên nhiều tỷ lệ scale của template
  Lựa chọn khớp tốt nhất trên tất cả scale
  Lưu ảnh vào Exercise6/tm_multiscale

Bài tập 3 phát hiện đối tượng với Haar cascade
  Tải cascade pre-trained (ví dụ face hoặc custom)
  Áp dụng detectMultiScale trên scene.jpg
  Vẽ khung quanh đối tượng tìm được, lưu vào Exercise6/cascade_detect
