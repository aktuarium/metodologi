# Quick Tools

_Hitung cepat nilai kini, konversi bunga, usia, CU, dan qx_

Layar: https://aktuarium.org/quick/

## Asumsi dan aturan model

- Q1. PV & anuitas: periode bulanan, bunga input annual effective. Due = pembayaran di awal bulan, immediate = di akhir bulan.
- Q2. Konversi bunga lewat annual effective sebagai basis tengah.
- Q3. Usia aktuaria dihitung dari tanggal. Ulang tahun 29 Februari jatuh pada 28 Februari di tahun bukan kabisat. Nearest birthday membulatkan setengah tahun ke atas.
- Q4. Coverage units: linear = 1 unit per periode, terdiskonto = v(t) pada tingkat locked-in. CSM berakresi pada tingkat yang sama lalu dilepas sebanding CU periode terhadap CU sisa (par. B119).
- Q5. Interpolasi qx log-linear antar usia jangkar; di luar jangkar tidak diekstrapolasi.
- Q6. Interpolasi tingkat: linear pada spot, atau log-linear pada faktor diskonto (forward konstan antar dua titik). Di luar dua titik nilainya diekstrapolasi dan ditandai.
- Q7. Semua tingkat annual effective kecuali disebut lain.

---
Teks ini sama dengan panel Penjelasan di aplikasi dan sheet Catatan pada berkas Excel yang diunduh.
