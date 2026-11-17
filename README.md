# Port/eame

**Native iOS ports of decompiled games — no emulator, no JIT, bring your own disc.**
*Ports nativos para iOS de juegos decompilados: sin emulador, sin JIT, con tu propio disco.*

Port/eame takes community decompilations (the game's code rebuilt as C) and compiles them as real iOS apps.
The game runs as native ARM64 code, so it works from any sideloading store and from LiveContainer without JIT.
**No game data is included**: you need your own copy of the game.

| Game | Based on | iOS build | Status |
|---|---|---|---|
| Yu-Gi-Oh! Forbidden Memories (USA, PS1) | [YFM Re-Decomp](https://github.com/Unchiga/Yu-Gi-Oh-Forbidden-Memories-Recompiled) v0.3.0 | [Releases](../../releases) | Playable |

---

## Español

### Yu-Gi-Oh! Forbidden Memories para iPhone y iPad

Un port nativo de **YFM Re-Decomp** (la versión para PC hecha desde la decompilación del juego) a iOS.
No es un emulador: el juego corre como una app normal de iPhone.

**Qué incluye**

- Controles táctiles modernos (cruceta, botones, L1/L2/R1/R2, SELECT, START y MENU), lejos del notch.
- Menú de opciones con estilo de iOS.
- Las opciones gráficas HD del proyecto original (resolución interna, texto HD, antialiasing, filtros).
- Audio, animaciones y video del juego.
- Partidas guardadas y *save states*.
- Los mods que trae el proyecto: **3D Monsters**, **Hand Camera**, **AI Hard Mode**, **Yamyi mods** y **Drop Missing Cards**.

**Qué NO incluye**

- El juego. Necesitas el `.bin` de **tu propio disco** de Yu-Gi-Oh! Forbidden Memories, **versión USA (SLUS-01411)**.
  Nunca se incluye ni se comparte aquí.

### Requisitos

- iPhone o iPad de 64 bits con **iOS 16 o superior**.
- Probado en un **iPhone 12 Pro (A14) con iOS 27**. En otros modelos debería funcionar, pero aún no está probado:
  si lo pruebas, cuéntanos en *Issues*.
- Una forma de instalar IPAs: **AltStore, SideStore, FlareStore, LiveContainer** u otra.
  **No necesita JIT.**

### Instalación y primer arranque

1. Descarga el `.ipa` de [Releases](../../releases) e instálalo con tu store o con LiveContainer.
2. Abre el juego. Te pedirá el disco: toca **Choose ROM...**. Va a marcar un error;
   es normal en esta versión. **Cierra la app.**
3. Abre la app **Archivos** y entra a la carpeta de la app.
   - Instalada con una store: **En mi iPhone → YFM Re-Decomp → game**.
   - En LiveContainer: dentro de la carpeta de LiveContainer, en la carpeta *Documents* de la app → **game**.
4. Copia ahí el `.bin` de tu disco.
5. Vuelve a abrir el juego. Ya arranca.

Tus partidas, ajustes y el registro `port-eame-log.txt` quedan en esa misma carpeta (la de *Documents*).
Si algo falla, ese registro es lo que hay que compartir.

### Limitaciones conocidas

- **Choose ROM...** no abre un selector de archivos en iOS: el disco se pone a mano en la carpeta `game`.
- Al cambiar de idioma, cierra la app y vuelve a abrirla.
- Los mods externos que traen código (`.dylib`) tienen que compilarse para iOS y firmarse junto con la app;
  los que solo traen datos o texturas deberían funcionar desde la carpeta `mods` (en pruebas).
- La app no trae ícono propio.

### Créditos y licencia

- **[YFM Re-Decomp](https://github.com/Unchiga/Yu-Gi-Oh-Forbidden-Memories-Recompiled)** de Unchiga y colaboradores:
  el port a PC en el que se basa todo esto, bajo licencia MIT (ver la licencia incluida en la app).
- **[memories-decomp](https://github.com/krystalgamer/memories-decomp)**: la decompilación del juego, de sus autores.
- **SDL3, FreeType, libpng y zlib**: sus licencias van dentro de la app (`licenses/`).
- El código del port a iOS: [muguiwara23/port-eame-yfm](https://github.com/muguiwara23/port-eame-yfm/tree/port-eame/ios), rama `port-eame/ios`.

Proyecto de aficionados, sin fines de lucro, sin relación con Konami.
*Yu-Gi-Oh!* y *Forbidden Memories* son de Konami. No se distribuye ningún dato del juego.

---

## English

### Yu-Gi-Oh! Forbidden Memories for iPhone and iPad

A native iOS port of **YFM Re-Decomp** (the PC version built from the game's decompilation).
It is not an emulator: the game runs as a regular iPhone app.

**What's included**

- Modern touch controls (D-pad, face buttons, L1/L2/R1/R2, SELECT, START and MENU), kept clear of the notch.
- An iOS-style options menu.
- The original project's HD graphics options (internal resolution, HD text, antialiasing, filters).
- The game's audio, animations and video.
- Saves and save states.
- The mods that ship with the project: **3D Monsters**, **Hand Camera**, **AI Hard Mode**, **Yamyi mods** and **Drop Missing Cards**.

**What's NOT included**

- The game. You need the `.bin` from **your own disc** of Yu-Gi-Oh! Forbidden Memories, **USA version (SLUS-01411)**.
  It is never included or shared here.

### Requirements

- A 64-bit iPhone or iPad on **iOS 16 or later**.
- Tested on an **iPhone 12 Pro (A14) running iOS 27**. Other models should work but haven't been tested yet:
  if you try one, let us know in *Issues*.
- A way to install IPAs: **AltStore, SideStore, FlareStore, LiveContainer** or similar.
  **No JIT needed.**

### Installation and first launch

1. Download the `.ipa` from [Releases](../../releases) and install it with your store or with LiveContainer.
2. Open the game. It will ask for the disc: tap **Choose ROM...**. It will show an error;
   that's expected in this version. **Close the app.**
3. Open the **Files** app and go to the app's folder.
   - Installed with a store: **On My iPhone → YFM Re-Decomp → game**.
   - In LiveContainer: inside LiveContainer's folder, in the app's *Documents* folder → **game**.
4. Copy your disc's `.bin` there.
5. Open the game again. It starts.

Your saves, settings and the `port-eame-log.txt` log stay in that same folder (the *Documents* one).
If something goes wrong, that log is what to share.

### Known limitations

- **Choose ROM...** doesn't open a file picker on iOS: the disc goes into the `game` folder by hand.
- After changing the language, close the app and open it again.
- External mods that include code (`.dylib`) have to be compiled for iOS and signed together with the app;
  mods with only data or textures should work from the `mods` folder (being tested).
- The app has no icon of its own.

### Credits and license

- **[YFM Re-Decomp](https://github.com/Unchiga/Yu-Gi-Oh-Forbidden-Memories-Recompiled)** by Unchiga and contributors:
  the PC port all of this is built on, under the MIT license (see the license included in the app).
- **[memories-decomp](https://github.com/krystalgamer/memories-decomp)**: the game's decompilation, by its authors.
- **SDL3, FreeType, libpng and zlib**: their licenses ship inside the app (`licenses/`).
- The iOS port's code: [muguiwara23/port-eame-yfm](https://github.com/muguiwara23/port-eame-yfm/tree/port-eame/ios), branch `port-eame/ios`.

A non-profit fan project, not affiliated with Konami.
*Yu-Gi-Oh!* and *Forbidden Memories* belong to Konami. No game data is distributed.
