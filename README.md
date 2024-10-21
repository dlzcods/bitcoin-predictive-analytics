# Laporan Proyek Machine Learning - Muhammad Abdiel Al Hafiz
## Domain Proyek
### Latar Belakang
Bitcoin adalah mata uang digital kriptografi yang beroperasi secara terdesentralisasi dan menggunakan sistem peer-to-peer. 
Identitas penciptanya tidak diketahui secara pasti, meskipun Satoshi Nakamoto sering disebut sebagai salah satu pengembangnya. 
Jaringan Bitcoin memanfaatkan teknologi yang dikenal dengan sebutan blockchain. Blockchain berfungsi sebagai buku besar digital yang mencatat semua transaksi yang telah terjadi. 
Buku besar ini dikelola secara peer-to-peer, yang berarti terdapat banyak komputer atau node yang terhubung dan berfungsi untuk memverifikasi setiap transaksi baru. 
Setiap transaksi dianggap sebagai satu blok, dan sekumpulan blok ini saling terhubung membentuk sebuah rantai [1]. 
Karena setiap blok menyimpan riwayat transaksi sebelumnya, blockchain menjadi sistem yang transparan dan aman untuk mengelola data transaksi secara desentralisasi.

<br>

Sejak diperkenalkan pada tahun 2009, Bitcoin telah menjadi salah satu mata uang digital yang paling dikenal dan diterima secara global. 
Daya tarik utama Bitcoin sebagai instrumen investasi terletak pada sifat desentralisasinya, yang mengurangi ketergantungan terhadap lembaga keuangan konvensional dan pemerintah. 
Selain itu, jumlah Bitcoin yang terbatas, yaitu hanya 21 juta sehingga menambahkan unsur kelangkaan yang dapat meningkatkan nilai pasar [1]. 
Kehadirannya sebagai “emas digital” telah menarik minat tinggi di kalangan investor, baik individu maupun institusi, yang melihatnya sebagai aset perlindungan terhadap inflasi dan ketidakpastian ekonomi.

<br>

Namun, harga Bitcoin terkenal sangat fluktuatif, dengan perubahan harga yang tajam dalam waktu singkat. 
Sebagai contoh, harga Bitcoin melonjak dari $5.033,42 pada 16 Maret 2020 menjadi $63.564,48 pada 13 April 2021, sebuah peningkatan sebesar 1.062,85% dalam waktu hanya 13 bulan. 
Setelah harga Bitcoin mencapai puncaknya pada pertengahan April, harga tersebut turun tajam menjadi $31.634,16 pada 21 Juni 2021, anjlok hampir setengahnya [4]. 
Fluktuasi harga ini dipengaruhi oleh berbagai faktor, termasuk sentimen pasar, kebijakan regulasi pemerintah, serta berita atau peristiwa yang muncul terhadap Bitcoin [2]. 
Ketidakpastian ini menjadi tantangan bagi investor dalam merumuskan strategi investasi yang efektif.

<br>

Oleh karena itu, penting bagi investor untuk memiliki alat yang dapat membantu mereka memahami dan memprediksi pergerakan harga Bitcoin di masa mendatang, 
salah satunya yaitu penerapan teknik machine learning [2]. Penerapan teknik machine learning dalam prediksi harga Bitcoin memungkinkan analisis pola kompleks dari berbagai variabel historis. 
Teknik ini dapat mengidentifikasi hubungan non-linear antara variabel dan menghasilkan prediksi yang lebih akurat dibandingkan metode tradisional

<br>

Dengan memanfaatkan analisis fundamental cryptocurrency, termasuk kapitalisasi pasar, yang mencerminkan nilai total Bitcoin yang beredar, volume transaksi yang menunjukkan likuiditas, 
serta pergerakan harga historis [3], faktor faktor ini dapat memberikan wawasan yang mendalam kepada investor tentang kekuatan dan potensi pertumbuhan Bitcoin di masa depan. 
Meskipun demikian, model prediksi dalam proyek ini hanya didasarkan pada data historis yang mencakup harga pembukaan, harga penutupan, harga tertinggi, harga terendah, volume transaksi, 
dan kapitalisasi pasar, sehingga tidak mencakup faktor eksternal lain yang juga mempengaruhi harga, seperti sentimen pasar atau regulasi.

<br>

Melalui analisis dan model prediksi yang akurat, investor dapat memperkirakan pergerakan harga Bitcoin dalam jangka waktu tertentu, 
sehingga dapat mengurangi risiko investasi dan memaksimalkan peluang keuntungan. Oleh karena itu, 
pengembangan model prediksi harga Bitcoin sangat penting bagi investor dalam menavigasi pasar yang dinamis dan kompleks ini.

## Business Understanding
Investor cryptocurrency, khususnya Bitcoin, adalah individu yang berusaha mendapatkan keuntungan dari fluktuasi harga aset digital. Dalam dunia investasi Bitcoin, kemampuan untuk menganalisis data historis seperti harga pembukaan, harga penutupan, harga tertinggi, harga terendah, volume transaksi, dan kapitalisasi pasar merupakan keahlian penting. Melalui analisis ini, investor berupaya memprediksi pergerakan harga Bitcoin di masa depan berdasarkan pola historis yang ada.

<br>

Bitcoin terkenal dengan volatilitasnya yang tinggi, di mana harga dapat berfluktuasi secara signifikan dalam waktu singkat. Prediksi yang terlalu optimis dapat menyebabkan kerugian besar, sementara sikap terlalu konservatif bisa mengakibatkan kehilangan peluang investasi yang berpotensi menguntungkan. Oleh karena itu, diperlukan sebuah metode yang mampu mengelola ketidakpastian ini dengan lebih akurat.

<br>

Salah satu solusi yang dapat diterapkan adalah dengan memanfaatkan teknik machine learning. Dengan memodelkan data historis yang mencakup berbagai faktor seperti harga dan volume transaksi, teknik ini dapat membantu investor mendapatkan prediksi yang lebih akurat mengenai pergerakan harga Bitcoin. Prediksi yang akurat tidak hanya membantu investor meminimalkan risiko kerugian, tetapi juga memaksimalkan peluang keuntungan di pasar yang dinamis dan sulit diprediksi ini.

### Problem Statement
Berdasarkan kondisi yang telah diuraikan sebelumnya, proyek ini akan mengembangkan sebuah sistem prediksi harga Bitcoin berdasarkan data historis yaitu harga tertinggi, harga terendah, harga pembukaan, harga penutupan, volume transaksi, dan kapitalisasi pasar dimana masing masing faktor memiliki peran penting dalam pergerakan harga Bitcoin seperti:
- Harga Tertinggi: Mencerminkan titik harga tertinggi yang dicapai Bitcoin dalam periode tertentu. Faktor ini penting karena menunjukkan batas atas kekuatan beli di pasar dan sering kali menjadi patokan untuk menentukan apakah harga sedang mendekati titik resistensi.
- Harga Terendah: Menunjukkan titik terendah harga Bitcoin dalam periode tertentu. Ini membantu mengidentifikasi titik dukungan dimana tekanan jual mungkin telah memudar, memberikan gambaran mengenai batas bawah dari volatilitas pasar.
- Harga Pembukaan: Adalah harga awal dari Bitcoin di awal periode perdagangan. Perbandingan antara harga pembukaan dan harga penutupan bisa memberikan indikasi tentang tren pasar yang sedang terjadi, apakah tren naik (bullish) atau turun (bearish).
- Harga Penutupan: Harga pada akhir periode perdagangan merupakan salah satu indikator kunci yang sering digunakan untuk melihat kecenderungan harga secara keseluruhan. Perubahan harga penutupan dari waktu ke waktu membantu dalam memahami pola tren harga di masa depan.
- Volume Transaksi: Volume transaksi mengukur seberapa banyak Bitcoin yang diperdagangkan dalam satu periode waktu. Tingginya volume transaksi sering kali dikaitkan dengan kekuatan pasar di balik pergerakan harga, di mana peningkatan volume dapat menandakan bahwa pergerakan harga tersebut lebih valid dan didukung oleh aktivitas pasar yang kuat.
- Kapitalisasi Pasar: Kapitalisasi pasar adalah nilai total dari semua Bitcoin yang beredar di pasar. Ini memberikan gambaran tentang seberapa besar pasar Bitcoin pada saat tertentu dan seberapa besar pengaruhnya terhadap fluktuasi harga. Kapitalisasi yang besar biasanya menunjukkan kestabilan, sedangkan kapitalisasi yang lebih kecil dapat berarti bahwa harga lebih rentan terhadap perubahan signifikan.

Dengan menggunakan teknologi machine learning algoritma XGBoost dan hyperparameter tuning diharapkan dapat menjawab permasalahan berikut: 
- Bagaimana cara memanfaatkan data historis harga BTC seperti harga pembukaan, harga penutupan, harga tertinggi, harga terendah, volume transaksi, dan kapitalisasi pasar untuk memprediksi harga BTC di masa depan?
- Bagaimana cara mengoptimalkan kinerja algoritma XGBoost untuk memprediksi harga Bitcoin melalui parameter-parameter penting seperti learning rate, max_depth, subsample, dan n_estimators?

### Goals
Untuk menjawab problem statement tersebut, akan dibuat predictive modelling dengan tujuan atau goals sebagai berikut:
- Membuat model machine learning yang dapat memprediksi harga Bitcoin untuk 5 hari ke depan berdasarkan parameter yang ditetapkan.
- Mencari nilai optimal untuk learning rate, max_depth, subsample, dan n_estimators pada algoritma XGBoost melalui proses hyperparameter tuning, dengan tujuan memaksimalkan akurasi prediksi harga Bitcoin.

### Solution Statement
Untuk mencapai goals tersebut, ada 2 pendekatan yang akan digunakan yaitu:
- Menggunakan Algoritma XGBoost: XGBoost merupakan algoritma ensemble yang sangat cocok untuk tugas prediksi, terutama pada data yang kompleks dan nonlinear seperti data harga Bitcoin. XGBoost bekerja dengan membangun banyak pohon keputusan (decision tree) secara berurutan, dengan setiap pohon belajar dari kesalahan pohon sebelumnya. Struktur ensemble ini memungkinkan XGBoost menangkap pola yang kompleks dalam data dan menghasilkan prediksi yang lebih akurat.
- Menentukan Nilai Optimal untuk Hyperparameter XGBoost: Untuk mengoptimalkan kinerja model XGBoost, kita akan melakukan hyperparameter tuning. Hyperparameter adalah parameter yang tidak dipelajari oleh model selama pelatihan, melainkan diatur sebelum pelatihan dimulai. Beberapa hyperparameter penting pada XGBoost antara lain:
  - learning_rate: Mengontrol tingkat di mana model belajar dari setiap iterasi. Nilai yang terlalu besar dapat menyebabkan overfitting, sedangkan nilai yang terlalu kecil dapat memperlambat konvergensi.
  - max_depth: Mengontrol kedalaman maksimum pohon keputusan. Nilai yang terlalu besar dapat menyebabkan overfitting, sedangkan nilai yang terlalu kecil dapat menghambat kemampuan model untuk menangkap pola yang kompleks.
  - subsample: Mengontrol proporsi data yang digunakan untuk membangun setiap pohon keputusan. Subsampling dapat membantu mengurangi overfitting.
  - n_estimators: Menentukan jumlah pohon keputusan yang akan dibangun. Jumlah pohon yang terlalu sedikit dapat menyebabkan underfitting, sedangkan jumlah pohon yang terlalu banyak dapat menyebabkan overfitting.




