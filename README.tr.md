🇸🇦 [العربية](README.ar.md) · 🇩🇪 [Deutsch](README.de.md) · 🇬🇧 [English](README.md) · 🇪🇸 [Español](README.es.md) · 🇫🇷 [Français](README.fr.md) · 🇮🇳 [हिन्दी](README.hi.md) · 🇮🇹 [Italiano](README.it.md) · 🇯🇵 [日本語](README.ja.md) · 🇰🇭 [ភាសាខ្មែរ](README.km.md) · 🇰🇷 [한국어](README.ko.md) · 🇳🇱 [Nederlands](README.nl.md) · 🇳🇴 [Norsk](README.no.md) · 🇵🇱 [Polski](README.pl.md) · 🇵🇹 [Português](README.pt.md) · 🇷🇺 [Русский](README.ru.md) · 🇹🇭 [ไทย](README.th.md) · 🇹🇷 [Türkçe](README.tr.md) · 🇺🇦 [Українська](README.uk.md) · 🇨🇳 [简体中文](README.zh-CN.md) · 🇹🇼 [繁體中文](README.zh-TW.md)
# 🎵 Müzik Çalar

> Vintage plak arayüzüne sahip, 150'den fazla küresel dili ve yaklaşık 50 bölgesel lehçeyi destekleyen saf HTML müzik çalar. **Tek bir HTML sayfasında, dünyanın dört bir yanından lehçelerle yavaş melodilerin tadını çıkarın.**

**Not: Bu proje, yapay zekanın katkısıyla oluşturulmuştur.**

---

## ✨ Özellikler

- 🎨 **Sürükleyici plak tasarımı** – dönen disk, ton kolu animasyonu, retro görsel deneyim.
- 🌍 **150+ dil ve 50 lehçe** – Wu, Kantonca, Hakka, Gan, Xiang, Jin ve daha fazlası dahil.
- 📂 **Sürükle ve bırak desteği** – ses dosyalarını (MP3/WAV/FLAC/OGG) sürükleyin veya "Müzik Ekle"ye tıklayın.
- 📝 **LRC şarkı sözü senkronizasyonu** – `.lrc` dosyalarını içe aktarın, vurgulu kaydırma ve tam ekran şarkı sözü modu ile.
- 🎛️ **Tam oynatma kontrolleri** – oynat/durdur, önceki/sonraki, karıştırma, tekrar modları (yok/tümü/bir) ve ses seviyesi ayarı.
- 📱 **Duyarlı** – masaüstü, tablet ve mobil cihazlarda sorunsuz çalışır.
- 🧩 **Harici bağımlılık yok** – tamamen tarayıcınızda çalışır, kurulum gerektirmez.

---

## 🚀 Hızlı Başlangıç

1. `TheMusicPlayer.html` dosyasını indirin.
2. Herhangi bir modern tarayıcıda (Chrome, Edge, Firefox, vb.) **çift tıklayarak** açın.
3. **"Müzik Ekle"** ye tıklayın veya ses dosyalarını pencereye sürükleyip bırakın.
4. Geçerli şarkı için bir `.lrc` şarkı sözü dosyasını içe aktarmak üzere **"Şarkı Sözleri"** düğmesine tıklayın.
5. Yazı tipini ve arayüz dilini değiştirmek için **dişli simgesine (ayarlar)** tıklayın.

---

### Detay

Bu müzik çalar, kullanıcıların koşuşturmacadan uzaklaşmasına ve güzel melodiler eşliğinde sakin bir yavaş yaşamı benimsemesine yardımcı olmak için hazırlanmıştır. 150 küresel dili ve yaklaşık 50 farklı bölgesel lehçeyi kapsayan kapsamlı yerelleştirme desteği sunar. İlk kez, oynatma arayüzüne sürükleyici bir vintage plak görsel tasarımı entegre ettik ve daha dokulu ve nostaljik bir dinleme deneyimi sunuyoruz. İndirmekten ve kendiniz denemekten çekinmeyin.

> **Tasarım amacı:** Temel ilham kaynağım, müziği rahat ve karmaşık olmayan bir şekilde takdir etme basit arzusundan kaynaklanmaktadır. Bu çalari tamamen HTML teknolojisiyle oluşturmayı tercih ettim çünkü tüm kişisel bilgisayarlarda evrensel uyumluluk sağlıyor. Bu sayede, her müzik sever, zahmetli kurulum veya karmaşık ayarlar olmadan harika melodilere erişebilir ve bunların keyfini çıkarabilir.

---

## 🛠️ Teknik Notlar

- **Saf HTML, CSS ve JavaScript** ile oluşturulmuştur – üçüncü taraf kütüphane yok.
- Yerleşik **ID3v2 ayrıştırıcısı** (v2.3 ve v2.4'ü destekler) başlık, sanatçı, albüm ve kapak resmini çıkarır.
- Sistem düzeyinde medya kontrolü için **Audio API** ve **Media Session API** kullanır.
- Tüm yerelleştirme kaynakları gömülüdür – dil değiştirmek için internet bağlantısı gerekmez.

---

## 📁 Desteklenen Dosya Biçimleri

### Ses Biçimleri
Çalar, "Müzik Ekle" düğmesi veya sürükle ve bırak yoluyla aşağıdaki ses dosyası türlerini açabilir ve oynatabilir:

- **MP3** (.mp3)
- **WAV** (.wav)
- **FLAC** (.flac)
- **OGG** (.ogg)
- Ayrıca **M4A**, **AAC** ve **WMA** gibi yaygın biçimler (tarayıcı desteğine bağlı olarak).

> Çalar, tarayıcının yerleşik ses motorunu kullanır, bu nedenle gerçek oynatma yeteneği tarayıcılar arasında biraz farklılık gösterebilir.

### Meta Veri Etiketleri (ID3v2)
Bir MP3 dosyası (veya ID3v2.3 / v2.4 etiketleri içeren herhangi bir dosya) eklediğinizde, çalar otomatik olarak aşağıdaki etiketleri okur:

| Etiket       | Anlamı                      | Görüntülendiği Yer       |
|--------------|-----------------------------|--------------------------|
| TIT2         | Başlık                      | Şarkı adı                |
| TPE1         | Sanatçı                     | Sanatçı adı              |
| TALB         | Albüm                       | Albüm adı                |
| TYER / TDRC  | Yıl / Yayın tarihi          | Yıl / Tarih              |
| TCOM         | Besteci                     | (ayrı görüntülenmez, sanatçıya düşer) |
| TCON         | Tür                         | Tür                      |
| TRCK         | Parça numarası              | Parça numarası           |
| TDAT         | Tarih                       | Tarih                    |
| APIC         | Ekli resim                  | Plak etiketindeki kapak resmi |

ID3 etiketleri bulunamazsa, çalar **dosya adını** `Sanatçı - Başlık` biçiminde ayrıştırmaya çalışır (son ` - ` ayırıcı olarak kullanılır).

### Şarkı Sözü Biçimi (LRC)
Standart **LRC** şarkı sözü dosyalarını (`.lrc` uzantılı) içe aktarabilirsiniz. Ayrıştırıcı aşağıdaki biçimlerdeki zaman damgalarını destekler:

- `[mm:ss.xx]` – dakika, saniye ve saniyenin yüzde biri
- `[mm:ss.xxx]` – dakika, saniye ve saniyenin binde biri

Çalar, oynatma ilerledikçe geçerli şarkı sözü satırını gerçek zamanlı olarak vurgular ve herhangi bir satıra tıklayarak o zaman damgasına atlayabilirsiniz.

LRC dosyasını içe aktarmak için: Çalardaki **"Şarkı Sözleri"** düğmesine tıklayın ve **"Şarkı Sözlerini İçe Aktar"** seçeneğini seçin; veya ilgili şarkı çalarken `.lrc` dosyasını doğrudan sayfaya sürükleyip bırakın.

---

Bu proje MIT Lisansı ile lisanslanmıştır - ayrıntılar için [LICENSE](LICENSE) dosyasına bakın.

---

## 📬 Geri Bildirim ve Destek

Bu çaları kullanırken herhangi bir sorunla karşılaşırsanız, GitHub üzerinde benimle tartışmaktan çekinmeyin. Alternatif olarak, e-posta yoluyla da bana ulaşabilirsiniz:  
WalkDolphin [at] outlook [dot] com