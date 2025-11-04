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
P5-CRUD-REST-230104040212
├── evidence
│ ├── delete.png
│ ├── get-all.png
│ ├── get-by-id.png
│ ├── post.png
│ └── put.png
├── node_modules
├── LICENSE
├── package-lock.json
├── package.json
├── README.md
└── server.js
```

---
