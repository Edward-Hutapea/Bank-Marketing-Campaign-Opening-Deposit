**BANK MARKETING CAMPAIGNS – OPENING DEPOSIT**

**Author: Edward Hutapea – Data Analyst**

**Dataset**
-	Lokasi https://www.kaggle.com/datasets/volodymyrgavrysh/bank-marketing-campaigns-dataset
-	Fitur-fitur di dataset berkaitan dengan profil demografi nasabah, riwayat kredit nasabah, riwayat komunikasi nasabah dengan tim marketing bank dan indikator makro ekonomi.

**Overview**

Deposito memberi manfaat bagi bank dan nasabah. Bank mendapat likuiditas yang stabil, sementara nasabah memperoleh bunga lebih tinggi dengan risiko rendah. Namun, Dataset menunjukkan hanya 11% nasabah yang tertarik membuka deposito. Kondisi ini membuat Bank merugi sebesar Rp 84.100.000 karena keuntungan dari pembukaan deposito tidak sebanding dengan biaya marketing yang telah dikeluarkan.

**Problem Statement**

Bank memprediksi nasabah yang sebenarnya berpotensi membuka deposito sebagai nasabah yang tidak mau membuka deposito", sehingga Bank kehilangan potensi keuntungan dari pembukaan deposito. Sebaliknya, nasabah yang sebenarnya "tidak mau membuka deposito" diprediksi sebagai "calon nasabah potensial", sehingga ada biaya marketing yang terbuang sia-sia. Kedua kesalahan prediksi ini bisa merugikan Bank. 

**Goals**

Tujuan project ini adalah membangun model machine learning untuk identifikasi calon nasabah potensial untuk membuka deposito dan calon nasabah yang cenderung menolak deposito. Project ini juga menganalisa riwayat data marketing untuk memberikan rekomendasi ”personalized campaign" yang bisa digunakan Bank dalam pendekatan kepada nasabah potensial. Kombinasi model machine learning dan personalized campaign mengoptimalkan kegiatan marketing dan meningkatkan profit Bank.

**Machine Learning Models Tested**
- Logistic Regression
- K-Nearest Neighbors (KNN) dan KNN Hyperparameter Tuning
- Decision Tree dan Decision Tree Hyperparameter Tuning
- Random Forest dan Random Forest Hyperparameter Tuning

**Evaluation Metrics: F1 Score**
- F1-Score merupakan metrik yang tepat untuk menyeimbangkan Recall dan Precision. Dimana Recall berfungsi untuk mengatasi False Negative (yang bisa menurunkan potensi keuntungan Bank), sedangkan Precision berfungsi untuk mengatasi False Positif (yang bisa membuat biaya marketing menjadi boros). 
- Dengan memilih F1-Score, kampanye marketing fokus pada menjangkau sebanyak mungkin nasabah potensial dan sambil menghindari nasabah yang tidak tertarik membuka deposito.

**Best Model Summary: Decision Tree Hyperparameter Tuning**
- F1 Score: 0.49
- Monetisasi - Pemanfaatan model ini membuat Bank bisa mengalami keuntungan sebesar Rp. 530.950.000. Ini adalah lompatan keuntungan yang besar karena sebelumnya (tanpa penggunaan model) Bank mengalami kerugian sebesar Rp 84.100.000.
 
**Key Insights**
1. Berdasarkan analisa riwayat data marketing, nasabah prioritas yang bisa dijadikan target utama oleh Bank adalah (1) kelompok “pensiunan, senior, silent generation atau baby boomers” dan (2) kelompok “single, high education, young atau gen Z.
2. Untuk nasabah prioritas, tingkat keberhasilan pembukaan deposito meningkat ketika marketing dilakukan kepada (1) existing customer, atau (2) nasabah yang sebelumnya telah membuka deposito, atau (3) nasabah yang tidak punya riwayat gagal bayar utang ke Bank.
3. Nasabah prioritas lebih responsif terhadap kampanye deposito jika dihubungi melalui HP pada hari selasa, rabu dan kamis (khususnya pada bulan April s/d Agustus).
4. Decision Tree Hyperparameter Tuning dengan class weight untuk mengatasi data imbalance menghasilkan sebuah model prediksi yang paling efektif.

**Rekomendasi**
1.	Add New Features – Tambah fitur baru seperti income nasabah, spending nasabah, nilai deposito yang dibuka nasabah, dan jangka waktu deposito yang dipilih nasabah.
2.	Test Alternative Models – Coba model XGBoost dan LightGBM untuk mengeksplorasi potensi model prediksi yang lebih efektif lagi.
3.	Model Segmentation – Pisahkan data nasabah prioritas dan data nasabah bukan prioritas. Kemudian kembangkan 2 model machine learning secara terpisah. Segmentasi seperti ini bisa menghasilkan model prediksi yang lebih akurat dan kontekstual.
4.	Integration into Operational Systems, Monitoring & Re-training Data – Integrasikan model ke dalam system operasional mobile banking dan internet banking sehingga Bank bisa monitor implementasi model prediksi secara real-time. Lakukan juga training data secara rutin berdasarkan data marketing terbaru untuk meningkatkan akurasi model terhadap data terbaru.
