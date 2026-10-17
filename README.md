# Digital-Audio-Noise-Reduction
Analisis dan implementasi filter digital FIR (Hamming dan Blackman) serta IIR (Butterworth dan Chebyshev) untuk mengurangi noise pada sinyal audio menggunakan Python.

# Analisis dan Implementasi Filter Digital untuk Noise Reduction pada Sinyal Audio

## Deskripsi Proyek

Repository ini berisi implementasi filter digital untuk mengurangi noise pada sinyal audio menggunakan metode Finite Impulse Response (FIR) dan Infinite Impulse Response (IIR). Proyek ini membandingkan filter FIR dengan window Hamming dan Blackman serta filter IIR Butterworth dan Chebyshev.

Proses pengolahan meliputi analisis frekuensi dominan, penambahan noise buatan, perancangan filter low-pass dan band-pass, filtering sinyal audio, serta evaluasi hasil menggunakan metrik Signal-to-Noise Ratio (SNR), Root Mean Square (RMS), dan spectral centroid. Analisis juga dilengkapi dengan visualisasi sinyal pada domain waktu, Fast Fourier Transform (FFT), serta respons frekuensi filter.

## Tujuan

- Merancang dan mengimplementasikan filter FIR menggunakan window Hamming dan Blackman.
- Merancang filter IIR menggunakan Butterworth dan Chebyshev.
- Membandingkan karakteristik filter low-pass dan band-pass.
- Menganalisis respons magnitudo dan fase dari masing-masing filter.
- Mengevaluasi perubahan kualitas sinyal melalui SNR, RMS, spectral centroid, FFT, dan visualisasi domain waktu.
- Membandingkan hasil filtering secara objektif dan melalui pendengaran audio.

## Metodologi

### 1. Memuat Sinyal Audio
Membaca file audio menggunakan Python, memeriksa sampling rate, dan mengubah sinyal stereo menjadi mono apabila diperlukan.

### 2. Analisis Frekuensi Dominan
Menggunakan Fast Fourier Transform (FFT) untuk mengidentifikasi frekuensi dominan pada sinyal audio sebagai dasar penentuan parameter filter.

### 3. Penambahan Noise
Menambahkan noise acak buatan ke sinyal audio untuk mensimulasikan kondisi sinyal yang terkontaminasi gangguan.

### 4. Perancangan Filter Digital

Dua jenis filter digunakan:

**FIR (Finite Impulse Response)**
- Hamming Window
- Blackman Window

**IIR (Infinite Impulse Response)**
- Butterworth
- Chebyshev Type I

Setiap metode diuji menggunakan konfigurasi low-pass dan band-pass.

### 5. Proses Filtering
Menerapkan filter pada sinyal audio yang telah diberi noise, kemudian menyimpan hasil pengolahan untuk dibandingkan dengan sinyal awal dan sinyal noisy.

### 6. Evaluasi dan Visualisasi
Evaluasi dilakukan menggunakan:
- **SNR:** mengukur perbandingan sinyal acuan dengan noise atau galat hasil filtering.
- **RMS:** mengukur besarnya amplitudo efektif sinyal.
- **Spectral centroid:** menggambarkan pusat distribusi energi spektrum frekuensi.
- **FFT:** membandingkan karakteristik spektrum sebelum dan sesudah filtering.
- **Respons frekuensi:** mengamati karakteristik magnitudo dan fase filter.
- **Audio playback:** mendengarkan hasil filtering untuk membandingkan kualitas suara secara subjektif.

## Hasil dan Pembahasan

Berdasarkan hasil eksekusi notebook, sinyal audio awal memiliki sampling rate sebesar 48.000 Hz dan frekuensi dominan sekitar 507,10 Hz. Noise acak kemudian ditambahkan sebelum proses filtering.

Hasil pengukuran SNR pada notebook adalah sebagai berikut:

| Metode | SNR (dB) |
|---|---:|
| Sinyal noisy | 3,93 |
| FIR Low-Pass (Hamming) | 6,68 |
| FIR Band-Pass (Hamming) | 3,34 |
| FIR Low-Pass (Blackman) | 6,66 |
| FIR Band-Pass (Blackman) | 4,25 |
| IIR Low-Pass (Butterworth) | 8,26 |
| IIR Band-Pass (Butterworth) | 2,47 |
| IIR Low-Pass (Chebyshev) | 8,39 |
| IIR Band-Pass (Chebyshev) | 2,27 |

Pada konfigurasi dan data uji tersebut, filter **IIR Low-Pass Chebyshev** menghasilkan SNR tertinggi sebesar 8,39 dB, diikuti IIR Low-Pass Butterworth sebesar 8,26 dB. Kedua hasil tersebut lebih tinggi daripada SNR sinyal noisy sebesar 3,93 dB.

Namun, hasil tersebut tidak berarti bahwa Chebyshev selalu menjadi filter terbaik untuk semua sinyal audio. Kualitas akhir tetap perlu mempertimbangkan karakteristik respons frekuensi, perubahan spektrum, dan hasil pendengaran audio.

## Konteks Akademik

Program Studi S1 Sains Data  
Fakultas Matematika dan Ilmu Pengetahuan Alam  
Universitas Negeri Surabaya
Mata Kuliah: Pengolahan Sinyal Digital
