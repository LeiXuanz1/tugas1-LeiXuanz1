# Data Tugas 1

## Dataset yang Dipilih

Isi informasi berikut sebelum Milestone 1.

| Item | Isi |
|---|---|
| Nama dataset | SIAGA Pantura: Coupled Flood and Water Stress Dataset (`flood_dataset.parquet`) |
| Sumber | https://huggingface.co/datasets/ethanchrstian/siaga-pantura-hazard-data data dasar berasal dari GADM v4.1, ERA5 via Open-Meteo Archive API, GloFAS v4 via Open-Meteo Flood API, dan WorldPop 2020 |
| Lisensi/ketentuan pakai | MIT untuk kompilasi dataset. Sumber data ERA5 & GloFAS mengikuti lisensi Copernicus, GADM untuk penggunaan akademik/non-komersial, dan WorldPop CC BY 4.0. |
| Ukuran | `flood_dataset.parquet`: 1.152.432 baris, 17.1 MB |
| Periode data | 30 Januari 2015 – 31 Desember 2024 |
| Unit analisis | Kecamatan (district) per hari, 318 kecamatan di 18 kabupaten/kota di Pantai Utara Jawa (Pantura) |

## Catatan
- `flood_label` dihitung dari debit yang melewati persentil ke-95 tiap kecamatan, bukan dari catatan bencana. Laju label positif keseluruhan ~7.3%.

## Tempat Mencari Dataset

Pilih dataset Indonesia yang legal digunakan, dapat didokumentasikan sumbernya, dan memenuhi batas ukuran tugas.

| Situs | Kegunaan |
|---|---|
| [Satu Data Indonesia](https://data.go.id/) | Portal data terbuka lintas instansi pemerintah Indonesia. |
| [Badan Pusat Statistik](https://www.bps.go.id/) | Statistik sosial, ekonomi, kependudukan, dan data wilayah. |
| [BMKG Data Online](https://dataonline.bmkg.go.id/) | Data cuaca, iklim, gempa bumi, dan observasi meteorologi. |
| [Hugging Face Datasets](https://huggingface.co/datasets) | Dataset publik yang dapat dicari berdasarkan topik, bahasa, atau ukuran. |
| [Kaggle Datasets](https://www.kaggle.com/datasets) | Katalog dataset publik; periksa lisensi dan dokumentasi pembuatnya. |
| [Google Dataset Search](https://datasetsearch.research.google.com/) | Mesin pencari untuk menemukan dataset dari berbagai portal. |

## Cara Memperoleh Data

1. Buka URL sumber di atas.
2. Unduh file ke folder `data/raw/` tanpa mengubah data mentah.
3. Catat nama file dan checksum bila tersedia.
4. Ubah variabel `DATA_PATH` pada `notebooks/01_data_profiling.ipynb` agar menunjuk ke file tersebut.

## Aturan Penyimpanan

- Jangan commit dataset mentah atau hasil olahan berukuran besar ke Git.
- File pada `data/raw/` adalah data asli dan tidak boleh diubah.
- Simpan hasil transformasi yang dapat direproduksi pada `data/processed/`.
