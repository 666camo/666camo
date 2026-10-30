# PLAN — GitHub Profile README | Alif Rifky

> **Status:** Implementasi selesai; validasi dan publikasi sedang berjalan  
> **Konsep:** **Noir / Maroon Developer Profile**  
> **Target:** Profil GitHub yang elegan, minimalis, dominan hitam, dengan aksen maroon yang tidak berlebihan.  
> **Bahasa konten README:** Bahasa Inggris yang ringkas dan profesional; catatan proyek ini menggunakan Bahasa Indonesia.

---

## 1. Tujuan

Membangun halaman profil GitHub yang:

- Memperkenalkan **Alif Rifky**, mahasiswa **Teknik Informatika** yang berdomisili di **Bandung, Indonesia**.
- Memperlihatkan teknologi yang **pernah dipelajari/dieksplorasi** tanpa mengklaim semua teknologi telah dikuasai secara profesional.
- Menampilkan **durasi coding dari WakaTime** yang diperbarui otomatis.
- Memiliki **animasi snake GitHub contribution graph** yang diperbarui otomatis.
- Memiliki **profile-view counter** serta tautan Instagram, LinkedIn, dan email.
- Nyaman dilihat dalam GitHub dark mode, rapi di desktop dan mobile, serta tidak ramai dengan badge/dekorasi berlebihan.

**Batasan desain:** README GitHub bukan halaman web bebas; tidak menggunakan JavaScript interaktif atau CSS custom yang mengandalkan GitHub untuk dijalankan. Desain dibuat melalui Markdown, HTML sederhana yang diizinkan, badge, dan gambar/SVG yang kompatibel dengan GitHub.

---

## 2. Design System — Black × Maroon

### 2.1 Palet warna final

| Peran | Nama warna | HEX | Penggunaan |
|---|---|---|---|
| **Background utama** | Obsidian Black | `#08080A` | Latar visual header, panel, dan aset SVG utama |
| **Background sekunder** | Charcoal Black | `#111114` | Kartu informasi, area statistik, section divider |
| **Background elevated** | Graphite | `#1B1A1E` | Panel kecil dan latar ikon saat diperlukan |
| **Border** | Smoky Maroon | `#34252B` | Outline halus, separator, garis pembatas |
| **Aksen utama** | Deep Maroon | `#7B263D` | Garis aksen, judul penting, snake, highlight |
| **Aksen aktif** | Muted Ruby | `#A43E5A` | Hover visual, garis aktif, gradien pendek |
| **Aksen terang** | Soft Rose Maroon | `#C66D87` | Teks link atau detail kecil yang perlu kontras |
| **Teks utama** | Soft White | `#F2EEF0` | Nama, heading, dan konten utama |
| **Teks sekunder** | Ash Gray | `#AAA2A7` | Deskripsi, metadata, label |
| **Teks redup** | Slate Gray | `#777077` | Catatan, caption, informasi tersier |

**Proporsi visual yang diinginkan:** kira-kira **85% hitam/abu gelap, 10% putih/abu terang, dan 5% maroon**. Ini adalah pedoman komposisi, bukan perhitungan piksel yang harus persis.

### 2.2 Aturan penggunaan warna

1. **Hitam sebagai identitas utama**. Latar dominan `#08080A` atau `#111114`.
2. **Maroon hanya aksen**: underline judul, satu sisi border, ikon kecil, atau elemen bergerak seperti ular; hindari satu panel penuh maroon terang.
3. **Teks tetap mudah dibaca** menggunakan `#F2EEF0` dan `#AAA2A7`. Jangan menulis paragraf panjang dengan maroon tua karena kontras rendah.
4. **Jangan gunakan** cyan, ungu neon, merah menyala, atau efek glow besar. Nuansa yang ditargetkan adalah **premium, kalem, dan developer-oriented**.
5. **Ikon teknologi** boleh tetap memakai warna resmi masing-masing supaya mudah dikenali; warna komponen dekorasi di sekitarnya tetap hitam-maroon.
6. **Pilih visual SVG transparan jika memungkinkan**, sehingga tetap terlihat rapi saat GitHub dibuka dalam mode terang maupun gelap. Aset yang memang berlatar hitam tetap dipertahankan sebagai elemen bergaya gelap.

### 2.3 Warna khusus snake

| Elemen | HEX |
|---|---|
| Snake body | `#7B263D` |
| Snake head / highlight | `#C66D87` |
| Contribution cell kosong | `#1B1A1E` |
| Contribution cell rendah | `#352028` |
| Contribution cell sedang | `#572637` |
| Contribution cell tinggi | `#87334D` |
| Latar canvas | `#08080A` |

> Catatan implementasi: palet snake kustom perlu dikonfigurasi pada output generator `Platane/snk` dan diperiksa tampilannya, bukan sekadar mengubah warna Markdown.

---

## 3. Identitas dan Kontak

| Field | Konten |
|---|---|
| Nama tampilan | **Alif Rifky** |
| Bidang studi | **Informatics Engineering / Teknik Informatika** |
| Lokasi | **Bandung, Indonesia** |
| Instagram | [`@cptaincm`](https://instagram.com/cptaincm) |
| LinkedIn | **Alif Rifky** — (https://www.linkedin.com/in/alif-rifky-a16144419/)|
| Email | [`pratamaalifrifky@gmail.com`](mailto:pratamaalifrifky@gmail.com) |
| GitHub username | **666camo** — dikonfirmasi dari repository pengguna |

Jangan memakai username `Yuuashura`, nama, kontak, atau tema RPG dari `README.md` referensi sebagai identitas pengguna. File tersebut hanya referensi mekanisme/fitur.

---

## 4. Struktur Visual README

### 01 — Hero / Introduction

**Tujuan:** Pengunjung langsung mengenal nama, bidang, dan keunikan profil.

Konten:
- Heading: **`Hi, I'm Alif Rifky.`**
- Subheading: **`Informatics Engineering Student`**
- Kalimat singkat tentang ketertarikan pada problem solving, algorithms, software development, dan belajar teknologi.
- Metadata: **Bandung, Indonesia**.
- **Profile Views** counter ukuran kecil di bawah header.
- Header visual minimalis: background black, satu garis maroon, tanpa anime/RPG/efek mencolok.

**Gaya:** rata tengah untuk hero atau kiri untuk teks utama; gunakan satu gaya secara konsisten.

### 02 — About Me & Teaching Experience

Bagian paling personal dan menjadi pembeda profil:

- Mahasiswa Teknik Informatika.
- Menyukai membangun pemahaman fundamental pemrograman dan menyelesaikan masalah secara terstruktur.

**Hindari:** mengarang nama lembaga, durasi mengajar, proyek, pekerjaan, atau pencapaian yang belum diberikan.

### 03 — Technologies I've Learned & Explored

Kelompok dan urutan mengikuti screenshot yang dikirim:

**Languages:** `C`, `C++`, `Java`, `JavaScript`, `TypeScript`, `Python`, `PHP`, `Go`.

**Web, Backend & Data:** `HTML5`, `CSS3`, `React`, `Tailwind CSS`, `Spring / Spring Boot`, `Node.js`, `Express.js`, `MySQL`, `PostgreSQL`, `Redis`, `RabbitMQ`.

**Development Tools:** `Git`, `GitHub`, `VS Code`, `Linux`, `Docker`, `Postman`, `Vite`.

Implementasi ikon:
- Utamakan `skillicons.dev` untuk logo yang didukung.
- Untuk teknologi yang tidak didukung atau kurang terbaca, gunakan ikon resmi/Simple Icons sebagai fallback.
- Bagi ikon menjadi tiga baris/kelompok yang berjarak rapi; jangan membuat satu baris sangat panjang sehingga terpotong di mobile.
- Tidak menampilkan progress bar **skill percentage** yang mengesankan tingkat kompetensi terukur padahal tidak ada sumbernya.

### 04 — Coding Activity · WakaTime

**Tujuan:** Menunjukkan waktu coding yang benar-benar tercatat.

Tampilan:
- Judul `Coding Activity` / `WakaTime Stats`.
- Total waktu coding yang tersedia dari WakaTime.
- Hingga 8 bahasa teratas dengan durasi dan proporsinya.
- Grafik teks otomatis atau aset statistik bernuansa gelap; hindari angka contoh/fiktif.
- Catatan `Updated automatically via WakaTime`.

**Penting:** Workflow referensi memakai `TIME_RANGE: all_time`; karena itu **jangan** memberi judul `Weekly Coding Activity` pada statistik tersebut. Jika nanti ingin statistik mingguan, buat blok lain dengan rentang minggu yang sesuai.

### 05 — GitHub Activity

Bagian opsional-terarah yang dapat memuat:
- Contribution/activity graph yang mendukung dark styling.
- Statistik singkat yang stabil dan tidak terlalu banyak kartu.
- Pilihan penyedia SVG yang ringan dan tetap tampil saat layanan pihak ketiga tersedia.

Utamakan **satu visual aktivitas**, bukan menumpuk banyak statistik serupa.

### 06 — Contribution Snake

- Judul `Contribution Snake` dengan aksen garis maroon tipis.
- SVG animasi snake dengan palet **black + maroon**, tanpa aksen cyan/ungu.
- Diproduksi dari kontribusi GitHub akun yang telah dikonfirmasi.
- Dibaca README dari file di branch `output`.
- Sediakan versi standar/dark bila dibutuhkan, dengan preferensi visual gelap.

> Snake dari `Platane/snk` adalah **animasi otomatis**, bukan game keyboard interaktif. Jika nanti membutuhkan game snake yang dapat dimainkan, itu memerlukan halaman/web app tersendiri dan bukan interaksi langsung dalam GitHub README.

### 07 — Connect With Me

Baris kontak kecil, rapi, tidak penuh badge besar:
- **Instagram:** `@cptaincm`.
- **LinkedIn:** `Alif Rifky` (https://www.linkedin.com/in/alif-rifky-a16144419/).
- **Email:** `pratamaalifrifky@gmail.com`.

Penutup sederhana, contohnya: **`Building, learning, and sharing — one commit at a time.`**

---

## 5. Rancangan Urutan Halaman

```text
┌─────────────────────────────────────────────┐
│  HI, I'M ALIF RIFKY.                       │
│  Informatics Engineering Student            │
│  Bandung, Indonesia                         │
│  [Profile Views]                            │
├─────────────────────────────────────────────┤
│  ABOUT ME                                  │
│  Former Instructor · C / Algorithms / DS    │
├─────────────────────────────────────────────┤
│  TECH STACK                                │
│  Languages / Web, Backend & Data / Tools    │
├─────────────────────────────────────────────┤
│  WAKATIME · CODING ACTIVITY                 │
│  Total Coding Time + Language Breakdown     │
├─────────────────────────────────────────────┤
│  GITHUB ACTIVITY                            │
│  Contribution / Activity Visualization      │
├─────────────────────────────────────────────┤
│  CONTRIBUTION SNAKE                         │
│  Animated SVG · Black / Maroon              │
├─────────────────────────────────────────────┤
│  CONNECT                                   │
│  Instagram  |  LinkedIn  |  Email           │
└─────────────────────────────────────────────┘
```

---

## 6. Arsitektur & File yang Dibutuhkan

```text
666camo/
├── README.md
└── .github/
    └── workflows/
        ├── snake.yml
        └── wakatime.yml

# Dibuat otomatis oleh workflow snake di branch terpisah:
output/
├── github-contribution-grid-snake.svg
└── github-contribution-grid-snake-dark.svg
```

**Syarat utama:** repository profil harus **public**, namanya sama persis dengan username GitHub, dan memiliki `README.md` pada root repository.

### 6.1 Snake workflow — rujukan `snake.yml`

Dari file referensi yang diberikan:
- Generator: `Platane/snk/svg-only@v3`.
- Akun: `${{ github.repository_owner }}`.
- Trigger: setiap **12 jam**, `workflow_dispatch`, dan push ke `main`/`master`.
- Output: SVG biasa dan SVG dark.
- Publish: file `dist/` ke branch **`output`** melalui `crazy-max/ghaction-github-pages@v3.1.0`.

Rencana penyempurnaan:
1. Pertahankan logika pengambilan contribution graph dan penulisan ke branch `output`.
2. Tambahkan konfigurasi **warna snake dan grid black-maroon** yang didukung generator.
3. Pastikan workflow memiliki izin `contents: write` bila dibutuhkan untuk publish.
4. Perbarui action yang memang perlu diperbarui hanya setelah diuji kompatibilitasnya.
5. Jalankan manual dari tab **Actions** untuk tes pertama.
6. Tampilkan SVG dengan URL branch `output` yang sesuai setelah username GitHub diketahui.

### 6.2 WakaTime workflow — rujukan `wakatime.yml`

Dari file referensi yang diberikan:
- Action: `athul/waka-readme@master`.
- Secret: `WAKATIME_API_KEY`.
- Trigger: setiap hari (`cron: "0 0 * * *"`), push ke `main`, dan `workflow_dispatch`.
- Rentang: `TIME_RANGE: all_time`.
- Jumlah bahasa: `LANG_COUNT: 8`.
- Durasi & total: `SHOW_TIME: true`, `SHOW_TOTAL: true`.
- Blok teks: `░▒▓█`.
- Izin: `contents: write`.

Rencana implementasi:
1. Pastikan akun WakaTime dan ekstensi editor sudah aktif untuk pencatatan.
2. Simpan token OAuth pembaca statistik melalui **Settings → Secrets and variables → Actions** sebagai `WAKATIME_API_KEY` (jangan letakkan key di README atau commit repository).
3. Tambahkan marker `<!--START_SECTION:waka-->` dan `<!--END_SECTION:waka-->` **tepat satu kali** pada bagian Coding Activity.
4. Gunakan workflow untuk memperbarui isi di antara marker; jangan isi total waktu/bahasa secara hardcode.
5. Uji `workflow_dispatch` dan periksa log bila statistik kosong; cek apakah data/rentang `all_time` tersedia di akun WakaTime.
6. Cegah dua workflow yang sama-sama commit ke branch default pada waktu yang bersamaan; snake sebaiknya menulis ke branch `output`, WakaTime menulis ke branch default.

**Catatan:** WakaTime menghitung aktivitas dari editor yang terhubung, bukan seluruh pengalaman ngoding sepanjang hidup. Data historis sebelum WakaTime aktif tidak boleh diada-adakan.

### 6.3 Profile views

- Gunakan badge counter eksternal yang menerima parameter `username=666camo`.
- Warna latar badge gelap dan label bernuansa abu; sedikit aksen maroon.
- Jangan mengklaim counter tersebut sebagai analitik **unique visitors** resmi GitHub.

---

## 7. Rencana Pengerjaan Bertahap

### Fase A — Finalisasi identitas
- [x] Konfirmasi username GitHub: 666camo.
- [x] Konfirmasi URL profil LinkedIn dari dokumen.
- [x] Nama tampilan: Alif Rifky.
- [x] Instagram: `cptaincm`.
- [x] Email: `pratamaalifrifky@gmail.com`.
- [x] Lokasi: Bandung, Indonesia.
- [x] Jurusan: Teknik Informatika.
- [x] Pengalaman instruktur C, Logika Algoritma, Struktur Data.

### Fase B — Implementasi tampilan
- [x] Susun ulang `README.md` dari nol menggunakan tema **Noir / Maroon**.
- [x] Buat hero minimalis (nama, bidang, lokasi, profile views).
- [x] Tulis About Me dan pengalaman instruktur secara ringkas.
- [x] Tambahkan semua kelompok teknologi berdasarkan screenshot.
- [x] Tambahkan blok WakaTime beserta marker automation.
- [x] Gunakan snake sebagai satu visual aktivitas; grafik tambahan opsional dihilangkan agar tidak duplikatif.
- [x] Tambahkan section snake dengan URL SVG dari branch `output`.
- [x] Tambahkan tautan kontak yang valid.

### Fase C — Otomasi
- [x] Sesuaikan `snake.yml` untuk warna black-maroon.
- [x] Pastikan izin GitHub Actions menulis output.
- [x] Periksa dan sesuaikan `wakatime.yml` serta secret.
- [ ] Jalankan dua workflow secara manual dan verifikasi hasil.
- [ ] Pastikan update WakaTime tidak menghapus konten README lainnya.

### Fase D — Quality Assurance
- [ ] Preview README di **GitHub desktop dark mode**.
- [ ] Preview README di **mobile**.
- [x] Periksa kontras teks dan maroon pada elemen penting.
- [x] Pastikan ikon teknologinya lengkap dan tidak rusak.
- [ ] Pastikan image, badge, grafik, dan SVG snake bisa diakses publik.
- [ ] Pastikan angka WakaTime berasal dari API, bukan contoh.
- [x] Pastikan token/API key tidak terekspos.
- [x] Pastikan tampilan tidak terlihat seperti tema RPG dan tidak terlalu ramai.

---

## 8. Kriteria Selesai (Definition of Done)

Pekerjaan dinyatakan selesai apabila:

1. README bisa dibuka pada profil GitHub dan terlihat **dominan hitam dengan aksen maroon tipis**.
2. Identitas dan pengalaman instruktur Alif Rifky ditampilkan akurat.
3. Seluruh daftar teknologi dari screenshot ada dan dikelompokkan benar.
4. Profile-view badge tampil dengan username GitHub yang benar.
5. WakaTime memperbarui statistik melalui GitHub Actions tanpa edit manual.
6. Snake tampil sebagai SVG animasi black-maroon dan workflow berhasil menghasilkan file di branch `output`.
7. Link Instagram, LinkedIn, dan email berfungsi.
8. Desktop/mobile tetap rapi, konten terbaca, dan tidak ada secret yang terekspos.

---

## 9. Deliverables Final

- **`README.md`** — profil baru lengkap dengan desain Noir / Maroon.
- **`.github/workflows/snake.yml`** — generator contribution snake dengan palet baru.
- **`.github/workflows/wakatime.yml`** — statistik coding WakaTime otomatis.
- **`plan.md`** — dokumen rencana, design tokens, checklist, dan keputusan desain ini.

## 10. Keputusan Desain yang Dikunci

- **Tema:** Dark / Black, bukan neon dan bukan RPG.
- **Aksen:** Maroon subtle, maksimum sekitar 5% elemen visual.
- **Palet utama:** `#08080A`, `#111114`, `#7B263D`, `#C66D87`, `#F2EEF0`.
- **Gaya:** Modern, minimalis, profesional, developer-oriented.
- **Fokus konten:** Identitas Teknik Informatika, pengalaman instruktur C, daftar teknologi yang pernah dipelajari.
- **Fitur otomatis:** WakaTime + animated GitHub contribution snake.
- **Identitas dikonfirmasi:** GitHub 666camo dan URL LinkedIn berasal dari instruksi pengguna.


## 11. Catatan implementasi dan verifikasi

- Ruling: Identitas GitHub dan LinkedIn sudah dikonfirmasi; placeholder lama diganti.
- Ruling: Go ditulis sebagai bahasa yang sedang dipelajari sesuai pengguna.
- Ruling: Snake menjadi satu visual aktivitas agar tidak duplikatif.
- Ruling: Ikon 48 px terpisah agar membungkus secara alami pada mobile.
- Ruling: Generator SVG tidak mendukung canvas dan warna kepala terpisah secara native. Langkah Python menambahkan latar hitam dan kepala rose, dengan pemeriksaan struktur SVG.
- Ruling: WakaTime dipin ke commit yang mendukung OAuth. Secret tetap WAKATIME_API_KEY; isinya token OAuth pembaca statistik, bukan key plugin yang hanya menulis aktivitas.
- Ruling: Trigger push dibatasi pada perubahan workflow agar commit statistik tidak memicu update berulang. Jadwal dan pemicu manual tetap tersedia.
- Ruling: Publikasi ke profil termasuk ruang lingkup yang sudah disetujui pengguna.
- Secret dikonfirmasi sudah ditambahkan oleh pengguna; nilainya tidak dibaca atau disimpan di repository.
- Validasi konten, YAML, XML/SVG, desktop/mobile, dan GitHub Actions; tidak menambah test suite untuk perubahan konten.

### Hasil validasi lokal

- YAML kedua workflow valid; izin, jadwal, dan dispatch diperiksa.
- Marker WakaTime tepat satu pasang; 26 ikon sesuai urutan.
- Header SVG valid. Pemrosesan snake diuji pada SVG asli generator; animasi tetap ada.
- Pratinjau bergaya GitHub dark pada 1200 px dan 390 px: tidak ada overflow halaman atau gambar gagal. Pratinjau lokal bukan screenshot halaman GitHub langsung.
- Publikasi dan hasil GitHub Actions menunggu pemeriksaan akhir.
