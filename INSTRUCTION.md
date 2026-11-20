# HƯỚNG DẪN VẬN HÀNH DÀNH CHO AI AGENT (AI AGENT INSTRUCTIONS)

> [!IMPORTANT]
> Tài liệu này là **System Instruction** dành cho mọi AI Agent (Antigravity, Claude, Gemini, Cursor, Copilot...) khi tham gia hỗ trợ **Nhóm 8** thực hiện **Đồ án 8: Hệ thống đặt phòng và quản lý khách sạn** (Học phần: Phân tích thiết kế hướng đối tượng — Mã HP: `841111`, Trường Đại học Sài Gòn).

---

## 1. QUY TRÌNH ĐỌC NGỮ CẢNH BẮT BUỘC (CONTEXT LOADING ORDER)

Trước khi thực hiện bất kỳ yêu cầu nào từ thành viên trong nhóm, AI Agent **bắt buộc** đọc theo thứ tự ưu tiên sau:
1. [YEU_CAU_DO_AN.md](file:///d:/Mon_hoc_dai_hoc_sgu/PTTK/YEU_CAU_DO_AN.md) — Nguồn chân lý nguyên văn (Single Source of Truth) về mọi yêu cầu từ giảng viên.
2. [RULE.md](file:///d:/Mon_hoc_dai_hoc_sgu/PTTK/RULE.md) — Các ràng buộc cứng về UML 2.5.1, mô hình lớp, trạng thái, công thức `DateRange` và định mức sơ đồ.
3. [PLAN.md](file:///d:/Mon_hoc_dai_hoc_sgu/PTTK/PLAN.md) — Kế hoạch phân công 4 cụm Use Case cho 4 thành viên và tiến độ 14 ngày.
4. [AGENTS.md](file:///d:/Mon_hoc_dai_hoc_sgu/PTTK/AGENTS.md) — Định nghĩa vai trò chuyên trách và giao thức bàn giao giữa các Agent.

---

## 2. TỪ ĐIỂN MIỀN CHUẨN HÓA (CANONICAL DOMAIN DICTIONARY)

AI Agent **không được tự ý bịa tên lớp khác** với bảng từ điển chuẩn dưới đây khi vẽ Class Diagram, Sequence Diagram, Collaboration Diagram, State Diagram và Lược đồ CSDL:

| Tên Lớp (Chuẩn UML) | Tên Bảng CSDL | Ý nghĩa Nghiệp vụ | Thuộc tính Cốt lõi | Phương thức Cốt lõi |
| :--- | :--- | :--- | :--- | :--- |
| `DateRange` *(Value Object)* | *(Nhúng thành `check_in_date`, `check_out_date`)* | Khoảng thời gian lưu trú nửa mở $[a, b)$ theo mẫu Fowler Range | `startDate: Date`, `endDate: Date` | `includes(date): bool`, `overlaps(other: DateRange): bool`, `getNights(): int` |
| `RoomType` | `room_types` | Loại phòng (hạng phòng) mà khách chọn khi đặt chỗ | `roomTypeId`, `code`, `name`, `maxOccupancy`, `basePrice`, `totalActiveRooms` | `getAvailableCount(range: DateRange): int`, `calculatePrice(range: DateRange, ratePlan: RatePlan): Money` |
| `Room` | `rooms` | Phòng vật lý cụ thể (VD: `P.301`), gán khi Check-in | `roomId`, `roomNumber`, `floor`, `status: RoomStatus` | `isAvailable(range: DateRange): bool`, `changeStatus(newStatus: RoomStatus): void` |
| `Booking` | `bookings` | Đơn đặt phòng (giữ chỗ theo `RoomType` và `DateRange`) | `bookingId`, `bookingCode`, `period: DateRange`, `roomQuantity`, `depositAmount`, `status: BookingStatus`, `holdExpiresAt: DateTime` | `confirmDeposit(): void`, `cancel(cancelDate): Money`, `markNoShow(): void`, `checkIn(): Stay` |
| `Stay` | `stays` | Lượt lưu trú thực tế tại phòng cụ thể từ Check-in đến Check-out | `stayId`, `actualPeriod: DateRange`, `checkInTime: DateTime`, `checkOutTime: DateTime`, `residenceDeclared: bool` | `assignRoom(newRoom: Room): void`, `changeRoom(newRoom: Room, reason: String): void`, `completeCheckOut(): Folio` |
| `Guest` | `guests` | Khách hàng / Khách lưu trú (cần CCCD/Hộ chiếu khai báo lưu trú) | `guestId`, `fullName`, `phone`, `email`, `idNumber`, `idType`, `nationality`, `guestType` | `validateIdentityForPolice(): bool` |
| `Folio` | `folios` | Hồ sơ thanh toán / Tài khoản chi phí của một lượt lưu trú `Stay` | `folioId`, `totalRoomCharge`, `totalServiceCharge`, `depositDeducted`, `discountAmount`, `balanceDue`, `status` | `addCharge(service: Service, qty: int): FolioCharge`, `recalculateTotal(): Money`, `settle(payment: Payment): void` |
| `FolioCharge` | `folio_charges` | Từng dòng chi phí phát sinh trong `Folio` (Composition) | `chargeId`, `description`, `quantity`, `unitPrice`, `subTotal`, `chargedAt: DateTime` | `getSubTotal(): Money` |
| `Service` | `services` | Danh mục dịch vụ phụ trợ (Minibar, Giặt là, Nhà hàng, Spa) | `serviceId`, `serviceCode`, `name`, `category`, `unitPrice`, `unit` | `getCurrentPrice(): Money` |
| `RatePlan` | `rate_plans` | Chính sách giá (Giá tiêu chuẩn, Giá không hoàn hủy, Giá cuối tuần) | `ratePlanId`, `name`, `weekendMultiplier`, `isRefundable`, `depositPercent` | `getNightlyRate(date: Date, basePrice: Money): Money` |
| `Season` | `seasons` | Mùa giá (Mùa cao điểm lễ/Tết, mùa thấp điểm) | `seasonId`, `name`, `period: DateRange`, `priceMultiplier` | `appliesTo(date: Date): bool` |
| `Payment` *(Abstract)* | `payments` | Giao dịch thanh toán (Tổng quát hóa cho Thẻ, Chuyển khoản, Tiền mặt) | `paymentId`, `amount`, `paidAt`, `paymentType`, `status`, `transactionRef` | `processPayment(): bool` *(đa hình ở `CardPayment`, `BankTransferPayment`, `CashPayment`)* |

---

## 3. MẪU CHUẨN SOẠN THẢO BÁO CÁO CHO AI AGENT (TEMPLATES)

### 3.1. Mẫu Đặc tả Use Case Đầy đủ (Fully Dressed Use Case — Chương 4)
Khi thành viên yêu cầu viết đặc tả cho bất kỳ Use Case nào trong 8 Use Case chính, AI Agent **phải** xuất đúng định dạng bảng sau:

```markdown
#### Đặc tả Use Case: [Mã UC] — [Tên Use Case]

| Thuộc tính | Nội dung chi tiết |
| :--- | :--- |
| **Mã Use Case** | `UC-XX` |
| **Tên Use Case** | [Tên chuẩn khớp 100% với Sơ đồ Use Case] |
| **Tác nhân chính (Primary Actor)** | [VD: Khách lẻ / Lễ tân] |
| **Tác nhân phụ / Hệ thống ngoài** | [VD: Cổng thanh toán / Hệ thống thông báo lưu trú của cơ quan công an] |
| **Mô tả ngắn gọn** | [1–2 câu mô tả mục tiêu nghiệp vụ] |
| **Tiền điều kiện (Preconditions)** | - [Điều kiện 1]<br>- [Điều kiện 2] |
| **Hậu điều kiện thành công (Postconditions)** | - [Trạng thái đối tượng thay đổi như thế nào]<br>- [Bản ghi nào được lưu vào CSDL] |
| **Quan hệ Use Case** | - `<<include>>`: [Nếu có]<br>- `<<extend>>`: [Nếu có]<br>- Tổng quát hóa: [Nếu có] |

**Luồng sự kiện chính (Basic Flow / Main Success Scenario):**
1. Tác nhân...
2. Hệ thống...
3. *(Nếu có `<<include>>` thì ghi rõ tại bước mấy: `Hệ thống thực hiện Use Case <<include>> "Kiểm tra phòng trống"`)*...

**Luồng thay thế / Mở rộng (Alternative / Extension Flows):**
- **3a. [Điều kiện rẽ nhánh — VD: Khách có nhập mã khuyến mãi (`<<extend>> "Áp dụng mã khuyến mãi"`):**
  - 3a.1. Hệ thống kiểm tra tính hợp lệ và thời hạn của mã khuyến mãi...
- **4a. [Ngoại lệ — VD: Hết phòng trống do khách khác trên OTA vừa đặt chỗ cuối cùng]:**
  - 4a.1. Hệ thống thông báo hết loại phòng đã chọn và gợi ý loại phòng/khoảng ngày khác...

**Quy tắc nghiệp vụ liên quan (Business Rules):** `BR-01`, `BR-02`...
```

---

### 3.2. Mẫu Quy chuẩn Sinh Mã Nguồn PlantUML (`uml/*.puml`)
Mọi sơ đồ UML do AI Agent sinh ra phải lưu thành file `.puml` độc lập trong thư mục `uml/` với header cấu hình font rõ nét, hỗ trợ tiếng Việt Unicode:

```plantuml
@startuml
skinparam shadowing false
skinparam defaultFontName "Segoe UI"
skinparam defaultFontSize 13
skinparam roundcorner 8
skinparam packageStyle rectangle

' Nội dung sơ đồ tại đây
@enduml
```

#### Quy tắc kiểm tra lỗi cú pháp PlantUML trước khi bàn giao:
1. Trong **Use Case Diagram**:
   - Quan hệ `<<include>>`: `UC_Base ..> UC_Included : <<include>>`
   - Quan hệ `<<extend>>`: `UC_Extending ..> UC_Base : <<extend>>` *(Chú ý chiều mũi tên từ Use Case mở rộng trỏ vào Use Case gốc!)*.
   - Quan hệ Tổng quát hóa: `ChildActor --|> ParentActor` và `UC_Child --|> UC_Parent`.
2. Trong **Sequence Diagram**:
   - Đánh số tự động bằng `autonumber`.
   - Phải có khung `alt` / `opt` / `loop` rõ ràng cho các nhánh kiểm tra phòng trống, thanh toán đặt cọc, gán phòng và gửi thông báo lưu trú.
3. Trong **State Diagram**:
   - Phải có nút bắt đầu `[*]` và nút kết thúc `[*]`.
   - Ghi rõ tên sự kiện chuyển trạng thái theo cú pháp: `SựKiện [ĐiềuKiệnChặn] / HànhĐộng`.

---

## 4. HƯỚNG DẪN XÂY DỰNG BẢN WEB DEMO CỘNG ĐIỂM (`demo-web/`)

Để giúp nhóm đạt **điểm cộng tối đa** ở mục *"Mã nguồn không bắt buộc; bản demo chạy được có thể tính điểm cộng"*, khi xây dựng `demo-web/`, AI Agent tuân thủ kiến trúc sau:
1. **Đơn giản, chạy ngay lập tức (Zero-Config / Instant Run):**
   - Thiết kế Web App giao diện hiện đại, có sẵn dữ liệu mẫu (Seed Data) của khách sạn quy mô vừa (VD: 4 hạng phòng `Standard`, `Superior`, `Deluxe`, `Family Suite`, 20 phòng từ tầng 1 đến tầng 4, các booking mẫu, dịch vụ Minibar/Giặt là/Nhà hàng).
   - Có thể chạy ngay trên máy tính khi lên bảo vệ mà không phụ thuộc cấu hình server phức tạp.
2. **Đầy đủ 8 màn hình giao diện khớp 100% với Chương 6 báo cáo:**
   - **Tab 1 (Cổng Khách hàng):** Tìm kiếm phòng trống theo khoảng ngày `DateRange` $[a, b)$ + Đặt phòng trực tuyến + Áp dụng mã khuyến mãi (`<<extend>>`) + Thanh toán đặt cọc.
   - **Tab 2 (Lễ tân — Sơ đồ phòng theo ngày / Room Rack Calendar):** Lưới lịch trực quan theo ngày và từng số phòng (`101`..`405`), hiển thị màu sắc theo trạng thái `Trống sạch`, `Có khách`, `Trống bẩn`, `Đang dọn`, `Bảo trì`.
   - **Tab 3 (Lễ tân — Nhận phòng & Đổi phòng):** Nhận phòng từ `Booking` đã xác nhận, gán phòng vật lý cụ thể (`Stay`), nhập CCCD khách và bấm **"Gửi thông báo lưu trú Cổng Công an"** (hiển thị trạng thái hạn 23:00 / 08:00 sáng hôm sau).
   - **Tab 4 (Lễ tân / Dịch vụ — Ghi dịch vụ phát sinh vào Folio):** Chọn phòng đang ở, thêm dịch vụ Minibar / Giặt là / Nhà hàng vào `FolioCharge`.
   - **Tab 5 (Lễ tân / Thu ngân — Trả phòng & Thanh toán hóa đơn):** Tổng hợp tiền phòng theo mùa + dịch vụ phát sinh − tiền cọc, chọn 1 trong 3 hình thức thanh toán (`Thanh toán thẻ`, `Chuyển khoản`, `Tiền mặt`) và xuất hóa đơn.
   - **Tab 6 (Buồng phòng — Housekeeping Board):** Nhân viên buồng phòng chuyển trạng thái phòng `Trống bẩn → Đang dọn → Trống sạch` hoặc báo `Bảo trì`.
   - **Tab 7 (Quản lý — Cấu hình Giá theo mùa & Khuyến mãi):** Quản lý `Season`, `RatePlan` và kiểm thử thuật toán chống chồng lấn `DateRange.overlaps()`.
   - **Tab 8 (Quản lý / Kế toán — Báo cáo Công suất phòng & Doanh thu):** Biểu đồ tỷ lệ lấp đầy phòng (Occupancy Rate %), doanh thu phòng & dịch vụ.
3. **Chụp ảnh màn hình từ Web Demo đưa ngược vào Chương 6 Báo cáo:**
   - Toàn bộ 8 màn hình trong Web Demo được dùng làm hình minh họa giao diện (UI Mockups) sắc nét, đồng nhất cho Chương 6 và Slide bảo vệ.

---

## 5. BỘ CÂU HỎI PHẢN BIỆN ("ĐIỂM CẦN BẢO VỆ") AI AGENT PHẢI LUÔN LÀM RÕ TRONG BÁO CÁO

Khi viết Chương 4, Chương 5 và Chương 6, AI Agent bắt buộc chèn các hộp giải thích (Callout / Lý giải thiết kế) trả lời sẵn 6 câu hỏi hội đồng thường hỏi nhất ở Đề tài 8:

1. **Câu hỏi 1:** *Vì sao khi Đặt phòng (`Booking`) chỉ gắn với Loại phòng (`RoomType`) mà chưa gán cứng Phòng cụ thể (`Room`), đến khi Nhận phòng (`Stay`) mới gán `Room`?*
   - **Trả lời chuẩn:** Giúp khách sạn tối ưu hóa xếp phòng (tránh phân mảnh lịch phòng trống), linh hoạt xử lý khi một phòng vật lý đột xuất bị hỏng (`Bảo trì`) hoặc khách trước trả phòng muộn mà không làm ảnh hưởng đến đơn đặt phòng của khách mới, miễn là tổng số phòng khả dụng của `RoomType` đó vẫn đủ.
2. **Câu hỏi 2:** *Vì sao kiểm tra khoảng ngày lưu trú dùng khoảng nửa mở $[a, b)$ thay vì đoạn đóng $[a, b]$?*
   - **Trả lời chuẩn:** Trong nghiệp vụ khách sạn, ngày trả phòng $b$ của khách trước (trả trước 12:00 trưa) có thể trùng với ngày nhận phòng $a$ của khách sau (nhận từ 14:00 chiều). Dùng khoảng nửa mở $[a, b)$ giúp hai lượt lưu trú kế tiếp nhau $[10/12, 12/12)$ và $[12/12, 15/12)$ có $10/12 < 15/12$ và $12/12 < 12/12$ (Sai) $\Rightarrow$ **không bị báo trùng lịch**, đúng thực tế vận hành.
3. **Câu hỏi 3:** *Vì sao không chọn `<<include>>` cho "Áp dụng mã khuyến mãi" hay `<<extend>>` cho "Kiểm tra phòng trống"?*
   - **Trả lời chuẩn:** Đã quy định chi tiết tại Mục 2.2 của `RULE.md`.
4. **Câu hỏi 4:** *Lớp nào chịu trách nhiệm `isAvailable(range)` theo GRASP?*
   - **Trả lời chuẩn:** Đã quy định chi tiết tại Mục 2.3 khoản 5 của `RULE.md`.
5. **Câu hỏi 5:** *Làm sao ngăn chặn bán trùng phòng khi khách trên Website, khách trên Agoda/Booking.com (OTA) và Lễ tân tại quầy cùng bấm đặt căn phòng trống cuối cùng ở cùng một giây?*
   - **Trả lời chuẩn:** Kết hợp khoá bi quan cấp độ dòng (`SELECT ... FOR UPDATE` trên `room_types`) trong Transaction kiểm tra quỹ phòng khi tạo `Booking`, cùng cơ chế giữ chỗ tạm thời có thời hạn (`Tạm giữ` 15 phút chờ thanh toán đặt cọc) và ràng buộc chống chồng lấn (`Exclusion Constraint`) trên bảng `stays`.
6. **Câu hỏi 6:** *Vì sao cần dùng mẫu thiết kế Adapter cho OTA và Hệ thống thông báo lưu trú của cơ quan công an?*
   - **Trả lời chuẩn:** Vì các hệ thống bên ngoài có giao thức và cấu trúc dữ liệu riêng biệt, nằm ngoài tầm kiểm soát của khách sạn và có thể thay đổi theo thời gian. Dùng **Adapter Pattern** (kết hợp nguyên tắc **Protected Variations** và **Indirection** trong GRASP) giúp lõi nghiệp vụ khách sạn (`BookingService`, `StayService`) chỉ làm việc với giao diện nội bộ ổn định (`IOtaChannelGateway`, `IResidenceDeclarationGateway`).
