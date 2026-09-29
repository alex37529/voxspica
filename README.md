# VoxSpica — Speech to Text, offline
<br>
<p align="center">
<img alt="VoxSpica" src="images/voxspica_en.png" width="60%">
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
download `VoxSpica-<version>-win64.zip`. The archive holds a single executable —
there is nothing else to install, and Python is not required.

On first launch the app asks for the interface language and offers to download a
recognition model for the language you picked. **Models are not bundled** (50 MB
to 1.8 GB each): they are downloaded once and stored next to the app.

Windows may show a SmartScreen warning — the builds are not code-signed. Choose
"More info" → "Run anyway".

The SHA256 of every archive is in `SHA256SUMS.txt` next to it in the same
release.

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
