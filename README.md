# Construction Toolkit — Bộ Công Cụ Xây Dựng

Bộ 18 công cụ cho công tác thi công, đấu thầu, tài chính dự án xây dựng.
Toàn bộ là **static site**: mỗi công cụ là một file HTML độc lập (HTML/CSS/JS thuần, dữ liệu nhúng sẵn),
chạy hoàn toàn trên trình duyệt, không cần backend, không upload dữ liệu đi đâu.

Mở `index.html` để vào trang tổng (dashboard) liệt kê tất cả công cụ theo nhóm.

## Danh sách công cụ

### 🏗️ Thi Công

| Công cụ | File | Mô tả |
|---|---|---|
| Định Mức RSMeans v7 | `Dinh-Muc-Xay-Dung-RSMeans-v7.html` | Tra cứu định mức năng suất nhân công & thiết bị theo RSMeans, lọc/sắp xếp, biểu đồ |
| Định Mức TT10/2019 | `Dinh Muc Xay Dung TT10.2019 - Ban Day Du.html` | Tra cứu định mức dự toán TT10/2019/TT-BXD (bản đầy đủ), lập bảng hao phí VL/NC/MTC theo khối lượng. Có nút “Hướng dẫn” (`Huong-dan-Dinh-Muc-TT10.html`): cách tìm, đọc mã hiệu, chú thích 13 chương |
| Checklist Nhà Cao Tầng | `Checklist-Nha-Cao-Tang.html` | Checklist QA/QC thi công & dự thầu nhà cao tầng, lưu trạng thái, in được |
| Checklist Tầng Hầm | `checklist-tang-ham.html` | Checklist QA/QC thi công tầng hầm, in A4 |
| Biểu Đồ Huy Động | `bieu-do-huy-dong.html` | Lập biểu đồ huy động nhân lực & máy móc, xuất PDF (jsPDF/html2canvas nhúng sẵn) |
| Metal Calculator | `metal-calculator.html` | Tính khối lượng thép hình (H, I, U, L, hộp, ống, tấm…) |

### 📋 Đấu Thầu

| Công cụ | File | Mô tả |
|---|---|---|
| QT Đấu Thầu | `CHECKLIST-01-QUY-TRINH-DAU-THAU.html` | Checklist quy trình đấu thầu |
| QT Đấu Thầu D&B | `CHECKLIST-02-QUY-TRINH-DU-AN-DB.html` | Checklist quy trình dự án Design & Build |
| Tổng Hợp TCQ / RFI | `TCQ RFI template.html` | Mẫu tổng hợp câu hỏi làm rõ (TCQ) / RFI |
| Danh Mục Vật Tư & BOQ | `Danh-muc-vat-tu-tra-cuu.html` | Nhập BOQ (Excel/CSV/dán, hỗ trợ font TCVN3) → tự đề xuất danh mục vật tư theo từng dòng công việc; tra cứu ~1.800 vật tư phân loại Bộ môn → Nhóm → Loại kèm tiêu chuẩn TCVN; xuất Excel danh mục + bảng đối chiếu BOQ |

### 💰 Tài Chính

| Công cụ | File | Mô tả |
|---|---|---|
| Chi Phí Nhân Sự | `Tinh-Chi-Phi-Nhan-Su-Du-An-v1.6.html` | Tính chi phí bộ máy nhân sự dự án theo giá trị & thời gian thi công |
| Cashflow S-Curve | `cashflow-projection-tool-v6.html` | Dự báo dòng tiền, đường cong S, kịch bản; xuất Excel/PDF |
| Chi Phí Công Tác Tạm | `Du_tru_chi_phi_CTT.html` | Dự trù chi phí công tác tạm theo quy mô hợp đồng và số tháng |

### 🧰 Tiện Ích

| Công cụ | File | Mô tả |
|---|---|---|
| Số Tiền Bằng Chữ | `so-tien-bang-chu.html` | Đổi số tiền thành chữ tiếng Việt / tiếng Anh |
| Excel Cleaner | `excel-cleaner.html` | Sửa lỗi "invalid XML" / stylesheet, xóa named range lỗi và calcChain cho file Excel (.xlsx…) — **giữ nguyên định dạng ô** (Comma style, định dạng số, font, màu) |
| Excel In & PDF | `excel-print-pdf.html` | Cài đặt in cho toàn bộ file Excel (khổ giấy, hướng, vừa 1 trang ngang, lề, vùng in, dòng tiêu đề lặp tự dò theo BOQ, header/footer, ngắt trang) → tải xlsx đã cài đặt, hoặc xuất PDF ngay trong trình duyệt (xem trước + tải về) |
| Danh Bạ Email | `ThongTin.html` | Danh bạ email tra cứu — dữ liệu được **mã hóa** (AES, PBKDF2), cần mật khẩu để mở |

### 📚 Tài Liệu

| Công cụ | File | Mô tả |
|---|---|---|
| Cẩm Nang Đàm Phán HĐ FIDIC | `CAM NANG DAM PHAN HD_FIDIC.html` | Cẩm nang đàm phán hợp đồng thi công FIDIC Red Book theo góc nhìn Nhà thầu, lọc theo chương/mức ưu tiên |

## Cấu trúc thư mục

```
.
├── index.html     # Dashboard — trang chủ liệt kê công cụ
├── *.html         # Mỗi công cụ là 1 file độc lập (18 file)
├── lib/           # Thư viện đóng gói sẵn cho Excel In & PDF (xem lib/README.md)
├── .nojekyll      # Tắt Jekyll trên GitHub Pages
└── README.md
```

## Chạy cục bộ

Không cần cài đặt gì — mở trực tiếp file `.html` bằng trình duyệt. Hoặc chạy một web server tĩnh:

```bash
python3 -m http.server 8000
# mở http://localhost:8000
```

## Deploy lên GitHub Pages

1. Push repo lên GitHub.
2. Vào **Settings → Pages** → **Source**: chọn branch `main`, thư mục `/ (root)` → **Save**.
3. Sau khoảng 1 phút, site có tại `https://<username>.github.io/<repo-name>/`.

## Thư viện bên ngoài

Phần lớn công cụ chạy hoàn toàn offline. Một số công cụ tải thư viện qua CDN (cần internet lần đầu):

| Công cụ | Thư viện (cdnjs) |
|---|---|
| Định Mức RSMeans | Chart.js 3.9 |
| Cashflow S-Curve | Chart.js 4.4, SheetJS (xlsx) 0.18, jsPDF 2.5, html2canvas 1.4 |
| Excel Cleaner | JSZip 3.10 |
| Excel In & PDF | Không dùng CDN — thư viện nằm trong `lib/`: JSZip 3.10, ExcelJS 4.4, pdfmake 0.2 (kèm font Roboto), SSF 0.11 |
| Danh Mục Vật Tư & BOQ | SheetJS (xlsx) 0.18 — chỉ khi nhập file .xls cũ; .xlsx/.csv đọc & xuất offline |

Font chữ dùng Google Fonts; khi offline trình duyệt tự dùng font hệ thống.

## Lưu ý

- Dữ liệu người dùng nhập (trạng thái checklist, ghi chú…) được lưu trong `localStorage` của trình duyệt — chỉ nằm trên máy người dùng.
- Khi thêm công cụ mới: tạo file HTML độc lập, sau đó thêm một ô (`<a class="tile">`) vào nhóm tương ứng trong `index.html` và cập nhật số đếm của nhóm.
- Tên file có dấu cách (ví dụ `TCQ RFI template.html`) vẫn hoạt động; liên kết trong `index.html` đã được mã hóa URL (`%20`).
