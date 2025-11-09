
# Laporan Praktikum Minggu [5]
Topik: [Penjadwalan CPU – FCFS dan SJF]

---

## Identitas
- **Nama**  : [Ahmad Wildan Asrovi]  
- **NIM**   : [250202927]  
- **Kelas** : [1IKRB]

---

## Tujuan
> Mahasiswa mampu menjelaskan fungsi utama sistem operasi dan peran kernel serta system call.
1.Menghitung waiting time dan turnaround time untuk algoritma FCFS dan SJF.
2.Menyajikan hasil perhitungan dalam tabel yang rapi dan mudah dibaca.
3.Membandingkan performa FCFS dan SJF berdasarkan hasil analisis.
4.Menjelaskan kelebihan dan kekurangan masing-masing algoritma.
5.Menyimpulkan kapan algoritma FCFS atau SJF lebih sesuai digunakan.

---

## Dasar Teori
FCFS (First Come First Served) menjadwalkan proses berdasarkan urutan kedatangannya dalam antrean FIFO, sedangkan SJF (Shortest Job First) memprioritaskan proses dengan waktu eksekusi (burst time) terpendek untuk dilayani terlebih dahulu. Keduanya adalah algoritma penjadwalan CPU yang bertujuan mengelola proses, tetapi memiliki kelebihan dan kekurangan yang berbeda, di mana FCFS sangat sederhana namun bisa menghasilkan waktu tunggu lama, sedangkan SJF dapat meminimalkan waktu tunggu rata-rata tetapi lebih kompleks.

---

## Langkah Praktikum
1. Langkah-langkah yang dilakukan.  
2. Perintah yang dijalankan.  
3. File dan kode yang dibuat.  
4. Commit message yang digunakan.

---

## Kode / Perintah
Tuliskan potongan kode atau perintah utama:
```bash
Waiting Time (WT) = waktu mulai eksekusi - Arrival Time
Turnaround Time (TAT) = WT + Burst Time
```

---

## Hasil Eksekusi
Sertakan screenshot hasil percobaan atau diagram:
![Screenshot hasil](screenshots/example.png)

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
   **Jawaban:**  
2. [Pertanyaan 2]  
   **Jawaban:**  
3. [Pertanyaan 3]  
   **Jawaban:**  

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?  

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
