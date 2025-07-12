# PROJEK_IBM
Capstone Projek Data Classification and Summarization Using IBM Granite Student Development Initiative Wave 4 juli 2025 [ Online Data Batch 9 ]

# 🏞️ Klasifikasi Kategori Pariwisata Menggunakan Model AI IBM Granite

## 📌 1. Project Title
**Klasifikasi Teks Berita Pariwisata ke dalam Kategori Wisata Alam, Wisata Buatan, Wisata Religi, dan Lainnya menggunakan LLM IBM Granite**

---

## 📖 2. Project Overview

Proyek ini bertujuan untuk mengklasifikasikan konten berita pariwisata Indonesia ke dalam empat kategori utama: **Wisata Alam**, **Wisata Buatan**, **Wisata Religi**, dan **Lainnya**.  
Klasifikasi dilakukan dengan bantuan **Large Language Model (LLM)** dari **IBM Granite** yang diakses melalui **Replicate API** dan diintegrasikan menggunakan framework **LangChain**.  

Pipeline utama meliputi:
- Pra-pemrosesan data teks (`judul` dan `konten`)
- Penerapan model IBM Granite melalui prompt klasifikasi
- Evaluasi akurasi dan f1-score menggunakan label manual
- Visualisasi confusion matrix untuk analisis kesalahan

---

## 🔗 3. Raw Dataset Link

Dataset yang digunakan dalam penelitian ini merupakan kumpulan berita pariwisata yang telah diproses, terdiri dari judul dan isi berita.  
Jika kamu ingin melihat dataset mentah (raw), bisa mengaksesnya di sini:

**[🔗 Link Dataset Mentah (CSV)](https://example.com/pariwisata_raw_dataset.csv)**  
> *Catatan: Link ini placeholder — silakan ganti dengan link asli jika tersedia.*

---

## 📊 4. Insight & Findings

Berdasarkan eksperimen awal menggunakan model **IBM Granite 3.3 8B Instruct**, diperoleh hasil sebagai berikut:

- **Akurasi keseluruhan**: 24.50%
- **Kategori dengan recall tertinggi**: `Wisata Alam` (85%)
- **Kesalahan klasifikasi terbesar terjadi pada**: `Lainnya`, di mana banyak prediksi masuk kategori ini meskipun seharusnya masuk ke 3 kategori lainnya.
- **F1-score tertinggi** ada pada `Wisata Religi` meskipun jumlah datanya paling sedikit.

> Temuan ini menunjukkan bahwa model LLM mampu memahami konteks teks, namun masih memiliki tantangan dalam membedakan kategori yang mirip secara semantik, seperti `Wisata Alam` vs `Wisata Buatan`.

---

## 🤖 5. AI Support Explanation

Model AI yang digunakan adalah **IBM Granite 3.3 8B Instruct**, sebuah **Large Language Model** yang diakses melalui **Replicate API** dan diintegrasikan menggunakan **LangChain**.  
Model ini digunakan dalam mode **zero-shot classification** dengan prompt eksplisit dalam Bahasa Indonesia seperti:

Klasifikasikan teks berikut ke dalam salah satu kategori: wisata alam, wisata buatan, wisata religi, atau lainnya.
Teks: "jelang raya hari raya waisak candi borobudur magelang jawa tengah harga tiket kereta jakarta yogyakarta akhir pekan pantau mulai rp puncak raya waisak jadwal gelar mei wisatawan hendak ikut me riah raya waisak candi borobudur beli tiket berangkat akhir pekan kompascom pantau harga tiket kereta jakarta tuju yogyakarta jelang waisak lalu access by kai rabu berangkat akhir pekan baca harga tiket kereta paling murah jakarta tuju yogyakarta akhir pekan pantau mulai rp sedia ka tambah pse lpn relasi pasarsenenyogyakarta ka tambah pse lpn relasi pasarsenenlempuyangan ka tambah pse lpn relasi jatinegarayogyakarta ka tambah pse lpn relasi jatinegaralempuyangan harga sedia berangkat sore hari tepat berangkat pukul wib baca kemudian sedia tiket kereta mulai rp ka bogowanto relasi jatinegaralempuyangan ka tambah pse slo relasi pasarsenenyogyakarta ka bogowanto relasi pasarsenenlempuyangan ka bogowanto relasi jatinegarayogyakarta ka bogowanto relasi pasarsenenyogyakarta kereta relasi harga sebut sedia berangkat sore malam hari berangkat pagi hari ratarata tiket habis jual dari itu apabila tetap tanggal cuti dapat harga tiket cocok baik pesan tiket kereta segera tiket habis"
Kategori: wisata religi
