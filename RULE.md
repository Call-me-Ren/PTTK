# BỘ QUY TẮC BẮT BUỘC (RULES & STANDARDS) — ĐỒ ÁN 8: HỆ THỐNG ĐẶT PHÒNG VÀ QUẢN LÝ KHÁCH SẠN

> [!CAUTION]
> Mọi thành viên trong **Nhóm 8** và mọi **AI Agent** tham gia soạn thảo báo cáo, vẽ sơ đồ UML, thiết kế CSDL, giao diện hay viết code **Web Demo** đều **BẮT BUỘC** tuân thủ tuyệt đối các quy tắc trong tệp này. Bất kỳ nội dung nào vi phạm `RULE.md` sẽ bị coi là lệch yêu cầu chấm điểm của giảng viên.

---

## 1. QUY TẮC TUÂN THỦ SỐ LƯỢNG & CẤU TRÚC SẢN PHẨM NỘP (DELIVERABLE RULES)

### 1.1. Danh mục hồ sơ bắt buộc
1. **Đề cương đồ án** (`docs/01_De_Cuong_Do_An.md` / `.docx`).
2. **Báo cáo tiến độ** (`docs/02_Bao_Cao_Tien_Do.md` / `.docx`).
3. **Báo cáo cuối kỳ** (`docs/03_Bao_Cao_Cuoi_Ky.md` / `.docx`) — tuân thủ đúng thứ tự chương của giảng viên:
   - **Chương 1 — Tổng quan:** bài toán, mục tiêu, phạm vi, quy trình phát triển đã chọn và lý do.
   - *(Lưu ý: Đề cương báo cáo của thầy ghi Chương 1 → Chương 3 → Chương 4 → Chương 5 → Chương 6 → Kết luận → Phụ lục; nếu cần Chương 2 Cơ sở lý thuyết UML & Hướng đối tượng thì trình bày ngắn gọn hoặc giữ đúng đánh số chương của thầy).*
   - **Chương 3 — Khảo sát hiện trạng và yêu cầu:** kết quả khảo sát (phỏng vấn lễ tân + khảo sát QloApps), yêu cầu chức năng, yêu cầu phi chức năng, bảng quy tắc nghiệp vụ, bảng thuật ngữ.
   - **Chương 4 — Mô hình hóa yêu cầu:** sơ đồ use case (tổng quát & phân rã) và đặc tả, sơ đồ hoạt động, sơ đồ tuần tự.
   - **Chương 5 — Phân tích:** sơ đồ lớp (mức phân tích & mức thiết kế), thuộc tính, phương thức, quan hệ, sơ đồ trạng thái.
   - **Chương 6 — Thiết kế:** dữ liệu (lược đồ CSDL quan hệ & điều kiện chồng lấn khoảng ngày), kiến trúc tổng thể, sơ đồ thành phần, sơ đồ cộng tác, thiết kế giao diện (8 màn hình), sơ đồ triển khai.
   - **Kết luận:** kết quả đạt được, hạn chế, hướng phát triển; **bảng phân công và tự đánh giá nhóm (CLO6)**.
   - **Phụ lục:** biên bản phỏng vấn, phiếu khảo sát, tài liệu tham khảo.
4. **Slide bảo vệ** (`docs/04_Slide_Bao_Ve.pptx` / HTML Slides).
5. **Tệp mô hình UML gốc:** Lưu toàn bộ mã nguồn **PlantUML (`uml/*.puml`)** và tệp **draw.io (`uml/*.drawio`)** kèm ảnh xuất `.png`/`.svg`.
6. **Bản mẫu giao diện (UI Mockups):** Tối thiểu **8 màn hình giao diện** chính.
7. **Bản Web Demo chạy được (`demo-web/`):** Ứng dụng web minh họa trực tiếp các luồng cốt lõi của khách sạn để lấy **điểm cộng tối đa** khi bảo vệ.

### 1.2. Định mức số lượng sơ đồ tối thiểu (Không được thiếu bất kỳ sơ đồ nào)

| Loại sơ đồ / Đặc tả | Số lượng tối thiểu theo đề | Định mức chuẩn của Nhóm 8 |
| :--- | :---: | :--- |
| **Sơ đồ Use Case** | Tổng quát + Phân rã | **1** sơ đồ tổng quát + **5** sơ đồ phân rã theo 5 cụm thành viên |
| **Đặc tả Use Case (Fully Dressed)** | $\ge 6$ use case chính | **10** đặc tả đầy đủ (mỗi thành viên đặc tả **2** use case chính trong cụm của mình) |
| **Sơ đồ Hoạt động (Activity Diagram)** | $\ge 3$ sơ đồ | **4** sơ đồ (1 sơ đồ tổng thể 4 làn *Nhận phòng → Trả phòng* + 3 sơ đồ nghiệp vụ) |
| **Sơ đồ Tuần tự (Sequence Diagram)** | $\ge 5$ sơ đồ | **6** sơ đồ (3 sơ đồ bắt buộc của đề tài 8 + 3 sơ đồ mở rộng cho đủ 4 thành viên) |
| **Sơ đồ Lớp (Class Diagram)** | Phân tích + Thiết kế | **1** sơ đồ lớp mức phân tích (Domain/Analysis) + **1** sơ đồ lớp mức thiết kế (Design Class + Patterns) |
| **Sơ đồ Trạng thái (State Diagram)** | $\ge 2$ sơ đồ | **2** sơ đồ trạng thái độc lập: **`Room`** và **`Booking`** |
| **Lược đồ CSDL quan hệ (ERD / Relational Schema)** | 1 lược đồ | **1** lược đồ CSDL quan hệ đầy đủ PK, FK, kiểu dữ liệu, ràng buộc khoảng ngày |
| **Sơ đồ Kiến trúc tổng thể** | 1 sơ đồ | **1** sơ đồ kiến trúc phân tầng (Layered Architecture / C4 Container) |
| **Sơ đồ Thành phần (Component Diagram)** | 1 sơ đồ | **1** sơ đồ thành phần UML có giao diện cung cấp/yêu cầu và 2 Adapter ngoài |
| **Sơ đồ Cộng tác (Communication Diagram)** | $\ge 2$ sơ đồ | **2** sơ đồ cộng tác (*Đặt phòng trực tuyến có đặt cọc* và *Nhận phòng & thông báo lưu trú*) |
| **Sơ đồ Triển khai (Deployment Diagram)** | 1 sơ đồ | **1** sơ đồ triển khai gồm *Website đặt phòng*, *Phần mềm quầy*, *Máy chủ CSDL* và hệ thống ngoài |
| **Màn hình Giao diện (UI Screens)** | Khoảng 8 màn hình | **8** màn hình giao diện (bắt buộc có *Màn hình sơ đồ phòng theo ngày cho lễ tân*) |

---

## 2. QUY TẮC NGHIỆP VỤ & TRỌNG TÂM ĐÁNH GIÁ CỦA ĐỀ TÀI 8 (DOMAIN & UML RULES)

### Quy tắc 2.1 — Tác nhân (Actors) trong Sơ đồ Use Case
Phải xuất hiện đầy đủ và đúng tên 8 tác nhân (5 tác nhân trong + 3 tác nhân ngoài):
- **Tác nhân con người (Bên trái sơ đồ):**
  1. `Khách` — **Bắt buộc tổng quát hóa (Generalization)** thành 2 tác nhân con: `Khách lẻ` và `Khách đoàn`.
  2. `Lễ tân`
  3. `Nhân viên buồng phòng`
  4. `Kế toán`
  5. `Quản lý`
- **Tác nhân hệ thống ngoài (Bên phải sơ đồ):**
  6. `Cổng thanh toán`
  7. `Kênh bán phòng trực tuyến (OTA)`
  8. `Hệ thống thông báo lưu trú của cơ quan công an`

### Quy tắc 2.2 — Ba quan hệ bắt buộc trong Sơ đồ Use Case & Lập luận bảo vệ
Trong Chương 4, sơ đồ Use Case **bắt buộc** sử dụng có chủ đích cả 3 loại quan hệ chuẩn UML 2.5.1 và **với mỗi quan hệ phải có đúng đoạn giải thích vì sao không chọn quan hệ khác**:

1. **Quan hệ `<<include>>`:**
   - **Áp dụng:** Use Case `“Đặt phòng”` và `“Đổi phòng”` cùng `<<include>>` Use Case `“Kiểm tra phòng trống”` (mũi tên nét đứt từ Use Case cơ sở trỏ tới `“Kiểm tra phòng trống”`).
   - **Lập luận bắt buộc:** *“Kiểm tra phòng trống” là bước bắt buộc phải thực hiện thành công trong mọi lần “Đặt phòng” hoặc “Đổi phòng” và được dùng chung ở cả hai ca sử dụng; do đó không thể dùng `<<extend>>` (vì không phải bước tùy chọn) và không dùng tổng quát hóa (vì “Kiểm tra phòng trống” chỉ là một bước con, không phải một biến thể cùng loại với “Đặt phòng”).*

2. **Quan hệ `<<extend>>`:**
   - **Áp dụng:** Use Case `“Áp dụng mã khuyến mãi”` mở rộng (`<<extend>>`) vào Use Case `“Đặt phòng”` (mũi tên nét đứt từ `“Áp dụng mã khuyến mãi”` trỏ về `“Đặt phòng”`, kèm Extension Point và điều kiện mở rộng `[Khách có nhập mã khuyến mãi]`).
   - **Lập luận bắt buộc:** *“Đặt phòng” vẫn hoàn tất đầy đủ và hợp lệ ngay cả khi khách không có mã khuyến mãi; hành vi này chỉ kích hoạt có điều kiện tại điểm tính giá nên phải dùng `<<extend>>` chứ không dùng `<<include>>` (tránh ép buộc mọi đơn đặt phòng đều phải có mã khuyến mãi).*

3. **Quan hệ Tổng quát hóa (Generalization):**
   - **Áp dụng:** Use Case trừu tượng/cha `“Thanh toán”` được tổng quát hóa từ 3 Use Case con: `“Thanh toán thẻ”`, `“Chuyển khoản”`, `“Tiền mặt”` (mũi tên nét liền đầu tam giác rỗng từ các Use Case con trỏ lên `“Thanh toán”`).
   - **Lập luận bắt buộc:** *“Thanh toán thẻ”, “Chuyển khoản” và “Tiền mặt” đều có chung mục đích nghiệp vụ là hoàn tất nghĩa vụ thanh toán cho hóa đơn/đặt cọc nhưng khác nhau về quy trình thực hiện chi tiết (quan hệ “là một loại / is-a”), nên phải dùng Tổng quát hóa thay vì `<<include>>` hay `<<extend>>`.*

---

### Quy tắc 2.3 — Mô hình Lớp (Chương 5): `RoomType` vs `Room`, `Booking` vs `Stay`, và `DateRange`
Sơ đồ lớp phân tích và thiết kế **bắt buộc** tuân thủ cấu trúc miền khách sạn chuẩn sau:

1. **Phân biệt `RoomType` (Loại phòng) và `Room` (Phòng vật lý cụ thể):**
   - Quan hệ: `RoomType` `1` ——— `1..*` `Room`.
   - `RoomType` lưu: `maLoaiPhong`, `tenLoaiPhong` (VD: Deluxe Double, Superior Twin), `sucChuaToiDa`, `dienTich`, `giaCoBan`, `moTaTienNghi`.
   - `Room` lưu: `maPhong`, `soPhong` (VD: `301`, `302`), `tang`, `trangThaiBuong` (`RoomStatus`: `TRONG_SACH`, `CO_KHACH`, `TRONG_BAN`, `DANG_DON`, `BAO_TRI`).
2. **Phân biệt `Booking` (Đặt phòng / Giữ chỗ) và `Stay` (Lượt lưu trú thực tế):**
   - Khi khách **Đặt phòng (`Booking`)**: hệ thống **giữ chỗ theo loại phòng (`RoomType`)** và số lượng phòng trong khoảng ngày `DateRange` (chưa khóa cứng số phòng vật lý `301` để lễ tân linh hoạt xếp phòng, trừ khi khách yêu cầu đặc biệt).
   - Khi khách **Nhận phòng (`Stay` / Check-in)**: lễ tân mới **gán phòng cụ thể (`Room`)** đang ở trạng thái `TRONG_SACH` cho lượt lưu trú `Stay`, ghi nhận danh sách khách lưu trú (`Guest`) và kích hoạt thông báo lưu trú.
3. **Lớp giá trị `DateRange` (Theo mẫu Range của Martin Fowler):**
   - Thuộc tính: `startDate: Date` (ngày nhận phòng dự kiến $a$), `endDate: Date` (ngày trả phòng dự kiến $b$, với ràng buộc $a < b$, biểu diễn khoảng nửa mở $[a, b)$ tính theo đêm lưu trú).
   - Phương thức bắt buộc:
     - `includes(date: Date): Boolean` — kiểm tra một ngày $d$ có thuộc khoảng lưu trú không ($a \le d < b$).
     - `overlaps(other: DateRange): Boolean` — kiểm tra hai khoảng $[a_1, b_1)$ và $[a_2, b_2)$ có chồng lấn nhau không theo đúng công thức toán học:
       $$\text{overlaps} \iff (a_1 < b_2) \land (a_2 < b_1)$$
     - `getNights(): Integer` — trả về số đêm lưu trú ($b - a$).
4. **Các lớp bắt buộc khác trong Sơ đồ lớp:**
   - `Guest` (Khách lưu trú: thông tin CCCD/Passport để khai báo lưu trú).
   - `Folio` (Hồ sơ công nợ/tài khoản chi phí của lượt lưu trú `Stay`).
   - `FolioCharge` (Khoản mục phí phát sinh trong `Folio` — quan hệ **Composition** `Folio 1 *-- 0..* FolioCharge`).
   - `Service` (Danh mục dịch vụ: Minibar, Giặt là, Nhà hàng...).
   - `RatePlan` (Chính sách giá) & `Season` (Mùa cao điểm / thấp điểm / cuối tuần — gắn với `DateRange`).
5. **Lập luận trách nhiệm `isAvailable(range: DateRange)` (Theo GRASP Information Expert):**
   - Phải thảo luận rõ hai cấp độ kiểm tra phòng trống:
     - **Ở giai đoạn Đặt phòng (`RoomType.getAvailableCount(range)` / `AvailabilityService`):** `RoomType` (hoặc dịch vụ miền `RoomAvailabilityService` truy vấn trên tập `Room` và tập `Booking`/`Stay` của `RoomType` đó) là **Information Expert** vì nó nắm tổng số phòng vật lý hoạt động của loại phòng đó trừ đi số lượng phòng đã được giữ chỗ (`Booking` ở trạng thái `TAM_GIU`, `DA_XAC_NHAN`, `DA_NHAN_PHONG`) có `bookingPeriod.overlaps(range) == true`.
     - **Ở giai đoạn Nhận phòng / Đổi phòng (`Room.isAvailable(range)`):** Từng đối tượng `Room` cụ thể kiểm tra xem nó có đang ở trạng thái `TRONG_SACH` (không bị `BAO_TRI`) và không có `Stay` nào chồng lấn với `range` hay không.

---

### Quy tắc 2.4 — Hai Sơ đồ Trạng thái Độc lập (Chương 5)
Không được gộp trạng thái của Phòng và Đặt phòng vào làm một! Phải vẽ **2 sơ đồ trạng thái (State Machine Diagrams)** hoàn toàn độc lập:

1. **Sơ đồ trạng thái của `Room` (Phòng vật lý):**
   - Luồng chính:
     `Trống sạch` $\xrightarrow{\text{nhận phòng / đổi sang phòng này}}$ `Có khách` $\xrightarrow{\text{trả phòng / đổi sang phòng khác}}$ `Trống bẩn` $\xrightarrow{\text{bắt đầu dọn buồng}}$ `Đang dọn` $\xrightarrow{\text{hoàn tất dọn & kiểm tra đạt}}$ `Trống sạch`.
   - Nhánh `Bảo trì`: Từ `Trống sạch` hoặc `Trống bẩn` $\xrightarrow{\text{phát hiện hỏng hóc / lịch bảo trì}}$ `Bảo trì` $\xrightarrow{\text{nghiệm thu sửa chữa xong}}$ `Trống bẩn` (để dọn lại) hoặc `Trống sạch`.

2. **Sơ đồ trạng thái của `Booking` (Đơn đặt phòng):**
   - Luồng chính:
     `Tạm giữ` $\xrightarrow{\text{thanh toán đặt cọc thành công / xác nhận}}$ `Đã xác nhận` $\xrightarrow{\text{khách đến check-in & gán phòng}}$ `Đã nhận phòng` $\xrightarrow{\text{khách check-out & tất toán folio}}$ `Đã trả phòng`.
   - Nhánh `Đã hủy`: Từ `Tạm giữ` (quá hạn thanh toán cọc hoặc khách hủy) hoặc từ `Đã xác nhận` (khách báo hủy trước giờ nhận phòng, áp dụng quy tắc tính phí hủy) $\rightarrow$ `Đã hủy`.
   - Nhánh `Không đến (No-show)` & **Sự kiện thời gian (Time Event) bắt buộc:**
     Từ `Đã xác nhận` $\xrightarrow{\text{after(hết giờ giữ phòng của ngày đến mà khách chưa nhận phòng)}}$ `Không đến`.

---

### Quy tắc 2.5 — Thiết kế CSDL, Chống Bán Trùng & Mẫu Adapter (Chương 6)

1. **Biểu diễn khoảng ngày và điều kiện chồng lấn trong CSDL:**
   - Trong bảng `bookings` và `stays`, lưu cặp cột `check_in_date DATE NOT NULL` ($a$) và `check_out_date DATE NOT NULL` ($b$) với ràng buộc `CHECK (check_in_date < check_out_date)`.
   - Mọi câu truy vấn tìm phòng trống cho khoảng $[a_1, b_1)$ (`:req_in`, `:req_out`) phải dùng đúng điều kiện chồng lấn của đề:
     ```sql
     -- Hai khoảng [a1, b1) và [a2, b2) chồng nhau khi a1 < b2 VÀ a2 < b1
     WHERE b.status IN ('TAM_GIU', 'DA_XAC_NHAN', 'DA_NHAN_PHONG')
       AND (:req_in < b.check_out_date AND b.check_in_date < :req_out)
     ```
2. **Cơ chế chống bán trùng (Overbooking / Race Condition Prevention) khi Website, OTA và Lễ tân cùng đặt:**
   - Phải trình bày rõ 2 lớp bảo vệ trong CSDL:
     1. **Pessimistic Locking / Transaction Isolation:** Khoá dòng loại phòng (`SELECT ... FROM room_types WHERE room_type_id = :id FOR UPDATE`) trong Transaction khi kiểm tra số lượng trống và chèn `Booking` mới, đảm bảo các yêu cầu đồng thời từ Website, OTA Webhook và Lễ tân phải xếp hàng tuần tự trên cùng `room_type_id`.
     2. **Exclusion Constraint đối với phòng vật lý (`stays`):** Trên PostgreSQL sử dụng `EXCLUDE USING gist (room_id WITH =, daterange(check_in_date, check_out_date, '[)') WITH &&)` (hoặc Unique/Trigger kiểm tra chồng lấn trong MySQL/SQL Server) để ngăn tuyệt đối việc gán 1 phòng cụ thể cho 2 lượt lưu trú trùng ngày.
3. **Quy định Pháp lý về Thông báo lưu trú (Chương 3 & Chương 6):**
   - Theo Luật Cư trú sửa đổi: Cơ sở lưu trú phải thông báo lưu trú cho cơ quan công an **trước 23:00** hàng ngày; trường hợp khách đến nhận phòng **sau 23:00** thì phải thông báo **trước 08:00 sáng ngày hôm sau**.
4. **Mẫu thiết kế Adapter (GoF Adapter Pattern):**
   - Bắt buộc thiết kế 2 giao diện và lớp Adapter trong Chương 6 (Sơ đồ lớp thiết kế & Sơ đồ thành phần):
     - `IOtaChannelGateway` $\leftarrow$ `BookingComOtaAdapter` / `AgodaOtaAdapter` (đồng bộ quỹ phòng & nhận booking từ OTA).
     - `IResidenceDeclarationGateway` $\leftarrow$ `PoliceResidencePortalAdapter` (chuyển đổi đối tượng `Stay` + danh sách `Guest` sang định dạng XML/JSON của Cổng thông báo lưu trú Bộ Công an).

---

## 3. QUY TẮC ĐẶT TÊN, MÃ NGUỒN UML & BẢN WEB DEMO

1. **Tính nhất quán (Single Source of Truth):**
   - Tên lớp, tên thuộc tính và tên phương thức xuất hiện trong **Sequence Diagram**, **Collaboration Diagram**, **State Diagram** phải **trùng khớp 100%** với **Class Diagram** và ánh xạ đúng sang **Lược đồ CSDL**.
2. **Quy ước ngôn ngữ trong mô hình UML:**
   - **Use Case, Activity, State Diagram:** Tên trạng thái, hành động và ca sử dụng viết bằng **Tiếng Việt có dấu chuẩn xác** theo đúng từ khóa của thầy (VD: `Đặt phòng`, `Kiểm tra phòng trống`, `Trống sạch`, `Có khách`, `Trống bẩn`, `Đang dọn`, `Bảo trì`).
   - **Class Diagram, Sequence Diagram (tên lớp & phương thức), CSDL:** Dùng tên lớp và phương thức tiếng Anh chuẩn đúng gợi ý của thầy (`RoomType`, `Room`, `Booking`, `Stay`, `DateRange`, `includes()`, `overlaps()`, `isAvailable(range)`, `Guest`, `Folio`, `FolioCharge`, `Service`, `RatePlan`, `Season`) kèm giải thích tiếng Việt trong bảng mô tả.
3. **Quy chuẩn Web Demo (`demo-web/`):**
   - Bản Web Demo phải thể hiện trực quan **8 màn hình giao diện** đã thiết kế ở Chương 6, đặc biệt là:
     1. Màn hình khách tìm phòng trống theo `DateRange` & Đặt phòng trực tuyến (có áp mã khuyến mãi & đặt cọc).
     2. **Màn hình sơ đồ phòng theo ngày cho lễ tân (Room Rack / Tape Chart Calendar)** — trọng tâm giao diện thầy yêu cầu.
     3. Màn hình Nhận phòng (Check-in: gán phòng cụ thể + nút gửi Thông báo lưu trú có cảnh báo mốc 23h00 / 08h00).
     4. Màn hình Ghi dịch vụ phát sinh vào `Folio` (Minibar, Giặt là, Nhà hàng).
     5. Màn hình Trả phòng (Check-out) & Thanh toán (Thẻ / Chuyển khoản / Tiền mặt) + Xuất hóa đơn.
     6. Màn hình Quản lý buồng phòng (Housekeeping chuyển trạng thái `Trống bẩn → Đang dọn → Trống sạch / Bảo trì`).
     7. Màn hình Cấu hình giá theo mùa (`Season` & `RatePlan`).
     8. Màn hình Báo cáo công suất phòng (Occupancy Report).
