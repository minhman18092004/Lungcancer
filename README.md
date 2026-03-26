<<<<<<< HEAD
# Lung Cancer CT Classification

Dự án phân loại ảnh CT phổi thành 3 lớp:

- Benign cases
- Malignant cases
- Normal cases

Mã nguồn chính được xây dựng dưới dạng Jupyter Notebook, bao gồm các mô hình CNN cơ bản, MobileNet, EfficientNet và các biến thể fusion/attention.

## 1. Cấu trúc thư mục

```text
Dataset/
  Benign cases/
  Malignant cases/
  Normal cases/

LungCancer/
  efficientnet_b0/
    efficientnet_b0.pth
    efficientnetb0.ipynb
  efficientnet_b1/
    efficientnet_b1.pth
    efficientnetb1.ipynb
  mobilenet_v1/
    mobilenet_v1.pth
    mobilenetv1.ipynb
  mobilenet_v2/
    mobilenet_v2.pth
    mobilenetv2.ipynb
  mobilenet_v3_large/
    mobilenet_v3_large.pth
    mobilenetv3large.ipynb
  mobilenet_v3_small/
    mobilenet_v3_small.pth
    mobilenetv3small.ipynb

Src/
  CNN.ipynb
  fusionmodelACMix_Film.ipynb
  fusionmodelAttention.ipynb
```

## 2. Dữ liệu

Dự án sử dụng bộ dữ liệu IQ-OTH/NCCD Lung Cancer Dataset (CT scan), phân loại đa lớp (3 classes).

Trong workspace hiện tại, dữ liệu được đặt tại:

- `Dataset/Benign cases`
- `Dataset/Malignant cases`
- `Dataset/Normal cases`

Lưu ý: một số notebook đang để sẵn đường dẫn kiểu Kaggle hoặc Google Drive. Cần sửa lại biến đường dẫn trước khi chạy (ví dụ `DATASET_PATH`, `data`, `MODEL_DIR`, `pth`).

## 3. Yêu cầu môi trường

Khuyến nghị:

- Python 3.9+
- CUDA (tuỳ chọn, giúp train nhanh hơn)
- Jupyter Notebook hoặc VS Code Notebook

Thư viện chính (theo notebook):

- torch
- torchvision
- numpy
- pandas
- matplotlib
- seaborn
- pillow
- scikit-learn
- tqdm

Cài nhanh:

```bash
pip install torch torchvision numpy pandas matplotlib seaborn pillow scikit-learn tqdm jupyter
```

## 4. Cách chạy

### Bước 1: Mở notebook

Bạn có thể bắt đầu từ:

- `Src/CNN.ipynb` (pipeline CNN baseline)
- `LungCancer/efficientnet_b0/efficientnetb0.ipynb`
- `LungCancer/efficientnet_b1/efficientnetb1.ipynb`
- `LungCancer/mobilenet_v1/mobilenetv1.ipynb`
- `LungCancer/mobilenet_v2/mobilenetv2.ipynb`
- `LungCancer/mobilenet_v3_large/mobilenetv3large.ipynb`
- `LungCancer/mobilenet_v3_small/mobilenetv3small.ipynb`
- `Src/fusionmodelAttention.ipynb`
- `Src/fusionmodelACMix_Film.ipynb`

### Bước 2: Sửa đường dẫn dữ liệu/model

Tìm các biến đường dẫn trong notebook và cập nhật theo máy cục bộ, ví dụ:

```python
DATASET_PATH = "./Dataset"
MODEL_DIR = "./LungCancer"
```

### Bước 3: Chạy tuần tự từng cell

- Tiền xử lý dữ liệu và augmentation
- Tạo DataLoader train/val/test
- Khởi tạo model
- Train
- Đánh giá (accuracy, confusion matrix, classification report)
- Lưu trọng số `.pth`

## 5. Trọng số mô hình

Repo đã có sẵn các file trọng số `.pth` trong từng thư mục mô hình dưới `LungCancer/`.

Bạn có thể:

- dùng lại để inference/đánh giá
- hoặc train lại để tái lập kết quả

## 6. Ghi chú

- Nhiều notebook được viết cho môi trường Kaggle/Colab, nên cần chỉnh path khi chạy local.
- Các notebook có thể có khác biệt về batch size, epoch, augmentation và cách chia tập train/val/test.
- Nếu dùng GPU, hãy kiểm tra `torch.cuda.is_available()` trước khi train.

## 7. Hướng phát triển

- Chuẩn hoá cấu hình vào một file chung (YAML/JSON)
- Tách notebook thành script/module để dễ tái sử dụng
- Thêm `requirements.txt` và `train.py`/`inference.py`
- Bổ sung quy trình đánh giá nhất quán giữa các kiến trúc
=======
# Lungcancer
>>>>>>> 5f8b1efe1a276db03c8f9df2c98f3697ce666255
