**BANK MARKETING CAMPAIGNS – OPENING DEPOSIT**

**Author: Edward Hutapea – Data Scientist**

Lokasi Dataset: https://www.kaggle.com/datasets/volodymyrgavrysh/bank-marketing-campaigns-dataset

**Overview**

Deposito memberi manfaat bagi bank dan nasabah. Bank mendapat likuiditas yang stabil, sementara nasabah memperoleh bunga lebih tinggi dengan risiko rendah. Namun, Dataset menunjukkan hanya 11% nasabah yang membuka deposito, sehingga Bank mengalami kerugian sebesar Rp 84.100.000 karena keuntungan dari pembukaan deposito tidak sebanding dengan biaya marketing yang telah dikeluarkan. Kondisi ini disebabkan oleh kesalahan Bank dalam memprediksi minat nasabah terhadap deposito.  Nasabah potensial diprediksi sebagai nasabah yang enggan membuka deposito, sehingga Bank kehilangan potensi keuntungan dari pembukaan deposito. Sebaliknya, nasabah yang enggan membuka deposito diprediksi sebagai nasabah potensial, sehingga ada biaya marketing yang terbuang sia-sia. Jika masalah ini tidak diselesaikan sekarang, kerugian Bank bisa membengkak.

Semakin banyak deposito dibuka oleh nasabah potensial, maka semakin kecil kerugian Bank, dan bahkan semakin  besar peluang Bank meraup untung. Project ini membangun model machine learning untuk identifikasi nasabah potensial (yang tertarik membuka deposito) dan nasabah yang cenderung menolak deposito. Di sisi lain, strategi marketing yang tepat sasaran dan atraktif bisa mempercepat tercapainya target Bank. Dengan menjangkau nasabah prioritas, Bank bisa lebih cepat memenuhi target marketing. Project ini juga bantu Bank menemukan nasabah prioritas berdasarkan analisa data historis marketing dan memberikan rekomendasi personalized campaign yang kontekstual sesuai profil mereka. Kombinasi model machine learning dan personalized campaign kepada nasabah prioritas bisa tingkatkan jumlah pembukaan deposito, mengurangi kerugian Bank, dan bahkan bisa memberikan Bank keuntungan.

**Insights**

1.	Nasabah Prioritas dan Personalized Campaign – Beberapa fitur dataset diolah lebih lanjut untuk menggambarkan profil demografi nasabah seperti generasi, usia, pendidikan, pekerjaan dan status pernikahan. Untuk setiap segmentasi demografi, rasio pembukaan deposito dihitung dengan membagi jumlah nasabah yang membuka deposito dengan jumlah nasabah keseluruhan. Semakin tinggi nilai rasio, maka semakin bagus riwayat pembukaan deposito, dan semakin layak menjadi prioritas dan target utama bagi Bank. Nasabah prioritas adalah (1) segmen “pensiunan, senior, silent generation atau baby boomers” dan (2) segmen “single, high education, young atau gen Z”. Selanjutnya, rekomendasi personalized promotion yang kontekstual disusun sesuai profil mereka.

2.	Model Machine Learning – Model terbaik dipilih berdasarkan F1 Score. F1-Score menyeimbangkan Recall dan Precision. Recall untuk atasi False Negative (yang menurunkan potensi keuntungan Bank), sedangkan Precision untuk atasi False Positif (yang membuat biaya marketing jadi boros). Dengan memilih F1-Score, kampanye marketing fokus pada menjangkau sebanyak mungkin nasabah potensial sambil menghindari nasabah yang enggan membuka deposito. Model terbaik yaitu Decision Tree Hyperparameter Tuning.

**Conclusion**

Jika Bank menerapkan model Decision Tree Hyperparameter Tuning dan melakukan personalized campaign kepada nasabah prioritas, maka Bank bisa beralih dari strategi marketing bersifat tebakan (instinct-driven) menjadi berbasis data (data-driven), serta memperoleh keuntungan sebesar Rp. 530.950.000. Ini adalah lompatan keuntungan yang besar karena sebelumnya (tanpa penggunaan model) Bank mengalami kerugian sebesar Rp 84.100.000.
