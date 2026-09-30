# Metodologi Aktuarium

Repositori ini memuat metodologi [Aktuarium](https://aktuarium.org), platform alat aktuaria yang gratis dan metodologinya terbuka untuk ditelaah. Isinya adalah asumsi dan aturan model setiap alat, serta contoh berkas Excel berformula yang dihasilkan aplikasi.

Saat ini tersedia alat pengukuran kontrak asuransi PSAK 117 (IFRS 17). Alat untuk PSAK 219 (imbalan kerja), PSAK 408 (asuransi syariah), serta alat lain menyusul.

## Isi

| Alat | Fungsi | Jumlah asumsi |
|---|---|---|
| [Discount Rate Lab](asumsi/01-discount-rate-lab.md) | Bentuk kurva diskonto current & locked-in dari data pasar | 12 |
| [Tabel Mortalita & Morbiditas](asumsi/02-tabel-mortalita.md) | Susun tabel qx atau frekuensi klaim dari acuan/pengalaman | 14 |
| [GMA Generator](asumsi/03-gma.md) | Ukur satu kontrak jangka panjang: BEL, RA, CSM, laporan | 17 |
| [PAA Generator](asumsi/04-paa-generator.md) | Ukur kontrak jangka pendek: LRC, LIC, uji kelayakan PAA | 18 |
| [VFA Generator](asumsi/05-vfa.md) | Ukur unit-link & partisipasi: fee variabel dan CSM | 15 |
| [Valuasi Polis](asumsi/06-valuasi-polis.md) | Hitung liabilitas seluruh polis dari data sistem polis | 11 |
| [Skenario & Sensitivitas](asumsi/07-skenario.md) | Uji dampak perubahan asumsi pada BEL, RA, dan CSM | 10 |
| [CSM Roll-Forward](asumsi/08-csm-roll-forward.md) | Telusuri pergerakan CSM per grup dan rekonsiliasinya | 10 |
| [Quick Tools](asumsi/09-quick-tools.md) | Hitung cepat nilai kini, konversi bunga, usia, CU, dan qx | 7 |

Folder [`contoh-excel/`](contoh-excel) berisi satu berkas Excel per alat, dibuat dengan nilai bawaan berlabel ILUSTRASI. Setiap angka di dalamnya adalah rumus yang dapat ditelusuri, dan sheet Ringkasan memuat pemeriksa (tie-out) yang wajib bernilai nol. `Aktuarium_DataPolis_GMA_ILUSTRASI.xlsx` adalah contoh data polis yang dapat langsung diunggah ke Valuasi Polis.

## Prinsip kerja

- Seluruh perhitungan dijalankan di browser pada perangkat pengguna. Tidak ada akun, basis data, atau layanan yang menerima data input.
- Setiap hasil dapat diunduh sebagai berkas Excel yang memuat rumus, bukan angka mati.
- Setiap perhitungan memuat tie-out yang wajib bernilai nol, dan setiap keluaran diuji dengan test otomatis serta perhitungan ulang independen.
- Asumsi yang tertulis di sini sama dengan panel Penjelasan di aplikasi dan sheet Catatan pada berkas Excel.

## Masukan

Temuan pada perhitungan, usulan penyempurnaan, dan diskusi metodologi dapat disampaikan melalui [Issues](https://github.com/aktuarium/metodologi/issues) atau [formulir Masukan](https://aktuarium.org/masukan/). Mohon tidak melampirkan data polis atau data perusahaan; contoh angka cukup memakai data ilustrasi.

Para aktuaris yang menelaah metodologi tercantum di [halaman Kontributor](https://aktuarium.org/kontributor/).

## Kode sumber

Kode aplikasi dikelola secara privat oleh pengembang. Yang dibuka di sini adalah metodologinya, sehingga setiap angka dapat ditelaah dan direproduksi di Excel.

## Lisensi dan batas tanggung jawab

Dokumentasi dan contoh berkas di repositori ini dilisensikan di bawah [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE). Anda boleh menyalin dan mengadaptasinya dengan menyebutkan sumber: *Aktuarium (aktuarium.org)*.

Aktuarium adalah alat bantu perhitungan. Hasilnya bergantung pada asumsi, data, dan pertimbangan yang dimasukkan pengguna, dan bukan merupakan opini aktuaria, nasihat profesional, atau pernyataan kepatuhan. Tanggung jawab atas penggunaan hasil berada pada pengguna.

---

Dikembangkan oleh Fadhil Muhammad Hafizd · [aktuarium.org](https://aktuarium.org) · [YouTube](https://www.youtube.com/@aktuarium_org)
