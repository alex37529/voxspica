# Installing on Ubuntu and Debian

VoxSpica ships as a native `.deb` and as an APT repository. **Use the
repository** — it is the only one of the two that gets the app into the Ubuntu
Software app with a screenshot and a description.

- [Why the repository, not the file](#why-the-repository-not-the-file)
- [Installing](#installing)
- [Updating and removing](#updating-and-removing)
- [If the repository is not signed](#if-the-repository-is-not-signed)
- [Troubleshooting](#troubleshooting)
- [See also](#see-also)

---

## Why the repository, not the file

Both ways give you the same program. They differ in what the Ubuntu Software
app shows afterwards.

| | `apt install voxspica` | opening the `.deb` file |
|---|---|---|
| Icon in Software app | VoxSpica | a grey placeholder |
| Screenshot | yes | none |
| Description and changelog | yes | none |
| "Installed" section | yes | no |
| `apt upgrade` picks up updates | yes | no |

This is not a defect in the build. The view that opens a `.deb` file builds its
page from the package's `control` file alone — the AppStream metadata that
carries the screenshot is a separate file inside the package and is simply not
read there. Only an **installed** package gets its metadata read, and only the
installed-from-a-repository one shows up with an icon worth looking at.

## Installing

Ubuntu 22.04 (`jammy`) and 24.04 (`noble`) are supported, architecture `amd64`.

### 1. Add the repository key

Check the key fingerprint before you trust it. It is printed by every release
and also served from the repository itself:

```
F118 995C 50C1 EACB 4922 2A33 0DBF 9437 A118 15D9
```

```bash
curl -fsSL https://alex37529.github.io/voxspica/voxspica-archive-keyring.asc \
  | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/voxspica.gpg
```

You can read it back and compare:

```bash
gpg --show-keys --with-fingerprint /etc/apt/trusted.gpg.d/voxspica.gpg
```

### 2. Add the repository

```bash
echo "deb https://alex37529.github.io/voxspica/repo/ jammy main" \
  | sudo tee /etc/apt/sources.list.d/voxspica.list
```

Use `noble` instead of `jammy` on Ubuntu 24.04.

### 3. Install

```bash
sudo apt update
sudo apt install voxspica
```

That puts `voxspica` on your `PATH`. The recognition model is not in the
package: on the first launch the program asks for a language and downloads one
(50 MB for a small model, up to 1.8 GB for a large one).

To remove it:

```bash
sudo apt remove voxspica
```

## Updating and removing

Later versions arrive with the normal system update:

```bash
sudo apt update && sudo apt upgrade
```

`apt upgrade` is enough — nothing needs to be downloaded by hand.

> Only the newest version is kept in the repository. Older `.deb` files are not
> discarded: they remain in the
> [releases](https://github.com/alex37529/voxspica/releases), where each version
> keeps its own assets.

## If the repository is not signed

A signed repository means `apt` verifies that the index really came from
VoxSpica before it reads it. If you are installing from a build where signing
was not set up, `apt` will refuse and ask for `[trusted=yes]`:

```bash
echo "deb [trusted=yes] https://alex37529.github.io/voxspica/repo/ jammy main" \
  | sudo tee /etc/apt/sources.list.d/voxspica.list
sudo apt update
```

`[trusted=yes]` turns off signature checking for that source entirely, packages
included. It is a fallback for a repository that is not signed, not the
recommended way to install.

## Troubleshooting

**`apt update` says the repository does not have a Release file.** The codename
in your `sources.list` does not match a directory the repository publishes.
Check that it is one of `jammy` or `noble`.

**`NO_PUBKEY` on `apt update`.** The key was not installed, or step 2 was
skipped. Re-run step 1 and then `sudo apt update`.

**The Software app still shows a placeholder.** The app is probably still
registered from the `.deb` you opened earlier. Uninstall that package, then
install from the repository:

```bash
sudo apt remove voxspica
sudo apt install voxspica
```

Then restart the Software app — it caches metadata and does not always notice a
package appearing on its own.

**No screenshot after installing from the repository.** A screenshot needs the
network: the image is fetched from the web, because that is what the AppStream
specification asks for. Behind a proxy or fully offline, the app is installed
and works, but the Software app has no picture to show.

**Verify by hand, without the Software app:**

```bash
apt-cache policy voxspica           # apt sees the package
sudo apt install --reinstall voxspica
appstreamcli validate /usr/share/metainfo/com.*voxspica.metainfo.xml
```

## See also

- [User guide](USER-GUIDE.md) — how to use the program
- [Releases](https://github.com/alex37529/voxspica/releases) — every version,
  and the per-language Windows installers
- [README](../README.md) — the other ways to install