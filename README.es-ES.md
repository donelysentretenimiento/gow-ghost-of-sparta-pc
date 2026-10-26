# Sparta ES — by Donelys

**God of War: Ghost of Sparta (PSP) para Android, con la interfaz y el audio de las cinemáticas en español de España.**

[English](README.md) · [Português (Brasil)](README.pt-BR.md) · **Español (España)**

Sparta ES es una versión adaptada de [Sparta](https://github.com/arnaldolima1/gow-ghost-of-sparta-pc), el port nativo de *God of War: Ghost of Sparta* creado por **arnaldolima1** sobre **PortableKit** (TeamGDB). Este proyecto no es el port original ni lo sustituye: es una adaptación independiente y no oficial, mantenida por Donelys, que puede instalarse junto al Sparta oficial.

> [!IMPORTANT]
> **No se incluye ningún recurso del juego.** El APK no contiene la ISO, ni vídeos, ni audio, ni texturas, ni ningún otro archivo del disco. Hace falta tu propia copia de la edición europea, **`UCES-01401`**, como `.iso` sin comprimir: la app te la pide en el dispositivo la primera vez que se abre. Igual que en el proyecto original, la aplicación lleva el código del juego ya recompilado a código nativo; los datos del juego siguen saliendo siempre de tu ISO.

## Qué aporta respecto al Sparta original

- **Interfaz en español de España** (launcher, menús, ajustes, explorador de archivos, avisos y ayudas), además de English y Português (Brasil). Se detecta solo cuando Android está en español, y se puede cambiar en *Ajustes del sistema → Idioma de la interfaz*.
- **Idioma del juego**, aparte del de la interfaz: español por defecto en la edición europea. Se puede elegir entre los cinco idiomas que trae el disco (English, Français, Español, Deutsch, Italiano). Se aplica la próxima vez que arranque el juego.
- **Doblaje de las cinemáticas.** Las películas del disco llevan cinco pistas de audio, una por idioma, y el port original solo leía la primera. Ahora se reproduce la pista que pide el juego, igual que hace PPSSPP. La única película con una sola pista (`R6_DEMO_ENDMOVIE`) no cambia.
- **Créditos**: «Traducción española por Donelys» en la pantalla principal y «Sparta ES — by Donelys» en *Acerca de*.
- **Coexistencia**: el identificador de la aplicación es `io.sparta.es`, distinto del oficial (`io.sparta`), así que no toca sus datos.

No se ha modificado la ISO, ni las voces, ni los textos del juego: los textos y las voces en español son los del propio disco.

## Requisitos

- Android 10 o superior, ARM64 y Vulkan 1.1.
- Tu propia ISO de la edición europea (`UCES-01401`, versión 1.00) sin comprimir y sin modificar. Unos 2 GB libres para copiarla.

## Limitaciones conocidas

- Es una versión alfa, como el proyecto original: puede haber fallos gráficos o cierres.
- El audio es el que trae tu disco: lo que no esté doblado en la ISO sigue en su idioma original.
- El APK está firmado con una clave propia de Donelys. Solo se actualiza sobre una instalación de Sparta ES firmada con esa misma clave, y no sobre el Sparta oficial.
- Compatibilidad con dispositivos concretos: no se garantiza más allá de lo probado.

## Compilar y mantener

- Rama de trabajo: `feature/spanish-es-android`. El submódulo `portablekit` apunta al fork [donelysentretenimiento/PortableKit](https://github.com/donelysentretenimiento/PortableKit), rama `feature/spanish-es`.
- Las traducciones están en `portablekit/host/ui/i18n_es.cpp`, aparte de la tabla portuguesa, para que las actualizaciones del original se fusionen sin conflictos.
- Compilación Android: `SPARTA_APP_ID=io.sparta.es scripts/build_android.sh`, con el código recompilado en `generated/` (`scripts/generate.sh`) y una clave propia (`KEYSTORE`, `KEYSTORE_PASS`, `KEY_ALIAS`). La clave no se sube nunca al repositorio.
- Pruebas del selector de audio: `portablekit_psmf_demuxer_tests`.

## Créditos y licencias

- **Sparta**: arnaldolima1 y colaboradores. **PortableKit**: TeamGDB. Se conservan todas las licencias y avisos del proyecto original y de sus dependencias (SDL3, Dear ImGui, FFmpeg, Noto Sans CJK, entre otras); véase `LICENSE` y `packaging/THIRD_PARTY_NOTICES.md`.
- **Traducción al español de España y adaptación del launcher**: Donelys.
- *God of War* es una marca de Sony Interactive Entertainment. Este proyecto no está afiliado a Sony Interactive Entertainment ni a Santa Monica Studio.
