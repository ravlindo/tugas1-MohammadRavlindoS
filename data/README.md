# Data Tugas 1

## Dataset yang Dipilih

| Item | Isi |
|---|---|
| Nama dataset | `idn-news-az - Indonesian News Dataset` |
| Sumber | `https://huggingface.co/datasets/esteler-ai/idn-news-az` |
| Lisensi/ketentuan pakai | `Creative Commons Attribution 4.0 (CC BY 4.0)` |
| Ukuran | `±1.56 GB dan 1.149.789 baris` |
| Periode data | `Mayoritas Januari 2023 - Oktober 2023, dengan sebagian data lebih lama` |
| Unit analisis | `Satu artikel berita Indonesia per baris` |

Dataset `idn-news-az` merupakan kumpulan artikel berita dari berbagai
portal berita Indonesia.

Dataset tersedia dalam format Parquet dan terdiri dari lebih dari satu juta
baris sehingga memenuhi ketentuan ukuran Dataset Tugas 1.

Kolom utama yang tersedia pada dataset antara lain:

- `date` : tanggal publikasi artikel
- `link` : URL sumber artikel
- `title` : judul artikel
- `text` : isi artikel

## Tempat Mencari Dataset

Pilih dataset Indonesia yang legal digunakan, dapat didokumentasikan sumbernya,
dan memenuhi batas ukuran tugas.

| Situs | Kegunaan |
|---|---|
| [Satu Data Indonesia](https://data.go.id/) | Portal data terbuka lintas instansi pemerintah Indonesia. |
| [Badan Pusat Statistik](https://www.bps.go.id/) | Statistik sosial, ekonomi, kependudukan, dan data wilayah. |
| [BMKG Data Online](https://dataonline.bmkg.go.id/) | Data cuaca, iklim, gempa bumi, dan observasi meteorologi. |
| [Hugging Face Datasets](https://huggingface.co/datasets) | Dataset publik yang dapat dicari berdasarkan topik, bahasa, atau ukuran. |
| [Kaggle Datasets](https://www.kaggle.com/datasets) | Katalog dataset publik; periksa lisensi dan dokumentasi pembuatnya. |
| [Google Dataset Search](https://datasetsearch.research.google.com/) | Mesin pencari untuk menemukan dataset dari berbagai portal. |

Dataset yang digunakan pada tugas ini diperoleh dari
[Hugging Face Datasets](https://huggingface.co/datasets/esteler-ai/idn-news-az).

## Cara Memperoleh Data

1. Buka halaman dataset:
   `https://huggingface.co/datasets/esteler-ai/idn-news-az`
2. Unduh seluruh file dataset dengan format Parquet dari folder `data_files`.
3. Simpan file tanpa melakukan perubahan pada folder:

   `data/raw/idn-news-az/`

4. Catat nama file dan checksum apabila tersedia pada sumber dataset.
5. File pada `data/raw/` digunakan sebagai data mentah dan tidak dimodifikasi.
6. Pada `notebooks/01_data_profiling.ipynb`, arahkan lokasi dataset ke:

   `../data/raw/idn-news-az/*.parquet`

7. Dataset dibaca menggunakan Polars Lazy API dengan `scan_parquet()` agar
   pengolahan dataset besar lebih efisien.

## Aturan Penyimpanan

- Jangan commit dataset mentah atau hasil olahan berukuran besar ke Git.
- File pada `data/raw/` adalah data asli dan tidak boleh diubah.
- Dataset mentah disimpan pada `data/raw/idn-news-az/`.
- Simpan hasil transformasi yang dapat direproduksi pada `data/processed/`.
- Hanya dokumentasi, notebook, source code, dan konfigurasi proyek yang
  disimpan pada repository GitHub.