
# Laporan Praktikum Minggu [9]
Topik: [Simulasi Algoritma Penjadwalan CPU]

---

## Identitas
- **Nama**  : [Ahmad Wildan Asrovi]  
- **NIM**   : [250202927]  
- **Kelas** : [1IKRB]

---

## Tujuan
Tuliskan tujuan praktikum minggu ini.  

1. Membuat program simulasi algoritma penjadwalan FCFS dan/atau SJF.
2. Menjalankan program dengan dataset uji yang diberikan atau dibuat sendiri.
3. Menyajikan output simulasi dalam bentuk tabel atau grafik.
4. Menjelaskan hasil simulasi secara tertulis.
5. Mengunggah kode dan laporan ke Git repository dengan rapi dan tepat waktu.

---

## Dasar Teori
1.Penjadwalan proses dalam sistem operasi bertujuan menentukan urutan eksekusi proses agar penggunaan CPU optimal serta waktu tunggu proses dapat diminimalkan.

2.First Come First Served (FCFS) merupakan algoritma penjadwalan non-preemptive yang mengeksekusi proses berdasarkan urutan kedatangan, di mana proses pertama yang masuk adalah proses pertama yang dijalankan.

3.FCFS menggunakan struktur antrian FIFO (First In First Out) sehingga setiap proses yang datang akan menunggu hingga proses sebelumnya selesai tanpa adanya interupsi atau pergantian konteks sebelum waktunya.

4.Waktu tunggu (Waiting Time) dan waktu penyelesaian (Turnaround Time) menjadi parameter utama dalam mengevaluasi performa algoritma FCFS, dengan perhitungan:

Waiting Time = StartTime – ArrivalTime

Turnaround Time = WaitingTime + BurstTime

5.FCFS mudah diimplementasikan dan tidak menyebabkan starvation, namun dapat menimbulkan convoy effect, yaitu proses dengan burst time besar dapat menghambat eksekusi proses lain yang datang kemudian, sehingga waktu rata-rata proses dapat meningkat.

---

## Langkah Praktikum
1.Menyiapkan dataset proses
Membuat file dataset.csv berisi data proses dengan kolom Process, Arrival, Burst sebagai input simulasi.

2.Membuat file program FCFS
Menulis script fcfs.py yang membaca dataset, mengurutkan proses berdasarkan waktu kedatangan, lalu menghitung Waiting Time dan Turnaround Time.

3.Mengimpor library yang diperlukan
Menggunakan pandas untuk membaca dataset dan mengolah data hasil perhitungan.

4.Menjalankan program simulasi
Program dijalankan melalui terminal menggunakan perintah python fcfs.py dari direktori file berada.

5.Mengamati dan mencatat hasil percobaan
Hasil berupa tabel proses beserta nilai Waiting Time dan Turnaround Time, serta perhitungan rata-ratanya ditampilkan di terminal.

6.Commit & Push

  ```bash
   git add .
   git commit -m "Minggu 9 - Simulasi Scheduling CPU"
   git push origin main
   ```

---

## Kode / Perintah
Tuliskan potongan kode atau perintah utama:
```bash
# Hitung waiting time & turnaround time
waiting_time = []
turnaround_time = []
current_time = 0

for i in range(len(df)):
    # mulai eksekusi setelah proses tiba
    current_time = max(current_time, df["Arrival"][i])
    
    wait = current_time - df["Arrival"][i]
    tat = wait + df["Burst"][i]
    
    waiting_time.append(wait)
    turnaround_time.append(tat)
    
    current_time += df["Burst"][i]

df["WaitingTime"] = waiting_time
df["TurnaroundTime"] = turnaround_time

# Tampilkan tabel hasil
print("\n=== HASIL SIMULASI FCFS ===\n")
print(df.to_string(index=False))
print("\nRata-rata Waiting Time :", df["WaitingTime"].mean())
print("Rata-rata Turnaround Time :", df["TurnaroundTime"].mean())
```

---

## Hasil Eksekusi
Sertakan screenshot hasil percobaan atau diagram:
![Screenshot hasil](screenshots/Simulasi_FCFS.png)

---

## Analisis
Pada percobaan ini dilakukan simulasi algoritma First Come First Served (FCFS) menggunakan empat proses dengan waktu kedatangan (arrival time) yang berbeda-beda serta burst time yang bervariasi. Berdasarkan hasil eksekusi program, proses pertama (P1) memiliki waktu tunggu 0 karena langsung dieksekusi ketika sistem mulai. Sementara itu, proses-proses berikutnya mengalami waktu tunggu yang semakin besar akibat penjadwalan berurutan sesuai kedatangan, tanpa mempertimbangkan panjang burst time.

Terlihat bahwa proses dengan burst time besar seperti P2 (burst = 8) dieksekusi lebih awal dibandingkan proses lain yang datang setelahnya. Hal ini menyebabkan proses berikutnya seperti P3 dan P4 mengalami waktu tunggu yang tinggi, yaitu masing-masing 12 dan 18 satuan waktu. Kondisi ini menunjukkan bahwa FCFS memiliki kecenderungan menciptakan antrean panjang (convoy effect), terutama ketika proses dengan durasi eksekusi besar berada di urutan awal.

Nilai rata-rata waiting time sebesar 8,75 dan rata-rata turnaround time sebesar 14,75 mengindikasikan bahwa performa FCFS pada dataset ini kurang optimal. Algoritma ini memang sederhana dan adil secara urutan kedatangan, namun tidak memperhatikan efisiensi waktu eksekusi secara keseluruhan. Akibatnya, respons sistem menjadi kurang baik ketika terdapat proses yang datang berurutan dengan perbedaan burst time yang cukup signifikan.

Secara keseluruhan, percobaan ini memperlihatkan bahwa algoritma FCFS cocok digunakan untuk sistem yang menekankan kesederhanaan dan fairness dalam penjadwalan, tetapi kurang efektif untuk meningkatkan throughput ataupun mengurangi waktu tunggu rata-rata pada beban kerja dengan variasi burst time yang besar. 

---

## Kesimpulan
1.Algoritma FCFS menjadwalkan proses berdasarkan urutan kedatangan, sehingga proses yang datang lebih awal selalu dieksekusi terlebih dahulu tanpa mempertimbangkan burst time. Hal ini membuat proses pertama tidak mengalami waktu tunggu, sedangkan proses selanjutnya menunggu sesuai lamanya eksekusi proses sebelumnya.

2.Variasi burst time yang besar menyebabkan peningkatan waktu tunggu dan turnaround time, terutama ketika proses dengan burst time panjang berada di awal urutan. Kondisi ini memunculkan convoy effect yang berdampak pada performa sistem secara keseluruhan.

3.Berdasarkan hasil percobaan, rata-rata waiting time sebesar 8,75 dan rata-rata turnaround time sebesar 14,75 menunjukkan bahwa FCFS kurang optimal dalam meminimalkan waktu tunggu rata-rata, meskipun algoritma ini sederhana dan mudah diimplementasikan.

---

## Quiz
1. [Mengapa simulasi diperlukan untuk menguji algoritma scheduling?]  

   **Mengapa simulasi diperlukan untuk menguji algoritma scheduling?
Simulasi diperlukan karena memungkinkan pengujian algoritma secara terstruktur tanpa harus menjalankan proses nyata pada sistem operasi. Dengan simulasi, kita dapat melihat urutan eksekusi, waktu tunggu, dan turnaround time secara detail sehingga performa setiap algoritma dapat dibandingkan. Selain itu, simulasi membantu menemukan potensi masalah seperti
starvation atau convoy effect sebelum algoritma diterapkan pada sistem sebenarnya.**
 
3. [Apa perbedaan hasil simulasi dengan perhitungan manual jika dataset besar?]  

   **Apa perbedaan hasil simulasi dengan perhitungan manual jika dataset besar?
Pada dataset kecil, hasil simulasi dan perhitungan manual cenderung sama karena mudah ditelusuri satu per satu. Namun pada dataset besar, perhitungan manual rawan terjadi kesalahan dan memakan waktu lama, sedangkan simulasi dapat menghitung secara konsisten dan cepat. Simulasi juga memudahkan visualisasi dan analisis performa untuk ratusan atau ribuan proses yang sulit dihitung secara manual.**
    
5. [Algoritma mana yang lebih mudah diimplementasikan? Jelaskan.]  

   **Algoritma mana yang lebih mudah diimplementasikan? Jelaskan.
Algoritma FCFS adalah yang paling mudah diimplementasikan karena hanya membutuhkan pengurutan berdasarkan waktu kedatangan dan menjalankan proses sesuai urutan tersebut tanpa logika tambahan. Tidak diperlukan prioritas, preemption, atau pemilihan burst time terkecil seperti pada SJF atau Priority Scheduling, sehingga kode yang dibuat lebih sederhana dan risiko error lebih kecil.:**  

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?  

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
