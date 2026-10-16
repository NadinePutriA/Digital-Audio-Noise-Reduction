# Digital-Audio-Noise-Reduction
Analisis dan implementasi filter digital FIR (Hamming dan Blackman) serta IIR (Butterworth dan Chebyshev) untuk mengurangi noise pada sinyal audio menggunakan Python.


**Analisis dan Implementasi Filter Digital FIR dan IIR untuk Noise Reduction pada Sinyal Audio**

Proyek Pengolahan Sinyal Digital yang membahas penerapan dan perbandingan filter digital FIR (Finite Impulse Response) dan IIR (Infinite Impulse Response) untuk mengurangi noise pada sinyal audio menggunakan Python.

**Deskripsi Proyek**

Sinyal audio dapat mengandung noise yang memengaruhi kualitas suara. Salah satu cara untuk mengurangi noise tersebut adalah dengan menerapkan filter digital yang dirancang untuk melewatkan atau meredam komponen frekuensi tertentu.

Pada proyek ini, dilakukan implementasi beberapa metode filter digital, yaitu FIR dengan window Hamming dan Blackman serta IIR dengan metode Butterworth dan Chebyshev. Setiap metode diuji menggunakan filter low-pass dan band-pass untuk mengamati perubahan sinyal audio sebelum dan sesudah proses filtering.

Hasilnya dianalisis melalui visualisasi sinyal pada domain waktu, analisis Fast Fourier Transform (FFT), respons frekuensi, serta pengukuran beberapa parameter sinyal.

**Tujuan**

- Merancang dan mengimplementasikan filter FIR menggunakan window Hamming dan Blackman.
- Merancang dan mengimplementasikan filter IIR menggunakan metode Butterworth dan Chebyshev.
- Membandingkan karakteristik filter melalui respons magnitude dan fase.
- Menganalisis perubahan sinyal audio sebelum dan sesudah filtering.
- Mengevaluasi hasil filtering menggunakan SNR, RMS, spectral centroid, dan FFT.
- Membandingkan kualitas hasil audio melalui analisis numerik dan pendengaran.

**Metode yang Digunakan**

1. Filter FIR
Filter FIR diimplementasikan menggunakan metode windowing dengan dua jenis window:
- Hamming Window: digunakan dalam perancangan filter FIR untuk membentuk respons frekuensi sesuai kebutuhan.
- Blackman Window: digunakan sebagai alternatif window untuk dibandingkan dengan Hamming.

2. Filter IIR
- Filter IIR diimplementasikan menggunakan dua metode:
- Butterworth: digunakan untuk merancang filter dengan respons frekuensi yang relatif halus pada passband.
- Chebyshev Type I: digunakan sebagai pembanding dengan karakteristik ripple pada passband.

3. Jenis Filter
Setiap metode diterapkan pada dua jenis filter:
- Low-pass filter: melewatkan frekuensi di bawah frekuensi cutoff dan meredam frekuensi yang lebih tinggi.
- Band-pass filter: melewatkan rentang frekuensi tertentu dan meredam frekuensi di luar rentang tersebut.

**Tahapan Pengerjaan**

1. Memuat Sinyal Audio
Membaca file audio dan mengambil informasi sampling rate. Jika audio memiliki dua kanal, sinyal dikonversi menjadi mono.
2. Analisis Frekuensi Dominan
Menggunakan FFT untuk mengidentifikasi frekuensi dominan pada sinyal audio.
3. Penambahan Noise
Menambahkan noise acak pada sinyal audio untuk membentuk sinyal yang akan diuji dalam proses filtering.
4. Penentuan Parameter Filter
Menentukan frekuensi cutoff untuk low-pass serta rentang frekuensi untuk band-pass.
5. Perancangan Filter FIR dan IIR
Membuat filter FIR dengan window Hamming dan Blackman serta filter IIR dengan metode Butterworth dan Chebyshev Type I.
6. Proses Filtering
Menerapkan filter pada sinyal audio yang telah diberi noise.
7. Penyimpanan Hasil Audio
Menyimpan hasil filtering dari setiap metode ke dalam file audio terpisah.
8. Visualisasi dan Evaluasi
Membandingkan sinyal dalam domain waktu, spektrum FFT, respons frekuensi, serta nilai SNR, RMS, dan spectral centroid.

**Konteks Akademik**

Mata Kuliah: Pengolahan Sinyal Digital
Proyek: Kelompok 8

**Catatan**
Proyek ini disusun untuk keperluan pembelajaran dan eksperimen pengolahan sinyal digital. Hasil filtering dapat berbeda bergantung pada karakteristik audio, sampling rate, parameter filter, dan tingkat noise yang digunakan.
