<p align="center">
  <img alt="VoxSpica" src="images/voxspica_en.png" width="620">
</p>

<h1 align="center">VoxSpica</h1>

<p align="center">
  <b>Dictado y transcripción de voz para Windows que no envía tu voz a ninguna parte.</b><br>
  <sub>Tu voz se queda en tu ordenador. Sin cuenta, sin suscripción, sin nube.</sub>
</p>

<p align="center">
  <a href="https://github.com/alex37529/voxspica/releases"><img alt="Descargar" src="https://img.shields.io/badge/descargar-releases-2C7BE0?style=for-the-badge"></a>
  <a href="docs/USER-GUIDE.md"><img alt="Guía" src="https://img.shields.io/badge/guía-0B1620?style=for-the-badge"></a>
  <a href="https://voxspica.4crytobot.xyz"><img alt="Sitio web" src="https://img.shields.io/badge/sitio-voxspica.4crytobot.xyz-0B1620?style=for-the-badge"></a>
</p>

<p align="center">
  <img alt="Windows" src="https://img.shields.io/badge/Windows-10%20%2F%2011%20x64-0B1620?style=flat-square">
  <img alt="Licencia" src="https://img.shields.io/badge/licencia-Apache--2.0-2C7BE0?style=flat-square">
  <img alt="Idiomas de la interfaz" src="https://img.shields.io/badge/interfaz-9%20idiomas-0B1620?style=flat-square">
  <img alt="Idiomas de reconocimiento" src="https://img.shields.io/badge/reconocimiento-33%20idiomas-0B1620?style=flat-square">
  <img alt="Motor" src="https://img.shields.io/badge/ASR-VOSK%20(Kaldi)-0B1620?style=flat-square">
</p>

<p align="center">
  <sub><a href="README.md">English</a> · <a href="README.de.md">Deutsch</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a> · <a href="README.it.md">Italiano</a> · <a href="README.ru.md">Русский</a> · <a href="README.zh.md">简体中文</a></sub>
</p>

---

## Qué es

VoxSpica convierte la voz en texto en Windows y nada sale del ordenador. El
motor de reconocimiento es [VOSK](https://alphacephei.com/vosk/), una versión de
escritorio de Kaldi, de código abierto, que se ejecuta en tu CPU. Sin GPU, sin
red, sin telemetría.

Funciona de dos maneras:

- **Dictado en vivo** desde el micrófono, con el texto apareciendo mientras hablas.
- **Transcripción de archivos** para todo lo que el sistema sepa reproducir:
  mp3, m4a, wav y otros si tienes [ffmpeg](https://ffmpeg.org/) en la ruta.

Cada reconocimiento se guarda en una base de datos local en la que puedes buscar.

## Por qué sin conexión

Los servicios de dictado que hayas usado envían tu audio al servidor de alguien
más. Para ellos es un diseño razonable y es una mala decisión para una
herramienta cuyo trabajo es anotar lo que acabas de decir en voz alta, que a
menudo es un documento privado, el nombre de un cliente o una idea que todavía
no has decidido publicar.

Aquí la respuesta es estructural, no una promesa: el modelo está en tu disco, la
base de datos está en tu disco y en el programa no hay ni un solo punto que abra
un socket.

<p align="center">
  <img alt="Selección del idioma de la interfaz" src="images/voxspica_interface_language.png" width="820">
  <br>
  <sub>La interfaz habla nueve idiomas, cada uno nombrado en su propia lengua.</sub>
</p>

## Las pantallas

<table>
<tr>
<td width="50%" align="center" valign="top">
  <img alt="Gestión de los modelos de reconocimiento" src="images/voxspica_models.png"><br>
  <sub><b>Modelos</b> — todos los idiomas, sus tamaños y lo que cuesta cada descarga.</sub>
</td>
<td width="50%" align="center" valign="top">
  <img alt="Elección del micrófono" src="images/voxspica_device.png"><br>
  <sub><b>Dispositivo</b> — elige el micrófono, con su frecuencia de muestreo real.</sub>
</td>
</tr>
<tr>
<td width="50%" align="center" valign="top">
  <img alt="Historial de reconocimientos" src="images/voxspica_history.png"><br>
  <sub><b>Historial</b> — cada reconocimiento, buscable, borrable y copiable.</sub>
</td>
<td width="50%" align="center" valign="top">
  <img alt="Selección del idioma de la interfaz" src="images/voxspica_interface_language.png"><br>
  <sub><b>Interfaz</b> — cambia de idioma cuando quieras.</sub>
</td>
</tr>
</table>

## Cómo obtenerlo

<table>
<tr>
<th align="left" width="50%">Instalador por idioma</th>
<th align="left" width="50%">Archivo portátil</th>
</tr>
<tr>
<td valign="top">

Siete instaladores, uno por idioma de interfaz. Cada uno trae consigo un modelo
de reconocimiento listo para ese idioma, así que el primer arranque funciona sin
internet. Elige el tuyo: los enlaces están justo debajo.

</td>
<td valign="top">

Un único <code>VoxSpica.exe</code> dentro de un zip. No se instala nada, no se
escribe nada en el sistema y la carpeta puede vivir en un pendrive. Eliges el
idioma de la interfaz y descargas un modelo en el primer arranque.

Las versiones portátiles están en [Releases](https://github.com/alex37529/voxspica/releases).

</td>
</tr>
</table>

### Los siete instaladores

Dirección base: <https://voxspica.4crytobot.xyz/downloads>

- <img src="https://flagcdn.com/16x12/gb.png" width="16" alt="GB"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-en-setup.exe"><code>VoxSpica-0.1.4-en-setup.exe</code></a> — English, 101.1 MB
- <img src="https://flagcdn.com/16x12/ru.png" width="16" alt="RU"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-ru-setup.exe"><code>VoxSpica-0.1.4-ru-setup.exe</code></a> — Русский, 106.1 MB
- <img src="https://flagcdn.com/16x12/de.png" width="16" alt="DE"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-de-setup.exe"><code>VoxSpica-0.1.4-de-setup.exe</code></a> — Deutsch, 106.1 MB
- <img src="https://flagcdn.com/16x12/fr.png" width="16" alt="FR"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-fr-setup.exe"><code>VoxSpica-0.1.4-fr-setup.exe</code></a> — Français, 102.4 MB
- <img src="https://flagcdn.com/16x12/es.png" width="16" alt="ES"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-es-setup.exe"><code>VoxSpica-0.1.4-es-setup.exe</code></a> — Español, 99.6 MB
- <img src="https://flagcdn.com/16x12/it.png" width="16" alt="IT"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-it-setup.exe"><code>VoxSpica-0.1.4-it-setup.exe</code></a> — Italiano, 109.5 MB
- <img src="https://flagcdn.com/16x12/cn.png" width="16" alt="CN"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.4-zh-setup.exe"><code>VoxSpica-0.1.4-zh-setup.exe</code></a> — 简体中文, 103.8 MB

La lista nombra una versión y se sustituye con cada publicación nueva. El
archivo portátil no está aquí a propósito: está en la release, y es el que
conviene si quieres un idioma de interfaz que no figure en la lista. Las
banderas vienen de [flagcdn.com](https://flagcdn.com) y marcan el idioma, no el
país: el inglés es 🇬🇧 y no 🇺🇸 porque la interfaz se llama `en` y no `en-US`, y
ningún instalador incluye una interfaz estadounidense. Si flagcdn no está
accesible, los enlaces siguen funcionando; solo desaparecen las imágenes.

> **Windows te avisará.** Las compilaciones no están firmadas, así que
> SmartScreen mostrará un editor desconocido. Pulsa *Más información* → *Ejecutar
> de todas formas*. Véase [qué no hace](#qué-no-hace): la firma está en la
> lista.

## Primera ejecución

1. Inicia el programa. En el primer arranque pregunta el idioma de la interfaz.
2. Elige el **idioma de reconocimiento**, es decir, aquel en el que vas a
   *hablar*. Es distinto del idioma de la interfaz e independiente de él.
3. Descarga un modelo para él. El **pequeño** ocupa unos 50 MB y basta para
   borradores; el **grande** es más exacto, necesita unos 8 GB de RAM y tarda
   entre 60 y 90 segundos en cargarse la primera vez de la sesión.
4. Elige un micrófono, pulsa grabar y habla.

La [guía](docs/USER-GUIDE.md) recorre cada pantalla, incluido qué hacer cuando
falta un modelo y en qué se diferencian los modelos pequeños de los grandes.

## Idiomas

La **interfaz** está disponible en nueve idiomas: bielorruso, alemán, inglés,
español, francés, italiano, ruso, ucraniano y chino simplificado.

El **reconocimiento** funciona en 33 idiomas. Están listados con el nombre de
sus modelos en [docs/LANGUAGES.md](docs/LANGUAGES.md). Reconocimiento e interfaz
son independientes: puedes dictar en ucraniano con una interfaz en inglés.

## Línea de órdenes

El programa no es solo una ventana. Todo lo que hace está disponible desde la
consola, que es lo que necesitas en un script o en un lanzador de teclas
rápidas:

```powershell
VoxSpica.exe mic --lang es --size small      # dictado, texto a stdout
VoxSpica.exe file meeting.mp3 --lang en-us   # transcribe un archivo
VoxSpica.exe devices                         # lista los micrófonos
VoxSpica.exe download --lang es --size small
VoxSpica.exe list                            # idiomas y sus modelos
VoxSpica.exe history --search "reunión"      # qué se reconoció antes
```

## Qué no hace

Escrito sin rodeos, porque es la parte que suele descubrirse después.

- **No está firmado.** Windows muestra un aviso de SmartScreen en cada
  instalación.
- **No hay comas.** VOSK devuelve palabras sin puntuación. VoxSpica restituye
  las mayúsculas y pone un punto al final de la frase, pero no puede colocar
  comas sin analizar la sintaxis: cualquier regla sencilla produce «Cómo, estás?»
  en lugar de «Cómo estás?».
- **Solo Windows x64.** No hay compilaciones para macOS ni para Linux.
- **Los modelos van aparte.** Salvo los instaladores por idioma, ningún archivo
  incluye un modelo, y van de 50 MB a 1,8 GB. Los instaladores por idioma son la
  excepción: cada uno lleva el suyo.

## Acerca de este repositorio

Aquí hay **solo las versiones publicadas**. El código fuente no es público y no
se refleja aquí: en este repositorio no hay ni una línea. Las etiquetas `vX.Y.Z`
apuntan al pequeño commit público que introduce este archivo, no al código de la
aplicación. Los archivos adjuntos a cada versión son binarios compilados.

Sitio web: <https://voxspica.4crytobot.xyz>

## Licencia

Apache-2.0, consulta [LICENSE](LICENSE). El reconocimiento lo hace
[VOSK](https://alphacephei.com/vosk/) (Apache-2.0); los modelos de
reconocimiento los distribuye Alpha Cephei también bajo Apache-2.0.
