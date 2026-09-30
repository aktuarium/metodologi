# Discount Rate Lab

_Bentuk kurva diskonto current & locked-in dari data pasar_

Layar: https://aktuarium.org/discount/

## Asumsi dan aturan model

- D1. Kurva dinyatakan sebagai faktor diskonto bulanan v(t), t = 1..1440; spot dan forward diturunkan dari v(t).
- D2. Tingkat input dinormalkan ke efektif tahunan sesuai basis compounding.
- D3. Kurva tiga segmen: observable (tenor ≤ LLP) mengikuti titik pasar dengan interpolasi hanya di antara titik; LLP–UP diekstrapolasi menuju URFR; setelah UP gaya forward sama dengan ln(1 + URFR).
- D4. Titik bertenor lebih panjang dari LLP tidak dipakai dan dilaporkan. Sebelum tenor pertama spot dianggap datar; bila titik terakhir lebih pendek dari LLP, forward segmen terakhir diteruskan.
- D5. Ekstrapolasi menyambung pada v(LLP). Smith-Wilson difit pada titik observable, v(t) = v(LLP)·P(t)/P(LLP) ditambah koreksi forward a·(1 − (t − LLP)/(UP − LLP)) agar forward menyambung di LLP, dengan alfa terkecil yang membuat forward di UP dalam toleransi. Linear: gaya forward linear dari forward di LLP ke ln(1 + URFR) di UP. NSS: level dikunci ln(1 + URFR), parameter lain difit pada titik observable, ditambah koreksi linear agar forward menyambung di LLP dan tepat URFR di UP.
- D6. Bottom-up: IP ditambahkan pada spot tahunan kurva bebas risiko. IP observable manual atau hybrid, IP = r × (spread − (ECL + UCL)) dan tidak negatif; antara LLP dan UP IP FORWARD bergerak linear ke UIP dan sesudah UP sama dengan UIP; IP pada spot adalah rata-ratanya (∫ IP forward ÷ t), sehingga forward kurva tidak melompat di LLP maupun UP.
- D7. Top-down: yield portofolio acuan dikurangi penyesuaian risiko kredit (manual, atau ECL = (1 − (1 − CPD)^(1/t)) × LGD ditambah UCL = margin × ECL) di setiap titik, ditambah penyesuaian lain, lalu dibangun dengan tiga segmen D3.
- D8. Kurva current dan locked-in memakai parameter yang sama, termasuk satu alfa Smith-Wilson (yang lebih besar dari kalibrasi kedua kurva), sehingga selisihnya murni perbedaan tingkat.
- D9. Uji konvergensi membandingkan gaya forward kurva dasar di UP dengan ln(1 + URFR). Linear dan NSS memenuhinya dari konstruksi; Smith-Wilson dalam toleransi bila alfa dikalibrasi.
- D10. Uji segmen observable membandingkan spot kurva dasar di setiap tenor input dengan tingkat terpakai.
- D11. Kedalaman pasar: R_T = porsi outstanding bertenor lebih dari T; LLP yang disarankan adalah T tertinggi dengan R_T tidak kurang dari ambang materialitas.
- D12. Penyesuaian lain top-down lebih dari 50 bp ditandai, merujuk batas SEOJK 23/SEOJK.05/2024.

---
Teks ini sama dengan panel Penjelasan di aplikasi dan sheet Catatan pada berkas Excel yang diunduh.
