🇸🇦 [العربية](README.ar.md) · 🇩🇪 [Deutsch](README.de.md) · 🇬🇧 [English](README.md) · 🇪🇸 [Español](README.es.md) · 🇫🇷 [Français](README.fr.md) · 🇮🇳 [हिन्दी](README.hi.md) · 🇮🇹 [Italiano](README.it.md) · 🇯🇵 [日本語](README.ja.md) · 🇰🇭 [ភាសាខ្មែរ](README.km.md) · 🇰🇷 [한국어](README.ko.md) · 🇳🇱 [Nederlands](README.nl.md) · 🇳🇴 [Norsk](README.no.md) · 🇵🇱 [Polski](README.pl.md) · 🇵🇹 [Português](README.pt.md) · 🇷🇺 [Русский](README.ru.md) · 🇹🇭 [ไทย](README.th.md) · 🇹🇷 [Türkçe](README.tr.md) · 🇺🇦 [Українська](README.uk.md) · 🇨🇳 [简体中文](README.zh-CN.md) · 🇹🇼 [繁體中文](README.zh-TW.md)
# 🎵 El Reproductor de Música

> Un reproductor de música en HTML puro con interfaz de vinilo vintage, compatible con más de 150 idiomas globales y casi 50 dialectos regionales. **En una sola página HTML, disfruta de melodías lentas con dialectos de todo el mundo.**

**Nota: este proyecto ha sido creado con la participación de inteligencia artificial.**

---

## ✨ Características

- 🎨 **Diseño inmersivo de vinilo** – disco giratorio, animación del brazo, experiencia visual retro.
- 🌍 **Más de 150 idiomas y 50 dialectos** – incluye wu, cantonés, hakka, gan, xiang, jin y otros.
- 📂 **Soporte de arrastrar y soltar** – arrastra archivos de audio (MP3/WAV/FLAC/OGG) o haz clic en "Agregar música".
- 📝 **Sincronización de letras LRC** – importa archivos `.lrc`, con resaltado en desplazamiento y modo de letras a pantalla completa.
- 🎛️ **Controles completos** – reproducir/pausar, anterior/siguiente, aleatorio, modos de repetición (ninguna/todas/una) y ajuste de volumen.
- 📱 **Adaptable** – funciona perfectamente en ordenadores de escritorio, tabletas y móviles.
- 🧩 **Sin dependencias externas** – se ejecuta completamente en el navegador, sin necesidad de instalación.

---

## 🚀 Inicio rápido

1. Descarga el archivo `TheMusicPlayer.html`.
2. Ábrelo con **doble clic** en cualquier navegador moderno (Chrome, Edge, Firefox, etc.).
3. Haz clic en **"Agregar música"** o arrastra archivos de audio a la ventana.
4. Haz clic en el botón **"Letras"** para importar un archivo `.lrc` para la canción actual.
5. Haz clic en el **icono de engranaje (ajustes)** para cambiar la fuente y el idioma de la interfaz.

---

### Detalle

Este reproductor de música está diseñado para ayudar a los usuarios a alejarse del ajetreo y abrazar una vida tranquila acompañada de hermosas melodías. Ofrece una completa localización que cubre 150 idiomas globales y casi 50 dialectos regionales distintivos. Por primera vez, hemos integrado un diseño visual de vinilo vintage inmersivo en la interfaz de reproducción, brindando una experiencia auditiva más texturizada y nostálgica. Siéntete libre de descargarlo y probarlo por ti mismo.

> **Intención de diseño:** Mi inspiración principal surge de un simple deseo: apreciar la música de una manera relajada y sin complicaciones. Opté por construir este reproductor únicamente con tecnología HTML porque ofrece compatibilidad universal en todas las computadoras personales. De esta forma, cualquier amante de la música puede acceder y disfrutar de maravillosas melodías sin necesidad de instalaciones molestas o configuraciones complejas.

---

## 🛠️ Notas técnicas

- Construido con **HTML, CSS y JavaScript puros** – sin bibliotecas de terceros.
- **Parser ID3v2 integrado** (compatible con v2.3 y v2.4) que extrae título, artista, álbum y carátula.
- Utiliza **API de Audio** y **API de Media Session** para el control multimedia a nivel de sistema.
- Todos los recursos de localización están incrustados – no se necesita conexión a Internet para cambiar de idioma.

---

## 📁 Formatos de archivo compatibles

### Formatos de audio
El reproductor puede abrir y reproducir los siguientes tipos de archivos de audio (mediante el botón "Agregar música" o arrastrar y soltar):

- **MP3** (.mp3)
- **WAV** (.wav)
- **FLAC** (.flac)
- **OGG** (.ogg)
- Además de formatos comunes como **M4A**, **AAC** y **WMA** (según el soporte del navegador).

> El reproductor utiliza el motor de audio integrado del navegador, por lo que la capacidad de reproducción real puede variar ligeramente entre navegadores.

### Etiquetas de metadatos (ID3v2)
Cuando agregas un archivo MP3 (o cualquier archivo que contenga etiquetas ID3v2.3 / v2.4), el reproductor lee automáticamente las siguientes etiquetas:

| Etiqueta    | Significado                   | Se muestra como            |
|-------------|-------------------------------|----------------------------|
| TIT2        | Título                        | Nombre de la canción       |
| TPE1        | Artista                       | Nombre del artista         |
| TALB        | Álbum                         | Nombre del álbum           |
| TYER / TDRC | Año / Fecha de lanzamiento    | Año / Fecha                |
| TCOM        | Compositor                    | (sin visualización separada, se recurre al artista) |
| TCON        | Género                        | Género                     |
| TRCK        | Número de pista               | Número de pista            |
| TDAT        | Fecha                         | Fecha                      |
| APIC        | Imagen adjunta                | Carátula en la etiqueta del vinilo |

Si no se encuentran etiquetas ID3, el reproductor intentará analizar el **nombre del archivo** en el formato `Artista - Título` (se utiliza el último ` - ` como separador).

### Formato de letras (LRC)
Puedes importar archivos de letras sincronizadas estándar **LRC** (con extensión `.lrc`). El analizador admite marcas de tiempo en los siguientes formatos:

- `[mm:ss.xx]` – minutos, segundos y centésimas de segundo
- `[mm:ss.xxx]` – minutos, segundos y milésimas de segundo

El reproductor resalta en tiempo real la línea actual durante la reproducción y puedes hacer clic en cualquier línea para saltar a esa marca de tiempo.

Para importar un archivo LRC: haz clic en el botón **"Letras"** del reproductor y selecciona **"Importar letras"**, o bien, mientras la canción correspondiente se está reproduciendo, arrastra y suelta el archivo `.lrc` directamente en la página.

---

Este proyecto está bajo la licencia MIT - consulte el archivo [LICENSE](LICENSE) para más detalles.

---

## 📬 Comentarios y soporte

Si encuentras algún problema al usar este reproductor, no dudes en comentarlo conmigo en GitHub. También puedes contactarme por correo electrónico:  
WalkDolphin [at] outlook [dot] com