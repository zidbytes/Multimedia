# Multimedia

Repositori ini berisi materi dan tugas praktik mata kuliah Multimedia, mencakup pengolahan gambar (Hands-on 2) dan pengolahan audio (Hands-on 3).

## Struktur Repository

```
Multimedia/
├─ Hands-on 1/                      # (Kosong untuk saat ini)
├─ Hands-on 2/                      # Praktik pengolahan audio, image, video
│  ├─ 122140100_Worksheet2.ipynb    
│  └─ data/                        
│     └─ [file-file pendukung]
├─ Hands-on 3/                      # Pengolahan audio
│  ├─ Tugas_3.ipynb                
│  ├─ 122140100_Tugas_3.pdf         
│  └─ Data/                         
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
3. Buka notebook yang diinginkan:
   - `Hands-on 2/122140100_Worksheet2.ipynb` untuk pengolahan audio, image, video
   - `Hands-on 3/Tugas_3.ipynb` untuk pengolahan audio
4. Pilih interpreter/kernel Python yang diinginkan (pojok kanan atas notebook) dan jalankan sel satu per satu atau "Run All".

### Opsi B: Jupyter Notebook lewat Terminal (PowerShell)

1. Buat dan aktifkan virtual environment di root repo:

```powershell
python -m venv .venv
./.venv/Scripts/Activate.ps1
```

2. Pasang paket yang dibutuhkan:

**Untuk Hands-on 2 (Image Processing):**
```powershell
pip install -U pip jupyter numpy matplotlib opencv-python pillow scikit-image ipykernel
```

**Untuk Hands-on 3 (Audio Processing):**
```powershell
pip install -U pip jupyter numpy matplotlib librosa soundfile pydub ipykernel
```

**Atau instal semua sekaligus:**
```powershell
pip install -U pip jupyter numpy matplotlib opencv-python pillow scikit-image librosa soundfile pydub ipykernel
```

Opsional (agar kernel mudah dipilih di Jupyter/VS Code):

```powershell
python -m ipykernel install --user --name multimedia-venv --display-name "Python (multimedia-venv)"
```

3. Jalankan Jupyter Notebook:

```powershell
jupyter notebook
```

Lalu buka notebook yang diinginkan dari browser.

## Akses Data

- **Hands-on 2**: Notebook `122140100_Worksheet2.ipynb` menggunakan gambar dari folder `Hands-on 2/data/`.
- **Hands-on 3**: Notebook `Tugas_3.ipynb` menggunakan file audio dari folder `Hands-on 3/Data/`.

Pastikan path relatif pada sel notebook tetap menunjuk ke lokasi data yang benar. Jika Anda memindahkan notebook atau data, sesuaikan path-nya.

## Troubleshooting

- **ImportError (modul tidak ditemukan)**:
    - Instal paket yang hilang, contoh: `pip install <nama-paket>`.

- **Peringatan/galat terkait audio decoding** (terutama saat menggunakan `pydub`):
    - Anda mungkin membutuhkan FFmpeg terpasang dan tersedia di PATH.
    - Cek dengan: `ffmpeg -version`.
    - Opsi instal cepat via Winget (jika tersedia):

        ```powershell
        winget install --id Gyan.FFmpeg -e
        ```

        Setelah instalasi, tutup terminal dan buka kembali agar PATH terbarui.

- **Error saat memuat gambar** (OpenCV/PIL):
    - Pastikan path file gambar benar dan file tidak corrupt.
    - Coba buka dengan image viewer lain untuk verifikasi.

## Catatan Tambahan

- Jika Anda menggunakan Conda:

    ```powershell
    conda create -n multimedia python=3.11 -y
    conda activate multimedia
    pip install -U jupyter numpy matplotlib opencv-python pillow scikit-image librosa soundfile pydub ipykernel
    ```

- Jika Anda menjalankan notebook dari folder berbeda, pastikan "Current Working Directory" mengarah ke root proyek atau perbarui path relatif pada sel yang membaca data.

---
