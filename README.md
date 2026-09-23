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

| Kondisi                          | Syarat                            | Output / Predikat |
|----------------------------------|-----------------------------------|-------------------|
| Input bukan angka                | tipe data tidak valid             | Ditolak           |
| Nilai ujian di luar rentang      | ujian < 0 atau ujian > 100        | Ditolak           |
| Nilai tugas di luar rentang      | tugas < 0 atau tugas > 100        | Ditolak           |
| Kehadiran di luar rentang        | hadir < 0 atau hadir > 100        | Ditolak           |
| Kehadiran tidak memenuhi syarat  | hadir < 80                        | Tidak lulus       |
| Nilai akhir ≥ 85                 | -                                 | A                 |
| 70 ≤ Nilai akhir < 85            | -                                 | B                 |
| 60 ≤ Nilai akhir < 70            | -                                 | C                 |
| 50 ≤ Nilai akhir < 60            | -                                 | D                 |
| Nilai akhir < 50                 | -                                 | E                 |

## Hasil Pengujian

| Masukan (ujian, tugas, hadir) | Keluaran yang Diharapkan                  | Keluaran Aktual                  | Status |
|-------------------------------|-------------------------------------------|----------------------------------|--------|
| 90, 80, 85                    | Nilai akhir = 86.00, Predikat A, Lulus    | Nilai akhir = 86.00, Predikat A, Lulus | ✅ |
| 75, 70, 90                    | Nilai akhir = 73.00, Predikat B, Lulus    | Nilai akhir = 73.00, Predikat B, Lulus | ✅ |
| 65, 60, 90                    | Nilai akhir = 63.00, Predikat C, Lulus    | Nilai akhir = 63.00, Predikat C, Lulus | ✅ |
| 55, 50, 90                    | Nilai akhir = 53.00, Predikat D, Belum lulus | Nilai akhir = 53.00, Predikat D, Belum lulus | ✅ |
| 40, 45, 90                    | Nilai akhir = 42.00, Predikat E, Belum lulus | Nilai akhir = 42.00, Predikat E, Belum lulus | ✅ |
| 80, 70, 70                    | Tidak memenuhi syarat kehadiran           | Tidak memenuhi syarat kehadiran  | ✅ |
| "abc", 70, 90                 | Masukan ditolak: tipe                     | Masukan ditolak: tipe            | ✅ |
| 120, 70, 90                   | Masukan ditolak: ujian di luar rentang    | Masukan ditolak: ujian di luar rentang | ✅ |

## Refleksi
Awalnya masukan kehadiran di luar rentang (misalnya 150) terlewat.
Perbaikan dilakukan dengan rantai elif untuk validasi kehadiran.
