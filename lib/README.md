# lib/

Thư viện bên thứ ba đóng gói sẵn cho `excel-print-pdf.html` (chạy được cả khi offline, không phụ thuộc phiên bản trên CDN).
Không sửa nội dung các file này — cập nhật bằng cách thay file mới từ nguồn.

| File | Thư viện | Phiên bản | Giấy phép | Nguồn |
|---|---|---|---|---|
| `jszip.min.js` | JSZip | 3.10.1 | MIT (hoặc GPL-3.0-or-later) | https://github.com/Stuk/jszip |
| `exceljs.min.js` | ExcelJS | 4.4.0 | MIT | https://github.com/exceljs/exceljs |
| `pdfmake.min.js` | pdfmake | 0.2.20 | MIT | https://github.com/bpampuch/pdfmake |
| `vfs_fonts.js` | Font Roboto đóng gói cho pdfmake (có đủ chữ Việt) | 0.2.20 | Apache-2.0 (font Roboto) | gói npm `pdfmake`, `build/vfs_fonts.js` |
| `ssf.js` | SSF (định dạng số kiểu Excel, của SheetJS) | 0.11.2 | Apache-2.0 | https://github.com/SheetJS/ssf |

Lấy từ gói npm tương ứng (`npm pack <tên>@<phiên bản>`): `dist/jszip.min.js`, `dist/exceljs.min.js`, `build/pdfmake.min.js`, `build/vfs_fonts.js`, `ssf.js`.
