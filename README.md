<div align="center">

# anti-ai-slop

**Anti Slop: Rules for AI Coding Agents.**

A filter that stops AI agents from generating generic **AI slop** in UI, copy, and code — without turning the result sterile.

**A filter, not a style guide.** It rejects *technique without purpose*, not the techniques themselves.

&nbsp;

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE)
[![Version](https://img.shields.io/badge/version-2.0.1-6366f1?style=flat-square)](#)
[![skills.sh](https://img.shields.io/badge/skills.sh-muris11%2Fanti--ai--slop-111827?style=flat-square&logo=github)](https://www.skills.sh/muris11/anti-ai-slop)
[![GitHub stars](https://img.shields.io/github/stars/muris11/anti-ai-slop?style=flat-square)](https://github.com/muris11/anti-ai-slop)

**17 skills · one always-on filter · 7 agents · 3 platforms**

</div>

---

## Overview

`anti-ai-slop` is a **filter** for AI coding agents. It tells them to stop producing the *default AI look* — the purple gradient, the centered hero, the three identical cards, the "unlock the power" copy, the fake metrics — **without imposing a single fixed aesthetic.**

The core idea, in four words:

> **No hierarchy + no specificity + no restraint + no opinion.**

AI slop isn't any one technique. A gradient is fine. A card grid is fine. Inter is fine. **Slop is the unmarked combination** of generic defaults that repeat because nobody made a decision. The two tests used throughout:

1. **Purpose test** — can you write one honest sentence explaining why this technique serves *this* product?
2. **Convergence test** — does the same technique appear across unrelated screens for no reason?

---

## What's inside

**17 skills**, grouped as:

| Area | Skills |
|---|---|
| **Core filter** | `antislop` — always on |
| **Master catalog** | `antislop-master` — the P0–P6 indicator audit |
| **Visual & layout** | `antislop-ui` · `antislop-layout` · `antislop-imagery` · `antislop-designsystem` |
| **Copy & content** | `antislop-copywriting` · `antislop-authenticity` |
| **Product & UX** | `antislop-dashboard` · `antislop-forms` · `antislop-motion` · `antislop-nav` |
| **People & platform** | `antislop-human` · `antislop-layoutmobile` · `antislop-mobile` |
| **Code** | `antislop-code` |
| **Loader** | `slop` — loads the whole family at once |

### The master taxonomy

`antislop-master` is a **severity-tiered catalog** of ~180 indicators spanning color, typography, layout, components, copy, motion, UX states, authenticity, code, and platform. Every indicator is rated by how strong a signal it is:

| Tier | Meaning |
|---|---|
| **P0** | Instant AI tell — the single strongest signal |
| **P1** | Strong tell — individually loud, usually wrong |
| **P2** | Suspicious pattern — common AI default, may be earned |
| **P3** | Context dependent — only slop in the wrong context |
| **P4** | Quality / UX slop — shipping an incomplete experience |
| **P5** | Authenticity slop — fake data, claims, or evidence |
| **P6** | Code slop — sloppy implementation of the design |

The catalog also ships a **Quick / Full / Deep** audit protocol so you can scan at the depth the task needs.

---

## Install

`anti-ai-slop` is a set of standard agent skills (one folder per skill, each with a `SKILL.md`). Pick any path.

### 1. The picker (recommended)

One command, then choose which skills, where (project or global), and which agents.

```bash
npx antislop-ai
```

The picker installs the folders and **writes the session pointer** that loads the filter every session. This is the only path that writes the pointer automatically.

### 2. The skills directory

```bash
npx skills add muris11/anti-ai-slop
```

Add `--all` for every skill, `-g` for a global install, or `--skill <name>` for a single one. Run `--list` first.

> This path copies skill folders but does **not** write the session pointer. If you used it, follow with the picker (path 1) and choose **Keep what is there**.

### 3. The plugin (Claude Code)

```text
/plugin marketplace add https://github.com/muris11/anti-ai-slop
/plugin install antislop@anti-ai-slop
```

### 4. The plugin (Antigravity)

```bash
agy plugin install https://github.com/muris11/anti-ai-slop
```

### 5. Manual (single file)

```bash
curl -o antislop.md https://raw.githubusercontent.com/muris11/anti-ai-slop/main/antislop.md
```

```powershell
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/muris11/anti-ai-slop/main/antislop.md" -OutFile "antislop.md"
```

---

## Skills

| Skill | What it covers | Ships in |
|---|---|---|
| **antislop** | The always-on core filter: purpose test, rule tiers, Delivery Gate | v2.0.1 |
| **antislop-master** | The P0–P6 master taxonomy: ~180 indicators + audit protocol | v2.0.1 |
| **antislop-ui** | UI & visual: color, components, decoration, motion, structure | v2.0.1 |
| **antislop-layout** | Layout & composition: hero, sections, symmetry, grids, spacing | v2.0.1 |
| **antislop-copywriting** | Copy & text: headlines, CTAs, tone, anti-AI-writing patterns | v2.0.1 |
| **antislop-human** | People: contrast (with checker), keyboard, focus, states | v2.0.1 |
| **antislop-layoutmobile** | Mobile layout: breakpoints, grids, overflow, tap targets | v2.0.1 |
| **antislop-mobile** | Mobile & native: reflow, no overflow, 44px targets, Flutter | v2.0.1 |
| **antislop-dashboard** | Dashboard & data: metric cards, charts, tables, complete states | v2.0.1 |
| **antislop-forms** | Forms & states: validation, empty/loading/error/offline | v2.0.1 |
| **antislop-motion** | Motion: a UX reason, one focal animation, reduced-motion | v2.0.1 |
| **antislop-nav** | Navigation & chrome: real IA, no dead links, honest footer | v2.0.1 |
| **antislop-authenticity** | Authenticity: no fake metrics, testimonials, logos, or claims | v2.0.1 |
| **antislop-designsystem** | Design-system consistency: real tokens, spacing scale, theme parity | v2.0.1 |
| **antislop-imagery** | Imagery & decoration: illustrations, backgrounds, icons, media | v2.0.1 |
| **antislop-code** | Code comments: remove AI-slop comments, keep the valuable ones | v2.0.1 |
| **slop** | One-shot loader for the whole family at once | v2.0.1 |

---

## Agent support

| Agent | Skill folder | Picker | Plugin |
|---|---|---|---|
| Claude Code | `.claude/skills` | Yes | Yes (marketplace) |
| Antigravity | `.agents/skills` | Yes | Yes (`agy`) |
| Codex | `.codex/skills` | Yes | No |
| OpenCode | `.opencode/skills` | Yes | No |
| Cursor | `.cursor/skills` | Yes | No |
| Gemini CLI | `.gemini/skills` | Yes | No |
| Hermes | `~/.hermes/skills` (global) | Yes | No |

Every skill is a folder of the open **Agent Skills** standard (`<name>/SKILL.md`), so it drops into any agent that reads the standard. Works on **Windows, macOS, and Linux**.

---

## Usage modes

Two modes, chosen at the start of a session:

| Mode | When | Flow |
|---|---|---|
| **DURING** | building new work | apply rules while building, end with the Delivery Gate |
| **AFTER** | auditing finished work | numbered findings list → you approve → fix → re-report |

The core skill asks, *"When does this apply — during the work, or after it is done?"* before anything proceeds.

---

## Directory structure

```
anti-ai-slop/
├── antislop.md                  # standalone core rules (single-file path)
├── guide.md                     # getting-started guide
├── ROADMAP.md                   # release history
├── SECURITY.md                  # security boundaries
├── LICENSE
├── plugin.json                  # Antigravity plugin door
├── .claude-plugin/              # Claude Code marketplace plugin
├── rules/antislop.md            # session pointer for the Antigravity plugin
├── cli/                         # the `antislop-ai` npm picker
│   ├── index.mjs
│   └── lib/install.mjs          # multi-agent installer
└── skills/                      # the 17 skills
    ├── antislop/SKILL.md
    ├── antislop-master/SKILL.md
    └── ...
```

---

## Roadmap

See [ROADMAP.md](ROADMAP.md). Highlights: **v2.0.0** added the master taxonomy and nine focused skills; **v2.0.1** polished the README, finalized the license, and verified skills.sh indexing.

---

## FAQ

**Is anti-ai-slop a style guide?** No — a filter. It does not prescribe colors, fonts, or layouts. It rejects technique without purpose and requires liveliness. Direction is yours (`DESIGN.md`).

**Am I only allowed to use it for web pages?** No. It audits and writes interface, copy, mobile, Flutter, dashboards, code comments, and design systems.

**Is `Inter`, a gradient, or a card grid automatically slop?** No. Each is only a candidate when it appears as a default without a product reason (the purpose and convergence tests).

**Do I need `DESIGN.md`?** Yes for UI. The filter can remove slop but cannot invent direction; a sterile result means direction was missing, not that the filter failed.

---

## Contributing

Found a new AI slop pattern, a rule that misses something, or a bug in the installer? Open an issue. PRs are welcome for new patterns, clarifications, or checklist items out of sync with their rule.

---

## License

[MIT](LICENSE) © 2026 muris11. Do whatever you want with it.

---

<div align="center">

*Filter the slop. Keep the craft.*

</div>

---

# Versi Bahasa Indonesia

<div align="center">

# anti-ai-slop

**Anti Slop: Aturan untuk AI Coding Agent.**

Sebuah filter yang menghentikan AI agent menghasilkan UI, teks, dan kode **AI slop** yang generik — tanpa membuat hasilnya jadi kaku.

**Filter, bukan style guide.** Ia menolak *teknik tanpa tujuan*, bukan tekniknya itu sendiri.

**17 skill · satu filter selalu-aktif · 7 agent · 3 platform**

</div>

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

### 1. Picker (disarankan)

```bash
npx antislop-ai
```

Picker menginstal folder dan **menulis pointer sesi** yang memuat filter setiap sesi. Satu-satunya jalur yang menulis pointer otomatis.

### 2. Skills directory

```bash
npx skills add muris11/anti-ai-slop
```

Tambahkan `--all`, `-g`, atau `--skill <nama>`. Jalankan `--list` dulu.

> Jalur ini menyalin folder skill tapi **tidak** menulis pointer sesi. Kalau sudah pakai, lanjutkan dengan picker (jalur 1) dan pilih **Keep what is there**.

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
| **antislop** | Filter inti selalu-aktif: tes tujuan, tier aturan, Delivery Gate | v2.0.1 |
| **antislop-master** | Taksonomi master P0–P6: ~180 indikator + protokol audit | v2.0.1 |
| **antislop-ui** | UI & visual: warna, komponen, dekorasi, motion, struktur | v2.0.1 |
| **antislop-layout** | Layout & komposisi: hero, section, simetri, grid, spacing | v2.0.1 |
| **antislop-copywriting** | Teks & copy: headline, CTA, tone, pola anti-AI-writing | v2.0.1 |
| **antislop-human** | Manusia: kontras (dengan checker), keyboard, fokus, state | v2.0.1 |
| **antislop-layoutmobile** | Layout mobile: breakpoint, grid, overflow, tap target | v2.0.1 |
| **antislop-mobile** | Mobile & native: reflow, tanpa overflow, target 44px, Flutter | v2.0.1 |
| **antislop-dashboard** | Dashboard & data: metric card, chart, tabel, state lengkap | v2.0.1 |
| **antislop-forms** | Form & state: validasi, empty/loading/error/offline | v2.0.1 |
| **antislop-motion** | Motion: alasan UX, satu animasi fokus, reduced-motion | v2.0.1 |
| **antislop-nav** | Navigasi & chrome: IA nyata, tanpa dead link, footer jujur | v2.0.1 |
| **antislop-authenticity** | Autentisitas: tanpa metric, testimoni, logo, atau klaim palsu | v2.0.1 |
| **antislop-designsystem** | Konsistensi design system: token nyata, skala spacing, paritas tema | v2.0.1 |
| **antislop-imagery** | Imagery & dekorasi: ilustrasi, background, ikon, media | v2.0.1 |
| **antislop-code** | Komentar kode: hapus komentar AI-slop, pertahankan yang berharga | v2.0.1 |
| **slop** | Loader sekali-jalan untuk seluruh keluarga sekaligus | v2.0.1 |

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

Lihat [ROADMAP.md](ROADMAP.md). **v2.0.0** menambahkan taksonomi master dan sembilan skill fokus; **v2.0.1** merapikan README, memfinalisasi lisensi, dan memverifikasi indeks skills.sh.

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

[MIT](LICENSE) © 2026 muris11.

---

<div align="center">

*Filter slop-nya. Jaga kerapiannya.*

</div>
