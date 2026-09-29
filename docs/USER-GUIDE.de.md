# Anleitung

<p align="center">
  <sub>[English](USER-GUIDE.md) · [Español](USER-GUIDE.es.md) · [Français](USER-GUIDE.fr.md) · [Italiano](USER-GUIDE.it.md) · [Русский](USER-GUIDE.ru.md)</sub>
</p>

VoxSpica erkennt Sprache unter Windows, ohne Audio irgendwohin zu schicken. Diese
Anleitung geht die Fenster in der Reihenfolge durch, in der sie Ihnen begegnen.

- [Installieren](#installieren)
- [Das Hauptfenster](#das-hauptfenster)
- [Erkennungssprache wählen](#erkennungssprache-wählen)
- [Ein Modell laden](#ein-modell-laden)
- [Klein oder groß?](#klein-oder-groß)
- [Mikrofon wählen](#mikrofon-wählen)
- [Diktieren](#diktieren)
- [Datei transkribieren](#datei-transkribieren)
- [Verlauf](#verlauf)
- [Oberflächensprache wechseln](#oberflächensprache-wechseln)
- [Kommandozeile](#kommandozeile)
- [Wenn etwas nicht klappt](#wenn-etwas-nicht-klappt)

---

## Installieren

Es gibt zwei Wege, und der Unterschied ist wichtig, wenn Ihnen der erste Start
am Herzen liegt.

**Der Installateur pro Sprache** installiert das Programm unter „Programme“ und
legt ein Erkennungsmodell für diese Sprache daneben. Es gibt sieben, einen pro
Oberflächensprache: Englisch, Russisch, Deutsch, Französisch, Spanisch,
Italienisch und Chinesisch. Weil das Modell schon da ist, braucht der erste
Start kein Internet.

**Das portable Archiv** ist eine einzelne `VoxSpica.exe` in einem Zip. Es wird
nichts installiert und nichts ins System geschrieben — der Ordner darf auf einem
USB-Stick liegen. Der Preis dafür ist der erste Start: das Programm fragt die
Oberflächensprache ab und lädt dann ein Modell, braucht also einmal Netz.

> **Windows wird warnen.** Die Builds sind nicht signiert. SmartScreen meldet
> einen unbekannten Herausgeber, und das sieht genauso aus wie Schadsoftware.
> Klicken Sie auf *Weitere Infos* → *Trotzdem ausführen*.

## Das Hauptfenster

Alles liegt in einem Fenster, drei Einstellungsseiten dahinter im Menü
`Settings`.

| Bedienelement | Wirkung |
| --- | --- |
| **Recognition language** | Die Sprache, in der Sie *sprechen*. Siehe unten. |
| **Model** | Welche Modellgröße: klein oder groß. |
| **Microphone** | Von welchem Gerät aufgenommen wird. |
| ● / ❙❙ / ■ | Aufnehmen, Pause, Stopp. |
| **Transcribe file** | Audiodatei wählen und erkennen. |
| **Copy text** | Erkannten Text in die Zwischenablage legen. |
| Statuszeile | Was das Programm tut und wie lange der letzte Ladevorgang brauchte. |

Die Statuszeile meldet, wann das Modell bereit ist. Wer vorher aufnimmt,
wartet.

## Erkennungssprache wählen

**Erkennungssprache und Oberflächensprache sind zwei verschiedene
Einstellungen.**

Die *Erkennungssprache* ist die, in der Sie sprechen. Sie entscheidet, welches
Modell geladen werden muss. Die *Oberflächensprache* ist die, in der die
Schaltflächen beschriftet sind. Beide sind unabhängig — Sie können Ukrainisch
dik tieren und eine englische Oberfläche haben, und der Installateur stellt
genauso ein.

Die Sprache wird über ihren VOSK-Code gewählt, nicht über ein Land. `en-us` und
`en-in` sind Englisch für unterschiedliche Akzente, `el-gr` ist Griechisch, `cn`
ist Mandarin, `uk` ist Ukrainisch.

Alle 33 Codes mit ihren Modellen stehen in [LANGUAGES.md](LANGUAGES.md).

## Ein Modell laden

Modelle sind nicht Teil des Programms. Sie werden einmal geladen, neben der
Anwendung abgelegt und können jederzeit entfernt werden.

Öffnen Sie `Settings` → **Models**. Links steht jede Sprache des Registers mit
den Größen, die es dafür gibt. Eine Auswahl zeigt rechts, was sie kostet:

- eine Karte für das **kleine** Modell mit seiner Größe auf der Platte und den
  Schaltflächen **Delete** und **Warm up in memory**;
- eine Karte für das **große** Modell mit der Schaltfläche **Download**.

Manche Sprache hat nur eine Größe: im Register gibt es kein `small` für Arabisch,
Brasilianisch-Portugiesisch, Griechisch und Tagalog und kein `large` für
Katalanisch, Tschechisch, Estnisch, Koreanisch, Polnisch, Schwedisch, Telugu,
Türkisch und Usbekisch. Die Seite sagt das, statt einen Download anzubieten, der
nicht funktionieren würde.

Modelle werden beim Start im Hintergrund geladen, deshalb beginnt die Aufnahme
nach dem Aufwärmen sofort.

## Klein oder groß?

| | klein | groß |
| --- | --- | --- |
| Größe auf der Platte | etwa 50 MB | etwa 1,8 GB |
| Ladezeit | Sekunden | 60–90 s beim ersten Mal |
| Arbeitsspeicher | ein paar hundert MB | rund 8 GB |
| Genauigkeit | reicht für Entwürfe | spürbar besser |

Das Hauptfenster weist auf die Ladezeit hin, weil das der Teil überrascht: Das
große Modell braucht nicht nur länger, es liest beim ersten Start einer Sitzung
anderthalb Minuten von der Platte.

**Fangen Sie mit klein an.** Wechseln Sie zu groß, wenn Sie ein Protokoll
brauchen, das zitiert wird — ein Interview, ein Zitat, ein Name, den man nicht
raten kann.

## Mikrofon wählen

`Settings` → **Device** listet alle Eingaben, die das System meldet, mit Index,
Namen und Abtastrate. *Default* ist die Systemvorgabe; mit einem Sternchen
sind die Geräte markiert, die das System als Vorgabe behandelt.

Ein Mikrofon mit 2 kHz ist keine echte Aufnahme — das ist eine Schleife oder
ein virtueller Endpunkt. Wählen Sie das, dessen Rate Ihnen vertraut ist, meist
16 kHz oder 44,1/48 kHz.

## Diktieren

1. Warten Sie, bis die Statuszeile das Modell als bereit meldet.
2. Mikrofon wählen.
3. Auf die Aufnahmeschaltfläche oder das Mikrofon-Symbol drücken.
4. Sprechen. Der Text erscheint währenddessen.
5. Stopp drücken. Für eine Pause die Pause taste.
6. **Copy text** legt das Ergebnis in die Zwischenablage.

Transkripte landen neben dem Programm, und jede Erkennung kommt in den Verlauf.

## Datei transkribieren

**Transcribe file** öffnet eine Dateiauswahl. WAV liest das Programm selbst; für
mp3, m4a, ogg und Ähnliches braucht es
[ffmpeg](https://ffmpeg.org/download.html) im `PATH` — unter Windows genügt
`winget install Gyan.FFmpeg`.

Die Datei läuft in einem Durchgang, was für die meisten Aufnahmen schneller ist
als in Echtzeit.

## Verlauf

Jede Erkennung liegt lokal in SQLite und erscheint im Verlaufsfenster.

Die Tabelle zeigt Kennung, Datum und Uhrzeit, Quelle (Mikrofon oder Datei),
Sprache, Dauer des Audios und eine Vorschau des Textes. Das Suchfeld filtert
über den Text; **Find** wendet den Filter an, **Show all** hebt ihn auf.

Eine markierte Zeile zeigt unten den ganzen Text. Von dort aus geht
**Copy text**, **Delete entry** oder **Clear history** für alles auf einmal.

Der Verlauf ist eine einfache SQLite-Datei im Benutzerprofil. Nichts wird
hochgeladen, und die Datei zu löschen löscht den Verlauf.

## Oberflächensprache wechseln

`Settings` → **Interface**. Neun Sprachen, jede in ihrer eigenen Sprache
aufgeführt: Беларуская, Deutsch, English, Español, Français, Italiano, Русский,
Українська, 简体中文.

Die Wahl gilt sofort. Beim ersten Start eines portablen Builds erscheint
dasselbe Fenster vor allem anderen.

![Oberflächensprache wählen](../images/voxspica_interface_language.png)

## Kommandozeile

Die Programmdatei funktioniert auch in der Konsole, und zwar genau so — das ist
die Form für Skripte und für Tastenkürzel-Launcher.

```powershell
VoxSpica.exe mic --lang de --size small       # diktieren, Text auf stdout
VoxSpica.exe file meeting.mp3 --lang en-us    # Datei transkribieren
VoxSpica.exe devices                          # Eingabegeräte auflisten
VoxSpica.exe list                             # Sprachen und ihre Modelle
VoxSpica.exe download --lang de --size small  # Modell laden
VoxSpica.exe history --search "Besprechung"   # frühere Erkennungen durchsuchen
VoxSpica.exe history show 3                   # einen Eintrag vollständig
VoxSpica.exe config lang=fr size=large        # eine Wahl merken
```

Nützliche Schalter bei den Aufnahmebefehlen:

| Schalter | Wirkung |
| --- | --- |
| `--no-punct` | Genau das, was VOSK gesagt hat: ohne Großschreibung und Punkt |
| `--no-history` | Ergebnis nicht in den Verlauf schreiben |
| `-o DATEI` | In eine Datei schreiben statt nach stdout |
| `--device N` | Ein bestimmtes Mikrofon nach Index |

Einstellungen folgen einer Regel: eingebaute Werte, dann die Einstellungen des
Installateurs, dann Ihre Datei, dann die Kommandozeile. Ein einmaliges
`--lang en-us` ändert also nicht, was das Fenster beim nächsten Mal benutzt.

## Wenn etwas nicht klappt

**„Model required“ beim Start.** Das Programm sucht ein Modell in der Sprache,
die Ihre Einstellungen nennen, und findet keins. Zwei Ursachen:

- die Einstellungen nennen eine Sprache aus einer früheren Installation, deren
  Modell mitgegangen ist — wählen Sie in `Settings` → **Models** die Sprache,
  die Sie tatsächlich haben;
- das Modell ist da, aber in der anderen Größe — prüfen Sie, ob **Model** im
  Hauptfenster zum Installierten passt.

**SmartScreen blockiert den Installateur.** Erwartet: die Builds sind nicht
signiert. *Weitere Infos* → *Trotzdem ausführen*.

**Im Text fehlen Kommas.** Erwartet, siehe README. VOSK liefert keine
Satzzeichen, und sie ohne Sprachmodell zu rekonstruieren ergibt Schlimmeres als
keine.

**„Die vorhandene Datei kann nicht zum Schreiben geöffnet werden.“** Modelle und
Transkripte liegen neben dem Programm. Unter `C:\Program Files` darf ein
normaler Benutzer nicht schreiben, also weicht das Programm nach
`%LOCALAPPDATA%\VoxSpica` aus und sagt es an.

**Zwei Kopien starten nicht.** Die zweite sieht die erste und verweigert den
Dienst. Das ist Absicht: zwei Kopien würden sich in der Einstellungsdatei, der
Verlaufsdatenbank und dem Modellverzeichnis in die Quere kommen. Schließen Sie
die erste oder setzen Sie `VOXSPICA_NO_SINGLE_INSTANCE=1`.

**Ein Modell lädt und verschwindet wieder.** Ein Download, der die
Integritätsprüfung nicht besteht, wird gelöscht statt halb geschrieben
zurückzulassen. Laden Sie es erneut; wiederholt es sich, bricht das Netz die
Übertragung ab.

---

## Siehe auch

- [LANGUAGES.md](LANGUAGES.md) — alle 33 Erkennungssprachen und ihre Modelle
- [Anleitung auf Russisch](USER-GUIDE.ru.md) · [中文 README](../README.zh.md) · [English](../README.md)
- <https://voxspica.4crytobot.xyz> — die Website
