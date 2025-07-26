Xử lý Ảnh Số – Extra

Notebook Extra.ipynb mở rộng segment background và tracking

Cấu trúc thư mục
Extra chứa video.mp4 và thư mục frames
Video sẽ được xử lý xuất ra frames đã track

Yêu cầu phần mềm
opencv-python
numpy
matplotlib

Bài tập 1 segment background
  Dùng BackgroundSubtractorMOG2 hoặc KNN
  Áp dụng trên video.mp4, lưu frames foreground vào Extra/frames

Bài tập 2 tracking đối tượng
  Khởi tạo tracker KCF hoặc CSRT
  Định vị bounding box ban đầu, gọi tracker.update trên từng frame
  Vẽ đường đi và khung lên video, ghi video kết quả
