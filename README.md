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

Aplikasi ini juga dapat diakses melalui [Streamlit Cloud](https://uapandiaswad.streamlit.app/).

## Deskripsi Model

Proyek ini menggunakan dua model transfer learning:

1. **GoogleNet**: Model ini merupakan arsitektur convolutional neural network yang efektif dalam klasifikasi gambar. Dikenal karena kompleksitasnya yang rendah namun memiliki performa yang tinggi.
2. **VGG16**: Model ini memiliki arsitektur yang lebih dalam dibandingkan GoogleNet, dengan fokus pada ekstraksi fitur mendetail dari gambar.

Kedua model ini dilatih menggunakan dataset augmented untuk meningkatkan akurasi dalam klasifikasi bunga.

## Hasil Akurasi dan Analisis

![Gambar1](https://github.com/UmiNursyafikaa/UAP_DS_Umi-Nursyafika_2021-334/blob/main/gambar/googleNet.1.png)

![Gambar2](https://github.com/UmiNursyafikaa/UAP_DS_Umi-Nursyafika_2021-334/blob/main/gambar/googleNet.2.png)

![Gambar3](https://github.com/UmiNursyafikaa/UAP_DS_Umi-Nursyafika_2021-334/blob/main/gambar/googleNet.3.png)

![Gambar1](https://github.com/UmiNursyafikaa/UAP_DS_Umi-Nursyafika_2021-334/blob/main/gambar/vgg16.1.png)

![Gambar2]()

![Gambar2]()

![Gambar2]()

![Gambar2]()



## Link Pembuatan Model

Model VGG16 : [VGG16](https://colab.research.google.com/drive/1NKFHV0IHULd5bYxTijs1g83_aoHXMNWo?usp=sharing)
Model GoogLeNet: [GoogLeNet](https://colab.research.google.com/drive/1GM1-XIHjKrXisE8-iAMrcKLAFpukZ4rX?usp=sharing)

## Link Aplikasi Web

Aplikasi web dapat diakses melalui link berikut: [Streamlit Web App](https://webprediksibunga-umi.streamlit.app/)

## Tampilan Web

**(Bagian ini akan dilengkapi dengan gambar tampilan aplikasi web)**

## Author

Dibuat oleh [Nama Anda](https://github.com/username).
