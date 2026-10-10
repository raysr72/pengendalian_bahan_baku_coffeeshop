# Functional Requirement

| ID | MODUL / FITUR | PERILAKU SISTEM |
| :--- | :--- | :--- |

| FR-01 | Autentikasi Login | Sistem harus menyediakan halaman login yang memvalidasi username, password, dan level user (Superadmin, Admin, Petugas) sebelum memberikan akses ke dashboard. |
| FR-02 | Manajemen Pengguna | Superadmin dapat mengelola data pengguna (menambah/verifikasi data Admin dan Petugas). |
| FR-03 | Manajemen Data Master | Admin dapat melakukan input, update, dan melihat data master yang terdiri dari: Data Supplier, Data Bahan Baku, Kategori Bahan, dan Satuan Bahan. |
| FR-04 | Pencatatan Bahan Masuk | Admin dapat mencatat transaksi bahan masuk dengan mengisi form yang mencakup: ID Transaksi, Pilih Bahan, Pilih Supplier, Nama Pengirim, Jumlah, dan Tanggal Masuk. |
| FR-05 | Pencatatan Bahan Keluar | Petugas (Head Bar) dapat mencatat transaksi bahan keluar (untuk produksi) dengan mengisi form yang mencakup: ID Transaksi, Pilih Bahan, Jumlah Keluar, dan Tujuan Penggunaan. |
| FR-06 | Log & Audit Bahan | Sistem harus mencatat seluruh riwayat perputaran stok (Log Bahan Masuk dan Log Bahan Keluar) secara otomatis ke dalam basis data yang hanya dapat dipantau penuh oleh Superadmin. |
| FR-07 | Unduh Laporan | Sistem harus menyediakan fitur untuk mengunduh laporan data bahan (masuk/keluar) agar data laporan dapat tersimpan pada perangkat pengguna (Superadmin, Admin, Petugas). |

# Non-Functional Requirement

| KATEGORI | PARAMETER KEBUTUH NON-FUNGSIONAL |
| :--- | :--- |

| Usability (Kegunaan) | Antarmuka (interface) sistem harus intuitif, mudah digunakan (user-friendly) oleh staf Antarmuka (interface) sistem harus intuitif, mudah digunakan (user-friendly) oleh staf operasional kafe tanpa memerlukan pelatihan teknis yang rumit. |
| Performance (Performa) | Sistem berbasis web harus dapat merespons navigasi menu dan pemrosesan data (seperti simpan transaksi atau unduh laporan) secara instan tanpa jeda yang signifikan dalam kondisi jaringan standar. |
| Security (Keamanan) | Akses berbasis peran (Role-Based Access Control / RBAC) yang ketat; halaman Superadmin, Admin, dan Petugas terisolasi sesuai hak aksesnya <br>  Mencegah akses halaman tanpa proses autentikasi login yang valid. |
| Compatibility (Kompatibilitas) | sistem harus dapat diakses melalui berbagai peramban web (browser standar seperti Chrome, Firefox, Safari) di perangkat desktop maupun mobile. |
| Reliability & Availability | Basis data harus dirancang terstruktur (menggunakan relasi tabel MySQL yang baik) untuk menghindari duplikasi data dan memastikan integritas stok tetap terjaga secara konsisten. |
