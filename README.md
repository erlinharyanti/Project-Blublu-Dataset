# Business Retail Performance & Customer Behavior Analysis

## 📌 Project Overview
Proyek ini bertujuan untuk menganalisis data customer dan transaksi mentah, melakukan pembersihan data (*data cleaning*) secara presisi, dan membangun *dashboard* interaktif menggunakan Power BI. Hasil akhir dari proyek ini berupa *insight* berbasis data yang membantu perusahaan mengevaluasi performa penjualan produk serta memahami perilaku belanja pelanggan untuk optimasi strategi bisnis.

## 🛠️ Tools & Tech Stack
* **Data Cleaning & Preparation:** Microsoft Excel (Power Query)
* **Data Modeling & Visualization:** Microsoft Power BI
* **Dataset:** Blublu Customer Dataset, Blublu helper (category & rates)

## ⚠️ Business Problem
Data transaksi mentah perusahaan masih memiliki berbagai inkonsistensi format penulisan, kesalahan tanda baca pada kategori, dan tipe data yang tidak terstruktur. Jika data ini langsung diolah, akan menghasilkan analisis yang bias atau *error*. Perusahaan membutuhkan proses pembersihan data yang hati-hati—agar riwayat transaksi berulang dari pelanggan yang valid tidak terhapus—dilanjutkan dengan pembuatan *dashboard* analitik.

## 🧹 Data Preparation & Data Modeling (Actions)
Langkah-langkah yang dilakukan dalam memproses data mentah menjadi data siap analisis:
1. **Handling Duplicates:** Mempertahankan data *Customer ID* yang duplikat karena teridentifikasi secara logis sebagai riwayat transaksi berulang yang valid dari pelanggan yang sama pada waktu yang berbeda.
2. **Data Type Formatting:** Mengoreksi tipe data di Power Query (konversi teks ke *whole number/decimal*, format YYYY/MM/DD untuk *date*, dan nilai *boolean* True/False).
3. **Data Quality Check:** Memvalidasi keutuhan dataset dan memastikan 100% data bersih dari *missing values* menggunakan fitur *Column Quality*.
4. **Standardization:** Melakukan *Trim*, *Clean*, dan standardisasi huruf (*Capitalize Each Word*) untuk menyeragamkan entri teks yang berantakan pada kolom `Payment_Method` (contoh: menyatukan "paypal", "Paypal", dan "other").
5. **Text Formatting:** Memperbaiki inkonsistensi tanda baca dan kurung pada kolom `Purchase_Category` (contoh pada entri "Travel & Leisure").
6. **Data Modeling:** Membangun relasi (*1-to-many*) di Power BI antara kolom `Category` pada tabel `category` (*dimension table*) dengan kolom `Purchase_Category` pada tabel `Cleaning` (*fact table*).

## 📊 Dashboard Visualizations
Proyek ini menghasilkan 2 halaman *dashboard* utama:
1. Business Performance:** Fokus pada metrik finansial utama, tren pendapatan per bulan, top kategori produk, kontribusi *channel* pembelian, dan pendapatan berdasarkan demografi.
2. **Dashboard 2 - Customer Satisfaction & Behavior:** Fokus pada analisis kepuasan pelanggan, metode pembayaran, sensitivitas terhadap diskon, dan tingkat loyalitas merek (*Brand Loyalty*).

## 💡 Key Insights & Recommendations (Results)
Berdasarkan visualisasi data yang telah dibangun, ditemukan beberapa temuan krusial untuk keputusan bisnis:

* **🎯 Optimasi Budget Promo (The "Aha!" Moment):** Matriks *Heatmap Purchase Intent* menunjukkan bahwa angka tertinggi pembeli dadakan (*Impulsive*) justru didominasi oleh kelompok pelanggan yang **tidak sensitif terhadap diskon** (*Not Sensitive*). Insight ini membuktikan bahwa dorongan belanja mereka murni karena keinginan sesaat, bukan karena potongan harga. **Rekomendasi:** Perusahaan dapat menyelamatkan margin keuntungan dengan memangkas pemberian diskon pada segmen ini tanpa takut kehilangan volume penjualan.
* **⭐ Performa Kualitas Produk:** Kategori *Travel* dan *Digital Goods* konsisten meraih rata-rata penilaian (*Average Product Rating*) tertinggi di angka >3.0. Kedua kategori ini memiliki tingkat kepuasan yang sangat baik dan potensial dijadikan ujung tombak untuk materi kampanye iklan.
* **🚚 Efisiensi Operasional:** Mayoritas pelanggan menggunakan PayPal dan lebih memilih pengiriman standar (*No Preference*) secara merata di semua tingkat pendapatan (*Income Level*). **Rekomendasi:** Operasional bisa difokuskan pada jalur pembayaran dan pengiriman tersebut tanpa perlu membuang biaya untuk membuat promo eksklusif berbasis kelas ekonomi pelanggan.
* **📈 Stabilitas Bisnis:** Total pendapatan sebesar $387.14K berhasil dicapai, dengan rata-rata kepuasan pengalaman belanja yang tergolong stabil di angka 5.37 dari skala 10.
