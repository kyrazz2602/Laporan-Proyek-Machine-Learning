# Laporan Proyek Machine Learning - Arizal Anshori

## Domain Proyek

Telekomunikasi merupakan salah satu bidang yang terus berkembang pesat seiring dengan kemajuan teknologi. Dalam era digital saat ini, jumlah data yang dihasilkan oleh jaringan telekomunikasi meningkat secara eksponensial. Data tersebut berasal dari berbagai sumber seperti data penggunaan pelanggan, log jaringan, serta data layanan pelanggan. Hal ini menciptakan tantangan besar dalam mengelola, menganalisis, dan memanfaatkan data untuk meningkatkan efisiensi jaringan, pengalaman pelanggan, dan kualitas layanan.

Machine Learning (ML) dan Deep Learning (DL) menawarkan solusi yang revolusioner dalam menangani tantangan-tantangan tersebut. Teknologi ini memungkinkan sistem untuk belajar dari data historis, mengenali pola-pola tertentu, dan membuat prediksi atau keputusan otomatis yang relevan. Misalnya, ML dapat digunakan untuk memprediksi gangguan jaringan, mendeteksi penipuan (fraud detection), atau meningkatkan alokasi sumber daya jaringan.

Dalam konteks pengalaman pelanggan, perusahaan telekomunikasi menghadapi tantangan untuk memahami kebutuhan pelanggan secara individu agar dapat memberikan layanan yang personal. Pelanggan cenderung memiliki ekspektasi tinggi terhadap layanan yang mereka terima, termasuk layanan yang disesuaikan dengan preferensi mereka. Selain itu, churn pelanggan atau perpindahan pelanggan ke penyedia layanan lain menjadi salah satu ancaman besar yang dihadapi industri ini. Oleh karena itu, pengelolaan hubungan pelanggan yang efektif menjadi kunci dalam mempertahankan loyalitas pelanggan dan meningkatkan pendapatan perusahaan.

Machine Learning dapat digunakan untuk menyelesaikan berbagai masalah terkait pengalaman pelanggan seperti:

1.  Prediksi Churn Pelanggan: Mengidentifikasi pelanggan yang kemungkinan besar akan meninggalkan layanan perusahaan agar dapat diambil tindakan preventif.

2.  Segmentasi Pelanggan: Mengelompokkan pelanggan berdasarkan perilaku, preferensi, atau pola penggunaan mereka untuk memberikan penawaran yang relevan.

3.  Prediksi Nilai Umur Pelanggan (Customer Lifetime Value): Memperkirakan nilai pelanggan dalam jangka panjang untuk membantu perusahaan dalam membuat keputusan strategis, seperti alokasi anggaran pemasaran atau desain program loyalitas.

Studi oleh Mishra et al. (2022) menunjukkan bahwa segmentasi pelanggan berbasis ML dapat meningkatkan efektivitas kampanye pemasaran hingga 25%. Selain itu, implementasi model prediksi churn pelanggan berbasis algoritma gradient boosting telah terbukti meningkatkan tingkat retensi pelanggan sebesar 20%.

Dengan memanfaatkan kekuatan ML dan DL, perusahaan telekomunikasi dapat menciptakan strategi yang lebih proaktif, efisien, dan terpersonalisasi untuk memenuhi kebutuhan pelanggan serta meningkatkan kepuasan mereka.

**Referensi:**

Chen, Y., et al. (2021). "Deep Learning for Network Management: Techniques and Applications." IEEE Communications Surveys & Tutorials. DOI: 10.1109/COMST.2021.3057800.

Zhang, X., et al. (2020). "Machine Learning for Telecom Networks: A Comprehensive Survey." IEEE Access. DOI: 10.1109/ACCESS.2020.2978494.

Mishra, R., et al. (2022). "Customer Segmentation in Telecom Industry Using Machine Learning." Journal of Big Data. DOI: 10.1186/s40537-022-00512-3.

## Business Understanding

### Problem Clarification

**Problem Statements**

1.  **Churn Pelanggan:** Perusahaan telekomunikasi sering kali kehilangan pelanggan karena perpindahan mereka ke penyedia layanan lain. Hal ini dapat terjadi karena kurangnya personalisasi layanan, pengalaman buruk, atau penawaran yang lebih menarik dari kompetitor.

**Goals**

  **Meningkatkan Tingkat Retensi Pelanggan:**

  Mengidentifikasi pelanggan yang kemungkinan besar akan churn sehingga dapat dilakukan tindakan preventif, seperti memberikan insentif atau meningkatkan kualitas layanan.

### Solution Statement

Untuk mencapai tujuan meningkatkan pengalaman pelanggan, berikut adalah beberapa solusi yang dapat diimplementasikan:

**1. Prediksi Churn Pelanggan dengan Model Klasifikasi**

**Algoritma yang Digunakan:**

  *   Gradient Boosting (misalnya, XGBoost atau LightGBM) untuk baseline model.

  *   Neural Network sederhana untuk mengeksplorasi performa model berbasis deep learning.

**Langkah Implementasi:**

  *   Mengumpulkan dan membersihkan data churn dari dataset seperti Telecom Churn Dataset.

  *   Melakukan eksplorasi data untuk memahami pola churn.

  *   Melatih model klasifikasi menggunakan data historis.

  *   Mengevaluasi model menggunakan metrik seperti AUC-ROC, akurasi, dan recall untuk mengukur kemampuan model dalam mendeteksi pelanggan yang berpotensi churn.

**Improvement:**

  *   Melakukan hyperparameter tuning pada model Gradient Boosting untuk meningkatkan performa.

  * Menggunakan teknik ensemble learning untuk menggabungkan prediksi beberapa model.

Dengan mengimplementasikan solusi ini, perusahaan telekomunikasi dapat meningkatkan loyalitas pelanggan, mengurangi tingkat churn, dan memaksimalkan nilai bisnis dari setiap pelanggan.

## Data Understanding

**[Link Sumber Dataset (Kaggle)](https://www.kaggle.com/datasets/suraj520/telecom-churn-dataset)**  

**Deskripsi Dataset**  
Dataset ini berisi **243.553 baris** data pelanggan dari empat mitra telekomunikasi besar di India: Airtel, Reliance Jio, Vodafone, dan BSNL. Dataset mencakup berbagai variabel demografi, lokasi, pola penggunaan, serta variabel biner yang menunjukkan apakah pelanggan telah churn (berhenti menggunakan layanan) atau tidak.  

---

**Variabel dalam Dataset**  

1. **customer_id**: Identitas unik untuk setiap pelanggan.  
2. **telecom_partner**: Nama mitra telekomunikasi pelanggan.  
3. **gender**: Jenis kelamin pelanggan.  
4. **age**: Usia pelanggan.  
5. **state**: Negara bagian tempat pelanggan tinggal.  
6. **city**: Kota tempat pelanggan tinggal.  
7. **pincode**: Kode pos lokasi pelanggan.  
8. **date_of_registration**: Tanggal registrasi pelanggan dengan mitra telekomunikasi.  
9. **num_dependents**: Jumlah tanggungan (misalnya, anak-anak) dari pelanggan.  
10. **estimated_salary**: Estimasi gaji pelanggan.  
11. **calls_made**: Jumlah panggilan yang dilakukan oleh pelanggan.  
12. **sms_sent**: Jumlah SMS yang dikirim oleh pelanggan.  
13. **data_used**: Jumlah data yang digunakan oleh pelanggan.  
14. **churn**: Variabel biner yang menunjukkan apakah pelanggan churn (1 = churn, 0 = tidak churn).  

---

### **Hasil Identifikasi Data**  

1. **Jumlah Data**  
   - **Baris**: 243.553  
   - **Kolom**: 14  

2. **Kondisi Data**  
   - **Missing Value**:  
     Beberapa kolom mungkin memiliki nilai yang hilang. Perlu dilakukan eksplorasi untuk menentukan jumlah dan proporsi missing value.  
   - **Data Duplikat**:  
     Perlu diperiksa apakah terdapat data yang terduplikasi pada kolom `customer_id` atau kombinasi variabel lainnya.  
   - **Outlier**:  
     Beberapa fitur numerik seperti `age`, `estimated_salary`, `calls_made`, dan `data_used` mungkin memiliki nilai outlier yang memengaruhi hasil analisis.  

3. **Uraian Fitur pada Data**  
   Semua fitur mencakup informasi yang relevan untuk analisis churn pelanggan. Fitur seperti **`calls_made`**, **`sms_sent`**, dan **`data_used`** sangat penting untuk memahami pola penggunaan layanan pelanggan, sedangkan variabel demografi seperti **`gender`**, **`age`**, dan **`num_dependents`** dapat membantu mengidentifikasi kelompok pelanggan yang lebih rentan untuk churn.  

**Kesimpulan**:  
Dataset ini siap untuk diproses lebih lanjut setelah memastikan tidak ada missing value, duplikasi, atau outlier yang signifikan yang memengaruhi kualitas data.

## Data Preparation

---

### **1. Pembersihan Data (Data Cleaning)**

#### **a. Menghapus Baris Duplikat**
```python
df.drop_duplicates(inplace=True)
```
…4. Fitur numerik telah distandarisasi.
5. Dataset telah dibagi menjadi data training dan testing.
6. Data training telah diseimbangkan menggunakan SMOTE.

## Modeling
### **Algoritma yang Digunakan**
#### **Gradient Boosting (XGBoost/LightGBM)**
- **Cara Kerja**:  
  Membangun ensemble pohon keputusan secara bertahap. Setiap pohon dikoreksi kesalahan prediksi pohon sebelumnya. Dilatih dengan teknik *boosting* untuk mengurangi bias.
- **Parameter Awal**:
  - `n_estimators=100` (jumlah pohon).
  - `learning_rate=1.0` (tingkat pembelajaran).
  - `max_depth=6` (kedalaman maksimum pohon).
- **Hyperparameter Tuning**:
  - **Grid Search** dengan kombinasi:
    - `n_estimators`: [100], `learning_rate`: [1.0], `max_depth`: [3], `subsample`: [0.8].
  - **Parameter Terbaik**:  
    `{'max_depth': 3, 'n_estimators': 100, 'learning_rate': 1.0, 'subsample': 0.8}`.

#### **Neural Network**
- **Cara Kerja**:  
  Jaringan saraf tiruan dengan satu lapisan tersembunyi (100 neuron). Menggunakan aktivasi ReLU dan optimasi Adam.
- **Parameter**:
  - `hidden_layer_sizes=(100,)` (1 lapisan tersembunyi dengan 100 neuron).
  - `max_iter=500` (iterasi maksimum pelatihan).


Parameter `GridSearchCV` yang digunakan sebagai berikut:

```python
grid_search_gb = GridSearchCV(
    estimator=gb_model,         # Model yang akan dioptimalkan (Gradient Boosting model)
    param_grid=param_grid_gb,   # Grid parameter yang akan dieksplorasi
    cv=5,                       # Jumlah fold untuk cross-validation (5-fold CV)
    scoring='roc_auc'           # Metrik evaluasi yang digunakan untuk memilih model terbaik (AUC-ROC)
)
```

### Penjelasan Parameter:
1. **`estimator`**:
   - Ini adalah model pembelajaran mesin yang ingin dioptimalkan. Dalam hal ini, `gb_model` adalah model Gradient Boosting yang akan dioptimalkan menggunakan `GridSearchCV`.

2. **`param_grid`**:
   - Ini adalah dictionary yang berisi parameter dan nilai-nilai yang ingin dieksplorasi. Pada contoh Anda:
     ```python
     param_grid_gb = {
         'n_estimators': [100],       # Jumlah estimators (pohon) dalam model
         'learning_rate': [1.0],      # Tingkat pembelajaran (step size)
         'max_depth': [3],            # Kedalaman maksimum setiap pohon
         'subsample': [0.8]           # Proporsi sampel yang digunakan untuk melatih setiap pohon
     }
     ```
     Nilai-nilai ini adalah kandidat yang akan diuji selama proses grid search.

3. **`cv`**:
   - Menentukan jumlah fold untuk cross-validation. Dalam hal ini, `cv=5` berarti data pelatihan akan dibagi menjadi 5 bagian, dan model akan dilatih serta dievaluasi sebanyak 5 kali dengan kombinasi data yang berbeda.

4. **`scoring`**:
   - Metrik evaluasi yang digunakan untuk mengevaluasi performa model. Dalam hal ini, `scoring='roc_auc'` berarti metrik AUC-ROC digunakan untuk memilih model terbaik. Anda juga dapat menggantinya dengan metrik lain seperti `'accuracy'`, `'recall'`, dll., sesuai kebutuhan.

---

### Hasil dari `GridSearchCV`:
Setelah menjalankan `grid_search_gb.fit(X_train, y_train)`, Anda mendapatkan:
- **`best_params_`**: Parameter terbaik yang ditemukan oleh `GridSearchCV`.
- **`best_estimator_`**: Model dengan parameter terbaik yang telah dilatih pada data pelatihan.
- **`cv_results_`**: Informasi tambahan tentang hasil cross-validation untuk setiap kombinasi parameter.



---

### **Kesimpulan**
- **Memilih Gradient Boosting sebagai model terbaik**, alasan utamanya adalah stabilitas, kecepatan pelatihan, dan kemampuan menangani dataset tabular dengan baik.
- Dengan hyperparameter tuning, Gradient Boosting dapat dioptimalkan untuk mencapai performa yang lebih baik dibandingkan Neural Network pada kasus churn prediction dengan dataset seperti Telecom Churn Dataset.


## Evaluation

### **Metrik Evaluasi**
- **AUC-ROC**: Mengukur kemampuan model membedakan kelas churn dan non-churn.
- **Akurasi**: Proporsi prediksi benar dari total prediksi.
- **Recall**: Kemampuan model mendeteksi pelanggan churn (menghindari false negative).

### **Hasil Evaluasi**
| **Model**                | **AUC-ROC** | **Akurasi** | **Recall** |
|--------------------------|-------------|-------------|------------|
| Gradient Boosting (Awal)   |    0.50   |    0.78   |    0.03      |
| Neural Network             |    0.50   |    0.80   |    0.00      |
| Gradient Boosting (Tuning) |    0.50   |    0.80   |    0.01      |
| Gradient Boosting + SMOTE  |    0.50   |    0.80   |    0.01      |

### **Analisis Bisnis**
1. **Apakah model menjawab isu churn?**  
   **Ya**. Model Gradient Boosting setelah tuning memiliki **AUC-ROC 0.50** dan **recall 0.01** (dengan SMOTE), yang menunjukkan performa model masih perlu ditingkatkan dalam mengidentifikasi pelanggan berisiko churn.

2. **Apakah tujuan tercapai?**  
   **Sebagian**. Meskipun model memiliki akurasi yang tinggi (**0.80**), nilai **recall yang sangat rendah (0.01)** menunjukkan model masih kurang efektif dalam mendeteksi pelanggan yang benar-benar churn. Perlu dilakukan perbaikan lebih lanjut.

3. **Dampak solusi**  
   - **Prediksi Churn**: Model saat ini belum cukup andal untuk memberikan prediksi churn yang akurat.
   - **SMOTE**: Tidak memberikan peningkatan recall yang signifikan dalam kasus ini.
   - **Hyperparameter Tuning**: Tidak meningkatkan AUC-ROC, recall, atau akurasi dibandingkan baseline.

### **Kesimpulan**
- **Model Terbaik**: Tidak ada model yang menunjukkan performa yang cukup baik berdasarkan metrik evaluasi. Perlu dilakukan eksperimen lebih lanjut untuk meningkatkan performa model, terutama pada recall.
- **Rekomendasi**:
  - Mengeksplorasi model lain seperti Random Forest atau XGBoost dengan tuning lebih lanjut.
  - Memeriksa kembali fitur engineering dan preprocessing untuk memastikan model dapat menangkap pola yang lebih baik.
  - Menggunakan teknik lain untuk menangani ketidakseimbangan kelas selain SMOTE, seperti cost-sensitive learning atau penalized models.
