**Sistem Rekomendasi Film Berbasis Konten Semantik**


✨ Pendahuluan
MovieVerse adalah proyek Content-Based Filtering (CBF) yang berevolusi dari metode statistik tradisional (TF-IDF) hingga model Deep Learning modern (S-BERT / Sentence-BERT) untuk memberikan rekomendasi film yang sangat akurat.

Tujuan utama proyek ini adalah memecahkan masalah klasik dalam CBF: bagaimana cara membandingkan input preferensi pengguna yang singkat ("Action, Matt Damon, Nolan") dengan konten film yang panjang (Sinopsis). Kami membuktikan bahwa S-BERT adalah solusi paling efektif untuk menghasilkan representasi vektor yang kaya semantik.

💡 Fitur Unggulan
Pembaruan Generasi Vektor: Menggantikan TF-IDF, Word2Vec, dan LSTM dengan S-BERT untuk vektorisasi sinopsis dan profil pengguna.

Rekomendasi Semantik: Menggunakan Cosine Similarity pada S-BERT Embeddings untuk menemukan film yang paling mirip makna kontekstualnya dengan preferensi pengguna.

Perbandingan Eksperimental: Mencakup analisis mendalam mengenai performa dan keterbatasan dari empat metode: TF-IDF, Word2Vec, LSTM, dan S-BERT.

Skalabilitas: Menggunakan dense vector untuk perhitungan similarity yang efisien.
