# Wallpaper Engine Download Web

> Download all wallpapers for Wallpaper Engine without logging in.

<p align="center">
  <a href="./README.md"><img src="https://img.shields.io/badge/%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87-Switch-2563eb?style=for-the-badge" alt="简体中文" /></a>
  <a href="./README.en.md"><img src="https://img.shields.io/badge/English-Current-16a34a?style=for-the-badge" alt="English" /></a>
</p>

## Badges

![version](https://img.shields.io/badge/version-2.0.0-3fb950?style=flat-square)
![node](https://img.shields.io/badge/node-%3E%3D16-43853d?style=flat-square&logo=nodedotjs&logoColor=white)
![runtime](https://img.shields.io/badge/runtime-Node.js-5fa04e?style=flat-square&logo=node.js&logoColor=white)
![downloader](https://img.shields.io/badge/downloader-SteamCMD-1b2838?style=flat-square&logo=steam&logoColor=white)
![frontend](https://img.shields.io/badge/frontend-Vanilla%20JS-f7df1e?style=flat-square&logo=javascript&logoColor=000)
![dependency](https://img.shields.io/badge/dependency-zero-0ea5e9?style=flat-square)

## Tech Stack

### Backend

<p>
  <img src="https://skillicons.dev/icons?i=nodejs" alt="Node.js" />
  <img src="https://cdn.simpleicons.org/steam/ffffff" alt="SteamCMD" width="48" height="48" />
</p>

### Frontend

<p>
  <img src="https://skillicons.dev/icons?i=js,html,css" alt="JavaScript, HTML, CSS" />
</p>

## Project Introduction

This tool is designed to retrieve and download wallpaper data from the Steam Workshop for Wallpaper Engine. It allows users to browse and download wallpapers directly through a web interface.

**Key Advantage**: It utilizes **SteamCMD**'s anonymous login feature to download workshop items, eliminating the need to log in to a Steam account for most free wallpapers.

## Core Features

- **No Login Required**: Leverages SteamCMD anonymous login to download resources.
- **Smart Parsing**: Automatically scrapes Workshop pages to retrieve File IDs and metadata.
- **Automatic Packaging**:
  - **Scene/App/Web Wallpapers**: Automatically packaged into `.zip` files.
  - **Video Wallpapers**: Downloads the raw video file directly for immediate playback.
- **Zero Dependency**: Built with pure Node.js (standard libraries only), no `npm install` required.

## Technical Architecture

- **Runtime**: Node.js (>=16)
- **Core Downloader**: [SteamCMD](https://developer.valvesoftware.com/wiki/SteamCMD) (Valve's command-line Steam client)
- **Frontend**: Vanilla JavaScript (No frameworks)
- **Backend**: Native Node.js `http` module

## Prerequisites

1. **Node.js**: Ensure Node.js (v16 or later) is installed.
2. **Network Access (Region-dependent)**: Whether a proxy is required depends on your network location. If Steam Workshop is directly reachable in your region, no proxy is needed. If access is restricted, enable a system proxy or configure proxy environment variables.
3. **SteamCMD**: The tool will attempt to automatically find or download SteamCMD. If it fails, you may need to install it manually.

## Quick Start

1. **Clone/Download** this repository.
2. **Start the Server**:
   ```bash
   node server.js
   ```
3. **Open Browser**: Visit `http://localhost:3090` (or the port displayed in the console).

## Configuration (Optional)

You can configure the tool using Environment Variables:

| Variable | Description | Default |
|----------|-------------|---------|
| `PORT` | Web server port | `3090` |
| `HTTP_PROXY` | Proxy URL (e.g., `http://127.0.0.1:7890`) | System Default |
| `STEAM_USERNAME` | Steam Account (if anonymous fails) | - |
| `STEAM_PASSWORD` | Steam Password | - |
| `STEAM_COUNTRY` | Store Country Code | - |
| `STEAM_LANG` | Store Language | `schinese` |

> **Note**: While the tool aims to be login-free, some wallpapers may strictly require a valid Steam account. In such cases, you can set `STEAM_USERNAME` and `STEAM_PASSWORD`.

## Development Statement

This project was constructed with the assistance of artificial intelligence. It is provided "as-is" for educational and personal use.
