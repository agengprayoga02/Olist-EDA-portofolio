# E-Commerce EDA & Data Preparation — Olist Brazilian E-Commerce Dataset

Latihan & proyek portofolio Data Analyst: **EDA, Data Preparation, dan Visualisasi** menggunakan dataset transaksi nyata dari marketplace Olist (Brazil, 2016–2018). Proyek ini terinspirasi dari notebook Kaggle [*E-Commerce Sentiment Analysis: EDA + Viz + NLP*](https://www.kaggle.com/code/thiagopanini/e-commerce-sentiment-analysis-eda-viz-nlp) oleh Thiago Panini, tetapi dibangun ulang dari nol dengan narasi dan interpretasi bisnis sendiri, difokuskan pada tiga skill inti: **data understanding & cleaning, EDA, dan visualisasi** — tanpa bergantung pada teks review berbahasa Portugis (bagian NLP/sentiment sengaja tidak direplikasi di fase ini).

Fase ini adalah **langkah 1** dari rencana besar: hasil (Analytical Base Table yang sudah bersih) akan menjadi fondasi data untuk **web dashboard** di fase berikutnya.

## 🎯 Pertanyaan Bisnis

1. Bagaimana tren penjualan Olist dari waktu ke waktu?
2. Seberapa baik performa pengiriman, dan apakah memengaruhi kepuasan pelanggan?
3. Kategori produk apa yang paling laris & paling menyumbang revenue?
4. Metode pembayaran apa yang paling banyak dipakai?
5. Dari mana mayoritas pelanggan & seller berasal?
6. Apakah Olist punya basis pelanggan loyal (repeat customer)?
7. Faktor apa yang paling berkorelasi dengan review score rendah?

## 📊 Ringkasan Temuan Utama

- Rata-rata waktu pengiriman **12 hari** (median 10 hari); **6,8% order terlambat**, rata-rata keterlambatan 10,6 hari.
- Order yang terlambat mendapat rata-rata review **2,27**, jauh di bawah order tepat waktu (**4,29**) — faktor operasional pengiriman adalah pendorong kepuasan pelanggan paling dominan (lebih kuat dari harga/cicilan).
- Kartu kredit mendominasi **76,9%** transaksi, rata-rata cicilan 2,9x.
- Seller terkonsentrasi **70% di São Paulo**, sementara pelanggan tersebar lebih merata — indikasi kesenjangan jarak kirim ke state lain.
- Kategori revenue tertinggi: `health_beauty`, `watches_gifts`, `bed_bath_table`.
- Hanya **3,1% pelanggan** yang repeat order — potensi terbesar untuk perbaikan bisnis ada di sisi retensi pelanggan.

Detail lengkap beserta chart ada di notebook.

## 🗂️ Struktur Project

```
├── data/
│   ├── raw/            # 9 CSV mentah dari Kaggle (tidak di-commit, lihat instruksi di bawah)
│   └── processed/       # orders_abt.csv & items_abt.csv — hasil cleaning & merge, siap pakai
├── notebooks/
│   └── 01_eda_data_preparation.ipynb
└── README.md
```

## 🔄 Cara Reproduksi

1. Unduh dataset dari Kaggle: [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
2. Letakkan ke-9 file CSV-nya di `data/raw/`
3. `pip install pandas numpy matplotlib seaborn jupyter`
4. Jalankan `notebooks/01_eda_data_preparation.ipynb`

## 🧰 Tech Stack

Python · Pandas · NumPy · Matplotlib · Seaborn · Jupyter Notebook

## 🚀 Roadmap

- [x] **Fase 1** — Data Understanding, Cleaning, EDA & Visualisasi *(notebook ini)*
- [ ] **Fase 2** — Web dashboard interaktif (KPI: revenue, delivery performance, top kategori, sebaran geografis) menggunakan `data/processed/*.csv` sebagai data source
- [ ] **Fase 3 (opsional)** — Sentiment analysis pada review pelanggan (butuh penanganan teks berbahasa Portugis)

## 📎 Sumber Data

[Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) — dirilis dengan lisensi CC BY-NC-SA 4.0. Digunakan untuk keperluan latihan & portofolio non-komersial.
