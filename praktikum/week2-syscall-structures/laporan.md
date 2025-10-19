
# Laporan Praktikum Minggu [2]
Topik: [syscall_structure]

---

## Identitas
- **Nama**  : [Ahmad Wildan Asrovi]  
- **NIM**   : [250202927]  
- **Kelas** : [1IKRB]

---

## Tujuan
Setelah menyelesaikan tugas ini, mahasiswa mampu:

1.Menjelaskan konsep dan fungsi system call dalam sistem operasi.
2.Mengidentifikasi jenis-jenis system call dan fungsinya.
3.Mengamati alur perpindahan mode user ke kernel saat system call terjadi.
4.Menggunakan perintah Linux untuk menampilkan dan menganalisis system call.

---

## Dasar Teori
cara terprogram bagi program untuk meminta layanan dari sistem operasi, berfungsi sebagai jembatan antara aplikasi pengguna dan kernel OS. Program menggunakan system call untuk meminta layanan tingkat rendah seperti membuat proses baru, membuka/menulis file, atau berinteraksi dengan perangkat keras, karena aplikasi tidak dapat mengakses perangkat keras atau sumber daya sistem secara langsung demi keamanan dan stabilitas. 

---

## Langkah Praktikum
1. Langkah-langkah yang dilakukan.  
2. Perintah yang dijalankan.  
3. File dan kode yang dibuat.  
4. Commit message yang digunakan.

---

## Kode / Perintah
potongan kode atau perintah utama:
```bash
strace ls
```

---

## Hasil Eksekusi
Sertakan screenshot hasil percobaan atau diagram:
![Screenshot 2025-10-19 141053 , Screenshot 2025-10-19 141054 , Screenshot 2025-10-19 141217](screenshots/example.png)

---

## Analisis
- Jelaskan makna hasil percobaan.  
- Hubungkan hasil dengan teori (fungsi kernel, system call, arsitektur OS).  
- Apa perbedaan hasil di lingkungan OS berbeda (Linux vs Windows)?  

---

## Kesimpulan
Tuliskan 2–3 poin kesimpulan dari praktikum ini.

---

## Quiz
1. [Pertanyaan 1]  
   **Manajemen Proses, Manajemen File, Manajemen Perangkat, Pemeliharaan Informasi, Komunikasi Antar Proses, Keamanan**  
2. [Pertanyaan 2]  
   **Manajemen Proses, Manajemen File, Manajemen Perangkat, Pemeliharaan Informasi**  
3. [Pertanyaan 3]  
   **karena system call memerlukan akses ke sumber daya (resource) yang hanya bisa diakses oleh kernel (mode kernel), bukan oleh program pengguna (user mode)**  

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?  

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_