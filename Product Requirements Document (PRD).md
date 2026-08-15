# Product Requirements Document (PRD)
## Sistem POS & Operasional Multi-Cabang — Mie Ayam

### 1. Ringkasan Produk

Sistem ini merupakan aplikasi operasional F&B untuk bisnis mie ayam yang memiliki beberapa cabang.

Aplikasi membantu proses operasional mulai dari transaksi kasir, pengelolaan pesanan dapur, stok per ca
bang, hingga monitoring performa seluruh outlet oleh owner melalui satu dashboard.

Fokus utama versi awal adalah:

**Transaksi cepat → Pesanan terhubung ke dapur → Stok per cabang → Monitoring seluruh outlet**

---

## 2. Tujuan Produk

### Tujuan Bisnis

- Mempermudah proses transaksi pada setiap cabang.
- Memusatkan data penjualan seluruh cabang.
- Memungkinkan owner memonitor performa outlet tanpa harus datang langsung.
- Mengurangi kesalahan komunikasi antara kasir dan dapur.
- Mempermudah kontrol stok setiap cabang.
- Menyediakan laporan penjualan secara real-time.

### Tujuan Pengguna

**Owner**
- Mengetahui omzet seluruh cabang.
- Membandingkan performa antar cabang.
- Memantau transaksi dan stok.

**Manager / Kepala Cabang**
- Mengelola operasional cabangnya.
- Melihat transaksi dan stok cabang.
- Memantau aktivitas kasir.

**Kasir**
- Membuat transaksi dengan cepat.
- Menerima pembayaran.
- Mencetak atau mengirim struk.

**Dapur**
- Melihat pesanan yang masuk.
- Melihat detail dan catatan pesanan.
- Mengubah status pengerjaan.

---

# 3. User Roles

## 3.1 Owner / Super Admin

Memiliki akses seluruh sistem dan seluruh cabang.

Hak akses:

- Dashboard seluruh cabang
- Dashboard per cabang
- Manajemen cabang
- Manajemen menu
- Manajemen harga
- Manajemen user
- Monitoring transaksi
- Monitoring stok
- Transfer stok
- Laporan penjualan
- Konfigurasi sistem

---

## 3.2 Manager Area

Opsional apabila bisnis memiliki banyak cabang.

Hak akses:

- Melihat beberapa cabang yang ditugaskan
- Monitoring transaksi
- Monitoring stok
- Laporan cabang
- Monitoring performa outlet

---

## 3.3 Kepala Cabang

Hanya memiliki akses ke cabang yang ditugaskan.

Hak akses:

- Dashboard cabang
- Transaksi cabang
- Stok cabang
- Kasir cabang
- Laporan cabang

---

## 3.4 Kasir

Hak akses:

- Membuka POS
- Membuat pesanan
- Memilih meja
- Menambahkan topping/add-on
- Memasukkan catatan pelanggan
- Memproses pembayaran
- Melihat transaksi shift
- Mencetak struk

---

## 3.5 Dapur

Hak akses:

- Melihat pesanan masuk
- Melihat detail pesanan
- Melihat catatan pelanggan
- Mengubah status pesanan

Dapur tidak dapat melihat informasi omzet maupun laporan keuangan.

---

# 4. Fitur Utama

## 4.1 Manajemen Cabang

Owner dapat membuat dan mengelola outlet.

Data cabang:

- Nama cabang
- Kode cabang
- Alamat
- Nomor telepon
- Jam operasional
- Status aktif/nonaktif

Contoh:

- Mie Ayam — Cabang Mataram
- Mie Ayam — Cabang Ampenan
- Mie Ayam — Cabang Cakranegara

Setiap transaksi wajib memiliki referensi cabang.

---

# 5. POS / Kasir

POS menjadi halaman utama bagi kasir.

## 5.1 Membuat Pesanan

Kasir dapat:

- Memilih menu
- Menentukan jumlah
- Menambah topping
- Memilih varian
- Memberikan catatan
- Memilih meja
- Memilih tipe pesanan

Tipe pesanan:

- Dine In
- Takeaway

Future development:

- Delivery
- Online Order
- QR Order

---

## 5.2 Produk

Contoh kategori:

### Mie

- Mie Ayam
- Mie Ayam Bakso
- Mie Ayam Pangsit
- Mie Ayam Komplit

### Bakso

- Bakso Biasa
- Bakso Urat
- Bakso Komplit

### Minuman

- Es Teh
- Teh Hangat
- Es Jeruk
- Air Mineral

---

## 5.3 Add-On / Topping

Sistem mendukung tambahan produk.

Contoh:

- Tambah Bakso
- Tambah Pangsit
- Tambah Ayam
- Ekstra Mie
- Tambah Sayur

Contoh transaksi:

**Mie Ayam**

+ Bakso × 2  
+ Pangsit × 1

---

# 6. Catatan Pesanan

Kasir dapat menambahkan catatan.

Contoh:

- Tanpa sawi
- Tidak pedas
- Kuah sedikit
- Mie matang
- Bakso dipisah

Catatan akan otomatis tampil pada Kitchen Display.

---

# 7. Manajemen Meja

Sistem menyimpan daftar meja per outlet.

Contoh:

- Meja 01
- Meja 02
- Meja 03
- Meja 04

Status meja:

- Kosong
- Terisi
- Menunggu pembayaran

Kasir dapat menambahkan pesanan baru ke meja yang masih aktif.

---

# 8. Kitchen Display System

Setelah transaksi dibuat, pesanan otomatis muncul pada layar dapur cabang tersebut.

Contoh:

### Order #A021

**Meja 05**

2 × Mie Ayam Bakso  
1 × Es Teh

Catatan:

> Tanpa sawi, kuah sedikit.

Status pesanan:

**Pesanan Baru**

↓

**Diproses**

↓

**Selesai**

Ketika dapur menandai pesanan selesai, status juga berubah pada POS.

---

# 9. Pembayaran

Metode pembayaran awal:

- Tunai
- QRIS
- Transfer

Kasir memilih metode pembayaran saat checkout.

Informasi pembayaran:

- Subtotal
- Diskon
- Total
- Jumlah dibayar
- Kembalian
- Metode pembayaran

---

# 10. Struk

Setelah pembayaran berhasil, sistem membuat struk transaksi.

Informasi struk:

- Logo bisnis
- Nama outlet
- Alamat
- Nomor transaksi
- Tanggal
- Kasir
- Detail pesanan
- Total
- Metode pembayaran

Output:

- Print thermal printer
- Digital receipt

---

# 11. Manajemen Menu

Owner dapat mengelola menu secara terpusat.

Data menu:

- Nama produk
- SKU
- Kategori
- Harga
- Foto
- Status
- Cabang tersedia

Status:

- Aktif
- Tidak tersedia
- Habis

---

# 12. Harga per Cabang

Harga dapat menggunakan dua skenario.

### Harga Global

Semua cabang menggunakan harga yang sama.

Contoh:

Mie Ayam = Rp15.000

### Harga Khusus Cabang

Cabang tertentu memiliki harga berbeda.

Contoh:

| Cabang | Harga |
|---|---:|
| Mataram | Rp15.000 |
| Ampenan | Rp15.000 |
| Senggigi | Rp17.000 |

Harga khusus cabang akan mengoverride harga global.

---

# 13. Inventory / Stok

Setiap cabang memiliki stok terpisah.

Contoh bahan:

- Mie
- Ayam
- Bakso
- Pangsit
- Sawi
- Saus
- Minuman

Data stok:

- Stok awal
- Stok masuk
- Stok keluar
- Stok saat ini
- Minimum stok

---

# 14. Stock Movement

Setiap perubahan stok memiliki histori.

Jenis movement:

- Stock In
- Stock Out
- Adjustment
- Transfer
- Waste

Contoh:

**Bakso**

Stock awal: 100

Penjualan: -30

Waste: -2

Sisa:

**68 pcs**

---

# 15. Transfer Stok Antar Cabang

Cabang dapat mengirim stok ke cabang lainnya.

Flow:

**Cabang A**

↓

Mengajukan transfer

↓

**Cabang B**

↓

Konfirmasi penerimaan

↓

Stok otomatis diperbarui.

Data transfer:

- Asal cabang
- Tujuan cabang
- Item
- Jumlah
- Tanggal
- Pengirim
- Penerima
- Status

Status:

- Draft
- Dikirim
- Diterima
- Dibatalkan

---

# 16. Dashboard Owner

Dashboard menampilkan ringkasan seluruh bisnis.

## Summary Card

### Omzet Hari Ini

Rp12.500.000

### Total Transaksi

520 transaksi

### Average Order Value

Rp24.038

### Cabang Aktif

6 outlet

---

# 17. Performa Cabang

Owner dapat membandingkan cabang.

Contoh:

| Cabang | Omzet | Transaksi |
|---|---:|---:|
| Mataram | Rp3.500.000 | 142 |
| Ampenan | Rp2.800.000 | 120 |
| Cakranegara | Rp2.500.000 | 105 |
| Senggigi | Rp1.900.000 | 78 |

Owner dapat melihat:

- Cabang omzet tertinggi
- Cabang transaksi tertinggi
- Average Order Value
- Pertumbuhan penjualan

---

# 18. Menu Terlaris

Dashboard menampilkan ranking produk.

Contoh:

1. Mie Ayam Bakso — 350
2. Mie Ayam Original — 290
3. Mie Ayam Pangsit — 230
4. Bakso Komplit — 180

Data dapat difilter berdasarkan:

- Hari
- Minggu
- Bulan
- Cabang

---

# 19. Laporan Penjualan

Filter:

- Tanggal
- Cabang
- Kasir
- Metode pembayaran

Laporan mencakup:

- Gross sales
- Discount
- Net sales
- Jumlah transaksi
- Average order value
- Produk terjual

Export:

- Excel
- PDF

---

# 20. Laporan Metode Pembayaran

Contoh:

| Metode | Transaksi | Total |
|---|---:|---:|
| Cash | 120 | Rp2.500.000 |
| QRIS | 250 | Rp5.800.000 |
| Transfer | 20 | Rp500.000 |

---

# 21. Manajemen User

Admin dapat membuat user.

Data:

- Nama
- Username
- Email
- Nomor HP
- Role
- Cabang
- Status

Satu user dapat memiliki akses terhadap satu atau beberapa outlet sesuai role.

---

# 22. Shift Kasir

Kasir harus membuka shift sebelum melakukan transaksi.

### Open Shift

Kasir memasukkan:

- Kas awal
- Waktu mulai

### Close Shift

Sistem menghitung:

- Cash sales
- QRIS
- Transfer
- Total penjualan
- Expected cash

Kasir memasukkan:

- Actual cash

Sistem menghitung selisih.

---

# 23. Void & Refund

Transaksi tertentu dapat:

- Dibatalkan
- Di-refund

Namun membutuhkan otorisasi role tertentu.

Informasi wajib:

- Alasan
- User yang melakukan
- Waktu
- Nilai transaksi

Semua aktivitas disimpan dalam audit log.

---

# 24. Audit Log

Sistem merekam aktivitas penting.

Contoh:

- User login
- Perubahan harga
- Void transaksi
- Refund
- Adjustment stok
- Transfer stok
- Perubahan menu

Tujuan:

Meningkatkan kontrol operasional multi-cabang.

---

# 25. Struktur Navigasi

## Owner

**Dashboard**

**Outlet**
- Daftar Cabang
- Detail Cabang

**Sales**
- Transactions
- Reports

**Products**
- Menu
- Categories
- Add-ons

**Inventory**
- Stock
- Stock Movement
- Stock Transfer

**Users**

**Settings**

---

## Kasir

- POS
- Orders
- Transactions
- Shift

---

## Dapur

- Kitchen Orders

---

# 26. MVP Scope

Versi pertama difokuskan pada fitur yang dibutuhkan untuk menjalankan operasional sehari-hari.

### Wajib MVP

- Login
- Role & permission
- Multi-cabang
- Menu
- Kategori
- Add-on
- Harga
- POS
- Dine-in
- Takeaway
- Meja
- Kitchen Display
- Cash payment
- QRIS manual
- Print receipt
- Shift kasir
- Inventory dasar
- Stok per cabang
- Dashboard owner
- Laporan penjualan
- Laporan per cabang

---

# 27. Phase 2

Setelah sistem operasional inti stabil:

- Transfer stok antar cabang
- Recipe / ingredient deduction
- Purchase order
- Supplier management
- Waste management
- Refund workflow
- Advanced reporting
- Loyalty customer

---

# 28. Future Development

Fitur yang dapat dikembangkan kemudian:

### QR Order

Pelanggan scan QR di meja.

↓

Pilih menu

↓

Order

↓

Order masuk ke dapur.

---

### Customer Loyalty

- Nomor HP pelanggan
- Point
- Reward
- Voucher
- Riwayat transaksi

---

### WhatsApp Integration

- Digital receipt
- Promo
- Voucher
- Loyalty notification

---

### Online Order

Integrasi:

- Website
- WhatsApp
- GoFood
- GrabFood
- ShopeeFood

---

### Central Kitchen

Untuk bisnis yang memiliki dapur pusat:

**Central Kitchen**

↓

Distribusi bahan

↓

Cabang

↓

Penjualan

---

# 29. Non-Functional Requirements

## Performance

Target:

- POS response < 2 detik
- Kitchen order muncul maksimal 2–3 detik setelah dibuat
- Dashboard dapat menampilkan data tanpa mengganggu operasional POS

---

## Availability

Sistem ditargetkan tersedia selama jam operasional outlet.

Target awal:

**99,5% uptime**

---

## Security

Minimum security:

- Authentication
- Role-based access control
- Password hashing
- Session management
- HTTPS
- Audit log
- API authorization

---

## Data Isolation

Seluruh data operasional harus memiliki referensi:

`outlet_id`

Contoh:

- Transaction
- Order
- Stock
- Shift
- User
- Kitchen Order

Hal ini penting agar data antar cabang tidak tercampur.

---

# 30. KPI Produk

Keberhasilan sistem dapat diukur melalui:

### Operational KPI

- Waktu input transaksi
- Waktu pesanan sampai dapur
- Waktu penyelesaian order
- Jumlah void transaksi
- Selisih kas

### Business KPI

- Daily Sales
- Number of Transactions
- Average Order Value
- Best Selling Product
- Sales per Outlet
- Outlet Growth

---

# 31. Core User Flow

### Dine-In

Pelanggan datang

↓

Pilih meja

↓

Kasir membuat pesanan

↓

Order masuk ke dapur

↓

Dapur memproses pesanan

↓

Pesanan selesai

↓

Pelanggan melakukan pembayaran

↓

Transaksi selesai

↓

Dashboard owner otomatis diperbarui.

---

# 32. Value Proposition

Sistem bukan sekadar aplikasi kasir.

Produk diposisikan sebagai:

> **Sistem operasional terpusat untuk bisnis mie ayam multi-cabang.**

Owner mendapatkan satu tempat untuk memonitor:

**Penjualan**

+

**Cabang**

+

**Kasir**

+

**Dapur**

+

**Stok**

+

**Laporan**

Sehingga bisnis dapat berkembang ke lebih banyak outlet tanpa kehilangan kontrol terhadap operasional.