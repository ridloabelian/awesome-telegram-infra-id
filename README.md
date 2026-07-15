<div align="center">

<img src="https://raw.githubusercontent.com/telegramdesktop/tdesktop/dev/Telegram/Resources/art/icon256.png" alt="Telegram Logo" width="130" />

<h1 align="center">Kitab Telegram ✈️ 🇮🇩<br><sub>(Infra Nol Rupiah)</sub></h1>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1000&color=229ED9&center=true&vCenter=true&width=640&lines=Bukan+Cuma+Chat%2C+Tapi+Infrastruktur;Penyimpanan+File+Eksperimental;Bot+%3D+Backend+%2B+CRM+%2B+Notifikasi;Bangun+Bisnis+Modal+Rp+0" alt="Typing SVG" />
</p>

Kumpulan *library*, *bot framework*, template, dan proyek *open-source* terbaik yang menjadikan **Telegram sebagai lapisan komunikasi berbiaya rendah** — bukan sekadar aplikasi chat, tapi webhook, penyimpanan file berbasis platform, CRM ringan, dan gateway notifikasi bermodal Rp 0.
Dibangun untuk solopreneur & developer Indonesia, di mana Telegram sudah jadi napas sehari-hari.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![Stars](https://img.shields.io/github/stars/ridloabelian/awesome-telegram-infra-id?style=flat&color=229ED9)](https://github.com/ridloabelian/awesome-telegram-infra-id/stargazers)
[![Last Commit](https://img.shields.io/github/last-commit/ridloabelian/awesome-telegram-infra-id?style=flat&color=229ED9)](https://github.com/ridloabelian/awesome-telegram-infra-id/commits/main)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat)](CONTRIBUTING.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat)](LICENSE)

</div>

> **Audit:** Terakhir diverifikasi **2026-07-15**. Kuota dan kebijakan dapat berubah; cek [sumber resmi](https://core.telegram.org/bots/faq) sebelum implementasi.
>
> **Disclaimer:** Proyek komunitas independen. Tidak berafiliasi dengan atau didukung oleh Telegram. Telegram dan logonya merupakan merek dagang pemiliknya. Patuhi Bot API Terms dan hindari spam/userbot abuse.

> 🗺️ **Bagian dari seri [Stack Nol Rupiah](https://github.com/ridloabelian/awesome-rp0-id)** — peta lengkap bootstrap gratisan Rp 0 untuk indie hacker Indonesia.

> 🔗 **Seri saudara:** [**Kitab Cloudflare**](https://github.com/ridloabelian/awesome-cloudflare-id) (edge/web) · [**Kitab Google**](https://github.com/ridloabelian/awesome-google-free-id) (automasi bisnis) · [**Kitab Supabase**](https://github.com/ridloabelian/awesome-supabase-id) (database/auth) · [**Kitab Oracle Cloud**](https://github.com/ridloabelian/awesome-oracle-free-id) (compute/self-hosting). **Telegram melengkapi semuanya sebagai lapisan komunikasi, notifikasi, Mini Apps, dan pengiriman file non-kritis.**

Telegram Bot API dapat digunakan gratis dengan **rate limit platform**, sementara file Telegram dapat membantu penyimpanan/pengiriman file non-kritis. Kombinasi ini berguna untuk webhook, CRM ringan, publikasi channel, dan notifikasi — tetapi bukan pengganti database atau object storage produksi. Cocok banget untuk pasar Indonesia yang aktivitas bisnisnya banyak berpusat di chat.

**Kriteria Kurasi:**
- Menjadikan Telegram sebagai *tools* produktivitas, backend, atau infrastruktur.
- Gratis dijalankan (Bot API gratis; hosting bisa serverless/free tier).
- *Open-source* dan idealnya masih aktif di-*maintain*.
- Relevan untuk solopreneur & developer Indonesia.


**Status kurasi:** `Official` = dikelola vendor/organisasi resmi · `Community` = proyek komunitas · `Experimental` = contoh/POC, audit sebelum produksi · `Archived` = read-only/tidak aktif. Lihat [audit katalog lengkap](CATALOG_AUDIT.md) (status, stars, last push, dan sumber README upstream; diverifikasi 2026-07-15).

---

## 💰 Kenapa Telegram = Infra Rp 0?

| Kapabilitas | Bagaimana | Batas |
|-------------|-----------|-------|
| **Bot API** | Webhook, command, inline | Gratis dengan [rate limit resmi](https://core.telegram.org/bots/faq#my-bot-is-hitting-limits-how-do-i-avoid-this) |
| **Penyimpanan file** | Kirim file ke bot/channel | Tunduk pada batas ukuran, akun, dan kebijakan Telegram; tanpa SLA storage |
| **Distribusi file** | `getFile` untuk pengambilan oleh backend | URL mengandung token bot; wajib diproksi, jangan dipublikasikan |
| **CRM ringan / log** | Pesan privat sebagai append-only log | Eksperimental; bukan database, tanpa query/transaksi/SLA |
| **CMS** | Channel + Instant View sebagai publikasi | Gratis |
| **Notifikasi** | Push alert instan ke HP via bot | Gratis, realtime |
| **Mini Apps** | Web app penuh di dalam Telegram | Gratis (hosting sendiri) |

> ⚠️ **Catatan:** Bot API-nya gratis, tapi **kode bot tetap perlu tempat berjalan**. Untuk benar-benar Rp 0, deploy webhook bot di **Cloudflare Workers** atau **Google Apps Script** (lihat repo saudara). Jangan simpan data sensitif tanpa enkripsi di channel — ini bukan pengganti database aman untuk data kritikal.

---

## Daftar Isi
- [💰 Kenapa Telegram = Infra Rp 0?](#-kenapa-telegram--infra-rp-0)
- [⚙️ Bot Framework (Node.js)](#️-bot-framework-nodejs)
- [🐍 Bot Framework (Python)](#-bot-framework-python)
- [☁️ Bot Serverless (Rp 0 Hosting)](#️-bot-serverless-rp-0-hosting)
- [💾 Telegram sebagai Storage & Drive](#-telegram-sebagai-storage--drive)
- [🖼️ Telegram sebagai CDN Gambar](#️-telegram-sebagai-cdn-gambar)
- [🤖 Bot AI (ChatGPT/Gemini)](#-bot-ai-chatgptgemini)
- [📱 Mini Apps (Web App)](#-mini-apps-web-app)
- [📚 Referensi](#-referensi)
- [📄 Template Siap Pakai](#-template-siap-pakai)

---

## ⚙️ Bot Framework (Node.js)
Kerangka kerja untuk membangun bot Telegram dengan JavaScript/TypeScript.

| Nama | Deskripsi |
|------|-----------|
| [telegraf/telegraf](https://github.com/telegraf/telegraf) ![](https://img.shields.io/github/stars/telegraf/telegraf?style=flat&label=%E2%98%85&color=229ED9) | *Bot framework* modern paling populer untuk Node.js. Lengkap, matang, dan banyak dipakai di produksi. |
| [grammyjs/grammY](https://github.com/grammyjs/grammY) ![](https://img.shields.io/github/stars/grammyjs/grammY?style=flat&label=%E2%98%85&color=229ED9) | *Bot framework* generasi baru untuk TypeScript. Cepat, ringan, *plugin ecosystem* kaya, dan jalan mulus di serverless. |
| [bot-base/telegram-bot-template](https://github.com/bot-base/telegram-bot-template) ![](https://img.shields.io/github/stars/bot-base/telegram-bot-template?style=flat&label=%E2%98%85&color=229ED9) | Template bot siap pakai berbasis grammY dengan struktur proyek yang rapi. |

## 🐍 Bot Framework (Python)
Untuk pengguna Python — dari Bot API sederhana hingga MTProto (akun user).

| Nama | Deskripsi |
|------|-----------|
| [python-telegram-bot/python-telegram-bot](https://github.com/python-telegram-bot/python-telegram-bot) ![](https://img.shields.io/github/stars/python-telegram-bot/python-telegram-bot?style=flat&label=%E2%98%85&color=229ED9) | Library Python paling populer & terlengkap untuk Bot API. Dokumentasi luar biasa, komunitas besar. |
| [LonamiWebs/Telethon](https://github.com/LonamiWebs/Telethon) ![](https://img.shields.io/github/stars/LonamiWebs/Telethon?style=flat&label=%E2%98%85&color=229ED9) | Library MTProto murni — bisa untuk bot maupun **akun user** (userbot). Untuk automasi tingkat lanjut & akses fitur penuh. |
| [pyrogram/pyrogram](https://github.com/pyrogram/pyrogram) ![](https://img.shields.io/github/stars/pyrogram/pyrogram?style=flat&label=%E2%98%85&color=229ED9) | Framework MTProto async yang elegan dan modern. Alternatif Telethon yang populer untuk userbot & bot. |

## ☁️ Bot Serverless (Rp 0 Hosting)
Deploy bot tanpa server/VPS — jalan di Cloudflare Workers, benar-benar gratis 24 jam.

| Nama | Deskripsi |
|------|-----------|
| [cvzi/telegram-bot-cloudflare](https://github.com/cvzi/telegram-bot-cloudflare) ![](https://img.shields.io/github/stars/cvzi/telegram-bot-cloudflare?style=flat&label=%E2%98%85&color=229ED9) | Contoh minimal bot Telegram di Cloudflare Workers. Titik awal terbaik untuk bot serverless Rp 0. |
| [tuanpb99/cf-worker-telegram](https://github.com/tuanpb99/cf-worker-telegram) ![](https://img.shields.io/github/stars/tuanpb99/cf-worker-telegram?style=flat&label=%E2%98%85&color=229ED9) | Cloudflare Worker sebagai *proxy transparan* untuk Telegram Bot API — berguna jika API Telegram terblokir di suatu wilayah. |
| [telegrambotindonesia/GAS-Lib-v3](https://github.com/telegrambotindonesia/GAS-Lib-v3) ![](https://img.shields.io/github/stars/telegrambotindonesia/GAS-Lib-v3?style=flat&label=%E2%98%85&color=229ED9) | Library Google Apps Script untuk Bot API buatan komunitas Indonesia. Bikin bot gratis di Apps Script tanpa VPS. |

## 💾 Penyimpanan File Berbasis Telegram (Eksperimental)
Eksperimen memanfaatkan file Telegram sebagai penyimpanan non-kritis. **Bukan pengganti Drive/S3/R2**, tidak memiliki SLA, dan tunduk pada kebijakan platform.

| Nama | Deskripsi |
|------|-----------|
| [caamer20/Telegram-Drive](https://github.com/caamer20/Telegram-Drive) ![](https://img.shields.io/github/stars/caamer20/Telegram-Drive?style=flat&label=%E2%98%85&color=229ED9) | Ubah akun Telegram menjadi *cloud storage* aman tak terbatas dengan antarmuka layaknya Drive. Open-source. |
| [ebinxavier/telegramCloudStorage](https://github.com/ebinxavier/telegramCloudStorage) ![](https://img.shields.io/github/stars/ebinxavier/telegramCloudStorage?style=flat&label=%E2%98%85&color=229ED9) | Alternatif Google Drive berbasis Telegram — upload & kelola file memanfaatkan storage Telegram. |

## 🖼️ Distribusi Gambar via Proxy Aman
Distribusikan gambar melalui backend/proxy yang menyembunyikan token. Jangan gunakan URL Bot API bertoken sebagai URL publik.

| Nama | Deskripsi |
|------|-----------|
| [missuo/Telegraph-Image-Hosting](https://github.com/missuo/Telegraph-Image-Hosting) ![](https://img.shields.io/github/stars/missuo/Telegraph-Image-Hosting?style=flat&label=%E2%98%85&color=229ED9) | Bangun *image hosting* berbasis Telegraph (layanan Telegram). Tunduk pada batas dan kebijakan platform, cocok untuk aset web. |

## 🤖 Bot AI (ChatGPT/Gemini)
Jadikan bot Telegram sebagai antarmuka AI pribadi Anda.

| Nama | Deskripsi |
|------|-----------|
| [tbxark/ChatGPT-Telegram-Workers](https://github.com/tbxark/ChatGPT-Telegram-Workers) ![](https://img.shields.io/github/stars/tbxark/ChatGPT-Telegram-Workers?style=flat&label=%E2%98%85&color=229ED9) | Deploy bot ChatGPT Telegram dengan mudah di Cloudflare Workers (atau Vercel/Docker). Multi-model, serverless, Rp 0. |
| [yym68686/ChatGPT-Telegram-Bot](https://github.com/yym68686/ChatGPT-Telegram-Bot) ![](https://img.shields.io/github/stars/yym68686/ChatGPT-Telegram-Bot?style=flat&label=%E2%98%85&color=229ED9) | Bot AI chat Telegram dengan kemampuan Web Search, DALL·E, dan dukungan multi-model. |
| [snakeying/GPT-Telegram-Worker](https://github.com/snakeying/GPT-Telegram-Worker) ![](https://img.shields.io/github/stars/snakeying/GPT-Telegram-Worker?style=flat&label=%E2%98%85&color=229ED9) | Bot AI multi-model di Cloudflare Workers yang mendukung berbagai penyedia LLM. |

## 📱 Mini Apps (Web App)
Bangun aplikasi web penuh yang berjalan di dalam Telegram.

| Nama | Deskripsi |
|------|-----------|
| [revenkroz/telegram-web-app-bot-example](https://github.com/revenkroz/telegram-web-app-bot-example) ![](https://img.shields.io/github/stars/revenkroz/telegram-web-app-bot-example?style=flat&label=%E2%98%85&color=229ED9) | Contoh lengkap Telegram Mini App (Web App) untuk bot. Titik awal membangun aplikasi in-app. |
| [deptyped/notepher-bot](https://github.com/deptyped/notepher-bot) ![](https://img.shields.io/github/stars/deptyped/notepher-bot?style=flat&label=%E2%98%85&color=229ED9) | Mini App pencatat (note-taking) di dalam Telegram. Contoh implementasi Mini App yang nyata & berguna. |

## 📚 Referensi
Kumpulan sumber daya dan awesome-list Telegram terbesar.

| Nama | Deskripsi |
|------|-----------|
| [ebertti/awesome-telegram](https://github.com/ebertti/awesome-telegram) ![](https://img.shields.io/github/stars/ebertti/awesome-telegram?style=flat&label=%E2%98%85&color=229ED9) | Koleksi besar grup, channel, bot, dan library Telegram terbaik. Rujukan utama (berbahasa Inggris). |
| [DenisIzmaylov/awesome-telegram-bots](https://github.com/DenisIzmaylov/awesome-telegram-bots) ![](https://img.shields.io/github/stars/DenisIzmaylov/awesome-telegram-bots?style=flat&label=%E2%98%85&color=229ED9) | Kumpulan contoh, library, dan *starter-kit* khusus untuk pengembangan Bot Telegram. |

## 📄 Template Siap Pakai
Pola paling umum untuk memakai Telegram sebagai infra. Buat bot via [@BotFather](https://t.me/botfather) untuk dapat `TOKEN`.

### 1. Kirim Notifikasi ke HP (dari script apa pun)
```bash
# Paling sederhana: alert dari server/cron/CI ke Telegram Anda. Ganti TOKEN & CHAT_ID.
curl -s "https://api.telegram.org/bot<TOKEN>/sendMessage" \
  -d chat_id="<CHAT_ID>" \
  -d text="🔔 Deploy sukses! Server online ✅"

# Cara dapat CHAT_ID: kirim pesan ke bot Anda, lalu buka:
# https://api.telegram.org/bot<TOKEN>/getUpdates  -> lihat field "chat":{"id":...}
```

### 2. Pengambilan File via Proxy Aman (token tetap rahasia)
```bash
# Backend mengambil file_path dengan TOKEN yang disimpan sebagai secret:
curl -s "https://api.telegram.org/bot<TOKEN>/getFile?file_id=<FILE_ID>"

# PENTING: endpoint file Telegram mengandung BOT_TOKEN.
# Jangan pernah kirim URL tersebut ke browser/user atau menyimpannya di HTML/log publik.
# Buat endpoint proxy Cloudflare Worker/server Anda sendiri yang:
# 1) menerima ID internal yang sudah divalidasi,
# 2) mengambil file dengan TOKEN dari secret/env,
# 3) mengalirkan bytes ke pengguna,
# 4) menerapkan auth, allowlist, rate limit, dan cache bila diperlukan.
```

### 3. Bot Sederhana di Cloudflare Worker (webhook, Rp 0)
```javascript
// Deploy di Cloudflare Workers. Set env TOKEN. Daftarkan webhook sekali:
// https://api.telegram.org/bot<TOKEN>/setWebhook?url=<URL_WORKER_ANDA>
export default {
  async fetch(request, env) {
    if (request.method !== 'POST') return new Response('OK');
    const update = await request.json();
    const msg = update.message;
    if (msg?.text) {
      await fetch(`https://api.telegram.org/bot${env.TOKEN}/sendMessage`, {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ chat_id: msg.chat.id, text: `Anda bilang: ${msg.text}` })
      });
    }
    return new Response('OK');
  }
};
```

### 4. Channel sebagai Append-only Log Eksperimental (bukan database)
```javascript
// Hanya untuk log non-kritis/eksperimen. Jangan gunakan untuk PII, transaksi, antrean, atau source of truth.
// Untuk data aplikasi gunakan D1, Supabase, PostgreSQL, atau database lain yang punya query, backup, dan SLA.
async function simpanData(token, channelId, data) {
  await fetch(`https://api.telegram.org/bot${token}/sendMessage`, {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ chat_id: channelId, text: JSON.stringify(data) })
  });
}
// Jangan bergantung pada getUpdates sebagai mekanisme pembacaan database/riwayat permanen.
```

---

## 🤝 Kontribusi
Menemukan *tools* Telegram menarik lainnya? Silakan buat *Pull Request*! Baca dulu [panduan kontribusi](CONTRIBUTING.md).

<a href="https://github.com/ridloabelian/awesome-telegram-infra-id/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ridloabelian/awesome-telegram-infra-id" alt="Contributors" />
</a>

## 📜 Lisensi
Lisensi MIT - [Ridlo Abelian](https://github.com/ridloabelian)

---

<div align="center">

<a href="#kitab-telegram--">⬆️ Kembali ke Atas</a>

</div>
