## 🎯 Tujuan Analisis

Tujuan utama dari analisis ini adalah untuk memahami karakteristik mendalam dari dataset yang digunakan. Analisis ini berfokus pada:

- **Distribusi Nilai:** Mengamati persebaran data pada fitur-fitur penting.
- **Identifikasi Outlier:** Mendeteksi nilai-nilai ekstrem yang dapat memengaruhi interpretasi.
- **Dasar Rule Engine:** Memberikan gambaran pola data untuk mendukung proses penalaran dalam pembuatan **sistem rule engine manual**.

Dengan memahami pola dasar ini, proses pembuatan aturan menjadi lebih terarah dan akurat dalam merepresentasikan kondisi data, tanpa bergantung pada model machine learning seperti KNN.

---

## 💡 Insight Utama dari Analisis Dataset

Berdasarkan eksplorasi data yang dilakukan, berikut adalah temuan kuncinya:

### 1. Pola Distribusi & Skewness
- **Variasi Pola:** Setiap fitur menunjukkan pola distribusi yang unik.
- **Keseimbangan Data:** Beberapa fitur memiliki nilai *mean* dan *median* yang berdekatan, menandakan distribusi yang relatif seimbang.
- **Indikasi Skewness:** Pada fitur lain, terdapat celah signifikan antara *mean* dan *median*, yang mengindikasikan ketidaksimetrisan (skewness) persebaran data.
- **Modus:** Munculnya nilai modus yang berulang menunjukkan adanya kecenderungan data untuk berkumpul pada nilai tertentu (pola alami populasi).

### 2. Deteksi Outlier (Metode IQR)
- **Keberadaan Outlier:** Sejumlah data terdeteksi berada jauh di luar rentang normal.
- **Sebaran Outlier:** Nilai ekstrem ini tidak hanya muncul pada fitur yang terlihat fluktuatif, tetapi juga pada fitur yang sekilas tampak stabil.
- **Dampak:** Keberadaan outlier ini krusial karena dapat memengaruhi akurasi pengambilan keputusan dalam *rule engine*. Temuan ini membantu menentukan strategi penanganan data (apakah perlu dibersihkan atau dijadikan aturan khusus).

### 3. Kesimpulan Akhir
Dataset memiliki **keragaman pola yang signifikan**. Pemahaman terhadap nilai pemusatan (central tendency), bentuk distribusi, dan outlier adalah langkah prasyarat yang vital sebelum menyusun aturan manual. Hal ini memastikan alur analisis lebih presisi dan hasil yang dapat dipertanggungjawabkan.
