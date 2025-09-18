# Analisis Eksplorasi Dataset Titanic

Proyek ini bertujuan untuk melakukan analisis eksploratif (EDA) dan visualisasi pada *dataset* Titanic yang populer, dimuat menggunakan *library* `seaborn`. Fokus analisis ini adalah untuk mengidentifikasi sebaran nilai, menemukan data yang hilang (*missing values*), dan mengungkap pola tersembunyi dari fitur-fitur kunci seperti usia, kelas penumpang, gender, dan tingkat kelangsungan hidup.

---

## Tahapan Analisis

### 1. Pemeriksaan Awal Data
* Melihat sampel data teratas untuk mendapatkan gambaran umum.
* Memeriksa tipe data setiap kolom dan jumlah nilai non-null.
* Menghitung total data kosong untuk setiap fitur.
* Mendapatkan ringkasan statistik (rata-rata, standar deviasi, kuartil) untuk data numerik.

### 2. Visualisasi Variabel Numerik
* Menggunakan **Boxplot** untuk mendeteksi sebaran dan *outlier* pada seluruh data numerik.
* Menganalisis **distribusi Usia dan Tarif** dengan *histogram* untuk melihat frekuensi dan bentuk sebaran data.

### 3. Visualisasi Variabel Kategorikal
* Menyelidiki sebaran **Kelas Penumpang** (`class`/`pclass`) melalui perbandingan *histogram* dan *pie chart*.
* Memetakan asal **Titik Keberangkatan** (`embark_town`) untuk melihat dari mana mayoritas penumpang berasal.
* Menghitung proporsi **Kategori Penumpang** (`who`: pria, wanita, anak) di atas kapal.
* Membandingkan distribusi **Usia berdasarkan Gender** menggunakan *violinplot*.
* Menganalisis kaitan antara **Gender dan Keselamatan** dengan *violinplot* untuk melihat pola *survival*.

### 4. Analisis Proporsi
* Menampilkan **proporsi data kategorikal** (`embark_town`, `who`, `class`) dalam bentuk **Pie Chart** untuk visualisasi persentase yang lebih intuitif.

---

## Temuan Utama dan Wawasan

* Sebaran **usia** penumpang terpusat pada kelompok dewasa muda.
* Data **tarif (fare)** sangat miring ke kanan (*right-skewed*), menandakan adanya beberapa harga tiket yang ekstrim (*outlier*).
* **Southampton** menjadi pelabuhan keberangkatan bagi sebagian besar penumpang.
* Jumlah penumpang **pria dewasa** secara signifikan lebih banyak daripada penumpang wanita dan anak-anak.
* **Gender** terbukti menjadi salah satu faktor kuat yang memengaruhi tingkat keselamatan (*survival*).
* **Kelas sosial** penumpang tidak hanya menentukan jumlah penumpangnya, tetapi juga berkorelasi dengan peluang mereka untuk selamat.
