# Tổ Vận Hành - Nước | Bệnh viện đa khoa Vĩnh Phúc

Ứng dụng web quản lý checklist vận hành ca trực cho Tổ Nước — chạy hoàn toàn trên trình duyệt, **không cần mạng Internet**, không cần backend.

## Tính năng

- **Checklist vận hành**: Trạm XLNT (MBR), Cấp nước sinh hoạt, Trạm RO, Bơm nước thải TNT (GĐ1/GĐ2), Bể tách mỡ
- **Quan trắc chỉ số online**: pH, TSS, BOD, Amoni, TDS — tự động cảnh báo khi vượt chuẩn
- **Nhật ký hóa chất & kho hóa chất**: nhập/xuất/tồn, xuất báo cáo Excel (.xlsx)
- **Quản lý vật tư, sự cố, thiết bị**
- **Xuất báo cáo ca trực** (Excel), xem trước báo cáo
- **Lưu trữ local**: toàn bộ dữ liệu lưu trong `localStorage` của trình duyệt
- Giao diện tối ưu cho điện thoại (mobile-first), có thể **Add to Home Screen** như app

## Chạy offline

Toàn bộ thư viện (Tailwind CSS, Font Awesome + fonts) đã được đóng gói sẵn trong thư mục `assets/`, không còn phụ thuộc CDN. Chỉ cần mở `index.html` là chạy, kể cả khi không có mạng.

## Deploy lên GitHub Pages

1. Tạo repo mới trên GitHub
2. Push toàn bộ thư mục này lên repo:
   ```bash
   git remote add origin https://github.com/<username>/<repo>.git
   git push -u origin main
   ```
3. Vào **Settings → Pages → Build and deployment**, chọn **Deploy from a branch**, branch `main`, thư mục `/ (root)`
4. Mở link `https://<username>.github.io/<repo>/` để sử dụng

## Cấu trúc

```
├── index.html              # App chính
├── manifest.json           # Cấu hình PWA / Add to Home Screen
├── assets/
│   ├── js/tailwind.js      # Tailwind CSS (local)
│   ├── fontawesome/        # Font Awesome 6.4.0 + webfonts (local)
│   └── img/                # Icon app (SVG + PNG)
└── README.md
```

## Lưu ý

- Dữ liệu lưu trên trình duyệt (localStorage) — mỗi thiết bị/trình duyệt có dữ liệu riêng
