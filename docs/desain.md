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
