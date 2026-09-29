# VoxSpica — Speech to Text, offline
<br>
<p align="center">
<img alt="VoxSpica" src="images/voxspica_en.png" width="80%">
</p>
<br>
**Free speech recognition for Windows that never sends your data to the
internet.**

Microphone dictation and audio file transcription powered by
[VOSK](https://alphacephei.com/vosk/) (Kaldi ASR) — local, on CPU, no GPU, no
cloud. 30+ recognition languages, 9 interface languages.

<p align="center">
  <a href="LICENSE"><img alt="License: Apache-2.0" src="https://img.shields.io/badge/license-Apache--2.0-blue.svg"></a>
  <img alt="Platform" src="https://img.shields.io/badge/platform-Windows%2010%20%2F%2011%20x64-0078D4">
  <img alt="ASR engine" src="https://img.shields.io/badge/ASR-VOSK-4B8B3F">
  <img alt="Privacy" src="https://img.shields.io/badge/privacy-100%25%20offline-success">
  <img alt="Interface languages" src="https://img.shields.io/badge/UI-9%20languages-6E7781">
  <img alt="Recognition languages" src="https://img.shields.io/badge/ASR-33%20languages-6E7781">
</p>

## Why VoxSpica

- **Free** — no subscription, no payment, no ads.
- **Private** — recordings and texts stay on your computer.
- **Offline** — once a model is downloaded, no internet is needed.
- **Live transcription** — the text appears while you speak, with pause and stop.
- **History** — every recognition is stored in SQLite and is searchable.

## Download

Go to the [Releases](https://github.com/alex37529/voxspica/releases) page and
download portable version `VoxSpica-<version>-win64.zip`. The archive holds a single executable —
there is nothing else to install, and Python is not required.

On first launch the app asks for the interface language and offers to download a
recognition model for the language you picked. **Models are not bundled** (50 MB
to 1.8 GB each): they are downloaded once and stored next to the app.

Windows may show a SmartScreen warning — the builds are not code-signed. Choose
"More info" → "Run anyway".

The SHA256 of every archive is in `SHA256SUMS.txt` next to it in the same
release.

## Installers

Per-language installers. Each one is in its own language and each carries a
ready small recognition model for that language, so the first start works
offline with nothing left to download. Pick the line for your language and
untick it when you have the file:

Base URL: <https://voxspica.4crytobot.xyz/downloads>

- <img src="https://flagcdn.com/16x12/gb.png" width="16" alt="GB"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-en-setup.exe"><code>VoxSpica-0.1.4-en-setup.exe</code></a> — English, 101.1 MB
- <img src="https://flagcdn.com/16x12/ru.png" width="16" alt="RU"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-ru-setup.exe"><code>VoxSpica-0.1.4-ru-setup.exe</code></a> — Russian, 106.1 MB
- <img src="https://flagcdn.com/16x12/de.png" width="16" alt="DE"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-de-setup.exe"><code>VoxSpica-0.1.4-de-setup.exe</code></a> — German, 106.1 MB
- <img src="https://flagcdn.com/16x12/fr.png" width="16" alt="FR"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-fr-setup.exe"><code>VoxSpica-0.1.4-fr-setup.exe</code></a> — French, 102.4 MB
- <img src="https://flagcdn.com/16x12/es.png" width="16" alt="ES"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-es-setup.exe"><code>VoxSpica-0.1.4-es-setup.exe</code></a> — Spanish, 99.6 MB
- <img src="https://flagcdn.com/16x12/it.png" width="16" alt="IT"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-it-setup.exe"><code>VoxSpica-0.1.4-it-setup.exe</code></a> — Italian, 109.5 MB
- <img src="https://flagcdn.com/16x12/cn.png" width="16" alt="CN"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-zh-setup.exe"><code>VoxSpica-0.1.4-zh-setup.exe</code></a> — Chinese, 103.8 MB

The list names one version; it is replaced when a new one is published. The
portable archive above is not among these — it is in the release, and it is the
one to take if you want a different interface language than the ones listed.
The flags are the languages, not the countries: English is 🇬🇧 rather than 🇺🇸
because the interface is `en` and not `en-US` — no installer ships a
US-specific interface.

## About this repository

This repository holds **the releases only**. The source code of VoxSpica is not
public and is not mirrored here, so nothing in this repository contains it: the
`vX.Y.Z` tags point at the small public commit that introduces this file, not at
any application code. The files attached to each release are built binaries.

Website: <https://voxspica.4crytobot.xyz>

## License

Apache-2.0, see [LICENSE](LICENSE). Recognition is done by
[VOSK](https://alphacephei.com/vosk/) (Apache-2.0); recognition models are
distributed by Alpha Cephei under the Apache-2.0 license as well.
