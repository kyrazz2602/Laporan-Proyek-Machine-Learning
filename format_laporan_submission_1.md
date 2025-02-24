# **Laporan Proyek Machine Learning - Arizal Anshori**

## **Project Overview**

### **Latar Belakang Proyek**
Di era digital yang serba terhubung, informasi dan konten tersedia dalam jumlah yang sangat besar. Salah satu bentuk konten yang paling banyak dikonsumsi adalah buku, baik dalam format fisik maupun digital (e-book). Namun, dengan semakin banyaknya pilihan buku yang tersedia di pasaran, pembaca sering kali mengalami kesulitan dalam memilih buku yang sesuai dengan minat, kebutuhan, atau preferensi mereka. Fenomena ini dikenal sebagai *information overload* atau kelebihan informasi, di mana pengguna merasa kewalahan dengan banyaknya opsi yang ada.

Menurut penelitian dari Nielsen Book Research, pada tahun 2021 saja, lebih dari 3 juta judul buku baru diterbitkan secara global. Dengan jumlah sebesar itu, menemukan buku yang relevan menjadi tantangan tersendiri bagi para pembaca. Di sisi lain, teknologi rekomendasi telah berkembang pesat dalam beberapa dekade terakhir, terutama di bidang e-commerce dan hiburan digital seperti Netflix dan Spotify. Teknologi ini mampu memberikan rekomendasi personal kepada pengguna berdasarkan data historis, perilaku, dan preferensi individu.

Proyek **Rekomendasi Buku** bertujuan untuk menghadirkan solusi berbasis teknologi yang dapat membantu pembaca menemukan buku-buku yang sesuai dengan minat mereka. Sistem rekomendasi buku ini akan menggunakan pendekatan algoritma machine learning, seperti *collaborative filtering* atau *content-based filtering*, untuk memberikan rekomendasi yang lebih akurat dan relevan.

### **Pentingnya Penyelesaian Proyek Ini**
1. **Meningkatkan Pengalaman Pembaca**  
   Dengan adanya sistem rekomendasi buku, pembaca tidak perlu lagi menghabiskan waktu berjam-jam untuk mencari buku yang tepat. Sistem ini akan memberikan saran yang dipersonalisasi, sehingga pengguna dapat menemukan buku yang benar-benar sesuai dengan minat mereka. Hal ini akan meningkatkan kepuasan pengguna dan memperkaya pengalaman membaca mereka.

2. **Mendorong Literasi dan Minat Membaca**  
   Menurut UNESCO, literasi adalah salah satu faktor kunci dalam pengembangan sumber daya manusia. Namun, rendahnya minat membaca di kalangan masyarakat sering kali disebabkan oleh kurangnya akses ke bahan bacaan yang relevan. Proyek ini dapat membantu meningkatkan minat membaca dengan menyediakan rekomendasi buku yang menarik dan sesuai dengan preferensi individu.

3. **Optimalisasi Industri Penerbitan**  
   Industri penerbitan juga dapat memperoleh manfaat dari proyek ini. Dengan adanya sistem rekomendasi, penerbit dapat memahami tren minat pembaca secara lebih mendalam. Informasi ini dapat digunakan untuk mengembangkan strategi pemasaran yang lebih efektif dan memproduksi buku-buku yang lebih sesuai dengan permintaan pasar.

4. **Mengatasi Kelebihan Informasi (*Information Overload*)**  
   Seperti yang telah disebutkan sebelumnya, jumlah buku yang tersedia di pasaran sangat besar. Proyek ini akan membantu mengurangi beban kognitif pembaca dengan menyaring informasi dan memberikan rekomendasi yang relevan. Hal ini sejalan dengan penelitian oleh Jakob Nielsen, yang menunjukkan bahwa pengguna cenderung lebih puas ketika diberikan opsi yang terbatas namun relevan.

5. **Pemanfaatan Teknologi Machine Learning**  
   Proyek ini juga memiliki nilai inovatif karena memanfaatkan teknologi machine learning. Algoritma seperti *collaborative filtering* dan *natural language processing* (NLP) dapat digunakan untuk menganalisis data pembaca, seperti ulasan buku, rating, dan deskripsi buku, untuk menghasilkan rekomendasi yang lebih akurat. Studi oleh Ricci et al. (2015) dalam buku *"Recommender Systems Handbook"* menunjukkan bahwa sistem rekomendasi berbasis AI dapat meningkatkan engagement pengguna hingga 30%.

### **Hasil Riset dan Referensi Terkait**
1. **Studi tentang Sistem Rekomendasi**  
   Menurut penelitian oleh Adomavicius dan Tuzhilin (2005), sistem rekomendasi telah terbukti efektif dalam meningkatkan kepuasan pengguna di berbagai platform digital. Penelitian ini menyoroti pentingnya pendekatan *personalization* dalam sistem rekomendasi.

2. **Tren Literasi Global**  
   Data dari World Bank menunjukkan bahwa tingkat literasi di beberapa negara masih rendah, terutama di kalangan anak muda. Proyek ini dapat menjadi langkah awal untuk meningkatkan aksesibilitas bahan bacaan yang relevan.

3. **Penerapan Machine Learning dalam Rekomendasi Buku**  
   Sebuah studi oleh Zhang et al. (2020) menunjukkan bahwa algoritma *deep learning* dapat digunakan untuk menganalisis teks deskripsi buku dan menghasilkan rekomendasi yang lebih akurat dibandingkan metode tradisional.

4. **Kasus Sukses di Industri Hiburan Digital**  
   Platform seperti Netflix dan Spotify telah berhasil menggunakan sistem rekomendasi untuk meningkatkan retensi pengguna. Netflix melaporkan bahwa 80% konten yang ditonton oleh pengguna berasal dari rekomendasi sistem mereka.

### Kesimpulan

Proyek **Rekomendasi Buku** memiliki relevansi yang tinggi dalam mengatasi tantangan yang dihadapi oleh pembaca modern, industri penerbitan, dan masyarakat secara umum. Dengan memanfaatkan teknologi machine learning, proyek ini tidak hanya akan meningkatkan pengalaman pembaca, tetapi juga berkontribusi pada peningkatan literasi dan optimalisasi industri penerbitan. Oleh karena itu, penyelesaian proyek ini sangat penting untuk menjawab kebutuhan masyarakat akan akses bahan bacaan yang relevan dan menarik.

**Referensi Utama:**
- Adomavicius, G., & Tuzhilin, A. (2005). Toward the Next Generation of Recommender Systems: A Survey of the State-of-the-Art and Possible Extensions.
- Ricci, F., Rokach, L., & Shapira, B. (2015). Recommender Systems Handbook.
- Zhang, Y., Dai, H., & Xu, C. (2020). Deep Learning for Recommender Systems.

---

## **Business Understanding**

### **Problem Statements (Pernyataan Masalah)**  
1. **Kesulitan Pembaca dalam Menemukan Buku yang Sesuai:**  
   Pembaca sering kali mengalami kesulitan menemukan buku yang sesuai dengan minat, kebutuhan, atau preferensi mereka di tengah ledakan jumlah pilihan buku yang tersedia, menyebabkan pengalaman membaca yang kurang optimal.  

2. **Beberapa Besar Informasi yang Membingungkan (*Information Overload*):**  
   Dengan lebih dari 3 juta judul buku baru diterbitkan setiap tahun, pembaca sering menghadapi *information overload*, yang meningkatkan beban kognitif dan membuat pengambilan keputusan menjadi sulit.  

3. **Kurangnya Personalisasi dalam Rekomendasi Buku:**  
   Platform digital seperti toko buku online sering kali gagal memberikan rekomendasi yang relevan dan dipersonalisasi, sehingga mengurangi engagement pembaca dan potensi penjualan industri penerbitan.  

4. **Rendahnya Literasi dan Minat Membaca Akibat Akses yang Tidak Efektif:**  
   Kurangnya akses mudah ke bahan bacaan yang menarik dapat menurunkan minat membaca masyarakat secara keseluruhan, yang pada akhirnya memengaruhi tingkat literasi dan pertumbuhan industri penerbitan.

### **Goals (Tujuan)**  
Tujuan dari proyek ini adalah untuk mengembangkan sistem rekomendasi buku yang dapat:  

1. **Memberikan Rekomendasi Buku yang Lebih Personal:**  
   Meningkatkan pengalaman pembaca dengan menyediakan rekomendasi buku yang sesuai dengan minat, preferensi, dan kebiasaan membaca mereka.  

2. **Mengurangi Kerumitan dalam Memilih Buku:**  
   Membantu pembaca menemukan buku yang relevan dengan lebih mudah, sehingga mengurangi stres akibat banyaknya pilihan yang tersedia (*information overload*).  

3. **Meningkatkan Kesuksesan Industri Penerbitan:**  
   Membantu penulis dan penerbit meningkatkan penjualan dengan memastikan buku-buku yang direkomendasikan sesuai dengan tren dan minat pembaca saat ini.  

4. **Mendorong Minat Membaca di Kalangan Masyarakat:**  
   Menjadikan aktivitas membaca lebih menarik dan mudah diakses melalui rekomendasi bahan bacaan yang relevan dan inspiratif, sehingga berkontribusi pada peningkatan literasi secara keseluruhan.

### **Solution Approach (Pendekatan Solusi)**  
Untuk mencapai tujuan proyek, kami mengusulkan dua pendekatan utama: **Content-Based Filtering** dan **Collaborative Filtering**. Kedua metode ini memiliki karakteristik unik dan saling melengkapi untuk memberikan rekomendasi buku yang relevan dan personal bagi pengguna.

---

1. **Content-Based Filtering (Rekomendasi Berbasis Konten)**  
   Pendekatan ini fokus pada informasi detail tentang buku itu sendiri untuk memberikan rekomendasi. Sistem akan menganalisis atribut seperti:  
   - Genre atau kategori buku  
   - Penulis  
   - Deskripsi buku  
   - Kata-kunci dalam teks atau ulasan  
   - Rating yang diberikan oleh pembaca  

   Dengan memahami preferensi pengguna terhadap buku-buku sebelumnya, sistem akan merekomendasikan buku baru yang serupa dengan apa yang sudah disukai atau dibeli oleh pengguna.  

   **Keunggulan:**  
   - Sangat efektif untuk pengguna baru yang belum memiliki banyak data interaksi.  
   - Memberikan rekomendasi yang lebih transparan karena berdasarkan konten buku yang jelas.  

---

2. **Collaborative Filtering (Rekomendasi Berbasis Kolaborasi)**  
   Pendekatan ini menggunakan pola perilaku pengguna lain untuk memberikan rekomendasi. Ada dua jenis utama:  

   - **User-Based Filtering (Berdasarkan Pengguna):**  
     Merekomendasikan buku dengan melihat preferensi pengguna lain yang memiliki selera serupa. Misalnya, jika dua orang sering membeli buku yang sama, sistem akan merekomendasikan buku dari satu pengguna kepada yang lain.  

   - **Item-Based Filtering (Berdasarkan Buku):**  
     Merekomendasikan buku berdasarkan hubungan antara buku-buku yang sering dibeli atau dinilai bersama. Contohnya, jika banyak pembaca membeli "Buku A" dan "Buku B" secara bersamaan, sistem akan merekomendasikan "Buku B" kepada pembaca yang hanya membeli "Buku A".  

   **Keunggulan:**  
   - Mampu menangkap preferensi pengguna yang lebih kompleks dan tidak langsung.  
   - Cocok untuk pengguna yang sudah memiliki riwayat interaksi yang cukup di platform.  

---

**Gabungan Kedua Pendekatan:**  
Untuk hasil yang optimal, kedua metode ini dapat digabungkan menjadi **Hybrid Filtering**, yaitu pendekatan yang mengombinasikan kekuatan Content-Based Filtering dan Collaborative Filtering. Dengan cara ini, sistem dapat memberikan rekomendasi yang lebih akurat, relevan, dan personal bagi setiap pengguna.  

**Contoh Penerapan:**  
- Jika seorang pengguna menyukai genre fiksi ilmiah, sistem akan menggunakan **Content-Based Filtering** untuk merekomendasikan buku dengan genre serupa.  
- Di saat yang sama, sistem juga akan menggunakan **Collaborative Filtering** untuk merekomendasikan buku-buku yang disukai oleh pengguna lain dengan minat serupa.  

---

## **Data Understanding**

### **Informasi Umum**
Dataset yang digunakan untuk proyek ini adalah **Goodreads Books Dataset**, sebuah dataset yang berisi informasi tentang buku dari platform Goodreads, salah satu komunitas pembaca terbesar di dunia. Dataset ini mencakup berbagai atribut yang relevan untuk membangun sistem rekomendasi buku.

---

### **Tautan Sumber Data**
Dataset dapat diunduh dari sumber berikut:
- **Kaggle**: [Goodreads Books Dataset](https://www.kaggle.com/datasets/jealousleopard/goodreadsbooks)

---

### **Jumlah Data**
Dataset ini memiliki:
- **Jumlah Baris (Entri):** 11123  
- **Jumlah Kolom (Fitur):** 12  

---

### **Kondisi Data**
Setelah dilakukan eksplorasi awal, kondisi dataset adalah sebagai berikut:
1. **Missing Values:**  
   - Beberapa fitur seperti `authors` dan `publication_date` mengandung nilai kosong atau hilang. Misalnya, ada beberapa entri yang tidak mencantumkan nama penulis atau tanggal publikasi.
   - Fitur `isbn` dan `isbn13` juga memiliki beberapa nilai yang hilang, namun jumlahnya relatif kecil (<1% dari total data).
2. **Duplikat:**  
   - Tidak ditemukan duplikat pada dataset ini. Setiap buku memiliki ID unik (`bookID`) yang memastikan tidak ada entri ganda.
3. **Outlier:**  
   - Fitur seperti `num_pages` memiliki beberapa outlier, misalnya buku dengan jumlah halaman sangat sedikit (<50) atau sangat banyak (>1000). Namun, outlier ini mungkin valid karena mencerminkan jenis buku tertentu (misalnya, buku anak-anak atau ensiklopedia).

---

### **Uraian Seluruh Fitur pada Data**
Berikut adalah deskripsi lengkap dari setiap fitur dalam dataset:

| **Fitur**             | **Deskripsi**                                                                  |
|------------------------|-------------------------------------------------------------------------------|
| `bookID`              | ID unik untuk setiap buku dalam dataset.                                     |
| `title`               | Judul buku.                                                                  |
| `authors`             | Nama penulis buku (bisa lebih dari satu).                                    |
| `average_rating`      | Rating rata-rata buku berdasarkan ulasan pengguna (skala 0–5).               |
| `isbn`                | Nomor ISBN (International Standard Book Number) untuk identifikasi buku.     |
| `isbn13`              | Versi ISBN 13-digit untuk identifikasi buku.                                |
| `language_code`       | Kode bahasa buku (contoh: "en" untuk bahasa Inggris).                        |
| `num_pages`           | Jumlah halaman dalam buku.                                                  |
| `ratings_count`       | Jumlah total rating yang diberikan oleh pengguna.                           |
| `text_reviews_count`  | Jumlah ulasan teks yang ditulis oleh pengguna.                               |
| `publication_date`    | Tanggal publikasi buku (format: MM/DD/YYYY).                                |
| `publisher`           | Nama penerbit buku.                                                         |

---

### **Tahapan Analisis**

#### **1. Eksplorasi Data Awal**
Untuk memahami karakteristik dataset, dilakukan eksplorasi data awal sebagai berikut:

- **Distribusi Rating (`average_rating`):**  
  - Mayoritas buku memiliki rating antara 3.5 hingga 4.5, dengan sedikit buku yang memiliki rating rendah (<3.0). Hal ini menunjukkan bahwa pembaca cenderung memberikan rating positif untuk buku-buku yang mereka sukai.
  - Visualisasi menggunakan histogram menunjukkan distribusi yang condong ke kanan (positively skewed).

- **Penulis Populer (`authors`):**  
  - Penulis seperti J.K. Rowling, Stephen King, dan Agatha Christie mendominasi dataset. Word cloud dibuat untuk menampilkan penulis dengan frekuensi kemunculan tertinggi.

- **Hubungan Antara Jumlah Halaman dan Rating (`num_pages` vs `average_rating`):**  
  - Scatter plot menunjukkan bahwa tidak ada korelasi signifikan antara jumlah halaman dan rating. Namun, buku dengan jumlah halaman sedang (200–500) cenderung lebih populer.

- **Bahasa Buku (`language_code`):**  
  - Sebagian besar buku dalam dataset berbahasa Inggris ("en"), dengan beberapa buku dalam bahasa lain seperti Spanyol ("es") dan Prancis ("fr").

#### **2. Analisis Korelasi**
Analisis korelasi dilakukan untuk memahami hubungan antarfitur numerik:
- **`ratings_count` vs `average_rating`:**  
  - Terdapat korelasi positif moderat, yang berarti buku dengan lebih banyak rating cenderung memiliki rating yang lebih tinggi.
- **`num_pages` vs `average_rating`:**  
  - Tidak ada korelasi signifikan antara jumlah halaman dan rating rata-rata.

#### **3. Visualisasi Data**
Beberapa visualisasi penting yang dihasilkan meliputi:
- **Histogram untuk Distribusi Rating:** Menunjukkan distribusi rating buku secara keseluruhan.
- **Word Cloud untuk Penulis:** Menampilkan penulis yang paling sering muncul dalam dataset.
- **Scatter Plot untuk Jumlah Halaman vs Rating:** Mengidentifikasi pola antara jumlah halaman dan popularitas buku.
- **Bar Chart untuk Bahasa Buku:** Menunjukkan proporsi buku berdasarkan bahasa.

---

### **Kesimpulan Awal**
Dataset ini cukup kaya dengan informasi yang relevan untuk membangun sistem rekomendasi buku. Namun, perlu dilakukan pembersihan data untuk menangani missing values dan outlier agar hasil analisis lebih akurat. Visualisasi data membantu memahami tren dan pola dalam dataset, seperti preferensi pembaca terhadap buku dengan jumlah halaman sedang dan rating yang tinggi.

---

## **Data Preparation**

### **Teknik Data Preparation yang Dilakukan**
Untuk memastikan dataset siap digunakan dalam pemodelan, dilakukan beberapa tahapan data preparation sebagai berikut:

1. **Penanganan Missing Values**  
   - Menghapus baris dengan nilai yang hilang pada kolom penting seperti `title`, `authors`, `average_rating`, `ratings_count`, dan `num_pages`. Hal ini dilakukan untuk memastikan bahwa hanya data yang lengkap yang digunakan dalam analisis.

2. **Normalisasi Data**  
   - Menggunakan `MinMaxScaler` untuk menormalisasi fitur numerik seperti `average_rating`, `ratings_count`, dan `num_pages`. Normalisasi memastikan semua fitur memiliki skala yang seragam, sehingga tidak ada fitur yang mendominasi model akibat perbedaan rentang nilai.

3. **Encoding Kategori**  
   - Menggunakan `LabelEncoder` untuk mengubah fitur kategorikal seperti `language_code` menjadi bentuk numerik. Encoding diperlukan agar algoritma machine learning dapat memproses data kategorikal.

4. **TF-IDF untuk Fitur Teks**  
   - Menggunakan `TfidfVectorizer` untuk mengubah fitur teks seperti `title` menjadi vektor numerik. Teknik ini membantu mengekstraksi informasi penting dari teks dan mengubahnya menjadi format yang dapat digunakan oleh model.

5. **Standarisasi Nama Kolom**  
   - Membersihkan nama kolom dengan menghapus spasi, mengubahnya menjadi huruf kecil, dan mengganti spasi dengan garis bawah (`_`). Standarisasi ini memastikan konsistensi dalam penamaan kolom untuk mempermudah analisis.

6. **Konversi Tipe Data (Tanggal)**  
   - Mengonversi kolom `publication_date` menjadi tipe data `datetime` menggunakan `pd.to_datetime()`. Konversi ini memungkinkan manipulasi tanggal yang lebih mudah dalam analisis.

7. **Pemisahan Data (Train-Test Split)**  
   - Membagi dataset menjadi data pelatihan (80%) dan data pengujian (20%) menggunakan `train_test_split()`. Pembagian ini memastikan bahwa model dapat dievaluasi secara objektif pada data yang belum pernah dilihat sebelumnya.

---

### **Alasan Tahapan Data Preparation**
Setiap langkah dalam data preparation memiliki tujuan spesifik untuk memastikan kualitas data dan hasil analisis:
- **Penanganan Missing Values:** Untuk menghindari bias atau kesalahan dalam model akibat data yang tidak lengkap.
- **Normalisasi Data:** Untuk memastikan semua fitur numerik memiliki skala yang sama, sehingga model tidak dipengaruhi oleh perbedaan rentang nilai.
- **Encoding Kategori:** Untuk mengubah data kategorikal menjadi format numerik yang dapat diproses oleh algoritma machine learning.
- **TF-IDF:** Untuk mengekstraksi fitur penting dari teks dan mengubahnya menjadi representasi numerik yang relevan.
- **Standarisasi Nama Kolom:** Untuk memastikan konsistensi dalam penamaan kolom, yang mempermudah proses analisis dan pemodelan.
- **Konversi Tipe Data:** Untuk memastikan bahwa setiap kolom memiliki tipe data yang sesuai dengan kebutuhan analisis.
- **Pemisahan Data:** Untuk memastikan bahwa model dapat dievaluasi secara objektif pada data yang belum pernah digunakan selama pelatihan.

---

#### 1. **Menghapus Duplikat**
```python
print("Number of duplicate rows:", df.duplicated().sum())
df.drop_duplicates(inplace=True)
```
- **Penjelasan:** Menghapus baris duplikat untuk memastikan bahwa setiap entri dalam dataset unik.

#### 2. **Menangani Nilai Hilang**
```python
df.dropna(subset=['title', 'authors', 'average_rating', 'ratings_count', 'num_pages'], inplace=True)
missing_values_after_drop = df.isnull().sum()
print("Missing Values After Dropping:\n", missing_values_after_drop)
```
- **Penjelasan:** Menghapus baris dengan nilai hilang pada kolom penting untuk memastikan data yang digunakan lengkap.

#### 3. **Normalisasi Fitur Numerik**
```python
scaler = MinMaxScaler()
numerical_features = ['average_rating', 'ratings_count', 'num_pages']
df[numerical_features] = scaler.fit_transform(df[numerical_features])
```
- **Penjelasan:** Menormalisasi fitur numerik ke rentang `[0, 1]` untuk memastikan skala yang seragam.

#### 4. **Encoding Variabel Kategorikal**
```python
le = LabelEncoder()
df['language_code'] = le.fit_transform(df['language_code'].astype(str))
```
- **Penjelasan:** Mengonversi variabel kategorikal seperti `language_code` menjadi nilai numerik.

#### 5. **Ekstraksi Fitur dari Teks**
```python
tfidf_vectorizer = TfidfVectorizer()
tfidf_title = tfidf_vectorizer.fit_transform(df['title'].astype(str))
tfidf_title_array = tfidf_title.toarray()
```
- **Penjelasan:** Mengubah teks dalam kolom `title` menjadi representasi numerik menggunakan TF-IDF.

#### 6. **Pemisahan Data**
```python
X = df.drop('average_rating', axis=1)
y = df['average_rating']
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```
- **Penjelasan:** Membagi dataset menjadi data pelatihan dan pengujian untuk evaluasi model.

---

### **Kesimpulan**
Proses data preparation mencakup langkah-langkah penting seperti penanganan missing values, normalisasi, encoding, ekstraksi fitur teks, dan pemisahan data. Setiap langkah dirancang untuk memastikan bahwa dataset siap digunakan dalam pemodelan dan menghasilkan hasil yang akurat serta andal. Langkah-langkah ini juga membantu meningkatkan performa model dengan menghilangkan noise dan memastikan konsistensi dalam data.

---

## **Modeling dan Hasil**

### **1. Algoritma SVD (Singular Value Decomposition)**
Algoritma **Singular Value Decomposition (SVD)** digunakan dalam pendekatan **Collaborative Filtering** untuk mereduksi dimensi dari matriks interaksi pengguna dan item (seperti rating). Proses ini membagi matriks menjadi tiga komponen utama:
- **Matriks Pengguna (U):** Representasi preferensi pengguna.
- **Matriks Singular Values (Σ):** Menangkap hubungan antara pengguna dan item.
- **Matriks Item (V):** Representasi karakteristik item.

Dengan reduksi dimensi, SVD dapat menangkap hubungan yang lebih kuat antara pengguna dan item, meningkatkan akurasi rekomendasi, serta mengatasi masalah *sparsity* pada matriks interaksi pengguna-item.

---

### **2. Content-Based Filtering**
Pendekatan **Content-Based Filtering** digunakan untuk merekomendasikan buku berdasarkan kemiripan fitur, seperti judul dan deskripsi, dengan metode **Cosine Similarity** untuk menghitung tingkat kemiripan antar buku.

#### **Hasil Rekomendasi untuk "Harry Potter and the Half-Blood Prince"**
| No | Judul Buku | Penulis | Similarity Score |
|----|--------------------------------------|--------------------------------|-----------------|
| 1  | Harry Potter and the Half-Blood Prince (Harry Potter #6) | J.K. Rowling/Mary GrandPré | **1.00** |
| 2  | Harry Potter Collection (Harry Potter #1-6) | J.K. Rowling | **0.78** |
| 3  | Harry Potter and the Philosopher's Stone (Harry Potter #1) | J.K. Rowling | **0.72** |
| 4  | Harry Potter and the Chamber of Secrets (Harry Potter #2) | J.K. Rowling | **0.72** |
| 5  | Harry Potter and the Chamber of Secrets (Harry Potter #2) | J.K. Rowling/Mary GrandPré | **0.72** |

---

### **3. Collaborative Filtering (SVD)**
Pendekatan **Collaborative Filtering** dengan algoritma **SVD** menganalisis pola interaksi pengguna dengan buku dan memprediksi rating untuk buku yang belum pernah mereka baca.

#### **Evaluasi Model (RMSE)**
- **Root Mean Squared Error (RMSE):** **0.0701**  
  *(Semakin rendah RMSE, semakin akurat prediksi model)*

#### **Top 5 Rekomendasi untuk User 1**
| No | Book ID | Predicted Rating |
|----|--------|-----------------|
| 1  | 34909  | **0.786** |
| 2  | 14243  | **0.786** |
| 3  | 38296  | **0.786** |
| 4  | 36438  | **0.786** |
| 5  | 2319   | **0.786** |

---

### **4. Analisis Hasil**
#### **Content-Based Filtering**
**Kelebihan:**
- Memberikan rekomendasi yang sangat relevan dengan preferensi pengguna.
- Tidak bergantung pada data interaksi pengguna lain (*cocok untuk pengguna baru*).

**Kekurangan:**
- Terbatas dalam eksplorasi, hanya merekomendasikan buku yang sangat mirip.
- Tidak dapat menangkap preferensi pengguna secara luas.

#### **Collaborative Filtering (SVD)**
**Kelebihan:**
- Lebih eksploratif, dapat merekomendasikan buku yang tidak selalu memiliki kemiripan langsung.
- Mampu menangkap preferensi pengguna secara lebih luas.

**Kekurangan:**
- Bergantung pada data interaksi pengguna (*kurang efektif untuk pengguna baru*).

---

### **5. Kesimpulan**
**Content-Based Filtering** memberikan rekomendasi yang sangat relevan tetapi kurang eksploratif.
**Collaborative Filtering (SVD)** menghasilkan prediksi rating yang akurat dengan **RMSE 0.0697**.
Kombinasi kedua pendekatan ini dapat meningkatkan kualitas rekomendasi dengan menggabungkan keunggulan masing-masing metode.
  
---

## **Evaluation**

### **Metrik Evaluasi**
1. **Mean Absolute Error (MAE) (Collaborative Filtering)**  
   - Digunakan untuk mengukur akurasi prediksi rating dalam collaborative filtering.  
   - Semakin rendah nilai MAE, semakin akurat prediksi model.

2. **Precision@K dan Recall@K (Content-Based Filtering)**  
   - **Precision@K:** Mengukur proporsi rekomendasi yang relevan di antara top-K rekomendasi.  
   - **Recall@K:** Mengukur seberapa baik sistem merekomendasikan semua item relevan yang ada di dataset.  

---

### **Hasil Evaluasi**

#### **Collaborative Filtering**
Untuk mengevaluasi pendekatan **Collaborative Filtering**, kami menggunakan metrik **Mean Absolute Error (MAE)**:

```plaintext
MAE: 0.0468
Mean Absolute Error (MAE): 0.04678655599895617
```

- **Interpretasi:**  
  - Nilai **MAE = 0.0468**, yang menunjukkan bahwa prediksi rating sangat akurat dengan selisih rata-rata yang kecil dari rating aktual.

#### **Content-Based Filtering**
Untuk mengevaluasi pendekatan **Content-Based Filtering**, kami menggunakan metrik **Precision@K** dan **Recall@K**:

```plaintext
Precision@5: 0.6
Recall@5: 0.6
```

- **Interpretasi:**  
  - **Precision@5 = 0.6** berarti 60% dari top-5 rekomendasi yang diberikan relevan dengan preferensi pengguna.  
  - **Recall@5 = 0.6** berarti sistem berhasil merekomendasikan 60% dari semua item relevan yang tersedia dalam dataset.

---

### **Kesimpulan**
Proyek **Rekomendasi Buku** ini berhasil mengimplementasikan sistem rekomendasi berbasis konten dan kolaboratif dengan hasil evaluasi sebagai berikut:

| **Pendekatan**          | **Metrik**            | **Hasil**       | **Interpretasi**                                                                 |
|--------------------------|-----------------------|-----------------|----------------------------------------------------------------------------------|
| **Collaborative**        | MAE                  | 0.0468          | Prediksi rating sangat akurat dengan selisih rata-rata kecil.                   |
| **Content-Based**        | Precision@5          | 0.6             | 60% dari top-5 rekomendasi relevan dengan preferensi pengguna.                   |
|                          | Recall@5             | 0.6             | 60% dari semua item relevan berhasil direkomendasikan.                          |

Pendekatan ini menunjukkan bahwa sistem rekomendasi bekerja dengan baik dalam memberikan rekomendasi yang akurat dan relevan bagi pengguna.

---

### **Kesimpulan**
Proyek **Rekomendasi Buku** ini berhasil mengimplementasikan sistem rekomendasi berbasis konten dan kolaboratif. Dengan menggunakan dataset Goodreads Books, sistem ini dapat memberikan rekomendasi buku yang relevan dan personal kepada pengguna. Pendekatan hybrid yang menggabungkan kedua metode ini diharapkan dapat meningkatkan pengalaman pembaca dan mendukung pertumbuhan industri penerbitan.
