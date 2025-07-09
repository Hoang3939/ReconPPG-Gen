# ReconPPG-Gen – Tái tạo & Tạo sinh tín hiệu PPG từ dữ liệu HR và BR

Dự án **ReconPPG-Gen** là bài tập lớn/báo cáo giữa kỳ cho học phần dữ liệu lớn, thực hiện bởi sinh viên ngành Kỹ thuật phần mềm. Mục tiêu của dự án là **tái tạo tín hiệu PPG từ dữ liệu thực tế** và **tạo sinh tín hiệu PPG từ nhịp tim (HR) và nhịp thở (BR)**, thông qua việc huấn luyện các mô hình học sâu.

---

## Thông tin sinh viên
- **Họ và tên:** Nguyễn Huy Hoàng  
- **Lớp:** 23DPM  
- **MSSV:** 81012302865  

---

## Nội dung chính

### I. Cài đặt & Thư viện sử dụng
Dự án sử dụng các thư viện phổ biến trong học máy và xử lý tín hiệu:
- `NumPy`, `Pandas`, `Matplotlib`, `Seaborn`
- `scikit-learn`, `SciPy`, `wfdb`
- `TensorFlow`
- Một số thư viện phục vụ huấn luyện mô hình sinh (`diffusers`, `accelerate`)

### II. Tiền xử lý dữ liệu
- Tải và xử lý dữ liệu tín hiệu thực tế
- Chuẩn hóa dữ liệu HR, BR và PPG
- Cắt đoạn và lấy mẫu phù hợp cho mô hình học sâu

### III. Mô hình DenseCVAE
- Xây dựng kiến trúc Conditional Variational AutoEncoder với kết nối dày đặc
- Huấn luyện và đánh giá khả năng tái tạo tín hiệu PPG

### IV. Mô hình Conv1DCVAE
- Sử dụng mạng tích chập 1 chiều để xử lý chuỗi tín hiệu
- Mô hình có khả năng học tốt các đặc trưng dạng sóng thời gian

### V. Mô hình Transformer Generative
- Ứng dụng mô hình Transformer để tạo sinh tín hiệu PPG từ HR và BR
- Mô hình được huấn luyện để học mối quan hệ giữa HR/BR và chuỗi tín hiệu PPG đầu ra

### VI. Đánh giá và So sánh mô hình
- Trực quan hóa tín hiệu PPG được tái tạo/tạo sinh từ từng mô hình
- So sánh độ chính xác qua hình ảnh và metric định lượng
- Tổng hợp kết quả so sánh chất lượng giữa các mô hình DenseCVAE, Conv1DCVAE và Transformer

---

## Cấu trúc notebook

- `Reconstruct & Generate PPG.ipynb`: chứa toàn bộ mã nguồn, mô hình và kết quả trực quan
- `results/`: (tuỳ chọn) nơi lưu trữ hình ảnh và dữ liệu đầu ra nếu xuất riêng

---

## Yêu cầu môi trường

- Python >= 3.7
- TensorFlow
- scikit-learn, NumPy, Matplotlib, wfdb

---

## Liên hệ
Mọi góp ý và phản hồi vui lòng liên hệ:
Email: nguyenhuyhoang0943@gmail.com

## Ghi chú
Đây là bài báo cáo học thuật, không sử dụng vào mục đích thương mại.
Dữ liệu sử dụng mang tính tham khảo và phục vụ học tập.
