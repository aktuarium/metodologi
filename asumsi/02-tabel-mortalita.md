# Tabel Mortalita & Morbiditas

_Susun tabel qx atau frekuensi klaim dari acuan/pengalaman_

Layar: https://aktuarium.org/lifetable/

## Asumsi dan aturan model

- L1. Mortalita: qx = peluang meninggal dalam setahun, qω = 1 sehingga kohort habis di ω. Morbiditas: frekuensi klaim tahunan per tertanggung, boleh melebihi 1.
- L2. Usia kosong pada tabel acuan diisi interpolasi geometrik; di luar usia pertama/terakhir nilai terdekat diteruskan.
- L3. Penyesuaian acuan: tingkat(x) = persentase × acuan(x + pergeseran usia). Tingkat mortalita dibatasi paling tinggi 1.
- L4. Tingkat kasar = klaim aktual ÷ eksposur per usia; baris berusia sama dijumlahkan. Rentang data = usia pertama sampai terakhir yang berekposur.
- L5. Graduasi Whittaker-Henderson: minimum Σ w(v − u)² + h Σ(Δᶻv)², w = eksposur ÷ rata-rata. Hasilnya menjaga Σ E·v = Σ klaim aktual (dan usia rata-rata klaim bila z ≥ 2).
- L6. Di luar rentang data: tingkat = acuan × A/E, A/E = Σ klaim ÷ Σ eksposur × acuan di rentang data.
- L7. Uji kecocokan χ² = Σ z², z = (A − E·v) ÷ √Var (binomial untuk mortalita, Poisson untuk morbiditas), dibandingkan nilai kritis 95% pada derajat kebebasan banyak usia berdata − tr(H).
- L8. Penutupan Gompertz: ln μ = a + b·x dari kuadrat terkecil pada rentang estimasi; μ = −ln(1 − q) untuk mortalita. Tidak diterapkan bila b ≤ 0 atau titik kurang dari tiga.
- L9. Radix di usia awal tabel; Lx = lx − dx/2 (UDD), sehingga e̊x = ex + ½ persis.
- L10. Komutasi Dx = lx vˣ, Nx = Σ Dy, Cx = dx v^(x+1), Mx = Σ Cy, Rx = Σ My pada bunga teknis.
- L11. Tabel mortalita diterbitkan ke Pustaka Asumsi sebagai tabel qx; tabel morbiditas sebagai tabel frekuensi per usia untuk semua jenis kelamin.
- L12. Premi dan cadangan dihitung di layar pengukuran (GMA, PAA Generator, VFA, dan Valuasi Polis) yang memakai tabel ini lewat Pustaka Asumsi.
- L13. Dasar tabel morbiditas: usia tertanggung (kesehatan, kecelakaan diri) atau umur objek (kendaraan; bertambah satu setiap tahun polis). Jenis kelamin hanya untuk usia tertanggung. Properti tidak memakai tabel ini: frekuensi per kelas disimpan di Pustaka Produk.
- L14. Tabel usia tertanggung dibentuk untuk laki-laki dan perempuan dengan langkah yang sama, masing-masing dari kolomnya sendiri (sheet _L dan _P; nama sel perempuan berakhiran P). Kolom perempuan yang kosong berarti tabel unisex untuk kedua jenis kelamin. Layar pengukuran memakai kolom sesuai jenis kelamin kontrak atau polis.

---
Teks ini sama dengan panel Penjelasan di aplikasi dan sheet Catatan pada berkas Excel yang diunduh.
