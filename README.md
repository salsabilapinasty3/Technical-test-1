# TechnicalTest-MandiriSekuritas  
# Transaction Patterns & Purchase Behavior Analysis 
# 📝 Ringkasan
Proyek ini berfokus pada analisis kebiasaan transaksi pengguna menggunakan tiga set data utama yaitu users, cards, dan transactions. Seluruh proses dimulai dari pembersihan data di Python (Google Colab), dilanjutkan dengan penyimpanan di BigQuery untuk memudahkan eksekusi  query berskala besar, dan diakhiri dengan pembuatan dashboard interaktif di Looker Studio.
# ⚙️ Alur Pengerjaan
1. Persiapan Data
- Jalankan script python (berisi keseluruhan data) yang diguanakn untuk membersihkan data dan merapihkan.
- Ekspor menjadi beberapa file CSV (data transaksi, karena data lebih dari 100 MB) berukuran ≤100 MB.
- Unggah file tersebut ke BigQuery menggunakan wildcard pada data transaksi (yang dibagi menjadi 27 data transaksi) agar menjadi satu file.
- Unggah file cards dan file users juga yang telah di bersihkan
2. Pembuatan Ringkasan Data
- Gunakan skrip SQL di folder /queries/ untuk menghasilkan tabel ringkasan seperti:
- transactions_per_gender - distribusi transaksi berdasarkan gender
- transactions_per_cards_brands – distribusi transaksi berdasarkan brand kartu
- transactions_per_age_group – distribusi transaksi berdasarkan kelompok usia
- transactions_monthly – transaksi setiap bulan
- transactions_darkweb – transaksi menggunakan web yang jelas atau tidak
-transactions_chanel – distibusi transaksi menggunakan online, bayar langsung dll
- income_vs_spending - melihat jumlah dan perbandingan
- debt_ratio_spending - melihat rasio hutang dengan pengeluaran
3. Visualisasi di Looker Studio
- Sambungkan dataset BigQuery yang telah diringkas menggunakan fitur yang terdapat pada looker studio
- Bangun dashboard berisi seluruh query yang telah di buat
# 📊 Isi Dashboard
# KPI Cards:
- Total Spent
- Total Transactions by Age
- Total Amount by Gender
- Average Transaction Value
# Visualisasi Utama:
- Proportion of Total Transactions by Cards
- Transactions per Gender
- Channel Transactions
- Transactions per Age Group
- Monthly Transaction Trend
- Average Spend by Age Group
# 🚀 Cara Menjalankan
- Clone repository ini
- Jalankan notebook pembersihan (clean.ipynb)
- Unggah hasil data users, cards, transaction (dibagi menjadi 27 file)ke BigQuery
- Gabungkan seluruh file transaction (27 file) agar menjadi 1 file
- Jalankan semua perintah SQL di direktori /queries/ guna membuat tabel ringkasan
- Setelah itu membuat dashboard di looker studio dengan menggunakan data hasil query yang telah di hubungkan



