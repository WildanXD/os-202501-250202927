
# Laporan Praktikum Minggu [6]
Topik: [Penjadwalan CPU – Round Robin (RR) dan Priority Scheduling]

---

## Identitas
- **Nama**  : [Ahmad Wildan Asrovi]  
- **NIM**   : [250202927]  
- **Kelas** : [1IKRB]

---

## Tujuan
Setelah menyelesaikan tugas ini, mahasiswa mampu:

1.Menghitung waiting time dan turnaround time pada algoritma RR dan Priority.

2.Menyusun tabel hasil perhitungan dengan benar dan sistematis.

3.Membandingkan performa algoritma RR dan Priority.

4.Menjelaskan pengaruh time quantum dan prioritas terhadap keadilan eksekusi proses.

5.Menarik kesimpulan mengenai efisiensi dan keadilan kedua algoritma.

---

## Dasar Teori
1.Penjadwalan CPU bertujuan mengatur urutan eksekusi proses agar pemanfaatan CPU optimal serta meminimalkan waiting time dan turnaround time.

2.Round Robin (RR) adalah algoritma penjadwalan preemptive yang memberikan jatah waktu CPU (time quantum) secara bergiliran untuk menjamin keadilan antar proses.

3.Priority Scheduling mengeksekusi proses berdasarkan tingkat prioritas, di mana proses dengan prioritas tertinggi akan dijalankan lebih dahulu.

4.Pada Priority Scheduling, dapat terjadi starvation pada proses berprioritas rendah, sehingga sering digunakan teknik aging untuk meningkatkan prioritas secara bertahap.

5.Pemilihan algoritma penjadwalan sangat bergantung pada kebutuhan sistem, seperti respons cepat pada sistem interaktif atau penanganan proses kritis pada sistem real-time.


---

## Langkah Praktikum
1.Mempelajari konsep penjadwalan CPU Round Robin dan Priority Scheduling (Non-Preemptive).
2.Menentukan data proses (arrival time, burst time, dan priority).
3.Menentukan nilai time quantum untuk algoritma Round Robin.
4.Mensimulasikan penjadwalan proses secara manual menggunakan tabel dan Gantt Chart.
5.Mencatat waktu mulai, waktu selesai, serta sisa burst time tiap proses.
6.Menghitung Waiting Time (WT) dan Turnaround Time (TAT) untuk masing-masing proses.
7.Membandingkan hasil RR dan Priority Scheduling berdasarkan nilai WT dan TAT.
8.Menarik kesimpulan dari hasil eksperimen.



---

## Kode / Perintah
Tuliskan potongan kode atau perintah utama:
```bash
Siapkan Data Proses
Gunakan time quantum (q) = 3.
Hitung waiting time dan turnaround time untuk tiap proses.
Catat sisa burst time tiap putaran.
Urutkan proses berdasarkan nilai prioritas (angka kecil = prioritas tinggi).
Lakukan perhitungan manual untuk:
WT[i] = waktu mulai eksekusi - Arrival[i]
TAT[i] = WT[i] + Burst[i]
Buat tabel perbandingan hasil RR dan Priority.
Ubah quantum menjadi 2 dan 5.
Amati perubahan nilai rata-rata waiting time dan turnaround time.
Buat tabel perbandingan efek quantum.


```

---

## Hasil Eksekusi
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
