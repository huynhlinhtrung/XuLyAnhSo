Xử lý Ảnh Số – Tuần 1
Notebook `tuan1.ipynb` gồm 5 bài tập cơ bản về đọc/ghi ảnh, thao tác kênh màu, chuyển đổi không gian màu và áp dụng bộ lọc.

Yêu cầu
- Python ≥ 3.6  
- OpenCV, NumPy, Matplotlib  
  bash
  pip install opencv-python numpy matplotlib 
- Thư mục chứa:
  .
  ├── tuan1.ipynb
  ├── bird.png          # Ảnh mẫu cho Bài 1–4
  └── Exercise/         # Ảnh mẫu cho Bài 5
      ├── img1.jpg
      ├── img2.png
      └── …
  ```

Cách chạy
1. Mở terminal, chuyển vào thư mục chứa `tuan1.ipynb`.  
2. Chạy:
   ```bash
   jupyter notebook
   ```  
3. Chạy lần lượt từng cell trong notebook.

Bài 1 – Tách & lưu từng kênh màu (BGR)

1. Nhập thư viện
   ```python
   import os
   import cv2
   import numpy as np
   import matplotlib.pyplot as plt
   ```
2. Tạo thư mục lưu ảnh 
   ```python
   os.makedirs('output_images', exist_ok=True)
   ```
3. Đọc ảnh 
   ```python
   img = cv2.imread('bird.png')  # BGR
   ```
4. Tách kênh màu
   ```python
   b, g, r = cv2.split(img)
   ```
5. Tạo ảnh chỉ giữ mỗi kênh  
   ```python
   zero = np.zeros_like(b)
   blue_img  = cv2.merge([b, zero, zero])
   green_img = cv2.merge([zero, g, zero])
   red_img   = cv2.merge([zero, zero, r])
   ```
6. Lưu ảnh  
   ```python
   cv2.imwrite('output_images/blue.png',  blue_img)
   cv2.imwrite('output_images/green.png', green_img)
   cv2.imwrite('output_images/red.png',   red_img)
   ```
7. Hiển thị ảnh trong notebook  
   ```python
   plt.figure(figsize=(12,4))
   plt.subplot(1,4,1); plt.title('Original'); plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB)); plt.axis('off')
   plt.subplot(1,4,2); plt.title('Blue');    plt.imshow(cv2.cvtColor(blue_img, cv2.COLOR_BGR2RGB)); plt.axis('off')
   plt.subplot(1,4,3); plt.title('Green');   plt.imshow(cv2.cvtColor(green_img, cv2.COLOR_BGR2RGB)); plt.axis('off')
   plt.subplot(1,4,4); plt.title('Red');     plt.imshow(cv2.cvtColor(red_img, cv2.COLOR_BGR2RGB)); plt.axis('off')
   plt.show()
   ```

Bài 2 – Hoán đổi kênh màu

1. Đọc ảnh
   ```python
   img = cv2.imread('bird.png')
   ```
2. Hoán đổi kênh
   swapped = img[..., [2,1,0]]  # B ↔ R
   ```
3. Lưu ảnh
   ```python
   cv2.imwrite('output_images/swapped.png', swapped)
   ```
4. Hiển thị 
   ```python
   plt.imshow(cv2.cvtColor(swapped, cv2.COLOR_BGR2RGB))
   plt.title('Swapped B↔R'); plt.axis('off'); plt.show()
   ```

Bài 3 – Chuyển sang HSV & tách kênh

1. Chuyển BGR → HSV 
   ```python
   hsv_img = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)
   ```
2. Tách kênh H, S, V  
   ```python
   h, s, v = cv2.split(hsv_img)
   ```
3. Tạo ảnh mỗi kênh
   ```python
   max_ch = np.full_like(h, 255)
   hue_img        = cv2.merge([h, max_ch, max_ch])
   saturation_img = cv2.merge([max_ch, s, max_ch])
   value_img      = cv2.merge([max_ch, max_ch, v])
   ```
4. Lưu & hiển thị** tương tự bài 1.

Bài 4 – Điều chỉnh Hue & Value

1. Chia nhỏ H & V  
   ```python
   h2 = (h / 3).astype(np.uint8)
   v2 = (v / 3).astype(np.uint8)
   hsv_mod = cv2.merge([h2, s, v2])
   result_img = cv2.cvtColor(hsv_mod, cv2.COLOR_HSV2BGR)
   ```
2. Lưu & hiển thị tương tự bài 1.

Bài 5 – Lọc trung bình (Mean Filter)

```python
input_dir  = 'Exercise/'
output_dir = 'Exercise/output/'
os.makedirs(output_dir, exist_ok=True)

for fname in os.listdir(input_dir):
    if fname.lower().endswith(('.jpg','.png')):
        img_i = cv2.imread(os.path.join(input_dir, fname))
        filtered = csv2.blur(img_i, (5,5))
        cv2.imwrite(os.path.join(output_dir, fname), filtered)
```

