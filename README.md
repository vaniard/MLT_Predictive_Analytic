# Laporan Proyek Machine Learning - Vania Rachmawati Dewi

## Domain Proyek

### Latar Belakang 

Wine merupakan salah satu minuman yang mengandung alkohol. Wine memiliki manfaat yang terdapat pada kandungan di dalamnya bagi kesehatan jika dikonsumsi secara tidak berlebihan. Beberapa manfaat wine bagi kesehatan diantaranya untuk mencegah penyakit kanker, memelihara kesehatan otak dan dungsi memori, menjaga kesehatan jantung, menjaga kesehatan gigi dan mulut serta menurunkan kadar gula darah[[1]](https://ejournal.akakom.ac.id/index.php/jiko/article/view/771/pdf). *Red wine* merupakan minuman anggur yang berasal dari buah anggur yang berwarna merah atau hitam. Warna merah yang dihasilkan merupakan hasil yang diperoleh dari pencelupan kulit dan biji ke dalam sari buah yang telah diperas untuk difermentasi dalam jangka waktu yang bervariasi. Di luar negeri *wine* menjadi minuman yang banyak dikonsumsi oleh berbagai lapisan masyarakat, khususnya negara-negara yang memiliki iklim dingin dan bersalju untuk menghangatkan badan. *Wine* memiliki berbagai karakteristik seperti kepadatan, nilai pH, alkohol dan asam lainnya [[2]](https://journal.stekom.ac.id/index.php/Bisnis/article/view/247/182).
Penilaian kualitas *wine* secara tradisional bergantung pada uji rasa yang dilakukan oleh ahli, yang bisa jadi subjektif dan memakan waktu. Pendekatan berbasis data diperlukan untuk memprediksi kualitas *wine* secara akurat berdasarkan sifat kimia yang terukur, yang dapat membantuk pembuat *wine* dan industri *stakeholder* meningkatkan proses produksi serta mempertahankan standar kualitas yang konsisten. 
Dedik & Yan Rianto (2024) pada penelitiannya mengevaluasi kinerja sembilan model machine learning dalam memprediksi kualitas *wine* menggunakan dataset dari repositori UCI. Model machine learning yang digunakan adalah Logistic Regression, K-Nearest Neighbor (KNN), Decision Tree, Support Vector Machine (SVM), Random  Forest,  XGBoost,  LightGBM, CatBoost,   dan   Gradient   Boosting [[3]](https://jurnal.upnyk.ac.id/index.php/telematika/article/view/13007/6670). 
Pada penelitian yang dilakukan terhadap dataset Red Wine Quality dengan membandingkan tiga algoritma yaitu Random Forest, Support Vector Machine (SVM), K-Nearest Neighbor (KNN). 

## Business Understanding

### Problem Statements 

1. Bagaimana memprediksi kualitas wine merah berdasarkan komposisi yang ada di dalamnya?
2. Kandungan apa yang paling berpengaruh terhadap kualitas dari red wine?
3. Bagaimana membangun sistem prediktif yang mampu mengklasifikasikan *red wine* berdasarkan komposisi atau bahan dengan akurasi yang dapat diandalkan?

### Goals
1. Mengembangkan model *machine learning* yang dapat memprediksi kualitas *red wine* yang dinilai pada skala 0 sampai 10. 
2. Memberikan wawasan bagi pembuatn *wine* untuk mengoptimalkan produksi dan meningkatkan kontrol kualitas. 
3. Membuat dan membandingkan beberapa algoritma klasifikasi seperti Random Forest, Support Vector Machine (SVM) dan K-Nearest Neighbor (KNN).

### Solution Statement 
1. Melakukan analisis data eksplorasi untuk melakukan hubungan antara fitur dan kualitas.
2. Menggunakan analisis fitur untuk menyoroti faktor-faktor utama yang mendorong kualitas *wine*.
3. Melatih dan mengevaluasi model klasifikasi Random Forest, Support Vector Machine (SVM), dan K-Nearest Neighhbor (KNN). Dan menggunakan metrik evaluasi seperti accuracy, precision, recall dan f1-score.

## Data Understanding

### Deskripsi Variable

#### Informasi Dataset

| Jenis     | Keterangan |
|-----------|------------|
| **Title** | *Red Wine Quality* |
| **Source** | [Kaggle](https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009) |
| **License** | Open Data Commons |
| **Visibility** | Public |
| **Tags** | *Eart and Nature*, *Education*, *Beginner*, *Alcohol*, *Benchmark* | 
| **Usability** | 8.82 |

Dataset yang digunakan berasal dari kaggle tentang *Red Wine Quality* dari anggur *Vinho Verde* Portugal. Terdapat 1.599 baris dengan 12 kolom yang terdiri dari fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, alcohol dan quality. Pada dataset tersebut memiliki input dan output yang menetapkan nilai kualitasnya mulai dari angka 3 yang berarti buruk dan angka 8 merupakan sangat baik. 



