**Sistem Rekomendasi Film Berbasis Konten Semantik**

🔥 **Mengapa Model Rekomendasi Anda Perlu S-BERT?**
Setiap sistem rekomendasi film berbasis konten (Content-Based Filtering) menghadapi tantangan fundamental: Bagaimana membandingkan profil preferensi pengguna yang sangat singkat (misalnya, "Action, Chris, Ang Lee") dengan sinopsis film yang panjang dan penuh nuansa?

Proyek ini adalah sebuah Odyssey Vektorisasi, sebuah perjalanan membuktikan bahwa metode tradisional sudah usang. Kami membawa movie recommendation ke level Deep Learning Semantik untuk memberikan hasil yang tidak hanya akurat, tetapi juga benar-benar kontekstual!

🔬 Evolusi Model: Mengapa Model Lain Tumbang?
Kami menguji empat generasi model vektorisasi, dan hasilnya menunjukkan bahwa hanya arsitektur Transformer yang mampu mengatasi tantangan similarity ini.

1. Era Klasik: TF-IDF dan Word2Vec 📉
TF-IDF: Metode statistik ini berhasil menemukan kecocokan literal (Ang Lee), tetapi gagal total dalam memahami makna yang lebih luas. Film yang direkomendasikan adalah hasil dari kecocokan kata kunci acak, bukan kesamaan konten semantik.

Word2Vec (Average): Model ini memahami makna kata (action vs thriller), tetapi ketika kami menggabungkan vektornya (average pooling) untuk mewakili sinopsis, vektor ini kehilangan informasi spesifik. Preferensi unik pengguna, seperti nama sutradara, menjadi terlalu encer, sehingga rekomendasi hanya berfokus pada genre-genre yang dominan.

2. Era Sekuensial: LSTM Encoder Sederhana ❌
Kami mencoba arsitektur LSTM (Long Short-Term Memory) untuk menangkap urutan kata dalam sinopsis. Secara teori, ini adalah langkah maju.

Hasilnya Gagal Total. Model LSTM yang dilatih pada teks panjang (sinopsis) menjadi sangat tidak stabil ketika diberi input pendek (profil pengguna). Perbedaan panjang input ini menyebabkan vektor keluarannya menjadi acak dan tidak relevan dengan preferensi sama sekali. Ini membuktikan bahwa LSTM sederhana tidak cocok untuk tugas similarity antar dokumen dengan panjang yang bervariasi.

3. Solusi Revolusioner: S-BERT (Sentence-BERT) ✨
S-BERT adalah pahlawan yang dibutuhkan proyek ini. Sebagai model berbasis Transformer yang dilatih ulang secara khusus untuk tugas Semantic Similarity, S-BERT berhasil mengatasi semua kelemahan model sebelumnya.

Model ini mampu menafsirkan input pendek ("Action, Chris, Ang Lee") sebagai entitas semantik yang utuh dan membandingkannya secara konsisten dengan sinopsis yang panjang. Vektor yang dihasilkan S-BERT kaya akan konteks mendalam, menghasilkan skor kemiripan yang tinggi dan rekomendasi yang benar-benar relevan.
