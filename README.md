# Laporan Proyek Machine Learning - Muhammad Abdiel Al Hafiz
## Domain Proyek
### Latar Belakang
Bitcoin adalah mata uang digital kriptografi yang beroperasi secara terdesentralisasi dan menggunakan sistem peer-to-peer. 
Identitas penciptanya tidak diketahui secara pasti, meskipun Satoshi Nakamoto sering disebut sebagai salah satu pengembangnya. 
Jaringan Bitcoin memanfaatkan teknologi yang dikenal dengan sebutan blockchain. Blockchain berfungsi sebagai buku besar digital yang mencatat semua transaksi yang telah terjadi. 
Buku besar ini dikelola secara peer-to-peer, yang berarti terdapat banyak komputer atau node yang terhubung dan berfungsi untuk memverifikasi setiap transaksi baru. 
Setiap transaksi dianggap sebagai satu blok, dan sekumpulan blok ini saling terhubung membentuk sebuah rantai [1]. 
Karena setiap blok menyimpan riwayat transaksi sebelumnya, blockchain menjadi sistem yang transparan dan aman untuk mengelola data transaksi secara desentralisasi.

Sejak diperkenalkan pada tahun 2009, Bitcoin telah menjadi salah satu mata uang digital yang paling dikenal dan diterima secara global. 
Daya tarik utama Bitcoin sebagai instrumen investasi terletak pada sifat desentralisasinya, yang mengurangi ketergantungan terhadap lembaga keuangan konvensional dan pemerintah. 
Selain itu, jumlah Bitcoin yang terbatas, yaitu hanya 21 juta sehingga menambahkan unsur kelangkaan yang dapat meningkatkan nilai pasar [1]. 
Kehadirannya sebagai “emas digital” telah menarik minat tinggi di kalangan investor, baik individu maupun institusi, yang melihatnya sebagai aset perlindungan terhadap inflasi dan ketidakpastian ekonomi.

Namun, harga Bitcoin terkenal sangat fluktuatif, dengan perubahan harga yang tajam dalam waktu singkat. 
Sebagai contoh, harga Bitcoin melonjak dari $5.033,42 pada 16 Maret 2020 menjadi $63.564,48 pada 13 April 2021, sebuah peningkatan sebesar 1.062,85% dalam waktu hanya 13 bulan. 
Setelah harga Bitcoin mencapai puncaknya pada pertengahan April, harga tersebut turun tajam menjadi $31.634,16 pada 21 Juni 2021, anjlok hampir setengahnya [4]. 
Fluktuasi harga ini dipengaruhi oleh berbagai faktor, termasuk sentimen pasar, kebijakan regulasi pemerintah, serta berita atau peristiwa yang muncul terhadap Bitcoin [2]. 
Ketidakpastian ini menjadi tantangan bagi investor dalam merumuskan strategi investasi yang efektif.

Oleh karena itu, penting bagi investor untuk memiliki alat yang dapat membantu mereka memahami dan memprediksi pergerakan harga Bitcoin di masa mendatang, 
salah satunya yaitu penerapan teknik machine learning [2]. Penerapan teknik machine learning dalam prediksi harga Bitcoin memungkinkan analisis pola kompleks dari berbagai variabel historis. 
Teknik ini dapat mengidentifikasi hubungan non-linear antara variabel dan menghasilkan prediksi yang lebih akurat dibandingkan metode tradisional

Dengan memanfaatkan analisis fundamental cryptocurrency, termasuk kapitalisasi pasar, yang mencerminkan nilai total Bitcoin yang beredar, volume transaksi yang menunjukkan likuiditas, 
serta pergerakan harga historis [3], faktor faktor ini dapat memberikan wawasan yang mendalam kepada investor tentang kekuatan dan potensi pertumbuhan Bitcoin di masa depan. 
Meskipun demikian, model prediksi dalam proyek ini hanya didasarkan pada data historis yang mencakup harga pembukaan, harga penutupan, harga tertinggi, harga terendah, volume transaksi, 
dan kapitalisasi pasar, sehingga tidak mencakup faktor eksternal lain yang juga mempengaruhi harga, seperti sentimen pasar atau regulasi.

Melalui analisis dan model prediksi yang akurat, investor dapat memperkirakan pergerakan harga Bitcoin dalam jangka waktu tertentu, 
sehingga dapat mengurangi risiko investasi dan memaksimalkan peluang keuntungan. Oleh karena itu, 
pengembangan model prediksi harga Bitcoin sangat penting bagi investor dalam menavigasi pasar yang dinamis dan kompleks ini.

## Business Understanding
Investor cryptocurrency, khususnya Bitcoin, adalah individu yang berusaha mendapatkan keuntungan dari fluktuasi harga aset digital. Dalam dunia investasi Bitcoin, kemampuan untuk menganalisis data historis seperti harga pembukaan, harga penutupan, harga tertinggi, harga terendah, volume transaksi, dan kapitalisasi pasar merupakan keahlian penting. Melalui analisis ini, investor berupaya memprediksi pergerakan harga Bitcoin di masa depan berdasarkan pola historis yang ada.

Bitcoin terkenal dengan volatilitasnya yang tinggi, di mana harga dapat berfluktuasi secara signifikan dalam waktu singkat. Prediksi yang terlalu optimis dapat menyebabkan kerugian besar, sementara sikap terlalu konservatif bisa mengakibatkan kehilangan peluang investasi yang berpotensi menguntungkan. Oleh karena itu, diperlukan sebuah metode yang mampu mengelola ketidakpastian ini dengan lebih akurat.

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

## Data Understanding
Data yang akan digunakan pada proyek kali ini adalah [Cryptocurrency Historical Prices](https://www.kaggle.com/datasets/sudalairajkumar/cryptocurrencypricehistory) yang diunduh dari kaggle dan [Historical Bitcoin Price](https://coinmarketcap.com/currencies/bitcoin/historical-data/) dari coinmarketcap. Untuk memudahkan pendefinisiannya, dataset dari kaggle akan disebut sebagai dataset pertama, sedangkan dataset dari coinmarketcap akan disebut sebagai dataset kedua.

Dataset pertama memiliki rentang waktu dari 29 April 2013 sampai 7 Juli 2021, sedangkan dataset kedua memiliki rentang waktu dari 8 Juli 2021 sampai 19 Oktober 2024.
Nantinya kedua dataset tersebut akan digabungkan, dengan menggabungkan kedua dataset, model dapat belajar dari berbagai kondisi pasar dan menangkap perubahan pola yang terjadi seiring waktu. Hal ini memungkinkan model untuk memberikan prediksi yang lebih akurat dan adaptif terhadap dinamika pasar kripto yang kompleks.

Dataset pertama berisi 2991 records dan 10 kolom yang memiliki karakteristik sebagai berikut:
- SNo: Nomor urut atau indeks data.
- Name: Nama aset, dalam kasus ini, "Bitcoin".
- Symbol: Simbol ticker untuk aset.
- Date: Tanggal data harga.
- High: Harga tertinggi yang dicapai Bitcoin pada hari tersebut.
- Low: Harga terendah yang dicapai Bitcoin pada hari tersebut.
- Open: Harga pembukaan Bitcoin pada hari tersebut.
- Close: Harga penutupan Bitcoin pada hari tersebut.
- Volume: Volume perdagangan Bitcoin pada hari tersebut.
- Marketcap: Kapitalisasi pasar Bitcoin pada hari tersebut, yang merupakan produk dari harga penutupan dan jumlah Bitcoin yang beredar.

Kemudian, dataset kedua berisi 1200 records dan 12 kolom yang memiliki karakteristik sebagai berikut:
- timeOpen: Menandakan waktu di mana pasar dibuka untuk perdagangan pada hari tersebut. 
- timeClose: Menandakan waktu di mana pasar ditutup untuk perdagangan pada hari tersebut.
- timeHigh: Menandakan waktu di mana harga tertinggi tercapai pada hari tersebut.
- timeLow: Menandakan waktu di mana harga terendah tercapai pada hari tersebut.
- name: Menunjukkan nama aset yang diperdagangkan, dalam hal ini Bitcoin.
- open: Harga pembukaan Bitcoin pada hari tersebut.
- high:Harga tertinggi yang dicapai Bitcoin pada hari tersebut.
- low:  Harga terendah yang dicapai Bitcoin pada hari tersebut.
- close: Harga penutupan Bitcoin pada hari tersebut.
- volume: olume perdagangan Bitcoin pada hari tersebut.
- marketCap: Kapitalisasi pasar Bitcoin pada hari tersebut, yang merupakan produk dari harga penutupan dan jumlah Bitcoin yang beredar.
- timestamp: Ini adalah stempel waktu yang mencatat kapan data tersebut direkam.

Untuk memahami data, selanjutnya akan dilakukan proses berikut:
### 1. Data Loading
Supaya isi dataset lebih mudah dipahami, kita perlu melakukan proses loading data terlebih dahulu dengan import library pandas untuk dapat membaca file datanya.
### 2. Exploratory Data Analysis
#### Informasi Dataset
Mengecek informasi pada dataset dengan fungsi info() berikut.
<br>

<!-- ![image](https://github.com/user-attachments/assets/03f174aa-ab23-40d8-84cb-ae3f14faac6c) -->

<img src="https://github.com/user-attachments/assets/03f174aa-ab23-40d8-84cb-ae3f14faac6c" alt="image" width="300"/>

<br>

Berdasarkan informasi di atas dataset pertama memiliki beberapa kriteria antara lain:
- 6 Kolom dengan tipe float64 yaitu High, Low, Open, Close, Volume, dan Marketcap
- 1 Kolom dengan tipe int64 yaitu SNo
- 3 Kolom dengan tipe object yaitu Name, Symbol, dan Date

<br>

Kemudian untuk dataset kedua juga menggunakan fungsi yang sama.
<br>

<!-- ![image](https://github.com/user-attachments/assets/ce85ffc1-4b54-46b8-8cf9-5eb3c488aacb) -->

<img src="https://github.com/user-attachments/assets/ce85ffc1-4b54-46b8-8cf9-5eb3c488aacb" alt="image" width="300"/>
<br>

Berdasarkan informasi di atas dataset kedua memiliki beberapa kriteria antara lain:
- 10 Kolom dengan tipe object yaitu timeOpen, timeClose, timeHigh, timeLow, open, high, low, close, volume, marketCap
- 1 Kolom dengan tipe datetime[ns, UTC] yaitu timestamp
- 1 Kolom dengan tipe int64 yaitu name

#### Cek Missing Value
Jika data terdiri dari ratusan bahkan ribuan baris tentu akan susah dalam menemukan nilai field yang kosong. Oleh karena itu, Pandas memungkinkan kita dapat menemukan missing value secara cepat dengan fungsi isna() dan sum().
<br>

<p align="left">
  <img src="https://github.com/user-attachments/assets/8efec933-e14f-431e-aee8-0d8c120727d9" alt="dataset 1" width="100"/>
  <img src="https://github.com/user-attachments/assets/dfcaa49b-937a-4485-aaca-3bf6caa8a8e9" alt="dataset 2" width="100"/>
</p>

<!-- ![image](https://github.com/user-attachments/assets/8efec933-e14f-431e-aee8-0d8c120727d9) -->
<!-- ![image](https://github.com/user-attachments/assets/dfcaa49b-937a-4485-aaca-3bf6caa8a8e9) -->

Pada dataset pertama dan kedua tidak ditemukan adanya missing value, sehingga bisa dilanjutkan ke proses berikutnya.

#### Merge Dataset
Sebelum melakukan visualisasi dan pengembangan model, langkah awal yang krusial adalah menggabungkan kedua dataset yang ada. Tujuannya adalah untuk mendapatkan satu dataset yang komprehensif, berisi data yang relevan, dan siap untuk dianalisis lebih lanjut.

Langkah-langkah yang Dilakukan:
##### 1. Seleksi Kolom:
- Pilih kolom date, high, low, open, close, volume, dan marketcap dari kedua dataset.
- Perubahan: Untuk dataset 2, ekstrak tanggal dari kolom timestamp dan simpan ke dalam kolom baru yang bernama date.

##### 2. Konversi Tipe Data:
- Pastikan tipe data pada kolom yang sama di kedua dataset konsisten.
- Konversi tipe data kolom date pada dataset kedua menjadi format tanggal yang sesuai.

##### 3. Penggabungan Dataset:
- Menggunakan metode concat untuk menggabungkan kedua dataset secara vertikal untuk menambahkan baris data dari dataset kedua ke akhir dataset pertama.

Dari ketiga langkah tadi, didapatkan dataset baru dari hasil penggabungan dataset pertama dan kedua. 
Untuk selanjutnya hasil penggabungan ini akan disebut sebagai dataset final.

<!-- ![image](https://github.com/user-attachments/assets/a1b03191-0ae4-4fe7-8449-6ea8031f36f7) -->

<img src="https://github.com/user-attachments/assets/a1b03191-0ae4-4fe7-8449-6ea8031f36f7" alt="image" width="570"/>


#### Analisis Tren Harga
<!-- ![image](https://github.com/user-attachments/assets/38a9a029-c739-485b-8c64-05391bf9ae3d) -->

<img src="https://github.com/user-attachments/assets/38a9a029-c739-485b-8c64-05391bf9ae3d" alt="image" width="680"/>

Dari visualisasi di atas nampak beberapa informasi di antaranya:
- Tren Keseluruhan: Terlihat adanya tren peningkatan harga Bitcoin secara umum selama periode tersebut.
Volatilitas: Terdapat periode fluktuasi harga yang signifikan, menunjukkan volatilitas yang tinggi. Misalnya, peningkatan dan penurunan harga yang tajam dapat diamati pada rentang waktu tertentu, seperti di tahun 2021.
- Hubungan antar harga: Harga pembukaan, penutupan, tertinggi, dan terendah cenderung bergerak bersama-sama, yang mengindikasikan adanya korelasi antara berbagai aspek aktivitas harga harian Bitcoin.

#### Analisis Volatilitas Perubahan Harga
Volatilitas adalah ukuran statistik yang menggambarkan tingkat perubahan atau fluktuasi harga suatu aset dalam periode waktu tertentu. Dalam konteks Bitcoin, volatilitas sering digunakan untuk mengukur risiko atau ketidakstabilan harga dari waktu ke waktu.

Untuk menghitung volatilitas harga Bitcoin, berikut langkah-langkahnya:

1. Perubahan Persentase Harga (Return): Perubahan harga harian dihitung menggunakan percentage change atau persentase perubahan harga penutupan dari satu hari ke hari berikutnya:
   ```math
    {P_t} = \frac{C_t - C_{t-1}}{C_{t-1}}
    ```

   Di mana:
   ```math
   \begin{aligned}
    P_t & = \text{Return harian pada hari } t, \; \textit{persentase perubahan harga penutupan.}\\
    C_t & = \text{Harga penutupan pada hari } t, \; \textit{harga Bitcoin di akhir hari perdagangan.}\\
    C_{t-1} & = \text{Harga penutupan pada hari } t-1, \; \textit{harga Bitcoin di akhir hari sebelumnya.}
   \end{aligned}
   ```
   
   
2. Standar Deviasi dari Return: Untuk mengukur volatilitas, diperlukan menghitung standar deviasi dari return harian. Standar deviasi mengukur seberapa jauh perubahan harga harian bervariasi dari nilai rata-ratanya. Semakin besar standar deviasi, semakin tinggi volatilitas harga Bitcoin.
    ```math
    {\sigma} = \sqrt{\frac{1}{N-1} \sum_{i=1}^{N} (R_i - \bar{R})^2}
    ```

   Di mana:
   ```math
   \begin{aligned}
   {\sigma} & = \text{Standar deviasi dari return, mengukur volatilitas harga.}\\
   N & = \text{Jumlah total observasi return (hari).}\\
   R_i & = \text{Return harian pada hari ke-} i, \; \text{perubahan persentase harga.}\\
   \bar{R} & = \text{Rata-rata return harian, memberikan nilai tengah dari semua return.}
   \end{aligned}
   ```
  
3. Penyesuaian ke Periode Tertentu (Misalnya Mingguan, Bulanan): Untuk mengukur volatilitas dalam rentang waktu tertentu, misalnya mingguan atau bulanan, standar deviasi harian disesuaikan dengan mengalikan akar kuadrat dari jumlah hari dalam periode tersebut:
   ```math
    \text{Volatilitas Periodik} = \sigma \times \sqrt{T}
    ```

   Di mana:
   ```math
   \begin{aligned}
     \text{Volatilitas Periodik} & = \text{Mengukur volatilitas dalam periode tertentu (mingguan, bulanan).}\\
    \sigma & = \text{Standar deviasi dari return harian, menggambarkan volatilitas harian.}\\
    T & = \text{Jumlah hari dalam periode yang dianalisis (contoh: 7 untuk mingguan, 30 untuk bulanan).}
   \end{aligned}
   ```

##### Volatilitas Jangka Pendek (7 Hari)
<!-- ![image](https://github.com/user-attachments/assets/39eefb2e-988f-4b9c-8330-07218ab0a0a6) -->

<img src="https://github.com/user-attachments/assets/39eefb2e-988f-4b9c-8330-07218ab0a0a6" alt="image" width="680"/>

##### Volatilitas Jangka Menengah (30 Hari)
<!-- ![image](https://github.com/user-attachments/assets/7e57deb6-3da2-4287-8b82-fbbe702134ff) -->

<img src="https://github.com/user-attachments/assets/7e57deb6-3da2-4287-8b82-fbbe702134ff" alt="image" width="680"/>

##### Volatilitas Jangka Panjang (90 Hari)
<!-- ![image](https://github.com/user-attachments/assets/67b10d59-0271-4d61-af0b-354e7fb410c3) -->

<img src="https://github.com/user-attachments/assets/67b10d59-0271-4d61-af0b-354e7fb410c3" alt="image" width="680"/>
<br>

Dari ketiga visualisasi tingkat volatilitas harga Bitcoin tersebut didapatkan beberapa informasi di antaranya:
- Volatilitas Tinggi pada 2013-2014 dan 2017-2018: Terlihat lonjakan volatilitas yang signifikan pada periode tersebut, mengindikasikan fluktuasi harga Bitcoin yang besar. Periode tersebut bertepatan dengan bubble dan koreksi harga Bitcoin
- Volatilitas Menurun seiring Waktu: Secara umum, volatilitas Bitcoin cenderung menurun seiring waktu, meskipun masih terdapat periode dengan volatilitas tinggi
- Volatilitas Jangka Panjang lebih Stabil: Volatilitas 90 hari (jangka panjang) cenderung lebih stabil dibandingkan dengan volatilitas mingguan dan bulanan. Hal ini menunjukkan bahwa fluktuasi harga Bitcoin cenderung mereda dalam jangka waktu yang lebih panjang


#### Rata-Rata Pergerakan Harga
Rata-rata Pergerakan Sederhana (Simple Moving Average - SMA) adalah metode perataan data harga dalam periode waktu tertentu untuk membantu mengidentifikasi tren dalam harga aset, seperti Bitcoin.

Perhitungan SMA dilakukan dengan cara mengambil rata-rata harga penutupan aset selama sejumlah hari tertentu, kemudian menggeser (rolling) jendela waktu tersebut setiap harinya untuk mendapatkan nilai SMA terbaru. Dengan cara ini, fluktuasi harga harian dapat dihaluskan sehingga tren harga lebih mudah dianalisis.

```math
\text{SMA}n = \frac{C_t + C{t-1} + C_{t-2} + \dots + C_{t-n+1}}{n} 
```

Di mana:
```math
\begin{aligned}
\text{SMA}_n & = \text{Simple Moving Average untuk periode } n \text{ hari.} \\[10pt] 
C_t & = \text{Harga penutupan pada hari ke-} t.\\[10pt] 
n & = \text{Jumlah hari dalam periode perhitungan SMA.}
\end{aligned}
```

<br>

Untuk SMA jangka pendek - menengah akan digunakan periode 50 hari, sedangkan untuk jangka panjang akan digunakan periode 200 hari.

***Mengapa 50 dan 200 Hari?***

- SMA-50 sering digunakan untuk mengukur tren jangka pendek hingga menengah. Periode 50 hari dianggap cukup untuk menunjukkan fluktuasi harga terbaru tanpa terlalu banyak "noise" dari pergerakan harga harian
- SMA-200 adalah indikator yang lebih umum digunakan untuk melihat tren jangka panjang. Periode ini cukup panjang untuk memberikan gambaran stabil tentang pergerakan harga dan menghilangkan fluktuasi harian yang tidak signifikan

<!-- ![image](https://github.com/user-attachments/assets/ffdc757a-7579-4862-ac04-5b4f40018d34) -->
<br>

<img src="https://github.com/user-attachments/assets/ffdc757a-7579-4862-ac04-5b4f40018d34" alt="image" width="680"/>

Dari visualasi di atas, didapatkan informasi sebagai berikut:

SMA-200 bertindak sebagai support (level harga di mana tren penurunan cenderung berhenti) dalam jangka panjang, sedangkan SMA-50 bertindak sebagai support dan resistance (level harga di mana tren kenaikan cenderung berhenti) dalam jangka pendek dan menengah.

- Golden Cross: Ketika SMA-50 memotong SMA-200 dari bawah ke atas, ini menandakan potensi dimulainya tren kenaikan harga (bullish)
- Death Cross: Ketika SMA-50 memotong SMA-200 dari atas ke bawah, ini menandakan potensi dimulainya tren penurunan harga (bearish)

#### Korelasi antara Harga Penutupan dengan Volume Transaksi
<!-- ![image](https://github.com/user-attachments/assets/37e5907e-aa66-454f-a02e-4872012475dc) -->

<img src="https://github.com/user-attachments/assets/37e5907e-aa66-454f-a02e-4872012475dc" alt="image" width="680"/>

<!-- ![image](https://github.com/user-attachments/assets/718743d9-1052-4142-9697-f08963e50caa) -->

<img src="https://github.com/user-attachments/assets/718743d9-1052-4142-9697-f08963e50caa" alt="image" width="680"/>

<!-- ![image](https://github.com/user-attachments/assets/f6f5a108-c2d7-4bcf-b38f-81f1c019cfae) -->

<img src="https://github.com/user-attachments/assets/f6f5a108-c2d7-4bcf-b38f-81f1c019cfae" alt="image" width="400"/>


Dari kedua visualisasi di atas dan hasil perhitungan korelasi, didapatkan informasi sebagai berikut:
- Sebaran titik-titik pada scatter plot menunjukkan adanya ketidaklinearan dalam hubungan antara harga dan volume. Titik-titik tidak membentuk pola garis lurus yang jelas, mengindikasikan faktor-faktor lain mungkin memengaruhi volume selain dari harga, seperti sentimen pasar, berita, dan regulasi, juga dapat memengaruhi volume transaksi Bitcoin dan perlu dipertimbangkan dalam analisis yang lebih komprehensif
- Meskipun umumnya positif, korelasi antara harga penutupan dan volume transaksi tidak selalu konsisten, ditunjukkan oleh fluktuasi pada grafik korelasi bergilir. Terdapat periode di mana korelasi melemah atau bahkan berbalik arah
- Nilai korelasi 0.67 menunjukkan hubungan yang cukup kuat, namun ketidaklinearan pada scatter plot mengingatkan kita bahwa korelasi tidak selalu berarti hubungan sebab-akibat yang sederhana

Setelah tahap visualisasi selesai, kolom-kolom yang sudah tidak diperlukan seperti Volatilitas Mingguan, Volatilitas Bulanan, Volatilitas Jangka Panjang, SMA-50, SMA-200, Korelasi Bergilir (30 Hari) akan dihapus.

## Data Preparation
Pada bagian ini akan dilakukan beberapa persiapan data yaitu:

### 1. Membagi Feature dan Target serta Shifting Data
Dalam rangka memprediksi harga Bitcoin untuk 5 hari ke depan, langkah pertama adalah membagi feature dan target. Numerical feature yang digunakan terdiri dari kolom high, low, open, close, volume, dan marketcap. Target merupakan prediksi harga penutupan (closing price) Bitcoin pada hari ke-5 setelah data pada hari yang sedang diproses. Untuk menetapkan kolom target ini, digunakan teknik shifting, di mana data harga penutupan bergeser sebanyak 5 hari ke depan dengan kode berikut:
```python
mrg_df['Prediction_5D'] = mrg_df['close'].shift(-5)
```

Setelah itu, fitur numerik perlu dimundurkan 5 hari agar selaras dengan target prediksi. Hal ini dilakukan untuk memastikan bahwa model menggunakan data dari 5 hari sebelumnya sebagai dasar prediksi harga di masa depan. Kode yang digunakan untuk proses shifting adalah sebagai berikut:
```python
mrg_df['high_shifted'] = mrg_df['high'].shift(5)
mrg_df['low_shifted'] = mrg_df['low'].shift(5)
mrg_df['open_shifted'] = mrg_df['open'].shift(5)
mrg_df['volume_shifted'] = mrg_df['volume'].shift(5)
mrg_df['marketcap_shifted'] = mrg_df['marketcap'].shift(5)
```

Pemunduran fitur ini penting untuk mencegah kebocoran data, di mana model dapat "melihat" informasi dari masa depan yang seharusnya belum tersedia. Pendekatan ini sesuai dengan prinsip dalam analisis time series, di mana variabel input (fitur) harus mencerminkan periode waktu sebelum variabel target. Setelah dilakukan pemunduran data dan menghapus nilai null, kini terdapat total 4,181 baris data yang siap untuk digunakan dalam model.

### 2. Split Dataset
Membagi dataset menjadi data latih (train) dan data uji (test) merupakan hal yang harus kita lakukan sebelum membuat model. proporsi pembagian data latih dan uji adalah 80:20. Proporsi tersebut cukup ideal untuk model dengan jumlah data 4181. Namun, jika memiliki dataset berukuran besar, kita perlu memikirkan strategi pembagian dataset lain agar proporsi data uji tidak terlalu banyak.  Pembagian ini menggunakan fungsi train_test_split dari sklearn hasil yang diperoleh berikut:

<!-- ![image](https://github.com/user-attachments/assets/ffb5e6c8-e3e0-4184-a618-c18ea520ba11) -->

<img src="https://github.com/user-attachments/assets/ffb5e6c8-e3e0-4184-a618-c18ea520ba11" alt="image" width="300"/>

## Modeling
