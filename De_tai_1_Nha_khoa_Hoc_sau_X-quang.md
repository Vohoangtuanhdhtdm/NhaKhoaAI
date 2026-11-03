# ĐỀ TÀI 1

# Nghiên cứu ứng dụng học sâu hỗ trợ bác sĩ đọc phim X-quang toàn cảnh tại phòng khám nha khoa quy mô nhỏ và vừa

> Tài liệu mô tả chi tiết đề tài, dùng làm cơ sở viết lại thuyết minh (.docx) và slide.
> Loại hình: **Nghiên cứu ứng dụng**. Lĩnh vực: Khoa học Kỹ thuật và Công nghệ.
> Đề tài **không nhằm mục tiêu công bố bài báo khoa học**.

---

## 1. Thông tin chung

| Mục | Nội dung |
|---|---|
| Tên đề tài | Nghiên cứu ứng dụng học sâu hỗ trợ bác sĩ đọc phim X-quang toàn cảnh tại phòng khám nha khoa quy mô nhỏ và vừa |
| Tên cũ (đã thay thế) | Xây dựng website quản lý phòng khám nha khoa tích hợp Voice AI Agent |
| Loại hình | Nghiên cứu ứng dụng |
| Thời gian | 06 tháng (10/2026 – 03/2027) |
| GVHD | ThS. Trần Bá Minh Sơn |
| Chủ nhiệm | Lê Thừa Quốc Anh – 2524802010014 – D25CNTT09 |
| Thành viên | Võ Hoàng Tuấn – 2224801030161 – D22KTPM03 |
| Kinh phí dự kiến | 4.900.000 đồng |

**Lưu ý thủ tục:** đổi tên và hướng đề tài cần GVHD đồng ý và kiểm tra quy định của Viện về thời hạn điều chỉnh đề tài đã đăng ký.

---

## 2. Tính cấp thiết

**Bối cảnh thực tế**
- Phim X-quang toàn cảnh (panoramic, OPG) được chụp cho phần lớn bệnh nhân khám lần đầu, trước khi niềng răng, nhổ răng khôn hay cấy implant.
- Bác sĩ phải tự rà soát toàn bộ cung răng trên phim. Việc này tốn thời gian và dễ bỏ sót tổn thương nhỏ (sâu răng giai đoạn sớm, tổn thương quanh chóp), nhất là khi phòng khám đông bệnh nhân.
- Phòng khám nhỏ và vừa thường không có bác sĩ chẩn đoán hình ảnh chuyên trách; bác sĩ điều trị tự đọc phim.

**Bối cảnh công nghệ**
- Học sâu đã đạt kết quả tốt trong phát hiện và đánh số răng trên phim toàn cảnh. Cuộc thi DENTEX (MICCAI 2023) đã công bố bộ dữ liệu chuẩn có nhãn do chuyên gia nha khoa thực hiện.
- Tuy nhiên, các mô hình được huấn luyện trên dữ liệu nước ngoài (DENTEX thu thập tại 3 bệnh viện ở Thổ Nhĩ Kỳ). **Chưa rõ mô hình còn dùng được đến đâu khi đưa về phòng khám Việt Nam** với máy chụp, quy trình chụp và đặc điểm bệnh nhân khác.

**Khoảng trống đề tài hướng tới**
Không phát triển thuật toán mới. Đề tài trả lời câu hỏi thực tiễn: *một phòng khám Việt Nam muốn áp dụng mô hình học sâu có sẵn thì cần điều chỉnh bao nhiêu, đạt độ chính xác bao nhiêu, và bác sĩ có thực sự được hỗ trợ hay không.*

---

## 3. Mục tiêu

### 3.1. Mục tiêu chung
Đánh giá khả năng áp dụng mô hình học sâu phát hiện và đánh số răng, khoanh vùng tổn thương trên phim X-quang toàn cảnh vào điều kiện thực tế của một phòng khám nha khoa quy mô nhỏ và vừa tại Việt Nam; đề xuất quy trình triển khai phù hợp.

### 3.2. Mục tiêu cụ thể
1. Xây dựng mô hình đánh số răng theo ký hiệu FDI và phát hiện 4 loại tổn thương (sâu răng, sâu răng sâu, tổn thương quanh chóp, răng ngầm) trên bộ dữ liệu công khai DENTEX.
2. Đo mức suy giảm độ chính xác khi áp dụng mô hình trên phim của phòng khám đối tác tại Việt Nam.
3. Xác định số lượng phim cục bộ cần thiết để tinh chỉnh mô hình đạt mức chấp nhận được.
4. Tích hợp mô hình vào website quản lý phòng khám (hiển thị gợi ý trên phim, bác sĩ xác nhận/sửa, tự điền sơ đồ răng).
5. Đánh giá tác động lên thời gian đọc phim và tỉ lệ bỏ sót tổn thương của bác sĩ.
6. Đề xuất khuyến nghị triển khai cho các phòng khám cùng quy mô.

---

## 4. Câu hỏi nghiên cứu

| Mã | Câu hỏi | Gắn với mục tiêu |
|---|---|---|
| CH1 | Mô hình huấn luyện trên dữ liệu công khai đạt độ chính xác bao nhiêu trên phim của phòng khám Việt Nam? Giảm bao nhiêu so với tập kiểm thử gốc? Loại tổn thương nào giảm nhiều nhất? | 1, 2 |
| CH2 | Tinh chỉnh với 30, 60, 100 phim cục bộ cải thiện kết quả đến mức nào? Cần khoảng bao nhiêu phim là đủ? | 3 |
| CH3 | Khi đọc phim có gợi ý của AI, thời gian đọc và số tổn thương bị bỏ sót của bác sĩ thay đổi thế nào so với tự đọc? | 4, 5 |

---

## 5. Đối tượng và phạm vi

**Đối tượng nghiên cứu:** mô hình học sâu phát hiện đối tượng trên ảnh X-quang toàn cảnh và quy trình ứng dụng mô hình vào công việc đọc phim của bác sĩ nha khoa.

**Phạm vi**
- Ảnh: chỉ phim X-quang toàn cảnh 2D. Không xử lý phim quanh chóp, cánh cắn hay CBCT 3D.
- Bệnh lý: 4 lớp theo DENTEX (Caries, Deep Caries, Periapical Lesion, Impacted Tooth).
- Đối tượng: phim của bệnh nhân từ 12 tuổi trở lên (giống điều kiện của DENTEX).
- Cơ sở thử nghiệm: 01 phòng khám nha khoa đối tác.
- Sản phẩm ở mức **nguyên mẫu thử nghiệm**. Hệ thống **chỉ hỗ trợ**; bác sĩ là người quyết định chẩn đoán. Không dùng để chẩn đoán tự động cho bệnh nhân.

---

## 6. Dữ liệu

### 6.1. Dữ liệu công khai: DENTEX
- Nguồn: DENTEX Challenge 2023 (MICCAI), tải tại Hugging Face / grand-challenge.
- Cấu trúc phân cấp:
  - 693 phim chỉ gán nhãn góc phần tư (quadrant);
  - 634 phim gán nhãn góc phần tư và số răng;
  - 1005 phim gán nhãn đầy đủ: góc phần tư, số răng, chẩn đoán;
  - 1571 phim chưa gán nhãn (dùng tiền huấn luyện nếu cần).
- Phần 1005 phim được chia sẵn 705 train / 50 validation / 250 test.
- Giấy phép: CC BY-NC-SA 4.0, cho phép dùng phi thương mại. Phải ghi nguồn trích dẫn đúng yêu cầu của tác giả.

### 6.2. Dữ liệu cục bộ: phòng khám đối tác
| Hạng mục | Yêu cầu |
|---|---|
| Số lượng | 150 phim toàn cảnh (tối thiểu 100) |
| Ẩn danh | Xóa tên, ngày sinh, mã bệnh nhân trên ảnh và trong metadata DICOM trước khi phòng khám giao |
| Gán nhãn | 01 bác sĩ nha khoa gán nhãn theo đúng 4 lớp và ký hiệu FDI, bằng công cụ CVAT hoặc Label Studio |
| Kiểm tra nhãn | 01 bác sĩ thứ hai kiểm tra ngẫu nhiên khoảng 20% số phim |
| Chia dữ liệu | **50 phim làm tập kiểm thử cố định** (không bao giờ dùng để huấn luyện); 100 phim còn lại làm kho tinh chỉnh, lấy lần lượt 30 / 60 / 100 phim |
| Thời gian thu thập | 2–3 tuần; gán nhãn khoảng 10–15 phút/phim |

**Phương án dự phòng nếu phòng khám chỉ cung cấp được ít phim (< 80):** giảm tập kiểm thử xuống 30 phim, chỉ thử 2 mức tinh chỉnh (20 và 50 phim), và nêu rõ đây là kết quả thí điểm.

---

## 7. Phương pháp nghiên cứu

### 7.1. Tổng quan quy trình

```
Khảo sát hiện trạng ──► Huấn luyện trên DENTEX ──► Đánh giá trên phim VN (zero-shot)
                                                        │
                                                        ▼
       Khuyến nghị ◄── Thực nghiệm với bác sĩ ◄── Tinh chỉnh 30/60/100 phim
                              ▲
                 Tích hợp vào website phòng khám
```

### 7.2. Các bước

| Bước | Nội dung | Phương pháp |
|---|---|---|
| B1. Khảo sát hiện trạng | Phỏng vấn 2–3 bác sĩ: số phim đọc mỗi ngày, thời gian đọc trung bình, loại tổn thương hay bỏ sót, cách ghi kết quả | Phỏng vấn bán cấu trúc, thống kê mô tả |
| B2. Mô hình nền | Huấn luyện YOLOv8 (thư viện Ultralytics) theo **hai giai đoạn**: (1) phát hiện và đánh số răng FDI; (2) phát hiện tổn thương, gán tổn thương vào răng bằng mức chồng lấn hộp (IoU) | Học chuyển giao từ trọng số tiền huấn luyện; tăng cường dữ liệu (độ sáng, tương phản, xoay nhẹ). **Không lật ngang ảnh** vì làm sai số răng trái/phải |
| B3. Đánh giá trên tập gốc | Đo trên 250 phim test của DENTEX | Làm mốc so sánh cho các bước sau |
| B4. Đánh giá zero-shot | Chạy mô hình nguyên vẹn trên 50 phim kiểm thử của phòng khám | Trả lời CH1 |
| B5. Tinh chỉnh | Tinh chỉnh với 30, 60, 100 phim cục bộ; mỗi mức chạy 3 lần với seed khác nhau, lấy trung bình | Vẽ đường cong "số phim – độ chính xác", trả lời CH2 |
| B6. Tích hợp | Đưa mô hình tốt nhất vào website: tải phim lên, hiện khung gợi ý, bác sĩ xác nhận/sửa, tự điền sơ đồ răng | Xây dựng phần mềm (mục 8) |
| B7. Thực nghiệm với bác sĩ | Nghiên cứu đọc phim (reader study), mục 9.2 | Trả lời CH3 |
| B8. Phân tích, khuyến nghị | Phân tích lỗi theo loại tổn thương, chất lượng phim; viết khuyến nghị triển khai | Thống kê mô tả, phân tích lỗi định tính |

### 7.3. Mốc so sánh (baseline)
- Mô hình chỉ huấn luyện trên DENTEX, không tinh chỉnh (B4).
- Bác sĩ đọc phim không có AI (B7).

Có baseline giúp mọi kết quả đều diễn giải được, kể cả khi mô hình không đạt kỳ vọng.

---

## 8. Hệ thống thử nghiệm

### 8.1. Kiến trúc

| Lớp | Thành phần | Công nghệ dự kiến |
|---|---|---|
| Giao diện | Trang hồ sơ bệnh nhân, trình xem phim có lớp phủ gợi ý, sơ đồ răng FDI | ReactJS |
| Ứng dụng | Quản lý bệnh nhân, phim, kết quả đọc; lưu lịch sử xác nhận/sửa của bác sĩ | Node.js hoặc FastAPI |
| Dịch vụ AI | API nhận ảnh, trả danh sách răng + tổn thương + độ tin cậy | Python, Ultralytics YOLOv8, ONNX Runtime |
| Dữ liệu | Cơ sở dữ liệu hồ sơ, kho ảnh, nhật ký đánh giá | PostgreSQL/MySQL, lưu trữ file |

### 8.2. Chức năng chính
1. Quản lý bệnh nhân và hồ sơ điều trị cơ bản (giữ lại từ website cũ, thu gọn).
2. Tải phim lên, AI phân tích, hiển thị khung tổn thương nghi ngờ trên phim.
3. Bác sĩ **chấp nhận / sửa / xóa** từng gợi ý; có thể thêm tổn thương AI bỏ sót.
4. Kết quả đã xác nhận tự điền vào sơ đồ răng và hồ sơ.
5. Ghi nhật ký: thời gian đọc, số gợi ý bị sửa/xóa. Dữ liệu này phục vụ đánh giá.
6. Ngưỡng độ tin cậy điều chỉnh được (ưu tiên độ nhạy cao, chấp nhận nhiều báo nhầm hơn).

### 8.3. Yêu cầu phi chức năng
- Thời gian phân tích một phim ≤ 5 giây trên máy chủ không có GPU (mục tiêu, sẽ đo thực tế).
- Phân quyền: chỉ bác sĩ được xác nhận kết quả.
- Giao diện ghi rõ "Gợi ý của AI – cần bác sĩ xác nhận".

---

## 9. Thực nghiệm và chỉ số đánh giá

### 9.1. Đánh giá mô hình (CH1, CH2)

| Chỉ số | Ý nghĩa | Ghi chú |
|---|---|---|
| mAP@0.5 | Độ chính xác phát hiện tổng hợp | Tính cho từng lớp bệnh và trung bình |
| **Độ nhạy (Sensitivity / Recall)** | Tỉ lệ tổn thương thật được phát hiện | **Chỉ số ưu tiên**: bỏ sót nguy hiểm hơn báo nhầm |
| Precision | Tỉ lệ gợi ý đúng | Đo mức "làm phiền" bác sĩ |
| Số báo nhầm trung bình / phim | Dễ hiểu với bác sĩ | |
| Độ chính xác đánh số răng | Tỉ lệ răng được gán đúng số FDI | |
| Thời gian suy luận | Giây / phim | Trên CPU và GPU |

So sánh: tập test DENTEX ↔ phim VN zero-shot ↔ phim VN sau tinh chỉnh 30/60/100.

### 9.2. Thực nghiệm với bác sĩ (CH3)

| Hạng mục | Thiết kế |
|---|---|
| Người tham gia | 2–3 bác sĩ nha khoa (khác bác sĩ đã gán nhãn đáp án) |
| Bộ phim | 30 phim trong tập kiểm thử cục bộ |
| Cách làm | Mỗi bác sĩ đọc 30 phim **2 lần**: lần không có AI và lần có AI; thứ tự phim xáo trộn |
| Thời gian nghỉ | Hai lần cách nhau **≥ 2 tuần** để giảm hiệu ứng nhớ phim |
| Đối trọng | Một nửa bác sĩ đọc "không AI" trước, nửa còn lại đọc "có AI" trước |
| Đáp án | Nhãn của bác sĩ gán nhãn ở mục 6.2 |
| Chỉ số | Thời gian đọc / phim; độ nhạy và số báo nhầm của bác sĩ; số gợi ý AI bác sĩ chấp nhận / sửa / bác bỏ; điểm SUS; phỏng vấn ngắn về mức độ tin tưởng |
| Phân tích | Thống kê mô tả; kiểm định Wilcoxon cho dữ liệu cặp nếu cỡ mẫu cho phép. Báo cáo dưới dạng **thực nghiệm thí điểm** do số bác sĩ ít |

### 9.3. Tiêu chí thành công (tham khảo, chốt sau thử nghiệm sơ bộ)
- Độ nhạy sau tinh chỉnh trên phim VN đạt tối thiểu bằng 90% độ nhạy trên tập test DENTEX.
- Thời gian đọc trung bình có AI không tăng so với không có AI.
- Độ nhạy của bác sĩ khi có AI không thấp hơn khi không có AI.

Nếu không đạt, đề tài vẫn có kết quả: chỉ ra được **điều kiện nào mô hình chưa dùng được** và cần bao nhiêu dữ liệu.

---

## 10. Nội dung nghiên cứu (dàn ý báo cáo)

| Chương | Nội dung |
|---|---|
| Mở đầu | Tính cấp thiết, mục tiêu, câu hỏi nghiên cứu, đối tượng, phạm vi, phương pháp |
| Chương 1 | Tổng quan: phim X-quang toàn cảnh, ký hiệu FDI, học sâu phát hiện đối tượng (YOLO), các bộ dữ liệu công khai (DENTEX, Tufts, OdontoAI), vấn đề lệch miền dữ liệu (domain shift), ứng dụng AI trong nha khoa tại Việt Nam |
| Chương 2 | Khảo sát hiện trạng đọc phim tại phòng khám đối tác |
| Chương 3 | Dữ liệu và mô hình: chuẩn bị dữ liệu, mô hình hai giai đoạn, kết quả trên DENTEX, zero-shot và tinh chỉnh |
| Chương 4 | Xây dựng hệ thống hỗ trợ đọc phim tích hợp website phòng khám |
| Chương 5 | Thực nghiệm với bác sĩ, thảo luận và khuyến nghị triển khai |
| Kết luận | Kết quả đạt được, hạn chế, hướng phát triển |

---

## 11. Tiến độ

| Thời gian | Công việc | Phụ trách chính |
|---|---|---|
| 10/2026 | Liên hệ phòng khám, xin thư đồng ý hợp tác; khảo sát hiện trạng; tải và tìm hiểu DENTEX | Quốc Anh |
| 11/2026 | Huấn luyện mô hình nền trên DENTEX (B2, B3); phòng khám ẩn danh và giao phim; bắt đầu gán nhãn | Tuấn (mô hình), Quốc Anh (dữ liệu) |
| 12/2026 | Hoàn tất gán nhãn; đánh giá zero-shot (B4); tinh chỉnh 30/60/100 (B5); bắt đầu xây website | Cả nhóm |
| 01/2027 | Tích hợp mô hình vào website; kiểm thử nội bộ; **lượt đọc thứ nhất** của bác sĩ (trước Tết) | Cả nhóm |
| 02/2027 | Nghỉ Tết (đầu tháng); khoảng nghỉ ≥ 2 tuần tự nhiên giữa hai lượt đọc; cuối tháng **lượt đọc thứ hai** | Quốc Anh |
| 03/2027 | Phân tích kết quả; viết khuyến nghị; hoàn thiện báo cáo và slide bảo vệ | Cả nhóm |

Kỳ nghỉ Tết được tận dụng làm khoảng nghỉ giữa hai lượt đọc của bác sĩ.

---

## 12. Sản phẩm

1. Hệ thống thử nghiệm: website hỗ trợ đọc phim X-quang toàn cảnh tích hợp mô hình học sâu.
2. Mô hình đã huấn luyện và tinh chỉnh, kèm mã nguồn và hướng dẫn chạy lại.
3. Bộ 150 phim cục bộ đã ẩn danh và gán nhãn (chỉ lưu nội bộ, theo thỏa thuận với phòng khám).
4. Báo cáo đánh giá thực nghiệm (mô hình và bác sĩ).
5. Tài liệu khuyến nghị triển khai cho phòng khám nha khoa quy mô nhỏ và vừa: cần bao nhiêu phim, yêu cầu chất lượng phim, ngưỡng độ tin cậy nên dùng, quy trình bác sĩ xác nhận.
6. Báo cáo tổng kết đề tài.

---

## 13. Kinh phí dự kiến

| Khoản mục | Số tiền (đồng) |
|---|---|
| Tài nguyên tính toán (GPU đám mây khi Colab/Kaggle miễn phí không đủ) | 1.200.000 |
| Bồi dưỡng bác sĩ gán nhãn và kiểm tra nhãn 150 phim | 1.500.000 |
| Bồi dưỡng bác sĩ tham gia thực nghiệm đọc phim | 900.000 |
| Máy chủ thử nghiệm, tên miền | 500.000 |
| In ấn báo cáo, tài liệu | 400.000 |
| Văn phòng phẩm, chi phí khác | 400.000 |
| **Tổng cộng** | **4.900.000** |

*(Bằng chữ: Bốn triệu chín trăm nghìn đồng.)* Các mức chi cần điều chỉnh theo định mức của trường.

---

## 14. Rủi ro và phương án xử lý

| Rủi ro | Mức độ | Phương án |
|---|---|---|
| Phòng khám không có máy chụp toàn cảnh hoặc không lưu phim | Cao | Hỏi ngay trong tháng 10; liên hệ song song 2–3 phòng khám hoặc trung tâm chụp X-quang nha khoa |
| Không đủ 150 phim | Trung bình | Phương án dự phòng ở mục 6.2 |
| Bác sĩ không đủ thời gian gán nhãn | Trung bình | Dùng mô hình gợi ý nhãn trước, bác sĩ chỉ sửa (giảm thời gian gán nhãn) |
| Mô hình kém với lớp "sâu răng" (tổn thương nhỏ) | Trung bình | Thử tăng độ phân giải ảnh đầu vào; báo cáo riêng từng lớp; đây vẫn là kết quả có giá trị |
| Thiếu GPU | Thấp | Colab/Kaggle miễn phí; dùng YOLOv8 bản nhỏ (n/s); khoản kinh phí GPU dự phòng |
| Võ Hoàng Tuấn làm song song 2 đề tài | Trung bình | Tuấn phụ trách phần mô hình (tập trung 11–12/2026); Quốc Anh phụ trách dữ liệu, website, thực nghiệm |

---

## 15. Đạo đức và bảo mật dữ liệu

- Có **văn bản đồng ý** của phòng khám về việc cung cấp phim cho mục đích nghiên cứu.
- Phim được ẩn danh **tại phòng khám** trước khi giao cho nhóm; nhóm không nhận thông tin định danh bệnh nhân.
- Dữ liệu cục bộ lưu trên thiết bị có mật khẩu, không đưa lên kho mã nguồn công khai, không chia sẻ ra ngoài nhóm.
- Tuân thủ quy định hiện hành của Việt Nam về bảo vệ dữ liệu cá nhân (dữ liệu sức khỏe là dữ liệu nhạy cảm).
- Thực nghiệm chỉ dùng phim đã có; **không ảnh hưởng đến việc điều trị** của bệnh nhân nào.
- Kết quả AI luôn hiển thị là gợi ý; quyết định chẩn đoán thuộc về bác sĩ.

---

## 16. Tài liệu tham khảo (dự kiến)

[1] Hamamci, I. E., Er, S., Simsar, E., et al. (2023). DENTEX: An abnormal tooth detection with dental enumeration and diagnosis benchmark for panoramic X-rays. arXiv:2305.19112.

[2] Bizjak, Ž., & Robič, T. (2024). Advancing dental caries detection in panoramic X-rays: A two-step deep learning approach. *Informatica Medica Slovenica*, 29(1).

[3] Panetta, K., Rajendran, R., Ramesh, A., Rao, S., & Agaian, S. (2022). Tufts Dental Database: A multimodal panoramic X-ray dataset for benchmarking diagnostic systems. *IEEE Journal of Biomedical and Health Informatics*, 26(4), 1650–1659.

[4] Silva, B. P. M., Pinheiro, L. B., Sobrinho, B. P. P., et al. (2023). Boosting research on dental panoramic radiographs: A challenging data set, baselines, and a task central online platform for benchmark. *Computer Methods in Biomechanics and Biomedical Engineering: Imaging & Visualization*, 11(4), 1327–1347.

[5] Redmon, J., Divvala, S., Girshick, R., & Farhadi, A. (2016). You only look once: Unified, real-time object detection. *Proceedings of CVPR*, 779–788.

[6] Jocher, G., Chaurasia, A., & Qiu, J. (2023). Ultralytics YOLOv8 [Phần mềm]. https://github.com/ultralytics/ultralytics

[7] Schwendicke, F., Samek, W., & Krois, J. (2020). Artificial intelligence in dentistry: Chances and challenges. *Journal of Dental Research*, 99(7), 769–774.

[8] Brooke, J. (1996). SUS: A "quick and dirty" usability scale. In *Usability Evaluation in Industry* (pp. 189–194). Taylor & Francis.

> Cần bổ sung: 1–2 công trình trong nước về ứng dụng AI trong nha khoa hoặc chẩn đoán hình ảnh y tế; kiểm tra lại thông tin xuất bản của [6], [7] trước khi đưa vào thuyết minh.

---

## 17. Việc cần làm ngay (tuần này)

- [ ] Trao đổi với GVHD về việc đổi tên và hướng đề tài.
- [ ] Liên hệ phòng khám đối tác, xác nhận 3 điều: có máy chụp toàn cảnh / lưu phim; đồng ý cung cấp ~150 phim ẩn danh; có bác sĩ gán nhãn.
- [ ] Tải bộ DENTEX, chạy thử YOLOv8 bản nhỏ trên Colab để ước lượng thời gian huấn luyện.
- [ ] Soạn mẫu thư đồng ý hợp tác và cam kết bảo mật dữ liệu.
