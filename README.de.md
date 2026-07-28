🇸🇦 [العربية](README.ar.md) · 🇩🇪 [Deutsch](README.de.md) · 🇬🇧 [English](README.md) · 🇪🇸 [Español](README.es.md) · 🇫🇷 [Français](README.fr.md) · 🇮🇳 [हिन्दी](README.hi.md) · 🇮🇹 [Italiano](README.it.md) · 🇯🇵 [日本語](README.ja.md) · 🇰🇭 [ភាសាខ្មែរ](README.km.md) · 🇰🇷 [한국어](README.ko.md) · 🇳🇱 [Nederlands](README.nl.md) · 🇳🇴 [Norsk](README.no.md) · 🇵🇱 [Polski](README.pl.md) · 🇵🇹 [Português](README.pt.md) · 🇷🇺 [Русский](README.ru.md) · 🇹🇭 [ไทย](README.th.md) · 🇹🇷 [Türkçe](README.tr.md) · 🇺🇦 [Українська](README.uk.md) · 🇨🇳 [简体中文](README.zh-CN.md) · 🇹🇼 [繁體中文](README.zh-TW.md)
# 🎵 Der Musikplayer

> Ein reiner HTML-Musikplayer mit Vintage-Schallplatten-Oberfläche, der mehr als 150 Sprachen und fast 50 regionale Dialekte unterstützt. **Genießen Sie auf einer einzigen HTML-Seite langsame Melodien mit Dialekten aus aller Welt.**

**Hinweis: Dieses Projekt wurde unter Beteiligung künstlicher Intelligenz erstellt.**

---

## ✨ Funktionen

- 🎨 **Immersives Vinyl-Design** – rotierende Platte, Tonarm-Animation, retro-optisches Erlebnis.
- 🌍 **Über 150 Sprachen und 50 Dialekte** – darunter Wu, Kantonesisch, Hakka, Gan, Xiang, Jin und weitere.
- 📂 **Drag & Drop-Unterstützung** – ziehen Sie Audiodateien (MP3/WAV/FLAC/OGG) oder klicken Sie auf „Musik hinzufügen“.
- 📝 **LRC-Textsynchronisation** – importieren Sie `.lrc`-Dateien mit hervorgehobenem Scrollen und Vollbild-Textmodus.
- 🎛️ **Vollständige Wiedergabesteuerung** – Wiedergabe/Pause, vorheriger/nächster Titel, Zufallswiedergabe, Wiederholungsmodi (keine/alle/einen) und Lautstärkeregelung.
- 📱 **Responsive** – funktioniert nahtlos auf Desktop, Tablet und Mobilgeräten.
- 🧩 **Keine externen Abhängigkeiten** – läuft vollständig im Browser, keine Installation erforderlich.

---

## 🚀 Schnellstart

1. Laden Sie die Datei `TheMusicPlayer.html` herunter.
2. Öffnen Sie sie mit einem **Doppelklick** in einem beliebigen modernen Browser (Chrome, Edge, Firefox usw.).
3. Klicken Sie auf **„Musik hinzufügen“** oder ziehen Sie Audiodateien in das Fenster.
4. Klicken Sie auf die Schaltfläche **„Texte“**, um eine `.lrc`-Datei für den aktuellen Song zu importieren.
5. Klicken Sie auf das **Zahnradsymbol (Einstellungen)**, um Schriftart und Oberflächensprache zu ändern.

---

### Detail

Dieser Musikplayer wurde entwickelt, um Nutzern zu helfen, dem Alltagsstress zu entfliehen und ein entschleunigtes, entspanntes Leben in Begleitung schöner Melodien zu genießen. Er bietet umfassende Lokalisierungsunterstützung für 150 Sprachen und fast 50 einzigartige regionale Dialekte. Erstmals haben wir ein immersives Vintage-Schallplatten-Design in die Wiedergabeoberfläche integriert, das ein noch taktileres und nostalgisches Hörerlebnis schafft. Laden Sie ihn herunter und probieren Sie es selbst aus.

> **Gestaltungsabsicht:** Meine Kerninspiration entspringt dem einfachen Wunsch, Musik auf eine entspannte, unkomplizierte Weise zu genießen. Ich habe mich für reine HTML-Technologie entschieden, weil sie universelle Kompatibilität auf allen Personalcomputern bietet. Auf diese Weise kann jeder Musikliebhaber ohne lästige Installation oder komplizierte Einrichtung auf wundervolle Melodien zugreifen und sie genießen.

---

## 🛠️ Technische Hinweise

- Erstellt mit **reinem HTML, CSS und JavaScript** – ohne Drittanbieter-Bibliotheken.
- Integrierter **ID3v2-Parser** (unterstützt v2.3 und v2.4) extrahiert Titel, Interpret, Album und Coverbild.
- Verwendet die **Audio-API** und **Media Session API** für die Mediensteuerung auf Systemebene.
- Alle Lokalisierungsressourcen sind eingebettet – für den Sprachwechsel ist keine Internetverbindung erforderlich.

---

## 📁 Unterstützte Dateiformate

### Audioformate
Der Player kann die folgenden Audiodateitypen öffnen und abspielen (über die Schaltfläche „Musik hinzufügen“ oder per Drag & Drop):

- **MP3** (.mp3)
- **WAV** (.wav)
- **FLAC** (.flac)
- **OGG** (.ogg)
- Sowie gängige Formate wie **M4A**, **AAC** und **WMA** (je nach Browserunterstützung).

> Der Player verwendet die integrierte Audio-Engine des Browsers, daher kann die tatsächliche Wiedergabefähigkeit je nach Browser leicht variieren.

### Metadaten-Tags (ID3v2)
Wenn Sie eine MP3-Datei (oder eine Datei mit ID3v2.3-/v2.4-Tags) hinzufügen, liest der Player automatisch die folgenden Tags:

| Tag         | Bedeutung                    | Anzeige als              |
|-------------|------------------------------|--------------------------|
| TIT2        | Titel                        | Songname                 |
| TPE1        | Interpret                    | Interpretenname          |
| TALB        | Album                        | Albumname                |
| TYER / TDRC | Jahr / Veröffentlichungsdatum | Jahr / Datum            |
| TCOM        | Komponist                    | (keine separate Anzeige, fällt auf Interpret zurück) |
| TCON        | Genre                        | Genre                    |
| TRCK        | Titelnummer                  | Titelnummer              |
| TDAT        | Datum                        | Datum                    |
| APIC        | Angehängtes Bild             | Cover auf dem Schallplattenetikett |

Wenn keine ID3-Tags gefunden werden, versucht der Player, den **Dateinamen** im Format `Interpret - Titel` zu analysieren (das letzte ` - ` wird als Trennzeichen verwendet).

### Textformat (LRC)
Sie können standardmäßige synchronisierte **LRC**-Textdateien (mit der Erweiterung `.lrc`) importieren. Der Parser unterstützt Zeitstempel in den folgenden Formaten:

- `[mm:ss.xx]` – Minuten, Sekunden und Hundertstelsekunden
- `[mm:ss.xxx]` – Minuten, Sekunden und Tausendstelsekunden

Der Player hebt die aktuelle Textzeile während der Wiedergabe in Echtzeit hervor, und Sie können auf jede Zeile klicken, um zu diesem Zeitstempel zu springen.

So importieren Sie eine LRC-Datei: Klicken Sie im Player auf die Schaltfläche **„Texte“** und wählen Sie **„Texte importieren“**; oder ziehen Sie während der Wiedergabe des entsprechenden Songs die `.lrc`-Datei direkt auf die Seite.

---

Dieses Projekt ist unter der MIT-Lizenz lizenziert - siehe die Datei [LICENSE](LICENSE) für Details.

---

## 📬 Feedback und Unterstützung

Wenn Sie bei der Verwendung dieses Players auf Probleme stoßen, können Sie sich gerne mit mir auf GitHub austauschen. Alternativ können Sie mich auch per E-Mail kontaktieren:  
WalkDolphin [at] outlook [dot] com