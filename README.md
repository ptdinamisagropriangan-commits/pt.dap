# myisthree.com - PT. Dinamis Agro Priangan Platform

![myisthree Logo](./public/logo-placeholder.png)

**Tagline:** Growing Together

## 📋 Deskripsi Project

myisthree.com adalah platform terintegrasi untuk meningkatkan pelayanan Business-to-Business (B2B) PT. Dinamis Agro Priangan. Platform ini menghubungkan:
- **Internal Management**: Work from Anywhere (WFA) system
- **B2B Partners**: Koperasi, BumDes, Pembeli, dan IKM
- **Product Marketplace**: Sistem stok dan order real-time

### Visi & Misi
Sarana kita tumbuh bersama dalam rantai pasok berkelanjutan untuk barang berkualitas dan volume terjaga.

---

## 🏢 Tentang PT. Dinamis Agro Priangan

**Berdiri:** 2016
**Bidang Usaha:** Perdagangan Umum & Ekspor-Impor

### Lokasi
```
Jl. Raya Tanjung Mulya No. 361
RT: 002 RW: 009
Kecamatan Panumbangan
Kabupaten Ciamis, Indonesia

Telepon: 082317226505, 081522807479
Email: pt.dinamis.agro.priangan@gmail.com
```

---

## 🎯 Fitur Utama

### 1. **Homepage (Public)**
- Menu navigasi utama
- Login Intranet (Internal Management)
- Login B2B (Partners)
- About Us (Profil Perusahaan)
- Produk (Marketplace - Mirip Shopee)
- Logo & Tagline myisthree
- Alamat lengkap perusahaan
- Background: Desain terkait alam Indonesia dan produk pertanian

### 2. **Login Intranet (Internal Management)**
- Autentikasi karyawan manajemen
- Dashboard WFA (Work From Anywhere)
- Manajemen user/karyawan
- Integrasi folder & file dari Google Drive
- Real-time collaboration tools

### 3. **Login B2B (Partners)**
- Registrasi mitra (Koperasi, BumDes, Pembeli, IKM)
- Dashboard Partner
- Menu: "Produk & Order"
- Upload produk ke stok
- Tracking order real-time
- Harga tersembunyi (B2B only)
- Checkout → Register Form Corporate

### 4. **About Us**
- Profil perusahaan
- Sejarah dan pengalaman
- Contact information

---

## 🛠️ Tech Stack

### Frontend
- **Framework**: Next.js 14 (React)
- **Styling**: Tailwind CSS
- **UI Components**: Shadcn/ui
- **State Management**: Zustand
- **HTTP Client**: Axios
- **Form**: React Hook Form + Zod

### Backend
- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: PostgreSQL / SQLite (dev)
- **ORM**: Prisma
- **Authentication**: JWT + bcrypt
- **Validation**: Zod

### DevOps
- **Package Manager**: pnpm
- **Version Control**: Git
- **Environment**: dotenv
- **Linting**: ESLint
- **Formatting**: Prettier
- **Testing**: Jest
- **Docker**: Docker Compose

---

## 📁 Struktur Project

```
pt.dap/
├── frontend/                 # Next.js Application
│   ├── public/
│   │   ├── logo-myisthree.png
│   │   ├── bg-natural.jpg
│   │   └── favicon.ico
│   ├── src/
│   │   ├── app/
│   │   │   ├── layout.tsx
│   │   │   ├── page.tsx              # Homepage
│   │   │   ├── about/
│   │   │   ├── login-intranet/
│   │   │   ├── login-b2b/
│   │   │   ├── products/
│   │   │   ├── dashboard/
│   │   │   └── api/
│   │   ├── components/
│   │   ├── lib/
│   │   ├── types/
│   │   ├── styles/
│   │   └── utils/
│   ├── .env.example
│   ├── package.json
│   ├── tsconfig.json
│   ├── next.config.js
│   └── tailwind.config.ts
│
├── backend/                  # Node.js + Express API
│   ├── src/
│   │   ├── server.ts
│   │   ├── config/
│   │   ├── controllers/
│   │   ├── routes/
│   │   ├── middleware/
│   │   ├── models/
│   │   ├── services/
│   │   └── utils/
│   ├── prisma/
│   │   └── schema.prisma
│   ├── .env.example
│   ├── package.json
│   ├── tsconfig.json
│   └── Dockerfile
│
├── docs/                     # Documentation
│   ├── API.md
│   ├── SETUP.md
│   ├── DATABASE.md
│   └── DEPLOYMENT.md
│
├── docker-compose.yml
├── .gitignore
└── README.md
```

---

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ 
- pnpm (`npm install -g pnpm`)
- PostgreSQL 14+ (atau gunakan Docker)
- Git

### Setup Development

#### 1. Clone Repository
```bash
git clone https://github.com/ptdinamisagropriangan-commits/pt.dap.git
cd pt.dap
```

#### 2. Backend Setup
```bash
cd backend
pnpm install
cp .env.example .env
# Edit .env dengan database URL
pnpm migrate
pnpm dev
# Backend: http://localhost:5000
```

#### 3. Frontend Setup
```bash
cd ../frontend
pnpm install
cp .env.example .env.local
pnpm dev
# Frontend: http://localhost:3000
```

#### 4. Akses Aplikasi
- **Homepage**: http://localhost:3000
- **Backend API**: http://localhost:5000/api
- **Health Check**: http://localhost:5000/api/health

---

## 📚 API Endpoints

### Authentication
```
POST   /api/auth/intranet/login      # Internal login
POST   /api/auth/b2b/register        # B2B registration
POST   /api/auth/b2b/login           # B2B login
GET    /api/auth/me                  # Get current user
```

### Products
```
GET    /api/products                 # List products (public)
GET    /api/products/:id             # Get product detail
POST   /api/products                 # Create product (B2B)
PUT    /api/products/:id             # Update product (B2B)
```

### Orders
```
GET    /api/orders                   # List orders
POST   /api/orders                   # Create order
GET    /api/orders/:id               # Get order detail
PUT    /api/orders/:id/status        # Update status
```

Lihat `docs/API.md` untuk dokumentasi lengkap.

---

## 🔐 Security Features

- ✅ JWT Authentication
- ✅ Password Hashing (bcrypt)
- ✅ CORS Protection
- ✅ Rate Limiting
- ✅ SQL Injection Prevention (Prisma ORM)
- ✅ HTTPS in Production
- ✅ Environment Variable Protection
- ✅ Role-based Access Control (RBAC)

---

## 🎨 UI/UX Guidelines

### Brand Colors
- **Primary**: #2D5016 (Hijau Gelap - Natural)
- **Secondary**: #F4A460 (Sandy Brown - Warm)
- **Accent**: #FFFFFF (White)
- **Background**: Alam Indonesia & produk pertanian

### Typography
- **Heading**: Inter Bold
- **Body**: Inter Regular
- **Code**: JetBrains Mono

---

## 📦 Database Schema

### Main Tables
- `users` - Karyawan & Partners
- `products` - Produk & stok
- `orders` - Pesanan B2B
- `categories` - Kategori produk
- `partners` - Data partner B2B
- `orderItems` - Detail order items

Lihat `prisma/schema.prisma` untuk schema lengkap.

---

## 🧪 Testing

```bash
# Backend testing
cd backend
pnpm test

# Frontend testing
cd ../frontend
pnpm test

# Coverage report
pnpm test:coverage
```

---

## 📦 Deployment

### Frontend (Vercel)
```bash
vercel deploy --prod
```

### Backend (Railway/Render)
```bash
git push production main
```

Lihat `docs/DEPLOYMENT.md` untuk guide lengkap.

---

## 🤝 Contributing

1. Buat branch feature: `git checkout -b feature/nama-fitur`
2. Commit changes: `git commit -m 'Add: deskripsi'`
3. Push: `git push origin feature/nama-fitur`
4. Buat Pull Request

---

## 📞 Contact & Support

**PT. Dinamis Agro Priangan**
- 📧 Email: pt.dinamis.agro.priangan@gmail.com
- 📱 Telepon: 082317226505, 081522807479
- 📍 Alamat: Jl. Raya Tanjung Mulya No. 361, Kecamatan Panumbangan, Kabupaten Ciamis

---

## 📄 License

Private Project - PT. Dinamis Agro Priangan © 2024

---

## ✨ Roadmap

- [ ] Phase 1: Homepage + Basic Authentication
- [ ] Phase 2: B2B Dashboard & Product Upload
- [ ] Phase 3: Order Management & Tracking
- [ ] Phase 4: Internal Management Dashboard
- [ ] Phase 5: Payment Integration
- [ ] Phase 6: Mobile App (React Native)
- [ ] Phase 7: Analytics & Reporting
- [ ] Phase 8: AI-based Product Recommendations

---

**Last Updated:** 2024
**Status:** 🚀 In Development
