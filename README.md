# Proyek Machine Learning: Prediksi Telco Customer Churn

Proyek ini bertujuan untuk membangun model _Machine Learning_ yang dapat memprediksi potensi _customer churn_ (pelanggan yang berhenti berlangganan) pada perusahaan telekomunikasi. Dengan model ini, tim bisnis dapat melakukan tindakan retensi secara proaktif kepada pelanggan yang terindikasi berisiko tinggi untuk _churn_.

---

## Daftar Isi

1. [Latar Belakang & Tujuan](#-latar-belakang--tujuan)
2. [Alur Kerja (Workflow)](#-alur-kerja-workflow)
3. [Teknologi & Library](#-teknologi--library)
4. [Struktur Direktori](#-struktur-direktori)
5. [Instalasi & Cara Menjalankan Proyek](#-instalasi--cara-menjalankan-proyek)
6. [Hasil & Evaluasi](#-hasil--evaluasi)

---

## Latar Belakang & Tujuan

_Churn_ merupakan salah satu tantangan terbesar dalam industri telekomunikasi. Mempertahankan pelanggan yang ada jauh lebih efisien dibandingkan mencari pelanggan baru.

Proyek ini bertujuan untuk:

- Menganalisis faktor-faktor utama yang memengaruhi keputusan pelanggan untuk _churn_.
- Membangun model klasifikasi machine learning untuk memprediksi _churn_ secara akurat.

---

## Alur Kerja (Workflow)

Proyek ini menggunakan siklus pengembangan Machine Learning yang terstruktur sebagai berikut:

1. **Data Loading**: Memuat dataset telekomunikasi (`WA_Fn-UseC_-Telco-Customer-Churn.csv`) ke dalam Dataframe Pandas dan memeriksa ringkasan tipe data serta dimensi awal data.
2. **Data Cleaning & Transformation**:
   - Menangani nilai kosong (_missing values_) pada kolom `TotalCharges` dan mengubah tipe datanya ke numerik.
   - Menghapus atribut yang tidak relevan untuk pemodelan (seperti `customerID`).
   - Melakukan _Encoding_ variabel kategorikal (One-Hot Encoding / Label Encoding) serta konversi kolom target `Churn` menjadi variabel biner (0 dan 1).
3. **Exploratory Data Analysis (EDA)**:
   - Menganalisis distribusi target `Churn`.
   - Visualisasi hubungan antara fitur pelanggan (seperti masa berlangganan/_tenure_, _MonthlyCharges_, tipe kontrak) dengan status _churn_.
4. **Data Splitting & Feature Scaling**:
   - Membagi data menjadi data latih (_training set_) dan data uji (_testing set_) dengan rasio 80:20.
   - Melakukan _scaling_ variabel numerik menggunakan `StandardScaler`.
5. **Modelling & Evaluation**:
   - Melatih model machine learning seperti **Logistic Regression** dan **Random Forest Classifier**.
   - Mengukur performa model menggunakan _Accuracy Score_, _Confusion Matrix_, dan _Classification Report_ (Precision, Recall, F1-Score).

---

## Teknologi & Library

Proyek ini dibangun menggunakan:

- **Bahasa Pemrograman**: Python
- **Lingkungan Pengembangan (IDE)**: Visual Studio Code (VS Code) & Jupyter Notebook Extension
- **Library Utama**:
  - `pandas` & `numpy`: Manipulasi dan pembersihan data.
  - `matplotlib` & `seaborn`: Visualisasi data dan EDA.
  - `scikit-learn`: Pemisahan data, kalkulasi skala fitur, pelatihan model, dan evaluasi performa.

---

## Struktur Direktori

```text
telco-customer-churn/
│
├── WA_Fn-UseC_-Telco-Customer-Churn.csv   # Dataset Telco Customer Churn
├── Telco_Customer_Churn_Prediction.ipynb  # Notebook Jupyter utama
└── README.md                              # Dokumentasi proyek
```

---

## Instalasi & Cara Menjalankan Proyek

### Prasyarat

Pastikan Anda sudah menginstal **Python (versi 3.8+)** dan **Visual Studio Code**.

### Langkah-langkah:

1. **Clone/Unduh Repository ini** ke direktori komputer Anda.
2. **Buka folder proyek di VS Code**:
   ```bash
   code .
   ```
3. **Pastikan Ekstensi Terpasang di VS Code**:
   - Extension **Python** (`ms-python.python`)
   - Extension **Jupyter** (`ms-toolsai.jupyter`)

4. **Buat dan Aktifkan Virtual Environment** _(opsional tetapi sangat disarankan)_:

   ```bash
   # Pembuatan venv
   python -m venv venv

   # Aktivasi di Windows (PowerShell)
   .\venv\Scripts\Activate.ps1

   # Aktivasi di macOS / Linux
   source venv/bin/activate
   ```

5. **Instal Dependencies**:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```

6. **Jalankan Jupyter Notebook**:
   - Buka file `Telco_Customer_Churn_Prediction.ipynb`.
   - Pilih Kernel Python yang telah dikonfigurasi (atau _Virtual Environment_ Anda).
   - Jalankan sel kode satu per satu (_Run All_ atau `Shift + Enter`).

---

## Hasil & Evaluasi

- **Logistic Regression**: Berfungsi sebagai model _baseline_ dengan hasil akurasi sekitar **80%**, sangat baik dalam mengidentifikasi pola umum dan hubungan linier antar fitur.

- **Random Forest Classifier**: Menghasilkan akurasi mendekati **78-79%**, memberikan wawasan mengenai _feature importance_ (fitur paling berpengaruh terhadap _churn_, seperti `tenure` dan `Contract_Month-to-month`).
