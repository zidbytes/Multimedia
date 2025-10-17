# Multimedia

Repositori ini berisi materi dan tugas praktik mata kuliah Multimedia. Saat ini, konten utama ada pada folder Hands-on 3 berupa notebook Jupyter untuk pengolahan audio beserta data WAV.

## Struktur Repository

```
Multimedia/
├─ Hands-on 1/                # (Kosong untuk saat ini)
├─ Hand-on 2/                 # (Perhatikan penamaan: "Hand-on" tanpa 's', saat ini kosong)
├─ Hands-on 3/
│  ├─ Tugas_3.ipynb           # Notebook Jupyter (tugas/praktik audio)
│  ├─ 122140100_Tugas_3.pdf   # Laporan/penjelasan tugas
│  └─ Data/                   # Dataset audio WAV yang digunakan oleh notebook
│     ├─ audio_1.wav
│     ├─ audio_2.wav
│     ├─ audio_chipmunk_combined.wav
│     ├─ audio_chipmunk_processed_-16LUFS.wav
│     ├─ RayRay & Aazar - Back n Forth.wav
│     ├─ rayray_cut.wav
│     ├─ rayray_processed_for_remix.wav
│     ├─ remix_final_echo_on_song1.wav
│     ├─ Sam Smith - Stay With Me.wav
│     ├─ samsmith_cut.wav
│     └─ samsmith_processed_for_remix.wav
└─ README.md
```

Catatan: Folder "Hand-on 2" dan "Hands-on 1" saat ini kosong. Nama folder dibiarkan apa adanya untuk konsistensi dengan materi/pertemuan.

## Prasyarat

- Windows 10/11, PowerShell (repo ini menggunakan contoh perintah PowerShell)
- Python 3.10 atau lebih baru (disarankan)
- VS Code dengan ekstensi:
	- Python (ms-python.python)
	- Jupyter (ms-toolsai.jupyter)

Alternatif: Anda bisa menggunakan Anaconda/Miniconda bila lebih nyaman.

## Cara Menjalankan Kode (Notebook)

Anda bisa memilih salah satu cara berikut.

### Opsi A: Langsung di VS Code

1. Buka folder repositori ini di VS Code.
2. Pastikan ekstensi Python dan Jupyter sudah terpasang.
3. Buka notebook `Hands-on 3/Tugas_3.ipynb`.
4. Pilih interpreter/kernel Python yang diinginkan (pojok kanan atas notebook) dan jalankan sel satu per satu atau "Run All".

### Opsi B: Jupyter Notebook lewat Terminal (PowerShell)

1. Buat dan aktifkan virtual environment di root repo:

```powershell
python -m venv .venv
./.venv/Scripts/Activate.ps1
```

2. Pasang paket yang umum dibutuhkan untuk pengolahan audio pada notebook (sesuaikan bila notebook membutuhkan paket lain):

```powershell
pip install -U pip jupyter numpy matplotlib librosa soundfile pydub ipykernel
```

Opsional (agar kernel mudah dipilih di Jupyter/VS Code):

```powershell
python -m ipykernel install --user --name multimedia-venv --display-name "Python (multimedia-venv)"
```

3. Jalankan Jupyter Notebook dan buka `Hands-on 3/Tugas_3.ipynb`:

```powershell
jupyter notebook
```

## Akses Data

Notebook `Tugas_3.ipynb` mengandalkan file WAV di folder `Hands-on 3/Data`. Pastikan path relatif pada sel notebook tetap menunjuk ke lokasi ini. Jika Anda memindahkan notebook atau data, sesuaikan path-nya.

## Troubleshooting

- ImportError (modul tidak ditemukan):
	- Instal paket yang hilang, contoh: `pip install <nama-paket>`.
- Peringatan/galat terkait audio decoding (terutama saat menggunakan `pydub`):
	- Anda mungkin membutuhkan FFmpeg terpasang dan tersedia di PATH.
	- Cek dengan: `ffmpeg -version`.
	- Opsi instal cepat via Winget (jika tersedia):

		```powershell
		winget install --id Gyan.FFmpeg -e
		```

		Setelah instalasi, tutup terminal dan buka kembali agar PATH terbarui.

## Catatan Tambahan

- Jika Anda menggunakan Conda:

	```powershell
	conda create -n multimedia python=3.11 -y
	conda activate multimedia
	pip install -U jupyter numpy matplotlib librosa soundfile pydub ipykernel
	```

- Jika Anda menjalankan notebook dari folder berbeda, pastikan "Current Working Directory" mengarah ke root proyek atau perbarui path relatif pada sel yang membaca data.

---

Terakhir diperbarui: 17 Oktober 2025