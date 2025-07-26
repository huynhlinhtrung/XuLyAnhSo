Xử lý Ảnh Số – Tuần 8

Notebook tuan8.ipynb giới thiệu CNN cơ bản để phân loại ảnh

Cấu trúc thư mục
Exercise8 chia thành train và test
Mỗi thư mục chứa nhiều subfolder theo class

Yêu cầu phần mềm
tensorflow
keras
numpy
matplotlib

Bài tập 1 xây dựng CNN đơn giản
  Định nghĩa Sequential model với Conv, Pool, Dense
  Biên dịch model với optimizer Adam và loss categorical_crossentropy
  Train trên dữ liệu Exercise8/train

Bài tập 2 đánh giá model
  Đánh giá accuracy và loss trên Exercise8/test
  Hiển thị biểu đồ training vs validation

Bài tập 3 lưu và nạp model
  Lưu model dưới dạng file .h5
  Load lại từ file và kiểm thử dự đoán trên ảnh sample
