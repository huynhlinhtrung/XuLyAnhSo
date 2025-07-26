Xử lý Ảnh Số – Tuần 3

Notebook tuan3.ipynb gồm 4 bài tập về cân bằng histogram, ngưỡng, toán học hình thái và phân đoạn màu

Cấu trúc thư mục
Exercise3/
    imgA.jpg
    imgB.png

Yêu cầu
pip install opencv-python numpy matplotlib

Chi tiết các bài tập
1. cân bằng histogram
   - áp dụng histogram equalization trên ảnh xám và từng kênh BGR
   - lưu kết quả vào equalized/

2. ngưỡng
   - sử dụng threshold cố định và adaptive threshold
   - lưu ảnh vào thresholds/

3. toán học hình thái
   - thực hiện erosion, dilation, opening, closing với kernel 3x3
   - lưu vào morph/

4. phân đoạn màu
   - chuyển sang HSV, áp dụng ngưỡng H,S,V để tách đối tượng
   - lưu vào segmented/

Chúc bạn thực hành thành công
