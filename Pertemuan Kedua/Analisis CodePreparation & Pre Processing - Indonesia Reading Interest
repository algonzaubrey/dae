# Analisis Pra-pemrosesan Data: Minat Baca di Indonesia (2020-2023)

Repositori ini berisi *notebook* Jupyter yang melakukan persiapan dan pra-pemrosesan data pada dataset "Indonesia Reading Interest 2020-2023". Tujuan utamanya adalah membersihkan data mentah agar siap digunakan untuk analisis lebih lanjut atau sebagai input untuk model *machine learning*.

## Alur Pra-pemrosesan Data

Proses yang dilakukan dalam *notebook* ini dibagi menjadi beberapa tahap utama:

### 1. Impor Pustaka (Libraries)
Kode mengimpor pustaka standar untuk analisis data dan visualisasi:
- **pandas**: Untuk manipulasi dan analisis data dalam bentuk DataFrame.
- **numpy**: Untuk operasi numerik.
- **matplotlib & seaborn**: Untuk membuat visualisasi data.
- **sklearn.preprocessing.MinMaxScaler**: Untuk melakukan normalisasi data.

### 2. Eksplorasi Data Awal
Tahap ini bertujuan untuk memahami struktur awal dataset:
- **Membaca Data**: Dataset `TGM 2020-2023_eng.csv` dimuat menggunakan `pd.read_csv()` dengan separator titik koma (`;`).
- **Pemeriksaan Awal**:
  - `df.info()`: Menunjukkan bahwa beberapa kolom numerik terbaca sebagai tipe `object` karena penggunaan koma (`,`) sebagai pemisah desimal.
  - `df.isnull().sum()`: Mengidentifikasi adanya **35 data yang hilang** di kolom terkait frekuensi dan durasi akses internet.

### 3. Pembersihan Data (Data Cleaning)
Ini adalah langkah inti untuk memperbaiki data yang "kotor":
- **Penanganan Duplikat**: Kode memastikan tidak ada baris data yang duplikat. Hasil pemeriksaan menunjukkan **tidak ada duplikat**.
- **Koreksi Tipe Data**: Karakter koma (`,`) pada kolom numerik diganti dengan titik (`.`) agar tipe datanya dapat diubah menjadi numerik.
- **Penanganan Data Hilang (_Missing Values_)**:
  - Kolom **numerik** yang kosong diisi dengan nilai **median** dari kolom tersebut untuk menghindari bias dari nilai ekstrem.
  - Kolom **kategorikal** yang kosong diisi dengan nilai **modus** (nilai yang paling sering muncul).

### 4. Penanganan Nilai Ekstrem (Outliers)
*Outlier* yang dapat memengaruhi hasil analisis dideteksi dan dihapus.
- **Metode IQR**: Deteksi *outlier* dilakukan menggunakan metode *Interquartile Range* (IQR).
- **Hasil**: Proses ini mengurangi jumlah data dari 140 baris menjadi **77 baris**, menandakan bahwa cukup banyak *outlier* yang berhasil diidentifikasi dan dihilangkan.

### 5. Normalisasi Data
Setelah data bersih dari *outlier*, semua fitur numerik diskalakan agar memiliki rentang yang seragam.
- **MinMaxScaler**: Digunakan untuk mengubah skala nilai pada semua kolom numerik ke dalam rentang **[0, 1]**. Langkah ini penting agar fitur dengan rentang nilai yang besar tidak mendominasi proses analisis atau pemodelan.

### 6. Visualisasi
Untuk memvalidasi setiap tahapan, distribusi kolom `Tingkat Kegemaran Membaca (Reading Interest)` divisualisasikan pada tiga kondisi:
1. Sebelum pembersihan.
2. Setelah penghapusan *outlier*.
3. Setelah normalisasi.

### Hasil Akhir
Kode ini menghasilkan dua file CSV baru yang siap digunakan:
1.  `TGM_2020-2023_cleaned.csv`: Data yang sudah bersih dari *outlier* (belum dinormalisasi).
2.  `TGM_2020-2023_normalized.csv`: Data bersih yang sudah dinormalisasi.

---
*Analisis ini dibuat berdasarkan eksekusi kode pada notebook `Preparation_&_Pre_Processing_Indonesia_Reading_Interest.ipynb`.*
