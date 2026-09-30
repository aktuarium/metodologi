# VFA Generator

_Ukur unit-link & partisipasi: fee variabel dan CSM_

Layar: https://aktuarium.org/vfa/

## Asumsi dan aturan model

- V1. Basis waktu bulanan, t = 1..n. Premi tunggal diterima di awal bulan 1; arus kas lain di akhir bulan.
- V2. Dana per polis: biaya dipungut di awal bulan, sisanya berkembang sebulan penuh, dana(t) = (dana(t-1) - biaya(t)) × (1 + g). Biaya yang sudah dipungut pindah ke akun umum entitas dan tidak diberi imbal hasil.
- V3. Biaya dari dana: COI atas uang pertanggungan berisiko, biaya administrasi tetap per polis, dan biaya pengelolaan tahunan atas saldo setelah dua biaya pertama. Setiap biaya dibatasi saldo dana sehingga dana tidak pernah negatif.
- V4. COI = max(UP - dana, 0) × qx bulanan × loading. Manfaat meninggal = max(UP, dana).
- V5. Dekremen: mortalita lalu lapse atas yang selamat, di akhir bulan setelah dana berkembang. Penyerahan dan jatuh tempo membayar nilai dana penuh.
- V6. Arus kas dipecah dua: yang BERVARIASI mengikuti underlying (seluruh pembayaran senilai dana) dan yang TIDAK (manfaat meninggal di atas dana, biaya pemeliharaan, biaya akuisisi). Biaya yang dipungut dari dana bukan arus kas kontrak.
- V7. Arus kas bervariasi didiskonto pada imbal hasil underlying, yang tidak bervariasi pada tingkat diskonto (par. B74-B75). Identitas yang wajib nol: PV(pembayaran senilai dana) = dana awal - PV(biaya yang dipungut).
- V8. Bagian entitas atas nilai wajar underlying items diturunkan sebagai PV biaya yang masih akan dipungut, bukan diinput. Rasio implisitnya terhadap dana awal ditampilkan agar bisa diaudit.
- V9. RA hanya atas PV arus kas tidak bervariasi; pembayaran senilai dana tidak membawa risiko non-keuangan bagi entitas.
- V10. CSM tanpa akresi locked-in: saldo awal + perubahan bagian entitas di luar biaya yang dipungut (B104(b)(i)) - perubahan jaminan akibat underlying (B112) -/+ perubahan estimasi FCF tidak bervariasi (B104(b)(ii)) - pelepasan coverage units. Penyesuaian yang menguntungkan lebih dulu membalik loss component (par. 50(b)).
- V11. Pembayaran senilai dana adalah komponen investasi (par. 85): ikut arus kas neto dan pergerakan liabilitas, tetapi tidak masuk pendapatan maupun beban jasa asuransi.
- V12. Tiga kriteria B101 adalah asersi pengguna atas syarat kontrak. Bukti (b) = PV pembayaran senilai dana / dana awal; bukti (c) = porsi pembayaran senilai dana terhadap total pembayaran kepada pemegang polis. Asersi yang tidak didukung bukti ditandai.
- V13. Imbal hasil aktual periode 1 diterapkan sebagai penilaian ulang dana sekali di akhir periode 1, setelah pembayaran bulan itu. CSM pengakuan awal tidak memakai hindsight.
- V14. Biaya akuisisi dibayar di bulan 1 dan diamortisasi lurus sepanjang masa pertanggungan.
- V15. Asumsi per tahun polis boleh diambil dari tabel asumsi per segmen Pustaka Asumsi. Dimensi produk tidak dibatasi di layar ini karena kontraknya unit-link, sehingga baris yang membatasi produk tidak pernah cocok.

---
Teks ini sama dengan panel Penjelasan di aplikasi dan sheet Catatan pada berkas Excel yang diunduh.
