<!-- header -->
<p align="center"><img src="icon.png" width="112" height="112" alt="" /></p>

<h1 align="center">TotalFetch</h1>

<p align="center">A summary of your computer in your terminal, with your logo, your colour and your lines.</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-0.1.0-9ad959" alt="Version 0.1.0" />
  <img src="https://img.shields.io/badge/status-beta-555" alt="Status: beta" />
  <img src="https://img.shields.io/badge/systems-macOS%20%C2%B7%20Windows%20%C2%B7%20Linux-0078d4" alt="macOS · Windows · Linux" />
</p>

<h2 align="center" id="download">Download</h2>

<p align="center">
  <b>macOS</b> <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalfetch-latest/TotalFetch-mac.dmg">Apple silicon and Intel</a><br>
  <b>Windows</b> <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalfetch-latest/TotalFetch-windows-x64-setup.exe">x64</a> · <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalfetch-latest/TotalFetch-windows-x64.msi">x64 MSI</a> · <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalfetch-latest/TotalFetch-windows-arm64-setup.exe">ARM64</a><br>
  <b>Linux x64</b> <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalfetch-latest/TotalFetch-linux-amd64.deb">deb</a> · <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalfetch-latest/TotalFetch-linux-x86_64.rpm">rpm</a> · <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalfetch-latest/TotalFetch-linux-x86_64.AppImage">AppImage</a><br>
  <b>Linux ARM64</b> <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalfetch-latest/TotalFetch-linux-arm64.deb">deb</a> · <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalfetch-latest/TotalFetch-linux-aarch64.rpm">rpm</a> · <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalfetch-latest/TotalFetch-linux-aarch64.AppImage">AppImage</a>
</p>
<!-- /header -->

TotalFetch puts a summary of your computer in your terminal: the kind of greeting that tells you where you are before you type the first command. The app sets it up with a live preview; the `totalfetch` command shows it in milliseconds.

## What it shows

- **System:** your operating system with its name (macOS Golden Gate 27.2.1), your computer (iMac (24-inch, 2023)), kernel, time since start, shell, terminal, processor and its load, memory, swap, disk, battery, language and local time.
- **Developer tools:** the versions of Node.js, Git, Docker, Ollama and the Total.js 5 command, and your GitHub account in `gh`.
- **Network:** your local IP address, and your public IP address if you turn it on (the only line that asks a server on the internet).

Lines with nothing to say hide themselves: no battery on a desktop, no swap when none is in use.

## Your look

- **Logo:** the mark of Total.js or of Total Avengers, your own ASCII art, or a picture turned into ASCII art with the width you choose.
- **Colour:** one colour for the logo and the labels, in the green of Total.js to start.
- **Layout:** what goes after each label (`:`, `→`, `|`, `·` or nothing), values in one column, and every line on or off, in your order.
- **Looks:** keep a whole look under a name and switch with a click.
- **Copy:** the fetch as plain text for a README, or with its colour codes for another terminal.

The preview shows it on a dark or a light terminal, so you see where your colours land.

## In your terminal

**Install the command** puts `totalfetch` in your terminal:

| System | Command | Greeting |
| --- | --- | --- |
| macOS and Linux | `~/.totaljs/bin/totalfetch` | a marked block at the end of `~/.zshrc` and `~/.bashrc`, and a file of its own for fish |
| Windows | `%LOCALAPPDATA%\TotalJS\bin\totalfetch.exe` | a marked block in the PowerShell profiles |

**Greet me when a terminal opens** turns the greeting on or off without touching those files again. Before a file is changed for the first time, a copy is kept next to it, and uninstalling takes out exactly what was put in.

```text
totalfetch            the summary
totalfetch --plain    without colours (also with NO_COLOR)
totalfetch --help     the options
```

## Privacy

Everything is read from your computer as you look at it. Nothing is sent anywhere, unless you turn on the public IP address.

## Report a problem

[Open an issue](https://github.com/totaljs-es/totaljs-desktop/issues/new/choose) and choose TotalFetch, with its version and your system.
