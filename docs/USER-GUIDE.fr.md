# Guide d'utilisation

<p align="center">
  <sub>[English](USER-GUIDE.md) · [Deutsch](USER-GUIDE.de.md) · [Español](USER-GUIDE.es.md) · [Italiano](USER-GUIDE.it.md) · [Русский](USER-GUIDE.ru.md)</sub>
</p>

VoxSpica reconnaît la parole sous Windows sans envoyer l'audio nulle part. Ce
guide parcourt les écrans dans l'ordre où vous les rencontrez.

- [Installation](#installation)
- [La fenêtre principale](#la-fenêtre-principale)
- [Choisir la langue de reconnaissance](#choisir-la-langue-de-reconnaissance)
- [Télécharger un modèle](#télécharger-un-modèle)
- [Petit ou grand ?](#petit-ou-grand-)
- [Choisir un micro](#choisir-un-micro)
- [Dicter](#dicter)
- [Transcrire un fichier](#transcrire-un-fichier)
- [Historique](#historique)
- [Changer la langue de l'interface](#changer-la-langue-de-linterface)
- [Ligne de commande](#ligne-de-commande)
- [Quand ça ne marche pas](#quand-ça-ne-marche-pas)

---

## Installation

Il y a deux façons, et la différence compte si le premier démarrage vous
intéresse.

**L'installateur par langue** installe le programme dans « Programmes » et pose
à côté un modèle de reconnaissance pour cette langue. Il y en a sept, un par
langue d'interface : anglais, russe, allemand, français, espagnol, italien et
chinois. Le modèle étant déjà là, le premier démarrage ne demande pas Internet.

**L'archive portable** est un unique `VoxSpica.exe` dans un zip. Rien ne
s'installe, rien ne s'écrit dans le système, et le dossier peut rester sur une
clé USB. Le prix à payer, c'est le premier démarrage : le programme demande la
langue de l'interface puis télécharge un modèle, il faut donc le réseau une
fois.

> **Windows vous préviendra.** Les builds ne sont pas signés. SmartScreen
> signale un éditeur inconnu, ce qui ressemble exactement à un logiciel
> malveillant. Cliquez *Informations détaillées* → *Exécuter quand même*.

## La fenêtre principale

Tout tient dans une fenêtre, avec trois écrans de réglages derrière le menu
`Settings`.

| Élément | Effet |
| --- | --- |
| **Recognition language** | La langue dans laquelle vous *parlez*. Voir plus bas. |
| **Model** | Quelle taille de modèle : petit ou grand. |
| **Microphone** | Le périphérique d'enregistrement. |
| ● / ❙❙ / ■ | Enregistrer, pause, arrêter. |
| **Transcribe file** | Choisir un fichier audio et le reconnaître. |
| **Copy text** | Mettre le texte reconnu dans le presse-papiers. |
| Barre d'état | Ce que fait le programme, et le temps du dernier chargement. |

La barre d'état indique quand le modèle est prêt. Enregistrer avant qu'elle
n'affiche `Model ready` vous fera attendre.

## Choisir la langue de reconnaissance

**Langue de reconnaissance et langue d'interface sont deux réglages
différents.**

La langue de *reconnaissance* est celle dans laquelle vous parlez. Elle décide
du modèle à charger. La langue d'*interface* est celle des boutons. Rien ne les
relie : on peut dicter en ukrainien dans une interface anglaise, et
l'installateur fait de même.

La langue se choisit par son code VOSK, pas par un pays. `en-us` et `en-in` sont
de l'anglais pour des accents différents, `el-gr` est le grec, `cn` le mandarin,
`uk` l'ukrainien.

Les 33 codes et leurs modèles sont dans [LANGUAGES.md](LANGUAGES.md).

## Télécharger un modèle

Les modèles ne font pas partie du programme. Ils sont téléchargés une fois,
gardés à côté de l'application, et peuvent être supprimés à tout moment.

Ouvrez `Settings` → **Models**. La colonne de gauche liste chaque langue du
registre et les tailles qui existent. Une sélection affiche à droite ce qu'elle
coûte :

- une carte pour le modèle **petit** avec sa taille sur le disque, et les
  boutons **Delete** et **Warm up in memory** ;
- une carte pour le modèle **grand**, avec un bouton **Download**.

Une langue n'a parfois qu'une seule taille : le registre n'a pas de `small` pour
l'arabe, le portugais brésilien, le grec et le tagalog, ni de `large` pour le
catalan, le tchèque, l'estonien, le coréen, le polonais, le suédois, le télougou,
le turc et l'ouzbek. L'onglet le dit au lieu de proposer un téléchargement qui
échouerait.

Les modèles se chargent en arrière-plan au démarrage, l'enregistrement commence
donc dès que le modèle est chaud.

![Gestion des modèles de reconnaissance](../images/voxspica_models.png)

## Petit ou grand ?

| | petit | grand |
| --- | --- | --- |
| Taille sur le disque | environ 50 Mo | environ 1,8 Go |
| Chargement | quelques secondes | 60 à 90 s la première fois |
| Mémoire | quelques centaines de Mo | environ 8 Go |
| Exactitude | assez pour des brouillons | nettement meilleure |

La fenêtre principale signale le temps de chargement, parce que c'est ce qui
surprend : le grand modèle ne met pas seulement plus de temps, il lit une
minute et demie depuis le disque au premier démarrage d'une session.

**Commencez par le petit.** Passez au grand quand vous avez besoin d'une
transcription qui sera citée : un entretien, une citation, un nom qu'on ne peut
pas deviner.

## Choisir un micro

`Settings` → **Device** liste toutes les entrées que le système déclare, avec
index, nom et fréquence d'échantillonnage. *Default* est l'entrée par défaut du
système ; un astérisque marque les périphériques que le système considère par
défaut.

Un micro annoncé à 2 kHz n'est pas une vraie entrée : c'est une boucle ou un
point virtuel. Choisissez celui dont la fréquence vous parle, généralement
16 kHz ou 44,1/48 kHz.

![Choix du micro](../images/voxspica_device.png)

## Dicter

1. Attendez que la barre d'état annonce le modèle prêt.
2. Choisissez le micro.
3. Appuyez sur le bouton d'enregistrement ou sur l'icône micro de la barre.
4. Parlez. Le texte apparaît au fur et à mesure.
5. Appuyez sur arrêter. Pause quand vous devez réfléchir.
6. **Copy text** met le résultat dans le presse-papiers.

Les transcriptions sont écrites à côté du programme, et chaque reconnaissance
arrive dans l'historique.

## Transcrire un fichier

**Transcribe file** ouvre un sélecteur. Le programme lit le WAV nativement ; pour
mp3, m4a, ogg et formats voisins, il faut
[ffmpeg](https://ffmpeg.org/download.html) dans le `PATH` — sous Windows,
`winget install Gyan.FFmpeg` suffit.

Le fichier est reconnu en une passe, ce qui est plus rapide que le temps réel
pour la plupart des enregistrements.

## Historique

Chaque reconnaissance est stockée localement dans SQLite et listée dans la
fenêtre d'historique.

Le tableau montre l'identifiant, la date et l'heure, la source (micro ou
fichier), la langue, la durée de l'audio et un aperçu du texte. Le champ de
recherche filtre sur le texte ; **Find** applique le filtre, **Show all** l'annule.

Une ligne sélectionnée affiche le texte entier en dessous. De là : **Copy text**,
**Delete entry** ou **Clear history** pour tout supprimer d'un coup.

L'historique est un simple fichier SQLite dans le profil utilisateur. Rien n'est
envoyé, et supprimer le fichier supprime l'historique.

![Historique des reconnaissances](../images/voxspica_history.png)

## Changer la langue de l'interface

`Settings` → **Interface**. Neuf langues, chacune listée dans la sienne :
Беларуская, Deutsch, English, Español, Français, Italiano, Русский, Українська,
简体中文.

Le choix s'applique immédiatement. Au premier démarrage d'une version portable,
la même boîte apparaît avant tout le reste.

![Choix de la langue de l'interface](../images/voxspica_interface_language.png)

## Ligne de commande

L'exécutable fonctionne aussi en console, et c'est la forme qu'il faut dans un
script ou un lanceur de raccourci :

```powershell
VoxSpica.exe mic --lang fr --size small       # dicter, texte sur stdout
VoxSpica.exe file meeting.mp3 --lang en-us    # transcrire un fichier
VoxSpica.exe devices                          # lister les périphériques d'entrée
VoxSpica.exe list                             # langues et leurs modèles
VoxSpica.exe download --lang fr --size small  # télécharger un modèle
VoxSpica.exe history --search "réunion"       # chercher dans le passé
VoxSpica.exe history show 3                   # une entrée en entier
VoxSpica.exe config lang=de size=large        # mémoriser un choix
```

Options utiles pour les commandes d'enregistrement :

| Option | Effet |
| --- | --- |
| `--no-punct` | Exactement ce que VOSK a dit : ni majuscules ni point |
| `--no-history` | Ne pas écrire le résultat dans l'historique |
| `-o FICHIER` | Écrire dans un fichier au lieu de stdout |
| `--device N` | Utiliser un micro précis par son index |

Les réglages suivent une règle : valeurs intégrées, puis ceux de l'installateur,
puis votre fichier, puis la ligne de commande. Un `--lang en-us` ponctuel ne
change donc pas ce qu'utilisera la fenêtre la fois suivante.

## Quand ça ne marche pas

**« Model required » au démarrage.** Le programme cherche un modèle dans la
langue que vos réglages nomment, et n'en trouve pas. Deux causes :

- les réglages nomment une langue d'une installation précédente, dont le modèle
  est parti avec elle — choisissez dans `Settings` → **Models** la langue que
  vous avez réellement ;
- le modèle est là, mais de l'autre taille — vérifiez que **Model** dans la
  fenêtre principale correspond à ce qui est installé.

**SmartScreen bloque l'installateur.** Normal : les builds ne sont pas signés.
*Informations détaillées* → *Exécuter quand même*.

**Pas de virgules dans le texte.** Normal, voir le README. VOSK ne produit pas
de ponctuation, et la reconstituer sans modèle de langue donne un résultat plus
mauvais que de ne rien faire.

**« Impossible d'ouvrir le fichier existant en écriture ».** Les modèles et les
transcriptions sont à côté du programme. Sous `C:\Program Files` un utilisateur
normal ne peut pas écrire, le programme bascule donc dans
`%LOCALAPPDATA%\VoxSpica` et le dit.

**Deux copies ne démarrent pas.** La seconde voit la première et refuse. C'est
voulut : deux copies se marcheraient dessus sur le fichier de réglages, la base
d'historique et le répertoire des modèles. Fermez la première, ou définissez
`VOXSPICA_NO_SINGLE_INSTANCE=1`.

**Un modèle se télécharge puis disparaît.** Un téléchargement qui échoue au
contrôle d'intégrité est supprimé plutôt que laissé à moitié écrit.
Retéléchargez-le ; si cela recommence, le réseau coupe le transfert.

---

## Voir aussi

- [LANGUAGES.md](LANGUAGES.md) — les 33 langues de reconnaissance et leurs modèles
- [Guide en allemand](USER-GUIDE.de.md) · [Русский README](../README.ru.md) · [English](../README.md)
- <https://voxspica.4crytobot.xyz> — le site
