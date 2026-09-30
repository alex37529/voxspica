# Guida utente

<p align="center">
  <sub>[English](USER-GUIDE.md) · [Deutsch](USER-GUIDE.de.md) · [Español](USER-GUIDE.es.md) · [Français](USER-GUIDE.fr.md) · [Русский](USER-GUIDE.ru.md)</sub>
</p>

VoxSpica riconosce la voce su Windows senza inviare l'audio da nessuna parte.
Questa guida percorre le schermate nell'ordine in cui le incontri.

- [Installazione](#installazione)
- [La finestra principale](#la-finestra-principale)
- [Scegliere la lingua di riconoscimento](#scegliere-la-lingua-di-riconoscimento)
- [Scaricare un modello](#scaricare-un-modello)
- [Piccolo o grande?](#piccolo-o-grande)
- [Scegliere il microfono](#scegliere-il-microfono)
- [Dettatura](#dettatura)
- [Trascrivere un file](#trascrivere-un-file)
- [Cronologia](#cronologia)
- [Cambiare la lingua dell'interfaccia](#cambiare-la-lingua-dellinterfaccia)
- [Riga di comando](#riga-di-comando)
- [Quando qualcosa non funziona](#quando-qualcosa-non-funziona)

---

## Installazione

Ci sono due modi, e la differenza conta se vi interessa il primo avvio.

**L'installer per lingua** installa il programma in «Programmi» e mette accanto
un modello di riconoscimento per quella lingua. Ce ne sono sette, uno per
lingua dell'interfaccia: inglese, russo, tedesco, francese, spagnolo, italiano
e cinese. Poiché il modello è già presente, il primo avvio non richiede
internet.

**L'archivio portatile** è un unico `VoxSpica.exe` dentro uno zip. Non si
installa nulla, non si scrive nulla nel sistema e la cartella può stare su una
chiavetta. Il prezzo è il primo avvio: il programma chiede la lingua
dell'interfaccia e poi scarica un modello, quindi serve la rete una volta.

> **Windows ti avviserà.** Le build non sono firmate. SmartScreen segnala un
> editore sconosciuto, che ha esattamente l'aspetto di un software dannoso.
> Clicca *Ulteriori informazioni* → *Esegui comunque*.

## La finestra principale

Tutto sta in una finestra, con tre schermate di impostazioni dietro il menu
`Settings`.

| Controllo | Cosa fa |
| --- | --- |
| **Recognition language** | La lingua in cui stai per *parlare*. Vedi sotto. |
| **Model** | Quale dimensione di modello: piccolo o grande. |
| **Microphone** | Da quale dispositivo si registra. |
| ● / ❙❙ / ■ | Registra, pausa, ferma. |
| **Transcribe file** | Scegli un file audio e riconoscilo. |
| **Copy text** | Metti il testo riconosciuto negli appunti. |
| Riga di stato | Cosa sta facendo il programma e quanto ha impiegato l'ultimo caricamento. |

La riga di stato avvisa quando il modello è pronto. Se registri prima che
compaia `Model ready`, il programma aspetta.

## Scegliere la lingua di riconoscimento

**Lingua di riconoscimento e lingua dell'interfaccia sono due impostazioni
diverse.**

La lingua di *riconoscimento* è quella in cui parli; decide quale modello va
caricato. La lingua dell'*interfaccia* è quella in cui sono scritte le pulsanti.
Non c'è un legame: puoi dettare in ucraino con un'interfaccia inglese, e
l'installer fa altrettanto.

La lingua si sceglie tramite il suo codice VOSK, non tramite un Paese. `en-us` e
`en-in` sono inglese per accenti diversi, `el-gr` è il greco, `cn` è il
mandarino, `uk` è l'ucraino.

Tutti i 33 codici con i loro modelli sono in [LANGUAGES.md](LANGUAGES.md).

## Scaricare un modello

I modelli non fanno parte del programma. Vengono scaricati una volta, tenuti
accanto all'applicazione e possono essere rimossi in qualsiasi momento.

Apri `Settings` → **Models**. La colonna di sinistra elenca ogni lingua del
registro e le dimensioni disponibili. Selezionandone una, a destra si vede
quanto costa:

- una scheda per il modello **piccolo** con la sua dimensione su disco, e i
  pulsanti **Delete** e **Warm up in memory**;
- una scheda per il modello **grande**, con un pulsante **Download**.

Alcune lingue hanno una sola dimensione: nel registro non c'è `small` per
l'arabo, il portoghese brasiliano, il greco e il filippino, né `large` per il
catalano, il ceco, l'estone, il coreano, il polacco, lo svedese, il telugu, il
turco e l'uzbeco. La scheda lo dice invece di offrire un download che
fallirebbe.

I modelli vengono caricati in background all'avvio, quindi la registrazione
parte appena il modello è caldo.

![Gestione dei modelli di riconoscimento](../images/voxspica_models.png)

## Piccolo o grande?

| | piccolo | grande |
| --- | --- | --- |
| Dimensione su disco | circa 50 MB | circa 1,8 GB |
| Caricamento | pochi secondi | 60–90 s la prima volta |
| Memoria | qualche centinaio di MB | circa 8 GB |
| Accuratezza | basta per le bozze | nettamente migliore |

La finestra principale porta una nota sul tempo di caricamento, perché è la
parte che sorprende: il modello grande non impiega solo più tempo, legge un
minuto e mezzo dal disco al primo avvio della sessione.

**Cominciate dal piccolo.** Passate al grande quando vi serve una trascrizione
che verrà citata: un'intervista, una citazione, un nome che non si può indovinare.

## Scegliere il microfono

`Settings` → **Device** elenca tutti gli ingressi che il sistema dichiara, con
indice, nome e frequenza di campionamento. *Default* è l'ingresso predefinito
del sistema; un asterisco segna i dispositivi che il sistema considera
predefiniti.

Un microfono a 2 kHz non è una cattura reale: è un loop o un punto virtuale.
Scegliete quello la cui frequenza vi suona nota, di solito 16 kHz o
44,1/48 kHz.

![Scelta del microfono](../images/voxspica_device.png)

## Dettatura

1. Verificate che la riga di stato dica che il modello è pronto.
2. Scegliete il microfono.
3. Premete il pulsante di registrazione o l'icona del microfono nella barra.
4. Parlate. Il testo compare mentre parlate.
5. Premete ferma. Pausa quando dovete pensare.
6. **Copy text** mette il risultato negli appunti.

Le trascrizioni vengono scritte accanto al programma, e ogni riconoscimento
finisce nella cronologia.

## Trascrivere un file

**Transcribe file** apre una finestra di selezione. Il programma legge i WAV da
sé; per mp3, m4a, ogg e simili serve
[ffmpeg](https://ffmpeg.org/download.html) nel `PATH` — su Windows basta
`winget install Gyan.FFmpeg`.

Il file viene riconosciuto in una passata, e per la maggior parte delle
registrazioni è più veloce del tempo reale.

## Cronologia

Ogni riconoscimento viene salvato localmente in SQLite e compare nella finestra
della cronologia.

La tabella mostra l'identificativo, la data e l'ora, l'origine (microfono o
file), la lingua, la durata dell'audio e un'anteprima del testo. Il campo di
ricerca filtra sul testo; **Find** applica il filtro e **Show all** lo toglie.

Una riga selezionata mostra sotto il testo completo. Da lì si può premere
**Copy text**, **Delete entry** o **Clear history** per eliminare tutto in una
volta.

La cronologia è un normale file SQLite nel profilo dell'utente. Non viene
caricato nulla da nessuna parte, e cancellare il file cancella la cronologia.

![Cronologia dei riconoscimenti](../images/voxspica_history.png)

## Cambiare la lingua dell'interfaccia

`Settings` → **Interface**. Nove lingue, ognuna indicata nella propria:
Беларуская, Deutsch, English, Español, Français, Italiano, Русский, Українська,
简体中文.

La scelta ha effetto immediato. Al primo avvio di una build portatile la stessa
finestra compare prima di tutto il resto.

![Scegliere la lingua dell'interfaccia](../images/voxspica_interface_language.png)

## Riga di comando

L'eseguibile funziona anche da console, ed è la forma che serve in uno script o
in un lanciatore da scorciatoie:

```powershell
VoxSpica.exe mic --lang it --size small       # dettatura, testo su stdout
VoxSpica.exe file meeting.mp3 --lang en-us    # trascrive un file
VoxSpica.exe devices                          # elenca i microfoni
VoxSpica.exe list                             # lingue e i loro modelli
VoxSpica.exe download --lang it --size small  # scarica un modello
VoxSpica.exe history --search "riunione"      # cosa è stato riconosciuto
VoxSpica.exe history show 3                   # una voce per intero
VoxSpica.exe config lang=fr size=large        # ricorda una scelta
```

Interruttori utili nei comandi di registrazione:

| Interruttore | Effetto |
| --- | --- |
| `--no-punct` | Esattamente ciò che ha detto VOSK: né maiuscole né punto |
| `--no-history` | Non scrivere il risultato nella cronologia |
| `-o FILE` | Scrivere su file invece che su stdout |
| `--device N` | Usare un microfono preciso per indice |

Le impostazioni seguono una regola: valori integrati, poi quelli
dell'installer, poi il tuo file, poi la riga di comando. Quindi un
`--lang en-us` una tantum non cambia ciò che la finestra userà la prossima
volta.

## Quando qualcosa non funziona

**«Model required» all'avvio.** Il programma cerca un modello nella lingua
indicata dalle tue impostazioni e non lo trova. Due cause:

- le impostazioni nominano una lingua di un'installazione precedente, il cui
  modello se n'è andato via — scegli in `Settings` → **Models** la lingua che
  hai davvero;
- il modello c'è, ma è dell'altra dimensione — verifica che **Model** nella
  finestra principale corrisponda a quello installato.

**SmartScreen blocca l'installer.** Normale: le build non sono firmate.
*Ulteriori informazioni* → *Esegui comunque*.

**Niente virgole nel testo.** Normale, vedi il README. VOSK non produce punteggiatura
e ricostruirla senza un modello linguistico dà un risultato peggiore che non
far nulla.

**«Impossibile aprire in scrittura il file esistente».** I modelli e le
trascrizioni stanno accanto al programma. Sotto `C:\Program Files` un utente
normale non può scrivere, quindi il programma passa a `%LOCALAPPDATA%\VoxSpica`
e lo segnala.

**Non partono due copie.** La seconda vede la prima e si rifiuta. È voluto:
due copie si pesterebbero i piedi nel file delle impostazioni, nel database
della cronologia e nella cartella dei modelli. Chiudete la prima, o impostate
`VOXSPICA_NO_SINGLE_INSTANCE=1`.

**Un modello si scarica e sparisce.** Un download che non supera il controllo
d'integrità viene cancellato invece di restare a metà. Scaricatelo di nuovo; se
si ripete, la rete sta interrompendo il trasferimento.

---

## Vedi anche

- [LANGUAGES.md](LANGUAGES.md) — tutte le 33 lingue di riconoscimento e i loro modelli
- [Guida in spagnolo](USER-GUIDE.es.md) · [Русский README](../README.ru.md) · [English](../README.md)
- <https://voxspica.4crytobot.xyz> — il sito
