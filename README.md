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

A native iOS port of **YFM Re-Decomp** (the PC version built from the game's decompilation). Not an emulator.

- Modern touch controls, an iOS-style options menu, the HD graphics options, audio, video, saves and save states,
  and the bundled mods (3D Monsters, Hand Camera, AI Hard Mode, Yamyi mods, Drop Missing Cards).
- **Requirements:** a 64-bit iPhone or iPad on **iOS 16+**. Tested on an iPhone 12 Pro (A14), iOS 27.
  Install with AltStore, SideStore, FlareStore, LiveContainer, etc. **No JIT needed.**
- **You need your own disc image:** the `.bin` of Yu-Gi-Oh! Forbidden Memories, **USA (SLUS-01411)**. None is included.

**First launch:** open the app, tap **Choose ROM...** (it shows an error in this version — close the app),
then in the **Files** app put your `.bin` in the app's `Documents/game` folder and open the game again.

Credits: [YFM Re-Decomp](https://github.com/Unchiga/Yu-Gi-Oh-Forbidden-Memories-Recompiled) (MIT),
[memories-decomp](https://github.com/krystalgamer/memories-decomp), SDL3, FreeType, libpng, zlib.
iOS source: [muguiwara23/port-eame-yfm](https://github.com/muguiwara23/port-eame-yfm/tree/port-eame/ios).
Fan project, not affiliated with Konami. *Yu-Gi-Oh!* and *Forbidden Memories* belong to Konami. No game data is distributed.
