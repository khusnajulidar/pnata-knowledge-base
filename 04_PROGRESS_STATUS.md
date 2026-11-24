# 04 — Progress Status Snapshot

**Snapshot:** 24 November 2026. Ini status dokumenter, bukan hasil QA langsung.

| Proyek | Status | Berikutnya |
|---|---|---|
| Adab Makan | Prototipe/fondasi + aset; belum terbukti production-ready | Audit commit terakhir, integrasi 25 aktivitas/audio, QA, verifikasi agama, deployment |
| Cinta Rasul | Konsep + audit bank 126 butir; TTS Pilot 02 tersedia | Final review sumber/proofreading, uji pilot, produksi layar/HTML |
| Hijaiyah | Banyak versi HTML; audio 29 huruf FINAL | Tentukan build authoritative, bandingkan branch, uji browser/responsif/audio |
| Activity Book Salat | H1–2 approved; H3 review; H4 concept approved; H5–10 belum final | Migrasi/verifikasi gambar H1–4, revisi H4, review H3, lanjut H5 |

## Adab Makan
Sudah terdokumentasi: GDD, 5 misi/25 aktivitas, pedoman ilustrasi, UI spec, 11 mockup, fondasi UI/gameplay, file HTML/CSS/JS, audio narasi 01–25 dan feedback.
Belum dinyatakan selesai di README: verifikasi materi/lafaz/audio/terjemahan, penyempurnaan mekanik dan integrasi mockup, integrasi audio, pengujian, deployment Netlify.
Commit berikutnya mengindikasikan integrasi sebagian mockup (aktivitas 1,3,4,5) dan refinements peta/bintang/Arab; belum membuktikan 25 aktivitas lengkap.

## Cinta Rasul
Konsep, 3 wilayah, 3 mode, 9 tantangan + bonus. Audit 20 Nov menyebut 126 butir (39 TTS, 48 word search, 39 matching) telah diaudit; ini bukan pengesahan visual/HTML. Bonus v1.0 menunggu proofreading/uji baca. TTS Pilot 02 tersedia; QA browser/responsif perlu bukti.

## Hijaiyah
Tree menunjukkan banyak HTML versi bertahap dan audio 29 huruf. Catatan 11 Nov menyebut perbaikan responsive landscape, touch, stop audio, indeks jawaban, win screen 10 soal, syntax check JS dan hash audio. Belum ada bukti uji browser/perangkat nyata, audio deployment, ZIP extraction, persetujuan visual, atau file authoritative. Branch fitur Misi 4 harus dibandingkan dengan main.

## Activity Book Salat
H1 sampul approved; H2 5 waktu salat approved; H3 perlu pemeriksaan akhir; H4 konsep approved dan arsip perlu revisi; H5–10 belum final. Prioritas: migrasi dan cek gambar H1–4, revisi H4, final review H3, lanjut H5+. Source repo tetap dipertahankan sampai migrasi selesai.

## Aturan membaca status
- “Disetujui” berarti konsep/keputusan disetujui, bukan otomatis aset final.
- “Ada di repo” tidak membuktikan file berfungsi.
- Nama file “FINAL” tidak membuktikan seluruh produk final.
- QA hanya boleh disebut selesai jika ada bukti uji.
