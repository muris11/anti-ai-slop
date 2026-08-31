# anti-ai-slop

<div align="center">

**Anti Slop: Aturan untuk AI Coding Agent.**

Sebuah filter yang menghentikan AI agent menghasilkan UI, teks, dan kode **AI slop** yang generik — tanpa membuat hasilnya jadi kaku.

**Filter, bukan style guide.** Ia menolak *teknik tanpa tujuan*, bukan tekniknya itu sendiri.

&nbsp;

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE)
[![Version](https://img.shields.io/badge/version-2.0.3-6366f1?style=flat-square)](#)
[![skills.sh](https://img.shields.io/badge/skills.sh-muris11%2Fanti--ai--slop-111827?style=flat-square&logo=github)](https://www.skills.sh/muris11/anti-ai-slop)
[![GitHub stars](https://img.shields.io/github/stars/muris11/anti-ai-slop?style=flat-square)](https://github.com/muris11/anti-ai-slop)

**17 skill · satu filter selalu-aktif · 7 agent · 3 platform**

</div>

&nbsp;

> **Bahasa:** **Bahasa Indonesia** · [English](README.md)

---

## Ringkasan

`anti-ai-slop` adalah **filter** untuk AI coding agent. Ia menyuruh agent berhenti menghasilkan *tampilan AI default* — gradient ungu, hero di tengah, tiga kartu identik, teks "unlock the power", metrik palsu — **tanpa memaksakan satu estetika tertentu.**

Ide intinya, dalam empat kata:

> **No hierarchy + no specificity + no restraint + no opinion.**

AI slop bukan satu teknik. Gradient itu fine. Card grid itu fine. Inter itu fine. **Slop adalah kombinasi tanpa-tanda** dari default generik yang berulang karena tidak ada yang mengambil keputusan. Dua tes yang dipakai di seluruh sistem:

1. **Tes tujuan** — bisakah kamu menulis satu kalimat jujur kenapa teknik ini melayani *produk ini*?
2. **Tes konvergensi** — apakah teknik yang sama muncul di layar/elemen tak-terkait tanpa alasan?

---

## Isi

**17 skill**:

- **Core filter** — `antislop` (selalu aktif)
- **Katalog master** — `antislop-master` (audit indikator P0–P6)
- **Visual & layout** — `antislop-ui` · `antislop-layout` · `antislop-imagery` · `antislop-designsystem`
- **Copy & konten** — `antislop-copywriting` · `antislop-authenticity`
- **Produk & UX** — `antislop-dashboard` · `antislop-forms` · `antislop-motion` · `antislop-nav`
- **Manusia & platform** — `antislop-human` · `antislop-layoutmobile` · `antislop-mobile`
- **Kode** — `antislop-code`
- **Loader** — `slop` (memuat seluruh keluarga sekaligus)

### Taksonomi master

`antislop-master` adalah **katalog ber-severity** dari ~180 indikator lintas warna, tipografi, layout, komponen, copy, motion, state UX, autentisitas, kode, dan platform. Setiap indikator dinilai kuat-lemahnya sinyal:

| Tier | Makna |
|---|---|
| **P0** | Tanda AI instan — sinyal terkuat |
| **P1** | Tanda kuat — satu pun cukup keras, biasanya salah |
| **P2** | Pola mencurigakan — default AI umum, mungkin sah |
| **P3** | Bergantung konteks — hanya slop di konteks yang salah |
| **P4** | Slop kualitas/UX — mengirim pengalaman yang belum utuh |
| **P5** | Slop autentisitas — data, klaim, atau bukti palsu |
| **P6** | Slop kode — implementasi yang buruk |

Katalog ini juga punya protokol audit **Quick / Full / Deep** supaya bisa memindai sedalam yang dibutuhkan tugas.

---

## Instalasi

Ikuti salah satu jalur berikut.

### 1. Skills directory (berfungsi sekarang, disarankan)

Jalur tercepat, dan terdaftar di [skills.sh](https://www.skills.sh/muris11/anti-ai-slop):

```bash
npx skills add muris11/anti-ai-slop
```

Tambahkan `--all`, `-g`, atau `--skill <nama>`. Jalankan `--list` dulu.

> Jalur ini menyalin folder skill tapi **tidak** menulis pointer sesi. Kalau sudah pakai, lanjutkan dengan picker (jalur 2) dan pilih **Keep what is there**.

### 2. Picker interaktif

Satu perintah, lalu pilih skill mana, di mana (project atau global), dan agent mana:

```bash
npx anti-ai-slop
```

Picker menginstal folder dan **menulis pointer sesi** yang memuat filter setiap sesi — satu-satunya jalur yang menulis pointer otomatis.

> `anti-ai-slop` dipublikasikan sebagai paket npm. Untuk menjalankan picker dari clone, gunakan `npm i && npm run installer` di folder `cli/` repo ini.

### 3. Plugin (Claude Code)

```text
/plugin marketplace add https://github.com/muris11/anti-ai-slop
/plugin install antislop@anti-ai-slop
```

### 4. Plugin (Antigravity)

```bash
agy plugin install https://github.com/muris11/anti-ai-slop
```

### 5. Manual (satu file)

```bash
curl -o antislop.md https://raw.githubusercontent.com/muris11/anti-ai-slop/main/antislop.md
```

```powershell
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/muris11/anti-ai-slop/main/antislop.md" -OutFile "antislop.md"
```

---

## Skills

| Skill | Cakupan | Ships in |
|---|---|---|
| **antislop** | Filter inti selalu-aktif: tes tujuan, tier aturan, Delivery Gate | v2.0.3 |
| **antislop-master** | Taksonomi master P0–P6: ~180 indikator + protokol audit | v2.0.3 |
| **antislop-ui** | UI & visual: warna, komponen, dekorasi, motion, struktur | v2.0.3 |
| **antislop-layout** | Layout & komposisi: hero, section, simetri, grid, spacing | v2.0.3 |
| **antislop-copywriting** | Teks & copy: headline, CTA, tone, pola anti-AI-writing | v2.0.3 |
| **antislop-human** | Manusia: kontras (dengan checker), keyboard, fokus, state | v2.0.3 |
| **antislop-layoutmobile** | Layout mobile: breakpoint, grid, overflow, tap target | v2.0.3 |
| **antislop-mobile** | Mobile & native: reflow, tanpa overflow, target 44px, Flutter | v2.0.3 |
| **antislop-dashboard** | Dashboard & data: metric card, chart, tabel, state lengkap | v2.0.3 |
| **antislop-forms** | Form & state: validasi, empty/loading/error/offline | v2.0.3 |
| **antislop-motion** | Motion: alasan UX, satu animasi fokus, reduced-motion | v2.0.3 |
| **antislop-nav** | Navigasi & chrome: IA nyata, tanpa dead link, footer jujur | v2.0.3 |
| **antislop-authenticity** | Autentisitas: tanpa metric, testimoni, logo, atau klaim palsu | v2.0.3 |
| **antislop-designsystem** | Konsistensi design system: token nyata, skala spacing, paritas tema | v2.0.3 |
| **antislop-imagery** | Imagery & dekorasi: ilustrasi, background, ikon, media | v2.0.3 |
| **antislop-code** | Komentar kode: hapus komentar AI-slop, pertahankan yang berharga | v2.0.3 |
| **slop** | Loader sekali-jalan untuk seluruh keluarga sekaligus | v2.0.3 |

---

## Dukungan Agent

| Agent | Folder skill | Picker | Plugin |
|---|---|---|---|
| Claude Code | `.claude/skills` | Ya | Ya (marketplace) |
| Antigravity | `.agents/skills` | Ya | Ya (`agy`) |
| Codex | `.codex/skills` | Ya | Tidak |
| OpenCode | `.opencode/skills` | Ya | Tidak |
| Cursor | `.cursor/skills` | Ya | Tidak |
| Gemini CLI | `.gemini/skills` | Ya | Tidak |
| Hermes | `~/.hermes/skills` (global) | Ya | Tidak |

Setiap skill adalah folder standar **Agent Skills** terbuka (`<nama>/SKILL.md`). Bekerja di **Windows, macOS, dan Linux**.

---

## Mode Penggunaan

| Mode | Kapan | Alur |
|---|---|---|
| **DURING** | membangun pekerjaan baru | terapkan aturan sambil membangun, akhiri dengan Delivery Gate |
| **AFTER** | mengaudit pekerjaan jadi | daftar temuan bernomor → kamu setujui → perbaiki → lapor ulang |

Core meminta, *"Kapan ini berlaku — selama pekerjaan, atau setelah selesai?"* sebelum apa pun berjalan.

---

## Roadmap

Lihat [ROADMAP.md](ROADMAP.md). **v2.0.0** menambahkan taksonomi master dan sembilan skill fokus; **v2.0.1** merapikan README, memfinalisasi lisensi, dan memverifikasi indeks skills.sh; **v2.0.2** memisahkan README menjadi bahasa Inggris dan Indonesia, lalu menulis ulang SECURITY.md; **v2.0.3** menambahkan CI, contributing, template, dan polesan repo.

---

## FAQ

**Apakah ini style guide?** Bukan — filter. Tidak menentukan warna, font, atau layout. Menolak teknik tanpa tujuan dan menuntut kehidupan. Arah adalah milikmu (`DESIGN.md`).

**Cuma untuk halaman web?** Tidak. Mengaudit dan menulis interface, teks, mobile, Flutter, dashboard, komentar kode, dan design system.

**Apakah `Inter`, gradient, atau card grid otomatis slop?** Tidak. Masing-masing hanya kandidat saat muncul sebagai default tanpa alasan produk (tes tujuan dan konvergensi).

**Apakah aku butuh `DESIGN.md`?** Ya untuk UI. Filter bisa menghapus slop tapi tidak menciptakan arah; hasil kaku berarti arahnya tidak ada, bukan filternya gagal.

---

## Kontribusi

Menemukan pola AI slop baru, aturan yang meleset, atau bug di installer? Buka issue. PR diterima untuk pola baru, klarifikasi, atau item checklist yang tidak sinkron dengan aturannya.

---

## Lisensi

[MIT](LICENSE) © 2026 muris11. Lakukan apa pun yang kamu mau.

---

<div align="center">

*Filter slop-nya. Jaga kerapiannya.*

</div>
