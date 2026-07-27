# Indonesia Stock Dividends 🇮🇩

[![Automated Update](https://img.shields.io/badge/Update-Automated-blue.svg)](#)
[![Data Format](https://img.shields.io/badge/Format-JSON-green.svg)](#)
[![Market](https://img.shields.io/badge/Market-IDX-red.svg)](#)

[🇮🇩 Bahasa Indonesia](#indonesia) | [🇬🇧 English](#english)

---

<a id="indonesia"></a>
## 🇮🇩 Bahasa Indonesia

Kumpulan data riwayat dividen saham untuk perusahaan yang terdaftar di Bursa Efek Indonesia (BEI / IDX). Repositori ini diperbarui secara otomatis secara berkala untuk memastikan data selalu *up-to-date*.

### 📂 Struktur Data

Data disediakan dalam format JSON dan dibagi menjadi dua bagian:

1. **Master File (`idx_dividends.json`)**: Berisi seluruh data dividen dari semua emiten yang tercatat, digabungkan menjadi satu file JSON. Sangat cocok untuk analisis keseluruhan pasar.
2. **Per Emiten (`dividends/`)**: Setiap emiten memiliki file JSON sendiri (contoh: `BBCA.json`, `TLKM.json`) di dalam direktori `dividends/`. Ini memudahkan jika Anda hanya membutuhkan data spesifik untuk saham tertentu tanpa harus mengunduh file master yang besar.

### 🚀 Cara Penggunaan

Anda dapat langsung menggunakan *raw URL* dari GitHub untuk mengakses data ini di aplikasi Anda.

Contoh mengambil data dari file master:
```javascript
fetch('https://raw.githubusercontent.com/dimasirginsyh/indonesia-stock-dividends/main/idx_dividends.json')
  .then(response => response.json())
  .then(data => console.log(data));
```

Contoh mengambil data untuk satu emiten (misalnya BBCA):
```javascript
fetch('https://raw.githubusercontent.com/dimasirginsyh/indonesia-stock-dividends/main/dividends/BBCA.json')
  .then(response => response.json())
  .then(data => console.log(data));
```

### ⚙️ Otomatisasi
Proses ekstraksi, pemrosesan, dan penyimpanan data dividen dijalankan secara otomatis. Data diperbarui secara berkala menggunakan GitHub Actions atau *cron job* dari *script* yang telah disiapkan.

---

<a id="english"></a>
## 🇬🇧 English

Historical stock dividend dataset for companies listed on the Indonesia Stock Exchange (IDX). This repository is automatically updated on a regular basis to ensure the data stays current.

### 📂 Data Structure

The data is provided in JSON format and is structured in two ways:

1. **Master File (`idx_dividends.json`)**: Contains the consolidated dividend data for all listed companies in a single JSON file. Ideal for comprehensive market analysis.
2. **Per-Symbol (`dividends/`)**: Each company has its own individual JSON file (e.g., `BBCA.json`, `TLKM.json`) located in the `dividends/` directory. This is useful if you only need data for specific stocks without downloading the large master file.

### 🚀 How to Use

You can fetch the data directly using the raw GitHub URLs in your applications.

Example fetching the master file:
```javascript
fetch('https://raw.githubusercontent.com/dimasirginsyh/indonesia-stock-dividends/main/idx_dividends.json')
  .then(response => response.json())
  .then(data => console.log(data));
```

Example fetching a specific symbol (e.g., BBCA):
```javascript
fetch('https://raw.githubusercontent.com/dimasirginsyh/indonesia-stock-dividends/main/dividends/BBCA.json')
  .then(response => response.json())
  .then(data => console.log(data));
```

### ⚙️ Automation
The extraction, processing, and storage of dividend data are fully automated. The dataset is updated periodically to reflect the latest dividend history available from the source.

---

**Disclaimer**: The data provided in this repository is for informational purposes only. Please verify the data with official sources before making any financial decisions. / Data yang disediakan di repositori ini hanya untuk tujuan informasi. Harap verifikasi data dengan sumber resmi sebelum membuat keputusan finansial.
