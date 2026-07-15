<div align="center">

<img src="https://raw.githubusercontent.com/telegramdesktop/tdesktop/dev/Telegram/Resources/art/icon256.png" alt="Telegram Logo" width="130" />

<h1 align="center">Kitab Telegram ✈️ 🇮🇩<br><sub>(Infra Nol Rupiah)</sub></h1>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1000&color=229ED9&center=true&vCenter=true&width=640&lines=Bukan+Cuma+Chat%2C+Tapi+Infrastruktur;Storage+Unlimited+Gratis;Bot+%3D+Backend+%2B+CRM+%2B+Notifikasi;Bangun+Bisnis+Modal+Rp+0" alt="Typing SVG" />
</p>

Kumpulan *library*, *bot framework*, template, dan proyek *open-source* terbaik yang menjadikan **Telegram sebagai infrastruktur gratis** — bukan sekadar aplikasi chat, tapi *backend*, *storage*, CDN, CRM, dan gateway notifikasi bermodal Rp 0.
Dibangun untuk solopreneur & developer Indonesia, di mana Telegram sudah jadi napas sehari-hari.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![Stars](https://img.shields.io/github/stars/ridloabelian/awesome-telegram-infra-id?style=flat&color=229ED9)](https://github.com/ridloabelian/awesome-telegram-infra-id/stargazers)
[![Last Commit](https://img.shields.io/github/last-commit/ridloabelian/awesome-telegram-infra-id?style=flat&color=229ED9)](https://github.com/ridloabelian/awesome-telegram-infra-id/commits/main)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat)](CONTRIBUTING.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat)](LICENSE)

</div>

> 🔗 **Seri saudara:** [**Kitab Cloudflare**](https://github.com/ridloabelian/awesome-cloudflare-id) (edge/web) · [**Kitab Google**](https://github.com/ridloabelian/awesome-google-free-id) (automasi bisnis) · [**Kitab Supabase**](https://github.com/ridloabelian/awesome-supabase-id) (database/auth). **Telegram melengkapi semuanya sebagai lapisan komunikasi, notifikasi, & storage gratis.**

Telegram Bot API **100% gratis tanpa batas**, dan setiap akun mendapat penyimpanan file praktis tak terbatas. Kombinasi ini bikin Telegram jadi "cheat code" infrastruktur: bot bisa jadi *backend* & CRM, channel jadi CMS, dan file API jadi CDN gambar gratis. Cocok banget untuk pasar Indonesia yang aktivitas bisnisnya banyak berpusat di chat.

**Kriteria Kurasi:**
- Menjadikan Telegram sebagai *tools* produktivitas, backend, atau infrastruktur.
- Gratis dijalankan (Bot API gratis; hosting bisa serverless/free tier).
- *Open-source* dan idealnya masih aktif di-*maintain*.
- Relevan untuk solopreneur & developer Indonesia.

---

## 💰 Kenapa Telegram = Infra Rp 0?

| Kapabilitas | Bagaimana | Batas |
|-------------|-----------|-------|
| **Bot API** | Backend, webhook, command, inline | Gratis total, tanpa kuota resmi |
| **Storage File** | Kirim file ke bot/channel/"Saved Messages" | Praktis unlimited; 2 GB/file (4 GB via MTProto) |
| **CDN Gambar** | `getFile` menghasilkan URL publik CDN Telegram | Gratis |
| **CRM / Database** | Simpan data di channel privat / pesan | Gratis (untuk skala kecil-menengah) |
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

## 💾 Telegram sebagai Storage & Drive
Ubah akun Telegram menjadi cloud storage tak terbatas — pengganti Google Drive/Dropbox.

| Nama | Deskripsi |
|------|-----------|
| [caamer20/Telegram-Drive](https://github.com/caamer20/Telegram-Drive) ![](https://img.shields.io/github/stars/caamer20/Telegram-Drive?style=flat&label=%E2%98%85&color=229ED9) | Ubah akun Telegram menjadi *cloud storage* aman tak terbatas dengan antarmuka layaknya Drive. Open-source. |
| [ebinxavier/telegramCloudStorage](https://github.com/ebinxavier/telegramCloudStorage) ![](https://img.shields.io/github/stars/ebinxavier/telegramCloudStorage?style=flat&label=%E2%98%85&color=229ED9) | Alternatif Google Drive berbasis Telegram — upload & kelola file memanfaatkan storage Telegram. |

## 🖼️ Telegram sebagai CDN Gambar
Host gambar gratis tanpa batas bandwidth memanfaatkan CDN Telegram/Telegraph.

| Nama | Deskripsi |
|------|-----------|
| [missuo/Telegraph-Image-Hosting](https://github.com/missuo/Telegraph-Image-Hosting) ![](https://img.shields.io/github/stars/missuo/Telegraph-Image-Hosting?style=flat&label=%E2%98%85&color=229ED9) | Bangun *image hosting* gratis memanfaatkan Telegraph (layanan Telegram). Tanpa batas, cocok untuk aset web. |

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

### 2. Telegram sebagai CDN Gambar (upload → URL publik)
```bash
# Upload gambar ke bot, dapat file_id
curl -s "https://api.telegram.org/bot<TOKEN>/sendPhoto" \
  -F chat_id="<CHAT_ID>" -F photo=@"gambar.jpg"
# Response berisi "file_id". Lalu tukar jadi URL CDN:
# 1) https://api.telegram.org/bot<TOKEN>/getFile?file_id=<FILE_ID>  -> dapat "file_path"
# 2) URL publik CDN: https://api.telegram.org/file/bot<TOKEN>/<file_path>
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

### 4. Telegram sebagai Database Sederhana (channel privat)
```javascript
// Simpan "record" sebagai pesan JSON di channel privat (bot harus jadi admin channel).
// Cocok untuk log, antrian, atau data kecil yang tidak sensitif.
async function simpanData(token, channelId, data) {
  await fetch(`https://api.telegram.org/bot${token}/sendMessage`, {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ chat_id: channelId, text: JSON.stringify(data) })
  });
}
// Baca kembali via getUpdates / getChatHistory (MTProto) lalu JSON.parse tiap pesan.
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
