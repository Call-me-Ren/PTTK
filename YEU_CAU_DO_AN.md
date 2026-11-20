# TỔNG HỢP NGUYÊN VĂN YÊU CẦU ĐỒ ÁN MÔN HỌC PHÂN TÍCH THIẾT KẾ HƯỚNG ĐỐI TƯỢNG (NHÓM 8)

> [!IMPORTANT]
> Tài liệu này trích xuất **nguyên văn 100% không thiếu, không sai một chữ** từ các tệp gốc của giảng viên trong thư mục dự án:
> 1. [Gủi SV -Đồ án môn học Phân tích thiết kế hướng đối tượng.pdf](file:///d:/Mon_hoc_dai_hoc_sgu/PTTK/File_thay-gui/G%E1%BB%A7i%20SV%20-%C4%90%E1%BB%93%20%C3%A1n%20m%C3%B4n%20h%E1%BB%8Dc%20Ph%C3%A2n%20t%C3%ADch%20thi%E1%BA%BFt%20k%E1%BA%BF%20h%C6%B0%E1%BB%9Bng%20%C4%91%E1%BB%91i%20t%C6%B0%E1%BB%A3ng.pdf) (Trang 1, 2, 10, 11, 18, 19)
> 2. [02. NEW DS SV Lớp Phân tích thiết kế HĐT Chiều  thú 6.xlsx](file:///d:/Mon_hoc_dai_hoc_sgu/PTTK/File_thay-gui/02.%20NEW%20DS%20SV%20L%E1%BB%9Bp%20Ph%C3%A2n%20t%C3%ADch%20thi%E1%BA%BFt%20k%E1%BA%BF%20H%C4%90T%20Chi%E1%BB%81u%20%20th%C3%BA%206.xlsx) (Dòng 1 và Dòng 26–29 — Nhóm 8)
> 3. [nhom_8_de_tai.md](file:///d:/Mon_hoc_dai_hoc_sgu/PTTK/nhom_8_de_tai.md)
> 4. [04. De Ôn thi kiểm tra giữa kỳ - Phân Tích TKHDT_he CLC-2026.pdf](file:///d:/Mon_hoc_dai_hoc_sgu/PTTK/On_Kiem_Tra/04.%20De%20%C3%94n%20thi%20ki%E1%BB%83m%20tra%20gi%E1%BB%AFa%20k%E1%BB%B3%20-%20Ph%C3%A2n%20T%C3%ADch%20TKHDT_he%20CLC-2026.pdf) (Trang 1–2)

---

## PHẦN 1. YÊU CẦU CHUNG, CẤU TRÚC BÁO CÁO & LỘ TRÌNH THỰC HIỆN (NGUYÊN VĂN TRANG 1–2 PDF)

### Đề tài đồ án môn học Phân tích thiết kế hướng đối tượng

#### Yêu cầu chung cho mọi đề tài

- **Nhóm:** 1–5 sinh viên (gợi ý; đề cương chỉ quy định làm theo nhóm). Mỗi thành viên phụ trách ít nhất một cụm use case từ đặc tả đến thiết kế, ghi rõ trong bảng phân công.
- **Sản phẩm nộp (theo mục 8 đề cương):** đề cương đồ án, báo cáo tiến độ, báo cáo cuối kỳ, slide bảo vệ, kèm tệp mô hình gốc (StarUML, Visual Paradigm, PlantUML hoặc draw.io) và bản mẫu giao diện. Mã nguồn không bắt buộc; bản demo chạy được có thể tính điểm cộng.
- **Bộ sơ đồ tối thiểu (gợi ý):** sơ đồ use case tổng quát và phân rã; đặc tả ít nhất 6 use case chính; 3 sơ đồ hoạt động; 5 sơ đồ tuần tự; sơ đồ lớp mức phân tích và mức thiết kế; 2 sơ đồ trạng thái; lược đồ CSDL quan hệ; sơ đồ kiến trúc tổng thể, sơ đồ thành phần, 2 sơ đồ cộng tác; sơ đồ triển khai; thiết kế khoảng 8 màn hình giao diện.

#### Cấu trúc báo cáo cuối kỳ

1. **Tổng quan:** bài toán, mục tiêu, phạm vi, quy trình phát triển đã chọn và lý do (Chương 1).
2. **Khảo sát hiện trạng và yêu cầu:** kết quả khảo sát, yêu cầu chức năng, yêu cầu phi chức năng, bảng thuật ngữ (Chương 3).
3. **Mô hình hóa yêu cầu:** sơ đồ use case và đặc tả, sơ đồ hoạt động, sơ đồ tuần tự (Chương 4).
4. **Phân tích:** sơ đồ lớp, thuộc tính, phương thức, quan hệ, sơ đồ trạng thái (Chương 5).
5. **Thiết kế:** dữ liệu, kiến trúc, thành phần, cộng tác, giao diện, triển khai (Chương 6).
6. **Kết luận:** kết quả, hạn chế, hướng phát triển; bảng phân công và tự đánh giá nhóm (CLO6).
7. **Phụ lục:** biên bản phỏng vấn, phiếu khảo sát, tài liệu tham khảo.

#### Lộ trình thực hiện

Nhóm nên chọn đề tài từ tuần 3 và làm song song với tiến độ lý thuyết, để tuần 11–12 (hai tuần dành cho đồ án trong đề cương) chỉ còn hoàn thiện và bảo vệ. Các mốc dưới đây là gợi ý, giảng viên điều chỉnh theo lịch thực tế.

##### Hồ sơ đồ án lớn dần theo từng chương lý thuyết *(Nguyên văn sơ đồ hình ảnh Trang 2 PDF)*
*Lộ trình gợi ý 12 tuần theo mục 7 của đề cương; giảng viên chỉnh mốc theo lịch thực tế*

| Tuần | Chương lý thuyết | Việc của nhóm | Mốc nộp |
| :---: | :--- | :--- | :--- |
| **1 – 4** | **Ch.1–2 Tổng quan, UML** | Đọc giáo trình, thử công cụ vẽ<br>Tuần 3: lập nhóm, chọn đề tài<br>Tuần 4: lập kế hoạch khảo sát | |
| **5** | **Ch.3 Yêu cầu người dùng** | Khảo sát, viết yêu cầu | ◇ **Nộp đề cương** |
| **6 – 7** | **Ch.4 Mô hình hóa yêu cầu** | Use case và đặc tả<br>Sơ đồ hoạt động, tuần tự | |
| **8 – 9** | **Ch.5 Phân tích** | Sơ đồ lớp, thuộc tính, phương thức<br>Sơ đồ trạng thái | |
| **10** | **Ch.6 Thiết kế** | CSDL, kiến trúc, UI, triển khai | |
| **11 – 12** | **Tuần đồ án** | Hoàn thiện hồ sơ, slide<br>Bảo vệ, sửa theo góp ý | Tuần 11: ◇ **Báo cáo tiến độ**<br>Tuần 12: ◈ **Nộp báo cáo và bảo vệ** |

---

## PHẦN 2. NGUYÊN VĂN ĐỀ TÀI CỦA NHÓM 8 TRONG FILE PDF (TRANG 10–11)

### Đồ án 8. Hệ thống đặt phòng và quản lý khách sạn

Nhóm phân tích và thiết kế hệ thống cho một khách sạn quy mô vừa: đặt phòng trực tuyến và tại quầy, nhận phòng, ghi dịch vụ phát sinh, trả phòng, thanh toán và quản lý buồng phòng. Trọng tâm là tổ chức sơ đồ use case bằng đủ ba quan hệ `include`, `extend`, tổng quát hóa, và mô hình hóa khoảng thời gian lưu trú trong sơ đồ lớp lẫn CSDL.

- **Tác nhân:** Khách (tổng quát hóa thành Khách lẻ, Khách đoàn), Lễ tân, Nhân viên buồng phòng, Kế toán, Quản lý; tác nhân ngoài: Cổng thanh toán, Kênh bán phòng trực tuyến (OTA), Hệ thống thông báo lưu trú của cơ quan công an.
- **Phạm vi tối thiểu:** tìm phòng trống theo khoảng ngày và loại phòng; đặt, sửa, hủy đặt phòng; đặt cọc; nhận phòng; đổi phòng; ghi dịch vụ phát sinh (minibar, giặt là, nhà hàng); trả phòng và xuất hóa đơn; quản lý tình trạng buồng; giá theo mùa và cuối tuần; báo cáo công suất phòng.
- **Trọng tâm đánh giá:** dùng đúng và có lập luận ba quan hệ giữa use case; phân biệt Loại phòng với Phòng cụ thể; lớp khoảng ngày `DateRange`; hai sơ đồ trạng thái độc lập cho phòng và cho đặt phòng.

#### Các bước gợi ý nghiên cứu

1. **Khảo sát hiện trạng (Chương 3).** Phỏng vấn lễ tân một khách sạn hoặc homestay; dùng thử bản demo QloApps ở cả trang đặt phòng lẫn trang quản trị để xem quy trình chuẩn. Thu thập bảng giá, chính sách hủy, giờ nhận và trả phòng; tìm hiểu quy định thông báo lưu trú (trước 23 giờ, khách đến sau 23 giờ thì trước 8 giờ sáng hôm sau) làm yêu cầu ràng buộc.
2. **Viết yêu cầu và quy tắc nghiệp vụ.** Yêu cầu phi chức năng quan trọng nhất: không được bán trùng một phòng khi website, OTA và lễ tân cùng đặt. Lập bảng quy tắc: đặt cọc, phí hủy theo số ngày báo trước, phụ thu nhận sớm – trả muộn, giá theo mùa.
3. **Sơ đồ use case (Chương 4).** Dùng có chủ đích cả ba quan hệ: `<<include>>` “Kiểm tra phòng trống” trong “Đặt phòng” và “Đổi phòng”; `<<extend>>` “Áp dụng mã khuyến mãi” vào “Đặt phòng”; tổng quát hóa “Thanh toán” thành “Thanh toán thẻ”, “Chuyển khoản”, “Tiền mặt”. Với mỗi quan hệ, viết một câu giải thích vì sao không chọn quan hệ khác.
4. **Sơ đồ hoạt động và tuần tự.** Sơ đồ hoạt động từ nhận phòng đến trả phòng với các làn Khách – Lễ tân – Buồng phòng – Kế toán. Sơ đồ tuần tự cho Đặt phòng trực tuyến có đặt cọc, Nhận phòng (gán phòng cụ thể, gửi thông báo lưu trú) và Trả phòng (tổng hợp chi phí).
5. **Sơ đồ lớp (Chương 5).** Gợi ý: `RoomType` 1–n `Room`; `Booking` giữ chỗ theo loại phòng, `Stay` gán phòng cụ thể khi nhận phòng; `DateRange` có `includes()`, `overlaps()`; `Guest`, `Folio`, `FolioCharge`, `Service`, `RatePlan`, `Season`. Thảo luận lớp nào nên chịu trách nhiệm `isAvailable(range)` và vì sao.
6. **Sơ đồ trạng thái.** `Room`: Trống sạch → Có khách → Trống bẩn → Đang dọn → Trống sạch, cùng nhánh Bảo trì. `Booking`: Tạm giữ → Đã xác nhận → Đã nhận phòng → Đã trả phòng, cùng các nhánh Đã hủy, Không đến; mô hình hóa sự kiện thời gian “hết giờ giữ phòng của ngày đến mà khách chưa nhận phòng”.
7. **Thiết kế (Chương 6).** Lưu khoảng ngày trong CSDL và viết điều kiện chồng lấn (hai khoảng $[a_1, b_1)$ và $[a_2, b_2)$ chồng nhau khi $a_1 < b_2$ và $a_2 < b_1$) để tìm phòng trống; đề xuất ràng buộc hoặc khóa chống bán trùng. Thiết kế adapter cho OTA và hệ thống thông báo lưu trú; màn hình sơ đồ phòng theo ngày cho lễ tân; sơ đồ triển khai gồm website đặt phòng, phần mềm quầy, máy chủ CSDL.

#### Tài liệu tham khảo *(kèm đường link gốc nhúng trong PDF)*

- [QloApps (GitHub)](https://github.com/Qloapps/QloApps) và [bản demo QloApps](https://demo.qloapps.com/) — hệ thống quản lý khách sạn và đặt phòng mã nguồn mở, dùng để khảo sát chức năng và cấu trúc dữ liệu.
- [Martin Fowler – Range](https://martinfowler.com/eaaDev/Range.html) — mẫu phân tích biểu diễn khoảng giá trị bằng một đối tượng, có ví dụ `DateRange` với các phép kiểm tra chồng lấn, bao hàm.
- [Visual Paradigm – Include and Extend Use Cases](https://blog.visual-paradigm.com/include-and-extend-use-cases/) — phân biệt include, extend, tổng quát hóa kèm ví dụ.
- [Thư viện Pháp luật – Khai báo lưu trú](https://thuvienphapluat.vn/phap-luat/chu-de/khai-bao-luu-tru) — trách nhiệm và thời hạn thông báo lưu trú của cơ sở lưu trú du lịch theo Luật Cư trú sửa đổi.
- **Giáo trình: Larman**, phần mô hình miền và sơ đồ trạng thái (xem mục Tài liệu tham khảo chung).

---

## PHẦN 3. NGUYÊN VĂN THÔNG TIN PHÂN CÔNG NHÓM 8 TRONG FILE EXCEL DANH SÁCH LỚP

Trích xuất nguyên văn từ tệp `File_thay-gui\02. NEW DS SV Lớp Phân tích thiết kế HĐT Chiều  thú 6.xlsx` (Dòng 1 tiêu đề và Dòng 26–29):

- **Các cột trong bảng Excel gốc:** `STT` | `Mã SV` | `Họ lót` | `Tên` | `Nhóm ` | `Đề tài` | `Hướng dẫn` | `Tài liệu tham khảo 1` | `Tài liệu tham khảo 2` | `Nhận xét` | `Điểm `
- **Danh sách thành viên Nhóm 8 (STT 25 → 28):**
  1. **STT 25:** Mã SV `3124411275` | Họ lót: `Đặng Phú` | Tên: `Thành` | Nhóm: `8`
  2. **STT 26:** Mã SV `3124411049` | Họ lót: `Nguyễn Trí` | Tên: `Cường` | Nhóm: `8`
  3. **STT 27:** Mã SV `3124411267` | Họ lót: `Võ Huỳnh Thanh` | Tên: `Tâm` | Nhóm: `8`
  4. **STT 28:** Mã SV `3124411142` | Họ lót: `Lê Anh ` | Tên: `Kiệt` | Nhóm: `8`
- **Đề tài (Ô F26:F29):**
  `Hệ thống đặt phòng và quản lý khách sạn`
- **Hướng dẫn (Ô G26:G29):**
  `Nhóm phân tích và thiết kế hệ thống cho một khách sạn quy mô vừa: đặt phòng trực tuyến và tại quầy, nhận phòng, ghi dịch vụ phát sinh, trả phòng, thanh toán và quản lý buồng phòng. Trọng tâm là tổ chức sơ đồ use case bằng đủ ba quan hệ include, extend, tổng quát hóa, và mô hình hóa khoảng thời gian lưu trú trong sơ đồ lớp lẫn CSDL.`
- **Tài liệu tham khảo 1 (Ô H26:H29):**
  - `• QloApps (GitHub) và bản demo QloApps — hệ thống quản lý khách sạn và đặt phòng mã nguồn mở, dùng để khảo sát chức năng và cấu trúc dữ liệu.`
  - `• Martin Fowler – Range — mẫu phân tích biểu diễn khoảng giá trị bằng một đối tượng, có ví dụ DateRange với các phép kiểm tra chồng lấn, bao hàm.`
- **Tài liệu tham khảo 2 (Ô I26:I29):**
  - `• Visual Paradigm – Include and Extend Use Cases — phân biệt include, extend, tổng quát hóa kèm ví dụ.`
  - `• Thư viện Pháp luật – Khai báo lưu trú — trách nhiệm và thời hạn thông báo lưu trú của cơ sở lưu trú du lịch theo Luật Cư trú sửa đổi.`
  - `• Giáo trình: Larman, phần mô hình miền và sơ đồ trạng thái (xem mục Tài liệu tham khảo chung).`

---

## PHẦN 4. NGUYÊN VĂN TÀI LIỆU THAM KHẢO CHUNG VÀ CÔNG CỤ (TRANG 18–19 PDF)

| Tài liệu | Loại | Dùng cho chương | Nên đọc |
| :--- | :--- | :--- | :--- |
| [Schach – Object-Oriented and Classical Software Engineering, 8th ed.](https://www.mheducation.com/highered/product/object-oriented-classical-software-engineering-schach/0073376183.html) | Tài liệu chính (đề cương) | 1–6 | Ch. 2 mô hình vòng đời; Ch. 13 phân tích hướng đối tượng |
| [Booch và cộng sự – Object-Oriented Analysis and Design with Applications, 3rd ed.](https://www.pearson.com/en-us/subject-catalog/p/object-oriented-analysis-and-design-with-applications/P200000000143/9780132797443) | Tham khảo (đề cương) | 2, 5, 6 | Ch. 2 mô hình đối tượng; Ch. 6 quy trình phân tích – thiết kế |
| [Larman – Applying UML and Patterns, 3rd ed.](https://www.informit.com/store/applying-uml-and-patterns-an-introduction-to-object-9780131489066) | Tham khảo (đề cương) | 4, 5, 6 | Use case, mô hình miền, GRASP, sơ đồ trạng thái, triển khai |
| [Sommerville – Software Engineering, 10th ed.](https://www.pearson.com/en-us/subject-catalog/p/software-engineering/P200000003258/9780137503148) | Tham khảo (đề cương) | 1, 3 | Ch. 2 quy trình phần mềm; Ch. 3 Agile; Ch. 4 kỹ nghệ yêu cầu |
| [OMG – UML 2.5.1 Specification](https://www.omg.org/spec/UML/2.5.1) | Đặc tả chuẩn | 2 | Tra cứu ký hiệu khi nhóm tranh luận cách vẽ đúng |
| [Visual Paradigm – Overview of the 14 UML Diagram Types](https://visual-paradigm.com/guide/uml-unified-modeling-language/overview-of-the-14-uml-diagram-types) | Hướng dẫn trực tuyến | 2, 4, 5, 6 | Mỗi loại sơ đồ có bài hướng dẫn riêng; bản Community Edition miễn phí |
| [uml-diagrams.org – UML Diagrams Examples](https://uml-diagrams.org/index-examples.html) | Ví dụ mẫu | 4, 5, 6 | Ví dụ use case, lớp, trạng thái, triển khai theo từng miền nghiệp vụ |
| [Scott Ambler – Mapping Objects to Relational Databases](https://agiledata.org/?p=3101) | Bài viết | 6.1 | Chuyển sơ đồ lớp sang mô hình quan hệ |
| [Nielsen Norman Group – 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) | Bài viết | 6.3 | Tiêu chí tự đánh giá bản thiết kế giao diện |
| [PlantUML](https://plantuml.com/) | Công cụ miễn phí | Mọi sơ đồ | Vẽ sơ đồ bằng văn bản, dễ quản lý phiên bản bằng Git |
| [draw.io](https://app.diagrams.net/) | Công cụ miễn phí | Mọi sơ đồ | Chạy trên trình duyệt, có sẵn thư viện ký hiệu UML |
| [StarUML](https://staruml.io/download) | Công cụ trả phí, dùng thử 30 ngày | Mọi sơ đồ | Mô hình hóa UML đầy đủ trong một tệp dự án |

---

## PHẦN 5. NGUYÊN VĂN ĐỀ ÔN TẬP GIỮA KỲ HỌC PHẦN 841111 (TRANG 1–2 FILE ÔN KIỂM TRA)

> *Trích nguyên văn từ tệp `On_Kiem_Tra\04. De Ôn thi kiểm tra giữa kỳ - Phân Tích TKHDT_he CLC-2026.pdf` để tham chiếu chuẩn câu hỏi và thang điểm của học phần.*

**TRƯỜNG ĐẠI HỌC SÀI GÒN**
**ĐỀ ÔN TẬP GIỮA KỲ HỌC PHẦN**
- **Học phần:** Phân tích thiết kế hướng đối tượng — **ĐỀ SỐ ….**
- **Mã học phần:** `841111`
- **Thời gian làm bài:** 150 phút, không kể thời gian phát đề
- **Học kỳ:** 1 — **Năm học:** 2026 – 2027
- **Sinh viên ĐƯỢC sử dụng tài liệu.** *(Cán bộ coi thi không giải thích gì thêm).*

### HỆ THỐNG QUẢN LÝ MƯỢN, TRẢ SÁCH

#### Tình huống
Thư viện một trường đại học cần xây dựng phần mềm quản lý mượn, trả sách với các yêu cầu sau:
1. Mỗi đầu sách có mã đầu sách, tên sách, tác giả và nhà xuất bản. Một đầu sách có thể có nhiều bản sao; mỗi bản sao có mã riêng và trạng thái `SAN_SANG` hoặc `DANG_MUON`.
2. Mỗi độc giả có mã độc giả, họ tên, email và ngày hết hạn thẻ.
3. Độc giả và thủ thư có thể tra cứu sách, xem thông tin đầu sách và số bản sao sẵn sàng.
4. Thủ thư lập phiếu mượn cho độc giả. Một phiếu gồm từ một đến ba bản sao khác nhau; mọi bản sao trong phiếu có cùng ngày mượn và hạn trả là 14 ngày sau ngày mượn.
5. Chỉ cho mượn khi:
   - Thẻ độc giả còn hiệu lực.
   - Tất cả bản sao được chọn đang sẵn sàng.
   - Tổng số bản sao độc giả đang giữ, cộng số bản sao muốn mượn, không vượt quá ba.
6. Nếu một điều kiện không thỏa mãn, hệ thống từ chối toàn bộ yêu cầu mượn và thông báo lý do. Nếu hợp lệ, hệ thống lưu phiếu, các chi tiết phiếu và chuyển các bản sao sang `DANG_MUON`.
7. Độc giả có thể trả từng bản sao trong một phiếu. Thủ thư ghi nhận ngày trả thực tế của từng bản sao; bản sao được chuyển về `SAN_SANG`.
8. Thủ thư phải đăng nhập trước khi thực hiện nghiệp vụ. Không xét tiền phạt, đặt trước sách, sách mất hoặc sách hỏng trong phạm vi đề.

#### Bảng Câu hỏi & Thang điểm

| Câu | Yêu cầu | Điểm |
| :---: | :--- | :---: |
| **1** | a) Phân biệt phân tích hướng đối tượng và thiết kế hướng đối tượng; minh họa bằng bài toán thư viện.<br>b) Trong trường hợp thư viện thường xuyên điều chỉnh yêu cầu sau khi xem bản mẫu, lựa chọn một quy trình phát triển phù hợp và giải thích. | **1,0** |
| **2** | a) Đề xuất hai kỹ thuật thu thập yêu cầu và thông tin cần thu được.<br>b) Nêu hai yêu cầu chức năng và đề xuất hai yêu cầu phi chức năng có thể kiểm chứng.<br>c) Vẽ sơ đồ Use Case, thể hiện tác nhân, ranh giới hệ thống và ít nhất một quan hệ `«include»` phù hợp. | **2,0** |
| **3** | Xây dựng sơ đồ lớp phân tích: xác định các lớp chính, thuộc tính, một số phương thức nghiệp vụ, quan hệ và bội số. Giải thích lựa chọn Composition và nêu các ràng buộc quan trọng. | **2,5** |
| **4** | a) Vẽ Sequence Diagram cho nghiệp vụ lập phiếu mượn, có nhánh hợp lệ và không hợp lệ.<br>b) Vẽ Activity Diagram cho nghiệp vụ này, thể hiện đầy đủ các điều kiện kiểm tra. | **2,5** |
| **5** | a) Chuyển mô hình lớp thành lược đồ quan hệ, chỉ rõ khóa chính và khóa ngoại.<br>b) Đề xuất kiến trúc phân lớp và minh họa bằng sơ đồ thành phần.<br>c) Thiết kế nội dung chính của màn hình lập phiếu mượn và cách phản hồi lỗi. | **2,0** |

---

## PHẦN 6. MA TRẬN KIỂM ĐỐI MỌI YÊU CẦU BẮT BUỘC CỦA ĐỒ ÁN 8 (CHECKLIST TỔNG HỢP)

| STT | Hạng mục yêu cầu | Số lượng / Quy định tối thiểu từ đề | Yêu cầu đặc thù bắt buộc riêng cho Đề tài 8 (Khách sạn) |
| :---: | :--- | :--- | :--- |
| **1** | **Phân công nhóm** | 1–5 SV (Nhóm 8 có 4 SV) | Mỗi thành viên phụ trách **ít nhất 1 cụm Use Case từ đặc tả đến thiết kế**, ghi rõ trong bảng phân công và tự đánh giá nhóm (CLO6). |
| **2** | **Hồ sơ văn bản nộp** | 4 tài liệu chính | 1. Đề cương đồ án<br>2. Báo cáo tiến độ<br>3. Báo cáo cuối kỳ (Chương 1, 3, 4, 5, 6, Kết luận, Phụ lục)<br>4. Slide bảo vệ |
| **3** | **Tệp đính kèm & Điểm cộng** | Tệp mô hình gốc + UI + Demo | 1. Tệp mô hình UML gốc (`PlantUML` / `draw.io` / `StarUML` / `Visual Paradigm`)<br>2. Bản mẫu giao diện (~8 màn hình)<br>3. **Bản Web Demo chạy được** (tính điểm cộng). |
| **4** | **Khảo sát & Nghiệp vụ (Chương 3)** | Khảo sát + Yêu cầu CN/PCN + Bảng thuật ngữ | - Phỏng vấn lễ tân khách sạn/homestay + Khảo sát bản demo **QloApps** (trang đặt phòng & trang quản trị).<br>- Thu thập bảng giá, chính sách hủy, giờ nhận/trả phòng.<br>- Quy định pháp lý **thông báo lưu trú**: trước **23 giờ**, khách đến sau 23 giờ thì báo trước **8 giờ sáng hôm sau**.<br>- Yêu cầu phi chức năng số 1: **Không được bán trùng một phòng** khi Website, OTA và Lễ tân cùng đặt.<br>- Bảng quy tắc nghiệp vụ: đặt cọc, phí hủy theo số ngày báo trước, phụ thu nhận sớm – trả muộn, giá theo mùa. |
| **5** | **Sơ đồ Use Case & Đặc tả (Chương 4)** | Use case tổng quát + phân rã + $\ge 6$ đặc tả Use Case chính | - Đủ 8 tác nhân: `Khách` (tổng quát hóa thành `Khách lẻ`, `Khách đoàn`), `Lễ tân`, `Nhân viên buồng phòng`, `Kế toán`, `Quản lý`; tác nhân ngoài: `Cổng thanh toán`, `Kênh bán phòng trực tuyến (OTA)`, `Hệ thống thông báo lưu trú của cơ quan công an`.<br>- Bắt buộc dùng đủ 3 quan hệ có chủ đích + **viết 1 câu giải thích vì sao không chọn quan hệ khác**:<br>  1. `<<include>>`: “Kiểm tra phòng trống” trong “Đặt phòng” và “Đổi phòng”<br>  2. `<<extend>>`: “Áp dụng mã khuyến mãi” vào “Đặt phòng”<br>  3. Tổng quát hóa: “Thanh toán” thành “Thanh toán thẻ”, “Chuyển khoản”, “Tiền mặt”. |
| **6** | **Sơ đồ Hoạt động (Chương 4)** | Tối thiểu **3 sơ đồ hoạt động** | Bắt buộc có Sơ đồ hoạt động xuyên suốt **từ Nhận phòng đến Trả phòng** với 4 làn: `Khách – Lễ tân – Buồng phòng – Kế toán`. |
| **7** | **Sơ đồ Tuần tự (Chương 4)** | Tối thiểu **5 sơ đồ tuần tự** | Bắt buộc có 3 sơ đồ cốt lõi:<br>1. Đặt phòng trực tuyến có đặt cọc<br>2. Nhận phòng (gán phòng cụ thể, gửi thông báo lưu trú)<br>3. Trả phòng (tổng hợp chi phí)<br>*(+ tối thiểu 2 sơ đồ tuần tự khác thuộc các cụm thành viên, ví dụ: Đổi phòng, Ghi dịch vụ phát sinh / Hủy đặt phòng).* |
| **8** | **Sơ đồ Lớp (Chương 5)** | Sơ đồ lớp **mức phân tích** và **mức thiết kế** | - Phân biệt `RoomType` 1–n `Room`.<br>- `Booking` giữ chỗ theo loại phòng (`RoomType`), `Stay` gán phòng cụ thể (`Room`) khi nhận phòng.<br>- Lớp `DateRange` có `includes()`, `overlaps()`.<br>- Các lớp gợi ý: `Guest`, `Folio`, `FolioCharge`, `Service`, `RatePlan`, `Season`.<br>- Thảo luận rõ lớp nào chịu trách nhiệm `isAvailable(range)` và vì sao. |
| **9** | **Sơ đồ Trạng thái (Chương 5)** | Tối thiểu **2 sơ đồ trạng thái** | Hai sơ đồ trạng thái độc lập:<br>1. **`Room`:** `Trống sạch → Có khách → Trống bẩn → Đang dọn → Trống sạch`, cùng nhánh `Bảo trì`.<br>2. **`Booking`:** `Tạm giữ → Đã xác nhận → Đã nhận phòng → Đã trả phòng`, cùng các nhánh `Đã hủy`, `Không đến`; mô hình hóa sự kiện thời gian *“hết giờ giữ phòng của ngày đến mà khách chưa nhận phòng”*. |
| **10** | **Thiết kế CSDL (Chương 6)** | Lược đồ CSDL quan hệ | - Lưu khoảng ngày trong CSDL.<br>- Viết điều kiện chồng lấn: hai khoảng $[a_1, b_1)$ và $[a_2, b_2)$ chồng nhau khi $a_1 < b_2$ và $a_2 < b_1$ để tìm phòng trống.<br>- Đề xuất ràng buộc hoặc khóa chống bán trùng (Transaction Isolation / Locking / Constraint). |
| **11** | **Kiến trúc, Thành phần, Cộng tác, Triển khai (Chương 6)** | 1 Kiến trúc tổng thể + 1 Thành phần + $\ge 2$ Cộng tác + 1 Triển khai | - Thiết kế **Adapter** cho **OTA** và **Hệ thống thông báo lưu trú**.<br>- Sơ đồ triển khai gồm: **Website đặt phòng**, **Phần mềm quầy**, **Máy chủ CSDL** (và kết nối các hệ thống ngoài). |
| **12** | **Thiết kế Giao diện & Demo (Chương 6)** | Khoảng **8 màn hình giao diện** + **Web Demo** | - Bắt buộc có **Màn hình sơ đồ phòng theo ngày cho lễ tân (Room Rack / Tape Chart)**.<br>- Đánh giá theo 10 Usability Heuristics của Nielsen Norman Group.<br>- Xây dựng bản **Web Demo chạy được** để lấy điểm cộng bảo vệ. |
