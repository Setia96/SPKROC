🗃️ DB Sistem Penilaian Tempat PKL Siswa Berbasis Multi-Kriteria

📌 Deskripsi
Repository ini berisi skrip SQL untuk membangun sistem database penilaian tempat praktik kerja lapangan (PKL) siswa menggunakan pendekatan multi-kriteria. Sistem ini dirancang untuk membantu institusi pendidikan dalam memilih tempat PKL yang paling sesuai berdasarkan berbagai kriteria penting seperti lokasi industri, nilai akademik siswa, finansial orang tua, hingga sikap dan kerjasama siswa.

🧱 Struktur Tabel
Berikut adalah tabel utama yang terdapat dalam file n1601716_spk.sql:

| Tabel               | Deskripsi                                                                                |
| ------------------- | ---------------------------------------------------------------------------------------- |
| `kriteria`          | Menyimpan daftar kriteria penilaian beserta bobot ROC dan rankingnya                     |
| `siswa`             | Menyimpan data siswa yang akan ditempatkan untuk PKL                                     |
| `tempat_pkl`        | Menyimpan informasi tempat PKL beserta kuota dan profil kriteria ideal dalam format JSON |
| `nilai_kriteria`    | Menyimpan nilai siswa terhadap masing-masing kriteria                                    |
| `profil_tempat_pkl` | Menyimpan nilai ideal masing-masing tempat PKL untuk setiap kriteria                     |

⚙️ Fitur Sistem
1. Mengelola data siswa dan tempat PKL
2. Menyimpan dan menghitung skor berdasarkan kriteria penilaian
3. Relasi antar tabel dengan foreign key
4. Profil tempat PKL disimpan dalam bentuk JSON agar fleksibel dan mudah dibandingkan
5. Basis data siap diintegrasikan ke dalam aplikasi web berbasis SPK

🛠️ Cara Menggunakan
1. Clone repository ini: git clone https://github.com/username/nama-repo.git
2. Buat database baru di MySQL / phpMyAdmin, misalnya spk_pkl.
3. Impor file SQL:
   * Buka phpMyAdmin > database spk_pkl > Import
   * Upload file n1601716_spk.sql dan klik Go
   * atau via terminal MySQL: **SOURCE path/to/n1601716_spk.sql;**

💡 Catatan Teknis
* File ini dibuat dengan phpMyAdmin 5.2.2 dan MariaDB 10.11
* Gunakan utf8mb4 agar mendukung karakter Unicode penuh
* Format waktu mengikuti datetime CURRENT_TIMESTAMP secara otomatis
