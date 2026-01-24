
# Laporan Praktikum Minggu [14]
Topik: [Penyusunan Laporan Praktikum Format IMRAD]

---

## Identitas
- **Nama**  : [Ahmad Wildan Asrovi]  
- **NIM**   : [250202927]  
- **Kelas** : [1 IKRB]

---

## Tujuan
Setelah menyelesaikan tugas ini, mahasiswa mampu:
1. Menyusun laporan praktikum dengan struktur ilmiah (Pendahuluan–Metode–Hasil–Pembahasan–Kesimpulan).
2. Menyajikan hasil uji dalam bentuk tabel dan/atau grafik yang jelas.
3. Menuliskan analisis hasil dengan argumentasi yang logis.
4. Menyusun sitasi dan daftar pustaka dengan format yang konsisten.
5. Mengunggah draft laporan ke repositori dengan rapi dan tepat waktu.


---

## Abstrak

Penjadwalan CPU merupakan mekanisme penting dalam sistem operasi untuk menentukan urutan eksekusi proses agar pemanfaatan prosesor lebih efisien. Setiap algoritma penjadwalan memiliki karakteristik yang berbeda dan berdampak langsung terhadap kinerja sistem, khususnya pada waktu tunggu (waiting time) dan waktu penyelesaian (turnaround time). Praktikum ini bertujuan untuk membandingkan kinerja algoritma First Come First Served (FCFS) dan Shortest Job First (SJF) menggunakan simulasi berbasis program Python. Data proses dibaca dari file CSV untuk meningkatkan keterulangan eksperimen. Hasil pengujian menunjukkan bahwa algoritma SJF menghasilkan rata-rata waiting time dan turnaround time yang lebih rendah dibandingkan FCFS. Namun, FCFS memiliki keunggulan dari sisi kesederhanaan implementasi. Dengan demikian, pemilihan algoritma penjadwalan harus disesuaikan dengan kebutuhan dan karakteristik sistem.

**Kata kunci:** CPU Scheduling, FCFS, SJF, Waiting Time, Turnaround Time

---

## 1.1 Pendahuluan (Introduction)

Penjadwalan CPU adalah salah satu fungsi utama sistem operasi yang bertugas mengatur urutan eksekusi proses yang berada dalam keadaan siap (ready state). Tujuan utama penjadwalan CPU adalah untuk meningkatkan efisiensi penggunaan prosesor serta meminimalkan waktu tunggu dan waktu penyelesaian proses.

Algoritma First Come First Served (FCFS) merupakan algoritma penjadwalan paling sederhana yang mengeksekusi proses berdasarkan urutan kedatangan. Meskipun mudah diimplementasikan, FCFS memiliki kelemahan berupa convoy effect, yaitu proses dengan waktu eksekusi panjang dapat menghambat proses lainnya. Sebaliknya, algoritma Shortest Job First (SJF) memilih proses dengan waktu eksekusi (burst time) terpendek terlebih dahulu sehingga secara teori mampu meminimalkan rata-rata waktu tunggu.

Praktikum ini dilakukan untuk membandingkan kinerja algoritma FCFS dan SJF berdasarkan nilai waiting time dan turnaround time menggunakan data proses yang sama.

Tujuan praktikum ini adalah:

1. Mengimplementasikan algoritma penjadwalan FCFS dan SJF.

2. Membandingkan kinerja kedua algoritma berdasarkan waiting time dan turnaround time.

3. Menganalisis kelebihan dan kekurangan masing-masing algoritma.

---

## 2.1 Metode (Methods)
**2.1.1 Lingkungan Pengujian**

Sistem Operasi: Windows

Bahasa Pemrograman: Python

Editor: Visual Studio Code

Metode Penjadwalan: FCFS dan SJF (non-preemptive)


**2.1.2 Data Proses**

Data proses disimpan dalam file Scheduling.csv untuk memisahkan data uji dari kode program sehingga eksperimen lebih terstruktur dan mudah direplikasi.

<div align="center">

| proses | arival time | brust time | 
| :--- | :--- | :--- | 
| **p1** | 0 | 8 |
| **p2** | 1 | 4| 
| **p3** | 2 | 9 | 
| **p4** | 3 | 5 | 

</div>

**2.1.3 Prosedur Praktikum**

1. Menyusun data proses dalam file CSV.

2. Membaca data CSV menggunakan program Python.

3. Melakukan simulasi penjadwalan menggunakan algoritma FCFS.

4. Menghitung waiting time dan turnaround time setiap proses.

5. Mengulangi simulasi menggunakan algoritma SJF.

6. Menampilkan hasil dalam bentuk tabel pada terminal.
   
---

## 3.1 Hasil(Result)

<div align="center">

**Hasil Penjadwalan FCFS**

| proses | Waiting Time | Turnaround Time | 
| :--- | :--- | :--- | 
| **p1** | 0 | 8 |
| **p2** | 7 | 11| 
| **p3** | 10 | 19 | 
| **p4** | 18 | 23 | 
| **Rata Rata** | 8.75 | 15.25 | 

</div>

<div align="center">

**Hasil Penjadwalan SJF**

| proses | Waiting Time | Turnaround Time | 
| :--- | :--- | :--- | 
| **p2** | 0 | 4 |
| **p4** | 4 | 9| 
| **p1** | 9 | 17 | 
| **p3** | 17 | 26 | 
| **Rata Rata** | 7.50 | 14 | 

</div>

![Screenshot hasil](screenshots/.png)

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
