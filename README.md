# Laporan Proyek Machine Learning - Vania Rachmawati Dewi

## 1. Domain Proyek

### 1.1 Latar Belakang 

*Wine* merupakan salah satu minuman yang mengandung alkohol. *Wine* memiliki manfaat yang terdapat pada kandungan di dalamnya bagi kesehatan jika dikonsumsi secara tidak berlebihan. Beberapa manfaat *wine* bagi kesehatan diantaranya untuk mencegah penyakit kanker, memelihara kesehatan otak dan fungsi memori, menjaga kesehatan jantung, menjaga kesehatan gigi dan mulut serta menurunkan kadar gula darah[[1]](https://ejournal.akakom.ac.id/index.php/jiko/article/view/771/pdf). *Red wine* merupakan minuman anggur yang berasal dari buah anggur yang berwarna merah atau hitam. Warna merah yang dihasilkan merupakan hasil yang diperoleh dari pencelupan kulit dan biji ke dalam sari buah yang telah diperas untuk difermentasi dalam jangka waktu yang bervariasi. Di luar negeri *wine* menjadi minuman yang banyak dikonsumsi oleh berbagai lapisan masyarakat, khususnya negara-negara yang memiliki iklim dingin dan bersalju untuk menghangatkan badan. *Wine* memiliki berbagai karakteristik seperti kepadatan, nilai pH, alkohol dan asam lainnya [[2]](https://journal.stekom.ac.id/index.php/Bisnis/article/view/247/182).
Penilaian kualitas *wine* secara tradisional bergantung pada uji rasa yang dilakukan oleh ahli, yang bisa jadi subjektif dan memakan waktu. Pendekatan berbasis data diperlukan untuk memprediksi kualitas *wine* secara akurat berdasarkan sifat kimia yang terukur, yang dapat membantu pembuat *wine* dan industri *stakeholder* meningkatkan proses produksi serta mempertahankan standar kualitas yang konsisten.
Dedik & Yan Rianto (2024) pada penelitiannya mengevaluasi kinerja sembilan model machine learning dalam memprediksi kualitas *wine* menggunakan dataset dari repositori UCI. Model *machine learning* yang digunakan adalah *Logistic Regression*, *K-Nearest Neighbor* (KNN), *Decision Tree*, *Support Vector Machine* (SVM), *Random  Forest*,  *XGBoost*,  *LightGBM*, *CatBoost*,   dan   *Gradient   Boosting* [[3]](https://jurnal.upnyk.ac.id/index.php/telematika/article/view/13007/6670). 
Pada penelitian ini yang dilakukan terhadap dataset *Red Wine Quality* dengan membandingkan tiga algoritma yaitu *Random Forest*, *Support Vector Machine* (SVM), *K-Nearest Neighbor* (KNN). 

## 2. Business Understanding

### 2.1 Problem Statements 

1. Bagaimana memprediksi kualitas *red wine* berdasarkan komposisi yang ada di dalamnya?
2. Fitur atau kandungan apa yang paling mempengaruhi kualitas *red wine*?
3. Algoritma klasifikasi apa yang memberikan performa terbaik untuk memprediksi kualitas *red wine*?

### 2.2 Goals
1. Mengembangkan model *machine learning* yang dapat memprediksi kualitas *red wine* yang dinilai pada skala 0 sampai 10. 
2. Mengidentifikasi dan menganalisis fitur-fitur yang paling signifikan terhadap kualitas *red wine*.
3. Membandingkan performa beberapa algoritma seperti *Random Forest*, *SVM*, *K-Nearest Neighbor (KNN)* untuk menentukan model terbaik dalam memprediksi kualitas *red wine*.

### 2.3 Solution Statement 
1. Melakukan analisis data eksplorasi untuk melakukan hubungan antara fitur dan kualitas.
2. Menggunakan analisis fitur untuk menyoroti faktor-faktor utama yang mendorong kualitas *wine*.
3. Melatih dan mengevaluasi model klasifikasi *Random Forest*, *Support Vector Machine* (SVM), dan *K-Nearest Neighhbor* (KNN). Dan menggunakan metrik evaluasi seperti *accuracy*, *precision*, *recall* dan *f1-score*.

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

Tabel 1. Informasi Dataset

Dataset yang digunakan berasal dari kaggle tentang *Red Wine Quality* dari anggur *Vinho Verde* Portugal. Terdapat 1.599 baris dengan 12 kolom yang terdiri dari fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, alcohol dan quality. Pada dataset tersebut memiliki input dan output yang menetapkan nilai kualitasnya mulai dari angka 3 yang berarti buruk dan angka 8 merupakan sangat baik.

![image](https://github.com/user-attachments/assets/c8f9c722-7d86-4e80-97ca-907cf50b75e1) 

Gambar 1 Informasi Dataset

![image](https://github.com/user-attachments/assets/24e1d54d-d5e2-4610-915c-5e8653339e0d)

Gambar 2 Sampel Dataset

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

Tabel 2. Variabel Dataset

#### 3.3 Univariate Analysis 

![image](https://github.com/user-attachments/assets/5d73b7dd-e881-46e5-9f7f-ad376427ece3)

Gambar 3. Histogram Univariate Analysis

Beberapa parameter seperti volatile acidity, citric acidity, residual sugar, chlorides dan sulphates menunjukkan distribusi yang sangat condong ke kanan, yang berarti sebagian besar *wine* memiliki kadar yang rendah. Sementara itu, parameter seperti fixed acidity, free sulfur dioxide, total sulfur dioxide, pH, dan alcohol menunjukkan distribusi yang lebih terpusat atau mendekati normal. Mayoritas *wine* memiliki kandungan alcohol antara 9% hingga 11%. Bahkan ada beberapa *wine* dengan kandungan alcohol yang lebih tinggi, hingga 14 - 15%. Distribusi density yang terlihat paling mendekati normal berdasarkan histogram di atas. Kemudian ada distribusi quality, yang menunjukkan bahwa sebagian besar *wine* yang dianggap berkualitas sangat rendah atau sangat tinggi. Sebagian besar *wine* memiliki kualitas 5 atau 6, menunjukkan bahwa ini adalah nilai kualitas yang paling umum. Tidak terdapat *wine* dengan kualitas di bawah 3 atau di atas 8. Ini mengindikasikan bahwa sebagian besar wine berada dalam rentang kualitas "rata-rata". 

#### 3.4 Bivariate Analysis 

![image](https://github.com/user-attachments/assets/df89d236-ad2d-476d-b622-3ef52354a2bb)

Gambar 4. Barchart Bivariate Analysis

- Alcohol : Terdapat kecenderungan bahwa *wine* dengan kadar alcohol lebih tinggi cenderung memiliki quality yang lebih baik.
- Sulphates : Kadar sulfat yang lebih tinggi memiliki quality yang lebih baik. 
- Citric acid : Tingkat asam nitrat juga mempengaruhi quality dan citric acid yang lebih tinggi cenderung ditemukan pada *wine* berkualitas lebih baik. 
- Volatile acidity : Anggur dengan kesamaan volatile yang lebih rendah cenderung memiliki quality yang lebih baik.

#### 3.5 Correlation Matrix

![image](https://github.com/user-attachments/assets/7ea1b86c-4ec6-44f4-b765-c6cbbd9d105d)

Gambar 5. Correlation Matrix

- Quality memiliki hubungan positif antara alcohol.
- Quality memiliki hubungan negatif lemah antara volitile acidity.
- Quality hampir tidak memiliki hubungan antara residual sugar, free sulfur dioxide, dan  pH.
- Alcohol memiliki hubungan positif antara quality dan pH.
- Alcohol memiliki hubungan negatif antara dencity.
- Alcohol hampir tidak memiliki hubungan antara fixed acidity, residual sugar, dan free sulfur dioxide. 
- Volitile acidity memiliki hubungan positif antara pH.
- Volitile acidity memiliki hubungan negatif antara citric acid.
- Volitile hampir tidak memiliki hubungan antara residual sugar, chloride, free sulfur dioxide dan total sulfur dioxide. 
- Density memiliki hubungan positif antara fixed acidity.
- Density memiliki hubungan negatif antara density.
- Density hampir tidak memiliki hubungan antara volitile acidity, free sulfur dioxide dan total sulfur dioxide. 
- Citric acid memiliki hubungan positif antara fixed acidity.
- Citric acid memiliki hubungan negatif antara volitile acidity dan pH.
- Citric acid hampir tidak memiliki hubungan antara residual sugar, free sulfur dioxide dan total sulfu dioxide. 

#### 3.6 Memeriksa Outlier

![image](https://github.com/user-attachments/assets/a41856b4-8c5b-466e-abcc-5ce73ea6d321)

Gambar 6. Boxplot

Boxplot menunjukkan adanya outlier pada beberapa fitur. Seperti pada fitur alcohol, chlorides dan sulphates. Hal tersebut ditunjukkan dengan adanya titik-titik yang berada jauh di luar garis vertikal dari boxplot. 

## 4. Data Preparation

1. Menghapus Data Duplikat :
   - Membuat salinan dataset asli `df_wine` ke dalam `df_cleaned`
   - Kemudian, baris data yang terduplikasi dihapus dari `df_cleaned` menggunakan metode `.drop_duplicates()`.
   - Setelah penghapusan, dilakukan pengecekan kembali jumlah data duplikat untuk memastikan prosesnya berhasil. 
3. Menangani Outlier :
   - Langkah ini bertujuan untuk mengidentifikasi dan menghapus outlier pada fitur-fitur yang memiliki korelasi kuat dengan target variabel yaitu `quality`.
   - Pertama, korelasi dihitung setiap fitur dengan `quality`, dan fitur-fitur dengan korelasi absolut lebih dari 0,2 dipilih `cols_select`. Fitur `quality` sendiri dihapus dari daftar ini.
   - Kemudian, untuk setiap fitur dalam `cols_select`, dihitung nilai kuartil ` (Q1), kuartil 3 (Q3), dan interquartile range (IQR).
   - Outlier diidentifikasi sebagai data yang berada di bawah Q1 - 1,5 * IQR atau di atas Q3 + 1,5 * IQR.
   - Baris-baris yang mengandung outlier pada fitur-fitur yang dipilih tersebut dihapus dari `df_cleaned`
5. Transformasi Variabel Quality :
   - Kolom `quality` diubah menjadi data kategorikal menggunakan `pd.cut()`. Data dibagi ke dalam 3 kategori berdasarkan rentang nilai : `'buruk' (0-4), 'sedang' (4-6), dan 'baik' (6-10)`.
   - Setelah itu, kategori-kategori tersebut diubah menjadi nilai numerik : `'buruk' menjadi 0, 'sedang' menjadi 1, dan 'baik' menjadi 2` menggunakan metode `.map()`. 
7. Split Data :
   - Dataset yang sudah dibersihkan `df_cleaned` dipisahkan menjadi fitur (variabel independen) dan target (variabel dependen). Fitur disimpan di variabel `X` semua kolom kecuali quality dan target disimpan di variabel `y` pada kolom quality.
   - Kemudian data dibagi menjadi data training dan data testing menggunakan `train_test_split` dengan proporsi 80% untuk training dan 20% untuk testing. `random_state` diatur untuk memastikan hasil pembagian data yang konsisten.  
9. Standardisasi Fitur :
    - Fitur pada data training `X_train` dan data testing `X_test` distandardisasi menggunakan `StandardScaler`.
    - `StandarScaler` digunakan untuk menghitung rata-rata dan standar variasi dari data training dan menggunakannya untuk mentransformasi baik data training maupun data testing. Dan standardisasi ini bertujuan untuk membuat fitur memiliki rata-rata nol dan standar deviasi satu, yang terpenting untuk kinerja beberapa algoritma machine learning.
  
## 5. Modelling

Algoritma yang digunakan dalam data latih ini yaitu *Random Forest*, *Support Vector Machine (SVM)* dan *K-Nearest Neighbor* (KNN). Dari algoritma yang digunakan bertujuan untuk mendapatkan model terbaik dengan membandingkan masing-masing hasil yang diperoleh untuk dapat melakukan prediksi dengan tingkat akurasi tertinggi terhadap kualitas yang ada pada *red wine* dan memprediksi kandungan yang terdapat pada *red wine* seberapa berpengaruhnya. 

a. *Random Forest*

Algoritma *random forest* merupakan model *ensamble*. Algoritma berbasis *ensamble* merupakan gabungan dari beberapa teknik *machine learning* yang digabungkan menjadi satu model prediktif [[4]](https://ejournal.pnc.ac.id/index.php/infotekmesin/article/view/1751/514).

Library : `sklearn.ensemble.RandomForestClassifier`

Parameter yang digunakan : 
- `n_estimators=100` , Jumlah pohon keputusan. 
- `max_depth=10` , Kedalaman maksimum tiap pohon untuk membatasi overfitting.
- `random_state=42` , Menjamin reprodusibilitas hasil.
- `criterion='gini'` , Berfungsi untuk mengukur kualitas split.
- `min_samples_split=2` , Jumlah minimum sampel yang dibutuhkan untuk membagi node internal.
- `min_samples_leaf=1` , Jumlah minimum sampel pada daun (leaf node).

Keunggulan algoritma *random forest* yaitu [[5]](https://www.google.co.id/books/edition/Algoritma_Klasifikasi_untuk_Pemula_Solus/y84TEQAAQBAJ?hl=id&gbpv=1&dq=random+forest&pg=PA51&printsec=frontcover) :
- Berjalan secara efisien pada basis data yang besar.
- Mampu memberikan perkiraan variabel atau atribut yang penting dalam klasifikasi
- *Random forest* merupakan salah satu algoritma pembelajaran paling akurat yang tersedia untuk kumpulan data, *Random Forest* menghasilkan pengklasifikasian yang sangat akurat.

Kelemahan algoritma *random forest* yaitu [[6]](https://www.google.co.id/books/edition/Algoritma_Klasifikasi_untuk_Pemula_Solus/y84TEQAAQBAJ?hl=id&gbpv=1&dq=random+forest&pg=PA51&printsec=frontcover) :
 - *Random forest* cenderung bias pada saat berhadapan dengan variabel kategorikal.
 - Waktu komputasi pada dataset berskala besar relatif lambat.
 - Lebih banyak sumber daya komputasi diperlukan untuk mengimplementasikan algoritma *random forest*.

b. *Support Vector Machine* (SVM)

SVM terkenal sebagai algoritma yang dapat menangani data dengan dimensi tinggi dan bekerja baik pada kasus dengan jumlah sample yang lebih kecil dibandingkan dengan dimensi fitur. Tujuan dari algoritma SVM ialah untuk menemukan hyperplane terbaik dalam ruang berdimensi-N yang berfungsi sebagai pemisah yang jelas bagi titik-titik data input [[7]](https://books.google.co.id/books?id=CzheEQAAQBAJ&newbks=0&printsec=frontcover&pg=PA58&dq=algoritma+support+vector+machine&hl=id&source=newbks_fb&redir_esc=y#v=onepage&q=algoritma%20support%20vector%20machine&f=true).

Library : `sklearn.svm.SVC`

Parameter yang digunakan : 
- `kernel='rbf'`, Berfungsi untuk memetakan input ke ruang berdimensi lebih tinggi.
- `C=1.0` , Merupakan parameter regulasi.
- `gamma='scale'` , Mengontrol jarak pengaruh satu titik data.

Keunggulan algoritma SVM [[8]](https://www.google.co.id/books/edition/Teori_Dan_Implementasi_Machine_Learning/GNJNEQAAQBAJ?hl=id&gbpv=1&dq=kelebihan+dan+kekurangan+algoritma+svm&pg=PA30&printsec=frontcover)yaitu :
- Cocok untuk ruang dimensi tinggi.
- Hemat memori, karena menggunakan training point dari fungsi keputusan (*support vector*).
- Bekerja relatif baik ketika ada margin pemisahan yang jelas antar kelas.

Kelemahan algoritma SVM [[9]](https://www.google.co.id/books/edition/Teori_Dan_Implementasi_Machine_Learning/GNJNEQAAQBAJ?hl=id&gbpv=1&dq=kelebihan+dan+kekurangan+algoritma+svm&pg=PA30&printsec=frontcover) yaitu :
- Algoritma SVM tidak cocok untuk dataset dalam jumlah yang besar karena membuatuhkan waktu training yang lama.
- Jika jumlah fitur untuk setiap titik data melebihi jumlah sampel data training, SVM akan memiliki performa yang kurang baik.
- SVM tidak bekerja dengan baik ketika dataset memiliki lebih banyak noise misalnya kelas target terjadi tumpang tindih. 

c. *K-Nearest Neighbor* (KNN)

KNN merupakan metode klasifikasi terhadap objek baru berdasarkan data training yang memiliki jarak tetangga terdekat (nearest neighbor) dengan objek baru tersebut [[10]](https://books.google.co.id/books?id=CzheEQAAQBAJ&newbks=0&printsec=frontcover&pg=PA58&dq=algoritma+support+vector+machine&hl=id&source=newbks_fb&redir_esc=y#v=onepage&q=algoritma%20support%20vector%20machine&f=true). 

Library : `sklearn.neighbors.KNeighborsClassifier`

Parameter yang digunakan :
- `n_neighbors=5` , Jumlah tetangga terdekat yang dipertimbangkan dalam klasifikasi.
- `weights='uniform'` , Untuk memberikan bobot yang sama untuk tetangga.
- `metric='minkowski'` , Metode pengukuran jarak. Pada umumnya mengarah ke Euclidean distance saat `p=2`.
- `p=2` , Parameter daya pada metrik Minkowski. 

Keunggulan algoritma KNN [[11]](https://www.google.co.id/books/edition/Data_Sebagai_Fondasi_Kecerdasan_Buatan/GLgFEQAAQBAJ?hl=id&gbpv=1&dq=kelebihan+dan+kekurangan+algoritma+knn&pg=PA131&printsec=frontcover) yaitu :
- Mudah diterapkan karena KNN merupakan salah satu metode yang paling sederhana dalam *machine learning*.
- KNN cocok untuk masalah klasifikasi dan regresi nonlinier karena dapat menangani hubungan nonlinier antara fitur dan target.
- KNN cenderung memberikan hasil yang baik untuk dataset kecil yang tidak memiliki banyak dimensi.

Kelemahan algoritma KNN [[12]](https://www.google.co.id/books/edition/Data_Sebagai_Fondasi_Kecerdasan_Buatan/GLgFEQAAQBAJ?hl=id&gbpv=1&dq=kelebihan+dan+kekurangan+algoritma+knn&pg=PA131&printsec=frontcover) yaitu :
- KNN sangat sensitif terhadap outlier dan noise dalam kumpulan data. Data outlier dapat mempengaruhi perhitungan jarak antar titik data, sehingga dapat menyebabkan hasil klasifikasi yang salah.
- Kinerja yang buruk untuk fitur-fitur pada skala yang berbeda.
- KNN memerlukan memori yang besar karena perlu menyimpan seluruh dataset yang dilatih. 

## 6. Evaluation

Selanjutnya dilakukan analisis hasil evaluasi kinerja model melalui *confussion matrix*. Hasil evaluasi meliputi nilai : 
- True Positive (TP) yang merupakan jumlah kasus positif yang diprediksi dengan benar oleh model, yang artinya model mengidentifikasi kasus positif secara akurat.
- True Negative (TN) merupakan jumlah kasus negatif yang diprediksi dengan benar oleh model, yang artinya model mengidentifikasi kasus negatif secara akurat.
- False Positive (FP) merupakan jumlah kasus negatif yang diprediksi secara salah oleh model sebagai positif.
- False Negative (FN) merupakan jumlah kasus positif yang diprediksi secara salah oleh model sebagai negatif.

![image](https://github.com/user-attachments/assets/2cc16ef4-36a1-4ae8-891f-9b2f61a4a711)

Accuracy adalah persentase total prediksi yang benar dari semua prediksi yang dibuat oleh model. 

![image](https://github.com/user-attachments/assets/4f2c3be0-48e8-42dd-8101-0103ab72289b)

Precision menunjukkan persentase kasus positif yang diprediksi dengan benar dari semua prediksi positif yang dibuat oleh model. 

![image](https://github.com/user-attachments/assets/92590333-de3f-4b38-9c78-5c7fa577c169)

Recall (Sensitivitas atau True Positif Rate) merupakan persentase kasus positif yang diidentifikasi dengan benar oleh model dari semua kasus positif yang sebenarnya.

![image](https://github.com/user-attachments/assets/28bce124-270c-4a19-82c8-400d6aae9b7e)

F1-Score merupakan rata-rata harmoni precision dan recall. F1-score memberikan keseimbangan antara kedua metrik tersebut dan berguna jika terjadi ketidakseimbangan kelas. 

Berikut hasil accuracy 3 model algoritma : 

| Model    | Accuracy | Pricision | Recall | F1-Score |
|-----------|------------|------------|------------|------------|
|  **Random Forest** | 0.87 | 0.8381 | 0.878  | 0.8532 |
| **SVM**            | 0.86 | 0.7434 | 0.8622 | 0.7984 |
| **KNN**            | 0.84 | 0.8177 | 0.8425 | 0.8295 |

Tabel 6. Hasil Accuracy

#### Evaluasi Terhadap Probelem Statements 

1. Bagaimana memprediksi kualitas *red wine* berdasarkan komposisi yang ada di dalamnya?

   Berdasarkan ketiga model yang telah dibangun dan dievaluasi, hasil terbaik ditunjukkan oleh **Random Forest** dengan akurasi 87%, precision 0.83%, recall 0.87% dan f1-score 0.85%.       Hal ini menunjukkan bahwa sistem prediktif yang dibangun dan bekerja dengan baik dalam mengklasifikasikan kualitas *red wine*. 

2. Fitur atau kandungan apa yang paling mempengaruhi kualitas *red wine*?

   Melalui analisis korelasi dan evaluasi fitur, ditemukan bahwa fitur seperti **alcohol, volatile acidity, dan sulphates** memiliki pengaruh yang signifikan terhadap kualitas *red         wine*. Alcohol juga memiliki korelasi positif yang kuat terhadap quality. 

3. Algoritma klasifikasi apa yang memberikan performa terbaik untuk memprediksi kualitas *red wine*?
  
   Berdasarkan evaluasi accuracy, precision, recall, dan f1-score **Random Forest** terbukti sebagai model terbaik dibandingkan SVM dan KNN. 

#### Evaluasi Terhadap Goals 

1. Mengembangkan model machine learning yang dapat memprediksi kualitas red wine yang dinilai pada skala 0 sampai 10.

   Model klasifikasi telah berhasil dikembangkan dengan hasil akurasi yang baik yaitu 87%, precision 0.83%, recall 0.87% dan f1-score 0.85%.

2. Mengidentifikasi fitur paling berpengaruh terhadap kualitas *red wine*.

   Analisis data dan korelasi fitur berhasil menunjukkan fitur utama yang berpengaruh terhadap kualitas untuk mendukung pengambilan keputusan bagi produsen *red wine*.

3. Membandingkan algoritma klasifikasi untuk menentukan model terbaik.

   Perbandingan algoritma antara *Random Forest*, SVM, dan KNN telah dilakukan dengan hasil evaluasi yang mendalam.

#### Evaluasi Terhadap Solution Statements 

1. Melakukan analisis data eksplorasi untuk melakukan hubungan antara fitur dan kualitas

   Analisis univariate, bivariate, confussion matrix dan outlier memberikan informasi tentang hubungan antara fitur dan kualitas.

2. Menggunakan analisis fitur untuk menyoroti faktor-faktor utama yang mendorong kualitas *red wine*

   Fitur seperti alcohol, volatile acidity, dan sulphates terbukti secara statistik berkorelasi dengan quality, hal ini menjadikan solusi    menjadi berdampak.

3. Melatih dan mengevaluasi model klasifikasi *Random Forest*, *Support Vector Machine* (SVM), dan *K-Nearest Neighhbor* (KNN). Dan menggunakan metrik evaluasi seperti *accuracy*

   Model telah dilatih dan dievaluasi dengan metrik accuracy, precision, recall, f1-score dan confussion matrix, kemudian hasilnya menunjukkan bahwa solusi ini tepat untuk memilih model terbaik.

Berdasarkan hasil pengujian terhadap data testing, didapatkan hasil sebagai berikut : 

![image](https://github.com/user-attachments/assets/58cb9878-528e-47a7-b06a-53230398baf2)

Gambar 6. Perbandingan Accuracy, Precison, Recall dan F1-Score

Dari ketiga model yang dibandingkan

Accuracy
*   Random Forest Model menunjukkan performa terbaik dalam hal accuracy score, dengan nilai tertinggi yaitu 0.8780.
*   SVM Model berada pada urutan kedua dengan accuracy score 0.8622.
*   KNN Model dengan accuracy score terendah diantara ketiganya yaitu 0.8425 

Precision
*  Random Forest juga menunjukkan precision tertinggi dengan score 0.8381. 
*  KNN pada urutan kedua dengan score 0.8177. 
*  SVM dengan score 0.7434 dibagian terendah. 

Recall 
*   Random Forest juga menunjukkan score Recall tertinggi dengan 0.878. 
*   SVM berada pada urutan kedua dengan score 0.8622.
*   KNN diurutan ketiga dengan score 0.8425.

F-1 Score
*   Random Forest menunjukkan score 0.8532.
*   KNN berada di posisi kedua dengan score 0.8295.
*   SVM dengan score 0.7984. 

Berdasarkan perbandingan keempat metrik evaluasi, **Random Forest** merupakan model yang paling unggul di antaranya ketiganya. Model ini tidak hanya memiliki akurasi yang tinggi tetapi juga menunjukkan keseimbangaan terbaik antara Precision, Recall dan F-1 score. Maka dari itu, **Random Forest** adalah model terbaik untuk memprediksi kualitas anggur berdasarkan hasil evaluasi yang dilakukan. 





### Kesimpulan 

Model yang dikembangkan secara langsung menjawab seluruh problem statemens, mencapai semua goals yang ditetapkan, dan menerapkan solusi yang efektif dan berdampak. Hasil prediksi yang akurat dan analisis fitur yang relevan dapat membantu produsen *red wine* dalam hal : 
- Mengomptimalkan formula produk untuk kualitas yang lebih tinggi.
- Meningkatkan efisiensi proses produksi.
- Mempertahankan konsistensi mutu produk di pasar.
  
Dengan demikian, hal ini dapat memberikan nilai bisnis yang nyata bagi industri *wine*. 

## Referensi 

1. KHAKIM, Erfin Nur Rohma; HERMAWAN, Arief; AVIANTO, Donny. Implementasi correlation matrix pada klasifikasi dataset wine. JIKO (Jurnal Informatika dan Komputer), 2023, 7.1: 158-166.
2. SUPRIYADI, Riki, et al. Penerapan Algoritma Random Forest Untuk Menentukan Kualitas Anggur Merah. E-Bisnis: Jurnal Ilmiah Ekonomi Dan Bisnis, 2020, 13.2: 67-75.
3. FABIYANTO, Dedik; RIANTO, Yan. Performance Evaluation of Multiple Deep Learning Models for Wine Quality Prediction. Telematika: Jurnal Informatika dan Teknologi Informasi, 2024, 21.2: 209-223.
4. SARI, Laura; ROMADLONI, Annisa; LISTYANINGRUM, Rostika. Penerapan Data Mining dalam Analisis Prediksi Kanker Paru Menggunakan Algoritma Random Forest. Infotekmesin, 2023, 14.1: 155-162.
5. Algoritma Klasifikasi untuk Pemula Solusi Python dan RapidMiner. (2023). (n.p.): Deepublish.
6. Algoritma dan Struktur Data. (2025). (n.p.) : Yayasan Tri Edukasi Ilmiah Redaksi.
7. Teori Dan Implementasi Machine Learning Menggunakan Python. (2025). (n.p.): Serasi Media Teknologi.
8. Data Sebagai Fondasi Kecerdasan Buatan. (2024). (n.p.): TOHAR MEDIA.











