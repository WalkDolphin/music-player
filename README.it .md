🇸🇦 [العربية](README.ar.md) · 🇩🇪 [Deutsch](README.de.md) · 🇬🇧 [English](README.md) · 🇪🇸 [Español](README.es.md) · 🇫🇷 [Français](README.fr.md) · 🇮🇳 [हिन्दी](README.hi.md) · 🇮🇹 [Italiano](README.it.md) · 🇯🇵 [日本語](README.ja.md) · 🇰🇭 [ភាសាខ្មែរ](README.km.md) · 🇰🇷 [한국어](README.ko.md) · 🇳🇱 [Nederlands](README.nl.md) · 🇳🇴 [Norsk](README.no.md) · 🇵🇱 [Polski](README.pl.md) · 🇵🇹 [Português](README.pt.md) · 🇷🇺 [Русский](README.ru.md) · 🇹🇭 [ไทย](README.th.md) · 🇹🇷 [Türkçe](README.tr.md) · 🇺🇦 [Українська](README.uk.md) · 🇨🇳 [简体中文](README.zh-CN.md) · 🇹🇼 [繁體中文](README.zh-TW.md)
# 🎵 Il Lettore Musicale

> Un lettore musicale in puro HTML con interfaccia vintage in vinile, che supporta oltre 150 lingue globali e quasi 50 dialetti regionali. **In una sola pagina HTML, goditi melodie lente con dialetti da tutto il mondo.**

**Nota: questo progetto è stato realizzato con il contributo dell'intelligenza artificiale.**

---

## ✨ Caratteristiche

- 🎨 **Design immersivo in vinile** – disco rotante, animazione del braccio, esperienza visiva retrò.
- 🌍 **Oltre 150 lingue e 50 dialetti** – tra cui Wu, Cantonese, Hakka, Gan, Xiang, Jin e altri.
- 📂 **Supporto drag & drop** – trascina file audio (MP3/WAV/FLAC/OGG) o clicca su "Aggiungi musica".
- 📝 **Sincronizzazione dei testi LRC** – importa file `.lrc`, con evidenziazione a scorrimento e modalità testi a schermo intero.
- 🎛️ **Controlli completi** – play/pausa, precedente/successivo, casuale, modalità ripetizione (nessuna/tutte/una) e regolazione del volume.
- 📱 **Adattivo** – funziona perfettamente su desktop, tablet e dispositivi mobili.
- 🧩 **Nessuna dipendenza esterna** – funziona interamente nel browser, senza installazione.

---

## 🚀 Guida rapida

1. Scarica il file `TheMusicPlayer.html`.
2. Apri il file con un **doppio clic** in qualsiasi browser moderno (Chrome, Edge, Firefox, ecc.).
3. Clicca su **"Aggiungi musica"** o trascina i file audio nella finestra.
4. Clicca sul pulsante **"Testi"** per importare un file `.lrc` per la canzone corrente.
5. Clicca sull'**icona a ingranaggio (impostazioni)** per cambiare il font e la lingua dell'interfaccia.

---

### Dettaglio

Questo lettore musicale è stato creato per aiutare gli utenti ad allontanarsi dal trambusto e abbracciare una vita lenta e rilassante accompagnata da belle melodie. Offre un supporto di localizzazione completo che copre 150 lingue globali e quasi 50 dialetti regionali distintivi. Per la prima volta, abbiamo integrato un design visivo immersivo in vinile vintage nell'interfaccia di riproduzione, offrendo un'esperienza di ascolto più tattile e nostalgica. Sentiti libero di scaricarlo e provarlo personalmente.

> **Intenzione progettuale:** La mia ispirazione principale nasce da un semplice desiderio: apprezzare la musica in modo rilassato e senza complicazioni. Ho scelto di costruire questo lettore esclusivamente con tecnologia HTML perché garantisce la massima compatibilità su tutti i computer. In questo modo, ogni amante della musica può accedere e godere di splendide melodie senza installazioni fastidiose o configurazioni complesse.

---

## 🛠️ Note tecniche

- Realizzato con **puro HTML, CSS e JavaScript** – nessuna libreria di terze parti.
- **Parser ID3v2 integrato** (supporta v2.3 e v2.4) che estrae titolo, artista, album e copertina.
- Utilizza le **API Audio** e **Media Session** per il controllo multimediale a livello di sistema.
- Tutte le risorse di localizzazione sono incorporate – non è necessaria una connessione Internet per cambiare lingua.

---

## 📁 Formati di file supportati

### Formati audio
Il lettore può aprire e riprodurre i seguenti tipi di file audio (tramite il pulsante "Aggiungi musica" o drag & drop):

- **MP3** (.mp3)
- **WAV** (.wav)
- **FLAC** (.flac)
- **OGG** (.ogg)
- Inoltre formati comuni come **M4A**, **AAC** e **WMA** (a seconda del supporto del browser).

> Il lettore utilizza il motore audio integrato del browser, quindi le effettive capacità di riproduzione possono variare leggermente tra i browser.

### Tag dei metadati (ID3v2)
Quando aggiungi un file MP3 (o qualsiasi file contenente tag ID3v2.3 / v2.4), il lettore legge automaticamente i seguenti tag:

| Tag         | Significato                   | Visualizzato come          |
|-------------|-------------------------------|----------------------------|
| TIT2        | Titolo                        | Nome della canzone         |
| TPE1        | Artista                       | Nome dell'artista          |
| TALB        | Album                         | Nome dell'album            |
| TYER / TDRC | Anno / Data di pubblicazione  | Anno / Data                |
| TCOM        | Compositore                   | (nessuna visualizzazione separata, ricade su artista) |
| TCON        | Genere                        | Genere                     |
| TRCK        | Numero traccia                | Numero traccia             |
| TDAT        | Data                          | Data                       |
| APIC        | Immagine allegata             | Copertina sull'etichetta del vinile |

Se non vengono trovati tag ID3, il lettore tenta di analizzare il **nome del file** nel formato `Artista - Titolo` (l'ultimo ` - ` viene utilizzato come separatore).

### Formato dei testi (LRC)
Puoi importare file di testi sincronizzati standard **LRC** (con estensione `.lrc`). Il parser supporta timestamp nei seguenti formati:

- `[mm:ss.xx]` – minuti, secondi e centesimi di secondo
- `[mm:ss.xxx]` – minuti, secondi e millisecondi

Il lettore evidenzia in tempo reale la riga corrente durante la riproduzione e puoi cliccare su qualsiasi riga per saltare a quel timestamp.

Per importare un file LRC: clicca sul pulsante **"Testi"** nel lettore e seleziona **"Importa testi"**; oppure, mentre la canzone corrispondente è in riproduzione, trascina il file `.lrc` direttamente nella pagina.

---

Questo progetto è concesso in licenza con licenza MIT - consultare il file [LICENSE](LICENSE) per i dettagli.

---

## 📬 Feedback e supporto

Se incontri problemi durante l'utilizzo di questo lettore, non esitare a discuterne con me su GitHub. In alternativa, puoi contattarmi via e-mail:  
WalkDolphin [at] outlook [dot] com