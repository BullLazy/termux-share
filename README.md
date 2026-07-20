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
```

### Git Clone

```bash
git clone https://github.com/BullLazy/termux-share.git
cd termux-share
cp termux-share ~/bin/
chmod +x ~/bin/termux-share
```

## Usage 

### Share Text

```bash
termux-share --content "Hello from Termux!"
termux-share --content "Meeting tomorrow at 3pm"
```
### Share Url

```bash
termux-share --url https://github.com
termux-share --url https://termux.dev
```

### Share Clipboard Content

```bash
termux-share --clipboard
termux-share -c
```
`Requires: termux-api`, `package: pkg install termux-api`

### Shared Piped Command Output

```bash
ls -la | termux-share --pipe
cat notes.txt | termux-share --pipe
df -h | termux-share -p
cal | termux-share --pipe
```
### Share File Content as Text

```bash
termux-share --file-content report.txt
termux-share -f ~/notes/todo.md
```

### Quick One-Liner

```bash
termux-share --quick "Don't forget the milk!"
termux-share -q "Server reboot at midnight"
```

### İnteractive Menu

```bash
termux-share --interactive
termux-share -i
```

## Dependencies 

`Termux` (obviously)
`termux-api` (only for --clipboard features)
```bash
pkg install termux-api
```

## Contributing

Contributions are welcome! Feel free to:

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m "Add amazing feature"`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Roadmap

- [ ] Direct file attachment sharing
- [ ] Share via specific app (`--via com.whatsapp`)
- [ ] Config file support (`~/.config/termux-share.conf`)
- [ ] History of shared items
- [ ] Add to official Termux packages

## License

MIT License - see [LICENSE](LICENSE) file for details.

## Acknowledgments

- - [Termux](https://termux.dev) - The terminal emulator that makes this possible
- Android's `am` (Activity Manager) command

## Support

If you find this tool useful, please consider starring the repo ⭐ and sharing it with the Termux community!


---

**Made with ❤️ for the Termux community**
