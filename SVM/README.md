# Support Vector Machine: Klasifikasi dan Regresi

Proyek ini berisi notebook Jupyter untuk mempelajari penerapan **Support Vector Machine (SVM)** menggunakan Python dan scikit-learn. Contohnya mencakup klasifikasi biner dengan SVC serta regresi dengan SVR.

## Daftar isi

- [Isi proyek](#isi-proyek)
- [Dataset](#dataset)
- [Persyaratan](#persyaratan)
- [Menjalankan proyek](#menjalankan-proyek)
- [Ringkasan metode](#ringkasan-metode)
- [Contoh hasil SVR](#contoh-hasil-svr)
- [Catatan](#catatan)

## Isi proyek

| File | Deskripsi |
| --- | --- |
| `SVMklasifikasi.ipynb` | Contoh klasifikasi menggunakan **SVC (Support Vector Classification)** pada data diabetes. Notebook menyiapkan fitur dan label, melakukan standardisasi, membagi data latih dan data uji, melatih model, lalu memeriksa skor model. |
| `SklearnSVR.ipynb` | Demonstrasi dasar **SVR (Support Vector Regression)** pada data gaji. Model dilatih dengan kernel RBF dan hasilnya divisualisasikan. |
| `SVMRegresi.ipynb` | Alur SVR yang lebih lengkap untuk memprediksi gaji dari lama pengalaman kerja. Mencakup pembagian data latih/uji, standardisasi fitur dan target, evaluasi metrik, visualisasi, dan contoh prediksi. |
| `diabetes.csv` | Dataset untuk contoh klasifikasi. |
| `Salary_Data.csv` | Dataset untuk contoh regresi gaji. |

## Dataset

### `diabetes.csv`

Dataset ini memiliki 768 baris dan 9 kolom. Delapan kolom pertama digunakan sebagai fitur:

- `fiPregnancies`
- `Glucose`
- `BloodPressure`
- `SkinThickness`
- `Insulin`
- `BMI`
- `DiabetesPedigreeFunction`
- `Age`

Kolom `Outcome` merupakan label klasifikasi biner.

### `Salary_Data.csv`

Dataset ini memiliki 30 baris dan dua kolom:

- `YearsExperience`: lama pengalaman kerja dalam tahun.
- `Salary`: nilai gaji yang diprediksi.

## Persyaratan

- Python 3
- Jupyter Notebook atau Visual Studio Code dengan ekstensi Jupyter
- Paket Python: `numpy`, `pandas`, `matplotlib`, dan `scikit-learn`

## Menjalankan proyek

1. Clone repository, lalu pindah ke folder proyek:

   ```bash
   git clone <URL-REPOSITORY>
   cd SVM
   ```

2. Buat dan aktifkan virtual environment (disarankan).

   **Windows PowerShell:**

   ```powershell
   python -m venv .venv
   .venv\Scripts\Activate.ps1
   ```

   **macOS/Linux:**

   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```

3. Instal dependensi:

   ```bash
   python -m pip install numpy pandas matplotlib scikit-learn jupyter
   ```

4. Jalankan Jupyter:

   ```bash
   jupyter notebook
   ```

   Buka salah satu file `.ipynb` dari browser atau buka repository di VS Code dan pilih kernel Python dari virtual environment.

5. Jalankan cell notebook secara berurutan. Pastikan file CSV berada di folder yang sama dengan notebook, karena notebook membacanya menggunakan nama file relatif.

## Ringkasan metode

### Klasifikasi dengan SVC

SVC digunakan ketika target berupa kelas, seperti nilai `Outcome` pada dataset diabetes. Notebook klasifikasi menstandardisasi fitur, membagi data menjadi data latih dan data uji, kemudian melatih model SVC.

### Regresi dengan SVR

SVR digunakan ketika target berupa nilai numerik kontinu, seperti `Salary`. Notebook `SVMRegresi.ipynb` menggunakan kernel RBF agar model dapat menangkap hubungan nonlinier. Fitur dan target distandardisasi; scaler dipelajari dari data latih, kemudian digunakan untuk mentransformasi data uji. Hasil prediksi target dikembalikan ke skala gaji asli sebelum evaluasi.

Metrik yang ditampilkan:

- **MAE**: rata-rata besar selisih absolut prediksi dengan nilai aktual.
- **RMSE**: akar rata-rata kuadrat error; lebih sensitif terhadap error besar.
- **R²**: ukuran seberapa baik model menjelaskan variasi target pada data uji.

## Contoh hasil SVR

Dengan pembagian data uji 20% dan `random_state=42` pada `SVMRegresi.ipynb`, contoh hasilnya:

| Metrik | Nilai |
| --- | ---: |
| MAE | 5.994,69 |
| RMSE | 7.343,23 |
| R² | 0,8944 |

Nilai tersebut adalah hasil pada dataset dan konfigurasi yang tersedia saat ini. Hasil dapat berubah jika data atau parameter model diubah.

## Catatan

- Proyek ini ditujukan untuk pembelajaran dan demonstrasi machine learning, bukan untuk penggunaan klinis atau pengambilan keputusan medis.
- Hasil model bergantung pada data dan parameter. Nilai metrik bukan jaminan performa pada data lain.
- Notebook `SklearnSVR.ipynb` merupakan contoh dasar yang melatih dan memvisualisasikan model pada seluruh dataset. Untuk evaluasi prediksi pada data yang tidak digunakan saat pelatihan, gunakan alur pemisahan train/test di `SVMRegresi.ipynb`.
- Pada `SVMklasifikasi.ipynb`, scaler saat ini dipasang sebelum pembagian train/test. Untuk menghindari kebocoran informasi dari data uji, pendekatan yang lebih tepat adalah memasang scaler hanya pada data latih lalu menerapkannya ke data uji.
