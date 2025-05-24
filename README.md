# Laporan Proyek Machine Learning - Vania Rachmawati Dewi

## 1. Domain Proyek

### 1.1 Latar Belakang 

Wine merupakan salah satu minuman yang mengandung alkohol. Wine memiliki manfaat yang terdapat pada kandungan di dalamnya bagi kesehatan jika dikonsumsi secara tidak berlebihan. Beberapa manfaat wine bagi kesehatan diantaranya untuk mencegah penyakit kanker, memelihara kesehatan otak dan dungsi memori, menjaga kesehatan jantung, menjaga kesehatan gigi dan mulut serta menurunkan kadar gula darah[[1]](https://ejournal.akakom.ac.id/index.php/jiko/article/view/771/pdf). *Red wine* merupakan minuman anggur yang berasal dari buah anggur yang berwarna merah atau hitam. Warna merah yang dihasilkan merupakan hasil yang diperoleh dari pencelupan kulit dan biji ke dalam sari buah yang telah diperas untuk difermentasi dalam jangka waktu yang bervariasi. Di luar negeri *wine* menjadi minuman yang banyak dikonsumsi oleh berbagai lapisan masyarakat, khususnya negara-negara yang memiliki iklim dingin dan bersalju untuk menghangatkan badan. *Wine* memiliki berbagai karakteristik seperti kepadatan, nilai pH, alkohol dan asam lainnya [[2]](https://journal.stekom.ac.id/index.php/Bisnis/article/view/247/182).
Penilaian kualitas *wine* secara tradisional bergantung pada uji rasa yang dilakukan oleh ahli, yang bisa jadi subjektif dan memakan waktu. Pendekatan berbasis data diperlukan untuk memprediksi kualitas *wine* secara akurat berdasarkan sifat kimia yang terukur, yang dapat membantuk pembuat *wine* dan industri *stakeholder* meningkatkan proses produksi serta mempertahankan standar kualitas yang konsisten. 
Dedik & Yan Rianto (2024) pada penelitiannya mengevaluasi kinerja sembilan model machine learning dalam memprediksi kualitas *wine* menggunakan dataset dari repositori UCI. Model machine learning yang digunakan adalah Logistic Regression, K-Nearest Neighbor (KNN), Decision Tree, Support Vector Machine (SVM), Random  Forest,  XGBoost,  LightGBM, CatBoost,   dan   Gradient   Boosting [[3]](https://jurnal.upnyk.ac.id/index.php/telematika/article/view/13007/6670). 
Pada penelitian yang dilakukan terhadap dataset Red Wine Quality dengan membandingkan tiga algoritma yaitu Random Forest, Support Vector Machine (SVM), K-Nearest Neighbor (KNN). 

## 2. Business Understanding

### 2.1 Problem Statements 

1. Bagaimana memprediksi kualitas wine merah berdasarkan komposisi yang ada di dalamnya?
2. Kandungan apa yang paling berpengaruh terhadap kualitas dari red wine?
3. Bagaimana membangun sistem prediktif yang mampu mengklasifikasikan *red wine* berdasarkan komposisi atau bahan dengan akurasi yang dapat diandalkan?

### 2.2 Goals
1. Mengembangkan model *machine learning* yang dapat memprediksi kualitas *red wine* yang dinilai pada skala 0 sampai 10. 
2. Memberikan wawasan bagi pembuatn *wine* untuk mengoptimalkan produksi dan meningkatkan kontrol kualitas. 
3. Membuat dan membandingkan beberapa algoritma klasifikasi seperti Random Forest, Support Vector Machine (SVM) dan K-Nearest Neighbor (KNN).

### 2.3 Solution Statement 
1. Melakukan analisis data eksplorasi untuk melakukan hubungan antara fitur dan kualitas.
2. Menggunakan analisis fitur untuk menyoroti faktor-faktor utama yang mendorong kualitas *wine*.
3. Melatih dan mengevaluasi model klasifikasi Random Forest, Support Vector Machine (SVM), dan K-Nearest Neighhbor (KNN). Dan menggunakan metrik evaluasi seperti accuracy, precision, recall dan f1-score.

## 3. Data Understanding

### 3.1 Deskripsi Dataset

#### 3.1.1 Informasi Dataset

| Jenis     | Keterangan |
|-----------|------------|
| **Title** | *Red Wine Quality* |
| **Source** | [Kaggle](https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009) |
| **License** | Open Data Commons |
| **Visibility** | Public |
| **Tags** | *Eart and Nature*, *Education*, *Beginner*, *Alcohol*, *Benchmark* | 
| **Usability** | 8.82 |

Dataset yang digunakan berasal dari kaggle tentang *Red Wine Quality* dari anggur *Vinho Verde* Portugal. Terdapat 1.599 baris dengan 12 kolom yang terdiri dari fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, alcohol dan quality. Pada dataset tersebut memiliki input dan output yang menetapkan nilai kualitasnya mulai dari angka 3 yang berarti buruk dan angka 8 merupakan sangat baik.

<t> ![image](https://github.com/user-attachments/assets/c8f9c722-7d86-4e80-97ca-907cf50b75e1) </t> 

Gambar 3.1 Informasi Dataset

<t> ![image](https://github.com/user-attachments/assets/24e1d54d-d5e2-4610-915c-5e8653339e0d) </t>

Gambar 3.2 Sampel Dataset

#### 3.2 Deskripsi Variabel

| Nama Variabel                                                    | Deskripsi                                                                                            |
| ---------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| Fixed acidity                                                    | Jumlah total asam yang tidak mudah menguap dalam anggur, terutama asam tartat, malat, dan sitrat.    |
| Volatile acidity                                                 | Jumlah total asam mudah menguap, terutama asam asetat.                                               |
| Citric acid                                                      | Asam alami yang ditemukan dalam buah jeruk.                                                          |
| Residual sugar                                                   | Jumlah gula yang tersisa setelah fermentasi alkohol selesai.                                         |
| Chlorides                                                        | Kandungan ion klorida dalam anggur.                                                                  |
| Free sulfur dioxide                                              | Jumlah sulfur dioksida bebas yang tersedia dalam anggur.                                             |
| Total sulfur dioxide                                             | Jumlah total sulfur dioksida, termasuk bentuk bebas dan terikat.                                     |
| Density                                                          | Kepadatan anggur, sering berkorelasi dengan kadar alkohol dan gula.                                  |
| pH                                                               | Tingkat keasaman atau alkalinitas anggur.                                                            |
| Sulphates                                                        | Senyawa sulfur, seperti kalium sulfat, ditemukan dalam anggur.                                       |
| Alcohol                                                          | Kandungan alkohol dalam anggur, biasanya diukur sebagai persentase volume.                           |
| Quality                                                          | Peringkat kualitas anggur, pada umumnya berskala numerik (misalnya 0 - 10).                          |

#### 3.3 Univariate Analysis 

![image](https://github.com/user-attachments/assets/5d73b7dd-e881-46e5-9f7f-ad376427ece3)

Gambar 3.3 Histogram Univariate Analysis

#### 3.4 Bivariate Analysis 

![image](https://github.com/user-attachments/assets/df89d236-ad2d-476d-b622-3ef52354a2bb)

Gambar 3.4 Barchat Bivariate Analysis

#### 3.5 Correlation Matrix

![image](https://github.com/user-attachments/assets/7ea1b86c-4ec6-44f4-b765-c6cbbd9d105d)

Gambar 3.5 Correlation Matrix


#### 3.6 Memeriksa Outlier

![image](https://github.com/user-attachments/assets/a41856b4-8c5b-466e-abcc-5ce73ea6d321)

Gambar 3.6 Boxplot 




