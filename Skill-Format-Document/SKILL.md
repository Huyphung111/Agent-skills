---
name: dinh-dang-bao-cao-word
description: "Áp dụng bộ quy tắc định dạng chuẩn (font, size, paragraph spacing, heading phân cấp, đánh số trang, bảng biểu, chú thích ảnh, màu sắc) cho các file Word dạng báo cáo/đồ án/SRS/PTYC học thuật theo mẫu của Huy. LUÔN dùng skill này khi Huy nhờ 'định dạng lại file Word', 'chuẩn hóa format báo cáo/đồ án', 'chỉnh heading cho đúng', 'gen mục lục', 'đánh số trang', hoặc khi tạo/chỉnh sửa bất kỳ file .docx nào là báo cáo, đồ án, SRS, PTYC, khóa luận — kể cả khi Huy không liệt lại chi tiết từng quy tắc mà chỉ nói 'format theo chuẩn cũ' hoặc 'làm giống mấy lần trước'. Dùng cùng với skill docx để thao tác kỹ thuật trên file."
---

# Định dạng báo cáo/đồ án Word (chuẩn của Huy)

Skill này định nghĩa **quy tắc trình bày** cho các file Word dạng báo cáo/đồ án/SRS/PTYC. Đây là lớp "quy tắc nghiệp vụ" — còn cách thao tác kỹ thuật trên file `.docx` (tạo bằng docx-js, sửa bằng XML, render kiểm tra bằng LibreOffice) thì dùng skill `docx`. Hai skill này đi cùng nhau.

Nguyên tắc bao trùm: **mọi chữ trong văn bản đều màu đen**, không có mục nào tô màu/tô nền (kể cả bảng), trừ khi Huy yêu cầu khác đi trong lần đó.

## 1. Bảng quy tắc theo loại nội dung

| Loại nội dung | Font | Size | Căn lề | Kiểu chữ | Line spacing | Before/After |
|---|---|---|---|---|---|---|
| Văn bản thân bài (nội dung thường) | Times New Roman | 13 | Đều hai bên (Justify) | Đứng, thường | Multiple, tại 1.3 | 3pt / 3pt |
| Mục trước Chương 1 (Mục Lục, Danh mục bảng, Danh mục hình, Lời cảm ơn, Mở đầu, Bảng phân công công việc, v.v.) | Times New Roman | 18 | Giữa | Đứng, có thể đậm nếu là tiêu đề mục lớn | Multiple, tại 1.3 | theo mặc định, không ghi đè trừ khi có yêu cầu |
| Tiêu đề mở đầu chương ("Chương 1 ...", "Chương 2 ...") | Times New Roman | 18 | Giữa | Đứng | Multiple, tại 1.3 | như trên |
| Heading mục trong chương (1, 1.1, 1.1.1, 1.1.1.1...) | Times New Roman | 13 | Trái | Xem mục 2 (đậm, chữ hoa, in nghiêng theo cấp) | Multiple, tại 1.3 | như văn bản thân bài trừ khi có yêu cầu khác |
| Chú thích ảnh (label ảnh) | Times New Roman | 13 | Theo vị trí ảnh (thường giữa) | In nghiêng, **không đậm**, chữ thường (không viết hoa) | Multiple, tại 1.3 | như văn bản thân bài |
| Nội dung trong bảng | Times New Roman | 13 | Theo cột | Đứng | — | After = 6pt nếu các dòng dính sát nhau, xem mục 3 |
| Hàng tiêu đề bảng (tên cột) | Times New Roman | 13 | Theo cột | **Đậm** | — | như trên |

## 2. Heading — phân cấp, chữ hoa, đậm/nghiêng

- Đánh số phân cấp luôn dùng **số Ả Rập**: **Mức 1 = "1."**, **Mức 2 = "1.1"**, **Mức 3 = "1.1.1"**, **Mức 4 (nếu có) = "1.1.1.1"**. Heading trong chương không dùng số La Mã — số La Mã chỉ dùng để đánh số trang phần trước Chương 1 (xem mục 7), hai việc này tách biệt nhau.
- Toàn bộ heading có đánh số (mọi mức) đều: Times New Roman, size 13, **chữ hoa (viết hoa toàn bộ)**, **đậm**.
- Từ mức 2 trở đi (1.1, 1.1.1, 1.1.1.1, ...): thêm **in nghiêng**. Mức 1 ("1.") giữ **đứng thẳng**, không nghiêng.
- **Luôn kiểm tra tính liên tục của số thứ tự** trước khi giao file: liệt kê toàn bộ heading theo đúng thứ tự xuất hiện trong văn bản và xác nhận không bị nhảy số (ví dụ 1.1 → 1.2 → tự nhiên nhảy lên 1.4 là sai), không bị trùng số, không bị lệch cấp (mục con phải nằm dưới đúng mục cha). Đây là bước dễ bị bỏ sót khi chỉnh sửa nhiều heading cùng lúc nên phải rà lại toàn bộ danh sách, không chỉ sửa chỗ được yêu cầu.
- Nên dùng multilevel list gắn với Heading style của Word (Heading 1/2/3) để số tự cập nhật và mục lục lấy đúng — tránh gõ tay số thứ tự nếu có thể, vì gõ tay dễ gây ra đúng lỗi nhảy số ở trên.

## 3. Bảng biểu

Nếu nội dung trong các dòng của bảng bị dính sát nhau, không có khoảng cách rõ ràng để phân biệt dòng: đặt **Spacing After = 6pt** cho paragraph trong các ô của bảng (thay vì 3pt như văn bản thường) để dòng bảng thoáng hơn.

## 4. Ảnh và chú thích ảnh

- Mỗi ảnh phải có tên/chú thích đi kèm.
- Chú thích ảnh: chữ thường (không viết hoa toàn bộ), Times New Roman, size 13, **in nghiêng**, **không in đậm**, màu đen.

## 5. Thụt lề đoạn văn

Bất kỳ đoạn văn nào xuống hàng (đoạn mới) đều có **thụt lề đầu dòng (First line indent) = 1.27 cm**, giống cấu hình trong hộp thoại "Đoạn Văn" mà Huy đã gửi (Đặc biệt: Dòng đầu, Cách: 1,27 cm).

## 6. Mục lục (Table of Contents)

Tự động sinh Mục lục dựa trên các heading đã được gắn cấp (Heading 1/2/3 hoặc outline level tương ứng) theo đúng mục 2. Không gõ tay mục lục — dùng field TOC của Word (hoặc tương đương khi tạo bằng docx-js) để mục lục tự cập nhật theo đúng số trang và số thứ tự heading thật.

## 7. Đánh số trang — BẮT BUỘC hỏi Huy trước khi thực hiện

Quy tắc mặc định (áp dụng sau khi đã xác nhận với Huy):
- Nếu file có trang bìa (khung bìa): **trang bìa không đánh số**.
- Bắt đầu đánh số từ trang đầu tiên **sau** trang bìa, dùng **số La Mã thường (i, ii, iii, ...)**.
- Số La Mã dùng cho toàn bộ phần trước Chương 1 (Lời cảm ơn, Mục lục, Danh mục bảng/hình, Mở đầu, Bảng phân công công việc...).
- Khi vào **Chương 1**, chuyển sang số Ả Rập bắt đầu lại từ **1**.

**Trước khi áp dụng đánh số trang, luôn hỏi lại Huy các điểm sau (đừng tự suy đoán):**
1. File có trang bìa hay không, và trang bìa có nằm trong cùng file cần đánh số này không.
2. Đâu là trang đầu tiên cần bắt đầu số La Mã (thứ tự các mục trước Chương 1 có thể thay đổi giữa các đồ án).
3. Đâu là trang đầu tiên của Chương 1 (nơi số Ả Rập bắt đầu lại từ 1).

Lý do phải hỏi: đánh số trang sai (lệch section break, quên restart số) là lỗi khó phát hiện bằng mắt khi chỉ xem một vài trang, nhưng lại rất dễ bị giám khảo/người review để ý — nên xác nhận trước rẻ hơn nhiều so với sửa lại sau khi đã đóng file.

## 8. Màu sắc và tô nền

- Toàn bộ chữ trong văn bản: màu đen (không dùng theme color tự động có thể ánh xám/xanh).
- Bảng: giữ nguyên trắng đen, không tô màu nền ô/hàng/cột.
- Chú thích ảnh cũng giữ màu đen như trên.

## 9. Bảng tham chiếu giá trị kỹ thuật (khi thao tác trực tiếp trên XML hoặc docx-js)

Dùng bảng này khi chỉnh `word/document.xml` (theo hướng dẫn của skill `docx`) hoặc khi viết script docx-js — đừng áng chừng bằng mắt, sai số nhỏ ở đây (vd nhầm pt với half-point) là lỗi rất phổ biến.

| Thuộc tính hiển thị | Giá trị OOXML (`document.xml`) | Giá trị docx-js |
|---|---|---|
| Font Times New Roman | `<w:rFonts w:ascii="Times New Roman" w:hAnsi="Times New Roman" w:cs="Times New Roman"/>` | `font: "Times New Roman"` |
| Size 13pt | `<w:sz w:val="26"/> <w:szCs w:val="26"/>` | `size: 26` |
| Size 18pt | `<w:sz w:val="36"/> <w:szCs w:val="36"/>` | `size: 36` |
| Line spacing multiple 1.3 | `<w:spacing w:line="312" w:lineRule="auto"/>` | `spacing: { line: 312, lineRule: "auto" }` |
| Before 3pt | `w:before="60"` | `spacing: { before: 60 }` |
| After 3pt | `w:after="60"` | `spacing: { after: 60 }` |
| After 6pt (dòng trong bảng) | `w:after="120"` | `spacing: { after: 120 }` |
| First line indent 1.27cm | `<w:ind w:firstLine="720"/>` | `indent: { firstLine: 720 }` |
| Chữ hoa toàn bộ (giữ nguyên text gốc) | `<w:caps/>` | `allCaps: true` |
| Đậm | `<w:b/>` | `bold: true` |
| Nghiêng | `<w:i/>` | `italics: true` |
| Màu đen tường minh | `<w:color w:val="000000"/>` | `color: "000000"` |

Ghi chú: `w:sz`/`size` tính theo **half-point** (13pt → 26, 18pt → 36) — đây là lỗi hay bị nhầm nhất. `w:before`/`w:after`/`w:firstLine` tính theo **twentieths of a point (dxa)** — 1pt = 20, 1cm ≈ 566.9 (1.27cm = 720 vừa đúng 0.5 inch).

## 10. Quy trình đề xuất khi thực hiện

1. Xác định file đang tạo mới hay chỉnh sửa file có sẵn → chọn cách thao tác phù hợp theo skill `docx` (docx-js cho tạo mới, unzip + sửa XML cho file có sẵn).
2. Nếu có liên quan tới đánh số trang → hỏi Huy 3 câu ở mục 7 trước khi làm.
3. Áp dụng bảng quy tắc ở mục 1–6, 8 cho từng loại nội dung tương ứng.
4. Rà lại toàn bộ heading theo mục 2 để đảm bảo số thứ tự liên tục và đúng cấp.
5. Sinh/khớp lại mục lục sau khi heading đã ổn định.
6. Render file ra ảnh (theo hướng dẫn `soffice.py` + `pdftoppm` trong skill `docx`) và tự kiểm tra bằng checklist ở mục 11 trước khi báo hoàn thành.

## 11. Checklist trước khi giao file

- [ ] Văn bản thân bài: TNR 13, line spacing 1.3, before/after 3pt, thụt lề đầu dòng 1.27cm ở các đoạn xuống hàng.
- [ ] Các mục trước Chương 1 và tiêu đề chương: TNR 18, căn giữa.
- [ ] Heading theo cấp: TNR 13, chữ hoa, đậm; mức ≥2 có thêm nghiêng; mức 1 đứng thẳng.
- [ ] Số thứ tự heading liên tục, đúng cấp, không nhảy số, không trùng.
- [ ] Bảng: dòng không bị dính, đã set after 6pt nếu cần; không tô màu nền; hàng tiêu đề/tên cột đã in đậm.
- [ ] Ảnh: có chú thích, chú thích chữ thường, nghiêng, không đậm.
- [ ] Toàn bộ chữ màu đen.
- [ ] Mục lục khớp với heading và số trang thật.
- [ ] Đánh số trang: đã hỏi và xác nhận với Huy trước khi áp dụng; bìa không số (nếu có bìa); La Mã cho phần trước Chương 1; Ả Rập bắt đầu lại từ 1 tại Chương 1.


