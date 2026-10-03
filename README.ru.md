<p align="center">
  <img alt="VoxSpica" src="images/voxspica_en.png" width="620">
</p>

<h1 align="center">VoxSpica</h1>

<p align="center">
  <b>Распознавание речи для Windows, которое никуда не отправляет ваш голос.</b><br>
  <sub>Голос остаётся на вашем компьютере. Без аккаунта, без подписки, без облака.</sub>
</p>

<p align="center">
  <a href="https://github.com/alex37529/voxspica/releases"><img alt="Скачать" src="https://img.shields.io/badge/скачать-releases-2C7BE0?style=for-the-badge"></a>
  <a href="docs/USER-GUIDE.ru.md"><img alt="Руководство" src="https://img.shields.io/badge/руководство-0B1620?style=for-the-badge"></a>
  <a href="https://voxspica.4crytobot.xyz"><img alt="Сайт" src="https://img.shields.io/badge/сайт-voxspica.4crytobot.xyz-0B1620?style=for-the-badge"></a>
</p>

<p align="center">
  <img alt="Windows" src="https://img.shields.io/badge/Windows-10%20%2F%2011%20x64-0B1620?style=flat-square">
  <img alt="Лицензия" src="https://img.shields.io/badge/лицензия-proprietary-2C7BE0?style=flat-square">
  <img alt="Языки интерфейса" src="https://img.shields.io/badge/интерфейс-9%20языков-0B1620?style=flat-square">
  <img alt="Языки распознавания" src="https://img.shields.io/badge/распознавание-33%20языка-0B1620?style=flat-square">
  <img alt="Движок" src="https://img.shields.io/badge/ASR-VOSK%20(Kaldi)-0B1620?style=flat-square">
</p>

<p align="center">
  <sub><a href="README.md">English</a> · <a href="README.de.md">Deutsch</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a> · <a href="README.it.md">Italiano</a> · <a href="README.ru.md">Русский</a> · <a href="README.zh.md">简体中文</a></sub>
</p>

---

## Что это

VoxSpica превращает речь в текст на Windows, и ничего не покидает компьютер.
Движок распознавания — [VOSK](https://alphacephei.com/vosk/), настольная сборка
Kaldi с открытым исходным кодом, работающая на вашем процессоре. Без
видеокарты, без сети, без телеметрии.

Работает двумя способами:

- **Диктовка** с микрофона в реальном времени, текст появляется по мере речи.
- **Расшифровка файлов** — всё, что система умеет воспроизводить: mp3, m4a,
  wav и прочее, если в системе есть [ffmpeg](https://ffmpeg.org/).

Каждое распознавание сохраняется в локальную базу, по которой потом можно
искать.

## Почему офлайн

Сервисы диктовки, которыми вы, возможно, пользовались, отправляют ваше аудио
на чужой сервер. Для них это разумное решение и плохое для инструмента, чья
работа — записывать то, что вы только что произнесли вслух. А это часто
закрытый документ, имя клиента или мысль, которую вы ещё не решили
публиковать.

Здесь ответ заложен конструкцией, а не обещанием: модель лежит на вашем
диске, база лежит на вашем диске, и в программе нет ни одного места, которое
открывает сокет.

<p align="center">
  <img alt="Выбор языка интерфейса" src="images/voxspica_interface_language.png" width="820">
  <br>
  <sub>Интерфейс говорит на девяти языках, каждый назван по-русски на своём.</sub>
</p>

## Экраны

<table>
<tr>
<td width="50%" align="center" valign="top">
  <img alt="Управление моделями распознавания" src="images/voxspica_models.png"><br>
  <sub><b>Модели</b> — все языки, их размеры и сколько стоит каждая загрузка.</sub>
</td>
<td width="50%" align="center" valign="top">
  <img alt="Выбор микрофона" src="images/voxspica_device.png"><br>
  <sub><b>Устройство</b> — выбор микрофона с настоящей частотой дискретизации.</sub>
</td>
</tr>
<tr>
<td width="50%" align="center" valign="top">
  <img alt="История распознаваний" src="images/voxspica_history.png"><br>
  <sub><b>История</b> — каждое распознавание можно найти, удалить и скопировать.</sub>
</td>
<td width="50%" align="center" valign="top">
  <img alt="Выбор языка интерфейса" src="images/voxspica_interface_language.png"><br>
  <sub><b>Интерфейс</b> — язык переключается в любой момент.</sub>
</td>
</tr>
</table>

## Как скачать

<table>
<tr>
<th align="left" width="50%">Установщик под язык</th>
<th align="left" width="50%">Портативный архив</th>
</tr>
<tr>
<td valign="top">

Семь установщиков, по одному на язык интерфейса. Каждый приносит готовую
модель распознавания для своего языка, поэтому первый запуск работает вообще
без интернета. Выберите свой язык — ссылки ниже.

</td>
<td valign="top">

Один <code>VoxSpica.exe</code> в zip-архиве. Ничего не устанавливается,
ничего не пишется в систему, папку можно носить на флешке. Язык интерфейса
вы выбираете при первом запуске, модель скачивается тогда же.

Портативные сборки — в [Releases](https://github.com/alex37529/voxspica/releases).

</td>
</tr>
</table>

### Scoop

Если у вас уже стоит [Scoop](https://scoop.sh):

```powershell
scoop bucket add voxspica https://github.com/alex37529/voxspica-scoop
scoop install voxspica
```

Ставится портативная сборка, команда `voxspica` появляется в PATH. Манифест
берёт контрольную сумму из `SHA256SUMS.txt` самого релиза, поэтому
`scoop update` подхватывает новую версию сам.

### Семь установщиков

Базовый адрес: <https://voxspica.4crytobot.xyz/downloads>

- <img src="https://flagcdn.com/16x12/gb.png" width="16" alt="GB"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.6-en-setup.exe"><code>VoxSpica-0.1.6-en-setup.exe</code></a> — English, 119.3 MB
- <img src="https://flagcdn.com/16x12/ru.png" width="16" alt="RU"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.6-ru-setup.exe"><code>VoxSpica-0.1.6-ru-setup.exe</code></a> — Русский, 124.3 MB
- <img src="https://flagcdn.com/16x12/de.png" width="16" alt="DE"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.6-de-setup.exe"><code>VoxSpica-0.1.6-de-setup.exe</code></a> — Deutsch, 124.3 MB
- <img src="https://flagcdn.com/16x12/fr.png" width="16" alt="FR"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.6-fr-setup.exe"><code>VoxSpica-0.1.6-fr-setup.exe</code></a> — Français, 120.6 MB
- <img src="https://flagcdn.com/16x12/es.png" width="16" alt="ES"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.6-es-setup.exe"><code>VoxSpica-0.1.6-es-setup.exe</code></a> — Español, 117.8 MB
- <img src="https://flagcdn.com/16x12/it.png" width="16" alt="IT"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.6-it-setup.exe"><code>VoxSpica-0.1.6-it-setup.exe</code></a> — Italiano, 127.7 MB
- <img src="https://flagcdn.com/16x12/cn.png" width="16" alt="CN"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.6-zh-setup.exe"><code>VoxSpica-0.1.6-zh-setup.exe</code></a> — 简体中文, 122.0 MB

Список называет одну версию и заменяется при выходе следующей. Портативный
архив здесь намеренно отсутствует: он лежит в релизе, и он же подходит, если
нужен язык интерфейса, которого в списке нет. Флаги отдаёт
[flagcdn.com](https://flagcdn.com) и обозначают язык, а не страну: у
английского 🇬🇧, а не 🇺🇸, потому что интерфейс называется `en`, а не `en-US`,
и ни один установщик не везёт американский интерфейс. Если flagcdn
недоступен, ссылки продолжат работать — пропадут только картинки.

> **Windows покажет предупреждение.** Сборки не подписаны, поэтому SmartScreen
> сообщит о неизвестном издателе. Нажмите *Подробнее* → *Выполнить в любом
> случае*. Подробности — в разделе
> [о чём это не умеет](#о-чём-это-не-умеет).

## Первый запуск

1. Запустите программу. При первом запуске она спросит язык интерфейса.
2. Выберите **язык распознавания** — тот, на котором вы будете *говорить*.
   Это не то же самое, что язык интерфейса, и он от него не зависит.
3. Скачайте для него модель. **Малая** — около 50 МБ, её хватает для
   черновиков. **Большая** — точнее, требует около 8 ГБ оперативной памяти и
   при первом запуске сессии читается с диска 60–90 секунд.
4. Выберите микрофон, нажмите запись и говорите.

[Руководство](docs/USER-GUIDE.ru.md) разбирает каждый экран по шагам, включая
что делать, если модель не найдена и чем малые модели отличаются от больших.

## Языки

**Интерфейс** доступен на девяти языках: белорусский, немецкий, английский,
испанский, французский, итальянский, русский, украинский, китайский.

**Распознавание** работает на 33 языках. Полный список с моделями —
в [docs/LANGUAGES.md](docs/LANGUAGES.md). Язык распознавания и язык интерфейса
независимы: можно диктовать по-украински в английском интерфейсе.

## Консоль

Программа не только окно. Всё, что она делает, доступно из консоли — это то,
что нужно в скрипте или в программе на горячих клавишах:

```powershell
VoxSpica.exe mic --lang ru --size small     # диктовка, текст в stdout
VoxSpica.exe file meeting.mp3 --lang en-us  # расшифровка файла
VoxSpica.exe devices                        # список микрофонов
VoxSpica.exe download --lang ru --size small
VoxSpica.exe list                           # языки и их модели
VoxSpica.exe history --search "meeting"     # что распознавалось раньше
```

## О чём это не умеет

Пишу прямо, потому что обычно об этом узнают позже.

- **Не подписано.** Windows показывает предупреждение SmartScreen при каждой
  установке.
- **Запятых не будет.** VOSK выдаёт слова без знаков препинания. VoxSpica
  восстанавливает регистр и ставит точку в конце фразы, но расставить запятые
  без разбора синтаксиса нельзя: любое простое правило даёт «Как, дела» вместо
  «Как дела».
- **Только Windows x64.** Сборок под macOS и Linux нет.
- **Модели отдельные.** Кроме установщиков под язык, модель не поставляется
  ни с чем, а весит от 50 МБ до 1,8 ГБ. Установщики — исключение: каждый
  несёт свою.

## Об этом репозитории

Здесь лежат **только релизы**. Исходный код не публичен и сюда не зеркалится —
в этом репозитории его нет целиком. Теги `vX.Y.Z` указывают на небольшой
публичный коммит, который добавляет этот файл, а не на код приложения. Файлы
прикреплённые к релизам — собранные бинарники.

Сайт: <https://voxspica.4crytobot.xyz>

## Лицензия

Проприетарная, бесплатное использование, см. [LICENSE](LICENSE). Распознавание выполняет
[VOSK](https://alphacephei.com/vosk/) (Apache-2.0); модели распознавания
распространяет Alpha Cephei тоже под Apache-2.0.
