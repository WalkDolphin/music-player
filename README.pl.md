🇸🇦 [العربية](README.ar.md) · 🇩🇪 [Deutsch](README.de.md) · 🇬🇧 [English](README.md) · 🇪🇸 [Español](README.es.md) · 🇫🇷 [Français](README.fr.md) · 🇮🇳 [हिन्दी](README.hi.md) · 🇮🇹 [Italiano](README.it.md) · 🇯🇵 [日本語](README.ja.md) · 🇰🇭 [ភាសាខ្មែរ](README.km.md) · 🇰🇷 [한국어](README.ko.md) · 🇳🇱 [Nederlands](README.nl.md) · 🇳🇴 [Norsk](README.no.md) · 🇵🇱 [Polski](README.pl.md) · 🇵🇹 [Português](README.pt.md) · 🇷🇺 [Русский](README.ru.md) · 🇹🇭 [ไทย](README.th.md) · 🇹🇷 [Türkçe](README.tr.md) · 🇺🇦 [Українська](README.uk.md) · 🇨🇳 [简体中文](README.zh-CN.md) · 🇹🇼 [繁體中文](README.zh-TW.md)
# 🎵 Odtwarzacz Muzyki

> Odtwarzacz muzyki w czystym HTML z interfejsem przypominającym winylową płytę, obsługujący ponad 150 języków światowych i prawie 50 dialektów regionalnych. **Na jednej stronie HTML ciesz się wolnymi melodiami z dialektami z całego świata.**

**Uwaga: ten projekt został stworzony z udziałem sztucznej inteligencji.**

---

## ✨ Funkcje

- 🎨 **Immersyjny design winylowy** – obracający się dysk, animacja ramienia, retro doświadczenie wizualne.
- 🌍 **Ponad 150 języków i 50 dialektów** – w tym wu, kantoński, hakka, gan, xiang, jin i inne.
- 📂 **Obsługa przeciągania i upuszczania** – przeciągnij pliki audio (MP3/WAV/FLAC/OGG) lub kliknij „Dodaj muzykę”.
- 📝 **Synchronizacja tekstów LRC** – importuj pliki `.lrc` z podświetlanym przewijaniem i trybem pełnoekranowym.
- 🎛️ **Pełna kontrola odtwarzania** – odtwarzanie/wstrzymanie, poprzedni/następny, losowy, tryby powtarzania (brak/wszystkie/jeden) oraz regulacja głośności.
- 📱 **Responsywność** – działa płynnie na komputerach stacjonarnych, tabletach i urządzeniach mobilnych.
- 🧩 **Brak zależności zewnętrznych** – działa w całości w przeglądarce, bez konieczności instalacji.

---

## 🚀 Szybki start

1. Pobierz plik `TheMusicPlayer.html`.
2. Otwórz go **podwójnym kliknięciem** w dowolnej nowoczesnej przeglądarce (Chrome, Edge, Firefox itp.).
3. Kliknij **„Dodaj muzykę”** lub przeciągnij pliki audio do okna.
4. Kliknij przycisk **„Teksty”**, aby zaimportować plik `.lrc` dla bieżącej piosenki.
5. Kliknij **ikonę koła zębatego (ustawienia)**, aby zmienić czcionkę i język interfejsu.

---

### Szczegóły

Ten odtwarzacz muzyki został stworzony, aby pomóc użytkownikom oderwać się od zgiełku i przyjąć kojące, spokojne życie w towarzystwie pięknych melodii. Oferuje wszechstronne wsparcie lokalizacyjne obejmujące 150 języków światowych i prawie 50 unikalnych dialektów regionalnych. Po raz pierwszy zintegrowaliśmy immersyjny projekt wizualny winylowej płyty z interfejsem odtwarzania, zapewniając bardziej namacalne i nostalgiczne doświadczenie słuchowe. Pobierz i wypróbuj sam.

> **Intencja projektowa:** Moja podstawowa inspiracja pochodzi z prostego pragnienia – cieszyć się muzyką w zrelaksowany, nieskomplikowany sposób. Wybrałem czystą technologię HTML, ponieważ zapewnia uniwersalną kompatybilność na wszystkich komputerach osobistych. W ten sposób każdy miłośnik muzyki może uzyskać dostęp i cieszyć się wspaniałymi melodiami bez uciążliwej instalacji czy skomplikowanej konfiguracji.

---

## 🛠️ Uwagi techniczne

- Zbudowany w **czystym HTML, CSS i JavaScript** – bez bibliotek zewnętrznych.
- Wbudowany **parser ID3v2** (obsługuje v2.3 i v2.4) wyodrębnia tytuł, artystę, album i okładkę.
- Wykorzystuje **Audio API** i **Media Session API** do sterowania multimediami na poziomie systemowym.
- Wszystkie zasoby lokalizacyjne są osadzone – zmiana języka nie wymaga połączenia z Internetem.

---

## 📁 Obsługiwane formaty plików

### Formaty audio
Odtwarzacz może otwierać i odtwarzać następujące typy plików audio (za pomocą przycisku „Dodaj muzykę” lub przeciągania i upuszczania):

- **MP3** (.mp3)
- **WAV** (.wav)
- **FLAC** (.flac)
- **OGG** (.ogg)
- Oraz popularne formaty, takie jak **M4A**, **AAC** i **WMA** (w zależności od obsługi przeglądarki).

> Odtwarzacz korzysta z wbudowanego silnika audio przeglądarki, więc rzeczywista wydajność odtwarzania może nieznacznie różnić się między przeglądarkami.

### Znaczniki metadanych (ID3v2)
Podczas dodawania pliku MP3 (lub dowolnego pliku zawierającego znaczniki ID3v2.3 / v2.4) odtwarzacz automatycznie odczytuje następujące znaczniki:

| Znacznik    | Znaczenie                    | Wyświetlane jako          |
|-------------|------------------------------|---------------------------|
| TIT2        | Tytuł                        | Nazwa utworu              |
| TPE1        | Artysta                      | Nazwa artysty             |
| TALB        | Album                        | Nazwa albumu              |
| TYER / TDRC | Rok / Data wydania           | Rok / Data                |
| TCOM        | Kompozytor                   | (brak osobnego wyświetlania, zastępuje artysta) |
| TCON        | Gatunek                      | Gatunek                   |
| TRCK        | Numer utworu                 | Numer utworu              |
| TDAT        | Data                         | Data                      |
| APIC        | Dołączone zdjęcie            | Okładka na etykiecie płyty |

Jeśli nie znaleziono znaczników ID3, odtwarzacz spróbuje przeanalizować **nazwę pliku** w formacie `Artysta - Tytuł` (ostatni ` - ` jest używany jako separator).

### Format tekstów (LRC)
Możesz importować standardowe pliki zsynchronizowanych tekstów **LRC** (z rozszerzeniem `.lrc`). Parser obsługuje znaczniki czasu w następujących formatach:

- `[mm:ss.xx]` – minuty, sekundy i setne sekundy
- `[mm:ss.xxx]` – minuty, sekundy i tysięczne sekundy

Odtwarzacz podświetla bieżącą linię tekstu w czasie rzeczywistym podczas odtwarzania, a kliknięcie dowolnej linii powoduje przeskoczenie do tego znacznika czasu.

Aby zaimportować plik LRC: kliknij przycisk **„Teksty”** w odtwarzaczu i wybierz **„Importuj teksty”**; lub podczas odtwarzania odpowiedniego utworu przeciągnij plik `.lrc` bezpośrednio na stronę.

---

Ten projekt jest licencjonowany na licencji MIT - szczegóły znajdują się w pliku [LICENSE](LICENSE).

---

## 📬 Opinie i wsparcie

Jeśli napotkasz jakiekolwiek problemy podczas korzystania z tego odtwarzacza, nie wahaj się podyskutować ze mną na GitHubie. Możesz również skontaktować się ze mną za pośrednictwem poczty elektronicznej:  
WalkDolphin [at] outlook [dot] com