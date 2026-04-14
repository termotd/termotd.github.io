# 🎨 MOTD Color Generator

> Transform ASCII art and banners into colorful bash scripts for your Linux terminal login screen.

![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen?style=flat-square&logo=github)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)
![No Install](https://img.shields.io/badge/No%20Install-Just%20open%20in%20browser-orange?style=flat-square)

---

## 🖥️ What is this?

When you log into a Linux server or Raspberry Pi via SSH, the terminal shows a **MOTD (Message of the Day)** — a welcome screen with system info, banners, and ASCII art.

To colorize that screen, you need `echo -e` commands with ANSI escape codes like:
```bash
echo -e "\033[32m  ██████╗ ██╗  \033[0m"
```

Writing those by hand for every single line is painful. **This tool does it for you in seconds.**

---

## ✨ Features

- 🎨 **Color per line** — assign a different ANSI color to each line individually
- 🖊️ **Inline placeholder mode** — use `{G}green text{/}` or `{YB}bold yellow{/}` inline
- 👁️ **Live terminal preview** — see exactly how it will look before copying
- 📋 **One-click copy** — copy the full script to clipboard instantly
- 📦 **Three output modes:**
  - Raw `echo -e "\033[...]"` script
  - Clean version with named variables (`${GREEN}`, `${CYAN}`)
  - Live terminal preview
- 🌙 **Dark terminal theme** — designed to feel like a real terminal
- 🔌 **No install needed** — just open `index.html` in any browser

---

## 🚀 How to use

### Online (GitHub Pages)
Just visit: **[termotd.github.io](https://termotd.github.io)**

### Offline
1. Download or clone this repo
2. Open `index.html` in your browser
3. Done — no server, no dependencies!


---

## 📖 Step by step

1. **Paste your ASCII art** into the left text box
   - You can grab free ASCII banners from [patorjk.com](https://patorjk.com/software/taag/) or [ascii-art.de](https://ascii-art.de)

2. **Choose a global color** from the color panel on the right

3. **Customize per line** — each line gets its own color dropdown

4. **Click ⚡ Generate Script**

5. **Copy the output** and paste it into your Raspberry Pi:

```bash
sudo nano /etc/update-motd.d/00-banner
```

Paste the script, save, then test it:
```bash
sudo run-parts /etc/update-motd.d/
```

---

## 🎨 Supported ANSI Colors

| Code | Color | Code | Color |
|------|-------|------|-------|
| `\033[32m` | 🟢 Green | `\033[1;32m` | 💚 Bold Green |
| `\033[36m` | 🔵 Cyan | `\033[1;36m` | 💙 Bold Cyan |
| `\033[33m` | 🟡 Yellow | `\033[1;33m` | 💛 Bold Yellow |
| `\033[31m` | 🔴 Red | `\033[1;31m` | ❤️ Bold Red |
| `\033[35m` | 🟣 Magenta | `\033[1;35m` | 💜 Bold Magenta |
| `\033[34m` | 🔵 Blue | `\033[1;37m` | 🤍 Bold White |

---

## 📂 Project structure

```
termotd.github.io/
├── index.html         ← The entire tool (single file, no dependencies)
├── README.md
└── .github/
    └── workflows/
        └── static.yml ← GitHub Pages auto-deploy
```

---

## 🍓 Tested on

- Raspberry Pi 5 (8GB)
- Raspberry Pi 4 Model B (4GB)
- Ubuntu Server 22.04
- Debian 12 (Bookworm)

---

## 📄 License

MIT — free to use, modify and share.

---

Made with ❤️ by [hohky](https://github.com/hohky)
