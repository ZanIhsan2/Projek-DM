# 🚀 Smart Waste: Optimasi Pemetaan Bank Sampah Berbasis Kelurahan

Proyek ini bertujuan untuk mendukung program **Zero Waste City** di Kecamatan Cibeunying Kidul, Kota Bandung, dengan memanfaatkan teknik *Data Mining* untuk memetakan tingkat partisipasi bank sampah di setiap kelurahan.

## 📌 Ringkasan Eksekutif
Dalam kerangka **Smart City (Smart Environment)**, pengelolaan data sampah yang tersebar seringkali tidak terorganisir. Proyek ini menggunakan algoritma **K-Means Clustering** untuk mengelompokkan wilayah berdasarkan tiga metrik utama:
* **Total Unit:** Kuantitas bank sampah yang tersedia.
* **Durasi Operasional:** Loyalitas dan keberlanjutan program (dalam tahun).
* **Aktualitas Data:** Tahun terakhir aktivitas tercatat.

## 🛠️ Metodologi (CRISP-DM)
Proyek ini mengikuti standar industri **CRISP-DM**:
1.  **Business Understanding:** Mengidentifikasi kebutuhan pemetaan wilayah untuk intervensi kebijakan lingkungan.
2.  **Data Preparation:** Agregasi data mentah (281 baris) menjadi fitur numerik berbasis kelurahan (6 baris).
3.  **Modeling:** Implementasi K-Means dengan evaluasi *Elbow Method* untuk menentukan jumlah klaster optimal ($k=3$).
4.  **Evaluation:** Validasi model menggunakan *Silhouette Score* (Skor: **0.5475**), yang menunjukkan struktur klaster yang kuat.

## 📊 Hasil Analisis (Profiling Klaster)
Berdasarkan visualisasi 3D, wilayah dikategorikan menjadi:

| Cluster | Kategori | Profiling |
| :--- | :--- | :--- |
| **Cluster 2** | **Mandiri** | Kelurahan dengan unit terbanyak dan operasional paling stabil (**Role Model**). |
| **Cluster 0** | **Berkembang** | Wilayah dengan partisipasi sedang yang memerlukan dorongan ekspansi. |
| **Cluster 1** | **Rintisan** | Wilayah dengan partisipasi rendah yang menjadi prioritas utama edukasi dan bantuan. |

## 📈 Visualisasi Model
Proyek ini menyertakan evaluasi model yang komprehensif untuk memastikan akurasi pengelompokan:
* **Elbow Method:** Penentuan jumlah klaster terbaik melalui analisis inersia.
* **Silhouette Plot:** Pengukuran kualitas pemisahan dan kerapatan antar klaster.
* **3D Projection Scatter Plot:** Representasi spasial klasifikasi kelurahan dengan garis proyeksi untuk mempermudah interpretasi data multidimensi.

## 🚀 Cara Menjalankan
Silakan ikuti langkah-langkah berikut untuk menjalankan analisis di lingkungan lokal Anda:

```bash
# 1. Clone repository
git clone [https://github.com/username/smart-waste-clustering.git](https://github.com/username/smart-waste-clustering.git)

# 2. Masuk ke direktori
cd smart-waste-clustering

# 3. Install dependensi yang diperlukan
pip install pandas scikit-learn matplotlib seaborn

# 4. Jalankan analisis (Jupyter Notebook)
jupyter notebook testing.ipynb