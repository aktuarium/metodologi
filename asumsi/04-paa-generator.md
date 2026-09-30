# PAA Generator

_Ukur kontrak jangka pendek: LRC, LIC, uji kelayakan PAA_

Layar: https://aktuarium.org/paa-generator/

## Asumsi dan aturan model

- G1. Basis bulanan. Satu grup kontrak diterbitkan pada t = 0; proyeksi berlanjut setelah coverage berakhir sampai klaim terakhir dibayar.
- G2. Premi, komisi, dan biaya terjadi di AWAL bulan; polis yang lapse berhenti membayar. Klaim terjadi dan dibayar di AKHIR bulan.
- G3. Pendapatan = premi yang diharapkan dialokasikan menurut pola pengakuan (par. B126): berlalunya waktu atau polis in-force.
- G4. Klaim terjadi = rasio klaim × premi portofolio × porsi pengakuan bulan itu. Biaya penanganan klaim adalah persentase klaim dan diselesaikan bersama klaimnya.
- G5. Klaim terjadi dibayar menurut pola pembayaran: porsi per bulan keterlambatan, dinormalkan menjadi 100%.
- G6. LIC = PV arus kas klaim yang belum dibayar + RA LIC (% dari PV). Tanpa diskonto faktornya 1 (par. 59(b)); dengan diskonto, bunga atas LIC awal bulan menjadi beban keuangan asuransi.
- G7. Biaya akuisisi dibayar pada t = 1: dibebankan langsung atau ditangguhkan dan diamortisasi sebanding pola pengakuan (par. 59(a)).
- G8. LRC tidak didiskonto (par. 56). Uji onerous (par. 57-58): arus kas pemenuhan sisa coverage (klaim × (1 + RA LRC) + pemeliharaan − premi mendatang) dibanding LRC dasar; kelebihannya adalah loss component sebagai level dan perubahannya masuk beban.
- G9. Liabilitas sebelum pengakuan awal nol, jadi loss component pada pengakuan awal diakui sebagai beban periode 1.
- G10. Klaim aktual periode 1 menggantikan klaim terjadi yang diharapkan pada bulan-bulan periode 1 secara proporsional dan ikut diselesaikan menurut pola pembayaran.
- G11. Basis klaim mortalita (asuransi jiwa berjangka): klaim terjadi = polis meninggal × UP. qx bulanan = 1 − (1 − qx tahunan)^(1/12) pada usia masuk + tahun coverage − 1; kematian mengurangi polis in-force sebelum lapse. Workbook PAA PAI memakai qx tahunan setiap bulan, sehingga klaimnya sekitar dua belas kali lipat.
- G12. Komisi = persentase premi, dibayar bersama premi; bersama biaya akuisisi per polis ia adalah arus kas akuisisi. Biaya yang tidak dapat diatribusikan tidak masuk LRC maupun uji onerous dan disajikan sebagai beban lain.
- G13. Kas menerima premi serta membayar komisi dan biaya di awal bulan, memperoleh bunga pada tingkat investasi atas saldo positif itu, lalu membayar klaim di akhir bulan. Pendapatan investasi disajikan terpisah dari beban keuangan asuransi. Cek neraca: kas = liabilitas + laba ditahan.
- E1. Uji kelayakan par. 53(b) hanya dijalankan bila diminta dan tidak mengubah pengukuran PAA.
- E2. Pembanding memakai arus kas yang sama, diukur dengan pendekatan umum: klaim dinilai pada PV saat terjadi memakai pola pembayaran, ditambah pemeliharaan dan arus kas akuisisi. Premi di awal bulan, arus keluar di akhir bulan.
- E3. Kurva pembanding adalah tingkat diskonto layar walau LIC tidak didiskonto; perbedaan diskonto itulah salah satu yang diuji.
- E4. RA pembanding = RA LRC × PV arus keluar sisa. CSM par. 38 = maks(0, −(BEL + RA)), diakresi pada kurva dan dilepas sebanding pola pengakuan yang sama.
- E5. Masa pertanggungan ≤ 12 bulan lolos otomatis (par. 53(a)). Bulan dengan LRC pembanding di bawah lantai materialitas dikecualikan; selisih terhadap puncak dan terhadap LRC keduanya dihitung.

---
Teks ini sama dengan panel Penjelasan di aplikasi dan sheet Catatan pada berkas Excel yang diunduh.
