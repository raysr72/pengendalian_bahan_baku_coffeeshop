# Pemodelan Sistem & Arsitektur (System Modeling)
## Pengendalian Bahan Baku

Dokumen ini memuat pemodelan alur kerja dan arsitektur basis data dari sistem pengendalian bahan baku yang dirancang untuk bisnis FnB.

---

## Flowchart Sistem
Diagram yang menggambarkan alur kerja secara keseluruhan dari masing-masing hak akses pengguna (Superadmin, Admin, Petugas) mulai dari proses autentikasi hingga pemrosesan data yang menunjukan proses Operasional. <br>


![Flowchart Sistem](./images/flowchart.png)

**Keterangan Alur:**
- **Autentikasi:** Pengguna melakukan login dengan memasukkan *username* dan *password*, sistem akan memverifikasi level aksesnya.
- **Admin & Petugas:** Admin bertugas mengelola data supplier dan bahan masuk, sedangkan Petugas (Head Bar) fokus mencatat bahan keluar untuk produksi.
- **Superadmin (Owner):** Memiliki hak akses penuh untuk melihat log keseluruhan aktivitas sirkulasi bahan. Serta superadmin memiliki kewenangan untuk memberikan atau membuatkan hak akses untuk semua pengguna (admin dan petugas).

## Diagram Konteks (Context Diagram)
Diagram yang menunjukkan batasan sistem serta entitas-entitas eksternal apa saja yang berinteraksi langsung dengan sistem pengendalian bahan baku.

![Diagram Konteks](./images/diagram_konteks.png)

**Entitas yang Terlibat:**
- **Owner (Superadmin):** Membuat atau memberikan akses ke pengguna dan menerima informasi rekapitulasi data atau laporan.
- **Admin:** Memberikan input data bahan dan bahan masuk, serta menerima informasi terkait.
- **Petugas:** Memberikan input data bahan keluar dan menerima laporan terkait penggunaan bahan.

## Data Flow Diagram (DFD) Level 1
Diagram yang merinci alur proses data yang terjadi di dalam sistem beserta tempat penyimpanan datanya (*data store*) seperti tabel *bahan*, *supplier*, *log_bahan*, dan *users*.

![DFD Level 1](./images/dfd-level-1.png)

## Relasi Basis Data
Diagram relasi basis data menggambarkan struktur tabel-tabel relasional yang digunakan untuk menyimpan seluruh informasi di dalam sistem.

![Relasi Basis Data](./images/er-diagram.png)

**Tabel Utama yang Digunakan:**
- `user`: Menyimpan data akun dan level hak akses.
- `bahan` & `jenis_bahan`: Menyimpan master data bahan baku.
- `supplier`: Menyimpan data pihak penyuplai bahan baku.
- `bahan_masuk` & `bahan_keluar`: Menyimpan riwayat transaksi harian.
- `log_bahan`: Menyimpan rekapitulasi perputaran stok.