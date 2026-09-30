# CSM Roll-Forward

_Telusuri pergerakan CSM per grup dan rekonsiliasinya_

Layar: https://aktuarium.org/csm/

## Asumsi dan aturan model

- C1. Satu baris grid = satu grup kontrak × satu periode pelaporan.
- C2. Akresi memakai tingkat locked-in TAHUNAN per baris, dikonversi ke panjang periode: (1 + locked-in)^(bulan per periode / 12) - 1.
- C3. Urutan pergerakan mengikuti par. 44-45: saldo awal, akresi, perubahan FCF jasa masa depan, lalu pelepasan berdasar coverage units.
- C4. Perubahan FCF bertanda POSITIF berarti arus kas pemenuhan naik, sehingga CSM turun.
- C5. Kelebihan perubahan FCF yang tidak terserap CSM menjadi kerugian dan menambah loss component (par. 48). CSM tidak pernah negatif.
- C6. Loss component dilepas sebanding coverage units, sama seperti CSM.
- C7. Tie-out membandingkan saldo akhir menurut penggerak dengan saldo akhir yang dilaporkan. Nilai bukan nol menunjukkan data yang ditempel belum konsisten dan perlu diperiksa.
- C8. Kolom LRC di luar LC memuat BEL + RA dari input periode ditambah komponen CSM dari grid, dikurangi loss component yang disajikan terpisah. BEL dan RA sendiri diukur di layar GMA atau PAA, bukan di sini.
- C9. Rekonsiliasi mencakup rentang periode: saldo awal dari periode pertama, saldo akhir dari periode terakhir, penggerak dijumlah. Klaim terjadi memindahkan LRC ke LIC; bagian yang dialokasikan ke loss component mengurangi LC dan sisanya mengurangi LRC di luar LC. Pelepasan RA jasa kini mengurangi LRC di luar LC.
- C10. Grid dapat diisi dari hasil Valuasi Polis: satu baris per grup GMA per bulan dengan tingkat locked-in, ΔFCF, dan coverage units persis seperti roll-forward mesin, sehingga rekonsiliasinya menutup tanpa selisih. Grup PAA (tanpa CSM) dan VFA tidak diisi.

---
Teks ini sama dengan panel Penjelasan di aplikasi dan sheet Catatan pada berkas Excel yang diunduh.
