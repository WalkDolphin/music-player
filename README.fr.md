🇸🇦 [العربية](README.ar.md) · 🇩🇪 [Deutsch](README.de.md) · 🇬🇧 [English](README.md) · 🇪🇸 [Español](README.es.md) · 🇫🇷 [Français](README.fr.md) · 🇮🇳 [हिन्दी](README.hi.md) · 🇮🇹 [Italiano](README.it.md) · 🇯🇵 [日本語](README.ja.md) · 🇰🇭 [ភាសាខ្មែរ](README.km.md) · 🇰🇷 [한국어](README.ko.md) · 🇳🇱 [Nederlands](README.nl.md) · 🇳🇴 [Norsk](README.no.md) · 🇵🇱 [Polski](README.pl.md) · 🇵🇹 [Português](README.pt.md) · 🇷🇺 [Русский](README.ru.md) · 🇹🇭 [ไทย](README.th.md) · 🇹🇷 [Türkçe](README.tr.md) · 🇺🇦 [Українська](README.uk.md) · 🇨🇳 [简体中文](README.zh-CN.md) · 🇹🇼 [繁體中文](README.zh-TW.md)
# 🎵 Le Lecteur de Musique

> Un lecteur de musique en HTML pur avec une interface vinyle vintage, prenant en charge plus de 150 langues mondiales et près de 50 dialectes régionaux. **Dans une seule page HTML, profitez de mélodies lentes avec des dialectes du monde entier.**

**Remarque : ce projet a été créé avec la participation de l'intelligence artificielle.**

---

## ✨ Fonctionnalités

- 🎨 **Design vinyle immersif** – disque tournant, animation du bras de lecture, expérience visuelle rétro.
- 🌍 **Plus de 150 langues et 50 dialectes** – dont le wu, le cantonais, le hakka, le gan, le xiang, le jin et bien d'autres.
- 📂 **Prise en charge du glisser-déposer** – glissez des fichiers audio (MP3/WAV/FLAC/OGG) ou cliquez sur "Ajouter de la musique".
- 📝 **Synchronisation des paroles LRC** – importez des fichiers `.lrc` avec surbrillance dynamique et mode paroles en plein écran.
- 🎛️ **Contrôles de lecture complets** – lecture/pause, précédent/suivant, aléatoire, modes de répétition (aucune/toute/une) et réglage du volume.
- 📱 **Adaptatif** – fonctionne parfaitement sur ordinateur de bureau, tablette et mobile.
- 🧩 **Aucune dépendance externe** – fonctionne entièrement dans le navigateur, sans installation.

---

## 🚀 Démarrage rapide

1. Téléchargez le fichier `TheMusicPlayer.html`.
2. Ouvrez-le en **double-cliquant** dans n'importe quel navigateur moderne (Chrome, Edge, Firefox, etc.).
3. Cliquez sur **"Ajouter de la musique"** ou glissez-déposez des fichiers audio dans la fenêtre.
4. Cliquez sur le bouton **"Paroles"** pour importer un fichier `.lrc` pour la chanson en cours.
5. Cliquez sur l'**icône d'engrenage (paramètres)** pour modifier la police et la langue de l'interface.

---

### Détail

Ce lecteur de musique est conçu pour aider les utilisateurs à s'éloigner de l'agitation du quotidien et à adopter une vie lente et apaisante, accompagnée de belles mélodies. Il offre une prise en charge complète de la localisation couvrant 150 langues mondiales et près de 50 dialectes régionaux distinctifs. Pour la toute première fois, nous avons intégré un design visuel immersif de vinyle vintage à l'interface de lecture, offrant une expérience d'écoute plus texturée et nostalgique. N'hésitez pas à le télécharger et à l'essayer par vous-même.

> **Intention de conception :** Mon inspiration principale provient d'un simple désir : apprécier la musique de manière détendue et sans complication. J'ai choisi de construire ce lecteur uniquement avec la technologie HTML car elle offre une compatibilité universelle sur tous les ordinateurs personnels. Ainsi, tout amateur de musique peut accéder et profiter de merveilleuses mélodies sans installation fastidieuse ni configuration complexe.

---

## 🛠️ Notes techniques

- Construit avec **HTML, CSS et JavaScript purs** – sans bibliothèques tierces.
- **Analyseur ID3v2 intégré** (compatible v2.3 et v2.4) qui extrait le titre, l'artiste, l'album et la pochette.
- Utilise l'**API Audio** et l'**API Media Session** pour le contrôle multimédia au niveau système.
- Toutes les ressources de localisation sont intégrées – aucune connexion Internet n'est nécessaire pour changer de langue.

---

## 📁 Formats de fichiers pris en charge

### Formats audio
Le lecteur peut ouvrir et lire les types de fichiers audio suivants (via le bouton "Ajouter de la musique" ou par glisser-déposer) :

- **MP3** (.mp3)
- **WAV** (.wav)
- **FLAC** (.flac)
- **OGG** (.ogg)
- Ainsi que les formats courants comme **M4A**, **AAC** et **WMA** (selon la prise en charge du navigateur).

> Le lecteur utilise le moteur audio intégré du navigateur, les capacités de lecture réelles peuvent donc varier légèrement selon les navigateurs.

### Balises de métadonnées (ID3v2)
Lorsque vous ajoutez un fichier MP3 (ou tout fichier contenant des balises ID3v2.3 / v2.4), le lecteur lit automatiquement les balises suivantes :

| Balise      | Signification                | Affichée comme           |
|-------------|------------------------------|--------------------------|
| TIT2        | Titre                        | Nom de la chanson        |
| TPE1        | Artiste                      | Nom de l'artiste         |
| TALB        | Album                        | Nom de l'album           |
| TYER / TDRC | Année / Date de sortie       | Année / Date             |
| TCOM        | Compositeur                  | (pas d'affichage séparé, utilise l'artiste) |
| TCON        | Genre                        | Genre                    |
| TRCK        | Numéro de piste              | Numéro de piste          |
| TDAT        | Date                         | Date                     |
| APIC        | Image jointe                 | Pochette sur l'étiquette du vinyle |

Si aucune balise ID3 n'est trouvée, le lecteur essaiera d'analyser le **nom du fichier** au format `Artiste - Titre` (le dernier ` - ` est utilisé comme séparateur).

### Format des paroles (LRC)
Vous pouvez importer des fichiers de paroles synchronisées standard **LRC** (avec l'extension `.lrc`). L'analyseur prend en charge les horodatages aux formats suivants :

- `[mm:ss.xx]` – minutes, secondes et centièmes de seconde
- `[mm:ss.xxx]` – minutes, secondes et millièmes de seconde

Le lecteur met en surbrillance la ligne de paroles actuelle en temps réel pendant la lecture, et vous pouvez cliquer sur n'importe quelle ligne pour sauter à cet horodatage.

Pour importer un fichier LRC : cliquez sur le bouton **"Paroles"** dans le lecteur et sélectionnez **"Importer des paroles"** ; ou, pendant que la chanson correspondante est en cours de lecture, glissez-déposez le fichier `.lrc` directement sur la page.

---

Ce projet est sous licence MIT - voir le fichier [LICENSE](LICENSE) pour plus de détails.

---

## 📬 Retours et assistance

Si vous rencontrez des problèmes lors de l'utilisation de ce lecteur, n'hésitez pas à en discuter avec moi sur GitHub. Vous pouvez également me contacter par e-mail :  
WalkDolphin [at] outlook [dot] com