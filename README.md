<p align="center">
  <img alt="VoxSpica" src="images/voxspica_en.png" width="620">
</p>

<h1 align="center">VoxSpica</h1>

<p align="center">
  <b>Free speech-to-text for Windows Ubuntu/Debian that never sends your voice anywhere.</b><br>
  <sub>Your voice stays on your computer. No account, no subscription, no cloud.</sub>
</p>

<p align="center">
  <a href="https://github.com/alex37529/voxspica/releases"><img alt="Download" src="https://img.shields.io/badge/download-releases-2C7BE0?style=for-the-badge"></a>
  <a href="docs/USER-GUIDE.md"><img alt="Guide" src="https://img.shields.io/badge/docs-user%20guide-0B1620?style=for-the-badge"></a>
  <a href="https://voxspica.4crytobot.xyz"><img alt="Website" src="https://img.shields.io/badge/website-voxspica.4crytobot.xyz-0B1620?style=for-the-badge"></a>
</p>

<p align="center">
<img alt="Windows 10 / 11 x64" src="https://img.shields.io/badge/Windows-10%20%2F%2011%20x64-0078D4?style=flat-square&logo=windows&logoColor=white">
<img alt="Ubuntu 22.04" src="https://img.shields.io/badge/Ubuntu-22.04-E95420?style=flat-square&logo=ubuntu&logoColor=white">
<img alt="Debian" src="https://img.shields.io/badge/Debian-12-A81D33?style=flat-square&logo=debian&logoColor=white">
  <img alt="License" src="https://img.shields.io/badge/license-proprietary-2C7BE0?style=flat-square">
  <img alt="Interface languages" src="https://img.shields.io/badge/interface-9%20languages-0B1620?style=flat-square">
  <img alt="Recognition languages" src="https://img.shields.io/badge/recognition-33%20languages-0B1620?style=flat-square">
  <img alt="Engine" src="https://img.shields.io/badge/ASR-VOSK%20(Kaldi)-0B1620?style=flat-square">
</p>

<p align="center">
  <sub><a href="README.md">English</a> · <a href="README.de.md">Deutsch</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a> · <a href="README.it.md">Italiano</a> · <a href="README.ru.md">Русский</a> · <a href="README.zh.md">简体中文</a></sub>
</p>

---

## What it is

VoxSpica turns speech into text on Windows or Ubuntu/Debian, and nothing leaves the
machine. The recognition engine is [VOSK](https://alphacephei.com/vosk/) — a
desktop build of Kaldi, open source — running on your CPU. No GPU, no network, no telemetry.

It works two ways:

- **Live dictation** from a microphone, with the text appearing as you speak.
- **File transcription** for anything the system can play — mp3, m4a, wav, and
  others if you have [ffmpeg](https://ffmpeg.org/) on the path.

Every recognition is stored in a local database you can search later.

## Why offline

The dictation services you may have used send your audio to someone else's
server. That is a reasonable design for them and a poor one for a tool whose job
is to write down what you just said out loud — which is often a private
document, a client's name, something you have not decided to publish yet.

Here the answer is structural rather than promised: the model is on your disk,
the database is on your disk, and there is no code path that opens a socket.

<p align="center">
  <img alt="Interface language selection" src="images/voxspica_interface_language.png" width="820">
  <br>
  <sub>The interface speaks nine languages, each named in its own language.</sub>
</p>

## Screens

<table>
<tr>
<td width="50%" align="center" valign="top">
  <img alt="Managing recognition models" src="images/voxspica_models.png"><br>
  <sub><b>Models</b> — every language, its sizes, and what each one costs to download.</sub>
</td>
<td width="50%" align="center" valign="top">
  <img alt="Choosing a microphone" src="images/voxspica_device.png"><br>
  <sub><b>Device</b> — pick the microphone, with its real sample rate.</sub>
</td>
</tr>
<tr>
<td width="50%" align="center" valign="top">
  <img alt="Recognition history" src="images/voxspica_history.png"><br>
  <sub><b>History</b> — every recognition, searchable, deletable, copyable.</sub>
</td>
<td width="50%" align="center" valign="top">
  <img alt="Interface language selection" src="images/voxspica_interface_language.png"><br>
  <sub><b>Interface</b> — switch the interface language at any time.</sub>
</td>
</tr>
</table>

## Get it

<table>
<tr>
<th align="left" width="50%">Per-language installer</th>
<th align="left" width="50%">Portable archive</th>
</tr>
<tr>
<td valign="top">

Seven installers, one per interface language. Each brings a ready recognition
model for that language, so the first launch works with no internet at all.
Pick your language and untick the box once you have the file — the links are
straight below.

</td>
<td valign="top">

A single <code>VoxSpica.exe</code> in a zip. Nothing is installed, nothing is
written to the system, and the folder can live on a USB stick. You pick the
interface language and download a model on first run.

Portable builds are in [Releases](https://github.com/alex37529/voxspica/releases).

</td>
</tr>
</table>

### Scoop

If you already use [Scoop](https://scoop.sh):

```powershell
scoop bucket add voxspica https://github.com/alex37529/voxspica-scoop
scoop install voxspica
```

That installs the portable archive and puts `voxspica` on your PATH. The
manifest reads the checksum from the release's own `SHA256SUMS.txt`, so
`scoop update` picks up a new version on its own.

### The seven installers

Base URL: <https://voxspica.4crytobot.xyz/downloads>

- <img src="https://flagcdn.com/16x12/gb.png" width="16" alt="GB"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.7-en-setup.exe"><code>VoxSpica-0.1.7-en-setup.exe</code></a> — English, 113.8 MB
- <img src="https://flagcdn.com/16x12/ru.png" width="16" alt="RU"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.7-ru-setup.exe"><code>VoxSpica-0.1.7-ru-setup.exe</code></a> — Russian, 118.6 MB
- <img src="https://flagcdn.com/16x12/de.png" width="16" alt="DE"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.7-de-setup.exe"><code>VoxSpica-0.1.7-de-setup.exe</code></a> — German, 118.5 MB
- <img src="https://flagcdn.com/16x12/fr.png" width="16" alt="FR"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.7-fr-setup.exe"><code>VoxSpica-0.1.7-fr-setup.exe</code></a> — French, 115.0 MB
- <img src="https://flagcdn.com/16x12/es.png" width="16" alt="ES"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.7-es-setup.exe"><code>VoxSpica-0.1.7-es-setup.exe</code></a> — Spanish, 112.4 MB
- <img src="https://flagcdn.com/16x12/it.png" width="16" alt="IT"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.7-it-setup.exe"><code>VoxSpica-0.1.7-it-setup.exe</code></a> — Italian, 121.8 MB
- <img src="https://flagcdn.com/16x12/cn.png" width="16" alt="CN"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.7-zh-setup.exe"><code>VoxSpica-0.1.7-zh-setup.exe</code></a> — Chinese, 116.4 MB

The list names one version and is replaced when a new one is published. The
portable archive is deliberately not in it — that one is in the release, and it
is the one to take if you want an interface language that is not on this list.
The flags mark the language, not the country: English is the British flag rather
than the American one, because the interface is `en` and not `en-US`, and no
installer ships a US-specific interface. They are served by
[flagcdn.com](https://flagcdn.com); if that host is unreachable the links below
still work, only the pictures disappear.

> **Windows will warn you.** The builds are not code-signed, so SmartScreen
> shows an unknown publisher. Click *More info* → *Run anyway*. See
> [known limitations](#what-this-does-not-do) — signing is on the list. This
> is Windows only — the Ubuntu `.deb` installs normally with no such warning.

### Ubuntu / Debian

**From the APT repository** — this is the way to install. The key, then the
repository, then `apt`:

```bash
curl -fsSL https://alex37529.github.io/voxspica/voxspica-archive-keyring.asc \
  | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/voxspica.gpg
echo "deb https://alex37529.github.io/voxspica/repo/ jammy main" \
  | sudo tee /etc/apt/sources.list.d/voxspica.list
sudo apt update
sudo apt install voxspica
```

Change `jammy` to `noble` on Ubuntu 24.04. Later versions are picked up with
plain `sudo apt upgrade`.

Check the key fingerprint `F118 995C 50C1 EACB 4922 A330 DBF9 437A 1181 5D9`
against the [release notes](https://github.com/alex37529/voxspica/releases)
before trusting it.

**Or download the `.deb`** — `voxspica_0.1.7_amd64.deb` for **Ubuntu 22.04**
and **24.04** (and Debian 12 and later). It is a
[release asset](https://github.com/alex37529/voxspica/releases/tag/v0.1.7),
not in the list above:

```bash
sudo dpkg -i voxspica_0.1.7_amd64.deb
```

or from a package manager: `sudo apt install ./voxspica_0.1.7_amd64.deb`.

Worth knowing if you pick this one: opening a `.deb` file in the Software app
shows a placeholder icon, with no screenshot and no description. That view
reads no metadata at all — only the **installed** package appears properly, and
only when it came from the repository above. The recognition model is not in
either form; on first launch pick a language and download a model, same as on
Windows.

## First run

1. Start the program. On the first launch it asks for the interface language.
2. Choose the **recognition language** — the language you are going to *speak*.
   This is separate from the interface language and independent of it.
3. Download a model for it. The **small** model is around 50 MB and is enough
   for drafts; the **large** one is more accurate, needs about 8 GB of RAM and
   takes 60–90 seconds to load the first time.
4. Pick a microphone, press record, and talk.

The [user guide](docs/USER-GUIDE.md) walks through each screen, including what
to do when a model is missing and how the models differ.

## Languages

The **interface** is available in nine languages: Belarusian, German, English,
Spanish, French, Italian, Russian, Ukrainian, Chinese.

**Recognition** works in 33 languages. They are listed with their model names in
[docs/LANGUAGES.md](docs/LANGUAGES.md). Recognition and interface are
independent — you can dictate Ukrainian into an English interface.

## Command line

The program is not only a window. Everything it does is available from a
console, which is what you want in a script or a hotkey launcher:

```powershell
VoxSpica.exe mic --lang ru --size small     # dictate, print to stdout
VoxSpica.exe file meeting.mp3 --lang en-us  # transcribe a file
VoxSpica.exe devices                        # list microphones
VoxSpica.exe download --lang ru --size small
VoxSpica.exe list                           # languages and their models
VoxSpica.exe history --search "meeting"     # what was recognised before
```

## What this does not do

Written plainly, because this is the part that usually gets discovered later.

- **Not signed on Windows.** SmartScreen (a Windows tool) warns of an
  unknown publisher. Does not apply on Ubuntu.
- **No commas.** VOSK outputs words without punctuation. VoxSpica restores
  capitalisation and puts a full stop at the end of a sentence, but it cannot
  place commas without parsing syntax — any simple rule produces
  "How, are you" instead of "How are you".
- **Windows x64, and now Ubuntu (22.04+).** No macOS build.
- **Models are separate.** Nothing but the portable archive ships a model, and
  the models are 50 MB to 1.8 GB. The per-language installers are the exception:
  they carry one.

## About this repository

This repository holds **the releases only**. The source code is not public and
is not mirrored here — nothing in this repository contains it. The `vX.Y.Z` tags
point at the small public commit that introduces this file, not at any
application code. The files attached to each release are built binaries.

Website: <https://voxspica.4crytobot.xyz>

## License

Proprietary, free of use, see [LICENSE](LICENSE). Recognition is done by
[VOSK](https://alphacephei.com/vosk/) (Apache-2.0); recognition models are
distributed by Alpha Cephei under the Apache-2.0 license as well.
