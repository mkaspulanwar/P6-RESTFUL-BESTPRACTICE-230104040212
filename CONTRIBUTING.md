# Panduan Berkontribusi (CONTRIBUTING.md)

Terima kasih atas minat Anda untuk berkontribusi pada proyek **P6-RESTful-BestPractices-NimAnda** ini. Proyek ini adalah implementasi dari Praktikum Web Service Engineering yang berfokus pada penerapan 7 Prinsip RESTful API menggunakan Express.js.

Panduan ini menjelaskan proses dan standar yang kami gunakan untuk menerima kontribusi.

## Bagaimana Cara Saya Berkontribusi?

Ada beberapa cara Anda dapat berkontribusi pada proyek ini:

### 1. Pelaporan *Bug* (Error)
Jika Anda menemukan *bug*, error, atau masalah inkonsistensi (misalnya, *status code* tidak sesuai, *response* JSON tidak konsisten, atau *middleware* tidak berfungsi), silakan laporkan masalah tersebut:

* **Langkah:**
    1.  Buka tab **Issues** di repositori ini.
    2.  Klik tombol **New Issue**.
    3.  Berikan judul yang jelas (misalnya: "BUG: Endpoint POST /api/products mengembalikan 200 alih-alih 201").
    4.  Sertakan langkah-langkah untuk mereproduksi *bug* tersebut (termasuk *request body* dan *expected vs actual response*).

### 2. Proposal Fitur (Enhancement)
Jika Anda memiliki ide untuk peningkatan yang relevan dengan topik praktikum (misalnya, menambahkan *unit testing* dasar, implementasi *rate limiting*, atau *logging* yang lebih detail menggunakan `morgan`), Anda dapat mengajukan proposal:

* **Langkah:**
    1.  Buka tab **Issues**.
    2.  Ajukan proposal Anda dengan menjelaskan *mengapa* fitur tersebut relevan dan *bagaimana* itu akan diimplementasikan.

### 3. Kontribusi Kode (*Pull Request*)
Untuk kontribusi berupa perbaikan *bug*, perbaikan dokumentasi, atau implementasi fitur, ikuti alur kerja *Pull Request* (PR) di bawah ini.

## Panduan Kontribusi Kode (Pull Request)

1.  **Fork** Repositori: *Fork* repositori ini ke akun GitHub pribadi Anda.
2.  **Clone** Repositori: *Clone* repositori yang sudah Anda *fork* ke lingkungan lokal Anda.
    ```bash
    git clone [https://github.com/UsernameAnda/P6-RESTful-BestPractices-NimAnda.git](https://github.com/UsernameAnda/P6-RESTful-BestPractices-NimAnda.git)
    cd P6-RESTful-BestPractices-NimAnda
    ```
3.  **Buat Branch Baru:** Buat *branch* baru untuk perubahan Anda (misalnya: `fix/bug-post-status` atau `feat/add-rate-limit`).
    ```bash
    git checkout -b nama-branch-anda
    ```
4.  **Lakukan Perubahan:** Terapkan perubahan kode atau dokumentasi Anda.
    * Pastikan perubahan Anda mematuhi **Arsitektur Modular** proyek (`src/routes/`, `src/middlewares/`, dll.).
    * Pastikan semua **7 Prinsip RESTful** tetap terjaga atau ditingkatkan.
5.  **Commit Perubahan:** Lakukan *commit* dengan pesan yang jelas dan deskriptif.
    ```bash
    git add .
    git commit -m "feat: Menambahkan penanganan status 404 pada GET by ID"
    ```
6.  **Push Branch:** Dorong perubahan Anda ke repositori *fork* Anda.
    ```bash
    git push origin nama-branch-anda
    ```
7.  **Buat Pull Request (PR):** Buka repositori utama, dan buat **Pull Request** dari *branch* yang baru Anda dorong.

## Standar Kualitas

Kami akan meninjau kontribusi Anda berdasarkan rubrik praktikum:

* [cite_start]**Konsistensi RESTful:** Penggunaan HTTP Method, URI, dan Status Code harus sesuai standar[cite: 84].
* [cite_start]**Struktur Kode:** Kode harus rapi, terorganisir, dan mengikuti struktur modular proyek[cite: 84].
* [cite_start]**Response JSON:** Response harus konsisten dalam format ` { success, message, data }`[cite: 84].
* **Uji Coba:** Jika Anda menambahkan fitur baru, pastikan untuk mengujinya secara manual via Postman.

Kami akan meninjau PR Anda secepat mungkin. Terima kasih telah membantu meningkatkan proyek ini!
