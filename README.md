# 📦 Sistem Inventaris Toko (Java Swing & MySQL)

Aplikasi *desktop* manajemen inventaris toko berbasis **Java Swing** dan **MySQL** yang dikembangkan menggunakan **NetBeans IDE**. Aplikasi ini mengelola data master (Supplier & Barang), pencatatan transaksi terstandarisasi, serta generator laporan PDF otomatis menggunakan **iText 5**.

## 📸 Tangkapan Layar Aplikasi

### 1. Menu Utama
![Menu Utama](screenshots/menu-utama.png)

### 2. Form Transaksi
![Form Transaksi](screenshots/form-transaksi.png)

### 3. Form Barang & Supplier
![Menu Barang](screenshots/menu-barang.png)
![Menu Supplier](screenshots/menu-suppllier.png)

### 4. Hasil Laporan PDF
![Hasil PDF](screenshots/laporan-pdf.png)

## 🏗️ Modul & Fitur Utama
1. **Koneksi Database (`Koneksi.java`)**: Jembatan penghubung JDBC antara Java Swing dan MySQL lokal XAMPP.
2. **Manajemen Supplier (`FormSupplier.java`)**: CRUD data pemasok dengan *refresh JTable* secara *real-time*.
3. **Manajemen Barang (`FormBarang.java`)**: Pengelolaan inventaris produk dan stok yang terelasi dengan data supplier.
4. **Manajemen Transaksi (`FormTransaksi.java`)**: Pencatatan arus barang masuk/keluar dengan validasi input tanggal otomatis (`YYYY-MM-DD`) via `JFormattedTextField`.
5. **Pelaporan PDF (`CetakLaporan.java`)**: Integrasi iText 5 untuk mengekspor rekapitulasi data transaksi ke dokumen berformat PDF secara instan.

---

## 🗄️ Skema Database (`db_inventaris`)
- **`tb_supplier`**: Data master pemasok (`id_supplier`, `nama_supplier`, `alamat`, `telepon`).
- **`tb_barang`**: Data produk dan stok (`kode_barang`, `nama_barang`, `kategori`, `harga`, `stok`, `id_supplier`).
- **`tb_transaksi`**: Catatan transaksi (`id_transaksi`, `kode_barang`, `jenis_transaksi`, `jumlah`, `tanggal`).

---

## 🚀 Panduan Singkat
1. **Clone Repository:**
   ```bash
   git clone [https://github.com/henricofernando18/Sistem-Inventaris-Toko.git](https://github.com/henricofernando18/Sistem-Inventaris-Toko.git)
