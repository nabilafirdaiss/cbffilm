Sistem Rekomendasi Film 

Proyek ini bertujuan untuk membangun sistem rekomendasi film yang dapat menampilkan daftar film yang mirip berdasarkan konten (genre, sinopsis, aktor, sutradara).
Selain metode klasik TF-IDF + Cosine Similarity, repositori ini juga mencakup implementasi deep learning menggunakan LSTM sebagai pembanding.

📌 Fitur Utama
1. Content-Based Filtering (CBF)

Menggabungkan beberapa fitur film (genre, sinopsis, aktor, sutradara).

Menggunakan TF-IDF dan Word2Vec untuk ekstraksi fitur teks.

Menggunakan Cosine Similarity untuk mengukur kemiripan antarfilm.

Menghasilkan daftar rekomendasi film paling mirip.

2. Implementasi Deep Learning (LSTM)

Mengubah sinopsis film menjadi vektor embedding menggunakan LSTM.

Menghasilkan latent representation film versi deep learning.

Mengukur kemiripan antarfilm menggunakan cosine similarity.

