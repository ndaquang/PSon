# Construction Tools Portal — VITECCONS

Bộ công cụ xây dựng tích hợp, deploy tĩnh trên GitHub Pages.

## 📦 Cấu trúc

```
portal/
├── index.html               ← Portal chính (navigation + iframe host)
├── dinh-muc-rsmeans-v6.html ← Định mức năng suất RSMeans v6.0
├── checklist-tang-ham.html  ← Checklist thi công tầng hầm
├── bieu-do-huy-dong.html    ← Biểu đồ huy động nhân lực & máy móc
└── excel-cleaner.html       ← Excel Cleaner
```

## 🚀 Deploy lên GitHub Pages

### Bước 1 — Tạo repo
```bash
git init
git add .
git commit -m "initial: construction tools portal"
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main
```

### Bước 2 — Bật GitHub Pages
1. Vào **Settings** → **Pages**
2. Source: **Deploy from a branch**
3. Branch: `main` / folder: `/ (root)` → Save

### Bước 3 — Truy cập
```
https://<username>.github.io/<repo>/
```

## 🛠 Công cụ trong portal

| Công cụ | Mô tả | Tag |
|---------|-------|-----|
| Định Mức RSMeans v6.0 | Tra cứu định mức năng suất lao động & máy thi công | CALC |
| Checklist Tầng Hầm | Danh sách kiểm tra thi công tầng hầm | QC |
| Biểu Đồ Huy Động | Biểu đồ nhân lực & máy móc cho dự án nhà xưởng | CHART |
| Excel Cleaner | Làm sạch & chuẩn hóa file Excel | TOOL |

## 📌 Lưu ý

- Toàn bộ là **static HTML** — không cần server, không cần backend
- Mỗi tool chạy trong `<iframe>` riêng biệt để tránh xung đột CSS/JS
- Các thư viện ngoài (Chart.js, JSZip, html2canvas...) load từ CDN — cần internet
