# Inkroom 🖊️

**Your own private PDF reading, highlighting & notes app.** Open PDFs, highlight in colour, underline, strike through, attach notes — everything stays on your device. No accounts, no tracking, no cloud.

Once installed (see below), Inkroom works **fully offline** — perfect for reading on planes, trains and anywhere without Wi-Fi.

---

## ✨ Features

- 📄 **Open any PDF** — readings, papers, lecture slides
- 🌈 **9 highlight colours** (bright + pastel) and 3 styles: highlight, underline, strike-through
- 🔍 **Full-text search** across the whole document, with jump-to-result
- 📝 **Notes** attached to each highlight or underline
- 🗂️ **File library** — every document you've marked, with reading-progress bars
- ↩️ **Undo / redo** (Ctrl+Z / Ctrl+Y)
- 🌗 **Dark & light themes** (press `T`)
- 📖 **Outline / table of contents** sidebar for PDFs that include one
- ⏱️ **Remembers your last page** — reopen a PDF and continue where you left off
- 🎯 **Focus mode** (`F`) hides the sidebar for distraction-free reading
- 💾 **Backup export / import** — move your highlights between devices as a JSON file
- 📲 **Installable PWA** — works offline after the first visit

## 🚀 Using the app

Open the live app here:

**→ https://jmikropoulos-svg.github.io/inkroom/**

Then **install it like a normal app**:

- **Chrome / Edge (desktop):** click the install icon in the address bar, or the "Install as app" button in the app sidebar
- **iPhone / iPad:** Share → *Add to Home Screen*
- **Android:** menu → *Install app*

## 🔒 Where are my highlights?

Everything (highlights, notes, progress, theme) is stored in your browser's local storage at the address you installed the app from — nothing is ever uploaded.

To move highlights between devices or browsers, use **Export backup** in the sidebar and **Import backup** on the other device.

## 🛠️ Tech notes

- Single-page app; PDF rendering by [pdf.js](https://mozilla.github.io/pdf.js/) (bundled in `lib/`, so it works offline)
- `sw.js` — the service worker that caches the app for offline use
- `manifest.webmanifest` — install/app info
- `icons/` — app icons, rebuilt automatically from base64 sources by a GitHub Action

## 📂 Repo structure

```
index.html            the app (everything in one page)
sw.js                 offline cache ("service worker")
manifest.webmanifest  app name + icons
lib/                  PDF engine (bundled, no CDN needed)
icons/                app icons
.github/workflows/    rebuilds the icons from base64 sources
```
