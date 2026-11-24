# 02 — Project History

## 1. Yuk Belajar Adab Makan
[Repository](https://github.com/khusnajulidar/pnata-digital-projects/tree/main/adab-makan)

- Target 3–4 tahun; web responsif; HTML/CSS/JS; LocalStorage; hosting rencana Netlify.
- Lima misi, 25 aktivitas, maksimum 5 bintang:
  1. Sebelum Makan (1–5)
  2. Makan dengan Tangan Kanan (6–10)
  3. Menghargai Makanan (11–15)
  4. Adab Saat Makan dan Minum (16–20)
  5. Setelah Makan (21–25)
- Tidak ada timer, nyawa, hukuman, leaderboard, atau skor angka yang membebani. Anak boleh mencoba lagi. Replay tidak menggandakan/mengurangi bintang. Petunjuk tersedia; Audio Ulang untuk aktivitas audio.
- Materi: Bismillah, Alhamdulillah, doa setelah makan, tangan kanan, makanan terdekat, menghargai makanan, dll.
- “Ambil makanan terdekat” hanya dalam konteks makan bersama dari satu wadah, bukan makanan terpisah.
- 11 mockup visual tercatat disiapkan/disetujui; file HTML/CSS/JS dan audio narasi aktivitas 01–25 + feedback tersedia.
- README masih menandai verifikasi agama/lafaz/audio/terjemahan, penyempurnaan mekanik dan integrasi aset, integrasi audio, QA, deployment sebagai belum selesai pada snapshot. Commit kemudian mengindikasikan integrasi sebagian mockup; belum membuktikan semua 25 aktivitas selesai.

Dokumen: [GDD](https://github.com/khusnajulidar/pnata-digital-projects/blob/main/adab-makan/GDD.md), [UI spec](https://github.com/khusnajulidar/pnata-digital-projects/blob/main/adab-makan/UI-IMPLEMENTATION-SPEC.md), [Mockup map](https://github.com/khusnajulidar/pnata-digital-projects/blob/main/adab-makan/MOCKUP-ACTIVITY-MAP.md), [Islamic references](https://github.com/khusnajulidar/pnata-digital-projects/blob/main/adab-makan/REFERENSI-ISLAM.md), [Asset needs](https://github.com/khusnajulidar/pnata-digital-projects/blob/main/adab-makan/ASSET-ILLUSTRATION-NEEDS.md).

## 2. Petualangan Cinta Rasul
[Repository](https://github.com/khusnajulidar/pnata-digital-projects/tree/main/petualangan-cinta-rasul)

- Game HTML responsif untuk SD kelas 1–6; profil Adik (1–3) dan Kakak (4–6); bank soal tertanam, target offline/no external API.
- Tiga wilayah: Jejak Rasulullah ﷺ, Keluarga Rasulullah ﷺ, Taman Para Shahabat.
- Tiga mode tiap wilayah: TTS, Berburu Kata, Matching; 9 tantangan utama/9 bintang.
- Bonus Jejak Para Ulama (“Buka Peti Ilmu”) satu tantangan/bintang; total 10 bintang.
- Penjelasan edukatif muncul setelah setiap jawaban; salah dapat mencoba kembali; LocalStorage menyimpan profil/progres/bintang/pengaturan.
- Materi membedakan Qur'an, hadis, atsar, sirah/tarikh, biografi; hindari riwayat lemah/ambigu. Jangan menggambarkan Rasulullah ﷺ atau Shahabat. Bonus ulama memakai simbol ilmu/karya, bukan avatar/wajah/tubuh.
- Audit 20 Nov 2026 menyatakan 126 butir utama telah diaudit: 39 TTS, 48 word search, 39 matching. Itu bukan persetujuan produksi visual/HTML. Beberapa rujukan dan redaksi masih perlu final review.
- Bonus v1.0 menunggu proofreading/uji keterbacaan. README menyebut delapan ulama, tetapi daftar yang terlihat hanya tujuh nama; perlu verifikasi.
- TTS Pilot 02 HTML dan JSON pilot tersedia; QA browser/responsivitas harus dibuktikan.

Dokumen: [README](https://github.com/khusnajulidar/pnata-digital-projects/blob/main/petualangan-cinta-rasul/README.md), [Audit 126 butir](https://github.com/khusnajulidar/pnata-digital-projects/blob/main/petualangan-cinta-rasul/materi/audit-akhir-gabungan-tts-berburu-kata-matching-v1.0.md), [Audit register](https://github.com/khusnajulidar/pnata-digital-projects/blob/main/petualangan-cinta-rasul/materi/master-index-audit-register-v0.1.md).

## 3. Petualangan Huruf Hijaiyah
[Repository](https://github.com/khusnajulidar/pnata-digital-projects/tree/main/petualangan-huruf-hijaiyah)

- Game edukasi interaktif untuk anak 4–8 tahun.
- Banyak versi HTML bertahap, terutama Misi 3; ada catatan finalisasi visual dan commit tahap Misi 4.
- Paket audio seimbang FINAL memuat 29 audio nama huruf; pemetaan ada di DAFTAR_AUDIO.txt. Catatan menyarankan index.html bersama assets dan server lokal/static hosting untuk konsistensi audio.
- Catatan 11 Nov menyebut perbaikan landscape pendek, touch-action, stop audio saat layar/soal/huruf berubah, indikator jawaban berbasis indeks, layar Win setelah 10 soal. Ada syntax check JS dan pemeriksaan hash audio.
- Belum terbukti: build authoritative, semua misi selesai/merge, tes browser langsung, QA portrait/landscape/laptop, audio perangkat nyata, ZIP extraction, persetujuan visual.
- Jangan pilih file “final” hanya dari nama; telusuri commit/branch dan isi.

## 4. Yuk, Belajar Salat! Activity Book
[Source repo](https://github.com/khusnajulidar/pnata-belajar-salat) → [Destination](https://github.com/khusnajulidar/pnata-activity-book/tree/main/02-activity-book-salat)

- Worksheet/activity book 10 halaman; kelas 1–2 SD; produk digital direncanakan dijual melalui Lynk.
- H1 sampul dan H2 lima waktu salat disetujui. H3 persiapan salat pernah dibuat, perlu final review. H4 gerakan salat konsep disetujui, arsip/ilustrasi perlu revisi. H5–10 belum final.
- H2: salat fardu mukim: Subuh 2, Zuhur 4, Asar 4, Magrib 3, Isya 4 (17 total).
- H3: bersuci dari hadas, bersih dari najis, menutup aurat, masuk waktu, kiblat, niat dalam hati; jangan mengajarkan lafaz niat sebagai syarat.
- H4: tujuh tahap satu rakaat: berdiri/takbiratul ihram, berdiri membaca bacaan, rukuk, iktidal, sujud pertama, duduk antara dua sujud, sujud kedua. Ini bukan keseluruhan salat; tasyahud dibahas lebih rinci pada rencana H8.
- Prioritas: revisi H4 setelah arsip tersedia, lalu lanjut H5+. Jangan ubah halaman yang disetujui tanpa arahan.
- Destination hanya untuk Salat; Wudhu dikeluarkan dari scope. Source repo dipertahankan sampai migrasi aset diverifikasi. README destination menyebut dokumentasi teks sudah disalin, empat gambar H1–H4 belum dimigrasikan.

Dokumen: [Source guide](https://github.com/khusnajulidar/pnata-belajar-salat/blob/main/PROJECT_GUIDE.md), [Destination guide](https://github.com/khusnajulidar/pnata-activity-book/blob/main/PROJECT_GUIDE.md), [Destination changelog](https://github.com/khusnajulidar/pnata-activity-book/blob/main/CHANGELOG.md).
