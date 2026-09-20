# Dokumen Desain

## 1. Data Layer (products.php)
File ini menyimpan seluruh data produk dalam sebuah array
multidimensi. Satu produk = satu array asosiatif.

Field setiap produk:
| Field | Tipe | Keterangan |
|---|---|---|
| id | integer | Nomor unik produk |
| nama | string | Nama produk |
| kategori | string | Kategori produk |
| harga | integer | Harga satuan (Rupiah) |
| stok | integer | Jumlah barang tersedia |
| deskripsi | string | Penjelasan singkat produk |

Contoh data:
| id | nama | kategori | harga | stok |
|---|---|---|---|---|
| 1 | Laptop Asus | Elektronik | 7500000 | 10 |
| 2 | Mouse Logitech | Aksesoris | 150000 | 2 |
| 3 | Keyboard Mekanik | Aksesoris | 450000 | 5 |

## 2. Processing Layer (functions.php)

### Fungsi hitungTotalNilaiStok()
- Input: array produk
- Proses: untuk setiap produk, hitung harga x stok, lalu jumlahkan semuanya
- Output: total nilai aset gudang (angka)

Rumus: Total = jumlah dari (harga x stok) semua produk

Contoh: (7.500.000 x 10) + (150.000 x 2) + (450.000 x 5)
= 75.000.000 + 300.000 + 2.250.000 = 77.550.000

### Logika Stok Kritis
- Jika stok < 3, baris tabel diberi warna khusus (misalnya merah)
- Jika stok >= 3, baris tampil normal
