# Customer Personality Analysis - Unsupervised Learning

Proyek ini merupakan implementasi **Unsupervised Learning** menggunakan algoritma **K-Means Clustering** untuk melakukan segmentasi pelanggan berdasarkan karakteristik dan perilaku pembelian pelanggan.

Notebook ini dibuat menggunakan Google Colab / Jupyter Notebook sebagai bagian dari tugas mata kuliah Data Science.

---

## Informasi Penulis

- **Nama:** Muhammad Zidan  
- **NIM:** 054872864  
- **Program Studi:** Data Science  
- **UPBJJ:** UT Palembang  

---

## Deskripsi Proyek

Tujuan utama proyek ini adalah melakukan analisis segmentasi pelanggan menggunakan teknik clustering agar perusahaan dapat memahami karakteristik pelanggan dengan lebih baik.

Metode yang digunakan:

- Data Preprocessing
- Missing Value Imputation
- One-Hot Encoding
- Feature Scaling
- K-Means Clustering
- Elbow Method
- Silhouette Score
- PCA (Principal Component Analysis)

Hasil clustering digunakan untuk:
- Mengidentifikasi kelompok pelanggan
- Memahami pola perilaku pembelian
- Membantu strategi pemasaran yang lebih tepat sasaran

---

## Dataset

Dataset yang digunakan adalah **Customer Personality Analysis**.

Dataset berisi informasi mengenai:
- Demografi pelanggan
- Pendapatan pelanggan
- Status pernikahan
- Tingkat pendidikan
- Pengeluaran produk
- Respons terhadap kampanye pemasaran

Contoh fitur:
- `Income`
- `Year_Birth`
- `Education`
- `Marital_Status`
- `MntWines`
- `MntMeatProducts`
- `NumWebPurchases`
- dan lainnya

File dataset yang digunakan:
```bash
cpa.csv
```

---

## Library yang Digunakan

Berikut beberapa library Python yang digunakan:

```python
pandas
numpy
scikit-learn
matplotlib
seaborn
```

Instalasi library:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

---

## Struktur Analisis

### 1. Load Dataset
Dataset dibaca menggunakan `pandas.read_csv()` dengan separator tab (`\t`).

### 2. Exploratory Data Analysis (EDA)
Dilakukan eksplorasi awal untuk:
- Melihat struktur data
- Mengecek tipe data
- Mengidentifikasi missing value
- Visualisasi distribusi data

### 3. Identifikasi Fitur Numerik dan Kategorikal
Kolom dipisahkan menjadi:
- Fitur numerik
- Fitur kategorikal

### 4. Penanganan Missing Value
Missing value pada kolom numerik diisi menggunakan:
- **Median**

### 5. Encoding Fitur Kategorikal
Kolom kategorikal:
- `Education`
- `Marital_Status`

diubah menggunakan:
- **One-Hot Encoding**

### 6. Feature Scaling
Dilakukan normalisasi data menggunakan:
- `StandardScaler`

### 7. Menentukan Jumlah Cluster Optimal
Metode yang digunakan:
- Elbow Method
- Silhouette Score

Hasil analisis menunjukkan:
- Nilai cluster optimal = **2**

### 8. Clustering dengan K-Means
Model clustering dibangun menggunakan:
```python
KMeans(n_clusters=2)
```

### 9. Visualisasi Cluster
Visualisasi dilakukan menggunakan:
- PCA 2D Projection
- Scatter Plot

### 10. Cluster Profiling
Dilakukan analisis rata-rata fitur pada setiap cluster untuk memahami karakteristik pelanggan.

---

## Hasil Analisis

Berdasarkan hasil clustering:

### Cluster 0
Karakteristik umum:
- Pendapatan lebih rendah
- Pengeluaran produk lebih rendah
- Aktivitas pembelian lebih sedikit

### Cluster 1
Karakteristik umum:
- Pendapatan lebih tinggi
- Pengeluaran produk lebih besar
- Lebih aktif dalam pembelian

---

## Insight Bisnis

Hasil segmentasi pelanggan dapat digunakan untuk:

- Menentukan strategi pemasaran yang berbeda untuk tiap segmen
- Menargetkan pelanggan potensial dengan promosi khusus
- Mengoptimalkan campaign marketing
- Meningkatkan loyalitas pelanggan

---

## Visualisasi yang Dihasilkan

Notebook menghasilkan beberapa visualisasi seperti:
- Distribusi fitur numerik
- Elbow Method Plot
- Silhouette Score Plot
- PCA Cluster Visualization

---

## Cara Menjalankan Project

1. Clone repository atau download file notebook
2. Pastikan dataset `cpa.csv` tersedia
3. Jalankan notebook secara berurutan

Menjalankan notebook:

```bash
jupyter notebook
```

atau gunakan Google Colab.

---

## Kesimpulan

Project ini berhasil menerapkan metode Unsupervised Learning menggunakan K-Means Clustering untuk melakukan segmentasi pelanggan berdasarkan pola perilaku dan karakteristik pelanggan.

Hasil clustering menunjukkan adanya dua kelompok pelanggan utama dengan karakteristik yang berbeda, sehingga dapat digunakan sebagai dasar pengambilan keputusan bisnis dan strategi pemasaran yang lebih efektif.

---

## Lisensi

Project ini dibuat untuk keperluan pembelajaran dan tugas akademik.
