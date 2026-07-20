# termux-share

> Share text, URLs, clipboard content, and piped data from the Termux terminal directly to Android's share menu.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-2.1-blue.svg)]()

---

## About

`termux-share` is a lightweight Bash script that bridges the gap between the Termux terminal and Android's native share system. It allows you to instantly send text, URLs, clipboard content, file contents, and piped command output to any app on your device (WhatsApp, Telegram, Gmail, Notes, etc.) without leaving the terminal.

---

## Features

| Feature | Command |
|---------|---------|
| Share text | `termux-share --content "text"` |
| Share URL | `termux-share --url https://...` |
| Share clipboard | `termux-share --clipboard` |
| Share piped input | `echo "text" \| termux-share --pipe` |
| Share file content | `termux-share --file-content file.txt` |
| Quick note | `termux-share --quick "note"` |
| Interactive menu | `termux-share --interactive` |

---

## Installation

### One-Line Install

```bash
curl -O https://raw.githubusercontent.com/BullLazy/termux-share/main/termux-share && chmod +x termux-share && mkdir -p ~/bin && mv termux-share ~/bin/ && echo 'export PATH="$HOME/bin:$PATH"' >> ~/.bashrc && source ~/.bashrc

### Git Clone
`git clone https://github.com/KULLANICI_ADIN/termux-share.git
cd termux-share
cp termux-share ~/bin/
chmod +x ~/bin/termux-share`
