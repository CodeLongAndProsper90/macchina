![Macchina preview image](screenshots/banner.png)

[![Crates.io](https://img.shields.io/crates/v/macchina?style=for-the-badge&label=VERSION&color=0D3B66)](https://crates.io/crates/macchina)
[![Crates.io](https://img.shields.io/crates/d/macchina?style=for-the-badge&label=DOWNLOADS&color=0D3B66)](https://crates.io/crates/macchina)
![reposize](https://img.shields.io/github/repo-size/grtcdr/macchina?color=0D3B66&logo=github&style=for-the-badge)
![loc](https://img.shields.io/tokei/lines/github/grtcdr/macchina?color=0D3B66&label=Lines%20of%20Code&logo=rust&style=for-the-badge)

---

# About Macchina
Macchina is a fetching program, not a library.

Macchina lets you view basic system information, like your hostname, kernel, uptime, memory usage, and much more.
It provides you with convenient features and customization options but doesn't lose sight of its two main priorities: minimalism and performance.

![Macchina preview image](screenshots/preview.png)

---

# Dependencies
- [wmctrl](http://tripie.sweb.cz/utils/wmctrl/) to print your window manager
- If you're on __NetBSD__, you'll want to install:
  - [ripgrep](https://github.com/BurntSushi/ripgrep)

---

# Benchmarks
Macchina is pretty fast, see for yourself!

- Execution time is measured using [hyperfine](https://github.com/sharkdp/hyperfine)

| Command | Mean [ms] | Min [ms] | Max [ms] | Relative |
|:---|---:|---:|---:|---:|
| `macchina` | 42.6 ± 0.5 | 41.8 | 45.2 | 1.00 |
| `neofetch` | 371.1 ± 3.0 | 366.4 | 379.9 | 8.71 ± 0.13 |

__Summary__: `macchina` runs __8.71 ± 0.13__ times __faster__ than `neofetch`

- Note that hiding elements with __--hide__ significantly improves speed

---

# Features
### Themes
![Theme preview](screenshots/themes.png)

### Bars
![Preview of bar argument](screenshots/bars.png)

### What it fetches
- Host
  - Username
  - Hostname
- Product
- Kernel
- Distribution
- Desktop Environment
- Window Manager
- Package count
- Shell
- Terminal
- Processor
  - Model
  - Thread count
- Uptime
- Memory Usage
- Battery
  - Percentage
  - Status
- Palette

Package count supports package managers of:
- Arch-based distributions
- Debian-based distributions
- Gentoo
- NetBSD

---

# Usage

Macchina comes packed with arguments that let you customize Macchina and its behavior.

The [usage wiki page](https://github.com/grtcdr/macchina/wiki/Usage) can tell you all about them and how they work.

---

# Installation
Macchina is available on:

- [AUR](https://aur.archlinux.org/packages/macchina/)
  ```
  git clone https://aur.archlinux.org/macchina.git
  cd macchina
  makepkg -si

- [NetBSD](https://pkgsrc.se/sysutils/macchina)
  ```
  pkgin install macchina
  ```

- [crates.io](https://crates.io/crates/macchina)
  ```
  cargo install macchina
  ```
  
---

# Platform Support	

|  Platform     |      Support       |
| :-:           |        :-:         |
| Linux         |        Yes         |
| NetBSD [1]    |        Yes         |
| MacOS         |                    |
| Windows       |                    |

[1]: Support for NetBSD would not be possible without the help and testing of NetBSD package maintainer [pin](https://pkgsrc.se/bbmaint.php?maint=pin@NetBSD.org). Thanks __pin__!
