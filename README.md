# Analisis-System-Rekomendasi-Musik-Spotify-Menggunakan-MachineLearning

**Nama**: Dhion Nur Damanhuri  
**NIM** : A11.2023.15448

# Ringkasan
Sistem rekomendasi ini dibangun untuk memprediksi apakah suatu lagu akan disukai pengguna atau tidak berdasarkan fitur audio seperti danceability, energy, valence, dll. Model machine learning yang digunakan meliputi Logistic Regression, KNN, dan Random Forest — dengan performa terbaik ditunjukkan oleh Random Forest.
  



# Ringkasan dan Permasalahan Project
  # Permasalahan
  Pengguna sering kesulitan menemukan lagu yang sesuai dengan selera mereka. Untuk itu, dibutuhkan sistem rekomendasi musik yang dapat memprediksi lagu mana yang disukai berdasarkan karakteristik audio dan metadata    lagu.

  # Tujuan
  1. Membuat sistem rekomendasi musik berbasis machine learning.
  2. Mengklasifikasikan lagu menjadi disukai (target = 1) atau tidak disukai (target = 0).
  3. Mengukur performa model dalam memprediksi ketertarikan pengguna terhadap lagu.

  # Model / Alur Penyelesain
  1. Preprocessing data Spotify Top Songs
  2. Analisis data (EDA) & feature engineering
  3. Pelatihan dan evaluasi model klasifikasi
  4. Penarikan kesimpulan dan potensi pengembangan





# Penjelasan Dataset, EDA, dan Proses features dataset
  # Dataset
  1. cleaned_spotify_top_songs.csv → Dataset utama untuk modeling, dengan 6509 entri dan 17 kolom.
  2. spotify_top_songs_audio_features.csv → Dataset lengkap dengan metadata (streams,     weeks_on_chart, dsb.)
  3. Numerik: danceability, energy, loudness, tempo
  4. Kategorikal: mode, source, key.
  5. Target: target (0 = tidak disukai, 1 = disukai)

  # EDA (Exploratory Data Analysis)
  1. Distribusi target → Apakah dataset imbalance?
  2. Korelasi antar fitur → Fitur mana paling berpengaruh terhadap target.
  3. Visualisasi: histogram, boxplot, heatmap korelasi.

  #  Proses Feature Dataset
  1. Konversi durasi dari milidetik ke menit.
  2. Encoding variabel kategorikal seperti mode, key, dan source.
  3. Normalisasi fitur numerik agar model bekerja optimal.


# Proses Learning / Modeling
  # Langkah-langkah
  1. Pisahkan fitur (X) dan target (y)
  2. Split dataset: train_test_split
  3. Model yang bisa digunakan:
     a. Logistic Regression
     b. Random Forest
     c. Decision Tree
     d. K-Nearest Neighbors (KNN)
     e. Gradient Boosting / XGBoost

  # Evaluasi Model
    1. Accuracy
    2. Precision
    3. Recall
    4. F1-score
    5. Confusion Matrix


# Performa Model
Decision Tree score: 0.95
Naive Bayes score: 0.98
Random Forest score: 1.0

# Diskusi Hasil
  1. Eksplorasi Data (EDA) menunjukkan bahwa:
     a. Lagu dengan danceability dan energy tinggi lebih disukai pengguna.
     b. Fitur seperti acousticness, instrumentalness, dan speechiness terlalu tinggi justru     cenderung menurunkan minat pendengar.
     c. Tempo dan durasi juga berperan, tetapi dalam rentang moderat (tidak terlalu cepat dan tidak terlalu lama).

  2. Pemilihan Target Kelas:
     a. Target diklasifikasikan berdasarkan kombinasi danceability dan loudness, serta dengan metode clustering (KMeans).
     b. Lagu dikategorikan sebagai disukai (1) atau tidak disukai (0).
     
  4. Model Klasifikasi Tradisional:
     a. Random Forest menghasilkan akurasi tertinggi yaitu 100% pada data latih dan sangat baik pada data uji (±98–100% tergantung split).
     b. Naive Bayes menunjukkan performa sangat baik dengan akurasi 98%, meskipun cenderung sensitif terhadap korelasi antar fitur.
     c. Decision Tree juga memberikan performa cukup baik dengan akurasi ±95%.
     
  5. Model Deep Learning (ANN):
     a. ANN dengan 2 hidden layers dan aktivasi ReLU/tanh menunjukkan akurasi yang bervariasi, berkisar 93%–95%, tergantung hyperparameter.
     b. Dengan arsitektur sederhana (input → 2 hidden → output), ANN mampu belajar dari fitur akustik seperti acousticness, liveness, valence, dll.
     c. erjadi potensi overfitting jika jumlah layer atau epoch terlalu tinggi, yang bisa mengurangi kemampuan generalisasi model.
  
