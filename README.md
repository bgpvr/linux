# BGPVR Player for Linux

Downloads of BGPVR Player for Linux (.deb and AppImage). Software only: the app shows the TV service of your own
provider and brings no TV channels or content. Builds only: the app's source code is not published here.

The files are on the [Releases](https://github.com/bgpvr/linux/releases) page. Checksums: [SHA256SUMS](SHA256SUMS).

## 1.9.4-3 (beta)

| File | For |
|---|---|
| [bgpvr-player-linux-1.9.4-3-x86_64.deb](https://github.com/bgpvr/linux/releases/download/v1.9.4-3/bgpvr-player-linux-1.9.4-3-x86_64.deb) | Ubuntu 22.04, Linux Mint 21, Pop!_OS 22.04 (x86_64) |
| [bgpvr-player-linux-1.9.4-3-x86_64.AppImage](https://github.com/bgpvr/linux/releases/download/v1.9.4-3/bgpvr-player-linux-1.9.4-3-x86_64.AppImage) | Other 64-bit (x86_64) Linux with glibc 2.35 or newer, Ubuntu 24.04 and later too |

Install:

- **.deb**: `sudo apt install ./bgpvr-player-linux-1.9.4-3-x86_64.deb`, then open **BGPVR Player** from the menu
  (the menu entry also has **Start in TV mode**).
- **AppImage**: `chmod +x bgpvr-player-linux-1.9.4-3-x86_64.AppImage`, then open it.

Check the download: `sha256sum -c SHA256SUMS --ignore-missing`.

Keys: **Esc** = Back, **F11** = full screen (a double click on the picture too). Start with `--tv` for the TV layout.

This is a beta. Video is drawn on the graphics card and switches to the CPU by itself if that does not work;
`BGPVR_SW_VIDEO=1` forces the CPU. Casting, recording to the device and push messages are not in the Linux app.

BGPVR Player is made by BGPVR Software. Linux is a registered trademark of Linus Torvalds.
