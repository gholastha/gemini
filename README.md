# Proyek E-commerce Siagian Agro Mandiri

[![Status Proyek](https://img.shields.io/badge/status-development-yellow)](link-ke-repo-anda) <!-- Ganti link-ke-repo-anda -->
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

Platform digitalisasi agribisnis dan e-commerce untuk Siagian Agro Mandiri, menggabungkan penjualan ritel dengan edukasi dan manajemen modern.

## Daftar Isi

1.  [Deskripsi Singkat](#deskripsi-singkat)
2.  [Fitur Utama (Target)](#fitur-utama-target)
3.  [Tumpukan Teknologi (Tech Stack)](#tumpukan-teknologi-tech-stack)
4.  [Rencana Iterasi Pengembangan](#rencana-iterasi-pengembangan)
    *   [Iterasi 0: Fondasi & Pengaturan Awal](#iterasi-0-fondasi--pengaturan-awal)
    *   [Iterasi 1: Katalog Produk & Kategori (Read-Only)](#iterasi-1-katalog-produk--kategori-read-only)
    *   [Iterasi 2: Autentikasi Pengguna (JWT) & Peran Dasar](#iterasi-2-autentikasi-pengguna-jwt--peran-dasar)
    *   [Iterasi 3: Fungsionalitas Keranjang Belanja](#iterasi-3-fungsionalitas-keranjang-belanja)
    *   [Iterasi 4: Alur Checkout Dasar & Pengumpulan Alamat](#iterasi-4-alur-checkout-dasar--pengumpulan-alamat)
    *   [Iterasi 5: Pembuatan Pesanan & Riwayat Pesanan Dasar](#iterasi-5-pembuatan-pesanan--riwayat-pesanan-dasar)
    *   [Iterasi 6: Pencarian & Penyaringan Produk Lanjutan](#iterasi-6-pencarian--penyaringan-produk-lanjutan)
    *   [Iterasi 7: Panel Admin - Manajemen Produk & Kategori (CRUD)](#iterasi-7-panel-admin---manajemen-produk--kategori-crud)
    *   [Iterasi 8: Panel Admin - Manajemen Pengguna & Profil Pengguna](#iterasi-8-panel-admin---manajemen-pengguna--profil-pengguna)
    *   [Iterasi 9: Modul Edukasi/Literasi (CRUD Konten)](#iterasi-9-modul-edukasi-literasi-crud-konten)
    *   [Iterasi 10: Interaksi Pengguna (Review Produk & Wishlist)](#iterasi-10-interaksi-pengguna-review-produk--wishlist)
    *   [Iterasi 11: Integrasi Gateway Pembayaran (Midtrans)](#iterasi-11-integrasi-gateway-pembayaran-midtrans)
    *   [Iterasi 12: Optimasi, Keamanan, & Deployment (Vercel, GCR, Supabase)](#iterasi-12-optimasi-keamanan--deployment-vercel-gcr-supabase)
    *   [Iterasi Berikutnya (Rencana Jangka Panjang)](#iterasi-berikutnya-rencana-jangka-panjang)
5.  [Prasyarat](#prasyarat)
6.  [Instalasi & Menjalankan Proyek Lokal](#instalasi--menjalankan-proyek-lokal)
7.  [Struktur Proyek](#struktur-proyek)
8.  [Kontribusi](#kontribusi)
9.  [Lisensi](#lisensi)

---

## Deskripsi Singkat

Proyek E-Commerce ini adalah implementasi agroteknologi dan digitalisasi sistem manajemen perusahaan ritel Siagian Agro Mandiri dalam e-commerce dan agribisnis.

**Visi:** Meningkatkan kinerja perusahaan dalam hal, penjualan/promosi produk, pelayanan konsumen, edukasi/literasi SDM, serta pencatatan/pelaporan.

**Misi:** Membangun aplikasi fleksibel yang kaya akan fitur, modern, stabil, skalabel dan aman serta penggunaan lintas platform/perangkat.

**Pengguna:** Masyarakat (Konsumen), Petani, Pengusaha Agribisnis, Karyawan Internal, dan Para Stakeholder.

---

## Fitur Utama (Target)

*   Penjelajahan produk berdasarkan kategori agrikultur (Benih, Pupuk, Pestisida, Alat, dll.).
*   Pencarian produk cerdas (nama, fungsi, hama target).
*   Filter produk berdasarkan atribut spesifik (jenis tanaman, komposisi, dll.).
*   Tampilan detail produk informatif (deskripsi, gambar, info teknis, cara pakai).
*   Registrasi dan login pengguna aman (JWT) dengan peran berbeda (Customer, Admin, dll.).
*   Manajemen profil pengguna.
*   Keranjang belanja persisten (untuk user login) & non-persisten (untuk tamu).
*   Proses checkout yang jelas dengan input alamat pengiriman.
*   Integrasi gateway pembayaran terpercaya (Midtrans).
*   Riwayat pesanan dan status pelacakan dasar untuk pengguna.
*   Modul Edukasi/Literasi: Artikel, panduan, tips agrikultur.
*   Sistem review dan rating produk oleh pengguna.
*   Fitur Wishlist produk.
*   Panel admin komprehensif: Manajemen produk, kategori, pesanan, pengguna, konten edukasi.
*   (Mendatang) Fitur pencatatan/pelaporan internal & stakeholder.
*   Desain responsif dan modern menggunakan Tailwind CSS.

---

## Tumpukan Teknologi (Tech Stack)

*   **Frontend:** React (Vite), Zustand (State Management), React Router (Routing), Tailwind CSS (Styling), Axios (HTTP Client)
*   **Backend:** Node.js, Express.js
*   **Database:** PostgreSQL (Managed via **Supabase**)
*   **ORM:** **Prisma**
*   **Autentikasi:** JWT (JSON Web Tokens) + bcrypt (Password Hashing)
*   **Validasi Skema:** **Zod** (Backend & Frontend)
*   **File Upload:** Multer (Manajemen Gambar)
*   **Real-time (Opsional):** Socket.io (Untuk Notifikasi Masa Depan)
*   **Deployment:**
    *   Frontend: **Vercel**
    *   Backend: **Google Cloud Run** (via Docker Container)
    *   Database: **Supabase**
*   **Lainnya:** `dotenv`, ESLint, Prettier, Docker

---

## Rencana Iterasi Pengembangan

Status: `[ ] To Do`, `[⏳] In Progress`, `[✅] Done`.

### Iterasi 0: Fondasi & Pengaturan Awal `[✅]` *(Asumsi selesai)*

*   **Tujuan:** Menyiapkan lingkungan & struktur proyek dasar.
*   **Tasks:**
    *   `[✅]` Inisialisasi proyek React (Vite) + **Tailwind CSS**.
    *   `[✅]` Inisialisasi proyek backend Node.js/Express.
    *   `[✅]` Pengaturan repositori Git & GitHub.
    *   `[✅]` Struktur folder standar (frontend & backend).
    *   `[✅]` Pengaturan ESLint & Prettier.
    *   `[✅]` Pengaturan `dotenv` untuk variabel lingkungan.
    *   `[✅]` Setup **Prisma**: `schema.prisma` awal (User minimal), koneksi ke DB **Supabase**, generate Prisma Client.
    *   `[✅]` Setup **Zustand**: store dasar (misal: UI state).
    *   `[✅]` Setup **React Router**: routing dasar & layout utama.
    *   `[✅]` Konfigurasi instance **Axios** dasar.
    *   `[✅]` Setup **Docker** dasar untuk backend.

### Iterasi 1: Katalog Produk & Kategori (Read-Only) `[Status]`

*   **Tujuan:** Menampilkan produk agrikultur kepada publik.
*   **Tasks:**
    *   `[ ]` Update `schema.prisma`: Tambah model `Product` (nama, deskripsi, harga, stok, gambarUrl, atribut teknis) & `Category`. Definisikan relasi.
    *   `[ ]` Jalankan `npx prisma migrate dev` untuk menerapkan perubahan schema.
    *   `[ ]` Buat script *seeding* (`prisma/seed.ts`) untuk data produk & kategori awal. Jalankan `npx prisma db seed`.
    *   `[ ]` Buat endpoint API backend (Express + **Prisma Client**) :
        *   `GET /api/products` (termasuk info kategori, paginasi dasar)
        *   `GET /api/products/:slugOrId` (detail produk)
        *   `GET /api/categories`
    *   `[ ]` Buat komponen UI React (**Tailwind CSS**): `ProductCard`, `CategoryList`, `ProductGrid/List`.
    *   `[ ]` Buat halaman `HomePage` (menampilkan beberapa produk/kategori unggulan).
    *   `[ ]` Buat halaman `ProductsPage` (menampilkan semua produk dengan paginasi, mengambil data via **Axios**).
    *   `[ ]` Buat halaman `ProductDetailPage` (menampilkan detail lengkap).
    *   `[ ]` Implementasi navigasi berdasarkan kategori.

### Iterasi 2: Autentikasi Pengguna (JWT) & Peran Dasar `[Status]`

*   **Tujuan:** Memungkinkan pengguna mendaftar & masuk, membedakan Customer dan Admin.
*   **Tasks:**
    *   `[ ]` Update `schema.prisma` model `User`: Tambah field `role` (enum: `CUSTOMER`, `ADMIN`), `passwordHash`. Migrasi DB.
    *   `[ ]` Implementasi hashing password dengan **bcrypt** di backend.
    *   `[ ]` Buat **Zod** schema untuk validasi input registrasi & login.
    *   `[ ]` Buat endpoint API backend (Express + **Prisma Client**):
        *   `POST /api/auth/register` (Validasi **Zod**, hash password, create user, issue **JWT**).
        *   `POST /api/auth/login` (Validasi **Zod**, verifikasi user & password, issue **JWT**).
    *   `[ ]` Buat middleware backend `authenticateToken` (verifikasi **JWT**) & `authorizeAdmin` (cek `req.user.role === 'ADMIN'`).
    *   `[ ]` Buat store **Zustand** (`authStore`) untuk menyimpan token JWT, data user, status login. Implementasi persistensi (misal: ke LocalStorage).
    *   `[ ]` Buat halaman & komponen UI React (**Tailwind CSS**) untuk form Registrasi & Login. Hubungkan ke API via **Axios**. Tangani state loading & error.
    *   `[ ]` Implementasi *Protected Routes* di **React Router** (misal: untuk halaman profil, admin).
    *   `[ ]` Implementasi fungsi Logout (hapus token dari state/storage, reset `authStore`).
    *   `[ ]` Update UI (misal: Header) untuk menampilkan status login/logout & nama user.

### Iterasi 3: Fungsionalitas Keranjang Belanja `[Status]`

*   **Tujuan:** Mengelola item yang ingin dibeli pengguna (login & tamu).
*   **Tasks:**
    *   `[ ]` Buat store **Zustand** (`cartStore`) untuk mengelola item keranjang di frontend. Implementasi persistensi (LocalStorage) untuk tamu & sinkronisasi untuk user login.
    *   `[ ]` (Untuk User Login) Update `schema.prisma`: Tambah model `Cart` & `CartItem`. Definisikan relasi dengan `User` & `Product`. Migrasi DB (`npx prisma migrate dev`).
    *   `[ ]` (Untuk User Login) Buat endpoint API backend (terproteksi `authenticateToken`, gunakan **Prisma Client**) untuk:
        *   `GET /api/cart` (ambil keranjang user)
        *   `POST /api/cart` (tambah/update item, validasi input dengan **Zod**)
        *   `PUT /api/cart/items/:itemId` (update kuantitas, validasi **Zod**)
        *   `DELETE /api/cart/items/:itemId` (hapus item)
        *   Implementasikan logika sinkronisasi saat user login (ambil cart dari DB, gabungkan dengan cart tamu jika ada, update DB).
    *   `[ ]` Tambahkan tombol "Tambah ke Keranjang" di `ProductCard` & `ProductDetailPage`.
    *   `[ ]` Implementasi logika di `cartStore` (Zustand): tambah item, update kuantitas (cek stok dasar), hapus item. Panggil API backend jika user login.
    *   `[ ]` Buat halaman/komponen UI Keranjang Belanja (`CartPage`, `CartItem`) dengan **Tailwind CSS**.
    *   `[ ]` Tampilkan item di keranjang (gambar, nama, harga, kuantitas, subtotal).
    *   `[ ]` Tampilkan total harga keseluruhan keranjang.
    *   `[ ]` Buat komponen indikator keranjang (misal: ikon dengan jumlah item) di header, update secara reaktif menggunakan `cartStore`.

### Iterasi 4: Alur Checkout Dasar & Pengumpulan Alamat `[Status]`

*   **Tujuan:** Memandu pengguna dari keranjang ke tahap pengumpulan info pengiriman.
*   **Tasks:**
    *   `[ ]` Buat halaman Checkout (`CheckoutPage`) - bisa multi-langkah (step 1: Alamat) atau satu halaman. Gunakan **React Router**.
    *   `[ ]` Buat komponen Form Alamat Pengiriman dengan **Tailwind CSS**.
    *   `[ ]` Buat **Zod** schema untuk validasi alamat pengiriman (nama penerima, no. telp, alamat lengkap, kota, provinsi, kode pos).
    *   `[ ]` Implementasi state management (bisa di `cartStore` Zustand atau store baru `checkoutStore`) untuk menyimpan data alamat sementara.
    *   `[ ]` Jika user login, coba isi otomatis form alamat dari profil pengguna (jika sudah ada).
    *   `[ ]` Tampilkan ringkasan item dari `cartStore`.
    *   `[ ]` Tampilkan kalkulasi subtotal, ongkir (placeholder/statis dulu), total.
    *   `[ ]` Validasi input form alamat menggunakan **Zod** di frontend.
    *   `[ ]` Tombol "Lanjut ke Pembayaran" (belum fungsional, hanya menyimpan alamat ke state).
    *   `[ ]` Proteksi halaman Checkout (memerlukan item di keranjang).

### Iterasi 5: Pembuatan Pesanan & Riwayat Pesanan Dasar `[Status]`

*   **Tujuan:** Menyimpan pesanan ke database saat checkout (tanpa pembayaran nyata) & menampilkan riwayat.
*   **Tasks:**
    *   `[ ]` Update `schema.prisma`: Tambah model `Order` (userId, alamatPengiriman [JSON atau relasi ke model Address], totalHarga, status [enum: `PENDING`, `PROCESSING`, `SHIPPED`, `DELIVERED`, `CANCELLED`]) & `OrderItem` (orderId, productId, kuantitas, hargaSaatBeli). Migrasi DB.
    *   `[ ]` Buat **Zod** schema untuk payload pembuatan pesanan di backend.
    *   `[ ]` Buat endpoint API backend `POST /api/orders` (terproteksi `authenticateToken`, gunakan **Prisma Client**):
        *   Validasi input (alamat, item keranjang) dengan **Zod**.
        *   Buat record `Order` dan `OrderItem` dalam satu transaksi database (**Prisma Transaction API**).
        *   Set status awal ke `PENDING`.
        *   Kosongkan `Cart` pengguna di database (atau tandai sebagai sudah di-checkout).
        *   *Opsional:* Kurangi stok produk (perlu penanganan race condition jika traffic tinggi).
    *   `[ ]` Hubungkan tombol "Buat Pesanan" (atau nama serupa) di akhir alur Checkout ke API ini. Handle state loading/error.
    *   `[ ]` Kosongkan `cartStore` (Zustand) di frontend setelah pesanan berhasil dibuat.
    *   `[ ]` Redirect pengguna ke halaman konfirmasi pesanan (`OrderSuccessPage`) yang menampilkan ringkasan pesanan (Order ID).
    *   `[ ]` Buat endpoint API backend `GET /api/orders/myorders` (terproteksi `authenticateToken`, **Prisma Client**) untuk mengambil daftar pesanan milik user yang login.
    *   `[ ]` Buat endpoint API backend `GET /api/orders/:orderId` (terproteksi, cek kepemilikan user).
    *   `[ ]` Buat halaman "Riwayat Pesanan" (`OrderHistoryPage`) & "Detail Pesanan" (`OrderDetailPage`) di frontend (React + **Tailwind CSS**).
    *   `[ ]` Tampilkan daftar pesanan (ID, tanggal, total, status) & detailnya.

### Iterasi 6: Pencarian & Penyaringan Produk Lanjutan `[Status]`

*   **Tujuan:** Meningkatkan kemampuan pengguna menemukan produk agrikultur yang relevan.
*   **Tasks:**
    *   `[ ]` Tambahkan komponen UI `SearchInput` & `FilterSidebar/Dropdown` (**Tailwind CSS**).
    *   `[ ]` Update endpoint API `GET /api/products` (Express + **Prisma Client**) untuk menerima query parameters: `keyword`, `categoryId`, `minPrice`, `maxPrice`, `sortBy`, `page`, `limit`.
    *   `[ ]` Implementasi logika pencarian di backend menggunakan fitur pencarian **Prisma** (misal: `contains`, `mode: 'insensitive'`) pada field relevan (nama, deskripsi, atribut).
    *   `[ ]` Implementasi logika filter berdasarkan kategori, rentang harga, dll., menggunakan klausa `where` **Prisma**.
    *   `[ ]` Implementasi logika sorting menggunakan klausa `orderBy` **Prisma**.
    *   `[ ]` Implementasi paginasi menggunakan `skip` dan `take` **Prisma**. Kembalikan juga total count untuk UI paginasi.
    *   `[ ]` Kelola state pencarian & filter di frontend (bisa di `ProductsPage` atau store **Zustand** terpisah). Gunakan `useEffect` untuk memanggil API saat state berubah.
    *   `[ ]` Update UI `ProductsPage` untuk menampilkan input pencarian, opsi filter/sorting, dan komponen paginasi.

### Iterasi 7: Panel Admin - Manajemen Produk & Kategori (CRUD) `[Status]`

*   **Tujuan:** Memberikan antarmuka Admin untuk mengelola katalog produk.
*   **Tasks:**
    *   `[ ]` Buat layout & routing khusus Admin (`/admin/*`) menggunakan **React Router** & **Tailwind CSS**.
    *   `[ ]` Terapkan middleware `authenticateToken` & `authorizeAdmin` pada semua endpoint API admin.
    *   `[ ]` Terapkan proteksi rute Admin di frontend (cek `user.role` dari `authStore`).
    *   `[ ]` **Manajemen Produk (CRUD):**
        *   `[ ]` Endpoint API Admin (Express + **Prisma Client**) untuk: `GET /api/admin/products`, `GET /api/admin/products/:id`, `POST /api/admin/products`, `PUT /api/admin/products/:id`, `DELETE /api/admin/products/:id`. Gunakan **Zod** untuk validasi input `POST` & `PUT`.
        *   `[ ]` UI Admin (`AdminProductListPage`, `AdminProductEditPage`): Tabel produk (dengan search & paginasi), Form tambah/edit produk (termasuk upload gambar). Gunakan library form (misal: React Hook Form) + **Zod** resolver untuk validasi frontend.
        *   `[ ]` Integrasi **Multer** di backend untuk menangani upload gambar produk. Simpan gambar (sementara lokal, target Cloud Storage) & simpan URL/path di `Product.gambarUrl`.
    *   `[ ]` **Manajemen Kategori (CRUD):**
        *   `[ ]` Endpoint API Admin untuk CRUD Kategori (mirip produk). Gunakan **Zod** untuk validasi.
        *   `[ ]` UI Admin (`AdminCategoryListPage`, `AdminCategoryEditPage`): Daftar kategori, Form tambah/edit kategori.

### Iterasi 8: Panel Admin - Manajemen Pengguna & Profil Pengguna `[Status]`

*   **Tujuan:** Mengelola data pengguna oleh Admin dan oleh pengguna sendiri.
*   **Tasks:**
    *   `[ ]` **Admin - Manajemen Pengguna:**
        *   `[ ]` Endpoint API Admin (terproteksi `authorizeAdmin`) untuk: `GET /api/admin/users`, `GET /api/admin/users/:id`, `PUT /api/admin/users/:id` (update peran, status aktif/nonaktif), `DELETE /api/admin/users/:id`. Gunakan **Zod** untuk validasi `PUT`.
        *   `[ ]` UI Admin (`AdminUserListPage`, `AdminUserEditPage`): Tabel daftar pengguna (search, filter by role), detail pengguna, opsi edit peran/status.
    *   `[ ]` **Pengguna - Manajemen Profil:**
        *   `[ ]` Endpoint API `GET /api/users/profile` & `PUT /api/users/profile` (terproteksi `authenticateToken`). Gunakan **Zod** untuk validasi `PUT`.
        *   `[ ]` Halaman Profil Pengguna (`ProfilePage`) di frontend (React + **Tailwind CSS**).
        *   `[ ]` Form untuk mengedit detail profil (nama, kontak - *tidak termasuk email/password untuk tahap ini*). Validasi **Zod** frontend.
        *   `[ ]` *Opsional:* Buat endpoint & UI terpisah untuk fitur ganti password (memerlukan password lama & baru).

### Iterasi 9: Modul Edukasi/Literasi (CRUD Konten) `[Status]`

*   **Tujuan:** Menyediakan & mengelola konten edukatif agrikultur.
*   **Tasks:**
    *   `[ ]` Update `schema.prisma`: Tambah model `Article` (judul, slug, konten [String panjang atau JSON], penulisId [relasi ke User], kategoriKonten, statusPublikasi [enum: `DRAFT`, `PUBLISHED`], gambarUtamaUrl). Migrasi DB.
    *   `[ ]` **Admin - Manajemen Konten:**
        *   `[ ]` Endpoint API Admin (terproteksi `authorizeAdmin`) untuk CRUD `Article`. Gunakan **Zod** untuk validasi.
        *   `[ ]` UI Admin (`AdminArticleListPage`, `AdminArticleEditPage`): Daftar artikel, Form tambah/edit artikel dengan Rich Text Editor (misal: React Quill, Tiptap) atau Markdown Editor.
        *   `[ ]` Integrasi **Multer** untuk upload gambar artikel.
    *   `[ ]` **Frontend - Tampilan Konten:**
        *   `[ ]` Endpoint API publik `GET /api/articles?status=PUBLISHED` (daftar artikel terpublikasi, paginasi) & `GET /api/articles/:slug`.
        *   `[ ]` Buat halaman daftar artikel/panduan (`ArticlesPage`) & detail artikel (`ArticleDetailPage`) (React + **Tailwind CSS**). Tampilkan konten yang sudah diformat.

### Iterasi 10: Interaksi Pengguna (Review Produk & Wishlist) `[Status]`

*   **Tujuan:** Meningkatkan engagement melalui review dan wishlist.
*   **Tasks:**
    *   `[ ]` **Review Produk:**
        *   `[ ]` Update `schema.prisma`: Tambah model `Review` (userId, productId, rating [Int 1-5], komentar, createdAt). Tambahkan relasi one-to-many dari Product dan User. Migrasi DB.
        *   `[ ]` Endpoint API (terproteksi `authenticateToken`) `POST /api/products/:productId/reviews`. Gunakan **Zod** untuk validasi. Pertimbangkan aturan: hanya user yang pernah beli produk ini? (Cek data `Order`).
        *   `[ ]` Endpoint API publik `GET /api/products/:productId/reviews` (paginasi).
        *   `[ ]` Update endpoint `GET /api/products/:id` & `GET /api/products` untuk menyertakan rating rata-rata & jumlah review (gunakan fitur agregasi **Prisma**).
        *   `[ ]` Tampilkan rating (bintang) di `ProductCard` & `ProductDetailPage`.
        *   `[ ]` Tampilkan daftar review di `ProductDetailPage`.
        *   `[ ]` Tambahkan Form UI (**Tailwind CSS**) untuk submit review di `ProductDetailPage` atau halaman riwayat pesanan.
    *   `[ ]` **Wishlist:**
        *   `[ ]` Update `schema.prisma`: Tambah model `WishlistItem` atau relasi many-to-many antara `User` dan `Product` untuk wishlist. Migrasi DB.
        *   `[ ]` Endpoint API (terproteksi `authenticateToken`, **Prisma Client**) `POST /api/wishlist/:productId` (toggle add/remove) & `GET /api/wishlist` (get user's wishlist).
        *   `[ ]` Tambahkan tombol "Tambah/Hapus dari Wishlist" (ikon hati) di `ProductCard` & `ProductDetailPage`. Kelola state-nya di frontend.
        *   `[ ]` Buat halaman Wishlist Pengguna (`WishlistPage`).

### Iterasi 11: Integrasi Gateway Pembayaran (Midtrans) `[Status]`

*   **Tujuan:** Memungkinkan pembayaran online yang sesungguhnya.
*   **Tasks:**
    *   `[ ]` Daftar akun Midtrans (Sandbox dulu). Dapatkan Server Key & Client Key. Simpan di `.env` backend & frontend.
    *   `[ ]` Install SDK Midtrans di backend (`npm install midtrans-client`).
    *   `[ ]` Update endpoint `POST /api/orders`: Jangan langsung set status `PENDING`. Alih-alih, buat transaksi Midtrans (misal: menggunakan Snap API) setelah order dibuat di DB (dengan status `PAYMENT_INITIATED` atau sejenisnya). Kembalikan `snapToken` ke frontend.
    *   `[ ]` Di frontend (`CheckoutPage`), setelah mendapatkan `snapToken` dari API, gunakan library Midtrans Snap (`snap.js`) untuk membuka popup/redirect pembayaran. (`window.snap.pay(snapToken, { onSuccess, onPending, onError, onClose })`).
    *   `[ ]` Buat endpoint API backend (webhook) `POST /api/payments/midtrans-notification` untuk menerima notifikasi status transaksi dari Midtrans.
    *   `[ ]` Implementasi logika di webhook handler:
        *   Verifikasi signature notifikasi Midtrans.
        *   Ambil `order_id` dari notifikasi.
        *   Update status `Order` di database (**Prisma Client**) sesuai status transaksi Midtrans (misal: `settlement` -> `PROCESSING`, `pending` -> `PENDING`, `expire` -> `CANCELLED`).
        *   Kirim respons yang benar ke Midtrans.
    *   `[ ]` Sesuaikan alur `OrderSuccessPage` atau tambahkan halaman `OrderPendingPage`. Update tampilan status di `OrderHistoryPage`.
    *   `[ ]` Konfigurasi URL Notifikasi di dashboard Midtrans agar mengarah ke endpoint webhook Anda (perlu URL publik saat testing/deployment).

### Iterasi 12: Optimasi, Keamanan, & Deployment (Vercel, GCR, Supabase) `[Status]`

*   **Tujuan:** Mempersiapkan dan meluncurkan aplikasi ke production.
*   **Tasks:**
    *   `[ ]` **Optimasi Frontend:**
        *   Code Splitting (Lazy loading) per rute/komponen besar menggunakan `React.lazy` & `Suspense`.
        *   Analisa ukuran bundle (misal: `vite-plugin-visualizer`) & optimasi import.
        *   Optimasi gambar (kompresi, format WebP, lazy loading native/library).
        *   Memoization (`React.memo`, `useMemo`, `useCallback`) jika diperlukan.
    *   `[ ]` **Optimasi Backend & Database:**
        *   Tambahkan index pada kolom database yang sering di-query/filter/sort di `schema.prisma`.
        *   Analisa query lambat (jika ada).
        *   Implementasi caching sederhana jika diperlukan (misal: Redis untuk data yang jarang berubah).
    *   `[ ]` **Keamanan:**
        *   Review & perketat aturan CORS di backend (Express `cors` middleware).
        *   Gunakan Helmet.js di Express untuk header keamanan HTTP.
        *   Pastikan validasi input (**Zod**) diterapkan di semua endpoint yang menerima data.
        *   Proteksi terhadap brute force login (misal: rate limiting).
        *   Review penanganan file upload (**Multer**) untuk keamanan.
        *   Gunakan variabel lingkungan untuk semua kredensial & secret.
        *   Implementasi HTTPS (otomatis di Vercel & Cloud Run biasanya).
    *   `[ ]` **Deployment:**
        *   Finalisasi `Dockerfile` untuk aplikasi backend Express.
        *   Build & push image Docker ke Google Container Registry (GCR) atau Artifact Registry.
        *   Deploy backend ke **Google Cloud Run**, konfigurasi environment variables, scaling, URL.
        *   Deploy frontend ke **Vercel**, hubungkan ke repo GitHub, konfigurasi environment variables (misal: URL API backend GCR).
        *   Konfigurasi **Supabase** untuk production (backup, monitoring).
    *   `[ ]` **Testing & Finalisasi:**
        *   Testing end-to-end manual di lingkungan staging/production.
        *   Setup CI/CD (GitHub Actions) untuk otomatisasi build & deploy frontend (Vercel) dan backend (GCR).
        *   Monitoring & Logging dasar.

### Iterasi Berikutnya (Rencana Jangka Panjang)

*   `[ ]` **Fitur Pelaporan & Analitik:** Dashboard Admin (penjualan, user, produk), ekspor laporan.
*   `[ ]` **Manajemen Inventaris Lanjutan:** Notifikasi stok, batch/kadaluarsa (jika relevan).
*   `[ ]` **Integrasi Ongkos Kirim Dinamis:** API RajaOngkir atau sejenisnya.
*   `[ ]` **Notifikasi (Email/Real-time):** Pendaftaran, pesanan, pengiriman, update stok (pakai **Socket.io** atau layanan email).
*   `[ ]` **Fitur Komunitas/Forum.**
*   `[ ]] `**Kupon Diskon & Promosi.**
*   `[ ]` **Pengujian Otomatis (Testing):** Unit (Jest), Integration, End-to-End (Cypress/Playwright).
*   `[ ]` **PWA (Progressive Web App).**
*   `[ ]` **Fitur Spesifik Karyawan/Stakeholder.**
*   `[ ]` **SEO Lanjutan.**

### Iterasi Berikutnya (Future Enhancements)

*   `[ ]` **Pencatatan/Pelaporan Lanjutan:** Dashboard analitik admin (penjualan, produk populer, user), laporan untuk stakeholder.
*   `[ ]` **Manajemen Inventaris Lanjutan:** Pelacakan stok detail, notifikasi stok rendah.
*   `[ ]` **Integrasi Ongkos Kirim:** API pihak ketiga (RajaOngkir, dll.).
*   `[ ]` **Notifikasi Real-time/Email:** Menggunakan **Socket.io** atau layanan email (SendGrid, Mailgun) untuk notifikasi pesanan, update stok, dll.
*   `[ ]` **Fitur Komunitas Petani/Pengusaha:** Forum diskusi, tanya jawab.
*   `[ ]` **Kupon Diskon / Program Loyalitas.**
*   `[ ]` **SEO Lanjutan.**
*   `[ ]` **Pengujian Otomatis:** Unit tests, integration tests, end-to-end tests (Jest, React Testing Library, Cypress/Playwright).
*   `[ ]` **PWA (Progressive Web App):** Kemampuan offline dasar, installable.
*   `[ ]` **Fitur Spesifik Karyawan/Stakeholder:** Dashboard atau akses data khusus.

---

## Prasyarat

*   Node.js (versi LTS direkomendasikan, cek `.nvmrc` jika ada)
*   npm atau Yarn
*   Git
*   Akun Supabase (untuk Database PostgreSQL)
*   Akun Google Cloud (untuk Backend Deployment via Cloud Run)
*   Akun Vercel/Netlify (untuk Frontend Deployment)
*   (Nanti) Akun Gateway Pembayaran (misal: Midtrans)
*   Docker (untuk development & deployment ke Cloud Run)

---

## Instalasi & Menjalankan Proyek Lokal

*(Tetap sama seperti sebelumnya, pastikan path `client` dan `server` sesuai)*

1.  **Clone repositori...**
2.  **Instal dependensi Frontend (`cd client && npm install`)...**
3.  **Instal dependensi Backend (`cd ../server && npm install`)...**
4.  **Setup Variabel Lingkungan:**
    *   Salin `.env.example` menjadi `.env` di `/server`. Isi `DATABASE_URL` (dari Supabase), `JWT_SECRET`, `PORT`, dll.
    *   Salin `.env.example` menjadi `.env` di `/client`. Isi `VITE_API_URL=http://localhost:[PORT_BACKEND]`, dll.
5.  **Setup Database (Prisma):**
    *   Pastikan koneksi ke Supabase di `.env` benar.
    *   Jalankan migrasi: `cd server && npx prisma migrate dev`
    *   (Opsional) Jalankan seeder: `cd server && npx prisma db seed` (jika script seed dikonfigurasi di `package.json` & `prisma/seed.ts`)
    *   *(Jika menggunakan Sequelize, langkahnya akan berbeda: `npx sequelize-cli db:migrate`, `npx sequelize-cli db:seed:all`)*
6.  **Jalankan Server Backend (`cd server && npm run dev`)...**
7.  **Jalankan Aplikasi Frontend (`cd client && npm start`)...**

---

## Struktur Proyek

project-root/
├── client/ # Frontend React (Vite)
│ ├── public/
│ ├── src/
│ │ ├── App.jsx
│ │ ├── main.jsx
│ │ └── ... (components, pages, store, services, hooks, assets)
│ ├── index.html
│ ├── package.json
│ ├── tailwind.config.js
│ ├── postcss.config.js
│ └── vite.config.js
├── server/ # Backend Node.js/Express
│ ├── prisma/ # Prisma schema, migrations, seed script
│ │ ├── migrations/
│ │ ├── schema.prisma
│ │ └── seed.ts # (Opsional)
│ ├── src/ # Kode sumber backend
│ │ ├── config/
│ │ ├── controllers/
│ │ ├── middleware/
│ │ ├── routes/
│ │ ├── services/ # (Opsional, untuk business logic)
│ │ ├── utils/
│ │ └── server.ts # atau index.ts/app.ts
│ ├── .env.example
│ ├── package.json
│ ├── tsconfig.json
│ └── Dockerfile # Untuk Cloud Run
├── .gitignore
├── README.md
└── ..

---

## Kontribusi

[Jelaskan bagaimana orang lain bisa berkontribusi. Misal: fork repo, buat branch fitur, buat Pull Request. Sebutkan standar coding jika ada.]

Saat ini kontribusi belum dibuka / Silakan ikuti langkah berikut untuk berkontribusi:
1. Fork repositori ini.
2. Buat branch baru (`git checkout -b fitur/NamaFiturAnda`).
3. Commit perubahan Anda (`git commit -m 'feat: Menambahkan fitur X'`).
4. Push ke branch Anda (`git push origin fitur/NamaFiturAnda`).
5. Buka Pull Request.

---

## Lisensi

Proyek ini dilisensikan di bawah Lisensi Siagian Agro Mandiri - lihat file [LICENSE](LICENSE) (jika ada) untuk detailnya.
