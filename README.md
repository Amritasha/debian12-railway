![Debian](https://img.shields.io/badge/Debian-12%20Bookworm-A81D33?logo=debian)
![Docker](https://img.shields.io/badge/Docker-Supported-blue?logo=docker)

# Debian 12 Terminal on Railway

A browser-accessible Debian 12 (Bookworm) terminal deployed on Railway using [ttyd](https://github.com/tsl0922/ttyd).

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.com/new/template)

## Description

Deploys a lightweight Debian 12 container accessible from any browser. No local installation required. Comes with essential dev tools pre-installed and a persistent volume mounted at `/root`.

## Environment Variables

| Variable | Description |
|----------|-------------|
| `PORT` | Port for ttyd to listen on (default: 7681) |
| `USERNAME` | Login username for the web terminal |
| `PASSWORD` | Login password for the web terminal |

> **Note:** Always set USERNAME and PASSWORD before deploying.

## Features

- 🐧 Debian 12 Bookworm (stable)
- 🔒 Password-protected web terminal
- 💾 Persistent volume mounted at `/root`
- 💻 Neofetch on login
- 🛠️ Pre-installed tools:

| Category | Tools |
|---|---|
| Editors | vim, nano |
| System | htop, tree, lsof, strace, less, man |
| Files | unzip, zip |
| Build | gcc, g++, make, build-essential |
| Network | ifconfig, ip, ping, dig, openssh-client, telnet, netcat |
| Data | jq |
| General | sudo, python3, pip, git, curl, wget, neofetch |

## Installing More Packages

```bash
apt-get install -y <package-name>
```

> **Note:** Files saved inside `/root` persist across restarts. Packages installed via `apt-get` will not survive a full redeploy.

## Use Cases

- Lightweight cloud Linux terminal
- Debian-based build and test environment
- Script development and automation
- Learning Debian/Linux without local setup
