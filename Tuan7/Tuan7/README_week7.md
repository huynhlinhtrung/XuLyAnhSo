Xử lý Ảnh Số – Tuần 7

Notebook tuan7.ipynb hướng dẫn ghép ảnh panorama

Cấu trúc thư mục
Exercise7 chứa left.jpg và right.jpg
Kết quả lưu vào panorama

Yêu cầu phần mềm
opencv-python
numpy
matplotlib

Bài tập 1 phát hiện và khớp keypoint
  Khởi tạo ORB detector, tìm keypoint và descriptor
  Dùng BFMatcher để ghép cặp descriptor
  Lọc matches tốt bằng ratio test

Bài tập 2 tính homography và warp ảnh
  Dùng các match tốt để tính ma trận H với RANSAC
  Warp one image vào không gian ảnh còn lại
  Ghép và cắt crop panorama, lưu vào Exercise7/panorama
