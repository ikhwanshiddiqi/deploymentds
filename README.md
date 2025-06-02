# Cryptocurrency Price Prediction System

Sistem ini adalah aplikasi web untuk memprediksi harga cryptocurrency. Aplikasi ini menggunakan Flask sebagai back-end untuk memproses data, memuat model prediksi, dan menghasilkan output prediksi. Antarmuka pengguna dibangun dengan Bootstrap dan JavaScript untuk memberikan pengalaman single-page yang dinamis dan interaktif.

## Struktur Repository

```

Project/
├── app.py                    # Aplikasi Flask utama
├── templates/
│   └── index.html            # Template halaman utama
├── static/                   # (Opsional) File statis (CSS, JS, gambar), tapi karena saya menggunakan cdn, jadi tidak ada
├── dataset/                  # File CSV dataset (misal: btc.csv, eth.csv, dll.)
├── model/                    # File model (.keras) untuk masing-masing dataset
├── scaler/                   # File scaler (.pkl) untuk masing-masing dataset
└── README.md    
```

## Prasyarat

- Python 3.8 atau lebih baru
- Virtual environment (disarankan)
- Paket Python yang dibutuhkan:
  - Flask
  - pandas
  - numpy
  - scikit-learn
  - tensorflow (atau package Keras dari tensorflow)
  - (pickle sudah termasuk di Python)
- Koneksi internet (untuk memuat Bootstrap dan Font Awesome dari CDN)

## Cara Menjalankan Sistem

1. **Persiapkan File**
   - Pastikan file dataset (CSV) tersedia di folder `dataset/`.
   - Pastikan file model (.keras) tersedia di folder `model/`.
   - Pastikan file scaler (.pkl) tersedia di folder `scaler/`.

2. **Jalankan Aplikasi**

   ```bash
   python app.py
   ```

3. **Akses Aplikasi**

   Buka browser dan masuk ke: [http://127.0.0.1:5000](http://127.0.0.1:5000)

4. **Gunakan Aplikasi**
   - Pada halaman utama, pilih opsi prediksi seperti jenis cryptocurrency, model, dan jumlah hari ke depan.
   - Klik tombol **Prediksi Sekarang** untuk melihat prediksi, grafik, dan metrik evaluasi.
   - Klik **Kembali** untuk mengubah pilihan dan membuat prediksi baru.

## Kustomisasi dan Pengembangan

- **Styling:** Template menggunakan Bootstrap dan beberapa custom CSS agar tampilan selaras dengan tema (mis., warna header, kartu, tombol).
- **JavaScript:** Penggunaan Fetch API memungkinkan tampilan bagian hasil diperbarui secara dinamis tanpa harus reload seluruh halaman.
- **Back-end:** Kode Flask pada `app.py` menangani pemrosesan data, pemuatan model, pembuatan prediksi, serta pengiriman data ke template.

## Troubleshooting

- **Field Tidak Valid/Csv Error:** Pastikan file CSV memiliki format yang konsisten dan kolom `Close` ada.
- **Model atau Scaler Tidak Ditemukan:** Periksa kembali penamaan file di folder `model/` dan `scaler/` serta pastikan nama yang dikirim dari form sesuai.
- **Masalah Tampilan:** Cek konsol browser dan pastikan fetch API berjalan tanpa error.

## Acknowledgements

- [Flask](https://flask.palletsprojects.com/)
- [Bootstrap](https://getbootstrap.com/)
- [Font Awesome](https://fontawesome.com/)
- [TensorFlow](https://www.tensorflow.org/)
- [scikit-learn](https://scikit-learn.org/)

## Dataset
Dataset yang digunakan dapat diakses pada website yahoo finance.
- Bitcoin (BTC-USD) -> [Akses Disini](https://finance.yahoo.com/quote/BTC-USD/)
- Ethereum (ETH-USD) -> [Akses Disini](https://finance.yahoo.com/quote/ETH-USD/)
- Ripple (XRP-USD) -> [Akses Disini](https://finance.yahoo.com/quote/XRP-USD/)
- Solana (SOL-USD) -> [Akses Disini](https://finance.yahoo.com/quote/SOL-USD/)

---

Selamat mencoba dan semoga bermanfaat!
