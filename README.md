# Analisis Performa Model Linear Regression dan SVM dalam Prediksi Harga Saham BBCA

### **Deskripsi Proyek**

Proyek ini bertujuan untuk memprediksi harga saham PT Bank Central Asia Tbk (BBCA) menggunakan dua metode model prediksi: **Linear Regression** dan **Support Vector Machine (SVM)**. Dataset yang digunakan mencakup harga saham BBCA dari tanggal 1 Juni 2022 hingga 1 Juni 2025. Evaluasi dilakukan untuk membandingkan akurasi antara kedua model berdasarkan metrik seperti **MAE**, **RMSE**, **MAPE**, dan **R²**.

### **Persyaratan**

* **Python**
* **Library yang diperlukan:**

  * yfinance
  * pandas
  * matplotlib
  * scikit-learn
  * numpy
    
### **Langkah-langkah:**

1. **Pengumpulan Data:**

   * Data harga saham BBCA diambil menggunakan library `yfinance`, dengan rentang waktu dari **1 Juni 2022** hingga **1 Juni 2025**. Data yang diambil mencakup harga **Open**, **High**, **Low**, **Close**, dan **Volume**.

2. **Preprocessing Data:**

   * Data yang diambil disusun dan diolah untuk membuat **lag features** yang mencakup harga penutupan saham pada waktu t-1, t-2, dan t-3.
   * Data kemudian dinormalisasi menggunakan `StandardScaler` untuk mempersiapkan model.

3. **Pembagian Data:**

   * Data dibagi menjadi dua bagian: **Data Pelatihan (80%)** dan **Data Pengujian (20%)**. Pembagian dilakukan tanpa pengacakan untuk menjaga urutan waktu dalam prediksi harga saham.

4. **Modeling:**

   * Dua model digunakan:

     * **Linear Regression** untuk memprediksi harga saham berdasarkan hubungan linier antar variabel.
     * **Support Vector Machine (SVM)** yang lebih kompleks, menggunakan kernel RBF untuk menangani pola non-linier pada data.

5. **Evaluasi Model:**

   * Evaluasi dilakukan dengan menggunakan metrik:

     * **MAE (Mean Absolute Error)**
     * **RMSE (Root Mean Squared Error)**
     * **MAPE (Mean Absolute Percentage Error)**
     * **R² (Koefisien Determinasi)**
   * Hasil menunjukkan bahwa **Linear Regression** lebih baik dalam hal **MAE** dan **RMSE**, sementara **SVM** menunjukkan performa sedikit lebih unggul dalam beberapa titik data.

6. **Visualisasi:**

   * Beberapa visualisasi digunakan untuk menunjukkan data harga saham, distribusi harga, pembagian data pelatihan dan pengujian, serta perbandingan prediksi antara kedua model.

### **Hasil Analisis**

* **Linear Regression** memberikan prediksi yang lebih akurat dan konsisten, terutama pada data dengan pergerakan harga yang stabil dan linier.
* **SVM (Tuned)** lebih responsif terhadap fluktuasi harga, tetapi tidak selalu lebih akurat pada data dengan pola linier.
* Evaluasi metrik menunjukkan bahwa **Linear Regression** lebih baik dalam menjelaskan variasi data (R²), namun **SVM** sedikit lebih unggul pada beberapa titik data.

### **Visualisasi:**

1. **Grafik Harga Penutupan Saham BBCA** - Menampilkan tren harga saham BBCA selama periode pengambilan data.
2. **Distribusi Harga Penutupan** - Memvisualisasikan distribusi harga saham BBCA.
3. **Perbandingan Prediksi Linear Regression dan SVM** - Menampilkan perbandingan antara harga aktual dan prediksi untuk kedua model.
4. **Pembagian Data Pelatihan dan Pengujian** - Visualisasi pembagian data menjadi pelatihan dan pengujian.
