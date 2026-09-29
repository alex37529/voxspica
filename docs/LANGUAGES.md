# Languages

Two independent settings decide what VoxSpica does with a language:

| | What it is | How many |
| --- | --- | --- |
| **Recognition language** | the language you *speak*; it decides which model is needed | 33 |
| **Interface language** | the language the buttons are written in | 9 |

You can dictate Ukrainian into an English interface. Nothing ties them
together, and nothing requires them to match.

---

## Interface languages

Switch in `Settings` → **Interface**. There are 9, each listed in its own
language so you can find yours without reading English.

| Code | Language | Has an installer? |
| --- | --- | --- |
| `be` | Беларуская | — |
| `de` | Deutsch | yes |
| `en` | English | yes |
| `es` | Español | yes |
| `fr` | Français | yes |
| `it` | Italiano | yes |
| `ru` | Русский | yes |
| `uk` | Українська | — |
| `zh` | 简体中文 | yes |

Seven of the nine have an installer. Belarusian and Ukrainian do not:
the installer builder ships wizard strings for 35 languages and these two
are not among them. The application speaks both — only the installer is
missing, and the portable build covers them.

---

## Recognition languages

All 33, with the models that exist in the VOSK registry. A dash means the
registry has no model of that size for that language, so the program does
not offer it.

| Code | Language | small (~50 MB) | large (~1.8 GB) |
| --- | --- | --- | --- |
| `ar` | العربية | — | `vosk-model-ar-mgb2-0.4` |
| `br` | Português (Brasil) | — | `vosk-model-br-0.8` |
| `ca` | Català | `vosk-model-small-ca-0.4` | — |
| `cn` | 中文 | `vosk-model-small-cn-0.22` | `vosk-model-cn-0.22` |
| `cs` | Čeština | `vosk-model-small-cs-0.4-rhasspy` | — |
| `de` | Deutsch | `vosk-model-small-de-0.15` | `vosk-model-de-0.21` |
| `el-gr` | Ελληνικά | — | `vosk-model-el-gr-0.7` |
| `en-in` | English (India) | `vosk-model-small-en-in-0.4` | `vosk-model-en-in-0.5` |
| `en-us` | English (US) | `vosk-model-small-en-us-0.15` | `vosk-model-en-us-0.22` |
| `eo` | Esperanto | `vosk-model-small-eo-0.42` | — |
| `es` | Español | `vosk-model-small-es-0.42` | `vosk-model-es-0.42` |
| `fa` | فارسی | `vosk-model-small-fa-0.42` | `vosk-model-fa-0.42` |
| `fr` | Français | `vosk-model-small-fr-0.22` | `vosk-model-fr-0.22` |
| `gu` | ગુજરાતી | `vosk-model-small-gu-0.42` | `vosk-model-gu-0.42` |
| `hi` | हिन्दी | `vosk-model-small-hi-0.22` | `vosk-model-hi-0.22` |
| `it` | Italiano | `vosk-model-small-it-0.22` | `vosk-model-it-0.22` |
| `ja` | 日本語 | `vosk-model-small-ja-0.22` | `vosk-model-ja-0.22` |
| `ka` | ქართული | `vosk-model-small-ka-0.42` | `vosk-model-ka-0.42` |
| `ko` | 한국어 | `vosk-model-small-ko-0.22` | — |
| `ky` | Кыргызча | `vosk-model-small-ky-0.42` | `vosk-model-ky-0.42` |
| `kz` | Қазақша | `vosk-model-small-kz-0.42` | `vosk-model-kz-0.42` |
| `nl` | Nederlands | `vosk-model-small-nl-0.22` | `vosk-model-nl-spraakherkenning-0.6` |
| `pl` | Polski | `vosk-model-small-pl-0.22` | — |
| `pt` | Português | `vosk-model-small-pt-0.3` | `vosk-model-pt-fb-v0.1.1-20220516_2113` |
| `ru` | Русский | `vosk-model-small-ru-0.22` | `vosk-model-ru-0.42` |
| `sv` | Svenska | `vosk-model-small-sv-rhasspy-0.15` | — |
| `te` | తెలుగు | `vosk-model-small-te-0.42` | — |
| `tg` | Тоҷикӣ | `vosk-model-small-tg-0.22` | `vosk-model-tg-0.22` |
| `tl-ph` | Tagalog | — | `vosk-model-tl-ph-generic-0.6` |
| `tr` | Türkçe | `vosk-model-small-tr-0.3` | — |
| `uk` | Українська | `vosk-model-small-uk-v3-nano` | `vosk-model-uk-v3` |
| `uz` | Oʻzbekcha | `vosk-model-small-uz-0.22` | — |
| `vn` | Tiếng Việt | `vosk-model-small-vn-0.4` | `vosk-model-vn-0.4` |

### Reading the table

- **Both sizes (20):** `cn`, `de`, `en-in`, `en-us`, `es`, `fa`, `fr`, `gu`, `hi`, `it`, `ja`, `ka`, `ky`, `kz`, `nl`, `pt`, `ru`, `tg`, `uk`, `vn`
- **Large only (4):** `ar`, `br`, `el-gr`, `tl-ph`
- **Small only (9):** `ca`, `cs`, `eo`, `ko`, `pl`, `sv`, `te`, `tr`, `uz`

Not every language has both sizes, and that is the registry's doing, not
the program's. `Settings` → **Models** says so rather than offering a
download that would fail.

### Notes on individual languages

- **English** is two: `en-us` and `en-in`, trained on different accents.
  `en-gb` does not exist; use `en-us`.
- **Portuguese** is `pt` (Brazilian, `vosk-model-pt-fb-…`). There is no
  European Portuguese model in the registry.
- **Chinese** is `cn` — Mandarin, `vosk-model-small-cn-0.22`.
- **Greek** is `el-gr`, **Filipino** is `tl-ph`, and the dashes in those
  codes are part of the registry name, not punctuation.
- **Gujarati** (`gu`), **Hindi** (`hi`) and **Telugu** (`te`) all map to
  the same scripts; VOSK ships separate models for each.

---

## Where models are stored

Next to the program when it can write there, otherwise in
`%LOCALAPPDATA%\VoxSpica\models`. The per-language installers unpack
their model next to the executable; anything downloaded at run time goes
to the writable location. You can delete a model from
`Settings` → **Models** and download it again later.

---

## See also

- [User guide](USER-GUIDE.md) — every screen, step by step
- [README](../README.md) — what it is, and what it does not do
- [VOSK models](https://alphacephei.com/vosk/models) — the upstream registry
