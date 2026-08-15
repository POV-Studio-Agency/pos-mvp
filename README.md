# Mie Ayam Nusantara — POS Prototype

Prototipe HTML interaktif untuk sistem POS dan operasional multi-cabang berdasarkan `Product Requirements Document (PRD).md`.

## Menjalankan

Jalankan server statis dari folder ini:

```bash
python3 -m http.server 4173
```

Kemudian buka `http://localhost:4173`.

## Area demo

- Owner: dashboard, outlet, penjualan, produk, inventori, dan pengguna.
- Kasir: buka/tutup shift, POS, order aktif, pembayaran, dan struk.
- Dapur: Kitchen Display dengan status Pesanan Baru, Diproses, dan Selesai.

Semua tab, filter, dan aksi utama dapat digunakan. Data master produk, kategori, add-on, harga cabang, outlet, inventori, dan pengguna dapat ditambah atau diedit. Perubahan produk langsung dipakai oleh POS, sementara order yang dikirim akan muncul pada Kitchen Display.

Pilih role pada halaman login. Tidak ada autentikasi backend; seluruh state demo disimpan pada `localStorage`. Tombol **Reset Demo** mengembalikan data awal. Ekspor Excel menghasilkan CSV dan ekspor PDF menggunakan print dialog browser.
