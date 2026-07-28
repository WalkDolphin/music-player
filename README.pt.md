🇸🇦 [العربية](README.ar.md) · 🇩🇪 [Deutsch](README.de.md) · 🇬🇧 [English](README.md) · 🇪🇸 [Español](README.es.md) · 🇫🇷 [Français](README.fr.md) · 🇮🇳 [हिन्दी](README.hi.md) · 🇮🇹 [Italiano](README.it.md) · 🇯🇵 [日本語](README.ja.md) · 🇰🇭 [ភាសាខ្មែរ](README.km.md) · 🇰🇷 [한국어](README.ko.md) · 🇳🇱 [Nederlands](README.nl.md) · 🇳🇴 [Norsk](README.no.md) · 🇵🇱 [Polski](README.pl.md) · 🇵🇹 [Português](README.pt.md) · 🇷🇺 [Русский](README.ru.md) · 🇹🇭 [ไทย](README.th.md) · 🇹🇷 [Türkçe](README.tr.md) · 🇺🇦 [Українська](README.uk.md) · 🇨🇳 [简体中文](README.zh-CN.md) · 🇹🇼 [繁體中文](README.zh-TW.md)
# 🎵 O Reprodutor de Música

> Um reprodutor de música em HTML puro com interface de vinil vintage, compatível com mais de 150 idiomas globais e quase 50 dialetos regionais. **Em uma única página HTML, desfrute de melodias lentas com dialetos de todo o mundo.**

**Nota: este projeto foi criado com a participação de inteligência artificial.**

---

## ✨ Características

- 🎨 **Design imersivo de vinil** – disco giratório, animação do braço, experiência visual retrô.
- 🌍 **Mais de 150 idiomas e 50 dialetos** – incluindo Wu, Cantonês, Hakka, Gan, Xiang, Jin e outros.
- 📂 **Suporte a arrastar e soltar** – arraste arquivos de áudio (MP3/WAV/FLAC/OGG) ou clique em "Adicionar música".
- 📝 **Sincronização de letras LRC** – importe arquivos `.lrc`, com destaque rolante e modo de letras em tela cheia.
- 🎛️ **Controles completos** – reproduzir/pausar, anterior/próximo, aleatório, modos de repetição (nenhuma/todas/uma) e ajuste de volume.
- 📱 **Adaptável** – funciona perfeitamente em desktops, tablets e dispositivos móveis.
- 🧩 **Sem dependências externas** – funciona inteiramente no navegador, sem necessidade de instalação.

---

## 🚀 Início rápido

1. Baixe o arquivo `TheMusicPlayer.html`.
2. Abra-o com **duplo clique** em qualquer navegador moderno (Chrome, Edge, Firefox, etc.).
3. Clique em **"Adicionar música"** ou arraste e solte arquivos de áudio na janela.
4. Clique no botão **"Letras"** para importar um arquivo `.lrc` para a música atual.
5. Clique no **ícone de engrenagem (configurações)** para alterar a fonte e o idioma da interface.

---

### Detalhe

Este reprodutor de música foi criado para ajudar os usuários a se afastarem da agitação e abraçarem uma vida lenta e relaxante, acompanhada por belas melodias. Oferece suporte abrangente de localização que cobre 150 idiomas globais e quase 50 dialetos regionais distintos. Pela primeira vez, integramos um design visual imersivo de vinil vintage à interface de reprodução, proporcionando uma experiência auditiva mais texturizada e nostálgica. Sinta-se à vontade para baixar e experimentar você mesmo.

> **Intenção do design:** Minha inspiração principal vem de um simples desejo: apreciar a música de uma forma relaxada e sem complicações. Optei por construir este reprodutor exclusivamente com tecnologia HTML porque oferece compatibilidade universal em todos os computadores pessoais. Dessa forma, qualquer amante da música pode acessar e desfrutar de melodias maravilhosas sem instalações incômodas ou configurações complexas.

---

## 🛠️ Notas técnicas

- Construído com **HTML, CSS e JavaScript puros** – sem bibliotecas de terceiros.
- **Parser ID3v2 integrado** (compatível com v2.3 e v2.4) que extrai título, artista, álbum e capa.
- Utiliza **Audio API** e **Media Session API** para controle de mídia em nível de sistema.
- Todos os recursos de localização estão incorporados – não é necessária conexão com a Internet para alterar o idioma.

---

## 📁 Formatos de arquivo compatíveis

### Formatos de áudio
O reprodutor pode abrir e reproduzir os seguintes tipos de arquivos de áudio (através do botão "Adicionar música" ou arrastar e soltar):

- **MP3** (.mp3)
- **WAV** (.wav)
- **FLAC** (.flac)
- **OGG** (.ogg)
- Além de formatos comuns como **M4A**, **AAC** e **WMA** (dependendo do suporte do navegador).

> O reprodutor utiliza o motor de áudio integrado do navegador, portanto, a capacidade real de reprodução pode variar ligeiramente entre navegadores.

### Tags de metadados (ID3v2)
Quando você adiciona um arquivo MP3 (ou qualquer arquivo que contenha tags ID3v2.3 / v2.4), o reprodutor lê automaticamente as seguintes tags:

| Tag         | Significado                   | Exibido como               |
|-------------|-------------------------------|----------------------------|
| TIT2        | Título                        | Nome da música             |
| TPE1        | Artista                       | Nome do artista            |
| TALB        | Álbum                         | Nome do álbum              |
| TYER / TDRC | Ano / Data de lançamento      | Ano / Data                 |
| TCOM        | Compositor                    | (sem exibição separada, usa o artista) |
| TCON        | Gênero                        | Gênero                     |
| TRCK        | Número da faixa               | Número da faixa            |
| TDAT        | Data                          | Data                       |
| APIC        | Imagem anexada                | Capa na etiqueta do vinil  |

Se nenhuma tag ID3 for encontrada, o reprodutor tentará analisar o **nome do arquivo** no formato `Artista - Título` (o último ` - ` é usado como separador).

### Formato de letras (LRC)
Você pode importar arquivos de letras sincronizadas padrão **LRC** (com extensão `.lrc`). O analisador suporta timestamps nos seguintes formatos:

- `[mm:ss.xx]` – minutos, segundos e centésimos de segundo
- `[mm:ss.xxx]` – minutos, segundos e milésimos de segundo

O reprodutor destaca em tempo real a linha atual durante a reprodução e você pode clicar em qualquer linha para saltar para aquele timestamp.

Para importar um arquivo LRC: clique no botão **"Letras"** no reprodutor e selecione **"Importar letras"**; ou, enquanto a música correspondente estiver tocando, arraste e solte o arquivo `.lrc` diretamente na página.

---

Este projeto está licenciado sob a licença MIT - consulte o arquivo [LICENSE](LICENSE) para obter detalhes.

---

## 📬 Comentários e suporte

Se você encontrar algum problema ao usar este reprodutor, não hesite em discutir comigo no GitHub. Alternativamente, você também pode entrar em contato por e-mail:  
WalkDolphin [at] outlook [dot] com