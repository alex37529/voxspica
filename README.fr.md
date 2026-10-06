<p align="center">
  <img alt="VoxSpica" src="images/voxspica_en.png" width="620">
</p>

<h1 align="center">VoxSpica</h1>

<p align="center">
  <b>Dictée et transcription vocale pour Windows, qui n'envoie votre voix nulle part.</b><br>
  <sub>Votre voix reste sur votre ordinateur. Aucun compte, aucun abonnement, aucun cloud.</sub>
</p>

<p align="center">
  <a href="https://github.com/alex37529/voxspica/releases"><img alt="Télécharger" src="https://img.shields.io/badge/télécharger-releases-2C7BE0?style=for-the-badge"></a>
  <a href="docs/USER-GUIDE.md"><img alt="Guide" src="https://img.shields.io/badge/guide-0B1620?style=for-the-badge"></a>
  <a href="https://voxspica.4crytobot.xyz"><img alt="Site web" src="https://img.shields.io/badge/site-voxspica.4crytobot.xyz-0B1620?style=for-the-badge"></a>
</p>

<p align="center">
  <img alt="Windows" src="https://img.shields.io/badge/Windows-10%20%2F%2011%20x64-0B1620?style=flat-square">
  <img alt="Ubuntu 22.04" src="https://img.shields.io/badge/platform-Ubuntu%2022.04-E95420?logo=ubuntu&logoColor=white">
  <img alt="Ubuntu 24.04" src="https://img.shields.io/badge/platform-Ubuntu%2024.04-E95420?logo=ubuntu&logoColor=white">
  <img alt="Licence" src="https://img.shields.io/badge/licence-proprietary-2C7BE0?style=flat-square">
  <img alt="Langues de l'interface" src="https://img.shields.io/badge/interface-9%20langues-0B1620?style=flat-square">
  <img alt="Langues de reconnaissance" src="https://img.shields.io/badge/reconnaissance-33%20langues-0B1620?style=flat-square">
  <img alt="Moteur" src="https://img.shields.io/badge/ASR-VOSK%20(Kaldi)-0B1620?style=flat-square">
</p>

<p align="center">
  <sub><a href="README.md">English</a> · <a href="README.de.md">Deutsch</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a> · <a href="README.it.md">Italiano</a> · <a href="README.ru.md">Русский</a> · <a href="README.zh.md">简体中文</a></sub>
</p>

---

## Ce que c'est

VoxSpica transforme la parole en texte sous Windows et Ubuntu, et rien ne
quitte la machine. Le moteur de reconnaissance est [VOSK](https://alphacephei.com/vosk/),
une version pour ordinateur de Kaldi, open source, qui tourne sur votre
processeur. Pas de GPU, pas de réseau, pas de télémétrie.

Il fonctionne de deux façons :

- **Dictée en direct** depuis le micro, le texte apparaissant au fil de la parole.
- **Transcription de fichiers** pour tout ce que la sait lire le système :
  mp3, m4a, wav et autres si [ffmpeg](https://ffmpeg.org/) est dans le chemin.

Chaque reconnaissance est conservée dans une base locale que vous pouvez
interroger.

## Pourquoi hors ligne

Les services de dictée que vous avez peut-être utilisés envoient votre audio sur
le serveur de quelqu'un d'autre. C'est un choix raisonnable pour eux, et un
mauvais choix pour un outil dont le métier est de noter ce que vous venez de
dire à voix haute : le plus souvent un document privé, le nom d'un client, ou
une idée que vous n'avez pas encore décidé de publier.

Ici la réponse est structurelle et non promissoire : le modèle est sur votre
disque, la base est sur votre disque, et le programme ne contient aucun point
qui ouvre une connexion.

<p align="center">
  <img alt="Choix de la langue de l'interface" src="images/voxspica_interface_language.png" width="820">
  <br>
  <sub>L'interface parle neuf langues, chacune nommée dans la sienne.</sub>
</p>

## Les écrans

<table>
<tr>
<td width="50%" align="center" valign="top">
  <img alt="Gestion des modèles de reconnaissance" src="images/voxspica_models.png"><br>
  <sub><b>Modèles</b> — chaque langue, ses tailles et ce que coûte le téléchargement.</sub>
</td>
<td width="50%" align="center" valign="top">
  <img alt="Choix du micro" src="images/voxspica_device.png"><br>
  <sub><b>Périphérique</b> — choisissez le micro, avec sa vraie fréquence d'échantillonnage.</sub>
</td>
</tr>
<tr>
<td width="50%" align="center" valign="top">
  <img alt="Historique des reconnaissances" src="images/voxspica_history.png"><br>
  <sub><b>Historique</b> — chaque reconnaissance, cherchable, supprimable, copiable.</sub>
</td>
<td width="50%" align="center" valign="top">
  <img alt="Choix de la langue de l'interface" src="images/voxspica_interface_language.png"><br>
  <sub><b>Interface</b> — changez de langue quand vous voulez.</sub>
</td>
</tr>
</table>

## Où le obtenir

<table>
<tr>
<th align="left" width="50%">Installateur par langue</th>
<th align="left" width="50%">Archive portable</th>
</tr>
<tr>
<td valign="top">

Sept installateurs, un par langue d'interface. Chacun embarque un modèle de
reconnaissance déjà prêt pour sa langue : le premier lancement fonctionne donc
sans internet. Choisissez le vôtre, les liens sont juste en dessous.

</td>
<td valign="top">

Un seul <code>VoxSpica.exe</code> dans un zip. Rien ne s'installe, rien ne
s'écrit dans le système, et le dossier peut vivre sur une clé USB. Vous
choisissez la langue de l'interface et téléchargez un modèle au premier lancement.

Les versions portables sont dans [Releases](https://github.com/alex37529/voxspica/releases).

</td>
</tr>
</table>

### Scoop

Si vous utilisez déjà [Scoop](https://scoop.sh) :

```powershell
scoop bucket add voxspica https://github.com/alex37529/voxspica-scoop
scoop install voxspica
```

Cela installe l'archive portable et met `voxspica` dans le PATH. Le manifeste
lit la somme de contrôle dans le `SHA256SUMS.txt` de la version, si bien que
`scoop update` prend les nouvelles versions tout seul.

### Les sept installateurs

Adresse de base : <https://voxspica.4crytobot.xyz/downloads>

- <img src="https://flagcdn.com/16x12/gb.png" width="16" alt="GB"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.7-en-setup.exe"><code>VoxSpica-0.1.7-en-setup.exe</code></a> — English, 113.8 MB
- <img src="https://flagcdn.com/16x12/ru.png" width="16" alt="RU"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.7-ru-setup.exe"><code>VoxSpica-0.1.7-ru-setup.exe</code></a> — Русский, 118.6 MB
- <img src="https://flagcdn.com/16x12/de.png" width="16" alt="DE"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.7-de-setup.exe"><code>VoxSpica-0.1.7-de-setup.exe</code></a> — Deutsch, 118.5 MB
- <img src="https://flagcdn.com/16x12/fr.png" width="16" alt="FR"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.7-fr-setup.exe"><code>VoxSpica-0.1.7-fr-setup.exe</code></a> — Français, 115.0 MB
- <img src="https://flagcdn.com/16x12/es.png" width="16" alt="ES"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.7-es-setup.exe"><code>VoxSpica-0.1.7-es-setup.exe</code></a> — Español, 112.4 MB
- <img src="https://flagcdn.com/16x12/it.png" width="16" alt="IT"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.7-it-setup.exe"><code>VoxSpica-0.1.7-it-setup.exe</code></a> — Italiano, 121.8 MB
- <img src="https://flagcdn.com/16x12/cn.png" width="16" alt="CN"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.7-zh-setup.exe"><code>VoxSpica-0.1.7-zh-setup.exe</code></a> — 简体中文, 116.4 MB

La liste nomme une version et est remplacée à chaque nouvelle publication.
L'archive portable n'y figure pas volontairement : elle est dans la release, et
c'est celle qu'il faut si vous voulez une langue d'interface qui n'y est pas.
Les drapeaux viennent de [flagcdn.com](https://flagcdn.com) et désignent la
langue, pas le pays : l'anglais est 🇬🇧 et non 🇺🇸 parce que l'interface
s'appelle `en` et non `en-US`, et aucun installateur ne fournit d'interface
américaine. Si flagcdn est injoignable, les liens fonctionnent quand même, seules
les images disparaissent.

> **Windows vous préviendra.** Les builds ne sont pas signés, SmartScreen
> signale donc un éditeur inconnu. Cliquez *Informations détaillées* →
> *Exécuter quand même*. Voir [ce que le programme ne fait pas](#ce-que-le-programme-ne-fait-pas) :
> la signature est sur la liste.

### Ubuntu / Debian

Pour **Ubuntu 22.04** et **24.04** (et Debian 12 et les versions suivantes),
il y a un paquet natif `voxspica_0.1.7_amd64.deb`. C'est un actif de la release,
pas dans la liste ci-dessus. Téléchargez-le, puis :

```bash
sudo dpkg -i voxspica_0.1.7_amd64.deb
```

ou avec un gestionnaire de paquets : `sudo apt install ./voxspica_0.1.7_amd64.deb`.
Le modèle de reconnaissance n'est pas dans le `.deb` ; au premier lancement,
choisissez une langue et téléchargez un modèle, comme sous Windows.

## Premier lancement

1. Lancez le programme. Au premier démarrage il demande la langue de
   l'interface.
2. Choisissez la **langue de reconnaissance**, c'est-à-dire celle dans laquelle
   vous allez *parler*. Elle est distincte de la langue de l'interface et en est
   indépendante.
3. Téléchargez un modèle. Le **petit** fait autour de 50 Mo et suffit pour des
   brouillons ; le **grand** est plus juste, demande environ 8 Go de RAM et met
   60 à 90 secondes à se charger au premier lancement de la session.
4. Choisissez un micro, appuyez sur enregistrer, parlez.

Le [guide](docs/USER-GUIDE.md) parcourt chaque écran, y compris ce qu'il faut
faire quand un modèle manque et en quoi les petits modèles diffèrent des
grands.

## Langues

L'**interface** existe en neuf langues : biélorusse, allemand, anglais, espagnol,
français, italien, russe, ukrainien, chinois simplifié.

La **reconnaissance** fonctionne en 33 langues, listées avec le nom de leurs
modèles dans [docs/LANGUAGES.md](docs/LANGUAGES.md). Reconnaissance et
interface sont indépendantes : vous pouvez dicter en ukrainien dans une
interface anglaise.

## Ligne de commande

Le programme n'est pas qu'une fenêtre. Tout ce qu'il fait est disponible depuis
une console, ce qui est utile dans un script ou un lanceur de raccourci :

```powershell
VoxSpica.exe mic --lang fr --size small      # dictée, texte sur stdout
VoxSpica.exe file meeting.mp3 --lang en-us   # transcribe un fichier
VoxSpica.exe devices                         # liste les micros
VoxSpica.exe download --lang fr --size small
VoxSpica.exe list                            # langues et leurs modèles
VoxSpica.exe history --search "réunion"      # ce qui a été reconnu auparavant
```

## Ce que le programme ne fait pas

Écrit sans détour, parce que c'est la partie qu'on découvre d'ordinaire après
coup.

- **Non signé.** Windows affiche un avertissement SmartScreen à chaque
  installation.
- **Pas de virgules.** VOSK renvoie des mots sans ponctuation. VoxSpica rétablit
  les majuscules et met un point en fin de phrase, mais ne peut pas placer les
  virgules sans analyser la syntaxe : toute règle simple produit « Comment, ça va ? »
  au lieu de « Comment ça va ? ».
- **Windows x64, et maintenant Ubuntu (22.04+).** Pas de build macOS.
- **Les modèles sont séparés.** Hormis les installateurs par langue, aucun
  fichier n'embarque un modèle, et ils vont de 50 Mo à 1,8 Go. Les installateurs
  par langue sont l'exception : chacun apporte le sien.

## À propos de ce dépôt

Il ne contient **que les versions publiées**. Le code source n'est pas public et
n'est pas mis en miroir ici : ce dépôt n'en contient pas la moindre trace. Les
étiquettes `vX.Y.Z` pointent sur le petit commit public qui introduit ce
fichier, pas sur le code de l'application. Les fichiers joints à chaque version
sont des binaires compilés.

Site web : <https://voxspica.4crytobot.xyz>

## Licence

Propriétaire, usage gratuit, voir [LICENSE](LICENSE). La reconnaissance est faite par
[VOSK](https://alphacephei.com/vosk/) (Apache-2.0) ; les modèles de
reconnaissance sont distribués par Alpha Cephei sous la même licence Apache-2.0.
