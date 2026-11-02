# Modul Pembuktian Penggunaan Regresi dan Interpretasi R²

**Referensi artikel jurnal SINTA 3 (2022--2023)**

## 1. Tujuan

Modul ini disusun untuk mengumpulkan bukti dari lima artikel jurnal
terakreditasi SINTA 3 yang menggunakan metode regresi dan melaporkan
nilai koefisien determinasi (R²). Fokusnya adalah membuktikan bagaimana
R² digunakan dan apakah nilainya harus selalu mendekati 1.

**Batas pekerjaan:** tahap ini merupakan studi literatur. Belum perlu
membuat program, melakukan training model, atau membangun dataset
sendiri.

## 2. Pengertian R²

R² (R-squared/koefisien determinasi) menunjukkan proporsi variasi nilai
target yang dapat dijelaskan oleh model pada data yang dievaluasi.

Contoh: - R² = 0,92 berarti sekitar 92% variasi target dapat dijelaskan
oleh model. - R² = 0,60 berarti sekitar 60% variasi target dapat
dijelaskan oleh model. - R² = 0,08 berarti sekitar 8% variasi target
dapat dijelaskan oleh model.

Dalam regresi standar, R² yang lebih tinggi biasanya menunjukkan
kecocokan model yang lebih baik pada data evaluasi. Namun, **tidak ada
satu ambang R² yang berlaku untuk semua bidang dan semua dataset**. R²
rendah bukan otomatis berarti perhitungan salah; itu menunjukkan
kemampuan penjelasan model terbatas. Untuk prediksi, R² harus dibaca
bersama MAE/RMSE, metode validasi, dan hasil pada data uji. R² pada data
training saja tidak cukup untuk membuktikan model mampu melakukan
generalisasi.

## 3. Lima artikel jurnal yang dijadikan bukti

### Jurnal 1 --- Support Vector Regression (SVR), 2023

- **Judul:** Implementasi GridSearchCV pada Support Vector Regression
  (SVR) untuk Peramalan Harga Saham
- **Penulis:** Aanisah Waliy Ishlah, Sudarno, dan Puspita Kartikasari
- **Jurnal:** Jurnal Gaussian, Vol. 12 No. 2, 2023, hlm. 276--286
- **DOI:** https://doi.org/10.14710/j.gauss.12.2.276-286
- **Bukti nilai:** R² = 0,9206643; MSE = 0,001237173; SMAPE =
  0,1167301.
- **Makna bukti:** penelitian ini memperoleh R² sekitar 92,07%
  menggunakan SVR kernel linear yang parameternya dipilih dengan
  GridSearchCV. Ini contoh hasil R² yang mendekati 1.
- **Sumber artikel/PDF:**
  https://ejournal3.undip.ac.id/index.php/gaussian/article/view/36643
- **Bukti peringkat:** laman SINTA mencantumkan artikel Jurnal
  Gaussian tahun 2023 dengan akreditasi SINTA 3:
  https://sinta.kemdiktisaintek.go.id/journals/profile/8421?page=4

### Jurnal 2 --- Regresi Semiparametrik, 2023

- **Judul:** Modelling of Poverty Percentage in East Java Province
  with Semiparametric Regression Approach
- **Penulis:** Idrus Syahzaqi, Salman Alfarizi P. A., dan Kartika
  Fithriasari
- **Jurnal:** BAREKENG: Jurnal Ilmu Matematika dan Terapan, Vol. 17
  No. 2, 2023, hlm. 727--734
- **DOI:** https://doi.org/10.30598/barekengvol17iss2pp0727-0734
- **Bukti nilai:** R² = 98,71%; MSE = 12,2156.
- **Makna bukti:** model regresi semiparametrik yang digunakan pada
  penelitian tersebut menghasilkan R² tinggi. Ini menunjukkan
  pendekatan regresi yang sesuai dengan karakteristik data dapat
  menghasilkan daya jelas yang tinggi.
- **Sumber artikel:**
  https://ojs3.unpatti.ac.id/index.php/barekeng/article/view/7712

### Jurnal 3 --- Nonparametric Geographically Weighted Regression, 2023

- **Judul:** Application of Nonparametric Geographically Weighted
  Regression Method on Open Unemployment Rate Data in Indonesia
- **Penulis:** Marisa Nanda Saputri, Sifriyani, dan Wasono
- **Jurnal:** BAREKENG: Jurnal Ilmu Matematika dan Terapan, Vol. 17
  No. 4, 2023, hlm. 2071--2080
- **DOI:** https://doi.org/10.30598/barekengvol17iss4pp2071-2080
- **Bukti nilai:** R² = 83,45% untuk model terbaik dengan pembobot
  kernel bisquare.
- **Makna bukti:** R² tidak harus tepat 1. Nilai 83,45% tetap
  dilaporkan sebagai proporsi variasi tingkat pengangguran terbuka
  yang dapat dijelaskan model. Penilaian kelayakan tetap harus melihat
  konteks penelitian dan metrik lain.
- **Sumber artikel/PDF:**
  https://ojs3.unpatti.ac.id/index.php/barekeng/article/download/9460/7193/

### Jurnal 4 --- Regresi Nonparametrik Campuran, 2023

- **Judul:** Mixed Estimators of Truncated Spline-Epanechnikov Kernel
  on Nonparametric Regression and Its Applications
- **Penulis:** Sifriyani, Andrea Tri Rian Dani, Meirinda Fauziyah, dan
  Zakiyah Mar'ah
- **Jurnal:** BAREKENG: Jurnal Ilmu Matematika dan Terapan, Vol. 17
  No. 4, 2023, hlm. 2023--2032
- **DOI:** https://doi.org/10.30598/barekengvol17iss4pp2023-2032
- **Bukti nilai:** R² = 98,11%.
- **Makna bukti:** penelitian ini menggabungkan estimator truncated
  spline dan kernel Epanechnikov. Hasilnya menunjukkan R² tinggi pada
  penerapan kasus yang diteliti.
- **Sumber artikel/PDF:**
  https://ojs3.unpatti.ac.id/index.php/barekeng/article/download/9262/7189/

### Jurnal 5 --- Regresi Linear, 2022

- **Judul:** The Effect of Earnings Per Share, Return on Equity, and
  Debt to Equity on BUMN Companies
- **Penulis:** Mega Citra Tumorang, Ike Rukmana Sari, dan Ribka
- **Jurnal:** Jurnal Ipteks Terapan: Research of Applied Science and
  Education, Vol. 16 No. 3, 2022, hlm. 533--542
- **DOI:** https://doi.org/10.22216/jit.v15i3.1128
- **Bukti nilai:** R² = 0,084 atau 8,4%.
- **Makna bukti:** nilai R² yang jauh dari 1 tetap merupakan hasil
  penelitian yang sah untuk dilaporkan. Namun, interpretasinya adalah
  variabel dalam model hanya menjelaskan 8,4% variasi harga saham,
  sedangkan 91,6% lainnya berada di luar variabel penelitian. Jadi,
  ini **bukan bukti model prediksi yang bagus**, melainkan bukti bahwa
  R² rendah tidak otomatis membuat penelitian atau perhitungannya
  salah.
- **Sumber artikel/PDF:**
  https://publikasi.lldikti10.id/index.php/jit/article/download/1128/796
- **Bukti peringkat:** artikel menyebut Jurnal Ipteks Terapan sebagai
  jurnal SINTA 3 pada halaman awal PDF.

## 4. Ringkasan perbandingan bukti

No. Metode Tahun Nilai R²

---

1 Support Vector Regression (SVR) 2023 0,9207
2 Regresi semiparametrik 2023 0,9871
3 Nonparametric Geographically Weighted Regression 2023 0,8345
4 Truncated spline--Epanechnikov kernel 2023 0,9811
5 Regresi linear 2022 0,0840

Catatan: nilai R² di atas berasal dari konteks, target, dan prosedur
evaluasi penelitian yang berbeda. Angka-angka ini **tidak boleh dianggap
sebagai perbandingan langsung untuk menentukan algoritma terbaik**,
karena dataset, variabel, pembagian data, dan tujuan penelitian tidak
sama.

## 5. Pembuktian dan jawaban atas pertanyaan

Berdasarkan lima artikel tersebut, dapat dibuktikan bahwa:

1. R² yang
   mendekati 1 sering menunjukkan bahwa model mampu menjelaskan variasi
   target dengan lebih besar pada data evaluasi. Contohnya SVR dengan R²
   0,9207 serta beberapa model regresi pada BAREKENG dengan R² di atas
   0,98.

2. R² tidak wajib selalu mendekati 1 agar sebuah penelitian dapat
   dilaporkan. Artikel regresi linear dengan R² 0,084 tetap menyajikan
   hasil penelitian; tetapi nilai tersebut menunjukkan daya jelas model
   yang rendah.

3. R² yang tinggi tidak otomatis membuktikan model terbaik
   atau bebas kesalahan. Perlu diperiksa apakah angka tersebut berasal dari
   data training atau testing, bagaimana validasinya, serta nilai MAE dan
   RMSE.

4. Algoritma tidak dapat dipilih hanya karena namanya populer atau
   karena satu artikel memperoleh R² tinggi. Pemilihan perlu disesuaikan
   dengan karakteristik data dan dibuktikan melalui pengujian yang adil
   pada dataset yang sama.

**Kesimpulan pembuktian:** pernyataan "semakin mendekati 1, semakin
baik" dapat diterima sebagai pedoman umum untuk R², tetapi bukan aturan
mutlak yang berdiri sendiri. Nilai R² yang rendah bukan berarti hasil
hitung salah; nilai itu menunjukkan bahwa model menjelaskan variasi
target dalam porsi yang kecil.
