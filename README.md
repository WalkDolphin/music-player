🇸🇦 [العربية](README.ar.md) · 🇩🇪 [Deutsch](README.de.md) · 🇬🇧 [English](README.md) · 🇪🇸 [Español](README.es.md) · 🇫🇷 [Français](README.fr.md) · 🇮🇳 [हिन्दी](README.hi.md) · 🇮🇹 [Italiano](README.it.md) · 🇯🇵 [日本語](README.ja.md) · 🇰🇭 [ភាសាខ្មែរ](README.km.md) · 🇰🇷 [한국어](README.ko.md) · 🇳🇱 [Nederlands](README.nl.md) · 🇳🇴 [Norsk](README.no.md) · 🇵🇱 [Polski](README.pl.md) · 🇵🇹 [Português](README.pt.md) · 🇷🇺 [Русский](README.ru.md) · 🇹🇭 [ไทย](README.th.md) · 🇹🇷 [Türkçe](README.tr.md) · 🇺🇦 [Українська](README.uk.md) · 🇨🇳 [简体中文](README.zh-CN.md) · 🇹🇼 [繁體中文](README.zh-TW.md)
# 🎵 The Music Player

> A pure HTML music player with vintage vinyl record interface, supporting 150+ global languages and nearly 50 regional dialects. **You can enjoy slow melodies with worldwide dialects in one HTML page.**

**Note: This project involves the participation of artificial intelligence in its creation.**

---

## ✨ Features

- 🎨 **Immersive vinyl record design** – spinning disc, tonearm animation, retro visual experience.
- 🌍 **150+ languages & 50 dialects** – including Wu, Cantonese, Hakka, Gan, Xiang, Jin, and more.
- 📂 **Drag & drop support** – just drag audio files (MP3/WAV/FLAC/OGG) or click "Add Music".
- 📝 **LRC lyrics sync** – import `.lrc` files, with highlighted scrolling and full-screen lyrics mode.
- 🎛️ **Full playback controls** – play/pause, next/prev, shuffle, repeat modes (none/all/one), and volume control.
- 📱 **Responsive** – works smoothly on desktop, tablet, and mobile.
- 🧩 **No external dependencies** – runs entirely in your browser, no installation required.

---

## 🚀 Quick Start

1. Download the `TheMusicPlayer.html` file.
2. Double-click to open it in any modern browser (Chrome, Edge, Firefox, etc.).
3. Click **"Add Music"** or drag and drop audio files into the window.
4. Click the **"Lyrics"** button to import a `.lrc` file for the current song.
5. Click the **gear icon (settings)** to switch fonts and interface languages.

---

### Detail

This music player is crafted to help users step away from hustle and bustle and embrace a soothing slow life accompanied by beautiful melodies. It comes with comprehensive localization support covering 150 global languages and close to 50 distinctive regional dialects. For the very first time, we've integrated an immersive vintage vinyl record visual design into the playback interface, bringing a more textured and nostalgic listening experience—feel free to download and try it out for yourself.

> **Design original intention:** My core inspiration stems from a simple wish to appreciate music in a relaxed, uncomplicated way. I opted to build this player purely with HTML technology, as it delivers universal compatibility across all personal computers. This way, every music lover can access and enjoy wonderful tunes without troublesome installation or complicated setup.

---

## 🛠️ Technical Notes

- Built with **pure HTML, CSS, and JavaScript** – no third-party libraries.
- Built-in **ID3v2 parser** (supports v2.3 and v2.4) extracts title, artist, album, and cover art.
- Uses **Audio API** and **Media Session API** for system-level media controls.
- All localization resources are embedded – no internet connection required to switch languages.

---

## 📁 Supported File Formats

### Audio Formats
The player can open and play the following audio file types (via the "Add Music" button or drag‑and‑drop):

- **MP3** (.mp3)
- **WAV** (.wav)
- **FLAC** (.flac)
- **OGG** (.ogg)
- Plus common formats like **M4A**, **AAC**, and **WMA** (depending on browser support).

> The player uses the browser's built‑in audio engine, so actual playback capability may vary slightly across browsers.

### Metadata Tags (ID3v2)
When you add an MP3 file (or any file that contains ID3v2.3 / v2.4 tags), the player automatically reads the following tags:

| Tag    | Meaning               | Displayed as         |
|--------|-----------------------|----------------------|
| TIT2   | Title                 | Song name            |
| TPE1   | Artist                | Artist name          |
| TALB   | Album                 | Album name           |
| TYER / TDRC | Year / Release date | Year / date        |
| TCOM   | Composer              | (falls back to artist) |
| TCON   | Genre                 | Genre                |
| TRCK   | Track number          | Track number         |
| TDAT   | Date                  | Date                 |
| APIC   | Attached picture      | Cover art (shown on vinyl label) |

If no ID3 tags are found, the player will try to parse the **filename** in the format `Artist - Title` (the last ` - ` is used as the separator).

### Lyrics Format (LRC)
You can import synchronized lyrics using standard **LRC** files (with the `.lrc` extension). The parser supports timestamps in the following formats:

- `[mm:ss.xx]` – minutes, seconds, and hundredths of a second
- `[mm:ss.xxx]` – minutes, seconds, and thousandths of a second

---

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 📬 Feedback & Support

If you encounter any problems while using this player, feel free to discuss with me on GitHub. Alternatively, you can also reach me via email: WalkDolphin [at] outlook [dot] com