# PRD — NutriGlow: Web App Kalkulator Gizi

| | |
|---|---|
| **Versi** | 1.0 (Draft) |
| **Tanggal** | 20 Oktober 2026 |
| **Status** | Draft untuk review |
| **Platform** | Web app (mobile-first, responsif hingga desktop), dapat di-install sebagai PWA |
| **Bahasa antarmuka** | Bahasa Indonesia (arsitektur siap multi-bahasa) |
| **Referensi desain** | `code.html` (mockup layar Jurnal) dan `DESIGN.md` (design system "Pastel Health & Nutrition") |

---

## 1. Ringkasan Produk

**NutriGlow** adalah web app untuk menghitung kebutuhan gizi harian dan mencatat asupan makanan dengan cepat. Pengguna memasukkan data tubuh dan tujuan, aplikasi menghitung target kalori serta makronutrien (karbohidrat, protein, lemak), lalu pengguna mencatat makanan per waktu makan dan melihat sisa kuota hariannya secara visual.

Pembeda utama: **pengalaman yang hangat dan tidak menghakimi**. Angka gizi disajikan dengan bahasa yang mendukung, warna pastel, dan interaksi yang terasa seperti perayaan kecil, bukan seperti alat klinis atau aplikasi diet yang menekan.

### 1.1 Visi
Membuat pencatatan gizi harian terasa ringan, akurat, dan menyenangkan, sehingga pengguna konsisten melakukannya.

### 1.2 Masalah yang Diselesaikan
- Banyak orang tidak tahu berapa kebutuhan kalori dan makro hariannya.
- Aplikasi pencatat kalori yang ada sering terasa rumit, kaku, dan membuat pengguna merasa bersalah.
- Basis data makanan global kurang mencakup makanan Indonesia (nasi padang, tempe, soto, jajanan pasar, dll.), sehingga pencatatan jadi lambat.
- Mencatat satu makanan terlalu banyak langkah, sehingga pengguna berhenti setelah beberapa hari.

---

## 2. Tujuan dan Metrik Keberhasilan

### 2.1 Tujuan Produk
1. Menghitung target kalori dan makro yang personal dalam kurang dari 2 menit saat onboarding.
2. Mencatat satu makanan dalam maksimal 3 ketukan untuk makanan yang sering dimakan.
3. Menampilkan progres harian yang langsung terbaca dalam sekali pandang.
4. Membangun kebiasaan: pengguna kembali mencatat secara rutin.

### 2.2 Metrik (target awal, perlu divalidasi)

| Metrik | Definisi | Target 3 bulan pertama |
|---|---|---|
| Aktivasi | % pengguna baru yang menyelesaikan onboarding dan mencatat ≥1 makanan di hari pertama | ≥ 60% |
| Retensi D7 | % pengguna aktif di hari ke-7 | ≥ 30% |
| Konsistensi | Rata-rata hari tercatat per minggu per pengguna aktif | ≥ 4 hari |
| Kecepatan log | Median waktu dari membuka form hingga tersimpan | ≤ 20 detik |
| Cakupan data | % pencarian makanan yang menemukan hasil relevan | ≥ 90% |
| Kepuasan | Skor kepuasan (CSAT) dalam aplikasi | ≥ 4,3 / 5 |

### 2.3 Non-Tujuan (di luar cakupan v1)
- Bukan alat diagnosis atau terapi medis, dan tidak menggantikan ahli gizi atau dokter.
- Tidak ada fitur sosial/komunitas, tantangan publik, atau papan peringkat.
- Tidak ada pelacakan vitamin dan mineral mikro lengkap (di luar serat, gula, natrium pada fase lanjutan).
- Tidak ada integrasi perangkat wearable di v1.
- Tidak ada marketplace atau belanja bahan makanan.

---

## 3. Target Pengguna

| Persona | Deskripsi | Kebutuhan utama |
|---|---|---|
| **Pemula peduli kesehatan** (utama) | 18–40 tahun, baru ingin mengatur pola makan, belum paham istilah makro | Penjelasan sederhana, target otomatis, tidak intimidatif |
| **Pelacak makro aktif** | Rutin olahraga atau punya target komposisi tubuh | Input cepat, akurasi porsi, statistik mingguan |
| **Ibu/pekerja sibuk** | Ingin menjaga pola makan keluarga atau diri sendiri di sela kesibukan | Log cepat, favorit, resep sehat |

Desain visual saat ini bernuansa feminin dan hangat. Cakupan persona sebaiknya diputuskan bersama tim (lihat Pertanyaan Terbuka).

---

## 4. Ruang Lingkup per Rilis

### 4.1 MVP (v1.0)
- Onboarding dan kalkulator kebutuhan harian (BMR, TDEE, target kalori, target makro)
- Jurnal makan harian per waktu makan (sarapan, makan siang, makan malam, camilan)
- Kalkulator Cepat (estimasi gizi per porsi sebelum dimakan)
- Basis data makanan (pencarian) + input manual
- Dashboard ringkasan: cincin kalori, 3 bar makro, serat, hidrasi
- Pencatatan air minum
- Navigasi tanggal (strip kalender mingguan)
- Profil dan pengaturan target
- Akun pengguna dan sinkronisasi data

### 4.2 v1.1
- Statistik: grafik harian, mingguan, bulanan
- Favorit dan makanan terbaru
- Duplikasi/salin makanan dari hari lain
- Notifikasi pengingat

### 4.3 v1.2 dan seterusnya
- Resep sehat (dengan hitung gizi otomatis per porsi)
- Pemindai barcode kemasan
- Foto makanan di jurnal
- Ekspor data (CSV/PDF)
- Target berat badan dan pelacakan berat

---

## 5. Peta Layar dan Navigasi

Navigasi bawah (bottom nav) dengan 4 tab, sesuai mockup:

| Tab | Ikon | Status desain | Cakupan |
|---|---|---|---|
| **Jurnal** | `lunch_dining` | Sudah didesain | MVP |
| **Statistik** | `insights` | Belum didesain | v1.1 |
| **Resep** | `local_dining` | Belum didesain | v1.2 |
| **Profil** | `person` | Belum didesain | MVP |

Layar tambahan yang perlu didesain: Onboarding, Login/Daftar, Pengaturan target, Detail makanan, Notifikasi, Pencarian makanan layar penuh.

---

## 6. Kebutuhan Fungsional

Prioritas: **P0** wajib MVP, **P1** penting, **P2** nice-to-have.

### 6.1 Onboarding dan Kalkulator Kebutuhan Harian

| ID | Kebutuhan | Prioritas |
|---|---|---|
| FR-1.1 | Pengguna mengisi: jenis kelamin, tanggal lahir/usia, tinggi (cm), berat (kg), tingkat aktivitas, dan tujuan (turun, jaga, naik berat badan). | P0 |
| FR-1.2 | Sistem menghitung BMR (Mifflin-St Jeor), TDEE, lalu target kalori sesuai tujuan. | P0 |
| FR-1.3 | Sistem menghitung target makro (gram) dari target kalori berdasarkan pembagian persen yang dapat disesuaikan. | P0 |
| FR-1.4 | Sistem menetapkan target default serat (±25 g) dan air (±2,5 L, dapat disesuaikan). | P0 |
| FR-1.5 | Pengguna dapat mengubah target secara manual kapan saja di Profil. | P0 |
| FR-1.6 | Sistem menampilkan penjelasan singkat cara perhitungan dan label bahwa hasil adalah estimasi. | P0 |
| FR-1.7 | Sistem membatasi target kalori pada batas aman minimum dan menampilkan peringatan lembut bila pengguna menetapkan target terlalu rendah. | P0 |
| FR-1.8 | Pengguna di bawah 18 tahun atau sedang hamil/menyusui diarahkan untuk berkonsultasi dengan tenaga kesehatan; target otomatis tidak ditampilkan sebagai rekomendasi tunggal. | P1 |

**Rumus acuan (v1):**

- BMR pria = 10 × berat(kg) + 6,25 × tinggi(cm) − 5 × usia + 5
- BMR wanita = 10 × berat(kg) + 6,25 × tinggi(cm) − 5 × usia − 161
- TDEE = BMR × faktor aktivitas (1,2 / 1,375 / 1,55 / 1,725 / 1,9)
- Target kalori = TDEE + penyesuaian tujuan (misal −10–20% untuk turun, +10% untuk naik)
- Konversi energi: karbohidrat 4 kkal/g, protein 4 kkal/g, lemak 9 kkal/g
- Contoh pembagian default pada mockup (1.850 kkal): karbo 220 g, protein 110 g, lemak 60 g (≈ 47% / 24% / 29%)

Rumus dan persentase pembagian perlu direview oleh ahli gizi sebelum rilis (lihat bagian Risiko).

### 6.2 Dashboard Ringkasan Nutrisi (kartu hero)

| ID | Kebutuhan | Prioritas |
|---|---|---|
| FR-2.1 | Menampilkan cincin progres kalori: terkonsumsi / target, persen terisi, dan badge "Tersisa X kkal". | P0 |
| FR-2.2 | Menampilkan 3 bar progres makro (Karbo, Protein, Lemak) dengan gram terkonsumsi / target dan persentase. | P0 |
| FR-2.3 | Menampilkan penghitung serat pangan dan hidrasi air. | P0 |
| FR-2.4 | Seluruh angka dihitung otomatis dari entri jurnal tanggal terpilih dan diperbarui seketika saat entri ditambah, diubah, atau dihapus. | P0 |
| FR-2.5 | Bila asupan melebihi target, tampilan berubah ke mode "surplus" dengan bahasa netral (tidak menyalahkan) dan warna yang tetap ramah. | P0 |
| FR-2.6 | Animasi pengisian cincin/bar saat nilai berubah, menghormati pengaturan "reduce motion". | P1 |

### 6.3 Navigasi Tanggal

| ID | Kebutuhan | Prioritas |
|---|---|---|
| FR-3.1 | Strip 7 hari (Sen–Min) dengan hari terpilih disorot; hari ini diberi penanda. | P0 |
| FR-3.2 | Geser/pilih hari lain untuk melihat dan mengedit jurnal tanggal tersebut (termasuk tanggal lampau). | P0 |
| FR-3.3 | Tombol "Hari Ini" mengembalikan ke tanggal hari ini; judul bulan dan tahun mengikuti tanggal terpilih. | P0 |
| FR-3.4 | Pemilih bulan/kalender penuh dari tombol dropdown. | P1 |
| FR-3.5 | Tanggal masa depan dapat dilihat (untuk perencanaan makan) namun diberi tanda bahwa itu rencana. | P2 |

### 6.4 Kalkulator Cepat

| ID | Kebutuhan | Prioritas |
|---|---|---|
| FR-4.1 | Kolom pencarian makanan/buah dengan saran otomatis (autocomplete) dari basis data. | P0 |
| FR-4.2 | Input porsi dalam gram (dan satuan umum, misal butir, sendok makan, piring, gelas). | P0 |
| FR-4.3 | Hasil estimasi kalori, karbo, protein, lemak dihitung proporsional: `nilai = nilai_per_100g × porsi / 100`. | P0 |
| FR-4.4 | Hasil diperbarui langsung saat porsi atau makanan berubah (tombol "Hitung" tetap tersedia sebagai pemicu eksplisit). | P0 |
| FR-4.5 | Pintasan makanan sehat (chip): Greek yogurt, pisang, telur rebus, dada ayam, dan seterusnya; sebaiknya dipersonalisasi dari makanan yang sering dicatat. | P1 |
| FR-4.6 | Tombol "Tambahkan ke jurnal" dari hasil kalkulator, dengan pilihan waktu makan. | P0 |

### 6.5 Jurnal Makan

| ID | Kebutuhan | Prioritas |
|---|---|---|
| FR-5.1 | Empat kartu waktu makan: Sarapan Pagi, Makan Siang, Makan Malam, Camilan Sehat; masing-masing menampilkan target kalori dan realisasi. | P0 |
| FR-5.2 | Target kalori per waktu makan diturunkan dari target harian (default pembagian mengikuti mockup: sekitar 25% / 35% / 30% / 10%) dan dapat disesuaikan. | P1 |
| FR-5.3 | Setiap entri menampilkan foto/ikon, nama, kalori, dan ringkasan P/K/L. | P0 |
| FR-5.4 | Status entri "Tercatat" dan penanda "Sudah disantap" (centang). Perilaku: entri dapat berstatus rencana atau sudah disantap; hanya yang sudah disantap dihitung ke ringkasan (perlu konfirmasi, lihat Pertanyaan Terbuka). | P0 |
| FR-5.5 | Menu titik tiga pada kartu: edit target, salin dari kemarin, kosongkan waktu makan. | P1 |
| FR-5.6 | Edit dan hapus entri (geser atau menu), dengan opsi "Urungkan" (undo) setelah menghapus. | P0 |
| FR-5.7 | Empty state ramah pada waktu makan tanpa entri, menampilkan sisa kuota kalori dan ajakan menambah. | P0 |
| FR-5.8 | Tombol "Tambah …" di tiap kartu membuka modal pencatatan dengan kategori terisi otomatis. | P0 |

### 6.6 Modal Catat Santapan (Quick Log)

| ID | Kebutuhan | Prioritas |
|---|---|---|
| FR-6.1 | Dibuka dari FAB "Catat Santapan" atau tombol tambah per waktu makan; tampil sebagai bottom sheet. | P0 |
| FR-6.2 | Field: nama makanan/minuman, estimasi kalori, porsi, dan makro opsional (karbo, protein, lemak). | P0 |
| FR-6.3 | Pencarian makanan dari basis data mengisi field secara otomatis; pengguna dapat menimpa nilai. | P0 |
| FR-6.4 | Validasi: nama wajib; angka tidak boleh negatif; peringatan bila kalori tidak sebanding dengan makro yang diisi (selisih besar). | P0 |
| FR-6.5 | Bila kalori kosong tetapi makro diisi, sistem menghitung kalori dari makro (4/4/9). | P1 |
| FR-6.6 | Konfirmasi keberhasilan berupa toast yang tidak menghalangi (bukan dialog `alert`). | P0 |
| FR-6.7 | Opsi "Simpan sebagai makanan saya" untuk membuat makanan kustom yang dapat dipakai ulang. | P1 |
| FR-6.8 | Modal dapat ditutup dengan tombol Batal, ikon tutup, ketuk di luar, atau tombol Esc; fokus terjaga di dalam modal saat terbuka. | P0 |

### 6.7 Hidrasi

| ID | Kebutuhan | Prioritas |
|---|---|---|
| FR-7.1 | Pencatatan air dengan penambahan cepat (misal +250 ml) dan koreksi. | P0 |
| FR-7.2 | Progres air terhadap target ditampilkan di kartu ringkasan (warna `#38BDF8`). | P0 |

### 6.8 Basis Data Makanan

| ID | Kebutuhan | Prioritas |
|---|---|---|
| FR-8.1 | Basis data awal mencakup makanan Indonesia (bahan dan masakan umum), disusun dari sumber resmi seperti Tabel Komposisi Pangan Indonesia (TKPI), dilengkapi sumber tepercaya lain yang berlisensi. | P0 |
| FR-8.2 | Setiap makanan memiliki nilai per 100 g (kalori, karbo, protein, lemak, serat) dan satuan porsi umum beserta bobot gramnya. | P0 |
| FR-8.3 | Pencarian toleran salah ketik dan sinonim (misal "alpukat"/"avokad", "tahu"/"tofu"). | P0 |
| FR-8.4 | Pengguna dapat menambah makanan kustom; makanan kustom bersifat pribadi. | P1 |
| FR-8.5 | Pengguna dapat melaporkan data makanan yang tampak keliru. | P2 |

### 6.9 Statistik (v1.1)

| ID | Kebutuhan | Prioritas |
|---|---|---|
| FR-9.1 | Segmented control Hari / Minggu / Bulan. | P1 |
| FR-9.2 | Grafik kalori dan makro terhadap target, rata-rata, dan jumlah hari tercatat. | P1 |
| FR-9.3 | Ringkasan mingguan dengan sorotan positif (misal "protein tercapai 5 dari 7 hari"). | P1 |

### 6.10 Profil dan Pengaturan

| ID | Kebutuhan | Prioritas |
|---|---|---|
| FR-10.1 | Ubah data tubuh, tujuan, dan target; hitung ulang target dengan konfirmasi. | P0 |
| FR-10.2 | Nama panggilan dan foto profil; sapaan pada header memakai nama panggilan pengguna. | P0 |
| FR-10.3 | Pengaturan satuan (metrik; opsi imperial P2), bahasa, dan notifikasi. | P1 |
| FR-10.4 | Ekspor data dan hapus akun beserta seluruh datanya. | P0 |

### 6.11 Notifikasi

| ID | Kebutuhan | Prioritas |
|---|---|---|
| FR-11.1 | Pusat notifikasi (ikon lonceng di header). | P1 |
| FR-11.2 | Pengingat makan dan minum yang dapat diatur waktunya dan dimatikan; nada pesan hangat, tidak memaksa. | P1 |

### 6.12 Akun dan Sinkronisasi

| ID | Kebutuhan | Prioritas |
|---|---|---|
| FR-12.1 | Daftar dan masuk dengan email dan Google; pemulihan kata sandi. | P0 |
| FR-12.2 | Data tersinkron antarperangkat. | P0 |
| FR-12.3 | Mode offline dasar: entri dapat dicatat tanpa internet dan disinkronkan saat kembali online. | P1 |

---

## 7. Alur Pengguna Utama

**Pengguna baru**
1. Membuka aplikasi → layar sambutan → daftar/masuk.
2. Onboarding: data tubuh → aktivitas → tujuan → tinjau target (dapat diedit) → selesai.
3. Mendarat di Jurnal dengan empty state yang mengajak mencatat makanan pertama.

**Mencatat makanan (jalur cepat)**
1. Ketuk FAB "Catat Santapan" atau "Tambah …" pada kartu waktu makan.
2. Cari makanan → pilih → atur porsi → Simpan.
3. Cincin dan bar makro diperbarui seketika; toast konfirmasi muncul.

**Estimasi sebelum makan**
1. Isi Kalkulator Cepat → lihat kalori dan makro.
2. Opsional: "Tambahkan ke jurnal".

---

## 8. Kebutuhan Desain dan UX

Mengacu pada `DESIGN.md`. Ringkasan hal yang wajib dipatuhi:

- **Gaya:** hangat, pastel, minimalis lembut; bahasa yang mendukung dan merayakan, tidak menghakimi.
- **Warna makro (konsisten di seluruh aplikasi):** Protein `#FB7185`, Karbohidrat `#FDBA74`, Lemak `#86EFAC`, Energi `#F43F5E`, Air `#38BDF8`.
- **Tipografi:** Plus Jakarta Sans untuk judul, label, dan metrik; Inter untuk teks isi dan data nutrisi.
- **Bentuk:** tombol dan chip berbentuk kapsul penuh; kartu dengan radius 1,5–2 rem; ujung progres membulat.
- **Elevasi:** bayangan bernuansa rose-mauve lembut, bukan hitam; border tipis `rgba(244,114,182,0.2)`.
- **Tata letak:** mobile-first, margin 20 px, jarak antarmodul 16 atau 24 px; kolom 4 → 8 → 12 pada tablet dan desktop.
- **Target sentuh:** minimal 44×44 px untuk elemen interaktif.
- **State wajib untuk tiap komponen:** default, hover, fokus, aktif (scale 0,97), nonaktif, memuat (skeleton), kosong, dan galat.
- **Aksesibilitas:** target WCAG 2.2 AA; label ARIA pada tombol ikon; urutan fokus logis; kontras teks terpenuhi; tidak mengandalkan warna saja untuk menyampaikan status; dukungan `prefers-reduced-motion`.
- **Desktop:** layout desktop belum didesain di mockup dan perlu dirancang (misal dashboard dua kolom dengan navigasi samping).

### Catatan Temuan pada Mockup (perlu diselaraskan sebelum pengembangan)

1. **Warna primer berbeda.** `DESIGN.md` menyebut primary `#F472B6` pada narasi komponen, sedangkan token `primary` di konfigurasi Tailwind adalah `#a43073` (mawar tua), dan `#F472B6` dipakai sebagai `primary-container`. Perlu ditetapkan satu aturan penggunaan token (mana untuk isian tombol, mana untuk teks).
2. **Data contoh tidak konsisten.** Total makro dari item yang tercatat (karbo ≈116 g, protein ≈95 g, lemak ≈37 g) berbeda dari angka di kartu ringkasan (145 g / 78 g / 42 g). Total kalori (410 + 520 + 310 = 1.240) sudah cocok. Pada implementasi, semua angka wajib dihitung dari data, bukan statis.
3. **Tanggal pada mockup** menampilkan "Oktober 2024" dan "Kam 24"; harus dinamis.
4. **Sapaan "Halo, Cantik ✨"** bersifat spesifik gender. Disarankan memakai nama panggilan pengguna.
5. **Kalkulator Cepat** saat ini menghitung dengan rasio tetap alpukat. Pada produk, harus memakai data makanan yang dipilih.
6. **Modal tersimpan dengan `alert()`.** Ganti dengan toast sesuai semangat desain.
7. **Elemen "Live"** pada Kalkulator Cepat perlu makna yang jelas (hasil otomatis) atau dihapus.
8. **Ikon dan aset eksternal** (Material Symbols, foto makanan dari URL pihak ketiga, Tailwind CDN) perlu diganti aset hosting sendiri untuk produksi.
9. **Pengaturan viewport** (`maximum-scale=1`, `user-scalable=no`) menghalangi zoom dan melanggar praktik aksesibilitas; sebaiknya dihapus.

---

## 9. Model Data (Konseptual)

| Entitas | Atribut utama |
|---|---|
| **User** | id, email, nama_panggilan, foto, tanggal_lahir, jenis_kelamin, tinggi_cm, berat_kg, tingkat_aktivitas, tujuan, satuan, bahasa, dibuat_pada |
| **Target** | user_id, kalori, karbo_g, protein_g, lemak_g, serat_g, air_ml, pembagian_waktu_makan, berlaku_sejak |
| **Food** | id, nama, nama_alternatif[], kategori, per_100g {kkal, karbo, protein, lemak, serat}, satuan_porsi[], sumber, is_custom, owner_id |
| **JournalEntry** | id, user_id, tanggal, meal_type, food_id (opsional), nama, porsi_gram, porsi_label, kkal, karbo, protein, lemak, serat, status (rencana/disantap), dibuat_pada |
| **WaterLog** | id, user_id, tanggal, jumlah_ml |
| **WeightLog** (v1.2) | id, user_id, tanggal, berat_kg |
| **Notification** | id, user_id, jenis, jadwal, aktif |

Catatan: nilai gizi pada `JournalEntry` disimpan sebagai snapshot saat dicatat, agar riwayat tidak berubah ketika data makanan diperbarui.

---

## 10. Kebutuhan Non-Fungsional

| Area | Kebutuhan |
|---|---|
| **Performa** | LCP < 2,5 detik pada jaringan 4G; interaksi < 100 ms; pembaruan dashboard setelah log < 200 ms; bundle awal dijaga ramping |
| **Kompatibilitas** | Dua versi terbaru Chrome, Safari, Firefox, Edge; Safari iOS dan Chrome Android; layar mulai 360 px |
| **Offline/PWA** | Dapat di-install, cache aset, antrean sinkronisasi untuk entri offline |
| **Keamanan** | HTTPS, kata sandi ter-hash, otorisasi per pengguna, perlindungan terhadap XSS/CSRF/injection, pembatasan laju (rate limiting) |
| **Privasi** | Persetujuan eksplisit, kebijakan privasi dalam bahasa Indonesia, kepatuhan terhadap UU Pelindungan Data Pribadi (UU PDP), kemampuan ekspor dan hapus data, data kesehatan diperlakukan sebagai data sensitif |
| **Aksesibilitas** | WCAG 2.2 AA |
| **Keandalan** | Ketersediaan ≥ 99,5%; pencadangan data berkala |
| **Lokalisasi** | Teks bahasa Indonesia; format angka lokal (1.240, koma desimal); siap menambah bahasa |
| **Observabilitas** | Pencatatan galat dan analitik produk yang meminimalkan data pribadi |

---

## 11. Saran Arsitektur Teknis (Dapat Didiskusikan)

- **Front-end:** SPA/PWA dengan komponen berbasis design token; mockup sudah memakai Tailwind CSS sehingga token dapat dipindahkan langsung ke konfigurasi proyek (React/Next.js atau Vue/Nuxt sama-sama cocok).
- **Back-end:** REST atau GraphQL API dengan basis data relasional (PostgreSQL); autentikasi email dan OAuth Google.
- **Pencarian makanan:** indeks pencarian teks penuh dengan toleransi salah ketik.
- **Perhitungan gizi:** fungsi murni yang dapat diuji unit (BMR, TDEE, makro, skala porsi) agar konsisten antara klien dan server.
- **Penyimpanan aset:** font, ikon, dan gambar di-host sendiri; gambar dioptimalkan (WebP/AVIF, lazy loading).

---

## 12. Analitik dan Event

Event utama yang dilacak (tanpa menyimpan konten sensitif yang tidak perlu): `onboarding_started`, `onboarding_completed`, `target_edited`, `food_searched`, `food_logged` (dengan sumber: pencarian/kalkulator/manual/favorit), `quick_calc_used`, `water_logged`, `date_changed`, `stats_viewed`, `notification_opt_in`.

---

## 13. Rencana Rilis (Usulan)

| Fase | Isi | Keluaran |
|---|---|---|
| **0. Penyelarasan** | Selesaikan Pertanyaan Terbuka, tinjau rumus oleh ahli gizi, rapikan token desain | PRD final, design system final |
| **1. Desain lanjutan** | Onboarding, login, profil, detail makanan, statistik, layout desktop, state kosong/galat/memuat | Desain lengkap MVP |
| **2. Fondasi** | Setup proyek, design token, akun, basis data makanan awal | Kerangka aplikasi dan API |
| **3. MVP inti** | Onboarding, kalkulator, jurnal, kalkulator cepat, dashboard, hidrasi | Beta tertutup |
| **4. Penyempurnaan** | Aksesibilitas, performa, PWA/offline, uji kegunaan | Rilis v1.0 |
| **5. Iterasi** | Statistik, favorit, notifikasi (v1.1), lalu resep dan barcode (v1.2) | Rilis berkala |

---

## 14. Risiko dan Mitigasi

| Risiko | Dampak | Mitigasi |
|---|---|---|
| Akurasi rumus dan data gizi dipertanyakan | Kepercayaan menurun, potensi saran tidak tepat | Tinjau ahli gizi; tampilkan sumber data; label "estimasi"; fitur lapor data keliru |
| Basis data makanan Indonesia tidak lengkap | Pencatatan lambat, pengguna berhenti | Mulai dari TKPI, tambah makanan kustom, prioritaskan makanan populer berdasarkan data pencarian |
| Pengguna menetapkan target ekstrem atau memiliki riwayat gangguan makan | Risiko kesehatan | Batas kalori minimum, bahasa non-judgmental, tidak ada "streak" yang menghukum, tautan ke sumber bantuan profesional, disclaimer yang jelas |
| Pengguna rentan (anak, hamil, kondisi medis) memakai target otomatis | Saran tidak sesuai | Deteksi dan arahkan konsultasi tenaga kesehatan (FR-1.8) |
| Pelanggaran privasi data kesehatan | Risiko hukum dan reputasi | Prinsip minimisasi data, enkripsi, kepatuhan UU PDP |
| Retensi rendah | Produk tidak berkembang | Log cepat, favorit, pengingat lembut, pencapaian positif |
| Inkonsistensi desain dan kode | Biaya pengerjaan ulang | Selaraskan token sebelum pengembangan (lihat Catatan Temuan) |

---

## 15. Pertanyaan Terbuka

1. **Audiens:** Apakah produk ditujukan untuk semua gender, atau berfokus pada perempuan? Ini memengaruhi bahasa sapaan dan pemasaran.
2. **Model bisnis:** Gratis penuh, freemium, atau berlangganan? Fitur mana yang berbayar?
3. **Sumber data makanan:** Apakah cukup TKPI dan input pengguna, atau perlu lisensi basis data komersial dan barcode?
4. **Status entri:** Apakah tombol centang "Sudah disantap" berarti entri berstatus rencana sampai dicentang, atau hanya penanda visual?
5. **Pembagian kalori per waktu makan:** Tetap (25/35/30/10) atau dapat dikustomisasi sejak onboarding?
6. **Akun:** Wajib login sejak awal, atau boleh mencoba sebagai tamu lebih dulu?
7. **Platform:** Apakah PWA cukup, atau akan ada aplikasi native di tahap berikutnya?
8. **Tujuan kesehatan khusus:** Apakah perlu mendukung kebutuhan tertentu (diabetes, hipertensi, ibu hamil) atau cukup umum pada v1?
9. **Nama dan merek:** Konfirmasi nama "NutriGlow" dan aset logo final.

---

## 16. Lampiran: Inventaris Komponen dari Mockup

| Komponen | Lokasi di `code.html` | Catatan implementasi |
|---|---|---|
| Header tetap (logo, sapaan, notifikasi, avatar) | `<header>` | Blur latar, mendukung safe-area |
| Strip kalender 7 hari | Section pertama | Hari aktif memakai gradien dan skala 1,05 |
| Kartu ringkasan hero | Section "Ringkasan Nutrisi" | Cincin SVG (r=40, keliling ≈251,2) + 3 bar makro + 2 penghitung mini |
| Kalkulator Cepat | Section "Kalkulator Cepat" | Pencarian, porsi gram, hasil K/P/L, chip pintasan |
| Kartu waktu makan | Section "Catatan Santapan Hari Ini" | 4 kartu; item dengan foto, kalori, makro, centang |
| Empty state camilan | Kartu Camilan Sehat | Tautan ajakan menambah |
| Modal Catat Santapan | `#quickLogModal` | Bottom sheet, maks. tinggi 85vh |
| FAB "Catat Santapan" | `<aside>` | Gradien rose, bayangan glow |
| Navigasi bawah | `<nav>` | 4 tab, tab aktif berwarna primer |
