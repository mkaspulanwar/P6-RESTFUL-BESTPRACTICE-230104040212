# P6-RESTFUL-BESTPRACTICE-230104040212: Implementasi RESTFUL API Best Practices (Express.js)

Praktikum ini bertujuan untuk mengimplementasikan **7 Prinsip RESTful API Best Practices** dalam sebuah Web Service sederhana menggunakan **Express.js** yang mencakup fungsionalitas CRUD lengkap, validasi input, dan penanganan error terstandar.

---

## Tim Developer

| Peran | Nama | Profil GitHub |
| :--- | :--- | :--- |
| **Pengembang Proyek** | M. Kaspul Anwar | [![](https://img.shields.io/badge/GitHub-M.KaspulAnwar-181717?style=flat&logo=github)](https://github.com/mkaspulanwar) |
| **Dosen Pengampu** | Muhayat, M. IT | [![](https://img.shields.io/badge/GitHub-Muhayat,M.IT-181717?style=flat&logo=github)](https://github.com/muhayat-lab) |

---

## Panduan Kontribusi

Kami sangat menghargai kontribusi dari komunitas. Untuk panduan lengkap tentang cara melaporkan *bug* dan mengajukan Pull Request, silakan merujuk ke dokumen **[CONTRIBUTING.md](CONTRIBUTING.md)**.

<p align="center">
  <a href="CONTRIBUTING.md">
    <img src="https://img.shields.io/badge/Kontribusi-Lihat%20Panduan-blue?style=for-the-badge&logo=github" alt="Kontribusi">
  </a>
</p>

---


### Detail Praktikum
| Aspek | Deskripsi |
| :--- | :--- |
| **Topik** | RESTful API Best Practices (Express) |
| **Aktivitas** | Menerapkan 7 prinsip RESTful pada API Express dengan membuat CRUD lengkap, validasi input, dan penanganan error. Setiap endpoint diuji via Postman untuk memastikan response JSON konsisten dan status code sesuai standar RESTful. |
| **Dosen Pengampu** | Muhayat, M.IT |
| **Durasi** | 1 pertemuan x 150 menit |

---

### Tujuan Praktikum
1. Memahami penerapan prinsip **RESTful** pada API Express.
2. Menggunakan **HTTP Method** dan **Status Code** secara tepat.
3. Mengimplementasikan **7 RESTful Principles** dalam desain endpoint.
4. Menangani **validasi input** dan **error** secara terstandar.
5. Menyiapkan **dokumentasi endpoint** yang mudah dibaca dan diuji.

---

### Lingkungan & Tools
* **Backend:** Node.js 18+ & npm, Express.js
* **Development:** VS Code / Postman / Thunder Client
* **Dependencies:** Nodemon (dev dependency), morgan (logging request)
* **Custom Middleware:** `validateProduct.js`, `errorHandler.js`
* **Versi Kontrol:** Git (opsional)

---

### Struktur Project
Struktur project dibuat modular dan rapi untuk memisahkan tanggung jawab (routes, data, middleware, utils).

```
P6-RESTFUL-BESTPRACTICE-230104040212/
├── node_modules/
├── src/
│   ├── controllers/
│   ├── data/
│   │   └── products.data.js
│   ├── evidence/
│   │   ├── 500 Internal Error.png
│   │   ├── DELETE id 1.png
│   │   ├── GET ALL.png
│   │   ├── GET by ID.png
│   │   ├── Health.png
│   │   ├── PATCH id 1.png
│   │   ├── POST new Product.png
│   │   ├── POST No Name.png
│   │   ├── POST No Price.png
│   │   ├── PUT id 1.png
│   │   └── PUT No Name.png
│   ├── middlewares/
│   │   ├── errorHandler.js
│   │   └── validateProduct.js
│   ├── routes/
│   │   └── products.routes.js
│   ├── utils/
│   │   └── apiResponse.js
│   └── app.js
├── LICENSE
├── package-lock.json
├── package.json
└── README.md
```

---
### Desain Endpoint (RESTful Best Practices)
Semua endpoint beroperasi di bawah *base path* `/api/`.

| No | Endpoint | Method | Deskripsi | Status Code | Body Contoh |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | `/api/products` | GET | Ambil semua produk | `200` | - |
| 2 | `/api/products/:id` | GET | Ambil 1 produk berdasarkan ID | `200 / 404` | - |
| 3 | `/api/products` | POST | Tambah produk baru | `201 / 400` | `{"name": "Keyboard", "price": 250000}` |
| 4 | `/api/products/:id` | PUT | Update penuh data produk | `200 / 400 / 404` | `{"name": "Laptop X", "price": 12000000}` |
| 5 | `/api/products/:id` | PATCH | Update sebagian data produk | `200 / 404` | `{"price": 9900000}` |
| 6 | `/api/products/:id` | DELETE | Hapus produk | `200 / 404` | - |
| 7 | `/api/health` | GET | Cek status API | `200` | - |

---

### Implementasi 7 Prinsip RESTful

Berikut adalah penerapan 7 Prinsip RESTful dalam praktikum ini:

1.  **Resource-Oriented URI:** Menggunakan **kata benda jamak** sebagai *resource*, seperti `/products`, bukan menggunakan kata kerja atau URI yang tidak jelas.
2.  **Proper HTTP Methods:** Menggunakan **GET** (baca), **POST** (buat), **PUT/PATCH** (ubah), dan **DELETE** (hapus) sesuai maknanya untuk operasi CRUD.
3.  **Stateless Communication:** Server **tidak menyimpan *state* sesi** antar-request, semua data yang dibutuhkan dikirim lengkap di tiap request.
4.  **Consistent HTTP Status Codes:** Menggunakan kode status yang benar: **200/201** (sukses), **400** (salah request/validasi), **404** (data tidak ditemukan), **500** (error server).
5.  **Content Negotiation & Representations (JSON):** Response default menggunakan format **JSON** (`application/json`) yang konsisten, terstruktur (`{ success, message, data }`), dan rapi.
6.  **Validation & Error Handling:** Menerapkan **middleware validasi** (`validateProduct.js`) pada POST dan PUT untuk menolak request tanpa field wajib (`name`, `price`) dengan status **400 Bad Request**. Serta menerapkan **middleware error global** (`errorHandler.js`) untuk menangkap error 500 tanpa *crash*.
7.  **Discoverability / Documentation-Friendly:** Endpoint mudah ditebak dan dilengkapi dengan **dokumentasi** (tabel ini) serta *health check* endpoint (`/api/health`).
