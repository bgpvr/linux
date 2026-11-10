# BGPVR Player for Linux

[![bgpvr-player](https://snapcraft.io/bgpvr-player/badge.svg)](https://snapcraft.io/bgpvr-player)

Downloads of BGPVR Player for Linux (.deb and AppImage). Software only: the app shows the TV service of your own
provider and brings no TV channels or content. Builds only: the app's source code is not published here. The source of
the open-source libraries inside the app (LGPL) is published next to each release.

The files are on the [Releases](https://github.com/bgpvr/linux/releases) page. Checksums: [SHA256SUMS](SHA256SUMS).

## Install with apt (recommended)

Ubuntu 22.04, 24.04 and newer and the distributions based on them (Linux Mint, Pop!_OS, Zorin OS, elementary OS), 64-bit PC.
New versions then arrive with your normal system updates.

```
curl -fsSL https://apt.bgpvr.com/bgpvr.gpg | sudo tee /usr/share/keyrings/bgpvr.gpg >/dev/null
echo "deb [signed-by=/usr/share/keyrings/bgpvr.gpg] https://apt.bgpvr.com stable main" | sudo tee /etc/apt/sources.list.d/bgpvr.list
sudo apt update && sudo apt install bgpvr-player
```

Signing key fingerprint: `EAB6 9BB9 68DF 78FA 7494 581F 31DF 41E0 3FFF D9E9`. Remove: `sudo apt remove bgpvr-player`.

## 1.9.9-24

| File | For |
|---|---|
| [bgpvr-player-linux-1.9.9-24-x86_64.deb](https://github.com/bgpvr/linux/releases/download/v1.9.9-24/bgpvr-player-linux-1.9.9-24-x86_64.deb) | Ubuntu 22.04, 24.04 and newer, Linux Mint, Pop!_OS (x86_64) |
| [bgpvr-player-linux-1.9.9-24-x86_64.AppImage](https://github.com/bgpvr/linux/releases/download/v1.9.9-24/bgpvr-player-linux-1.9.9-24-x86_64.AppImage) | Other 64-bit (x86_64) Linux with glibc 2.35 or newer |
| [bgpvr-player-linux-1.9.9-24-lgpl-sources.tar](https://github.com/bgpvr/linux/releases/download/v1.9.9-24/bgpvr-player-linux-1.9.9-24-lgpl-sources.tar) | The source of the LGPL libraries in this release (FFmpeg, mpv, libplacebo …) and how to rebuild and replace them |

Install by hand:

- **.deb**: `sudo apt install ./bgpvr-player-linux-1.9.9-24-x86_64.deb`, then open **BGPVR Player** from the menu
  (the menu entry also has **Start in TV mode**). The .deb brings its own libmpv and FFmpeg in /opt/bgpvr-player.
- **AppImage**: `chmod +x bgpvr-player-linux-1.9.9-24-x86_64.AppImage`, then open it. If it asks for libfuse.so.2:
  `sudo apt install libfuse2` (22.04) or `libfuse2t64` (24.04 and newer).

Check the download: `sha256sum -c SHA256SUMS --ignore-missing`.

Hardware video decoding uses VA-API. On Intel graphics install `intel-media-va-driver` (`sudo apt install intel-media-va-driver`);
without it the app decodes on the CPU.

Keys: **Esc** = Back, **F11** = full screen (a double click on the picture too). Start with `--tv` for the TV layout.
Casting, recording to the device, picture-in-picture and push messages are not in the Linux app.

Older builds stay on the [Releases](https://github.com/bgpvr/linux/releases) page.

BGPVR Player is made by BGPVR Software. Linux is a registered trademark of Linus Torvalds.

## Snap Store

    sudo snap install bgpvr-player
