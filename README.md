## 📌 Overview
Project ini dibuat untuk mensimulasikan proses kerja Data Engineer dalam mengelola dan menganalisis **log transaksi sistem**. Fokus utama meliputi:

- Data preprocessing (cleaning & validation)
- Log analysis
- Evaluasi performa sistem
- Simulasi kondisi data real-world (dirty data)

Project ini juga mencerminkan transisi dari background **Quality Assurance (QA)** ke **Data Engineering**, dengan pendekatan berbasis analisis sistem dan deteksi anomali.

---

## 🎯 Objectives
- Mengubah raw log menjadi dataset terstruktur
- Mengidentifikasi data invalid dan anomali
- Melakukan analisis agregasi transaksi
- Menyediakan dataset siap pakai untuk analisis lanjutan / eksperimen

---

## 🧾 Dataset Description

### 1. Raw Transaction Log
Dataset mentah yang mensimulasikan log sistem dengan berbagai masalah umum:

- Format timestamp tidak konsisten
- Missing values (user_id, IP)
- Invalid data (amount = "abc")
- Nilai tidak logis (amount negatif / nol)
- Duplikasi transaksi

👉 Merepresentasikan kondisi **real-world system logs**

---

### 2. Cleaned Dataset
Dataset hasil preprocessing:

- Timestamp sudah distandarisasi
- Amount dikonversi ke numerik
- Data invalid dihapus
- Missing values ditangani
- Transaksi tidak valid difilter

---
### 3. Summary Analysis
Ringkasan hasil analisis:

- Total event per action (LOGIN, TRANSFER)
- Total nilai transaksi
- Insight awal performa sistem

---

## ⚙️ Data Processing Steps

### 1. Data Cleaning
- Parsing dan normalisasi timestamp
- Konversi tipe data
- Handling missing values
- Filtering data tidak valid

### 2. Data Validation
- Menghapus transaksi dengan:
  - user_id kosong
  - amount tidak valid
  - nilai negatif / tidak logis

### 3. Data Transformation
- Struktur data dibuat konsisten
- Field disiapkan untuk analisis

### 4. Data Aggregation
- Menghitung total transaksi
- Mengelompokkan berdasarkan action

---
## 🛠️ Tools & Technologies

- Python (Pandas)
- CSV (data storage)
- Jupyter Notebook (opsional untuk eksplorasi)

---
## 👤 Author

Background: Quality Assurance (QA)  
Transitioning into: Data Engineering  

Memiliki pengalaman dalam analisis sistem, validasi data, dan deteksi anomali, yang diperluas ke domain data engineering melalui pengolahan log dan data pipeline sederhana.

---

📌 1. System Activity Pattern

“Berdasarkan analisis volume transaksi per jam, terlihat adanya peningkatan aktivitas pada jam-jam tertentu yang mengindikasikan peak usage period. Hal ini dapat digunakan untuk mengidentifikasi waktu kritis dalam sistem dan kebutuhan scaling infrastructure.”

📌 2. System Reliability

“Distribusi status transaksi menunjukkan adanya proporsi kegagalan (FAILED) yang perlu diperhatikan. Error rate yang konsisten atau meningkat pada jam tertentu dapat mengindikasikan bottleneck atau overload pada sistem.”

📌 3. User Behavior Insight

“Sebagian besar pengguna mengakses sistem melalui device tertentu, yang menunjukkan dominasi platform. Hal ini penting untuk prioritas optimasi performa dan testing.”

📌 4. Transaction Pattern Analysis

“Distribusi nilai transaksi menunjukkan adanya pola normal serta kemungkinan outlier. Nilai ekstrem perlu dianalisis lebih lanjut untuk mendeteksi potensi anomali atau kesalahan sistem.”

📌 5. System Performance Issue Detection

“Error rate per jam menunjukkan fluktuasi yang dapat dikaitkan dengan beban sistem. Peningkatan error pada jam tertentu berpotensi menunjukkan keterbatasan kapasitas atau masalah performa.”
