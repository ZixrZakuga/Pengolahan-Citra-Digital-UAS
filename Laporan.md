# Face Recognition dengan Metode Haar Cascade dan FaceNet

**Nama: [Nama Anda]**  
**NPM: [NPM Anda]**

## 1. Pendahuluan

### Latar Belakang

Face recognition atau pengenalan wajah adalah salah satu bidang dalam kecerdasan buatan (AI) yang berkembang pesat. Teknologi ini digunakan dalam berbagai aplikasi, seperti keamanan, autentikasi, dan sistem pengawasan. Face recognition menjadi semakin populer karena kemampuannya untuk mengidentifikasi individu dengan cepat dan akurat tanpa perlu interaksi fisik. Beberapa aplikasi utama dari teknologi ini meliputi sistem keamanan berbasis biometrik, pengelolaan absensi di perusahaan atau institusi pendidikan, serta sistem pembayaran berbasis pengenalan wajah.

Kemajuan dalam machine learning dan deep learning telah memungkinkan pengembangan algoritma yang lebih akurat dan efisien dalam pengenalan wajah. Metode deteksi dan pengenalan wajah saat ini umumnya menggunakan pendekatan berbasis fitur dan pembelajaran mendalam. Dua metode yang sering digunakan dalam face recognition adalah Haar Cascade untuk deteksi wajah dan FaceNet untuk ekstraksi fitur wajah.

### Penelitian atau Teori Terkait

Haar Cascade adalah metode berbasis machine learning yang dikembangkan oleh Paul Viola dan Michael Jones untuk deteksi objek dalam gambar. Metode ini bekerja dengan menggunakan fitur Haar untuk membedakan objek yang diinginkan dari latar belakangnya. Dengan menggunakan serangkaian fitur sederhana yang diekstrak dari gambar, metode ini mampu mendeteksi wajah dengan efisiensi tinggi.

Sementara itu, FaceNet adalah model deep learning yang dikembangkan oleh Google, yang bertujuan untuk menghasilkan representasi numerik dari wajah dalam bentuk vektor fitur yang disebut embedding wajah. Embedding ini memungkinkan sistem untuk membandingkan wajah secara lebih akurat dibandingkan dengan metode tradisional seperti Eigenfaces atau Fisherfaces. FaceNet bekerja dengan mengubah gambar wajah menjadi vektor 128 dimensi yang dapat dibandingkan dengan wajah lain menggunakan metrik jarak, seperti jarak Euclidean.

### Tujuan Tugas

Tujuan dari proyek ini adalah mengimplementasikan sistem pengenalan wajah menggunakan metode Haar Cascade untuk deteksi wajah dan FaceNet untuk ekstraksi fitur. Secara khusus, tujuan yang ingin dicapai dalam penelitian ini meliputi:

1. Membangun sistem deteksi wajah menggunakan Haar Cascade yang mampu mengenali wajah dengan tingkat akurasi tinggi.
2. Mengimplementasikan FaceNet untuk mengekstrak fitur wajah dan menyimpannya dalam bentuk embedding.
3. Membandingkan hasil pengenalan wajah dengan database yang telah dibuat sebelumnya.
4. Mengevaluasi performa sistem dalam berbagai kondisi pencahayaan, sudut wajah, dan jumlah dataset yang berbeda.
5. Menganalisis batasan metode yang digunakan serta memberikan rekomendasi untuk peningkatan di masa depan.

## 2. Metode

### Langkah-langkah Implementasi

Metode yang digunakan dalam penelitian ini terdiri dari beberapa tahapan utama, yaitu:

1. **Import Library**: Memuat pustaka yang diperlukan seperti OpenCV untuk deteksi wajah, TensorFlow dan Keras untuk implementasi model FaceNet, serta NumPy dan pickle untuk pengolahan data.
2. **Mount Google Drive**: Menyimpan dan mengambil data dari Google Drive untuk memudahkan pengelolaan dataset wajah.
3. **Preprocessing Data**:
   - Mengubah gambar wajah ke dalam skala abu-abu agar lebih efisien dalam deteksi.
   - Melakukan normalisasi dan cropping untuk memastikan wajah berada dalam posisi yang sama.
   - Menggunakan teknik augmentasi data untuk meningkatkan variasi dataset, seperti rotasi, perubahan pencahayaan, dan flipping.
4. **Load Haar Cascade Model**:
   - Menggunakan model Haar Cascade yang telah dilatih sebelumnya untuk mendeteksi wajah dalam gambar.
   - Menyesuaikan parameter seperti `scaleFactor` dan `minNeighbors` untuk meningkatkan akurasi deteksi.
5. **Initialize FaceNet Model**:
   - Menggunakan model FaceNet yang telah dilatih sebelumnya untuk menghasilkan embedding wajah.
   - Memanfaatkan arsitektur jaringan syaraf dalam untuk mengubah wajah menjadi representasi numerik.
6. **Membuat Database Embedding Wajah**:
   - Mengumpulkan gambar wajah dari beberapa individu yang akan dimasukkan ke dalam database.
   - Mengonversi setiap gambar wajah menjadi embedding menggunakan model FaceNet.
   - Menyimpan hasil embedding ke dalam format yang dapat diakses kembali saat proses identifikasi.
7. **Menyimpan Database ke File**:
   - Menggunakan pustaka `pickle` untuk menyimpan database embedding wajah dalam file `.pkl` agar dapat digunakan kembali tanpa perlu melakukan ekstraksi ulang.
8. **Deteksi dan Identifikasi Wajah**:
   - Menggunakan Haar Cascade untuk mendeteksi wajah dalam gambar atau video secara real-time.
   - Menggunakan FaceNet untuk mencocokkan wajah yang terdeteksi dengan embedding yang tersimpan dalam database.
   - Menghitung jarak antara embedding wajah yang terdeteksi dengan embedding dalam database untuk menentukan identitas individu.
9. **Mengambil Foto dari Webcam**:
   - Menggunakan OpenCV untuk menangkap frame dari webcam secara real-time.
   - Menggunakan JavaScript di Google Colab untuk mengaktifkan akses ke kamera dan mengambil gambar.
10. **Menghitung Akurasi Model**:
    - Menggunakan metrik akurasi, precision, recall, dan F1-score untuk mengevaluasi performa model.
    - Menganalisis tingkat kesalahan dan faktor-faktor yang mempengaruhi hasil pengenalan wajah.

### Visualisasi Model

- **Haar Cascade** digunakan untuk mendeteksi wajah dengan menampilkan kotak di sekitar wajah yang terdeteksi.
- **FaceNet** menghasilkan embedding wajah dalam bentuk vektor numerik yang divisualisasikan dalam bentuk scatter plot untuk menunjukkan sebaran data wajah yang telah diproses.
- **Hasil pengenalan wajah** divisualisasikan dengan gambar yang telah diberi label identitas berdasarkan database yang telah dibuat sebelumnya.

Dengan pendekatan ini, sistem diharapkan dapat mendeteksi dan mengenali wajah dengan tingkat akurasi tinggi dalam berbagai kondisi lingkungan.
