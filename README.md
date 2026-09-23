# Pertemuan 04 Seleksi Multi-Kondisi dan Validasi Input
Nama: Siti Nurhasanah
NIM: 2225250073
Kelas: 3B

## Tujuan
Membangun program validasi dan klasifikasi dengan rantai if-elif-else.

## Cara Menjalankan

### Latihan
python3 latihan/01_predikat_nilai.py
python3 latihan/02_kategori_bilangan.py
python3 latihan/03_jenis_sudut.py
python3 latihan/04_tuntas_soal.py
python3 latihan/05_jenis_segitiga_sudut.py

### Praktik
python3 praktik/validasi_klasifikasi_nilai.py

## Tabel Keputusan
- Penolakan tipe: input bukan angka
- Penolakan rentang ujian: ujian < 0 atau > 100
- Penolakan rentang tugas: tugas < 0 atau > 100
- Penolakan rentang kehadiran: hadir < 0 atau > 100
- Tidak memenuhi syarat kehadiran: hadir < 80
- Predikat A: nilai akhir ≥ 85
- Predikat B: 70 ≤ nilai akhir < 85
- Predikat C: 60 ≤ nilai akhir < 70
- Predikat D: 50 ≤ nilai akhir < 60
- Predikat E: nilai akhir < 50

## Hasil Pengujian
- Input: 90, 80, 85 → Nilai akhir = 86.00, Predikat A, Lulus
- Input: 75, 70, 90 → Nilai akhir = 73.00, Predikat B, Lulus
- Input: 65, 60, 90 → Nilai akhir = 63.00, Predikat C, Lulus
- Input: 55, 50, 90 → Nilai akhir = 53.00, Predikat D, Belum lulus
- Input: 40, 45, 90 → Nilai akhir = 42.00, Predikat E, Belum lulus
- Input: 80, 70, 70 → Tidak memenuhi syarat kehadiran
- Input: "abc", 70, 90 → Masukan ditolak: tipe
- Input: 120, 70, 90 → Masukan ditolak: ujian di luar rentang

## Refleksi
Awalnya masukan kehadiran di luar rentang (misalnya 150) terlewat.
Perbaikan dilakukan dengan rantai elif untuk validasi kehadiran.
