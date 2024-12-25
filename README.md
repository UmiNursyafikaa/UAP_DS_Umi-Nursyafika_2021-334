# Identifikasi Jenis Bunga Hias

## Deskripsi Proyek

Proyek ini bertujuan untuk mengembangkan model machine learning yang dapat mengidentifikasi jenis bunga hias berdasarkan citra. Latar belakang dari proyek ini adalah untuk mempermudah pengenalan berbagai jenis bunga secara otomatis, yang dapat dimanfaatkan dalam berbagai bidang seperti pertanian, pendidikan, dan e-commerce.

## Dataset

Dataset yang digunakan dalam proyek ini berasal dari Kaggle: [Flowers Recognition Dataset](https://www.kaggle.com/datasets/alxmamaev/flowers-recognition). Dataset ini terdiri dari 4,317 gambar bunga dari berbagai kategori. 

Untuk meningkatkan performa model, dilakukan augmentasi pada data training sehingga jumlah data training bertambah menjadi 11,268 gambar.

## Langkah Instalasi

1. Clone repository ini ke komputer Anda:
   ```bash
   git clone https://github.com/username/repository-name.git
   ```
2. Masuk ke direktori project:
   ```bash
   cd repository-name
   ```
3. Pastikan Anda telah menginstal Python dan pip. Install dependencies yang dibutuhkan dengan:
   ```bash
   pip install -r requirements.txt
   ```
4. Jalankan aplikasi menggunakan Streamlit:
   ```bash
   streamlit run app.py
   ```

Aplikasi ini juga dapat diakses melalui [Streamlit Cloud](https://webprediksibunga-umi.streamlit.app/).

## Pustaka Yang Diperlukan
- **Streamlit** : Digunakan untuk membuat aplikasi web interaktif.
- **TensorFlow** : Digunakan untuk memuat model deep learning dan melakukan prediksi.
- **NumPy** : Digunakan untuk manipulasi array dan operasi numerik.
- **Pillow** : Digunakan untuk memproses dan memanipulasi gambar.
- **FungsiPreprocessing** : Digunakan untuk mempersiapkan gambar sesuai dengan standar model GoogleNet. Fungsi ini sudah termasuk dalam pustaka TensorFlow.

## Deskripsi Model

Proyek ini menggunakan dua model transfer learning:

1. **GoogleNet**: Model ini merupakan arsitektur convolutional neural network yang efektif dalam klasifikasi gambar. Dikenal karena kompleksitasnya yang rendah namun memiliki performa yang tinggi.
2. **VGG16**: Model ini memiliki arsitektur yang lebih dalam dibandingkan GoogleNet, dengan fokus pada ekstraksi fitur mendetail dari gambar.

Kedua model ini dilatih menggunakan dataset augmented untuk meningkatkan akurasi dalam klasifikasi bunga.

## Hasil Akurasi dan Analisis

### Gambar Model VGG16
![Gambar1](https://github.com/UmiNursyafikaa/UAP_DS_Umi-Nursyafika_2021-334/blob/main/gambar/googleNet.1.png)

![Gambar2](https://github.com/UmiNursyafikaa/UAP_DS_Umi-Nursyafika_2021-334/blob/main/gambar/googleNet.2.png)

![Gambar3](https://github.com/UmiNursyafikaa/UAP_DS_Umi-Nursyafika_2021-334/blob/main/gambar/googleNet.3.png)

### Gambar Model GoogleNet
![Gambar1](https://github.com/UmiNursyafikaa/UAP_DS_Umi-Nursyafika_2021-334/blob/main/gambar/vgg16.1.png)

![Gambar2](https://github.com/UmiNursyafikaa/UAP_DS_Umi-Nursyafika_2021-334/blob/main/gambar/vgg16.2.png)

![Gambar3](https://github.com/UmiNursyafikaa/UAP_DS_Umi-Nursyafika_2021-334/blob/main/gambar/vgg16.3.png)

### Hasil dan Analisis
1.Perbandingan Akurasi
GoogleNet:
Train Accuracy meningkat secara konsisten hingga mencapai lebih dari 80%.
Validation Accuracy stabil di sekitar 79%-80% setelah beberapa epoch.
VGG16:
Train Accuracy meningkat secara konsisten dengan performa stabil.
Validation Accuracy mencapai nilai lebih tinggi dibanding GoogleNet, yaitu 83%.
Kesimpulan:
VGG16 memiliki akurasi validasi yang lebih tinggi daripada GoogleNet, menunjukkan kemampuan generalisasi yang sedikit lebih baik. Namun, performa GoogleNet tetap kompetitif.

2.Perbandingan Loss
GoogleNet:
Train Loss dan Validation Loss menunjukkan tren menurun secara konsisten.
Validation Loss mendekati Train Loss tanpa pola overfitting yang jelas.
VGG16:
Train Loss terus menurun dengan pola yang stabil.
Validation Loss juga menurun dan lebih rendah daripada Train Loss, menunjukkan bahwa VGG16 memiliki model yang lebih baik dalam menyesuaikan diri dengan data validasi.
Kesimpulan:
Kedua model menunjukkan tidak adanya overfitting, tetapi VGG16 tampaknya lebih unggul dalam menjaga hubungan antara train loss dan validation loss.

3.Perbandingan Metrik Evaluasi
GoogleNet:
Accuracy keseluruhan: 79%.
Precision, Recall, dan F1-Score per kelas berkisar antara 0.68 hingga 0.88, dengan kelas "rose" memiliki kinerja terendah.
Macro Avg dan Weighted Avg berada di 0.79, menunjukkan performa stabil pada kelas dengan distribusi data seimbang.
VGG16:
Accuracy keseluruhan: 83%.
Precision, Recall, dan F1-Score per kelas berkisar antara 0.77 hingga 0.89, menunjukkan performa lebih konsisten pada semua kelas.
Macro Avg dan Weighted Avg berada di sekitar 0.83, yang juga lebih baik dibandingkan GoogleNet.
Kesimpulan:
VGG16 memiliki keunggulan dalam metrik evaluasi, dengan akurasi, precision, recall, dan F1-score yang lebih tinggi pada hampir semua kelas.

4.Efisiensi Model
GoogleNet dirancang untuk efisiensi dan kecepatan, memiliki lebih sedikit parameter dibandingkan VGG16. Ini membuatnya lebih ringan dan lebih cepat pada hardware yang terbatas.
VGG16 adalah model yang lebih berat dengan lebih banyak parameter, tetapi dapat memberikan hasil yang lebih baik dalam hal akurasi jika hardware mendukung.

### Kesimpulan Akhir
GoogleNet adalah pilihan yang baik jika efisiensi komputasi menjadi prioritas, terutama pada hardware terbatas, dengan akurasi validasi mencapai 79%.
VGG16 lebih unggul dalam hal akurasi (83%) dan metrik evaluasi lainnya, membuatnya pilihan yang lebih baik jika tujuan utama adalah akurasi, asalkan hardware mendukung.
Rekomendasi: Jika Anda memerlukan model yang ringan dan cepat untuk implementasi nyata, gunakan GoogleNet. Namun, untuk keperluan akurasi tinggi seperti riset atau pengembangan lebih lanjut, pilih VGG16.

## Link Pembuatan Model

Model VGG16 : [VGG16](https://colab.research.google.com/drive/1NKFHV0IHULd5bYxTijs1g83_aoHXMNWo?usp=sharing)
Model GoogLeNet: [GoogLeNet](https://colab.research.google.com/drive/1GM1-XIHjKrXisE8-iAMrcKLAFpukZ4rX?usp=sharing)

## Link Aplikasi Web

Aplikasi web dapat diakses melalui link berikut: [Streamlit Web App](https://webprediksibunga-umi.streamlit.app/)

## Tampilan Web
![HasilApp](https://github.com/UmiNursyafikaa/UAP_DS_Umi-Nursyafika_2021-334/blob/main/gambar/hasilApp.png)

![HasilRun](https://github.com/UmiNursyafikaa/UAP_DS_Umi-Nursyafika_2021-334/blob/main/gambar/hasilRun.jpg)

## Author

Dibuat oleh [Umi Nursyafika](https://github.com/UmiNursyafikaa).
