Xử lý Ảnh Số – Thi thử

Notebook thithu.ipynb là bài thi thử bao gồm 5 bài tập tổng hợp kiến thức tuần 1–8

Cấu trúc thư mục
Exercises/
    exam_images/     chứa các ảnh dùng cho đề thi
    templates/       chứa file template cần match
    model/           chứa mô hình sample (tuần 8)

Yêu cầu phần mềm
opencv-python
numpy
matplotlib
tensorflow
scipy

Bài tập 1 tách kênh màu và hiển thị
  Đọc ảnh exam_images/img_test1.png
  Tách và hiển thị kênh B, G, R cạnh nhau

Bài tập 2 chuyển đổi không gian màu
  Chuyển BGR sang HSV
  Tách H, S, V và tạo ảnh kết quả

Bài tập 3 lọc và biên
  Khử nhiễu với Gaussian filter
  Dò biên bằng Canny

Bài tập 4 phát hiện template
  Dùng matchTemplate với file trong templates/template1.png
  Vẽ khung bao quanh kết quả khớp tốt nhất

Bài tập 5 phân loại ảnh với CNN
  Tải model sample từ model/model.h5
  Nạp tập test images exam_images/test_set
  Dự đoán nhãn và in accuracy

Lưu kết quả vào thư mục output/ tương ứng với mỗi bài tập

Chúc bạn làm bài tốt