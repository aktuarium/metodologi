# GMA Generator

_Ukur satu kontrak jangka panjang: BEL, RA, CSM, laporan_

Layar: https://aktuarium.org/gma/

## Asumsi dan aturan model

- A1. Basis waktu bulanan, t = 1..n, dengan n = masa pertanggungan dalam bulan. Usia yang dipakai adalah usia masuk + tahun polis − 1.
- A2. Premi, komisi, dan seluruh biaya terjadi di AWAL bulan; manfaat meninggal, manfaat jatuh tempo, dan nilai tunai di AKHIR bulan. Roll-forward menjadi eksak: BEL(t) = (BEL(t−1) + premi(t) − arus keluar awal(t)) × (1 + i(t)) − arus keluar akhir(t).
- A3. Urutan dekremen dalam satu bulan: mortalita lebih dulu, lalu lapse atas yang selamat dari mortalita. qx bulanan = 1 − (1 − qx tahunan)^(1/12).
- A4. Lapse hanya terjadi pada akhir bulan jatuh tempo premi (bulan ke 12/k, 24/k, …; k = banyak pembayaran setahun) dengan tingkat per kejadian 1 − (1 − lapse tahunan)^(1/k). Premi tunggal memakai k = 1.
- A5. Premi per pembayaran = premi tahunan × faktor modal cara bayar; premi tahunan memakai faktor 1.
- A6. Biaya dinyatakan per polis per tahun dan dibayar 1/12 setiap bulan, dipisah menjadi dapat dan tidak dapat diatribusikan. Biaya yang tidak dapat diatribusikan tidak masuk arus kas pemenuhan (par. B65(l)) dan disajikan sebagai beban lain. Biaya akuisisi satu angka berlaku di tahun polis 1 saja.
- A7. Komisi tahun polis 1 dan biaya akuisisi yang dapat diatribusikan adalah arus kas akuisisi asuransi: dicatat sebagai aset saat dibayar, diakresi, lalu diamortisasi sebanding coverage units; amortisasinya masuk pendapatan DAN beban jasa asuransi.
- A8. Manfaat jatuh tempo dwiguna = persentase UP, dibayar pada akhir bulan ke-n kepada polis yang bertahan. Nilai tunai per polis mengikuti rumus nilai tunai dan dibayar kepada polis yang lapse.
- A9. Kurva locked-in sama dengan kurva pengakuan awal karena proyeksi dimulai saat penerbitan.
- A10. Risk adjustment metode PAD = BEL dengan asumsi bermargin (mortalita, lapse, biaya) − BEL terbaik. RA dan CSM diakresi pada tingkat bulan itu lalu dilepas sebanding coverage units. Loss component dialokasikan dengan porsi yang sama dan mengurangi pendapatan DAN beban (par. 51-52).
- A11. Coverage units = polis in-force pada akhir bulan.
- A12. Manfaat jatuh tempo dan nilai tunai adalah komponen investasi (par. 85): tetap masuk arus kas dan pergerakan liabilitas, tetapi tidak masuk pendapatan maupun beban jasa asuransi.
- A13. Aset yang menutup liabilitas diasumsikan menghasilkan tingkat diskonto yang sama, sehingga pendapatan investasi sama dengan beban keuangan asuransi dari akresi.
- A14. Komponen arus kas dari rumus (Pustaka Produk) dievaluasi per bulan sesudah dekremen dengan variabel bulan itu (polis awal bulan, meninggal, lapse, premi, dst.) dan dibayar di akhir bulan. Manfaat masuk klaim diharapkan, biaya masuk beban. Pembagian dengan nol bernilai 0. Di Excel tiap komponen adalah kolom berformula di sheet arus kas.
- A15. Asumsi per tahun polis boleh diambil dari tabel asumsi per segmen di Pustaka Asumsi: nilainya dicocokkan menurut produk, jenis kelamin, usia yang dicapai pada tahun polis itu, durasi, dan tahun terbit (tahun tanggal valuasi). Baris paling spesifik yang dipakai; tahun tanpa baris yang cocok memakai nilai satu angka dan ditandai peringatan.
- A16. Tanpa rumus manfaat meninggal, bentuk manfaat mengikuti jenis produk: berjangka, dwiguna, dwiguna pendidikan, dan seumur hidup membayar UP; berjangka UP menurun membayar UP × (1 − (t − 1)/n); anuitas tidak membayar manfaat meninggal, tetapi membayar UP/12 setiap akhir bulan kepada polis yang bertahan (UP = pembayaran anuitas per tahun). Manfaat jatuh tempo hanya untuk dwiguna dan dwiguna pendidikan.
- A17. Kurva diskonto yang diambil dari Pustaka Asumsi dipakai apa adanya. Pendekatan bottom-up atau top-down dan premi ilikuiditasnya sudah diterapkan di Discount Rate Lab, sehingga pilihan pendekatan dan premi ilikuiditas di layar ini tidak dipakai dan tidak ada premi ilikuiditas yang dihitung dua kali.

---
Teks ini sama dengan panel Penjelasan di aplikasi dan sheet Catatan pada berkas Excel yang diunduh.
