# User guide

<p align="center">
  <sub>[Deutsch](USER-GUIDE.de.md) · [Español](USER-GUIDE.es.md) · [Français](USER-GUIDE.fr.md) · [Italiano](USER-GUIDE.it.md) · [Русский](USER-GUIDE.ru.md)</sub>
</p>

VoxSpica recognises speech on Windows without sending audio anywhere. This guide
walks through the screens in the order you meet them.

- [Installing](#installing)
- [The main window](#the-main-window)
- [Choosing the recognition language](#choosing-the-recognition-language)
- [Downloading a model](#downloading-a-model)
- [Small or large?](#small-or-large)
- [Choosing a microphone](#choosing-a-microphone)
- [Dictating](#dictating)
- [Transcribing a file](#transcribing-a-file)
- [History](#history)
- [Changing the interface language](#changing-the-interface-language)
- [Command line](#command-line)
- [When something does not work](#when-something-does-not-work)

---

## Installing

There are two ways to get the program, and the difference matters if you care
about the first launch.

**The per-language installer** installs the program under Program Files and puts
a recognition model for that language next to it. There are seven, one per
interface language: English, Russian, German, French, Spanish, Italian and
Chinese. Because the model is already there, the first launch needs no internet.

**The portable archive** is a single `VoxSpica.exe` in a zip. Nothing is
installed and nothing is written to the system — you can keep the folder on a USB
stick. The trade is the first launch: it asks for the interface language and then
downloads a model, so it needs the network once.

> **Windows will show a warning during installation.** The builds are not
> code-signed. SmartScreen reports an unknown publisher, which looks exactly
> like malware. Click *More info* → *Run anyway*.

## The main window

Everything lives in one window, with three settings screens behind the
`Settings` menu.

| Control | What it does |
| --- | --- |
| **Recognition language** | The language you will *speak*. See below. |
| **Model** | Which size of model to use: small or large. |
| **Microphone** | Which input device to record from. |
| ● / ❙❙ / ■ | Record, pause, stop. |
| **Transcribe file** | Pick an audio file and recognise it. |
| **Copy text** | Put the recognised text on the clipboard. |
| Status line | What the program is doing, and how long the last load took. |

The status line tells you when the model is ready. Recording before it says
`Model ready` will make the program wait.

## Choosing the recognition language

**Recognition language and interface language are two different settings.**

The *recognition* language is the language you speak. It decides which model
must be downloaded. The *interface* language is the language the buttons are
written in. They are independent — you can dictate Ukrainian into an English
interface, and the installer will happily set both.

The language is chosen by its VOSK code, not by a country. `en-us` and `en-in`
are English for different accents; `el-gr` is Greek; `cn` is Mandarin; `uk` is
Ukrainian.

All 33 codes, with the models that exist for each, are in
[LANGUAGES.md](LANGUAGES.md).

## Downloading a model

Models are not part of the program. They are downloaded once, kept next to the
application, and can be removed at any time.

Open `Settings` → **Models**. The left column lists every language in the
registry and which sizes exist for it. Selecting one shows what it costs:

- a card for the **small** model with its size on disk, and buttons to
  **Delete** it or **Warm up in memory**;
- a card for the **large** model, with a **Download** button.

A language may have only one size — the registry has no `small` for Arabic,
Brazilian Portuguese, Greek or Filipino, and no `large` for Catalan, Czech,
Estonian, Korean, Polish, Swedish, Telugu, Turkish or Uzbek. The tab says so
rather than offering a download that would fail.

Models are loaded in the background on start, so recording begins without
waiting once the model is warm.

![Managing recognition models](../images/voxspica_models.png)

## Small or large?

| | small | large |
| --- | --- | --- |
| Size on disk | about 50 MB | about 1.8 GB |
| Load time | seconds | 60–90 s the first time |
| Memory | a few hundred MB | roughly 8 GB |
| Accuracy | good enough for drafts | noticeably better |

The main window carries a note about the load time, because it is the part that
surprises people: the large model does not just take longer, it takes a minute
and a half on the first run of the session.

**Start with small.** Move to large when you need a transcript you are going to
quote — an interview, a statement, a name you cannot guess.

## Choosing a microphone

`Settings` → **Device** lists every input the system reports, with its index,
name and sample rate. *Default* is the system default; entries marked with a
star are the ones the system considers default devices.

A microphone listed at 2 kHz is not a real capture device — it is a loopback
or a virtual endpoint. Pick the one with a rate you recognise, usually 16 kHz or
44.1/48 kHz.

![Choosing a microphone](../images/voxspica_device.png)

## Dictating

1. Make sure the status line says the model is ready.
2. Choose the microphone.
3. Press the record button, or the microphone icon in the toolbar.
4. Talk. The text appears as you speak.
5. Press stop. Use pause if you need to think.
6. **Copy text** puts the result on the clipboard.

Transcripts are written next to the program, and every recognition is added to
the history.

## Transcribing a file

`Transcribe file` opens a file picker. The program handles WAV natively; for
mp3, m4a, ogg and similar, put
[ffmpeg](https://ffmpeg.org/download.html) on the path — `winget install
Gyan.FFmpeg` is enough on Windows.

The file is recognised in one pass, which is faster than real time for most
recordings.

## History

Every recognition is stored locally in SQLite and listed in the history window.

The table shows the id, the date and time, the source (microphone or file), the
language, the duration of the audio, and a preview of the text. The search box
filters across the text; **Find** applies it, **Show all** clears it.

Selecting a row shows the full text below. From there you can **Copy text**,
**Delete entry** or **Clear history** to remove everything at once.

The history is a plain SQLite file in your user profile. Nothing is uploaded,
and deleting it deletes the record.

![Recognition history](../images/voxspica_history.png)

## Changing the interface language

`Settings` → **Interface**. Nine languages, each listed in its own language:
Беларуская, Deutsch, English, Español, Français, Italiano, Русский, Українська,
简体中文.

The choice takes effect immediately. On the first launch of a portable build the
same dialog appears, before anything else.

![Selecting the interface language](../images/voxspica_interface_language.png)

## Command line

The executable works from a console too, and this is the form to use in scripts
or from a hotkey launcher.

```powershell
VoxSpica.exe mic --lang ru --size small       # dictate, text to stdout
VoxSpica.exe file meeting.mp3 --lang en-us    # transcribe a file
VoxSpica.exe devices                          # list input devices
VoxSpica.exe list                             # languages and their models
VoxSpica.exe download --lang ru --size small  # fetch a model
VoxSpica.exe history --search "meeting"       # search past recognitions
VoxSpica.exe history show 3                   # one entry in full
VoxSpica.exe config lang=de size=large        # remember a choice
```

Useful switches on the recording commands:

| Switch | Effect |
| --- | --- |
| `--no-punct` | Exactly what VOSK said, without capitalisation or a full stop |
| `--no-history` | Do not write the result to the history |
| `-o FILE` | Write to a file instead of stdout |
| `--device N` | Use a specific microphone by index |

Settings follow one rule: built-in defaults, then the installer's settings, then
your settings file, then the command line. So a one-off
`--lang en-us` does not change what the window will use next time.

## When something does not work

**"Model required" on start.** The program is looking for a model in the
language your settings name, and there is none. Two causes:

- the settings name a language from a previous install, and that model went
  with it — pick the language you actually have in `Settings` → **Models**;
- the model is there but for the other size — check that `Model` in the main
  window matches what is installed.

**SmartScreen blocks the installer.** Expected: the builds are not signed. *More
info* → *Run anyway*.

**No commas in the output.** Expected, see the README. VOSK does not produce
punctuation and reconstructing it without a syntax model produces worse results
than none.

**"You can't open the existing file for writing".** The models and transcripts
live next to the program. Under `C:\Program Files` a normal user cannot write
there, so the program falls back to `%LOCALAPPDATA%\VoxSpica` and says so.

**Two copies will not start.** The second one sees the first and says so. This
is on purpose — two copies would fight over the settings file, the history
database and the model directory. Close the first, or set
`VOXSPICA_NO_SINGLE_INSTANCE=1`.

**A model downloads and then vanishes.** A download that did not finish its
integrity check is deleted rather than left half-written. Download it again; if
it repeats, the network is cutting the transfer.

---

## See also

- [LANGUAGES.md](LANGUAGES.md) — all 33 recognition languages and their models
- [INSTALL-LINUX.md](INSTALL-LINUX.md) — installing on Ubuntu and Debian
- [Русский](USER-GUIDE.ru.md) · [中文 README](../README.zh.md) · [Русский README](../README.ru.md)
- [README](../README.md) — what it is, and what it does not do
- <https://voxspica.4crytobot.xyz> — the website
