
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
Berdasarkan hasil simulasi penjadwalan CPU yang telah dilakukan, terlihat bahwa setiap algoritma memiliki karakteristik dan performa yang berbeda terhadap nilai Waiting Time (WT) dan Turnaround Time (TAT).

Pada algoritma Round Robin dengan quantum 3, sistem bersifat sangat adil karena setiap proses mendapatkan jatah CPU yang sama. Namun, nilai WT dan TAT cenderung lebih besar akibat sering terjadinya context switching, terutama pada proses dengan burst time besar seperti p3 dan p4. Hal ini menyebabkan proses harus menunggu lebih lama sebelum dapat kembali dieksekusi.

Ketika nilai time quantum diperbesar menjadi 5, jumlah context switching berkurang dan proses dapat berjalan lebih lama dalam satu giliran. Akan tetapi, karakteristik Round Robin mulai mendekati FCFS, sehingga proses yang datang lebih awal memiliki waktu tunggu lebih panjang. Akibatnya, rata-rata WT dan TAT justru meningkat dibandingkan quantum 3.

Pada Priority Scheduling (Non-Preemptive), proses dengan prioritas tinggi dieksekusi lebih awal tanpa preemption. Hasilnya, algoritma ini menghasilkan nilai rata-rata WT dan TAT paling kecil pada percobaan ini. Namun demikian, proses dengan prioritas rendah seperti p4 mengalami waktu tunggu yang cukup besar, sehingga algoritma ini berpotensi menyebabkan starvation jika tidak dikombinasikan dengan mekanisme aging. 

---

## Kesimpulan
Round Robin unggul dalam keadilan dan cocok untuk sistem interaktif.

Priority Scheduling lebih efisien dari sisi waktu, tetapi kurang adil.

Pemilihan algoritma penjadwalan harus disesuaikan dengan kebutuhan sistem, apakah mengutamakan responsivitas atau efisiensi eksekusi.

---

## Quiz
1. [Pertanyaan 1]  
   **Jawaban: 1. Perbedaan Utama antara Round Robin dan Priority Scheduling
Perbedaan utama antara Round Robin dan Priority Scheduling terletak pada cara penentuan urutan eksekusi proses.
Round Robin membagi waktu CPU secara merata kepada semua proses menggunakan time quantum, sehingga setiap proses mendapatkan kesempatan yang adil untuk dieksekusi.
Sebaliknya, Priority Scheduling menentukan urutan eksekusi berdasarkan tingkat prioritas, di mana proses dengan prioritas tertinggi akan dijalankan terlebih dahulu.**  
2. [Pertanyaan 2]  
   **Jawaban: 2. Pengaruh Besar/Kecilnya Time Quantum terhadap Performa Sistem
Ukuran time quantum sangat mempengaruhi performa sistem pada algoritma Round Robin:
Time quantum kecil menyebabkan context switching lebih sering, sehingga meningkatkan overhead dan waktu tunggu proses.
Time quantum besar mengurangi context switching, tetapi membuat perilaku Round Robin mendekati FCFS, sehingga respons sistem menjadi lebih lambat.
Oleh karena itu, time quantum harus dipilih secara seimbang agar sistem tetap responsif dan efisien.**  
3. [Pertanyaan 3]  
   **Jawaban: 3. Mengapa Algoritma Priority dapat Menyebabkan Starvation?
Starvation terjadi pada Priority Scheduling karena proses dengan prioritas rendah terus-menerus kalah oleh proses dengan prioritas lebih tinggi.
Jika proses prioritas tinggi terus masuk ke sistem, maka proses prioritas rendah dapat menunggu tanpa batas waktu dan tidak pernah dieksekusi.
Masalah ini biasanya diatasi dengan teknik aging, yaitu meningkatkan prioritas proses yang terlalu lama menunggu.**  

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?  

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
