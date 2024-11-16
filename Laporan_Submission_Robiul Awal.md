# Laporan Proyek Machine Learning Sistem Rekomendasi Produk di Amazon - Robiul Awal

## Project Overview

Dengan kemajuan teknologi dan inovasi yang terus berkembang, kehidupan masyarakat menjadi jauh lebih nyaman. Berbelanja di internet telah menjadi bagian penting dari kehidupan masyarakat. Saat ini, masyarakat lebih suka membeli produk secara daring karena mereka memiliki akses cepat ke berbagai jenis barang dalam satu platform. Namun, mereka menghabiskan banyak waktu di situs web komersial daring untuk mengevaluasi kualitas produk dan membaca ulasan produk untuk mendapatkan wawasan tentang produk tertentu. Menemukan barang yang sesuai dengan pilihan pengguna merupakan pilihan yang sangat sulit karena membutuhkan banyak waktu dan tenaga untuk memeriksa semua produk satu per satu secara manual (Ahmed, Md Zaid & Singh, Abhay & Paul, Abir & Ghosh, Sayantani & Chaudhuri, Avijit. 2022).

Dalam lingkungan digital, pelanggan juga tidak dapat menyentuh atau menguji kualitas produk secara fisik. Akibatnya, masyarakat bergantung pada umpan balik pelanggan lain untuk memperoleh pengetahuan tentang produk yang ingin mereka beli. Namun, masyarakat mengalami kesulitan menemukan ulasan yang diinginkan karena umpan balik dan komentar yang tidak perlu. Oleh karena itu, diperlukan suatu sistem yang dapat membantu pelanggan menemukan ulasan yang relevan dengan cepat, menyaring ribuan komentar, dan membantu pengguna menghemat waktu dan tenaga dengan merekomendasikan produk yang sesuai (Ahmed, Md Zaid & Singh, Abhay & Paul, Abir & Ghosh, Sayantani & Chaudhuri, Avijit. 2022).

Amazon adalah salah satu platform e-commerce terbesar dan paling terkenal di dunia, dengan menawarkan berbagai macam produk mulai dari buku, elektronik, pakaian, hingga kebutuhan sehari-hari. Sebagai perusahaan e-commerce global, Amazon memiliki jutaan produk yang tersedia untuk pelanggan di berbagai negara. Keberagaman produk yang sangat luas ini memberikan keuntungan bagi konsumen karena mereka memiliki banyak pilihan, tetapi juga menciptakan tantangan bagi Amazon untuk membantu pelanggan menemukan produk yang paling relevan sesuai dengan kebutuhan dan preferensi mereka. Dalam konteks ini, sistem rekomendasi menjadi sangat penting sebagai alat untuk meningkatkan pengalaman berbelanja pelanggan dan mengoptimalkan penjualan.

Masalah utama yang dihadapi oleh e-commerce seperti Amazon adalah bagaimana cara menyajikan produk yang relevan dan menarik kepada pengguna secara efisien. Dengan banyaknya jumlah produk dan variasi kategori, pelanggan seringkali merasa kesulitan dalam mencari produk yang sesuai di tengah lautan pilihan yang ada. Selain itu, masalah "information overload" atau kebanjiran informasi juga sering muncul, di mana terlalu banyak pilihan dapat membuat pelanggan kesulitan dalam mengambil keputusan. Tantangan lain adalah "cold start" atau kesulitan memberikan rekomendasi akurat untuk produk baru atau pengguna baru yang belum memiliki banyak interaksi di platform. Tantangan ini menuntut adanya sistem yang dapat menyaring, memprioritaskan, dan menyajikan produk yang paling relevan bagi setiap pengguna.

Sistem rekomendasi muncul sebagai solusi efektif untuk mengatasi masalah-masalah ini dengan memberikan saran produk yang disesuaikan berdasarkan data pengguna, seperti riwayat pencarian, pembelian, dan penilaian produk. Sistem rekomendasi telah mengubah cara interaksi antara pengguna dan situs web dan semakin penting saat ini. Sistem rekomendasi meningkatkan akses dan bertanggung jawab untuk merekomendasikan item yang sesuai kepada pengguna dengan mempertimbangkan pilihan dan perilaku objektif pengguna. Sebagai situs web iklan daring atau e-commerce, sistem rekomendasi tidak dapat dihindari saat ini. Setiap perusahaan lain mencoba menggunakan kekuatan sistem rekomendasi (Dwivedi, Rohit & Anand, Abhineet & Johri, Prashant & Banerji, Arpit & Gaur, N. 2020).

### Penjelasan mengapa proyek ini penting untuk diselesaikan.

Solusi ini tidak hanya membantu dalam menyederhanakan proses pencarian bagi pelanggan, tetapi juga meningkatkan nilai bisnis. Dengan memberikan rekomendasi yang relevan, Amazon dapat meningkatkan tingkat konversi penjualan dan mendorong pengguna untuk mengeksplorasi produk lain yang mungkin tidak mereka pertimbangkan sebelumnya. Selain itu, sistem rekomendasi juga dapat meningkatkan loyalitas pengguna dengan menghadirkan pengalaman belanja yang lebih personal dan terarah. Meskipun masih ada tantangan dalam meningkatkan akurasi dan mengatasi masalah "cold start," sistem rekomendasi telah terbukti menjadi alat yang sangat berguna dalam memaksimalkan potensi e-commerce dan menghadirkan pengalaman belanja yang lebih menyenangkan bagi pelanggan.

## Business Understanding

Dalam pengembangan sistem rekomendasi produk untuk e-commerce seperti Amazon, proses klarifikasi masalah atau business understanding bertujuan untuk memahami tujuan bisnis dan masalah yang ingin diselesaikan. Amazon adalah salah satu platform e-commerce terbesar di dunia, dengan jutaan produk yang tersedia. Tujuan utamanya adalah meningkatkan penjualan dan menjaga kepuasan pelanggan. Untuk mencapai tujuan tersebut, Amazon perlu menyediakan pengalaman belanja yang dipersonalisasi bagi setiap pengguna, sehingga pengguna dapat menemukan produk yang relevan dengan minat dan kebutuhannya secara lebih efisien. Namun, terdapat beberapa masalah atau tantangan yang dihadapi antara lain, volume produk yang sangat besar, keberagaman preferensi pengguna, informasi yang terlalu banyak (information overload), dan peningkatan konversi dan retensi pengguna. Amazon memiliki jutaan produk di berbagai kategori. Dengan banyaknya pilihan, pengguna mungkin merasa kewalahan untuk menemukan produk yang tepat. Setiap pengguna memiliki preferensi dan kebutuhan yang unik, sehingga produk yang relevan untuk satu pengguna mungkin tidak relevan bagi pengguna lain. Dengan banyaknya produk dan ulasan, pengguna mungkin mengalami kesulitan menyaring informasi untuk menemukan produk yang sesuai. Amazon perlu mendorong pengguna untuk membeli lebih banyak produk dan mengunjungi kembali platform secara rutin. Tanpa rekomendasi yang tepat, pengguna mungkin kehilangan minat atau beralih ke platform lain. Berdasarkan hal ini dapat dirumuskan beberapa problem statements seperti berikut ini.

### Problem Statements

- Berdasarkan data mengenai pengguna, bagaimana membuat sistem rekomendasi yang dipersonalisasi dengan teknik content-based filtering?
- Dengan data rating yang dimiliki, bagaimana perusahaan dapat merekomendasikan produk lain yang mungkin disukai dan belum pernah dibeli oleh pengguna?

### Goals

- Menghasilkan sejumlah rekomendasi produk yang dipersonalisasi untuk pengguna dengan teknik content-based filtering.
- Menghasilkan sejumlah rekomendasi produk yang sesuai dengan preferensi pengguna dan belum pernah dibeli sebelumnya dengan teknik collaborative filtering.

- Menambahkan bagian “Solution Approach” yang menguraikan cara untuk meraih goals. Bagian ini dibuat dengan ketentuan sebagai berikut:

### Solution Approach

Sistem rekomendasi dapat menggunakan berbagai algoritma seperti content-based filtering, collaborative filtering, dan hybrid methods untuk menghasilkan daftar produk yang relevan bagi pengguna. Pada proyek ini, algoritma yang digunakan adalah content-based filtering dan collaborative filtering. Content-based filtering merekomendasikan produk yang serupa dengan produk yang pernah diminati atau dibeli pengguna sebelumnya, berdasarkan fitur-fitur produk (misalnya kategori, deskripsi, harga). Algoritma yang satu ini menggunakan pendekatan hitungan jarak antar variabel menggunakan formula cosine similarity untuk menentukan kesamaan. Sedangkan, Collaborative filtering menggunakan data dari pengguna lain yang memiliki preferensi serupa untuk merekomendasikan produk. Teknik collaborative filtering menggunakan pendekatan deep learning sebagai model yang dapat memprediksi rekomendasi yang tepat beradasarkan training dan testing. Dengan berbagai pendekatan solusi di atas, sistem rekomendasi di Amazon dapat dioptimalkan untuk mencapai tujuan bisnis seperti meningkatkan penjualan, memperbaiki pengalaman pengguna, dan meningkatkan retensi pelanggan.

Terdapat dua matriks evaluasi yang digunakan sesuai dengan algoritma yang digunakan. Metrik evaluasi dapat digunakan untuk mengukur seberapa baik sistem tersebut memberikan rekomendasi kepada pengguna. Matriks evaluasi yang digunakan pada algoritma content-based filtering dalam mengevaluasi sistem rekomendasi yang menggunakan teknik cosine_similarity, adalah matrik precision. Precision mengukur proporsi item relevan yang direkomendasikan. Dalam konteks sistem rekomendasi, precision dihitung sebagai rasio antara jumlah rekomendasi yang benar-benar relevan terhadap total jumlah item yang direkomendasikan. Sedangkan pada algoritma collaborative filtering digunakan matriks evaluasi Root Mean Squared Error (RMSE). RMSE adalah metrik evaluasi yang sering digunakan dalam sistem rekomendasi untuk mengukur seberapa baik prediksi model terhadap data yang sebenarnya. RMSE mengukur rata-rata dari kuadrat selisih antara nilai yang diprediksi oleh model dan nilai yang sebenarnya, kemudian diakarkan. Metrik ini memberikan gambaran tentang seberapa jauh prediksi dari nilai aktual dalam satuan skala yang sama dengan data asli.

## Data Understanding

Kumpulan data pertama ini terdiri dari koleksi ekstensif lebih dari 2 juta ulasan dan peringkat pelanggan untuk produk terkait kecantikan yang tersedia di platform Amazon. Lebih tepatnya dataset customer_ratings terdiri dari 1.048.575 baris dengan 4 kolom. Kumpulan data tersebut mencakup informasi penting seperti ID Pengguna Unik, ASIN, Peringkat, dan stempel waktu sebagai 4 kolom tersebut (Ahmed Ali. 2023).

Kumpulan data ini hanyalah sebagian kecil dari kumpulan data produk Amazon yang luas, yang mencakup 142,8 juta ulasan yang mencakup periode dari Mei 1996 hingga Juli 2014. Kumpulan data lengkap menyediakan banyak informasi, termasuk ulasan produk terperinci, metadata, informasi kategori, data harga, detail merek, dan bahkan fitur gambar (Ahmed Ali. 2023).

Dengan kumpulan data kedua, Anda bisa mendapatkan gambaran mendalam tentang produk mana yang paling laku, judul SEO mana yang menghasilkan penjualan terbanyak, kisaran harga terbaik untuk produk dalam kategori tertentu, dan banyak lagi (Asaniczka. 2024).

Kumpulan data ini terdiri dari dua kumpulan data, amazon_products.csv dan amazon_categories.csv. Dataset kedua yaitu amazon_categories yang tediri dari 248 baris dengan 2 kolom yaitu id dan category_name. Dataset ketiga yaitu amazon_products yang terdiri dari 1.426.337 baris dengan 11 kolom yaitu asin, title, imgUrl, productURL, stars, reviews, price, listPrice, category_i, isBestSeller, boughtInLastMonth.

Kedua kumpulan data ini dapat dihubungkan melalui hubungan kunci asing, di mana kolom ‘category_id’ dalam ‘amazon_products’ merujuk ke kolom ‘id’ dalam ‘amazon_categories’, yang memungkinkan kita untuk menghubungkan setiap produk ke kategori yang sesuai (Asaniczka. 2024). Kumpulan data besar berisi 1,4 juta produk Amazon. Termasuk judul, jumlah ulasan, peringkat, harga, dan data penjualan dari September 2023 (Asaniczka. 2024).

### Sumber Data

Pengumpulan data dilakukan dengan mengunduh dataset dari sumber referensi resmi dari Kaggle yaitu pada link berikut:
[Customer Rating Data By Amazon](https://www.kaggle.com/datasets/ahmedaliraja/customer-rating-data-by-amazon)
[Amazon Products Dataset 2023 (1.4M Products)](https://www.kaggle.com/datasets/asaniczka/amazon-products-dataset-2023-1-4m-products)

### Definisi Variabel

Kumpulan data pertama yaitu customer_ratings yang terdiri dari 4 variabel beserta penjelasannya berikut ini:

- User Id: merupakan ID pengguna Unik untuk identifikasi pelanggan.
- Product Id : merupakan ASIN produk (pengidentifikasi produk unik Amazon).
- rating : merupakan rating yang mencerminkan kepuasan pelanggan pada skala 1 hingga 5.
- timestamp : merupakan Waktu yang dicatat dalam waktu UNIX, yang menunjukkan kapan peringkat tersebut dikirimkan.

Kumpulan data kedua yaitu amazon_products yang teridiri dari 11 variabel beserta penjelasannya sebagai berikut ini:

- asin : merupakan product id yang dimiliki setiap produk unik.
- title : merupakan nama dari produk.
- imgUrl : merupakan link gambar dari produk.
- productURL : merupakan link yang menuju aplikasi amazon dari produk.
- stars : merupakan nilai total rating yang diberikan kepada produk.
- reviews : merupakan jumlah review yang diberikan kepada produk.
- price : merupakan besaran harga dari produk.
- listPrice : merupakan list dari harga produk.
- category_id : merupakan id kategori dari produk.
- isBestSeller : merupakan nilai benar atau salah terkait apakah produk masuk dalam kategori best seller atau tidak.
- boughtInLastMonth : jumlah pembelian dalam bulan terakhir dari produk.

Kumpulan data ketiga yaitu amazon_categories yang terdiri dari 2 variabel beserta penjelasannya sebagai berikut ini:

- id : merupakan id yang dimiliki oleh kategori produk.
- category_name : merupakan nama dari kategori produk.

### Exploratory Data Analysis

Pada proyek ini dilakukan juga proses exploratory data analysis (EDA). EDA merupakan proses investigasi awal pada data untuk menganalisis karakteristik, menemukan pola, anomali, dan memeriksa asumsi pada data. Teknik ini biasanya menggunakan bantuan statistik dan representasi grafis atau visualisasi. Proses ini untuk mengetahui beberapa hal seperti berikut ini:

- Apa saja jenis variabel pada dataset?
  Untuk menetahui jenis variabel pada dataset sudah dilakukan sebelumnya yaitu memahami definsi dari setiap variabeldengan teknik univariate analisis. Kemudian menggunakan perintah `dataset.info()` untuk mengetahui tipe dari setiap variabel dalam masing-msaing dataset. Berdasarkan output dari `amazon_categories.info()`, dapat dilihat bahwa ada 2 variabel dalam amazon_categories. Variabel id memiliki tipe data int 64 sedangkan variabel category_name memiliki tipe objek atau karakter. Terdapat 248 kategori di dalam dataset amazon_categories. - Berdasarkan output `amazon_products.info()`, dapat dilihat bahwa terdapat 4 variabel bertipe data objek, terdapat 3 variabel bertipe data numerik float64, terdapat 3 variabel bertipe data numerik int64, dan terdapat 1 variabel bertipe data bool. Yang terakhir, berdasarkan output `customer_ratings.inf()` dapat dilihat bahwa terdapat 2 variabel bertipe data objek dan terdapat 2 variabel bertipe data numerik int64.
- Apakah ada missing value?
  Untuk mengetahui nilai kosong dapat menggunakan perintah `dataNull = dataset.isnull().sum()`. Berdasarkan output, pada dataset amazon_categories tidak memiliki data kosong, pada data amaozn_product memiliki data kosong pada satu baris dan berada pada kolom title, sedangkan pada customer_ratings tidak terdapat data kosong. Oleh karena itu, jika dataset produk dengan kategori digabungkan, maka terdapat satu nilai kosong yaitu pada kolom title. Namun, ketika semua dataset digabungkan atau merge antara data produk, kategori, dan customer_ratings dengan hanya produk id yang cocok, maka akan terdapat 943067 nilai yang kosong dan terdapat pada kolom product_name, category_id, dan category_name. Pada data preparation menggunakan algoritma content-based learning, data kosong ini akan ditangani menggunakan `all_product.dropna()`.
- Apakah ada fitur yang tidak berguna (redundant)?
  Kemudian diputuskan beberapa variabel untuk dihapus karena merupakan noise atau redundant yang tidak memiliki pengaruh pada model prediksi dalam proyek ini. Pada teknik content-based filtering, fitur yang digunakan adalah product_id, product_name, dan category_name. Sedangkan pada teknik collaborative filtering fitur yang didgunakan adalah user_id, product_id, category_name, dan rating. Kemudian, category_id digunakan untuk menggabungkan dataset produk dan kategori. Oleh karena itu, pada proyek ini hanya menggunakan fitur atau variabel user_id, product_id, category_id, product_name, category_name, dan rating. Oleh karena itu, fitur-fitur yang tidak berguna, noise, atau redundant adalah variabelimgUrl, productURL, stars (total rating pada produk), reviews, price, listPrice, isBestSeller, boughtInLastMonth, dan Time stamp.
- Bagaimana distribusi variabel dalam dataset?
  Untuk mengetahui distribusi variabel dalam dataset, dilakukan analisis univariat. ![image](https://github.com/user-attachments/assets/79b8ff58-e18a-4f49-9386-9dbdce2feb41) Berdasarkan analisis unvariat diperoleh hasil bahwa hanya sekitar 0,6% saja yang merupakan produk best seller. ![image](https://github.com/user-attachments/assets/b09e3b15-c818-46f4-a7ac-c633685dc653) Dari plot di atas, dapat diperoleh informasi bahwa jumlah produk dengan rating sekitar 4,5 adalah yang terbesar. ![image](https://github.com/user-attachments/assets/ffc301be-af14-4c4b-b237-3e2f942d00f3) Berdasarkan grafik di atas, dapat diperoleh informasi bahwa rating yang paling banyak deberikan oleh customer pada produk di amazon commerce adalah rating 5, dan yang paling sedikit adalah rating 2.
- Bagaimana korelasi antara fitur dan target?
  Untuk mengetahui hal ini, dilakukan analisis multivariat. Proses dilakukan dengan cara mencari korelasi antar variabel. ![image](https://github.com/user-attachments/assets/d5c52c4c-e26c-4eac-8641-74e2ebc540b8) Dari gambar di atas, terlihat bahwa setiap variabel memiliki korelasi acak dengan variabel lainnya, kecuali variabel harga dengan harga daftar yang menunjukkan sedikit korelasi positif antara kedua variabel. ![image](https://github.com/user-attachments/assets/5a7f1f15-2bf0-4d8a-b7fa-57f2620ffc95) Sejalan dengan hasil korelasi masing-masing variabel numerik di atas, korelasi tertinggi terdapat pada korelasi antara harga dan harga pokok sebesar 0,43. Namun, variabel lainnya terlihat memiliki korelasi yang sangat lemah, bahkan sebagian besar memiliki nilai korelasi mendekati 0.

## Data Preparation

Pada proyek ini menggunakan dua algoritma untuk membentuk sistem rekomendasi produk. Setiap algoritma memiliki teknik data preparation masing-masing dan berbeda dengan algoritma lainnnya. Namun, terdapat beberapa proses data preparation yang dilakukan secara umum seperti data preprocessing. Ini adalah tahap penyiapan data sebelum data digunakan untuk proses selanjutnya. Pada tahap ini, beberapa file digabung sehingga menjadi satu kesatuan file yang utuh dan siap digunakan pada tahap pemodelan.

Berikut ini adalah perubahan nama kolom id pada amazon_categories menjadi category_id sehingga sama dengan nama kolom pada amazon_products. Berikut ini kode yang digunakan untuk mengubah nama kolom.

```
amazon_categories= amazon_categories.rename(columns={'id': 'category_id'})
```

Berikut ini adalah penggabungan amazon_products dengan amzon_categories berdasarkan category_id.

```
# Menggabungkan dataframe product dengan category berdasarkan nilai category_id
product_info = pd.merge(amazon_products, amazon_categories , on='category_id', how='left')
```

Kemudian lakukan handling data kosong pada data product info ini lalu menyimpannya pada dataset bernama clean_product_info dengan menggunakan kode berikut ini.

```
# Membersihkan missing value dengan fungsi dropna()
clean_product_info = product_info.dropna()
```

Selanjutnya akan menggabungkannya dengan dataset customer ratings. Namun sebelumnya perlu perubahan nama kolom sebagai kunci penggabungan yaitu product id. Berikut ini adalah perubahan nama kolom Product Id pada clean_product_info menjadi product_id.

```
clean_product_info = clean_product_info.rename(columns = {'asin':'product_id', 'title':'product_name'})
```

Berikut ini adalah perubahan nama kolom Product Id pada all_product_rate menjadi product_id sehingga sama dengan nama kolom pada amazon_products.

```
all_product_rate = all_product_rate.rename(columns = {'Product Id':'product_id'})
```

Berikut ini adalah penggabungan clean_product_info dengan all_product_rate berdasarkan product_id.

```
# Menggabungkan data hanya untuk 'product_id' yang cocok
all_product = pd.merge(
    all_product_rate,
    clean_product_info[['product_id', 'product_name', 'category_id', 'category_name']],
    on='product_id',
    how='left'
)
```

Selanjutnya akan dijelaskan data preparation yang dilakukan sebelum pengembangan sistem rekomendasi pada masing-masing teknik yang digunakan. Teknik data preparation yang digunakan pada algoritma content-based filtering adalah sebagai berikut:

1. Handling Missing Values
2. Handling Duplicates Values
3. Feature Selection (Pemilihan Fitur)
4. Feature Extraction

Sedangkan pada algoritma collaborative filtering menggunakan teknik data preparation sebagai berikut:

1. Feature Encoding
2. Feature Selection dan Normalisasi
3. Splitting Data

Berikut adalah penjelasan dari teknik data preparation yang digunakan dalam algoritma **content-based filtering** dan **collaborative filtering**, lengkap dengan penjelasan tentang proses yang dilakukan dan alasan mengapa tahapan tersebut diperlukan.

### Data Preparation untuk Content-Based Filtering

1. **Handling Missing Values**

   - **Proses**: Mengidentifikasi kolom atau fitur yang memiliki nilai hilang (missing values), kemudian menangani nilai-nilai tersebut. Cara penanganan pada proyek ini adalah dengan cara **Penghapusan**: Menghapus baris atau kolom yang memiliki banyak nilai hilang jika nilai tersebut dianggap tidak signifikan atau tidak memberikan informasi yang relevan dengan kode `dataset.dropna()`.
   - **Alasan Diperlukan**:
     - Data yang hilang dapat menyebabkan algoritma content-based filtering tidak dapat memproses informasi dengan baik, karena sebagian besar metode machine learning membutuhkan data yang lengkap. Menangani nilai yang hilang membantu memastikan kualitas data dan akurasi model yang lebih baik.

2. **Handling Duplicate Values**
   - **Proses**: Mengidentifikasi dan menghapus data duplikat, seperti baris yang memiliki informasi produk yang sama. Proses ini dilakukan dengan menggunakan fungsi deduplication pada DataFrame (`drop_duplicates()` pada Pandas).
   - **Alasan Diperlukan**:
     - Data duplikat dapat menyebabkan bias dalam model rekomendasi, sehingga produk yang sama mungkin disarankan berulang kali. Dengan menghapus duplikat, kita dapat memastikan bahwa rekomendasi yang diberikan lebih bervariasi dan akurat.
3. **Feature Selection**
   Feature Selection adalah proses dalam pembelajaran mesin dan statistik yang bertujuan untuk memilih subset fitur (variabel) yang paling relevan dari sekumpulan fitur yang lebih besar. Proses ini dilakukan sebelum tahap pelatihan model untuk meningkatkan kinerja dan efisiensi model. Pemilihan ini dilakukan secara manual dengan membuang variabel yang tidak berguna/redundant/noise dan mengambil variabel yang digunakan saja. Pemilihan fitur dilakukan dengan kode berikut ini.

```
# Mengonversi data series ‘product_id’ menjadi dalam bentuk list
product_id = preparation['product_id'].tolist()
# Mengonversi data series ‘Name’ menjadi dalam bentuk list
product_name = preparation['product_name'].tolist()
# Mengonversi data series ‘Rcategory’ menjadi dalam bentuk list
product_category = preparation['category_name'].tolist()
# Membuat dictionary untuk data ‘product_id’, ‘product_name’, dan ‘category’
product_new = pd.DataFrame({
    'product_id': product_id,
    'product_name': product_name,
    'category_name': product_category
})
```

Dari pengambilan tiga fitur saja pada pemodalan kali ini berarti juga terjadi pembuangan atau dropping dari variabel-variabel lain yang tidak digunakan. Jadi dari pada memilih menggunakan teknik drop(), saya memilih menggunakan teknik pengambilan nilai pada kolom seperti yang dilakukan pada kode di atas.

- **Alasan Diperlukan**:
  Meningkatkan Kinerja Model:Dengan memilih fitur yang paling relevan, model dapat lebih fokus pada informasi yang penting dan mengurangi kebisingan dari fitur yang tidak relevan, yang dapat meningkatkan akurasi prediksi.
  Mengurangi Overfitting: Dengan mengurangi jumlah fitur yang digunakan, risiko model belajar dari data noise atau pola yang tidak penting dapat diminimalkan, sehingga meningkatkan generalisasi model pada data yang belum pernah dilihat.
  Meningkatkan Pemahaman Domain: Proses seleksi fitur dapat membantu dalam mengidentifikasi fitur-fitur yang paling berpengaruh dalam memprediksi variabel target, yang dapat memberikan wawasan berharga tentang fenomena yang sedang dipelajari.

4. **Feature Extraction**
   - **Proses**: Mengambil informasi penting dari data yang ada, seperti ekstraksi kata-kata kunci dari deskripsi produk, kategori, atau ulasan pelanggan. Teknik yang digunakan adalah **TF-IDF (Term Frequency-Inverse Document Frequency)**. Teknik ini digunakan untuk mengubah teks menjadi vektor numerik yang dapat digunakan untuk menghitung kesamaan antar produk. Berikut ini kode yang digunakan untuk feature extraction.
   ```
    # Inisialisasi TfidfVectorizer
    tf = TfidfVectorizer()
    # Melakukan perhitungan idf pada data cuisine
    tf.fit(data['category_name'])
    # Mapping array dari fitur index integer ke fitur nama
    tf.get_feature_names_out()
    # Melakukan fit lalu ditransformasikan ke bentuk matrix
    tfidf_matrix = tf.fit_transform(data['category_name'])
    # Mengubah vektor tf-idf dalam bentuk matriks dengan fungsi todense()
    tfidf_matrix.todense()
   ```
   - **Alasan Diperlukan**:
     - Fitur yang diekstrak menjadi representasi utama dari produk dalam content-based filtering. Dengan mengekstraksi fitur yang relevan, kita dapat menentukan kemiripan antara produk dengan lebih efektif, sehingga menghasilkan rekomendasi yang lebih akurat.

### Data Preparation untuk Collaborative Filtering

1. **Feature Encoding**

   - **Proses**: Mengonversi data kategori (seperti ID pengguna atau ID produk) menjadi format yang dapat digunakan oleh algoritma machine learning. Teknik encoding yang digunakan adalah teknik manual dengan meng enumerate setiap variabel unik kemudian memetakan setiap data user id dan produk id ke dalam nilai enumeratenya. Berikut ini kode yang digunakan untuk encoding.

   ```
    # Mengubah User Id menjadi list tanpa nilai yang sama
    user_ids = df['User Id'].unique().tolist()
    # Melakukan encoding User Id
    user_to_user_encoded = {x: i for i, x in enumerate(user_ids)}
    # Melakukan proses encoding angka ke ke User Id
    user_encoded_to_user = {i: x for i, x in enumerate(user_ids)}
    # Mapping userID ke dataframe user
    df['user'] = df['User Id'].map(user_to_user_encoded)
    # Mapping product Id ke dataframe product
    df['product'] = df.product_id.map(product_to_product_encoded)
   ```

   - **Alasan Diperlukan**:
     - Algoritma collaborative filtering biasanya memerlukan data dalam format numerik untuk menghitung kemiripan atau interaksi antara pengguna dan produk. Oleh karena itu, encoding diperlukan untuk mengubah data kategorikal menjadi numerik agar dapat diproses oleh algoritma.

2. **Feature Selection (Pemilihan Variabel) dan Normalisasi**
   Feature Selection adalah proses dalam pembelajaran mesin dan statistik yang bertujuan untuk memilih subset fitur (variabel) yang paling relevan dari sekumpulan fitur yang lebih besar. Proses ini dilakukan sebelum tahap pelatihan model untuk meningkatkan kinerja dan efisiensi model. Pemilihan ini dilakukan secara manual dengan membuang variabel yang tidak berguna/redundant/noise dan mengambil variabel yang digunakan saja. Pemilihan fitur dilakukan dengan kode berikut ini.

```
# Membuat variabel x untuk mencocokkan data user dan product menjadi satu value
x = df[['user', 'product']].values
# Membuat variabel y untuk membuat Rating dari hasil
y = df['Rating'].apply(lambda x: (x - min_Rating) / (max_Rating - min_Rating)).values
```

Dari kode di atas dapat dilihat bahwa hanya fitur user, product hasil dari proses sebelumnya yaitu feature encoding dan rating yang sekaligus dilakukan normalisasi data menggunakan metode min-max yang digunakan dalam proses pemodelan. Dari pengambilan tiga fitur saja pada pemodalan kali ini berarti juga terjadi pembuangan atau dropping dari variabel-variabel lain yang tidak digunakan. Jadi dari pada memilih menggunakan teknik drop(), saya memilih menggunakan teknik pengambilan nilai pada kolom seperti yang dilakukan pada kode di atas.

**Normalisasi** adalah proses yang digunakan dalam pengolahan data untuk mengubah skala fitur sehingga mereka memiliki rentang nilai yang sama. Salah satu metode normalisasi yang umum digunakan adalah **Min-Max Normalization**.

- Apa itu Min-Max Normalization?

**Min-Max Normalization** adalah teknik untuk merubah nilai-nilai fitur menjadi rentang [0, 1] atau rentang yang ditentukan lainnya. Proses ini dilakukan dengan rumus berikut:

$$X' = \frac{X - \text{min}(X)}{\text{max}(X) - \text{min}(X)}$$

Di mana:

- $X$ adalah nilai asli dari fitur.
- $X'$ adalah nilai ter-normalisasi.
- $\text{min}(X)$ adalah nilai minimum dari fitur dalam dataset.
- $\text{max}(X)$ adalah nilai maksimum dari fitur dalam dataset.

- **Alasan Diperlukan**:

1. **Skala yang Seragam**:
   - Fitur dalam dataset seringkali memiliki skala yang berbeda. Beberapa fitur mungkin memiliki rentang yang sangat besar, sementara yang lain mungkin memiliki rentang yang kecil. Normalisasi membantu untuk memastikan bahwa semua fitur berada dalam skala yang sama.
2. **Menghindari Dominasi Fitur Tertentu**:
   - Tanpa normalisasi, fitur dengan nilai yang lebih besar dapat mendominasi perhitungan jarak atau pembobotan dalam model, yang dapat mengakibatkan bias terhadap fitur tersebut.
3. **Meningkatkan Konvergensi**:
   - Dalam algoritma pembelajaran berbasis gradien, seperti regresi dan jaringan syaraf, normalisasi membantu mempercepat proses konvergensi dan meningkatkan kinerja pelatihan model.
4. **Meningkatkan Akurasi Model**:
   - Normalisasi dapat berkontribusi pada akurasi model yang lebih tinggi, karena model dapat lebih baik dalam belajar dari data yang terstandarisasi.
5. **Kesesuaian untuk Jaringan Syaraf**:
   - Jaringan syaraf dalam machine learning sering kali berfungsi lebih baik ketika input berada dalam rentang tertentu (misalnya, [0, 1]). Normalisasi memfasilitasi ini dan membantu dalam proses pelatihan.

Min-Max Normalization adalah metode yang penting dalam preprocessing data untuk memastikan bahwa semua fitur dalam dataset memiliki skala yang sebanding, yang pada gilirannya meningkatkan kinerja dan stabilitas model pembelajaran mesin.

3. **Splitting Data**
   - **Proses**: Memisahkan dataset menjadi dua bagian, yaitu **training data** dan **testing data**. Data pelatihan digunakan untuk melatih model, sedangkan data pengujian digunakan untuk mengevaluasi kinerja model. Teknik yang umum digunakan adalah membagi data secara acak pada proyek ini dengan perbandingan 80:20 seperti pada kode berikut ini.
   ```
   # Membagi menjadi 80% data train dan 20% data validasi
    train_indices = int(0.8 * df.shape[0])
    x_train, x_val, y_train, y_val = (
        x[:train_indices],
        x[train_indices:],
        y[:train_indices],
        y[train_indices:]
    )
   ```
   - **Alasan Diperlukan**:
     - Splitting data penting untuk memastikan bahwa model yang dibangun dapat dievaluasi secara objektif. Tanpa pemisahan data, kita tidak akan dapat mengetahui apakah model bekerja dengan baik pada data baru (generalization). Melakukan split pada dataset memungkinkan kita untuk mengevaluasi model dengan cara yang lebih adil dan menghindari overfitting.

### Mengapa Data Preparation Diperlukan?

Data preparation adalah tahap yang krusial dalam membangun sistem rekomendasi, baik untuk content-based filtering maupun collaborative filtering. Beberapa alasan utamanya meliputi:

- **Mengatasi Kualitas Data yang Buruk**: Data yang memiliki nilai hilang, duplikat, atau format yang tidak sesuai dapat menurunkan kualitas hasil prediksi. Tahap persiapan data membantu membersihkan dan merapikan data sehingga lebih siap untuk digunakan oleh model.
- **Meningkatkan Kinerja Algoritma**: Dengan data yang terstruktur dan lengkap, algoritma dapat belajar lebih baik dan memberikan hasil yang lebih akurat. Data yang bersih dan relevan membantu meminimalkan noise dan bias.
- **Memastikan Evaluasi Model yang Adil**: Dengan membagi dataset menjadi data pelatihan dan pengujian, kita dapat menilai kinerja model pada data yang tidak dilihat sebelumnya, yang memberikan indikasi yang lebih baik tentang seberapa baik model akan bekerja dalam situasi nyata.

Secara keseluruhan, data preparation adalah langkah penting untuk memastikan bahwa model rekomendasi dapat memberikan hasil yang relevan dan bermanfaat bagi pengguna.

## Modeling and Result

Berikut adalah dua solusi rekomendasi dengan algoritma yang berbeda beserta kelebihan dan kekurangannya.

### 1. Content-Based Filtering

Content-based filtering bekerja dengan merekomendasikan produk yang mirip dengan produk yang pernah dibeli oleh pengguna berdasarkan fitur produk tersebut. Pada proyek ini, fitur-fitur yang digunakan yaitu kategori produk, id produk, dan nama produk yang diolah menggunakan teknik seperti TF-IDF untuk mengekstrak representasi fitur dari produk.

#### Kelebihan:

- **Personalisasi Tinggi**: Algoritma ini memberikan rekomendasi yang sangat relevan karena didasarkan pada preferensi dan riwayat pengguna sebelumnya.
- **Tidak Memerlukan Data Pengguna Lain**: Algoritma hanya membutuhkan informasi produk yang pernah dibeli pengguna, sehingga cocok jika data interaksi pengguna terbatas.
- **Adaptasi untuk Produk Baru**: Content-based filtering dapat merekomendasikan produk baru yang tidak memiliki banyak interaksi, selama informasi deskripsi atau fitur tersedia.

#### Kekurangan:

- **Terbatas pada Fitur Produk**: Jika fitur produk tidak mencerminkan preferensi pengguna dengan baik, kualitas rekomendasi bisa menurun.
- **Kurang Variasi**: Hasil rekomendasi cenderung mirip dengan produk yang sudah dibeli oleh pengguna, sehingga produk yang berbeda mungkin tidak muncul dalam rekomendasi.

### 2. Collaborative Filtering

Collaborative filtering merekomendasikan produk berdasarkan kemiripan perilaku antar pengguna atau kesamaan produk berdasarkan interaksi. Dua pendekatan utama dalam collaborative filtering adalah **user-based** dan **item-based collaborative filtering**. Algoritma ini menggunakan matriks user-item untuk menganalisis interaksi berdasarkan rating yang pernah diberikan pengguna paad suatu produk sebelumnya.

#### Kelebihan:

- **Menghasilkan Rekomendasi yang Lebih Beragam**: Dengan memanfaatkan data dari banyak pengguna, collaborative filtering dapat merekomendasikan produk yang mungkin belum pernah dipertimbangkan pengguna.
- **Tidak Memerlukan Informasi Produk yang Mendetail**: Algoritma hanya membutuhkan data interaksi (seperti rating), sehingga bisa digunakan untuk berbagai jenis produk.

#### Kekurangan:

- **Masalah Cold-Start**: Sulit memberikan rekomendasi yang baik untuk pengguna baru yang belum memiliki banyak data interaksi, atau untuk produk baru.
- **Sparsity Problem**: Data interaksi user-item biasanya sangat jarang (sparse), yang dapat menyebabkan penurunan akurasi jika tidak ditangani dengan baik.

### Implementasi dan Output

Untuk menyelesaikan masalah rekomendasi di Amazon, berikut adalah langkah-langkah untuk top-N recommendation:

1. **Menggunakan Content-Based Filtering**:

   - Hitung skor kemiripan antara produk menggunakan metode cosine similarity berdasarkan fitur yang diekstraksi. Berikut ini kode yang digunakan untuk menganalisis tingkat kesamaan menggunakan teknik cosine similarity.

   ```
    # Menghitung cosine similarity pada matrix tf-idf
    cosine_sim = cosine_similarity(tfidf_matrix)
    cosine_sim
   ```

   - Berikan rekomendasi produk dengan skor kemiripan tertinggi. Berikut ini contoh hasil rekomendasi dengan contoh input nama produk sebagai produk yang sudah pernah dibeli.
     ![image](https://github.com/user-attachments/assets/665d54c1-53a6-4a63-9d9a-1ddcf0ee3d4d) Gambar di atas merupakan produk yang sudah pernah dibeli. ![image](https://github.com/user-attachments/assets/6cc00d20-8538-4df9-8fd1-2af64365617c) Kemudian, berikut ini hasil 5 produk rekomendasi yang diberikan oleh sistem. Dapat dilihat pada gambar di atas, bahwa hasil rekomendasi relevan semua dengan produk yang diinput yaitu memiliki kategori makeup semua.

2. **Menggunakan Collaborative Filtering**:
   - Terapkan matrix factorization dengan jaringan saraf (neural networks) untuk memprediksi nilai rating pada matriks user-item yang kosong. Model ini menggunakan teknik Embedding untuk memetakan pengguna dan produk ke dalam ruang vektor berdimensi lebih rendah, yang bertujuan untuk menangkap fitur-fitur laten yang mendasari interaksi antara pengguna dan produk.Model ini menyajikan pendekatan yang kuat untuk collaborative filtering dengan menggunakan embedding dalam neural network, memberikan kemampuan adaptif untuk menangkap hubungan kompleks antara pengguna dan produk.
   - Berikan rekomendasi top-N produk dengan prediksi rating tertinggi. ![image](https://github.com/user-attachments/assets/f356681e-2651-425c-80ba-65340d5e2f2f) Berdasarkan output di atas, dapat dilihat bahwa hasil rekomendasi cukup baik. Pengguna memberikan rating tinggi pada kategori skin care and Personal Care product. Kemudian, rekomendasi yang diberikan sistem adalah produk pada kategori skin care, Foot, Hand & Nail Care, Beauty Tools & Accessories, Hair Care, Health Care Products. Semua produk yang direkomendasikan masih sangat terkait dengan produk yang diberi rating tertinggi oleh pengguna.

Setelah kedua pendekatan diterapkan, kita dapat mengevaluasi hasilnya menggunakan metrik seperti precision dan RMSE untuk mengetahui performa dari masing-masing model.

## Evaluation

### Metrik Evaluasi

Pada proyek ini, digunakan dua metrik evaluasi yang berbeda untuk menilai performa sistem rekomendasi, yaitu **Precision** untuk teknik **Content-Based Filtering** dan **Root Mean Squared Error (RMSE)** untuk teknik **Collaborative Filtering**.

#### 1. Precision pada Content-Based Filtering

- **Definisi Precision**:
  Precision mengukur proporsi item yang direkomendasikan dan relevan (benar-benar disukai pengguna) terhadap semua item yang direkomendasikan. Precision berkaitan dengan seberapa banyak rekomendasi yang diberikan yang relevan untuk pengguna.

- **Formula Precision**:
  $$\text{Precision} = \frac{\text{Jumlah item yang relevan dan direkomendasikan}}{\text{Jumlah total item yang direkomendasikan}}$$

- **Cara Kerja Precision**:
  Precision menghitung seberapa tepat sistem dalam memberikan rekomendasi kepada pengguna. Jika sistem merekomendasikan banyak item yang tidak relevan, nilai precision akan rendah. Sebaliknya, jika banyak item yang direkomendasikan relevan dengan minat pengguna, precision akan tinggi.

- **Penggunaan pada Proyek Ini**:
  Pada teknik Content-Based Filtering, precision dihitung dengan melihat seberapa banyak produk yang direkomendasikan sesuai dengan preferensi pengguna berdasarkan fitur-fitur produk yang dianalisis. Precision tinggi menunjukkan bahwa sistem mampu memberikan rekomendasi yang akurat dan sesuai dengan preferensi pengguna.

#### 2. RMSE pada Collaborative Filtering

- **Definisi RMSE**:
  **Root Mean Squared Error (RMSE)** adalah metrik yang mengukur rata-rata kuadrat kesalahan (error) antara nilai prediksi dan nilai aktual. RMSE menunjukkan seberapa dekat prediksi sistem dengan data asli, dengan nilai yang lebih rendah menunjukkan performa yang lebih baik.

- **Formula RMSE**:
  $$\text{RMSE} = \sqrt{\frac{1}{N} \sum_{i=1}^{N} (y_i - \hat{y_i})^2}$$
  Di mana:

  - $N$ adalah jumlah total observasi
  - $y_i$ adalah nilai aktual
  - $\hat{y_i}$ adalah nilai prediksi

- **Cara Kerja RMSE**:
  RMSE menghitung rata-rata kuadrat perbedaan antara prediksi dan nilai aktual, lalu mengambil akar dari nilai rata-rata tersebut. RMSE yang lebih rendah menunjukkan bahwa prediksi model lebih akurat dan lebih mendekati nilai sebenarnya. Dalam konteks sistem rekomendasi, RMSE digunakan untuk menilai kesalahan prediksi rating antara pengguna dan produk.

- **Penggunaan pada Proyek Ini**:
  Pada teknik Collaborative Filtering, RMSE digunakan untuk mengevaluasi seberapa akurat model dalam memprediksi rating yang diberikan oleh pengguna terhadap produk. Semakin kecil nilai RMSE, semakin baik model dalam memprediksi rating yang sesuai dengan preferensi pengguna.

### Hasil Evaluasi Berdasarkan Metrik

1. **Precision pada Content-Based Filtering**:
   - Precision yang tinggi menunjukkan bahwa sistem berhasil merekomendasikan produk-produk yang sesuai dengan preferensi pengguna berdasarkan kesamaan fitur produk. Pada hasil rekomendasi berikut ini
     ![image](https://github.com/user-attachments/assets/263939c6-5c65-46fc-bbc3-124d53d63309)
     Dilakukan perhitungan nilai precision dengan menghitung banyak hasil rekomendasi yang relevan dibagi dengan banyak hasil rekomendasi = 5. Berikut ini hasil perhitungan nilai precision pada hasil rekomendasi di atas.![image](https://github.com/user-attachments/assets/1c14c376-efed-40f8-b50a-244a2deabffa) Berdasarkan gambar di atas dapat diketahui bahwa hasil nilai precision dari rekomendasi ini adalah 100% untuk rekomendasi yang relevan.
2. **RMSE pada Collaborative Filtering**:
   - RMSE yang rendah menandakan bahwa prediksi rating yang diberikan oleh model cukup akurat dibandingkan dengan nilai aktual. Hasil evaluasi metriks menggunakan RMSE dapat dilihat pada plot berikut ini. ![image](https://github.com/user-attachments/assets/4f4c8df2-6e43-4fe7-a224-fd96d6cbf6bf)Penurunan Train dan Test: Pada awal training (epoch 0-2), nilai RMSE untuk data train dan test menurun dengan cepat, yang mengindikasikan bahwa model mempelajari pola dalam data dengan cepat. Kesenjangan yang kecil mengindikasikan bahwa model cukup baik dalam melakukan generalisasi, tetapi masih ada kesenjangan kecil yang dapat mengindikasikan overfitting minor. Grafik ini menunjukkan bahwa model sistem rekomendasi mengalami peningkatan akurasi seiring dengan bertambahnya jumlah epoch, baik pada data train yang berhasil mencapai nilai RMSE sebesar 0,2633 maupun pada data test yang berhasil mencapai nilai RMSE sebesar 0,3045.

Dengan menggunakan kedua metrik ini, sistem dapat dievaluasi secara menyeluruh baik dalam hal seberapa akurat sistem merekomendasikan item yang sesuai (precision) maupun seberapa dekat prediksi rating dengan nilai aktual (RMSE).

### Kesimpulan

Berdasarkan analisis dan pengolahan data yang dilakukan untuk membentuk sistem rekomendasi produk dengan menggunakan dua teknik diperoleh kesimpulan sebagai berikut.

1. Sejumlah rekomendasi produk yang dipersonalisasi untuk pengguna dengan teknik content-based filtering berhasil menghasilkan 5 rekomendasi dengan nilai precision 1,0 atau 100% untuk rekomendasi yang relevan.
2. Sejumlah rekomendasi produk yang sesuai dengan preferensi pengguna dan belum pernah dibeli sebelumnya dengan teknik collaborative filtering berhasil menghasilkan 10 rekomendasi dengan nilai evaluasi RMSE pada data train yang berhasil mencapai nilai RMSE sebesar 0,2633 sedangkan pada data test yang berhasil mencapai nilai RMSE sebesar 0,3045.

Berdasarkan kesimpulan di atas, menunjukkan bahwa problem statement dapat diselesaikan dan semua goals atau tujuan dari proyek ini tercapai. Kedua sistem rekomendasi yang dibangun menggunakan dua teknik yang berbeda masing-masing memiliki tingkat evaluasi yang baik. Kedua sistem ini juga mampu dan berhasil memberikan rekomendasi produk sesuai dengan jumlah masing-masing.

## Referensi/Daftar Pustaka

[Asaniczka. (2024). Amazon Products Dataset 2023 (1.4M Products)](https://kaggle.com/asaniczka/amazon-products-dataset-2023-1-4m-products)

[Ahmed Ali. (2023). Customer Rating Data By Amazon](https://www.kaggle.com/ahmedaliraja/customer-rating-data-by-amazon)

[Dwivedi, Rohit & Anand, Abhineet & Johri, Prashant & Banerji, Arpit & Gaur, N. (2020). Product Based Recommendation System On Amazon Data.](https://www.researchgate.net/profile/Abhineet-Anand/publication/352815845_Product_Based_Recommendation_System_On_Amazon_Data/links/60dacdcaa6fdccb745f0cdaa/Product-Based-Recommendation-System-On-Amazon-Data.pdf)

[Ahmed, Md Zaid & Singh, Abhay & Paul, Abir & Ghosh, Sayantani & Chaudhuri, Avijit. (2022). Amazon Product Recommendation System. IJARCCE. 11. 10.17148/IJARCCE.2022.11356.](https://www.researchgate.net/profile/Md-Zaid-Ahmed-2/publication/360000178_Amazon_Product_Recommendation_System/links/62795821107cae291996400d/Amazon-Product-Recommendation-System.pdf)
