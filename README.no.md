🇸🇦 [العربية](README.ar.md) · 🇩🇪 [Deutsch](README.de.md) · 🇬🇧 [English](README.md) · 🇪🇸 [Español](README.es.md) · 🇫🇷 [Français](README.fr.md) · 🇮🇳 [हिन्दी](README.hi.md) · 🇮🇹 [Italiano](README.it.md) · 🇯🇵 [日本語](README.ja.md) · 🇰🇭 [ភាសាខ្មែរ](README.km.md) · 🇰🇷 [한국어](README.ko.md) · 🇳🇱 [Nederlands](README.nl.md) · 🇳🇴 [Norsk](README.no.md) · 🇵🇱 [Polski](README.pl.md) · 🇵🇹 [Português](README.pt.md) · 🇷🇺 [Русский](README.ru.md) · 🇹🇭 [ไทย](README.th.md) · 🇹🇷 [Türkçe](README.tr.md) · 🇺🇦 [Українська](README.uk.md) · 🇨🇳 [简体中文](README.zh-CN.md) · 🇹🇼 [繁體中文](README.zh-TW.md)
# 🎵 Musikkspilleren

> En ren HTML-musikkspiller med vintage vinylplate-grensesnitt, som støtter over 150 globale språk og nesten 50 regionale dialekter. **På én enkelt HTML-side kan du nyte langsomme melodier med dialekter fra hele verden.**

**Merk: dette prosjektet er laget med deltakelse av kunstig intelligens.**

---

## ✨ Funksjoner

- 🎨 **Immersivt vinyldesign** – roterende plate, tonearm-animasjon, retro visuell opplevelse.
- 🌍 **Over 150 språk og 50 dialekter** – inkludert Wu, kantonesisk, Hakka, Gan, Xiang, Jin og flere.
- 📂 **Dra og slipp-støtte** – dra lydfiler (MP3/WAV/FLAC/OGG) eller klikk på "Legg til musikk".
- 📝 **LRC-tekstsynkronisering** – importer `.lrc`-filer med fremhevet rulling og fullskjerms tekstmodus.
- 🎛️ **Full avspillingskontroll** – spill/pause, forrige/neste, tilfeldig avspilling, gjentakelsesmoduser (ingen/alle/en) og volumjustering.
- 📱 **Responsiv** – fungerer sømløst på stasjonære datamaskiner, nettbrett og mobile enheter.
- 🧩 **Ingen eksterne avhengigheter** – kjører helt i nettleseren din, ingen installasjon nødvendig.

---

## 🚀 Kom raskt i gang

1. Last ned filen `TheMusicPlayer.html`.
2. Åpne den med **dobbeltklikk** i en hvilken som helst moderne nettleser (Chrome, Edge, Firefox, osv.).
3. Klikk på **"Legg til musikk"** eller dra lydfiler inn i vinduet.
4. Klikk på **"Tekst"**-knappen for å importere en `.lrc`-fil for den gjeldende sangen.
5. Klikk på **tannhjulet (innstillinger)** for å endre skrifttype og grensesnittspråk.

---

### Detalj

Denne musikkspilleren er laget for å hjelpe brukere med å komme vekk fra kjas og mas, og omfavne et rolig, langsomt liv akkompagnert av vakre melodier. Den tilbyr omfattende lokaliseringsstøtte som dekker 150 globale språk og nesten 50 unike regionale dialekter. For første gang har vi integrert et immersivt vintage vinyldesign i avspillingsgrensesnittet, noe som gir en mer taktil og nostalgisk lytteopplevelse. Last det ned og prøv selv.

> **Designhensikt:** Min kjerneinspirasjon kommer fra et enkelt ønske – å sette pris på musikk på en avslappet, ukomplisert måte. Jeg valgte å bygge denne spilleren med ren HTML-teknologi fordi den gir universell kompatibilitet på alle personlige datamaskiner. På denne måten kan alle musikkelskere få tilgang til og nyte fantastiske melodier uten plagsom installasjon eller komplisert oppsett.

---

## 🛠️ Tekniske notater

- Bygget med **ren HTML, CSS og JavaScript** – ingen tredjepartsbiblioteker.
- Innebygd **ID3v2-parser** (støtter v2.3 og v2.4) som trekker ut tittel, artist, album og coverbilde.
- Bruker **Audio API** og **Media Session API** for systemnivå mediekontroll.
- Alle lokaliseringsressurser er innebygd – ingen internettforbindelse nødvendig for å bytte språk.

---

## 📁 Støttede filformater

### Lydformater
Spilleren kan åpne og spille følgende lydfiltyper (via "Legg til musikk"-knappen eller dra og slipp):

- **MP3** (.mp3)
- **WAV** (.wav)
- **FLAC** (.flac)
- **OGG** (.ogg)
- I tillegg vanlige formater som **M4A**, **AAC** og **WMA** (avhengig av nettleserstøtte).

> Spilleren bruker nettleserens innebygde lydmotor, så den faktiske avspillingskapasiteten kan variere noe mellom nettlesere.

### Metadata-tagger (ID3v2)
Når du legger til en MP3-fil (eller en hvilken som helst fil som inneholder ID3v2.3 / v2.4-tagger), leser spilleren automatisk følgende tagger:

| Tagg        | Betydning                    | Vises som               |
|-------------|------------------------------|-------------------------|
| TIT2        | Tittel                       | Sangenavn               |
| TPE1        | Artist                       | Artistnavn              |
| TALB        | Album                        | Albumnavn               |
| TYER / TDRC | År / Utgivelsesdato          | År / Dato               |
| TCOM        | Komponist                    | (ingen separat visning, faller tilbake til artist) |
| TCON        | Sjanger                      | Sjanger                 |
| TRCK        | Spornummer                   | Spornummer              |
| TDAT        | Dato                         | Dato                    |
| APIC        | Vedlagt bilde                | Coverbilde på vinyl-etiketten |

Hvis ingen ID3-tagger blir funnet, vil spilleren prøve å analysere **filnavnet** i formatet `Artist - Tittel` (den siste ` - ` brukes som skilletegn).

### Tekstformat (LRC)
Du kan importere standard synkroniserte **LRC**-tekstfiler (med filtypen `.lrc`). Parseren støtter tidsstempler i følgende formater:

- `[mm:ss.xx]` – minutter, sekunder og hundredeler av et sekund
- `[mm:ss.xxx]` – minutter, sekunder og tusendeler av et sekund

Spilleren fremhever gjeldende tekstlinje i sanntid under avspilling, og du kan klikke på hvilken som helst linje for å hoppe til det tidsstempelet.

Slik importerer du en LRC-fil: Klikk på **"Tekst"**-knappen i spilleren og velg **"Importer tekst"**; eller mens den tilsvarende sangen spilles, dra og slipp `.lrc`-filen direkte på siden.

---

Dette prosjektet er lisensiert under MIT-lisensen - se filen [LICENSE](LICENSE) for detaljer.

---

## 📬 Tilbakemelding og støtte

Hvis du opplever problemer mens du bruker denne spilleren, må du gjerne diskutere med meg på GitHub. Alternativt kan du også kontakte meg via e-post:  
WalkDolphin [at] outlook [dot] com