 SinarDigital BE Mini Project 3

 📌 Deskripsi Proyek

Project ini merupakan Mini Project 3 Back End dari BNCC (Bina Nusantara Computer Club). Aplikasi ini berupa RESTful API yang dibangun menggunakan Node.js, Express, dan Prisma ORM, serta menerapkan JWT Authentication, CRUD API, dan middleware keamanan.

Tema aplikasi bersifat bebas, dengan fokus utama pada implementasi autentikasi pengguna dan operasi CRUD yang aman dan terstruktur.

---

 🛠️ Tech Stack

 Node.js
 Express.js
 Prisma ORM
 PostgreSQL
 JWT (JSON Web Token)
 bcrypt (password hashing)
 Multer (upload image)

---

 📂 Struktur Folder

```
TPM_BE_MiniProject3_BrianAntonia_BE1/
├── prisma/
│   ├── schema.prisma
│   └── migrations/
├── src/
│   ├── controllers/
│   │   ├── auth/
│   │   └── api/
│   ├── routes/
│   │   ├── auth/
│   │   └── api/
│   ├── middlewares/
│   ├── utils/
│   └── config/
├── uploads/
├── app.js
├── .env.example
├── .gitignore
└── package.json
```

---

 ⚙️ Instalasi & Setup

 1️⃣ Clone Repository

```bash
git clone https://github.com/brianantonia/SinarDigital_BE_MiniProject3_BrianAntonia_BE1.git
cd SinarDigital_BE_MiniProject3_BrianAntonia_BE1
```

 2️⃣ Install Dependencies

```bash
npm install
```

 3️⃣ Setup Environment Variable

Buat file `.env` di root project, lalu isi:

```
DATABASE_URL="postgresql://username:password@localhost:5432/db_name"
JWT_SECRET=your_secret_key
```

 4️⃣ Prisma Migration

```bash
npx prisma migrate dev --name init
```

 5️⃣ Jalankan Server

```bash
npm run dev
```

Server akan berjalan di:

```
http://localhost:3000
```

---

 🔐 Authentication API

 Register

```
POST /api/auth/register
```

Body:

```json
{
  "email": "user@email.com",
  "password": "password123"
}
```

 Login

```
POST /api/auth/login
```

Response:

```json
{
  "token": "JWT_TOKEN"
}
```

Gunakan token ini sebagai Bearer Token untuk mengakses protected routes.

---

 📦 Product API (Protected)

> Semua endpoint di bawah memerlukan Authorization Bearer Token

 Create Product

```
POST /api/products
```

Body (form-data):

 `name`
 `price`
 `image` (optional)

 Get All Products

```
GET /api/products
```

 Get Product by ID

```
GET /api/products/:id
```

 Update Product

```
PUT /api/products/:id
```

 Delete Product

```
DELETE /api/products/:id
```

---

 🧪 Testing

Testing API dilakukan menggunakan:

 Postman
 Thunder Client

Pengujian meliputi:

 Register & Login
 Protected Routes
 CRUD Operations

---

 ✅ Fitur yang Diimplementasikan

 JWT Authentication (Register, Login, Logout)
 RESTful CRUD API
 Protected Routes
 Upload Image
 Prisma ORM + Relational Database
 Middleware Authorization & Validation

---

 👤 Author

Brian Antonia
BNCC TPM BE1

---

 📎 Catatan

Project ini dibuat untuk keperluan pembelajaran dan penilaian Mini Project BNCC.
