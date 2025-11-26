**Sistem Rekomendasi Film Berbasis Konten Semantik**

✨ Revolusi dari Frekuensi Kata ke Pemahaman Makna
MoviePulse adalah proyek Content-Based Filtering (CBF) yang merevolusi cara film direkomendasikan. Kami beralih dari metode statistik yang dangkal ke model Deep Learning tingkat lanjut, Sentence-BERT (S-BERT), untuk menghasilkan rekomendasi yang didasarkan pada pemahaman semantik mendalam.

Proyek ini mengatasi tantangan inti CBF: Bagaimana membandingkan profil preferensi pengguna yang sangat singkat (misalnya, genre, aktor, sutradara) dengan sinopsis film yang panjang dan kaya narasi?

🎯 Tujuan Proyek: Mengukur Kemiripan Konten yang Sebenarnya
Tujuan kami adalah mengimplementasikan Deep Learning untuk mengubah sinopsis film menjadi Dense Vector (Embedding), dan kemudian menggunakan Cosine Similarity untuk merekomendasikan film.

Kami tidak hanya ingin mencocokkan kata kunci; kami ingin model memahami makna kontekstual dari sinopsis, sehingga film tentang "petualangan survival" mirip dengan preferensi yang berfokus pada "aksi" dan "drama".

🛠️ Perjalanan Eksperimental: Mengapa Model Lain Gagal?
MoviePulse melalui serangkaian eksperimen yang membuktikan mengapa arsitektur Transformer (S-BERT) adalah satu-satunya solusi yang stabil untuk proyek ini.

1. Kegagalan Baseline (TF-IDF & Word2Vec) 📉
Kami memulai dengan standar industri:

TF-IDF: Berhasil mencocokkan nama unik seperti "Ang Lee," tetapi gagal total dalam memahami bahwa Action dan Thriller memiliki makna yang dekat. Rekomendasi didominasi oleh kebetulan kata kunci, bukan konten sebenarnya.

Word2Vec (Average): Model ini memahami makna kata (action), tetapi ketika kami menggabungkan semua vektor kata menjadi satu (average pooling), bobot preferensi unik pengguna menjadi encer. Model ini tidak mampu menemukan aktor atau sutradara spesifik, hanya berfokus pada genre yang dominan.

2. Eliminasi Model Sekuensial (LSTM Encoder) ❌
Kami meningkatkan proyek dengan menggunakan LSTM untuk memproses sinopsis, dengan harapan model belajar urutan kata. Namun, model ini gagal karena masalah fundamental:

Ketidakstabilan Vektor: LSTM kami dilatih pada sinopsis yang sangat panjang, tetapi ketika dihadapkan pada input pengujian yang sangat pendek (preferensi pengguna), model gagal menghasilkan vektor yang stabil dan konsisten. Hasil rekomendasi menjadi acak dan tidak relevan.

3. Solusi Kunci: S-BERT (Sentence-BERT) ✅
S-BERT adalah model yang menyelesaikan semua masalah di atas karena dirancang secara spesifik untuk tugas similarity.

Stabil Terhadap Panjang Teks: S-BERT dilatih untuk memaksa vektor dari teks yang mirip (terlepas dari apakah teks itu pendek atau panjang) untuk berdekatan dalam ruang embedding. Ini menjamin bahwa profil pengguna dapat dibandingkan secara adil dengan sinopsis film.

Kontekstualitas Mendalam: Menggunakan arsitektur Transformer, S-BERT mampu menangkap konteks bidireksional dan menghasilkan embedding yang paling kaya semantik, menghasilkan skor kemiripan yang akurat dan relevan.

🚀 Quick Start: Menjalankan MoviePulse
Untuk memulai dan menguji sendiri superioritas S-BERT:
