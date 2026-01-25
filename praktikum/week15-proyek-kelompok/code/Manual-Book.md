# MANUAL BOOK PENGGUNAAN SISTEM

## Proyek Akhir Sistem Operasi

**Judul:** Simulasi Algoritma Sistem Operasi Menggunakan Python dan Docker

---

## 1. Pendahuluan

Manual book ini disusun sebagai panduan penggunaan sistem simulasi Sistem Operasi yang dikembangkan pada proyek akhir mata kuliah Sistem Operasi. Sistem ini mencakup dua modul utama, yaitu simulasi algoritma CPU Scheduling menggunakan metode **First Come First Served (FCFS)** dan simulasi **Manajemen Memori** menggunakan algoritma **Page Replacement FIFO**. Sistem dijalankan menggunakan bahasa pemrograman Python dan diintegrasikan dengan teknologi container Docker.

---

## 2. Kebutuhan Sistem

### 2.1 Perangkat Lunak

* Sistem Operasi Windows / Linux / macOS
* Python versi 3.9 atau lebih baru
* Docker Desktop
* Git (opsional, untuk clone repositori)

### 2.2 Perangkat Keras

* Laptop/PC dengan minimal RAM 4 GB

---

## 3. Struktur Proyek

Struktur direktori proyek sebagai berikut:

```
project/
├── pemutaran_musik.py
├── Page Replacement.py
├── Dockerfile
├── README.md
└── docs/
    └── MANUAL_BOOK.md
```

---

## 4. Cara Menjalankan Sistem Tanpa Docker

### 4.1 Menjalankan Simulasi FCFS

1. Buka terminal atau command prompt.
2. Masuk ke direktori proyek.
3. Jalankan perintah:

   ```bash
   python pemutaran_musik.py
   ```
4. Sistem akan menampilkan simulasi pemutaran musik berdasarkan algoritma FCFS beserta nilai Turnaround Time dan Waiting Time.

### 4.2 Menjalankan Simulasi Page Replacement FIFO

1. Buka terminal.
2. Jalankan perintah:

   ```bash
   python "Page Replacement.py"
   ```
3. Sistem akan menampilkan simulasi penggunaan RAM laptop dan hasil Page Fault serta Hit Ratio.

---

## 5. Cara Menjalankan Sistem Menggunakan Docker

### 5.1 Build Docker Image

1. Pastikan Docker Desktop sudah berjalan.
2. Masuk ke direktori proyek.
3. Jalankan perintah:

   ```bash
   docker build -t simulasi-so .
   ```

### 5.2 Menjalankan Container

1. Jalankan container dengan perintah:

   ```bash
   docker run --rm simulasi-so
   ```
2. Output simulasi akan langsung tampil di terminal.

---

## 6. Penjelasan Output Sistem

### 6.1 Output Simulasi FCFS

* Nama Musik
* Waktu Datang
* Durasi Musik
* Waktu Selesai
* Turnaround Time (TAT)
* Waiting Time
* Rata-rata TAT dan Waiting Time

### 6.2 Output Simulasi Page Replacement FIFO

* Urutan aplikasi yang dibuka
* Isi RAM pada setiap langkah
* Status HIT atau FAULT
* Total Page Fault
* Hit Ratio

---

## 7. Troubleshooting

| Masalah               | Solusi                                    |
| --------------------- | ----------------------------------------- |
| Python tidak dikenali | Pastikan Python sudah ditambahkan ke PATH |
| Docker tidak berjalan | Jalankan Docker Desktop                   |
| File tidak ditemukan  | Periksa nama file dan direktori           |

---

## 8. Penutup

Manual book ini diharapkan dapat membantu pengguna dalam menjalankan dan memahami sistem simulasi Sistem Operasi yang telah dikembangkan. Sistem ini dibuat untuk tujuan pembelajaran dan demonstrasi konsep-konsep dasar Sistem Operasi.

---

**Penulis:** Ahmad Wildan Asrovi
