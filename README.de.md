<p align="center">
  <img alt="VoxSpica" src="images/voxspica_en.png" width="620">
</p>

<h1 align="center">VoxSpica</h1>

<p align="center">
  <b>Diktieren und Sprache-zu-Text für Windows, das Ihre Stimme nirgendwohin schickt.</b><br>
  <sub>Ihre Stimme bleibt auf Ihrem Rechner. Kein Konto, kein Abo, keine Cloud.</sub>
</p>

<p align="center">
  <a href="https://github.com/alex37529/voxspica/releases"><img alt="Herunterladen" src="https://img.shields.io/badge/herunterladen-releases-2C7BE0?style=for-the-badge"></a>
  <a href="docs/USER-GUIDE.md"><img alt="Anleitung" src="https://img.shields.io/badge/anleitung-0B1620?style=for-the-badge"></a>
  <a href="https://voxspica.4crytobot.xyz"><img alt="Website" src="https://img.shields.io/badge/website-voxspica.4crytobot.xyz-0B1620?style=for-the-badge"></a>
</p>

<p align="center">
  <img alt="Windows" src="https://img.shields.io/badge/Windows-10%20%2F%2011%20x64-0B1620?style=flat-square">
  <img alt="Lizenz" src="https://img.shields.io/badge/lizenz-Apache--2.0-2C7BE0?style=flat-square">
  <img alt="Sprachen der Oberfläche" src="https://img.shields.io/badge/oberfläche-9%20sprachen-0B1620?style=flat-square">
  <img alt="Erkennungssprachen" src="https://img.shields.io/badge/erkennung-33%20sprachen-0B1620?style=flat-square">
  <img alt="Motor" src="https://img.shields.io/badge/ASR-VOSK%20(Kaldi)-0B1620?style=flat-square">
</p>

<p align="center">
  <sub><a href="README.md">English</a> · <a href="README.de.md">Deutsch</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a> · <a href="README.it.md">Italiano</a> · <a href="README.ru.md">Русский</a> · <a href="README.zh.md">简体中文</a></sub>
</p>

---

## Was es ist

VoxSpica wandelt Sprache unter Windows in Text um, und nichts verlässt den
Rechner. Die Erkennung übernimmt [VOSK](https://alphacephei.com/vosk/), eine
Desktop-Build von Kaldi, quelloffen, die auf Ihrer CPU läuft. Keine GPU, kein
Netz, kein Telemetrie.

Es funktioniert auf zwei Arten:

- **Live-Diktieren** vom Mikrofon, der Text erscheint während des Sprechens.
- **Dateien transkribieren** für alles, was das System abspielen kann: mp3, m4a,
  wav und weitere, wenn [ffmpeg](https://ffmpeg.org/) im Pfad liegt.

Jede Erkennung landet in einer lokalen Datenbank, in der Sie suchen können.

## Warum offline

Die Dikttierdienste, die Sie vielleicht benutzt haben, schicken Ihr Audio an
den Server von jemand anderem. Für sie ist das eine vernünftige Konstruktion
und für ein Werkzeug schlecht, dessen Aufgabe es ist, festzuhalten, was Sie
gerade laut gesagt haben — und das ist oft ein vertrauliches Dokument, der Name
eines Kunden oder ein Gedanke, den Sie noch nicht veröffentlichen wollen.

Hier ist die Antwort strukturell und nicht zugesichert: Das Modell liegt auf
Ihrer Platte, die Datenbank liegt auf Ihrer Platte, und im Programm gibt es
keine einzige Stelle, die eine Verbindung öffnet.

<p align="center">
  <img alt="Auswahl der Oberflächensprache" src="images/voxspica_interface_language.png" width="820">
  <br>
  <sub>Die Oberfläche spricht neun Sprachen, jede in ihrer eigenen Sprache benannt.</sub>
</p>

## Die Fenster

<table>
<tr>
<td width="50%" align="center" valign="top">
  <img alt="Verwaltung der Erkennungsmodelle" src="images/voxspica_models.png"><br>
  <sub><b>Modelle</b> — jede Sprache, ihre Größen und was der Download kostet.</sub>
</td>
<td width="50%" align="center" valign="top">
  <img alt="Mikrofon auswählen" src="images/voxspica_device.png"><br>
  <sub><b>Gerät</b> — Mikrofon wählen, mit seiner echten Abtastrate.</sub>
</td>
</tr>
<tr>
<td width="50%" align="center" valign="top">
  <img alt="Verlauf der Erkennungen" src="images/voxspica_history.png"><br>
  <sub><b>Verlauf</b> — jede Erkennung, durchsuchbar, löschbar, kopierbar.</sub>
</td>
<td width="50%" align="center" valign="top">
  <img alt="Auswahl der Oberflächensprache" src="images/voxspica_interface_language.png"><br>
  <sub><b>Oberfläche</b> — Sprache jederzeit umschalten.</sub>
</td>
</tr>
</table>

## Herunterladen

<table>
<tr>
<th align="left" width="50%">Installateur pro Sprache</th>
<th align="left" width="50%">Portables Archiv</th>
</tr>
<tr>
<td valign="top">

Sieben Installateure, einer pro Oberflächensprache. Jeder bringt ein fertiges
Erkennungsmodell für seine Sprache mit, deshalb funktioniert der erste Start
ganz ohne Internet. Wählen Sie Ihres, die Links stehen direkt darunter.

</td>
<td valign="top">

Eine einzige <code>VoxSpica.exe</code> in einem Zip. Es wird nichts installiert,
nichts ins System geschrieben, und der Ordner darf auf einem USB-Stick liegen.
Oberflächensprache und Modell wählen Sie beim ersten Start.

Die portablen Fassungen liegen in den [Releases](https://github.com/alex37529/voxspica/releases).

</td>
</tr>
</table>

### Die sieben Installateure

Basisadresse: <https://voxspica.4crytobot.xyz/downloads>

- <img src="https://flagcdn.com/16x12/gb.png" width="16" alt="GB"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-en-setup.exe"><code>VoxSpica-0.1.4-en-setup.exe</code></a> — English, 101.1 MB
- <img src="https://flagcdn.com/16x12/ru.png" width="16" alt="RU"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-ru-setup.exe"><code>VoxSpica-0.1.4-ru-setup.exe</code></a> — Русский, 106.1 MB
- <img src="https://flagcdn.com/16x12/de.png" width="16" alt="DE"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-de-setup.exe"><code>VoxSpica-0.1.4-de-setup.exe</code></a> — Deutsch, 106.1 MB
- <img src="https://flagcdn.com/16x12/fr.png" width="16" alt="FR"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-fr-setup.exe"><code>VoxSpica-0.1.4-fr-setup.exe</code></a> — Français, 102.4 MB
- <img src="https://flagcdn.com/16x12/es.png" width="16" alt="ES"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-es-setup.exe"><code>VoxSpica-0.1.4-es-setup.exe</code></a> — Español, 99.6 MB
- <img src="https://flagcdn.com/16x12/it.png" width="16" alt="IT"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-it-setup.exe"><code>VoxSpica-0.1.4-it-setup.exe</code></a> — Italiano, 109.5 MB
- <img src="https://flagcdn.com/16x12/cn.png" width="16" alt="CN"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-zh-setup.exe"><code>VoxSpica-0.1.4-zh-setup.exe</code></a> — 简体中文, 103.8 MB

Die Liste nennt eine Version und wird bei jeder Veröffentlichung ersetzt. Das
portable Archiv steht absichtlich nicht darin: es liegt im Release, und es ist
das Richtige, wenn Sie eine Oberflächensprache brauchen, die nicht auf der Liste
steht. Die Flaggen kommen von [flagcdn.com](https://flagcdn.com) und bezeichnen
die Sprache, nicht das Land: Englisch ist 🇬🇧 und nicht 🇺🇸, weil die Oberfläche
`en` heißt und nicht `en-US`, und kein Installateur bringt eine
US-Oberfläche mit. Ist flagcdn nicht erreichbar, funktionieren die Links
trotzdem, nur die Bilder verschwinden.

> **Windows wird warnen.** Die Builds sind nicht signiert, also meldet
> SmartScreen einen unbekannten Herausgeber. Klicken Sie auf *Weitere Infos* →
> *Trotzdem ausführen*. Siehe [was das Programm nicht kann](#was-das-programm-nicht-kann):
> die Signatur steht auf der Liste.

## Erster Start

1. Starten Sie das Programm. Beim ersten Start fragt es die Oberflächensprache.
2. Wählen Sie die **Erkennungssprache** — die Sprache, in der Sie *sprechen*
   werden. Das ist etwas anderes als die Oberflächensprache und hängt nicht
   davon ab.
3. Laden Sie das passende Modell. Das **kleine** ist rund 50 MB groß und reicht
   für Entwürfe; das **große** ist genauer, braucht etwa 8 GB RAM und braucht
   beim ersten Start einer Sitzung 60 bis 90 Sekunden.
4. Mikrofon wählen, auf Aufnahme drücken, sprechen.

Die [Anleitung](docs/USER-GUIDE.md) geht jedes Fenster durch, auch was zu tun
ist, wenn ein Modell fehlt, und wie sich kleine und große Modelle unterscheiden.

## Sprachen

Die **Oberfläche** gibt es in neun Sprachen: Weißrussisch, Deutsch, Englisch,
Spanisch, Französisch, Italienisch, Russisch, Ukrainisch, Chinesisch
(vereinfacht).

Die **Erkennung** funktioniert in 33 Sprachen. Sie sind mit ihren Modellnamen in
[docs/LANGUAGES.md](docs/LANGUAGES.md) aufgeführt. Erkennung und Oberfläche
sind unabhängig voneinander — Sie können Ukrainisch diktieren und eine englische
Oberfläche haben.

## Kommandozeile

Das Programm ist nicht nur ein Fenster. Alles, was es kann, geht auch von der
Kommandozeile — das ist es, was Sie in einem Skript oder einem Hotkey-Launcher
brauchen:

```powershell
VoxSpica.exe mic --lang de --size small      # diktieren, Text auf stdout
VoxSpica.exe file meeting.mp3 --lang en-us   # Datei transkribieren
VoxSpica.exe devices                         # Mikrofone auflisten
VoxSpica.exe download --lang de --size small
VoxSpica.exe list                            # Sprachen und ihre Modelle
VoxSpica.exe history --search "Besprechung"  # was zuletzt erkannt wurde
```

## Was das Programm nicht kann

Ehrlich aufgeschrieben, weil das der Teil ist, den man gewöhnlich später
herausfindet.

- **Nicht signiert.** Windows zeigt bei jeder Installation eine
  SmartScreen-Warnung.
- **Keine Kommas.** VOSK gibt Wörter ohne Satzzeichen aus. VoxSpica stellt
  Großschreibung wieder her und setzt am Satzende einen Punkt, aber es kann
  keine Kommas setzen, ohne die Syntax zu zerlegen: jede einfache Regel ergibt
  „Wie, geht's dir?“ statt „Wie geht's dir?“.
- **Nur Windows x64.** Es gibt keine Builds für macOS und Linux.
- **Modelle sind separat.** Außer den Installateuren pro Sprache bringt keine
  Datei ein Modell mit, und die Modelle wiegen 50 MB bis 1,8 GB. Die
  Installateure pro Sprache sind die Ausnahme: jeder bringt eins mit.

## Über dieses Repository

Hier liegen **nur die Releases**. Der Quellcode ist nicht öffentlich und nicht
hier gespiegelt — in diesem Repository ist nichts davon zu finden. Die Tags
`vX.Y.Z` zeigen auf den kleinen öffentlichen Commit, der diese Datei
einführt, nicht auf Anwendungscode. Die an jedes Release angehängten Dateien
sind kompilierte Binärdateien.

Website: <https://voxspica.4crytobot.xyz>

## Lizenz

Apache-2.0, siehe [LICENSE](LICENSE). Die Erkennung übernimmt
[VOSK](https://alphacephei.com/vosk/) (Apache-2.0); die Erkennungsmodelle
verteilt Alpha Cephei ebenfalls unter Apache-2.0.
