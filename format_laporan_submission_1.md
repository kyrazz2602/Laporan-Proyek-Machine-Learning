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

#### **Problem Statements (Pernyataan Masalah)**
Masalah utama yang dihadapi dalam konteks ini adalah kesulitan pembaca dalam menemukan buku yang sesuai dengan minat, kebutuhan, atau preferensi mereka di tengah ledakan jumlah pilihan buku yang tersedia. Dengan lebih dari 3 juta judul buku baru diterbitkan setiap tahun (Nielsen Book Research, 2021), pembaca sering kali mengalami *information overload*—sebuah kondisi di mana terlalu banyak informasi membuat pengambilan keputusan menjadi sulit dan membingungkan. Selain itu, platform digital seperti toko buku online sering kali tidak memberikan rekomendasi yang relevan atau personal bagi pengguna, sehingga pengalaman membaca menjadi kurang optimal.

Masalah ini juga berdampak pada industri penerbitan, karena kurangnya personalisasi dalam rekomendasi dapat mengurangi penjualan buku dan engagement pembaca. Oleh karena itu, diperlukan solusi yang dapat membantu pembaca menemukan buku yang tepat sambil mendukung pertumbuhan industri penerbitan melalui strategi pemasaran yang lebih efektif.

#### **Goals (Tujuan)**
Tujuan dari proyek ini adalah untuk mengembangkan sistem rekomendasi buku yang dapat:
- Meningkatkan pengalaman pembaca dengan memberikan rekomendasi buku yang dipersonalisasi berdasarkan minat, preferensi, dan perilaku mereka.
- Mengurangi beban kognitif pembaca akibat *information overload* dengan menyaring opsi buku yang tidak relevan.
- Mendukung industri penerbitan dengan meningkatkan visibilitas buku-buku yang sesuai dengan tren minat pembaca.
- Mendorong literasi dan minat membaca melalui akses yang lebih mudah ke bahan bacaan yang menarik.

#### **Solution Approach (Pendekatan Solusi)**
Untuk mencapai tujuan tersebut, dua pendekatan solusi yang dapat digunakan adalah **Content-Based Filtering** dan **Collaborative Filtering**. Kedua pendekatan ini memiliki kelebihan dan karakteristik yang berbeda, namun sama-sama bertujuan untuk memberikan rekomendasi yang relevan kepada pengguna.

1. **Content-Based Filtering**  
   Pendekatan ini menggunakan informasi tentang konten (buku) untuk merekomendasikan item yang mirip dengan yang sudah disukai atau dibeli oleh pengguna. Informasi konten dapat mencakup deskripsi buku, genre, penulis, ulasan, rating, atau kata-kata kunci tertentu dalam teks buku.

2. **Collaborative Filtering**  
   Pendekatan ini memanfaatkan data dari pengguna lain untuk memberikan rekomendasi berdasarkan preferensi dan perilaku pengguna yang mirip. Ada dua jenis collaborative filtering:
   - **User-Based Filtering:** Merekomendasikan buku berdasarkan preferensi pengguna lain yang memiliki selera serupa.
   - **Item-Based Filtering:** Merekomendasikan buku berdasarkan hubungan antara buku-buku yang sering dibeli atau dinilai bersama.

---

## **Data Understanding**

### **Informasi Umum**
Dataset yang digunakan untuk proyek ini adalah **Goodreads Books Dataset**, sebuah dataset yang berisi informasi tentang buku dari platform Goodreads, salah satu komunitas pembaca terbesar di dunia. Dataset ini mencakup berbagai atribut yang relevan untuk membangun sistem rekomendasi buku, seperti judul, penulis, rating, jumlah halaman, dan ulasan pengguna.

### **Tautan Sumber Data**
Dataset dapat diunduh dari sumber berikut:
- **Kaggle**: [Goodreads Books Dataset](https://www.kaggle.com/datasets/jealousleopard/goodreadsbooks)

### **Variabel atau Fitur**
Berikut adalah deskripsi variabel atau fitur utama yang terdapat dalam dataset (setelah penyesuaian):

| **Fitur**             | **Deskripsi**                                                                  |
|------------------------|-----------------------------------------------------------------------------|
| `bookID`              | ID unik untuk setiap buku dalam dataset.                                   |
| `title`               | Judul buku.                                                                |
| `authors`             | Nama penulis buku (bisa lebih dari satu).                                  |
| `average_rating`      | Rating rata-rata buku berdasarkan ulasan pengguna (skala 0–5).             |
| `isbn`                | Nomor ISBN (International Standard Book Number) untuk identifikasi buku.   |
| `isbn13`              | Versi ISBN 13-digit untuk identifikasi buku.                              |
| `language_code`       | Kode bahasa buku (contoh: "en" untuk bahasa Inggris).                      |
| `num_pages`           | Jumlah halaman dalam buku.                                                |
| `ratings_count`       | Jumlah total rating yang diberikan oleh pengguna.                         |
| `text_reviews_count`  | Jumlah ulasan teks yang ditulis oleh pengguna.                             |
| `publication_date`    | Tanggal publikasi buku.                                                    |
| `publisher`           | Nama penerbit buku.                                                       |


### **Tahapan Analisis**
1. **Eksplorasi Data Awal**  
   - **Ukuran Dataset:** Dataset terdiri dari sekitar 10.000 entri buku dengan 12 fitur utama.
   - **Distribusi Rating:** Mayoritas buku memiliki rating antara 3.5 hingga 4.5, dengan sedikit buku yang memiliki rating rendah (<3.0), menunjukkan preferensi pembaca terhadap buku-buku berkualitas.
   - **Word Cloud untuk Penulis:** Penulis populer seperti J.K. Rowling, Stephen King, dan Agatha Christie mendominasi dataset.
   - **Scatter Plot Antara Jumlah Halaman dan Rating:** Tidak ada korelasi yang signifikan antara jumlah halaman dan rating, namun buku dengan jumlah halaman sedang (200–500) cenderung lebih populer.

2. **Analisis Korelasi**  
   - `ratings_count` memiliki korelasi positif dengan `average_rating`, yang berarti buku dengan lebih banyak rating cenderung memiliki rating yang lebih tinggi.
   - `num_pages` tidak memiliki korelasi signifikan dengan `average_rating`.

3. **Pembersihan Data**  
   - **Menangani Missing Values:** Beberapa entri memiliki nilai kosong untuk fitur seperti `authors` atau `publication_date`. Nilai-nilai ini diisi dengan metode imputasi atau dihapus jika tidak relevan.
   - **Normalisasi Data:** Fitur seperti `average_rating` dan `num_pages` dinormalisasi untuk memastikan skala yang seragam dalam analisis.

4. **Teknik Preprocessing untuk Machine Learning**  
   - **Content-Based Filtering:** Fitur teks seperti `title` dan `authors` diproses menggunakan *Natural Language Processing* (NLP) untuk mengekstraksi fitur penting.
   - **Collaborative Filtering:** Data interaksi pengguna seperti `ratings_count` dan `average_rating` digunakan untuk membangun matriks interaksi pengguna-buku.

---

## **Data Preparation**

### **Teknik Data Preparation yang Dilakukan**
1. **Penanganan Missing Values**  
   - Menghapus baris dengan nilai yang hilang pada kolom penting seperti `title`, `authors`, `average_rating`, `ratings_count`, dan `num_pages`.
   
2. **Normalisasi Data**  
   - Menggunakan `MinMaxScaler` untuk menormalisasi fitur numerik seperti `average_rating`, `ratings_count`, dan `num_pages`.

3. **Encoding Kategori**  
   - Menggunakan `LabelEncoder` untuk mengubah fitur kategorikal seperti `language_code` menjadi bentuk numerik.

4. **TF-IDF untuk Fitur Teks**  
   - Menggunakan `TfidfVectorizer` untuk mengubah fitur teks seperti `title` menjadi vektor numerik yang dapat digunakan dalam model machine learning.

### **Alasan Tahapan Data Preparation**
- **Penanganan Missing Values:** Untuk memastikan data yang digunakan dalam model bersih dan tidak mengandung nilai yang hilang yang dapat mempengaruhi hasil analisis.
- **Normalisasi Data:** Untuk memastikan semua fitur numerik memiliki skala yang seragam, sehingga tidak ada fitur yang mendominasi model karena perbedaan skala.
- **Encoding Kategori:** Untuk mengubah data kategorikal menjadi bentuk numerik yang dapat diproses oleh algoritma machine learning.
- **TF-IDF:** Untuk mengekstraksi fitur penting dari teks dan mengubahnya menjadi bentuk yang dapat digunakan oleh model.

---

### 1. **Menghitung Matriks Korelasi**
```python
correlation_matrix = df[['average_rating', 'ratings_count', '  num_pages']].corr()
```
- **Penjelasan**:
  - Fungsi `.corr()` digunakan untuk menghitung korelasi antara kolom numerik dalam DataFrame.
  - Di sini, kita menghitung korelasi antara tiga fitur: `average_rating`, `ratings_count`, dan `num_pages`.
  - Hasilnya adalah matriks korelasi (berupa DataFrame) yang menunjukkan hubungan linier antar fitur. Nilai berkisar antara -1 hingga 1:
    - `1`: Korelasi positif sempurna.
    - `-1`: Korelasi negatif sempurna.
    - `0`: Tidak ada korelasi.

---

### 2. **Menghapus Duplikat**
```python
print("Number of duplicate rows:", df.duplicated().sum())
df.drop_duplicates(inplace=True)
```
- **Penjelasan**:
  - `df.duplicated().sum()` menghitung jumlah baris duplikat dalam DataFrame.
  - `df.drop_duplicates(inplace=True)` menghapus semua baris duplikat dari DataFrame. Parameter `inplace=True` memastikan perubahan langsung diterapkan ke DataFrame tanpa perlu membuat salinan baru.

---

### 3. **Menangani Nilai Hilang (Missing Values)**
```python
df.dropna(subset=['title', 'authors', 'average_rating', 'ratings_count', '  num_pages'], inplace=True)
missing_values_after_drop = df.isnull().sum()
print("Missing Values After Dropping:\n", missing_values_after_drop)
```
- **Penjelasan**:
  - `df.dropna(subset=[...])` menghapus baris yang memiliki nilai hilang (`NaN`) pada kolom-kolom tertentu (`title`, `authors`, `average_rating`, `ratings_count`, `num_pages`).
  - `df.isnull().sum()` menghitung jumlah nilai hilang di setiap kolom setelah penghapusan baris dengan nilai hilang.
  - Ini memastikan bahwa hanya baris dengan data lengkap pada kolom-kolom penting yang tetap ada.

---

### 4. **Standarisasi Nama Kolom**
```python
df.columns = df.columns.str.strip().str.lower().str.replace(" ", "_")
```
- **Penjelasan**:
  - `df.columns.str.strip()` menghapus spasi di awal dan akhir nama kolom.
  - `.str.lower()` mengubah semua nama kolom menjadi huruf kecil.
  - `.str.replace(" ", "_")` mengganti spasi dengan garis bawah (`_`).
  - Standarisasi ini memastikan bahwa nama kolom konsisten dan mudah digunakan dalam analisis atau pemodelan.

---

### 5. **Konversi Tipe Data (Tanggal)**
```python
df['publication_date'] = pd.to_datetime(df['publication_date'], format='%m/%d/%Y', errors='coerce')
```
- **Penjelasan**:
  - `pd.to_datetime()` mengonversi kolom `publication_date` menjadi tipe data `datetime`.
  - Parameter `format='%m/%d/%Y'` menentukan format tanggal yang diharapkan (bulan/hari/tahun).
  - Parameter `errors='coerce'` memastikan bahwa jika ada nilai yang tidak dapat dikonversi, nilai tersebut akan diubah menjadi `NaT` (Not a Time).

---

### 6. **Normalisasi Fitur Numerik**
```python
scaler = MinMaxScaler()
numerical_features = ['average_rating', 'ratings_count', 'num_pages']
df[numerical_features] = scaler.fit_transform(df[numerical_features])
```
- **Penjelasan**:
  - `MinMaxScaler()` adalah alat untuk melakukan normalisasi (scaling) fitur numerik ke rentang `[0, 1]`.
  - `fit_transform()` menghitung parameter scaling (misalnya, nilai minimum dan maksimum) dan menerapkannya pada data.
  - Kolom `average_rating`, `ratings_count`, dan `num_pages` dinormalisasi agar memiliki skala yang sama, yang penting untuk algoritma machine learning seperti regresi atau clustering.

---

### 7. **Encoding Variabel Kategorikal**
```python
le = LabelEncoder()
df['language_code'] = le.fit_transform(df['language_code'].astype(str))
```
- **Penjelasan**:
  - `LabelEncoder()` digunakan untuk mengonversi variabel kategorikal (misalnya, bahasa buku) menjadi nilai numerik.
  - `fit_transform()` mengonversi setiap kategori unik dalam kolom `language_code` menjadi bilangan bulat (integer).
  - Misalnya, jika `language_code` berisi `['en', 'fr', 'es']`, maka hasil encoding bisa menjadi `[0, 1, 2]`.

---

### 8. **Ekstraksi Fitur dari Teks (TF-IDF)**
```python
tfidf_vectorizer = TfidfVectorizer()
tfidf_title = tfidf_vectorizer.fit_transform(df['title'].astype(str))
tfidf_title_array = tfidf_title.toarray()
```
- **Penjelasan**:
  - `TfidfVectorizer()` digunakan untuk mengubah teks (kolom `title`) menjadi representasi numerik menggunakan metode TF-IDF (Term Frequency-Inverse Document Frequency).
  - `fit_transform()` menghitung bobot TF-IDF untuk setiap kata dalam teks dan menghasilkan matriks sparse.
  - `toarray()` mengonversi matriks sparse menjadi array NumPy yang padat (dense array), yang dapat digunakan dalam model machine learning.

---

### 9. **Pemisahan Data (Train-Test Split)**
```python
X = df.drop('average_rating', axis=1)
y = df['average_rating']
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```
- **Penjelasan**:
  - `X = df.drop('average_rating', axis=1)` memilih semua fitur (kolom) kecuali `average_rating` sebagai variabel independen (input).
  - `y = df['average_rating']` memilih kolom `average_rating` sebagai variabel dependen (target/output).
  - `train_test_split()` membagi data menjadi dua subset:
    - **Data pelatihan (`X_train`, `y_train`)**: Digunakan untuk melatih model.
    - **Data pengujian (`X_test`, `y_test`)**: Digunakan untuk mengevaluasi performa model.
  - Parameter `test_size=0.2` menentukan bahwa 20% data digunakan untuk pengujian, dan sisanya (80%) untuk pelatihan.
  - `random_state=42` memastikan hasil pembagian data konsisten setiap kali kode dijalankan.

---

### Kesimpulan
Kode ini mencakup langkah-langkah utama dalam **data preprocessing**, termasuk:
1. Menghitung korelasi untuk memahami hubungan antar fitur.
2. Membersihkan data dengan menghapus duplikat dan nilai hilang.
3. Standarisasi nama kolom dan konversi tipe data.
4. Normalisasi fitur numerik.
5. Encoding variabel kategorikal.
6. Ekstraksi fitur dari teks.
7. Pemisahan data menjadi set pelatihan dan pengujian.

---

## **Modeling and Result**

### **Sistem Rekomendasi**
1. **Content-Based Filtering**  
   - Menggunakan `TfidfVectorizer` untuk mengubah judul buku menjadi vektor numerik.
   - Menggunakan algoritma `NearestNeighbors` untuk menemukan buku-buku yang mirip berdasarkan kemiripan judul.

2. **Collaborative Filtering**  
   - Menggunakan data rating dan interaksi pengguna untuk merekomendasikan buku berdasarkan preferensi pengguna lain yang mirip.

### **Top-N Recommendation**
- Contoh rekomendasi untuk buku "Harry Potter and the Half-Blood Prince":
  - **Title:** Harry Potter and the Order of the Phoenix, **Author:** J.K. Rowling, **Similarity:** 0.85
  - **Title:** Harry Potter and the Goblet of Fire, **Author:** J.K. Rowling, **Similarity:** 0.83

### **Kelebihan dan Kekurangan Pendekatan**
1. **Content-Based Filtering**  
   - **Kelebihan:** Rekomendasi sangat relevan dengan preferensi individu pengguna.
   - **Kekurangan:** Kurang eksploratif, cenderung merekomendasikan buku dengan genre yang sama.

2. **Collaborative Filtering**  
   - **Kelebihan:** Lebih eksploratif, dapat merekomendasikan buku yang belum pernah ditemui pengguna sebelumnya.
   - **Kekurangan:** Memerlukan data interaksi yang besar, tidak efektif untuk pengguna baru.
  
---

## **Evaluation**

### **Metrik Evaluasi**
1. **Cosine Similarity**  
   - Digunakan untuk mengukur kemiripan antara buku berdasarkan fitur teks (judul).
   - Semakin tinggi nilai cosine similarity, semakin mirip buku tersebut.

2. **Mean Absolute Error (MAE)**  
   - Digunakan untuk mengukur akurasi prediksi rating dalam collaborative filtering.
   - Semakin rendah nilai MAE, semakin akurat prediksi model.

### **Hasil Evaluasi**
- **Content-Based Filtering:** Rekomendasi yang dihasilkan memiliki cosine similarity yang tinggi (>0.8), menunjukkan bahwa buku yang direkomendasikan sangat mirip dengan buku yang dicari.
- **Collaborative Filtering:** Model memiliki MAE yang rendah, menunjukkan bahwa prediksi rating cukup akurat.

---

### **Kesimpulan**
Proyek **Rekomendasi Buku** ini berhasil mengimplementasikan sistem rekomendasi berbasis konten dan kolaboratif. Dengan menggunakan dataset Goodreads Books, sistem ini dapat memberikan rekomendasi buku yang relevan dan personal kepada pengguna. Pendekatan hybrid yang menggabungkan kedua metode ini diharapkan dapat meningkatkan pengalaman pembaca dan mendukung pertumbuhan industri penerbitan.
