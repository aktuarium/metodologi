# Skenario & Sensitivitas

_Uji dampak perubahan asumsi pada BEL, RA, dan CSM_

Layar: https://aktuarium.org/skenario/

## Asumsi dan aturan model

- S1. Setiap skenario menjalankan ulang seluruh model point dan pengukuran grup dengan asumsi yang digeser; tidak ada pendekatan linear.
- S2. Pengali mortalita, lapse, biaya, dan RA dikalikan pada asumsi dasar di setiap tahun polis, termasuk asumsi per tahun dan dari Pustaka Asumsi. Lapse dibatasi 100%.
- S3. Guncangan inflasi dan diskonto ditambahkan dalam basis poin pada tingkat tahunan di setiap tahun polis atau tenor; kurva penuh digeser pada spot efektif tahunan.
- S4. Guncangan biaya berlaku pada biaya pemeliharaan, biaya akuisisi, dan komponen biaya dari Pustaka Produk; komisi dan komponen manfaat mengikuti ketentuan kontrak dan tidak digeser.
- S5. Guncangan berlaku pada arus kas SESUDAH tanggal valuasi; riwayat dan pengelompokan tetap memakai asumsi dasar. Bisnis baru diukur pada pengakuan awal dengan asumsi skenario. Untuk model point in-force, perubahan FCF jasa masa depan pada kurva locked-in menyesuaikan CSM (par. 44) dan perubahan akibat diskonto masuk IFIE. Identitas per grup: Δ(CSM − LC) + FCF yang menyesuaikan CSM = 0.
- S6. Skenario dasar selalu dihitung tanpa guncangan dan menjadi pembanding semua selisih; model point, pengelompokan, dan metode sama dengan layar Valuasi Polis (M1–M10).
- S7. Tabel asumsi per segmen di-resolve lebih dulu per model point, baru guncangan skenario dikalikan atau ditambahkan pada hasilnya.
- S8. Grup PAA tidak memakai tabel mortalita, jadi pengali mortalita berlaku sebagai pengali RASIO KLAIM di grup itu. Pengali biaya, lapse, dan RA serta pergeseran inflasi dan diskonto berlaku seperti biasa; diskonto hanya menyentuh LIC karena LRC tidak didiskonto (par. 56). Grup PAA tidak punya CSM, jadi identitas CSM tidak berlaku dan yang wajib nol hanyalah tie-out-nya.
- S9. Kolom Imbal hasil (bp) menggeser imbal hasil underlying items dan hanya menyentuh grup VFA; di situlah imbal hasil dana menjadi penggerak utama pengukuran. Biaya yang DIPUNGUT dari dana tidak digeser pengali biaya karena ia syarat kontrak, bukan biaya entitas. Nilai dana pada tanggal valuasi adalah fakta dan tidak pernah digeser skenario. Arah dampaknya bergantung produk: dana yang lebih kecil menaikkan uang pertanggungan berisiko (COI naik) tetapi menurunkan biaya pengelolaan, jadi tanda perubahan CSM tidak selalu sama.
- P10. Skenario & sensitivitas memakai produk dan data polis yang sama dengan Valuasi Polis. Setiap skenario menghitung ulang seluruh polis dengan asumsi sesudah tanggal valuasi yang digeser; riwayat dan pengelompokan tetap memakai asumsi dasar. Paling banyak 10 skenario per perhitungan.

---
Teks ini sama dengan panel Penjelasan di aplikasi dan sheet Catatan pada berkas Excel yang diunduh.
