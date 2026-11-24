# mirror.cx

Arch Linux and CachyOS package mirrors, served from five countries.

**Status:** <https://mirror.cx/>
**Arch listing:** <https://archlinux.org/mirrors/mirror.cx/>

## Mirrors

| Mirror | Location |
| --- | --- |
| `ca.mirror.cx` | Canada |
| `ch.mirror.cx` | Switzerland |
| `uk.mirror.cx` | United Kingdom |
| `nl.mirror.cx` | Netherlands |
| `no.mirror.cx` | Norway |

Access is available over HTTP, HTTPS and rsync. Arch syncs hourly, CachyOS
every 30–60 minutes. Arch ISOs and CachyOS ISOs are included.

## Use

Arch Linux — `/etc/pacman.d/mirrorlist` (swap `nl` for your nearest node):

```ini
Server = https://nl.mirror.cx/archlinux/$repo/os/$arch
```

CachyOS — `/etc/pacman.d/cachyos-mirrorlist`:

```ini
Server = https://nl.mirror.cx/cachyos/repo/$arch/$repo
```

rsync, for downstream mirrors:

```sh
rsync -rtlH --delete-after --safe-links \
  rsync://nl.mirror.cx/archlinux/ /srv/mirror/archlinux/
```

## Contact

Open an issue in this repository. Include the mirror hostname and the URL you
were fetching.
