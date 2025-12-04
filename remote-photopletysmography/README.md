# Remote Photoplethysmography (rPPG) - Non-Contact Vital Sign Monitoring

## 📌 Deskripsi Proyek
Detak jantungmu, dari kamera biasa.
Proyek ini akan mengubah cara kita melihat vital sign—secara harfiah.
Tanpa alat khusus. Tanpa kabel. Hanya kamera dan kecerdasan.

Sistem remote photoplethysmography (rPPG) mengembangkan teknologi yang memungkinkan pengukuran detak jantung dan laju napas hanya lewat video wajah, tanpa kontak fisik sama sekali. Dengan menggabungkan kekuatan computer vision dan signal processing, sistem ini mendeteksi area dahi dan menangkap perubahan mikro pada warna kulit, lalu mengubahnya menjadi data biometrik secara real-time.

Sistem ini juga memanfaatkan pergerakan bahu yang terekam di video untuk menghitung laju pernapasan. Dengan menganalisis pola naik-turun pada area bahu saat seseorang bernapas, sistem dapat memperkirakan ritme respirasi secara non-invasif, cukup dari kamera biasa.

Bayangkan memantau kondisi tubuh cukup lewat kamera laptop atau smartphone—tanpa ribet, tanpa sensor tempel. Teknologi ini punya potensi besar untuk diterapkan dalam telemedicine, pemantauan pasien jarak jauh, hingga kebutuhan personal seperti self-monitoring kesehatan harian. Lebih simpel, lebih nyaman, lebih masa depan.

---

## 💻 Instruksi Instalasi

Panduan ini menjelaskan langkah-langkah untuk menyiapkan dan menjalankan project Python secara lokal **tanpa perlu melakukan clone dari GitHub**. Pastikan kamu sudah memiliki folder project di komputer (hasil download, ekstrak zip, atau salinan dari flashdisk).

**Requirements:**
- Python 3.8 atau lebih baru
- Webcam/kamera untuk pengujian real-time

**Langkah Instalasi:**

1. Buka terminal atau command prompt untuk masuk ke direktori project yang akan dijalankan.
```bash
cd path/ke/folder-project
```

2. Buat dan aktifkan virtual environment:
```bash
python -m venv rppg-env
# Aktivasi di Windows
rppg-env\Scripts\activate
# Aktivasi di MacOS/Linux  
source rppg-env/bin/activate
```

3. Install library yang dibutuhkan program dari `requirements.txt`:
```bash
pip install -r requirements.txt
```

4. Jalankan program utama yaitu `main.py`:
```bash
python main.py
```

---


