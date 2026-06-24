# Introduction to Machine Learning with Python

Repository ini berisi hasil reproduksi kode, ringkasan materi, dan penjelasan konsep dari buku ***Introduction to Machine Learning with Python: A Guide for Data Scientists*** karya **Andreas C. Müller** dan **Sarah Guido**.
Seluruh notebook disusun sebagai bagian dari tugas individu untuk memperdalam pemahaman teori sekaligus praktik implementasi machine learning menggunakan Python dan scikit-learn.

## Tujuan Repository

Repository ini dibuat untuk:

* mereproduksi kode dari setiap chapter buku,
* merangkum isi tiap chapter dalam bentuk notebook,
* menjelaskan konsep-konsep penting yang dibahas pada setiap bab,
* serta mendokumentasikan workflow machine learning dari dasar hingga topik lanjutan seperti pipeline dan text processing.

## Struktur Repository

Setiap notebook mewakili satu chapter dari buku, dengan isi berupa:

* ringkasan materi,
* penjelasan teori,
* reproduksi kode program,
* visualisasi,
* serta interpretasi hasil.

Daftar notebook dalam repository ini:

* `Chapter1_Introduction.ipynb`
* `Chapter2_Supervised_Learning.ipynb`
* `Chapter3_Unsupervised_Learning_and_Preprocessing.ipynb`
* `Chapter4_Representing_Data_and_Engineering_Features.ipynb`
* `Chapter5_Model_Evaluation_and_Improvement.ipynb`
* `Chapter6_Algorithm_Chains_and_Pipelines.ipynb`
* `Chapter7_Working_with_Text_Data.ipynb`
* `Chapter8_Wrapping_Up.ipynb`

---

# Chapter Summary

## Chapter 1 – Introduction to Machine Learning

Chapter pertama membahas pengenalan dasar tentang machine learning, alasan mengapa machine learning dibutuhkan, serta perbedaan antara supervised learning dan unsupervised learning.
Pada notebook ini, implementasi dilakukan menggunakan **dataset Iris** dengan model **K-Nearest Neighbors (KNN)**.

Hal-hal utama yang dibahas:

* pengertian machine learning sebagai metode yang belajar dari data,
* keterbatasan pendekatan tradisional berbasis aturan,
* jenis machine learning secara umum,
* proses dasar workflow machine learning:

  * memuat dataset,
  * memahami struktur data,
  * visualisasi data,
  * membagi data train dan test,
  * melatih model,
  * mengevaluasi hasil prediksi.

Pada bagian implementasi, model KNN digunakan untuk mengklasifikasikan spesies bunga iris berdasarkan fitur seperti panjang dan lebar sepal/petal. Evaluasi dilakukan menggunakan **accuracy**, **classification report**, dan **confusion matrix**. Selain itu, dilakukan juga percobaan beberapa nilai **K** untuk melihat pengaruhnya terhadap performa model.

---

## Chapter 2 – Supervised Learning

Chapter ini membahas algoritma-algoritma utama dalam **supervised learning**, yaitu pendekatan machine learning yang menggunakan data berlabel. Fokus utama chapter ini adalah memahami bagaimana model belajar dari data training, bagaimana model melakukan generalisasi pada data baru, serta bagaimana memilih model yang sesuai untuk suatu permasalahan.

Topik utama yang dipelajari:

* konsep **generalization**, **overfitting**, dan **underfitting**,
* pengaruh kompleksitas model terhadap performa,
* algoritma supervised learning untuk klasifikasi dan regresi.

Beberapa model yang direproduksi pada chapter ini meliputi:

* **k-Nearest Neighbors (KNN)** untuk klasifikasi,
* **Linear Models** seperti Logistic Regression dan Linear Regression,
* **Decision Tree**,
* **Random Forest**,
* **Gradient Boosting**,
* **Support Vector Machine (SVM)**,
* serta pengantar model regresi.

Notebook chapter ini menunjukkan bagaimana parameter model memengaruhi performa, misalnya:

* jumlah tetangga pada KNN,
* parameter regularisasi pada Logistic Regression,
* kedalaman pohon pada Decision Tree,
* serta parameter pada ensemble methods.

Melalui chapter ini, dipahami bahwa tidak ada satu model yang selalu terbaik untuk semua kasus. Pemilihan model harus mempertimbangkan:

* ukuran dataset,
* jumlah fitur,
* kompleksitas pola data,
* interpretabilitas model,
* dan kebutuhan komputasi.

---

## Chapter 3 – Unsupervised Learning and Preprocessing

Chapter 3 membahas **unsupervised learning** dan teknik **preprocessing** data. Berbeda dari supervised learning, unsupervised learning bekerja pada data yang tidak memiliki label target. Tujuannya adalah menemukan pola, struktur, atau representasi tersembunyi dari data.

Topik yang dipelajari dalam chapter ini meliputi:

### 1. Preprocessing

Sebelum model digunakan, data sering kali perlu diproses terlebih dahulu. Teknik preprocessing yang dibahas antara lain:

* **StandardScaler**
* **MinMaxScaler**
* **RobustScaler**
* **Normalizer**

Chapter ini menunjukkan bahwa preprocessing sangat penting, terutama untuk algoritma yang sensitif terhadap skala fitur seperti KNN, SVM, PCA, dan clustering.

### 2. Dimensionality Reduction

Beberapa teknik reduksi dimensi yang dibahas:

* **Principal Component Analysis (PCA)**
  Digunakan untuk mereduksi jumlah fitur sambil mempertahankan informasi penting sebanyak mungkin.
* **Non-negative Matrix Factorization (NMF)**
  Digunakan untuk representasi data berbasis komponen non-negatif.
* **t-SNE**
  Digunakan untuk visualisasi data berdimensi tinggi ke ruang 2 dimensi.

### 3. Clustering

Algoritma clustering yang dibahas:

* **K-Means**
* **Agglomerative Clustering**
* **DBSCAN**

Melalui chapter ini, dipahami bahwa unsupervised learning berguna untuk:

* eksplorasi struktur data,
* segmentasi data,
* visualisasi,
* dan representasi fitur sebelum digunakan oleh model lain.

---

## Chapter 4 – Representing Data and Engineering Features

Chapter ini berfokus pada bagaimana data direpresentasikan sebelum digunakan oleh model, serta bagaimana membuat fitur baru yang lebih informatif melalui **feature engineering**.

Topik utama yang dibahas:

* pentingnya representasi data,
* transformasi fitur numerik,
* penanganan fitur kategorikal,
* pembuatan fitur baru dari fitur yang sudah ada.

Beberapa konsep penting yang dipelajari:

* **one-hot encoding** untuk data kategorikal,
* **binning/discretization** untuk mengubah fitur kontinu menjadi interval,
* **interaksi antar fitur**,
* **polynomial features** untuk menambahkan hubungan non-linear,
* dan penggunaan representasi fitur yang tepat agar model dapat menangkap pola data dengan lebih baik.

Chapter ini menekankan bahwa performa model tidak hanya dipengaruhi oleh algoritma, tetapi juga oleh kualitas representasi data. Feature engineering yang baik dapat membuat model sederhana bekerja jauh lebih baik.

---

## Chapter 5 – Model Evaluation and Improvement

Chapter 5 membahas bagaimana mengevaluasi model machine learning secara benar dan bagaimana meningkatkan performanya secara sistematis.

Topik utama pada chapter ini meliputi:

### 1. Cross-Validation

Cross-validation digunakan untuk mengukur performa model secara lebih stabil dibanding hanya satu kali train-test split.
Beberapa bentuk evaluasi yang dibahas:

* train-test split,
* k-fold cross-validation,
* stratified cross-validation.

### 2. Evaluation Metrics

Metrik evaluasi yang digunakan harus sesuai dengan jenis masalah. Pada chapter ini dibahas:

* **accuracy**
* **precision**
* **recall**
* **f1-score**
* **confusion matrix**
* **ROC curve** dan **AUC**
* evaluasi untuk dataset tidak seimbang

### 3. Hyperparameter Tuning

Untuk meningkatkan performa model, chapter ini memperkenalkan:

* **GridSearchCV**
* **parameter grid**
* pencarian kombinasi hyperparameter terbaik

### 4. Model Selection

Setelah berbagai model dan parameter dicoba, model dipilih berdasarkan performa validasi, bukan hanya berdasarkan hasil pada training set.

Chapter ini sangat penting karena menjelaskan bahwa model yang terlihat bagus di training set belum tentu bagus pada data baru. Evaluasi yang benar adalah inti dari machine learning yang valid.

---

## Chapter 6 – Algorithm Chains and Pipelines

Chapter 6 membahas bagaimana menyusun beberapa langkah machine learning menjadi satu workflow yang rapi menggunakan **Pipeline** dan **algoritma chain**.

Masalah yang sering muncul dalam machine learning adalah:

* preprocessing dilakukan manual,
* rawan data leakage,
* kode menjadi panjang dan sulit dirawat,
* tuning parameter preprocessing dan model sulit dilakukan bersamaan.

Untuk mengatasi hal tersebut, chapter ini memperkenalkan:

* **Pipeline**
* **make_pipeline**
* kombinasi preprocessing + model dalam satu objek
* tuning hyperparameter pada pipeline menggunakan **GridSearchCV**

Contoh alur yang dibahas:

* scaling data → model klasifikasi
* feature selection → model
* preprocessing → dimensionality reduction → classifier

Keuntungan pipeline:

* kode lebih bersih dan konsisten,
* preprocessing hanya dipelajari dari data training,
* lebih aman terhadap data leakage,
* mudah digunakan bersama cross-validation dan grid search.

Chapter ini menekankan pentingnya membangun workflow machine learning yang reproducible dan terstruktur.

---

## Chapter 7 – Working with Text Data

Chapter 7 membahas bagaimana data teks diubah menjadi representasi numerik agar dapat digunakan oleh algoritma machine learning.

Karena model machine learning tidak bisa langsung memproses teks mentah, maka diperlukan teknik representasi teks. Chapter ini membahas beberapa pendekatan utama, yaitu:

### 1. Bag-of-Words

Teks diubah menjadi vektor frekuensi kata menggunakan:

* **CountVectorizer**

### 2. TF-IDF Representation

Untuk memberikan bobot lebih besar pada kata-kata yang informatif dan mengurangi pengaruh kata yang terlalu umum, digunakan:

* **TfidfVectorizer**

### 3. Parameter Penting pada Text Vectorization

Beberapa parameter yang dipelajari:

* `min_df`
* `max_df`
* `ngram_range`
* penggunaan unigram dan bigram

### 4. Text Classification

Setelah teks diubah menjadi fitur numerik, model seperti **Logistic Regression** dapat digunakan untuk klasifikasi dokumen.

### 5. Pipeline untuk Text Data

Chapter ini juga menunjukkan bagaimana vectorizer dan classifier dapat digabungkan ke dalam pipeline agar proses klasifikasi teks menjadi lebih praktis dan konsisten.

Melalui chapter ini, dipahami bahwa keberhasilan text classification sangat bergantung pada bagaimana teks direpresentasikan, bukan hanya pada model yang digunakan.

---

## Chapter 8 – Wrapping Up

Chapter terakhir berfungsi sebagai penutup dan rangkuman keseluruhan isi buku. Fokus utamanya adalah menyatukan semua konsep yang telah dipelajari menjadi satu **workflow machine learning end-to-end**.

Chapter ini menekankan bahwa proyek machine learning yang baik umumnya melalui tahapan berikut:

1. memahami masalah,
2. memahami data,
3. membagi data menjadi training dan test,
4. melakukan preprocessing,
5. memilih dan melatih model,
6. mengevaluasi model,
7. melakukan tuning hyperparameter,
8. dan menginterpretasikan hasil.

Pada notebook chapter ini, seluruh konsep sebelumnya dirangkum melalui contoh pipeline klasifikasi lengkap yang melibatkan:

* preprocessing dengan `StandardScaler`,
* model klasifikasi,
* evaluasi menggunakan confusion matrix, classification report, ROC curve,
* serta tuning parameter menggunakan `GridSearchCV`.

Chapter ini menegaskan bahwa machine learning bukan hanya soal memilih algoritma, tetapi tentang membangun proses analisis yang terstruktur, aman, dan dapat digeneralisasikan ke data baru.

---

# Tools and Libraries

Beberapa library utama yang digunakan di repository ini antara lain:

* **Python**
* **NumPy**
* **Pandas**
* **Matplotlib**
* **Seaborn**
* **scikit-learn**

Beberapa modul scikit-learn yang sering digunakan:

* `train_test_split`
* `KNeighborsClassifier`
* `LogisticRegression`
* `LinearRegression`
* `DecisionTreeClassifier`
* `RandomForestClassifier`
* `GradientBoostingClassifier`
* `SVC`
* `StandardScaler`, `MinMaxScaler`, `RobustScaler`
* `PCA`, `NMF`, `TSNE`
* `KMeans`, `AgglomerativeClustering`, `DBSCAN`
* `Pipeline`, `make_pipeline`
* `GridSearchCV`, `cross_val_score`
* `CountVectorizer`, `TfidfVectorizer`

---

# What I Learned from This Repository

Melalui reproduksi buku ini, saya mempelajari bahwa machine learning bukan hanya tentang menjalankan model, tetapi juga tentang memahami keseluruhan proses dari data mentah hingga evaluasi hasil.

Beberapa hal penting yang saya pelajari:

* cara membedakan supervised dan unsupervised learning,
* bagaimana overfitting dan underfitting memengaruhi performa model,
* pentingnya preprocessing dan feature engineering,
* cara mengevaluasi model dengan metrik yang tepat,
* pentingnya cross-validation dan hyperparameter tuning,
* manfaat pipeline untuk workflow yang rapi,
* serta bagaimana data teks dapat diproses menjadi fitur numerik.

Repository ini membantu saya memahami machine learning secara lebih menyeluruh, tidak hanya dari sisi teori tetapi juga implementasi langsung menggunakan Python.

---

# How to Run

1. Clone repository ini:

```bash
git clone https://github.com/USERNAME/Introduction-to-Machine-Learning-with-Python.git
```

2. Masuk ke folder repository:

```bash
cd Introduction-to-Machine-Learning-with-Python
```

3. Buka notebook menggunakan:

* **Google Colab**, atau
* **Jupyter Notebook**

4. Jalankan notebook per chapter sesuai urutan:

* Chapter 1
* Chapter 2
* Chapter 3
* Chapter 4
* Chapter 5
* Chapter 6
* Chapter 7
* Chapter 8

---

# Repository Notes

* Notebook pada repository ini merupakan hasil reproduksi dan ringkasan pembelajaran dari buku ***Introduction to Machine Learning with Python***.
* Beberapa bagian telah disesuaikan agar lebih mudah dipahami dalam konteks pembelajaran.
* Visualisasi, tabel, dan evaluasi model disusun agar hasil running dapat langsung dilihat di notebook maupun GitHub.

---

# Author

**Naufal Alif Abyan**
**NIM:** 101032300032
**Course:** Machine Learning / Enrichment for Machine Learning and Deep Learning Classes
