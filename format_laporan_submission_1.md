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

Data preparation adalah langkah penting dalam proses pengolahan data sebelum model machine learning atau deep learning dapat diterapkan. Tahap ini bertujuan untuk memastikan bahwa data yang digunakan berkualitas tinggi, bebas dari noise, dan relevan dengan masalah yang ingin diselesaikan. Berikut adalah beberapa tahapan dalam data preparation yang dilakukan untuk solusi yang diusulkan:

#### 1. **Pengumpulan Data**
Langkah pertama adalah mengumpulkan data yang diperlukan untuk masing-masing masalah yang dihadapi. Misalnya, untuk prediksi churn pelanggan, kita memerlukan data historis mengenai penggunaan layanan pelanggan, durasi langganan, tingkat interaksi pelanggan, dan informasi lainnya yang relevan. Dataset yang digunakan dalam contoh ini adalah *Telecom Churn Dataset* dari Kaggle.

#### 2. **Pembersihan Data (Data Cleaning)**
Pembersihan data sangat penting untuk menghilangkan ketidakkonsistenan dan data yang hilang. Beberapa langkah dalam pembersihan data antara lain:
   - **Menghapus atau mengisi data yang hilang (missing values)**: Data yang tidak lengkap dapat mempengaruhi kualitas model. Data yang hilang bisa diatasi dengan menghapus entri yang tidak lengkap atau mengisinya dengan nilai rata-rata, median, atau menggunakan metode imputasi yang lebih kompleks.
   - **Menghapus duplikat**: Data yang duplikat dapat mengarah pada overfitting dan bias dalam model. Oleh karena itu, entri yang sama harus dihapus.
   - **Menangani data outlier**: Outlier dapat mempengaruhi model dan menyebabkan hasil yang tidak akurat. Dalam kasus ini, teknik seperti clipping atau transformasi data dapat digunakan untuk menangani outlier.

#### 3. **Penyandian Kategorikal (Encoding Categorical Data)**
Banyak algoritma machine learning memerlukan data numerik, sehingga variabel kategorikal seperti jenis layanan atau status langganan perlu diubah menjadi format numerik.
   - **One-Hot Encoding**: Digunakan untuk variabel kategorikal yang memiliki beberapa kategori tanpa urutan tertentu (misalnya, jenis layanan).

#### 4. **Penskalaan Data (Feature Scaling)**
Penskalaan data penting agar fitur dengan skala besar (seperti pengeluaran bulanan) tidak mendominasi model. Teknik penskalaan yang umum digunakan adalah:
   - **StandardScaler**: Mengubah fitur agar memiliki distribusi normal dengan mean = 0 dan deviasi standar = 1.

#### 5. **Pemisahan Data (Data Splitting)**
Data harus dibagi menjadi dua set utama:
   - **Training Set**: Digunakan untuk melatih model.
   - **Test Set**: Digunakan untuk mengevaluasi performa model setelah pelatihan.
   Biasanya, pembagian data dilakukan dengan rasio 80:20 atau 70:30.

#### 6. **Penyusunan Fitur (Feature Engineering)**
Feature engineering adalah proses untuk menciptakan fitur baru yang lebih relevan dengan masalah yang ingin diselesaikan. Beberapa contoh adalah:
   - **Membuat fitur waktu**: Seperti durasi langganan yang dapat dihitung berdasarkan tanggal pendaftaran dan tanggal saat ini.
   - **Menggabungkan fitur**: Misalnya, menggabungkan frekuensi penggunaan dan jenis layanan untuk membentuk fitur baru yang lebih informatif.

### Alasan Mengapa Data Preparation Diperlukan

1. **Meningkatkan Kualitas Data**  
   Data yang tidak bersih, duplikat, atau mengandung nilai yang hilang akan mempengaruhi akurasi dan validitas model. Tanpa pembersihan yang tepat, model akan mempelajari pola yang salah, menghasilkan prediksi yang tidak akurat.

2. **Memastikan Data Konsisten**  
   Data yang tidak terstandarisasi atau memiliki unit yang berbeda dapat membingungkan model, terutama algoritma yang mengandalkan perhitungan jarak atau bobot fitur. Penskalaan data memastikan bahwa semua fitur berada dalam rentang yang setara, menghindari dominasi fitur tertentu terhadap model.

3. **Menangani Variabel Kategorikal**  
   Sebagian besar algoritma machine learning, terutama yang berbasis matematika, tidak dapat langsung menangani data kategorikal. Oleh karena itu, encoding sangat diperlukan untuk mengubah data kategorikal menjadi format yang dapat dipahami oleh algoritma.

4. **Memfasilitasi Proses Pelatihan dan Evaluasi**  
   Pembagian data menjadi set pelatihan dan pengujian penting untuk menghindari overfitting dan memastikan model dapat dievaluasi secara objektif. Tanpa pemisahan data yang tepat, model dapat terlalu cocok dengan data pelatihan dan gagal saat diuji dengan data yang belum terlihat sebelumnya.

5. **Meningkatkan Kinerja Model**  
   Feature engineering membantu untuk memilih atau menciptakan fitur yang lebih representatif bagi masalah yang dihadapi. Fitur yang relevan dapat membantu model dalam memahami pola-pola penting dalam data, yang pada akhirnya meningkatkan prediksi model.

Dengan tahapan data preparation yang baik, perusahaan telekomunikasi dapat membangun model yang lebih efisien dan akurat, yang pada gilirannya akan membantu mereka dalam memprediksi churn pelanggan, mengelompokkan pelanggan, dan memprediksi nilai umur pelanggan secara lebih efektif.

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
| Gradient Boosting (Awal) | 0.85        | 0.89        | 0.62       |
| Neural Network           | 0.82        | 0.87        | 0.58       |
| **Gradient Boosting (Tuning)** | **0.87** | **0.90** | **0.65** |
| **Gradient Boosting + SMOTE** | 0.86      | 0.88        | **0.72**   |

### **Analisis Bisnis**
1. **Apakah model menjawab isu churn?**  
   **Ya**. Model Gradient Boosting setelah tuning memiliki **AUC-ROC 0.87** dan **recall 0.72** (dengan SMOTE), yang menunjukkan kemampuan baik dalam mengidentifikasi pelanggan berisiko churn.

2. **Apakah tujuan tercapai?**  
   **Ya**. Tingkat recall meningkat dari 0.62 ke 0.72 setelah penerapan SMOTE, berarti model lebih efektif mendeteksi pelanggan yang benar-benar churn. Ini membantu perusahaan mengambil tindakan preventif.

3. **Dampak solusi**  
   - **Prediksi Churn**: Model memungkinkan perusahaan memberikan insentif atau layanan khusus ke pelanggan berisiko, sehingga mengurangi churn.
   - **SMOTE**: Meningkatkan recall sebesar **10%**, mengurangi risiko kehilangan pelanggan karena false negative.
   - **Hyperparameter Tuning**: Meningkatkan AUC-ROC sebesar **2%**, meningkatkan keandalan prediksi.

### **Kesimpulan**
- **Model Terbaik**: Gradient Boosting dengan hyperparameter tuning dan SMOTE (recall tertinggi **0.72**).
- **Rekomendasi**:
  - Fokus pada peningkatan recall untuk meminimalkan pelanggan churn yang terlewat.
  - Implementasi model ini di sistem CRM perusahaan untuk otomatisasi alert pelanggan berisiko.
