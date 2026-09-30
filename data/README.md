# Dataset idn-news-az

## Informasi dataset

| Item | Keterangan |
|---|---|
| Nama | `idn-news-az - Indonesian News Dataset` |
| Sumber | [Hugging Face](https://huggingface.co/datasets/esteler-ai/idn-news-az) |
| Lisensi | Creative Commons Attribution 4.0 (CC BY 4.0) |
| Format | Parquet |
| Jumlah file | 441 |
| Jumlah baris | 1.149.789 artikel |
| Ukuran | 1.558.347.901 byte (sekitar 1,56 GB) |
| Unit analisis | Satu artikel berita Indonesia per baris |

Dataset memiliki empat kolom utama:

- `date`: tanggal publikasi;
- `link`: URL sumber artikel;
- `title`: judul artikel;
- `text`: isi artikel.

## Lokasi penyimpanan

Seluruh file data mentah disimpan tanpa modifikasi di:

```text
data/raw/idn-news-az/data_files/*.parquet
```

Folder tersebut sengaja diabaikan oleh Git. Cache dari proses pengunduhan tidak
diperlukan untuk menjalankan analisis dan tidak disimpan di dalam proyek.

## Cara memperoleh data

1. Buka repository dataset
   [`esteler-ai/idn-news-az`](https://huggingface.co/datasets/esteler-ai/idn-news-az/tree/main/data_files).
2. Unduh semua file `.parquet` dari folder `data_files`.
3. Simpan seluruh file ke `data/raw/idn-news-az/data_files/`.
4. Jangan mengubah file mentah. Hasil cleaning disimpan terpisah di
   `data/processed/`.

Notebook `notebooks/01_data_profiling.ipynb` membaca seluruh file menggunakan
`pl.scan_parquet()` agar pemrosesan memanfaatkan lazy evaluation dan tidak
memuat dataset sekaligus ke memori.

Dataset memenuhi ketentuan tugas karena ukurannya lebih dari 500 MB dan jumlah
barisnya lebih dari satu juta.
