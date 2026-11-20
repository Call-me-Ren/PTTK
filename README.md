# ĐỒ ÁN MÔN HỌC PHÂN TÍCH THIẾT KẾ HƯỚNG ĐỐI TƯỢNG — NHÓM 8

> **Đề tài 8:** **Hệ thống đặt phòng và quản lý khách sạn (Hotel Booking & Management System)**  
> **Học phần:** Phân tích thiết kế hướng đối tượng (`841111`) — Lớp Chiều Thứ 6  
> **Trường:** Đại học Sài Gòn (SGU)  
> **Thời gian thực hiện:** `21/11/2026` $\rightarrow$ `05/12/2026` (2 tuần)

---

## 1. Danh sách Thành viên Nhóm 8 (5 thành viên) & Phân công Cụm Use Case

| STT | MSSV | Họ và Tên | Cụm Use Case Phụ trách (Xuyên suốt từ Đặc tả $\rightarrow$ Thiết kế $\rightarrow$ Giao diện & Demo) |
| :---: | :---: | :--- | :--- |
| **1** | `3124411275` | **Đặng Phú Thành** | **Cụm 1:** Tìm phòng trống theo khoảng ngày & loại phòng, Đặt phòng trực tuyến/OTA, Áp dụng mã khuyến mãi (`<<extend>>`), Đặt cọc & Sửa/Hủy đặt phòng |
| **2** | `3124411049` | **Nguyễn Trí Cường** | **Cụm 2:** Nhận phòng (Check-in & gán phòng cụ thể), Đổi phòng (`<<include>>` Kiểm tra phòng trống), Sơ đồ phòng theo ngày cho lễ tân & Gửi thông báo lưu trú cơ quan công an |
| **3** | `3124411267` | **Võ Huỳnh Thanh Tâm** | **Cụm 3:** Ghi nhận dịch vụ phát sinh (Minibar, giặt là, nhà hàng) vào `Folio`, Trả phòng (Check-out), Tổng quát hóa Thanh toán (Thẻ / Chuyển khoản / Tiền mặt) & Xuất hóa đơn |
| **4** | — | **Nguyễn Hoài Quân** | **Cụm 4:** Quản lý tình trạng buồng phòng (Housekeeping: `Trống bẩn → Đang dọn → Trống sạch`), Quản lý bảo trì phòng (`Bảo trì`) & Quản lý hồ sơ khách lưu trú |
| **5** | `3124411142` | **Lê Anh Kiệt** | **Cụm 5:** Cấu hình giá theo mùa (`Season`) & cuối tuần (`RatePlan`), Báo cáo công suất phòng & Thiết kế Kiến trúc tổng thể, Thành phần, Triển khai |

---

## 2. Danh mục Tài liệu Điều hướng Trung tâm (Core Project Documents)

| Tệp tài liệu | Mô tả vai trò | Đối tượng sử dụng |
| :--- | :--- | :--- |
| [YEU_CAU_DO_AN.md](file:///d:/Mon_hoc_dai_hoc_sgu/PTTK/YEU_CAU_DO_AN.md) | **Tổng hợp nguyên văn 100%** mọi yêu cầu chung, cấu trúc báo cáo, lộ trình 12 tuần, chi tiết Đồ án 8, danh sách nhóm từ Excel và bảng tài liệu tham khảo của giảng viên. | Toàn bộ 5 thành viên & AI Agent |
| [RULE.md](file:///d:/Mon_hoc_dai_hoc_sgu/PTTK/RULE.md) | **Bộ quy tắc kỹ thuật & nghiệp vụ bắt buộc:** Chuẩn UML 2.5.1, 3 quan hệ Use Case, mô hình lớp (`RoomType` vs `Room`, `Booking` vs `Stay`, `DateRange`), 2 State Diagrams, công thức chống chồng lấn $[a_1, b_1) \cap [a_2, b_2)$, Luật Cư trú 23h/8h, Adapter và Web Demo. | Toàn bộ 5 thành viên & AI Agent |
| [PLAN.md](file:///d:/Mon_hoc_dai_hoc_sgu/PTTK/PLAN.md) | **Kế hoạch hành động A–Z trong 14 ngày (21/11 $\rightarrow$ 05/12/2026):** Lịch trình từng ngày cho 5 thành viên từ khảo sát, vẽ sơ đồ, viết báo cáo đến xây dựng Web Demo và bảo vệ. | Toàn bộ 5 thành viên |
| [INSTRUCTION.md](file:///d:/Mon_hoc_dai_hoc_sgu/PTTK/INSTRUCTION.md) | **Hướng dẫn kỹ thuật cho AI Agent:** Từ điển lớp chuẩn hóa, mẫu bảng đặc tả Use Case (Fully Dressed), chuẩn sinh mã PlantUML, kiến trúc Web Demo và 6 câu hỏi phản biện trọng tâm. | AI Agent & Thành viên khi prompt AI |
| [AGENTS.md](file:///d:/Mon_hoc_dai_hoc_sgu/PTTK/AGENTS.md) | **Định nghĩa 6 vai trò AI Agent chuyên biệt** (Analyst, Behavioral Modeler, Class/State Architect, DB/System/UI Designer, Demo Builder, QA Reviewer) và workflow phối hợp. | AI Agent |
| [nhom_8_de_tai.md](file:///d:/Mon_hoc_dai_hoc_sgu/PTTK/nhom_8_de_tai.md) | Tóm tắt nhanh thông tin Nhóm 8, đề tài, hướng dẫn và tài liệu tham khảo. | Toàn bộ 5 thành viên |

---

## 3. Cấu trúc Thư mục Dự án (Project Directory Structure)

```text
PTTK/
├── README.md                 # Trang tổng quan & điều hướng dự án Nhóm 8
├── YEU_CAU_DO_AN.md          # Nguyên văn 100% yêu cầu đồ án từ tài liệu giảng viên
├── RULE.md                   # Quy tắc bắt buộc về UML, Nghiệp vụ KS, CSDL & Demo
├── PLAN.md                   # Kế hoạch 14 ngày từ Zero đến Final nộp bài cho 4 thành viên
├── INSTRUCTION.md            # Hướng dẫn vận hành & mẫu chuẩn cho AI Agent
├── AGENTS.md                 # Định nghĩa 6 vai trò AI Agent chuyên trách
├── nhom_8_de_tai.md          # Thông tin tóm tắt Nhóm 8
├── File_thay-gui/            # Tài liệu gốc của giảng viên (PDF đề tài & Excel danh sách lớp)
├── docs/                     # Hồ sơ văn bản nộp (Đề cương, Báo cáo tiến độ, Báo cáo cuối kỳ, Slide)
├── uml/                      # Tệp mô hình gốc PlantUML (.puml), draw.io (.drawio) & ảnh xuất (.png)
├── database/                 # Lược đồ CSDL, script SQL & truy vấn chống bán trùng DateRange
├── ui-mockups/               # Thiết kế 8 màn hình giao diện (UI Mockups)
└── demo-web/                 # Bản Web Demo chạy được (8 màn hình tương tác - Điểm cộng bảo vệ)
```

---

## 4. Bảng Theo dõi Tiến độ Sản phẩm Nộp (Master Deliverables Checklist)

- [ ] **1. Đề cương đồ án** (`docs/01_De_Cuong_Do_An.md` / `.docx`)
- [ ] **2. Báo cáo tiến độ** (`docs/02_Bao_Cao_Tien_Do.md` / `.docx`)
- [ ] **3. Báo cáo cuối kỳ hoàn chỉnh** (`docs/03_Bao_Cao_Cuoi_Ky.md` / `.docx`):
  - [ ] Chương 1: Tổng quan (Bài toán, mục tiêu, phạm vi, quy trình phát triển Lặp & Tăng trưởng)
  - [ ] Chương 3: Khảo sát hiện trạng (QloApps + Phỏng vấn lễ tân), Yêu cầu CN/PCN, Quy tắc nghiệp vụ (Thông báo lưu trú 23h/8h, Chống bán trùng), Bảng thuật ngữ
  - [ ] Chương 4: Sơ đồ Use Case tổng quát & 4 phân rã (đủ `<<include>>`, `<<extend>>`, Tổng quát hóa + câu giải thích), 8 Đặc tả Use Case, 4 Activity Diagrams (có sơ đồ 4 làn), 6 Sequence Diagrams
  - [ ] Chương 5: Sơ đồ lớp mức phân tích & thiết kế (`RoomType` 1–n `Room`, `Booking` vs `Stay`, `DateRange.includes/overlaps`, thảo luận `isAvailable(range)`), 2 Sơ đồ trạng thái độc lập (`Room`, `Booking`)
  - [ ] Chương 6: Lược đồ CSDL quan hệ & điều kiện chồng lấn $[a_1, b_1) \cap [a_2, b_2)$, Kiến trúc tổng thể, Component Diagram (có Adapter OTA & Công an), 2 Collaboration Diagrams, Deployment Diagram, 8 Màn hình giao diện (có Sơ đồ phòng theo ngày cho lễ tân)
  - [ ] Kết luận & Bảng phân công, tự đánh giá nhóm (CLO6) + Phụ lục
- [ ] **4. Bộ tệp mô hình UML gốc** (`uml/*.puml` / `*.drawio`)
- [ ] **5. Bản Web Demo chạy được** (`demo-web/` — điểm cộng)
- [ ] **6. Slide bảo vệ** (`docs/04_Slide_Bao_Ve.pptx`)
