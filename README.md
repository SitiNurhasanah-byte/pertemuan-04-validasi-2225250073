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

## Hasil Pengujian Wajib

| Masukan (Ujian, Tugas, Kehadiran) | Nilai Akhir | Keluaran yang Diharapkan                                | Keluaran Aktual                                    | Status |
|-----------------------------------|-------------|---------------------------------------------------------|---------------------------------------------------|--------|
| 90, 80, 95                        | 86.00       | Predikat A, Lulus                                       | Predikat A, Lulus                                 | ✅ |
| 75, 70, 85                        | 73.00       | Predikat B, Lulus                                       | Predikat B, Lulus                                 | ✅ |
| 60, 60, 80                        | 60.00       | Predikat C, Lulus                                       | Predikat C, Lulus                                 | ✅ |
| 55, 50, 90                        | 53.00       | Predikat D, Belum lulus                                 | Predikat D, Belum lulus                           | ✅ |
| 40, 30, 100                       | 36.00       | Predikat E, Belum lulus                                 | Predikat E, Belum lulus                           | ✅ |
| 90, 90, 75                        | 90.00       | Nilai akhir tampil, status Tidak memenuhi syarat hadir  | Tidak memenuhi syarat kehadiran                   | ✅ |
| 105, 80, 90                       | -           | Pesan penolakan rentang nilai ujian                     | Masukan ditolak: nilai ujian di luar rentang 0–100 | ✅ |
| 80, -5, 90                        | -           | Pesan penolakan rentang nilai tugas                     | Masukan ditolak: nilai tugas di luar rentang 0–100 | ✅ |
| 80, 80, abc                       | -           | Pesan penolakan tipe                                    | Masukan ditolak: seluruh data harus berupa angka   | ✅ |

## Refleksi
Awalnya masukan kehadiran di luar rentang (misalnya 150) terlewat.
Perbaikan dilakukan dengan rantai elif untuk validasi kehadiran.
