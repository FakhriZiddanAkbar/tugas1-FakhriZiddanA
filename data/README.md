# Data Tugas 1

## Dataset yang Dipilih

| Item | Isi |
|---|---|
| Nama dataset | `ID_REG_Parsed - Indonesian Regulation Parsed Dataset` |
| Sumber | `https://huggingface.co/datasets/Azzindani/ID_REG_Parsed` |
| Lisensi/ketentuan pakai | `Apache License 2.0` |
| Ukuran | `±1.58 GB dan ±3.63 juta baris` |
| Periode data | `Tahun regulasi tersedia pada kolom Year; rentang aktual akan divalidasi melalui profiling` |
| Unit analisis | `Satu pasal, ayat, klausul, atau bagian regulasi Indonesia per baris` |

Dataset `ID_REG_Parsed` merupakan kumpulan hasil parsing dokumen regulasi
Indonesia. Sumber dataset terdiri dari lebih dari 250.000 dokumen regulasi
yang diekstraksi dari PDF menjadi unit pasal, klausul, atau bagian.

Dataset tersedia dalam format Parquet dan memiliki lebih dari 3 juta baris
dengan ukuran sekitar 1.58 GB sehingga memenuhi persyaratan Dataset Tugas 1.

Kolom utama dataset antara lain:

- `Regulation Name` : nama atau jenis regulasi
- `Regulation Number` : nomor regulasi
- `Year` : tahun regulasi
- `About` : topik regulasi
- `Chapter` : bab
- `Article` : pasal
- `Content` : isi regulasi

## Tempat Mencari Dataset

Pilih dataset Indonesia yang legal digunakan, dapat didokumentasikan sumbernya,
dan memenuhi batas ukuran tugas.

| Situs | Kegunaan |
|---|---|
| [Satu Data Indonesia](https://data.go.id/) | Portal data terbuka lintas instansi pemerintah Indonesia. |
| [Badan Pusat Statistik](https://www.bps.go.id/) | Statistik sosial, ekonomi, kependudukan, dan data wilayah. |
| [BMKG Data Online](https://dataonline.bmkg.go.id/) | Data cuaca, iklim, gempa bumi, dan observasi meteorologi. |
| [Hugging Face Datasets](https://huggingface.co/datasets) | Dataset publik berdasarkan topik, bahasa, atau ukuran. |
| [Kaggle Datasets](https://www.kaggle.com/datasets) | Katalog dataset publik. |
| [Google Dataset Search](https://datasetsearch.research.google.com/) | Mesin pencari dataset. |

Dataset yang digunakan dalam tugas ini diperoleh dari Hugging Face Datasets.

## Cara Memperoleh Data

1. Buka:
   `https://huggingface.co/datasets/Azzindani/ID_REG_Parsed`
2. Unduh file-file `.parquet`.
3. Simpan tanpa modifikasi pada:
   `data/raw/DataSet/`
4. Catat nama file dan checksum apabila tersedia.
5. Arahkan `DATA_PATH` pada `notebooks/01_data_profiling.ipynb`
   ke file Parquet tersebut.
6. Dataset diproses menggunakan Polars Lazy API.

## Aturan Penyimpanan

- Jangan commit dataset mentah atau hasil olahan berukuran besar ke Git.
- File pada `data/raw/` adalah data asli dan tidak boleh diubah.
- Dataset mentah disimpan pada `data/raw/DataSet/`.
- Hasil transformasi disimpan pada `data/processed/`.
