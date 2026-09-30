# Valuasi Polis

_Hitung liabilitas seluruh polis dari data sistem polis_

Layar: https://aktuarium.org/valuasi-polis/

## Asumsi dan aturan model

- P1. Asumsi, metode, kurva, dan ketentuan produk diambil dari run sumber yang tersimpan, lewat pembaca isian yang sama dengan layar Generator-nya. Polis yang atributnya sama dengan kontrak di run sumber memberi angka yang sama.
- P2. Satu baris = satu polis. Usia masuk dihitung dari tanggal lahir pada tanggal terbit menurut aturan usia yang dipilih; bila tanggal lahir kosong, kolom usia masuk dipakai.
- P3. Sel yang dikosongkan memakai nilai run sumber: jenis kelamin, cara bayar, masa bayar, dan jumlah polis (1).
- P4. Polis yang terbit sesudah tanggal valuasi atau yang masa pertanggungannya sudah berakhir tidak diukur. Polis PAA tetap diukur selama klaimnya masih dalam masa penyelesaian.
- P5. Kolom penimpa — biaya pemeliharaan per polis, komisi, pengali mortalita, frekuensi dan severitas klaim — menggantikan asumsi run sumber untuk polis itu saja, termasuk vektor per tahunnya. Asumsi pasar dan perilaku (diskonto, lapse, inflasi, RA) tetap satu untuk seluruh polis.
- P6. Polis dikelompokkan menjadi grup kontrak PSAK 117 (par. 14–24) dan diukur per grup: arus kas anggota dijumlahkan pada garis waktu kalender grup, CSM in-force diturunkan retrospektif dari tanggal terbit (GMA, VFA), kecuali grup yang diberi saldo awal.
- P7. Nilai per polis (PV premi, PV arus kas keluar, BEL, RA) dijumlahkan menjadi nilai grup; PV linear terhadap polis, jadi jumlahnya eksak. CSM dan loss component hanya bermakna per grup; CSM mandiri per polis dihitung sampai 20.000 polis.
- P8. Di atas 20.000 polis berkas Excel memuat satu baris agregat per grup, dan nilai per polis tersedia di CSV per polis.
- P9. Beberapa produk dapat divaluasi bersama. Tiap produk memakai run sumbernya sendiri dan kode produknya menjadi awalan grup kontrak, sehingga grup dua produk tidak pernah digabung (par. 14). Total, subtotal per model, dan penyajian bulanan adalah jumlah seluruh produk.
- P10. Skenario & sensitivitas memakai produk dan data polis yang sama dengan Valuasi Polis. Setiap skenario menghitung ulang seluruh polis dengan asumsi sesudah tanggal valuasi yang digeser; riwayat dan pengelompokan tetap memakai asumsi dasar. Paling banyak 10 skenario per perhitungan.
- P11. Laporan keuangan portofolio merinci pendapatan (pelepasan CSM dan RA, klaim & biaya diharapkan, pemulihan arus kas akuisisi, alokasi premi PAA, alokasi loss component), beban, pendapatan investasi, IFIE, laba sebelum pajak, arus kas, serta LRC dan LIC. Semuanya dijumlahkan dari penyajian bulanan GMA, PAA, dan VFA; pos yang nol di setiap bulan disembunyikan. Pendapatan investasi grup VFA disajikan sebesar IFIE-nya karena underlying items menutupnya (V10).

---
Teks ini sama dengan panel Penjelasan di aplikasi dan sheet Catatan pada berkas Excel yang diunduh.
