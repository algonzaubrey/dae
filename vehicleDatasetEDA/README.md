### Proyek: Analisis dan Pembersihan Dataset Kendaraan Bekas 🚗

Notebook ini merupakan panduan lengkap untuk menganalisis dan membersihkan dataset kendaraan bekas. Tujuan utamanya adalah mempersiapkan data untuk digunakan dalam model **Machine Learning**, seperti prediksi harga mobil, dengan memastikan data yang digunakan akurat dan bebas dari anomali.

---

### Tujuan Proyek

* **Memahami Struktur Dataset**: Mengidentifikasi kolom, tipe data, dan dimensi awal dataset.
* **Pembersihan Outlier**: Menghilangkan nilai-nilai ekstrem (outlier) yang dapat memengaruhi performa model.
* **Visualisasi**: Menyajikan perubahan data secara visual sebelum dan sesudah pembersihan.
* **Laporan Profiling Otomatis**: Membuat laporan analisis data yang komprehensif dengan cepat.

---

### Rangkuman Proses dalam Notebook

#### 1. Memuat dan Memeriksa Dataset Awal
Notebook memulai dengan memuat dataset dari file CSV, menampilkan informasi dasar seperti nama kolom (`Name`, `Year`, `Selling_Price`, `Km_Driven`, `Fuel`, `Seller_Type`, `Transmission`, `Owner`), dan dimensi awal dataset.

#### 2. Pembersihan Outlier
Metode **Interquartile Range (IQR)** digunakan untuk membersihkan outlier pada dua kolom kunci: `Selling_Price` dan `Km_Driven`. Proses ini secara efektif menghapus data yang berada di luar batas wajar, menghasilkan dataset yang lebih bersih dan representatif.

#### 3. Visualisasi Perubahan Data
Sebuah **bar chart** dibuat untuk memvisualisasikan perbandingan jumlah baris data sebelum dan sesudah pembersihan outlier. Grafik ini memberikan bukti visual yang jelas tentang dampak proses pembersihan, yaitu berkurangnya jumlah data karena outlier telah dihilangkan.

#### 4. Laporan Profiling Dataset
Sebagai langkah terakhir, notebook menggunakan library **`ydata-profiling`** untuk menghasilkan laporan analisis data yang mendalam. Laporan ini mencakup statistik deskriptif, distribusi data, korelasi, dan identifikasi potensi anomali, memberikan ringkasan yang cepat dan efisien tentang dataset.

Notebook ini adalah langkah awal yang krusial dalam alur kerja Machine Learning, memastikan data yang digunakan berkualitas tinggi, yang pada gilirannya akan menghasilkan model prediktif yang lebih akurat dan dapat diandalkan.
