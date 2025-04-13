Analisis Efektivitas Kampanye terhadap Produk Supermarket  
### Studi Multi-Kampanye terhadap Pola Pengeluaran Pelanggan  

---

## Ringkasan Proyek

Proyek ini merupakan tugas capstone untuk Modul 2 dari program Data Science di Purwadhika.  
Saya menganalisis bagaimana berbagai *kampanye pemasaran* memengaruhi *perilaku pengeluaran pelanggan* terhadap berbagai kategori produk di sebuah supermarket.

Melalui pipeline analisis data yang sistematis, saya menghasilkan metrik utama dan wawasan berbasis data untuk mendukung keputusan strategis dalam pemasaran.

---

## Rumusan Masalah

> *Kampanye pemasaran mana yang paling efektif dalam meningkatkan pengeluaran pelanggan pada tiap kategori produk supermarket?*

Definisi efektivitas kampanye diukur berdasarkan:
- Tingkat penerimaan kampanye (`AcceptedCmp1` hingga `AcceptedCmp5`, dan `Response`)
- Nilai pembelian per kategori produk
- Korelasi antara respons pelanggan dan total pengeluaran

---

## Tools & Teknologi

| Tools | Fungsi |
|-------|--------|
| Python (pandas, numpy, seaborn, matplotlib) | Pembersihan & analisis data |
| Jupyter Notebook | Eksplorasi & dokumentasi interaktif |
| GitHub | Versi kontrol & dokumentasi |
| CSV / Excel | Format dataset awal |
| Plotly | Visualisasi interaktif (jika diperlukan) |

---

## Dataset

Dataset berisi informasi profil pelanggan supermarket dan histori partisipasi mereka dalam kampanye pemasaran.  
Setiap baris mewakili satu pelanggan, dengan variabel demografi, total pengeluaran, dan penerimaan kampanye.

Fitur utama yang digunakan:
- Demografi: usia, status menikah, pendidikan, pendapatan
- Pengeluaran: `MntWines`, `MntFruits`, `MntMeatProducts`, `MntFishProducts`, `MntSweetProducts`, `MntGoldProds`
- Kampanye: `AcceptedCmp1–5`, `Response`
- Aktivitas belanja: saluran (web, store), waktu menjadi pelanggan

---

## Pembersihan & Pemrosesan Data

Langkah-langkah yang dilakukan:

1. Menghapus kolom tidak relevan (misalnya `ID`, `Z_CostContact`)
2. Membuat fitur baru:
   - `TotalSpend`: total belanja di semua kategori produk
3. Mengubah tipe data dan menangani missing values
4. Membuat flag biner untuk penerimaan kampanye
5. Menyaring outlier agar hasil analisis valid
6. Membuat *heatmap* korelasi untuk mengukur hubungan antar variabel

---

## Visualisasi & Eksplorasi

| Jenis Visualisasi | Judul | Insight |
|-------------------|-------|---------|
| Heatmap | *Kampanye vs Pengeluaran Produk* | Menunjukkan hubungan kuat antara kampanye dan kategori tertentu |
| Bar Chart | *Visualisasi Data untuk Memahami Efektivitas Kampanye* | Pola preferensi kampanye berdasarkan tingkat penjualan |

---

## Insight Utama

- `AcceptedCmp5` berkorelasi kuat dengan pembelian produk anggur (`MntWines`)  
- Pelanggan yang menerima lebih banyak kampanye cenderung belanja lebih banyak di kategori *emas* dan *daging*  
- Pendidikan tinggi cenderung lebih responsif terhadap kampanye  
- `TotalAccepted` berkorelasi positif dengan keterlibatan kanal digital dan transaksi toko  
- Kampanye tertentu menciptakan *efek lintas kategori* (cross-selling)

---

## Kesimpulan

Proyek ini menunjukkan bagaimana kampanye pemasaran yang ditargetkan dapat berdampak signifikan pada peningkatan pengeluaran pelanggan pada kategori produk tertentu.  
Dengan membuat metrik turunan dan melakukan analisis korelasi, kita bisa mengidentifikasi kampanye mana yang paling *efisien dan efektif* secara strategis.

Wawasan ini berguna untuk:
- Tim pemasaran dalam merancang kampanye personalisasi
- CRM untuk pengelompokan dan targeting pelanggan
- Tahapan lanjutan seperti *uplift modeling* dan prediksi respons kampanye

---

## Tautan

-  *Notebook Proyek*: `Capstone Supermarket.ipynb`  
- *Presentasi*: [Link ke Canva atau PDF](https://www.canva.com/design/DAGkf6kkyQo/H9-_3kY5arQ8Q2XbMC0OjA/edit)
