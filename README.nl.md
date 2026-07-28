🇸🇦 [العربية](README.ar.md) · 🇩🇪 [Deutsch](README.de.md) · 🇬🇧 [English](README.md) · 🇪🇸 [Español](README.es.md) · 🇫🇷 [Français](README.fr.md) · 🇮🇳 [हिन्दी](README.hi.md) · 🇮🇹 [Italiano](README.it.md) · 🇯🇵 [日本語](README.ja.md) · 🇰🇭 [ភាសាខ្មែរ](README.km.md) · 🇰🇷 [한국어](README.ko.md) · 🇳🇱 [Nederlands](README.nl.md) · 🇳🇴 [Norsk](README.no.md) · 🇵🇱 [Polski](README.pl.md) · 🇵🇹 [Português](README.pt.md) · 🇷🇺 [Русский](README.ru.md) · 🇹🇭 [ไทย](README.th.md) · 🇹🇷 [Türkçe](README.tr.md) · 🇺🇦 [Українська](README.uk.md) · 🇨🇳 [简体中文](README.zh-CN.md) · 🇹🇼 [繁體中文](README.zh-TW.md)
# 🎵 De Muziekspeler

> Een pure HTML-muziekspeler met een vintage vinylplaatinterface, met ondersteuning voor meer dan 150 wereldtalen en bijna 50 regionale dialecten. **In één enkele HTML-pagina geniet je van langzame melodieën met dialecten van over de hele wereld.**

**Opmerking: dit project is tot stand gekomen met medewerking van kunstmatige intelligentie.**

---

## ✨ Functies

- 🎨 **Meeslepend vinylontwerp** – draaiende schijf, toonarmanimatie, retro visuele ervaring.
- 🌍 **150+ talen en 50 dialecten** – waaronder Wu, Kantonees, Hakka, Gan, Xiang, Jin en meer.
- 📂 **Ondersteuning voor slepen en neerzetten** – sleep audiobestanden (MP3/WAV/FLAC/OGG) of klik op "Muziek toevoegen".
- 📝 **LRC-tekstsynchronisatie** – importeer `.lrc`-bestanden met gemarkeerd scrollen en volledig scherm-tekstmodus.
- 🎛️ **Vollige afspeelbediening** – afspelen/pauzeren, vorige/volgende, shuffle, herhaalmodi (geen/alle/één) en volumeregeling.
- 📱 **Responsief** – werkt soepel op desktop, tablet en mobiel.
- 🧩 **Geen externe afhankelijkheden** – draait volledig in je browser, geen installatie vereist.

---

## 🚀 Snel aan de slag

1. Download het bestand `TheMusicPlayer.html`.
2. Open het met een **dubbele klik** in elke moderne browser (Chrome, Edge, Firefox, enz.).
3. Klik op **"Muziek toevoegen"** of sleep audiobestanden naar het venster.
4. Klik op de knop **"Tekst"** om een `.lrc`-bestand voor het huidige nummer te importeren.
5. Klik op het **tandwielpictogram (instellingen)** om het lettertype en de interfacetaal te wijzigen.

---

### Detail

Deze muziekspeler is ontworpen om gebruikers te helpen ontsnappen aan de drukte en een rustig, ontspannen leven te omarmen, begeleid door mooie melodieën. Het biedt uitgebreide lokalisatie-ondersteuning die 150 wereldtalen en bijna 50 unieke regionale dialecten dekt. Voor de allereerste keer hebben we een meeslepend vintage vinylplaatontwerp in de afspeelinterface geïntegreerd, wat zorgt voor een meer tastbare en nostalgische luisterervaring. Download het gerust en probeer het zelf uit.

> **Ontwerpintentie:** Mijn belangrijkste inspiratie komt voort uit een eenvoudige wens: op een ontspannen, ongecompliceerde manier van muziek genieten. Ik heb ervoor gekozen deze speler puur met HTML-technologie te bouwen omdat het universele compatibiliteit biedt op alle persoonlijke computers. Zo kan elke muziekliefhebber toegang krijgen tot en genieten van prachtige melodieën zonder vervelende installatie of ingewikkelde configuratie.

---

## 🛠️ Technische notities

- Gebouwd met **pure HTML, CSS en JavaScript** – geen bibliotheken van derden.
- Ingebouwde **ID3v2-parser** (ondersteunt v2.3 en v2.4) die titel, artiest, album en hoesafbeelding extraheert.
- Gebruikt **Audio API** en **Media Session API** voor systeemmediabediening.
- Alle lokalisatiebronnen zijn ingebed – geen internetverbinding nodig om van taal te wisselen.

---

## 📁 Ondersteunde bestandsformaten

### Audioformaten
De speler kan de volgende audiobestandstypen openen en afspelen (via de knop "Muziek toevoegen" of slepen en neerzetten):

- **MP3** (.mp3)
- **WAV** (.wav)
- **FLAC** (.flac)
- **OGG** (.ogg)
- Plus veelgebruikte formaten zoals **M4A**, **AAC** en **WMA** (afhankelijk van browserondersteuning).

> De speler gebruikt de ingebouwde audiomachine van de browser, dus de daadwerkelijke afspeelmogelijkheden kunnen per browser iets verschillen.

### Metadatatags (ID3v2)
Wanneer je een MP3-bestand (of elk bestand met ID3v2.3 / v2.4-tags) toevoegt, leest de speler automatisch de volgende tags:

| Tag         | Betekenis                   | Weergegeven als          |
|-------------|-----------------------------|--------------------------|
| TIT2        | Titel                       | Nummernaam               |
| TPE1        | Artiest                     | Artiestnaam              |
| TALB        | Album                       | Albumnaam                |
| TYER / TDRC | Jaar / Releasedatum         | Jaar / Datum             |
| TCOM        | Componist                   | (geen aparte weergave, valt terug op artiest) |
| TCON        | Genre                       | Genre                    |
| TRCK        | Tracknummer                 | Tracknummer              |
| TDAT        | Datum                       | Datum                    |
| APIC        | Bijgevoegde afbeelding      | Hoesafbeelding op het vinyllabel |

Als er geen ID3-tags worden gevonden, probeert de speler de **bestandsnaam** te ontleden in het formaat `Artiest - Titel` (de laatste ` - ` wordt als scheidingsteken gebruikt).

### Tekstformaat (LRC)
Je kunt standaard gesynchroniseerde **LRC**-tekstbestanden importeren (met de extensie `.lrc`). De parser ondersteunt tijdstempels in de volgende formaten:

- `[mm:ss.xx]` – minuten, seconden en honderdsten van een seconde
- `[mm:ss.xxx]` – minuten, seconden en duizendsten van een seconde

De speler markeert in realtime de huidige tekstregel tijdens het afspelen en je kunt op elke regel klikken om naar dat tijdstip te springen.

Een LRC-bestand importeren: klik op de knop **"Tekst"** in de speler en selecteer **"Tekst importeren"**; of sleep terwijl het betreffende nummer wordt afgespeeld het `.lrc`-bestand rechtstreeks naar de pagina.

---

Dit project is gelicenseerd onder de MIT-licentie - zie het bestand [LICENSE](LICENSE) voor details.

---

## 📬 Feedback en ondersteuning

Als je problemen ondervindt bij het gebruik van deze speler, aarzel dan niet om met mij te overleggen op GitHub. Je kunt me ook bereiken via e-mail:  
WalkDolphin [at] outlook [dot] com