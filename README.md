# Analisis Dataset Berita Indonesia

Proyek Tugas 1 Analisis Big Data menggunakan dataset `idn-news-az`. Informasi
dataset dan cara memperolehnya tersedia pada [`data/README.md`](data/README.md).

Notebook dikerjakan berurutan:

1. `notebooks/01_data_profiling.ipynb`
2. `notebooks/02_data_cleaning.ipynb`
3. `notebooks/03_eda_and_insights.ipynb`

## Menjalankan Project

Pastikan Docker sudah terpasang pada komputer Anda.

### Build Docker Image

```bash
docker build -t tugas1-bigdata .
```

### Jalankan Container

```bash
docker run --rm -p 8888:8888 -v "$(pwd)":/home/jovyan/work tugas1-bigdata
```

### Membuka JupyterLab

Buka browser dan akses:

http://localhost:8888/lab

> **Catatan:** Konfigurasi Dockerfile menjalankan JupyterLab tanpa password atau token untuk penggunaan lokal. Jangan gunakan konfigurasi ini pada server atau jaringan publik.

---

## Menyiapkan Dataset

1. Letakkan dataset yang akan digunakan pada folder:

```text
data/raw/
```

2. Buka notebook profiling atau notebook yang digunakan.
3. Sesuaikan nilai variabel `DATA_PATH` agar mengarah ke file dataset yang Anda gunakan.

Contoh:

```python
DATA_PATH = "data/raw/nama_dataset.csv"
```

---

## Mengerjakan Tugas

1. Baca seluruh instruksi yang terdapat pada notebook.
2. Kerjakan setiap bagian sesuai perintah.
3. Simpan perubahan secara berkala.

---

## Commit Perubahan

Setelah tugas selesai dikerjakan, simpan hasil pekerjaan ke Git menggunakan perintah berikut:

```bash
git add .
git commit -m "Menyelesaikan Tugas 1 Analisis Big Data"
```

Anda dapat mengganti pesan commit sesuai kebutuhan.

---

## Push ke Repository GitHub

Kirim hasil pekerjaan ke repository GitHub milik Anda:

```bash
git push origin main
```

Apabila branch utama bernama `master`, gunakan:

```bash
git push origin master
```

---

## Verifikasi Pengumpulan

1. Buka repository GitHub milik Anda.
2. Pastikan file yang telah dikerjakan sudah muncul.
3. Pastikan terdapat minimal satu commit hasil pekerjaan Anda.
4. Salin URL repository Anda untuk keperluan penilaian jika diminta dosen.

Contoh URL repository:

```text
https://github.com/USERNAME-ANDA/tugas1-abd-2026
```

---

## Menjalankan Project

```bash
docker build -t tugas1-bigdata .
docker run --rm -p 8888:8888 -v "$(pwd)":/home/jovyan/work tugas1-bigdata
```

Buka JupyterLab pada `http://localhost:8888/lab`. Konfigurasi Dockerfile menjalankan JupyterLab tanpa password atau token untuk penggunaan lokal. Jangan gunakan konfigurasi ini pada server atau jaringan publik. Letakkan dataset pada `data/raw/`, lalu sesuaikan `DATA_PATH` di notebook profiling.

## Aturan Teknis

- Gunakan Polars untuk manipulasi data dan DuckDB untuk analitik SQL.
- Dataset harus minimal 500 MB atau lebih dari 1 juta baris.
- Jangan commit file data besar; simpan instruksi unduhan dan sumber data pada `data/README.md`.
- Gunakan commit bertahap dan pesan yang jelas, misalnya `feat: add initial dataset profiling`.

## Integritas Akademik dan Penggunaan AI

- Dilarang menyalin kode, laporan, atau visualisasi mahasiswa lain maupun repository publik tanpa sitasi dan atribusi yang jelas.
- Dilarang menggunakan jasa joki atau menyerahkan pekerjaan yang tidak dapat dijelaskan sendiri.
- AI boleh digunakan untuk belajar, mencari rujukan, menjelaskan konsep, atau debugging. AI tidak menggantikan tanggung jawab mahasiswa atas kebenaran dan kualitas solusi.
- Mahasiswa wajib dapat menjelaskan setiap bagian kode, menjalankan serta memverifikasi ulang hasilnya, dan memastikan penggunaan Polars serta DuckDB sesuai standar kuliah.
- Setiap penggunaan AI harus dicantumkan pada bagian AI Disclosure Statement di bawah.
- Pelanggaran pertama bernilai 0 untuk tugas terkait; pelanggaran berikutnya dapat berakibat nilai E untuk mata kuliah sesuai ketentuan akademik.

## AI Disclosure Statement

Isi bagian ini sebelum pengumpulan akhir.

> Alat AI yang digunakan: [nama alat].
>
> Bagian yang dibantu: [contoh: penjelasan error Polars atau review dokumentasi].
>
> Verifikasi yang dilakukan: [contoh: menjalankan ulang kode, memeriksa dokumentasi resmi, dan memahami setiap cell].
