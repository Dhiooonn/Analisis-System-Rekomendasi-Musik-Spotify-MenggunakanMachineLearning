# Analisis-System-Rekomendasi-Musik-Spotify-MenggunakanMachineLearning

**Nama**: Dhion Nur Damanhuri  
**NIM** : A11.2023.15448


# Ringkasan dan Permasalahan Project
  # Permasalahan
  Pengguna sering kesulitan menemukan lagu yang sesuai dengan selera mereka. Untuk itu, dibutuhkan sistem rekomendasi musik yang dapat memprediksi lagu mana yang disukai berdasarkan karakteristik audio dan metadata    lagu.

  # Tujuan
  1. Membuat sistem rekomendasi musik berbasis machine learning.
  2. Mengklasifikasikan lagu menjadi disukai (target = 1) atau tidak disukai (target = 0).
  3. Mengukur performa model dalam memprediksi ketertarikan pengguna terhadap lagu.

  # Model / Alur Penyelesain


# Penjelasan Dataset, EDA, dan Proses features dataset
  # Dataset
  1. cleaned_spotify_top_songs.csv → Dataset utama untuk modeling, dengan 6509 entri dan 17 kolom.
  2. spotify_top_songs_audio_features.csv → Dataset lengkap dengan metadata (streams,     weeks_on_chart, dsb.)
  3. Numerik: danceability, energy, loudness, tempo
  4. Kategorikal: mode, source, key.
  5. Target: target (0 = tidak disukai, 1 = disukai)
