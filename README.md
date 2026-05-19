# DNG Investment — Landing Page

Website landing page cho **Công ty Cổ phần Tập đoàn Đầu tư Quốc tế DNG**.

## Cấu trúc

```
dnginvest/
├── index.html        # Trang chủ duy nhất (single-page)
├── images/           # Toàn bộ ảnh
│   ├── LOGODNG.png
│   ├── phongkham.png
│   ├── vncord.png
│   ├── dng-clinic.png
│   ├── tazawa.png
│   ├── yarraland.png
│   ├── machinex.png
│   ├── Picture13.png
│   └── haivan-park.png
├── vercel.json       # Config deploy Vercel
├── .gitignore
└── README.md
```

## Deploy lên Vercel

### Cách 1: Qua GitHub (khuyến nghị)

1. Tạo repo mới trên GitHub, đặt tên `dnginvest` (hoặc tùy ý)
2. Push code lên:
   ```bash
   git init
   git add .
   git commit -m "init: DNG Invest landing page"
   git remote add origin https://github.com/<username>/<repo>.git
   git push -u origin main
   ```
3. Vào [vercel.com](https://vercel.com) → **Add New Project** → Import repo vừa tạo
4. Framework Preset: **Other** (static)
5. Nhấn **Deploy** → xong ✅

### Cách 2: Vercel CLI

```bash
npm i -g vercel
vercel login
vercel --prod
```

## Gắn domain dnginvest.vn

Sau khi deploy xong trên Vercel:
1. Vào **Project Settings → Domains**
2. Thêm `dnginvest.vn` và `www.dnginvest.vn`
3. Vercel sẽ cấp SSL tự động (HTTPS)
4. Cập nhật DNS tại nhà đăng ký domain:
   - **A record**: `@` → IP Vercel (Vercel sẽ hiển thị)
   - **CNAME**: `www` → `cname.vercel-dns.com`
