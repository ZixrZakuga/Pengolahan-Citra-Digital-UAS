# Face Recognition dengan Metode Haar Cascade dan FaceNet

## Nama : Maula Muhammad Maridjan 
## NIM  : 2206138
Institut Teknologi Garut, Indonesia  
[2206138@itg.ac.id](mailto:2206138@itg.ac.id)

## 1. PENDAHULUAN
-------------

### 1.1 Latar Belakang
-------------------

Perkembangan teknologi dalam bidang kecerdasan buatan (artificial intelligence) semakin pesat seiring dengan kebutuhan manusia untuk menciptakan sistem yang dapat melakukan tugas secara otomatis, salah satunya dalam deteksi wajah. Wajah manusia merupakan salah satu fitur biometrik yang sangat khas dan efektif untuk digunakan dalam identifikasi seseorang. Dalam beberapa aplikasi, seperti sistem akses keamanan, absensi, hingga kontrol sistem, wajah menjadi kunci identifikasi yang paling banyak digunakan. Salah satu metode yang dapat digunakan untuk mendeteksi wajah adalah dengan menggunakan citra digital yang diolah dengan algoritma deteksi wajah.

Citra digital sendiri merupakan representasi visual dari objek atau fenomena yang diproses dalam bentuk digital melalui perangkat seperti kamera atau scanner. Citra digital sangat berperan dalam banyak sistem berbasis komputer, terutama dalam aplikasi pengenalan wajah yang memanfaatkan algoritma tertentu untuk mendeteksi dan mengenali wajah secara akurat. Salah satu algoritma yang sering digunakan adalah Haar Cascade Classifier, yang efektif dalam mendeteksi objek, khususnya wajah, dengan waktu pemrosesan yang cepat.

Haar Cascade Classifier adalah metode berbasis fitur yang digunakan untuk mendeteksi objek dalam citra digital, termasuk wajah manusia. Metode ini dikembangkan oleh Paul Viola dan Michael Jones pada tahun 2001. Haar-like features menggunakan pola persegi panjang untuk mendeteksi perbedaan antara area gelap dan terang pada gambar, sehingga dapat menunjukkan lokasi objek tertentu, termasuk wajah manusia. Metode ini memiliki kelebihan dalam komputasi cepat, memungkinkan proses deteksi wajah dilakukan secara real-time.

Selain itu, pengolahan citra digital menggunakan teknik-teknik lainnya seperti deteksi tepi dan konvolusi juga sering dikombinasikan dengan Haar Cascade untuk meningkatkan akurasi dan efektivitas deteksi wajah dalam berbagai kondisi pencahayaan, kemiringan wajah, dan perbedaan jarak antara wajah dan kamera.

### 1.2 Rumusan Masalah
----------------------

1. Bagaimana cara mengimplementasikan algoritma Haar Cascade Classifier untuk mendeteksi wajah pada citra digital?
2. Bagaimana kinerja aplikasi dalam melakukan deteksi dan identifikasi wajah secara cepat dan efisien?

### 1.3 Tujuan
-------------

1. Mengimplementasikan algoritma Haar Cascade Classifier untuk mendeteksi wajah pada citra digital.
2. Mengembangkan aplikasi yang mampu melakukan deteksi dan identifikasi wajah dengan akurasi yang baik serta waktu pemrosesan yang cepat.

## 2. METODE PENELITIAN
----------------------

### 2.1 Langkah Langkah Implementasi
---------------------------------

Pada penelitian ini, dilakukan pengembangan sistem deteksi dan pengenalan wajah menggunakan metode Haar Cascade Classifier dan FaceNet. Metodologi yang digunakan mencakup beberapa tahapan utama yang dilakukan secara sistematis, yaitu inisialisasi pustaka dan model deteksi wajah, pembacaan citra input, deteksi wajah, ekstraksi fitur wajah, identifikasi wajah berdasarkan database yang telah dibuat, perhitungan akurasi, serta penampilan hasil deteksi dalam bentuk visual dan numerik.

1. Inisialisasi Library dan Model Deteksi Wajah
Tahapan pertama adalah inisialisasi pustaka dan model deteksi wajah. Pada tahap ini, pustaka yang diperlukan seperti OpenCV digunakan untuk membaca dan memproses gambar, Haar Cascade digunakan untuk mendeteksi wajah dalam citra, serta FaceNet digunakan untuk mengekstrak fitur wajah dan membandingkannya dengan database wajah yang telah dibuat sebelumnya.

2. Membaca Citra Wajah
Setelah model diinisialisasi, langkah berikutnya adalah membaca citra wajah menggunakan OpenCV. Citra diambil dari kamera atau file gambar yang telah disimpan sebelumnya. Gambar yang berhasil dibaca kemudian dikonversi ke format grayscale untuk mempercepat proses deteksi wajah menggunakan Haar Cascade Classifier.

3. Deteksi Wajah dalam Citra
Setelah membaca citra wajah, sistem akan melakukan deteksi wajah menggunakan Haar Cascade Classifier. Algoritma ini akan mencari pola wajah dalam gambar berdasarkan haar-like features dan menghasilkan koordinat area wajah yang terdeteksi. Jika wajah ditemukan, maka akan dilakukan cropping pada area wajah untuk diekstraksi lebih lanjut.

4. Ekstraksi Fitur Wajah Menggunakan FaceNet
Setelah wajah berhasil dideteksi, sistem akan melakukan ekstraksi fitur menggunakan model FaceNet. Model ini akan mengonversi wajah yang telah diproses ke dalam bentuk vektor numerik yang dikenal sebagai embedding wajah. Embedding ini kemudian dibandingkan dengan database wajah yang telah dibuat sebelumnya untuk menentukan identitas wajah.

5. Identifikasi Wajah Berdasarkan Database
Setelah memperoleh embedding wajah, sistem akan membandingkannya dengan embedding dalam database. Perbandingan ini dilakukan dengan menghitung jarak Euclidean antara vektor wajah yang baru dengan vektor dalam database. Identitas wajah akan ditentukan berdasarkan vektor dengan jarak terpendek dari database yang telah disimpan.

6. Perhitungan Akurasi Model
Untuk mengukur performa sistem, dilakukan perhitungan akurasi dengan membandingkan identitas yang diprediksi dengan identitas yang sebenarnya. Perhitungan akurasi dilakukan menggunakan rumus : Jika identifikasi wajah sesuai dengan database, maka sistem dinyatakan berhasil mengenali wajah dengan akurasi yang tinggi. Namun, jika terjadi kesalahan identifikasi, maka akurasi akan berkurang.

7. Menampilkan Hasil Deteksi dan Akurasi
Tahapan terakhir adalah menampilkan hasil deteksi dan akurasi. Hasil deteksi wajah akan ditampilkan dalam bentuk visual, di mana sistem akan menambahkan teks pada gambar yang menunjukkan identitas wajah yang dikenali serta tingkat akurasinya. Selain itu, gambar hasil deteksi wajah juga akan ditampilkan sebagai referensi tambahan. Informasi numerik mengenai identitas yang sebenarnya, hasil prediksi, serta tingkat akurasi juga dicetak di layar untuk dianalisis lebih lanjut.

Berdasarkan hasil pengujian, sistem mampu mengenali wajah dengan tingkat akurasi yang baik. Kecepatan deteksi juga cukup tinggi karena Haar Cascade Classifier memiliki keunggulan dalam pemrosesan cepat. Namun, sistem masih memiliki beberapa keterbatasan, seperti sensitivitas terhadap variasi pencahayaan dan sudut wajah yang berbeda.

### 2.2 Haar Cascade
-------------------

Deteksi Objek menggunakan pengklasifikasi kaskade berbasis fitur Haar adalah metode efektif yang diusulkan oleh Paul Viola dan Michael Jones dalam makalah tahun 2001, "Deteksi Objek Cepat menggunakan Kaskade Fitur Sederhana yang Ditingkatkan". Ini adalah pendekatan berbasis pembelajaran mesin di mana fungsi kaskade dilatih dari banyak gambar positif dan negatif. Ini kemudian digunakan untuk mendeteksi objek dalam gambar lain.

Di sini kita akan bekerja dengan deteksi wajah. Awalnya, algoritma membutuhkan banyak gambar positif (gambar wajah) dan gambar negatif (gambar tanpa wajah) untuk melatih pengklasifikasi. Maka kita perlu mengekstrak fitur darinya. Untuk ini, fitur Haar yang ditunjukkan pada gambar di bawah ini. Mereka seperti kernel konvolusional kita. Setiap fitur adalah nilai tunggal yang diperoleh dengan mengurangi jumlah piksel di bawah persegi panjang putih dari jumlah piksel di bawah persegi panjang hitam.
![Image](https://github.com/ZixrZakuga/Pengolahan-Citra-Digital-UAS/issues/1#issue-2822482378)

Sekarang semua kemungkinan ukuran dan lokasi dari setiap kernel digunakan untuk menghitung banyak fitur. Untuk setiap perhitungan fitur, kita perlu menemukan jumlah piksel di bawah persegi panjang putih dan hitam. Untuk mengatasi ini, mereka memperkenalkan gambar integral. Ini menyederhanakan perhitungan jumlah piksel, seberapa besar jumlah piksel, menjadi operasi yang hanya melibatkan empat piksel.

Tetapi di antara semua fitur yang kami hitung ini, kebanyakan dari mereka tidak relevan. Misalnya, perhatikan gambar di bawah ini. Baris atas menunjukkan dua fitur bagus. Fitur pertama yang dipilih tampaknya berfokus pada properti bahwa daerah mata seringkali lebih gelap daripada daerah hidung dan pipi. Fitur kedua yang dipilih bergantung pada sifat bahwa mata lebih gelap daripada pangkal hidung. Tetapi jendela yang sama yang diterapkan di pipi atau tempat lain tidak relevan. Jadi bagaimana kita memilih fitur terbaik dari 160000+ fitur? Itu dicapai oleh Adaboost.

![Image](https://github.com/ZixrZakuga/Pengolahan-Citra-Digital-UAS/issues/12#issue-2822509796)

Untuk ini, kami menerapkan setiap fitur pada semua gambar pelatihan. Untuk setiap fitur, ia menemukan ambang batas terbaik yang akan mengklasifikasikan wajah menjadi positif dan negatif. Namun jelas, akan ada kesalahan atau salah klasifikasi. Kami memilih fitur dengan tingkat kesalahan minimum, yang berarti fitur tersebut adalah fitur yang paling baik mengklasifikasikan gambar wajah dan non-wajah.

Pengklasifikasi akhir adalah jumlah tertimbang dari pengklasifikasi lemah ini. Disebut lemah karena itu sendiri tidak dapat mengklasifikasikan gambar, tetapi bersama dengan yang lain membentuk pengklasifikasi yang kuat. Makalah tersebut mengatakan bahkan 200 fitur memberikan deteksi dengan akurasi 95%. Pengaturan akhir mereka memiliki sekitar 6000 fitur.

Jadi sekarang anda mengambil gambar. Ambil setiap jendela 24x24. Terapkan 6000 fitur ke dalamnya. Periksa apakah itu wajah atau bukan. Dalam gambar, sebagian besar wilayah gambar adalah wilayah non-wajah. Jadi lebih baik untuk memiliki metode sederhana untuk memeriksa apakah jendela bukan wilayah wajah. Jika tidak, buang dalam satu tembakan. Jangan memprosesnya lagi. Alih-alih fokus pada wilayah di mana mungkin ada wajah.

Untuk ini mereka memperkenalkan konsep Kaskade Pengklasifikasi. Alih-alih menerapkan semua 6000 fitur pada jendela, kelompokkan fitur ke dalam tahapan pengklasifikasi yang berbeda dan terapkan satu per satu. Jika jendela gagal pada tahap pertama, buang. Kami tidak mempertimbangkan fitur yang tersisa di dalamnya. Jika lolos, terapkan fitur tahap kedua dan lanjutkan prosesnya. Jendela yang melewati semua tahapan adalah wilayah wajah.

Detektor penulis memiliki 6000+ fitur dengan 38 tahap dengan 1, 10, 25, 25 dan 50 fitur dalam lima tahap pertama.

### 2.3 Facenet
----------------

FaceNet merupakan sistem pengenalan wajah yang dikembangkan oleh peneliti Google. FaceNet mengekstrak fitur wajah menjadi vektor menggunakan arsitektur deep Convolutional Neural Network (deep CNN). Facenet mengambil input berupa foto wajah dan akan mengeluarkan output berupa 128 nilai vektor yang disebut embedding. Idealnya, embedding dari wajah yang sama akan memiliki nilai vektor yang sama. Vektor nilai atau vector embedding yang dihasilkan dapat memetakan kemiripan wajah yang memiliki kedekatan posisi pada embedding space, wajah yang serupa cenderung memiliki jarak yang lebih dekat dengan 0 sedangkan yang tidak serupa memiliki jarak yang lebih jauh.

Model Deep CNN yang digunakan pada FaceNet bisa berupa ZF-Net atau Inception. Pada penelitian ini kami menggunakan FaceNet pada tahapan feature learning. Hasil dari FaceNet yang berupa vektor sebanyak 128 elemen atau Face embedding akan diklasifikasi menggunakan SVM. Model SVM mengklasifikasi identitas wajah dari vector embedding tersebut.

Data yang digunakan untuk test didapatkan dari facenet yang sudah disediakan oleh hiroki taniai. Data wajah yang sudah di pretrained sebanyak 1 juta wajah. kemudian untuk sample kita mencari secara manual kemudian memasukkan ke dalam folder database agar wajah yang sudah dikenal dapat dikenali oleh sistem. Untuk data satu orang cukup menggunakan satu foto. Dikarenakan facenet sudah membuat pola pintar agar satu wajah dapat membuat 128 vektor agar dapat mudah dikenali oleh sistem.

## 3. HASIL DAN PEMBAHASAN
-------------------------

Dalam pengujian sistem deteksi wajah menggunakan Haar Cascade Classifier, dilakukan sepuluh skenario berbeda untuk mengevaluasi efektivitas dan akurasi sistem dalam mengenali wajah dalam berbagai kondisi. Berikut adalah deskripsi masing-masing pengujian:

1. Nasep Ependi (100%)
Pada pengujian ini, wajah Nasep Ependi diuji dalam kondisi normal dengan pencahayaan yang cukup dan posisi wajah menghadap langsung ke kamera. Sistem berhasil mengenali wajahnya dengan akurasi 100%.
![Image](https://github.com/ZixrZakuga/Pengolahan-Citra-Digital-UAS/issues/2#issue-2822504160)
2. Jamil dan Maula (100%)
Dua individu, Jamil dan Maula, berada dalam satu frame dengan wajah menghadap kamera secara langsung. Sistem berhasil mengenali keduanya dengan akurasi 100%, menunjukkan bahwa model dapat mendeteksi lebih dari satu wajah dalam satu gambar.
![Image](https://github.com/ZixrZakuga/Pengolahan-Citra-Digital-UAS/issues/3#issue-2822504465)
3. Rivan (100%)
Pengujian dilakukan terhadap Rivan dalam kondisi normal dengan pencahayaan yang baik dan posisi wajah yang jelas. Sistem berhasil mendeteksi wajahnya dengan tingkat akurasi 100%.
![Image](https://github.com/ZixrZakuga/Pengolahan-Citra-Digital-UAS/issues/4#issue-2822504817)
4. Maula Lihat Samping (0%)
Dalam skenario ini, Maula menghadap ke samping (profil wajah tidak sepenuhnya terlihat). Sistem gagal mengenali wajahnya, yang menunjukkan bahwa Haar Cascade kurang efektif dalam mendeteksi wajah dengan sudut kemiringan ekstrem.
![Image](https://github.com/ZixrZakuga/Pengolahan-Citra-Digital-UAS/issues/5#issue-2822505135)
5. Maula Lihat Miring (0%)
Maula menghadap kamera dengan posisi miring, di mana sebagian wajah masih terlihat. Namun, sistem tidak berhasil mendeteksinya, menunjukkan keterbatasan model dalam mengenali wajah yang tidak menghadap langsung ke kamera.
![Image](https://github.com/ZixrZakuga/Pengolahan-Citra-Digital-UAS/issues/6#issue-2822505477)
6. Maula Kacamata (100%)
Pengujian dilakukan dengan Maula mengenakan kacamata. Sistem tetap mampu mengenali wajahnya dengan akurasi 100%, menunjukkan bahwa pemakaian kacamata tidak terlalu memengaruhi kinerja deteksi.
![Image](https://github.com/ZixrZakuga/Pengolahan-Citra-Digital-UAS/issues/7#issue-2822506392)
7. Maula Tanpa Kacamata (100%)
Maula diuji tanpa kacamata dalam kondisi normal. Hasilnya, sistem berhasil mengenali wajahnya tanpa kendala dengan akurasi 100%.
![Image](https://github.com/ZixrZakuga/Pengolahan-Citra-Digital-UAS/issues/8#issue-2822506672)
8. Maula Pencahayaan Gelap (0%)
Dalam kondisi pencahayaan yang minim atau gelap, sistem gagal mengenali wajah Maula. Hal ini menunjukkan bahwa Haar Cascade sangat bergantung pada pencahayaan yang memadai untuk melakukan deteksi secara optimal.
![Image](https://github.com/ZixrZakuga/Pengolahan-Citra-Digital-UAS/issues/9#issue-2822506958)
9. Nasep, Ilman, dan Maula (100%)
Pengujian dilakukan dengan tiga orang dalam satu frame (Nasep, Ilman, dan Maula). Sistem berhasil mengenali semua wajah dalam gambar dengan akurasi 100%, menunjukkan kemampuan model dalam mendeteksi banyak wajah secara bersamaan jika pencahayaan dan sudut wajah optimal.
![Image](https://github.com/ZixrZakuga/Pengolahan-Citra-Digital-UAS/issues/10#issue-2822507304)
10. Alvarizky (100%)
Pengujian dilakukan terhadap Alvarizky dalam kondisi normal, dengan wajah yang menghadap langsung ke kamera dan pencahayaan yang cukup. Sistem berhasil mendeteksinya dengan tingkat akurasi 100%.
![Image](https://github.com/ZixrZakuga/Pengolahan-Citra-Digital-UAS/issues/11#issue-2822507624)
## 4. KESIMPULAN
--------------

Berdasarkan hasil pengujian yang dilakukan sebanyak sepuluh kali percobaan, sistem deteksi dan pengenalan wajah menggunakan Haar Cascade Classifier menunjukkan hasil yang cukup baik dalam kondisi tertentu, namun masih memiliki keterbatasan dalam situasi tertentu.

### 4.1 Ringkasan Temuan:

1. Sistem berhasil mengenali wajah dengan akurasi 100% dalam sebagian besar kondisi normal, seperti pada individu Nasep Ependi, Jamil dan Maula, Rivan, serta Maula dengan atau tanpa kacamata.
2. Sistem mengalami kegagalan dalam mendeteksi wajah ketika subjek melihat ke samping, melihat secara miring, atau berada dalam kondisi pencahayaan yang gelap (akurasi 0%).
3. Sistem tetap dapat mengenali wajah dalam kondisi pencahayaan yang cukup meskipun terdapat beberapa orang dalam satu frame, seperti dalam kasus "Nasep, Ilman, dan Maula" yang mendapatkan akurasi 100%.

### 4.2 Batasan Pekerjaan:

1. Model Haar Cascade masih memiliki keterbatasan dalam mengenali wajah dari sudut samping atau miring.
2. Pencahayaan yang buruk sangat memengaruhi kinerja sistem, menyebabkan deteksi wajah gagal dilakukan.
3. Sistem lebih optimal dalam mendeteksi wajah yang menghadap langsung ke kamera dengan pencahayaan yang cukup.
4. Model ini tidak mempertimbangkan perubahan ekspresi wajah atau fitur wajah yang tertutup sebagian.

### 4.3 Rekomendasi untuk Pekerjaan di Masa Depan:

1. Menggunakan model deteksi wajah yang lebih canggih seperti FaceNet atau MTCNN yang memiliki ketahanan lebih baik terhadap variasi sudut dan pencahayaan.
2. Mengintegrasikan teknik preprocessing gambar, seperti peningkatan pencahayaan dan normalisasi kontras, agar sistem lebih adaptif terhadap kondisi pencahayaan yang buruk.
3. Mengembangkan sistem yang mampu mengenali wajah dalam berbagai sudut pandang dengan menggunakan model 3D face recognition atau deep learning-based face recognition.
4. Menggabungkan metode data augmentation untuk melatih sistem dengan lebih banyak variasi wajah dalam kondisi berbeda agar akurasi meningkat.
5. Mengoptimalkan waktu pemrosesan untuk memastikan sistem tetap bekerja secara real-time tanpa mengurangi akurasi deteksi wajah.
