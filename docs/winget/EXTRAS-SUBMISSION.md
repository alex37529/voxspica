# Extras: черновик issue и PR

Опубликуй от своего аккаунта: https://github.com/ScoopInstaller/Extras/issues/new
и https://github.com/ScoopInstaller/Extras/pulls

Scoop требует именно такого порядка: сначала **issue** с мейнтейнерами, и только
после их ответа — PR. Проверку из шаблона PR нужно отметить, иначе бот напомнит.

---

## Черновик issue (английский, для Package Request)

**Title**

```
Package Request: VoxSpica — offline speech-to-text for Windows
```

**Body**

```markdown
I'd like to add VoxSpica, a free offline speech-to-text application for Windows.

### What it is

Records speech or transcribes an audio file into text, entirely on the local
machine. No account, no subscription, no telemetry: the audio is never uploaded
anywhere. 33 recognition languages, 9 interface languages, live transcription
while you speak, a searchable SQLite history, punctuation and capitalisation.

The engine is VOSK (Kaldi ASR) on the CPU — no GPU, and no network once the
recognition model is downloaded.

### Why it suits a Scoop bucket

- A single portable executable in a zip — no installer, nothing to register,
  no system-wide state beyond the files Scoop manages.
- Free, no account, no ads.
- Closed source with a permissive-use licence: free to install and use on your
  own machines, no redistribution or modification. The licence text is linked
  in the manifest, as required for proprietary packages.
- Releases carry a `SHA256SUMS.txt`, so `autoupdate` reads the hash from the
  release instead of hardcoding it.

### The manifest

- Version: 0.1.5
- Source: https://github.com/alex37529/voxspica/releases/tag/v0.1.5
- `bin`: `VoxSpica.exe`

I have already run `scoop bucket add`, `scoop install voxspica` and
`scoop uninstall voxspica` against a personal bucket
(https://github.com/alex37529/voxspica-scoop) — the install, the shim and the
uninstall all succeed, and `scoop update` reports the manifest up to date.

### What a user should know before installing

- The recognition model is **not** in the archive. On the first launch the
  program asks for a language and downloads one: roughly 50 MB for the small
  model, up to 1.8 GB for the large one. Per-language installers that already
  include a model are published on the project site.
- The executable is **not code-signed**, so Windows may show an unknown
  publisher warning. I expect this to be the main reason for a maintainer to
  hesitate, and I would rather raise it now than have it discovered in review.
- Windows 10/11 x64 only.
```

---

## Черновик PR (после ответа мейнтейнеров)

Ветка в форке `ScoopInstaller/Extras`, файл `bucket/voxspica.json` — ровно тот
манифест, что уже лежит в
https://github.com/alex37529/voxspica-scoop/blob/main/bucket/voxspica.json

**Title** — по шаблону Extras, обычный conventional:

```
voxspica: Add version 0.1.5
```

**Body**

```markdown
- [x] Use conventional PR title
- [x] I have read the [Contributing Guide](https://github.com/ScoopInstaller/.github/blob/main/.github/CONTRIBUTING.md)

Closes #<номер issue>

Offline speech-to-text for Windows: 33 recognition languages, no cloud, no
account, no telemetry. A single portable executable, free of charge; the
licence forbids redistribution and modification and is linked in the manifest.

Tested: `scoop install voxspica`, `voxspica --version` → `VoxSpica 0.1.5`,
`scoop uninstall voxspica`, and `scoop update voxspica` → up to date.
```

---

## Что сделано и что дальше

Готово: https://github.com/alex37529/voxspica-scoop — бакет с манифестом,
проверенный настоящим Scoop:

| Проверка | Результат |
|---|---|
| `scoop bucket add` | бакет подключился |
| `scoop search voxspica` | `voxspica 0.1.5` в списке |
| `scoop install voxspica` | скачал 58.3 МБ, хеш сошёлся, shim создан |
| `voxspica --version` | `VoxSpica 0.1.5` |
| `scoop update voxspica` | `0.1.5 (latest version)` — `checkver` и `autoupdate` разбираются |
| `scoop uninstall voxspica` | shim удалён, следов не осталось |

На машине Scoop остался установленным (это его обычное состояние, и бакет
подключён), но **VoxSpica через Scoop удалён** — не оставлял вторую копию
программы рядом с той, что стоит в Program Files.

Твой ход: опубликовать issue по черновику выше. Дальше по обсуждению покажу
PR — текст уже готов.
