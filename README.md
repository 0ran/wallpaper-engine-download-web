# Wallpaper Engine 创意工坊下载工具

> 免登录下载 Wallpaper Engine 创意工坊壁纸。

<p align="center">
  <a href="./README.en.md">English</a>
   · 
  <a href="./README.md">简体中文</a>
</p>

## 项目徽章

[![version](https://img.shields.io/badge/version-2.0.0-3fb950?style=flat-square)](https://semver.org/)
[![node](https://img.shields.io/badge/node-%3E%3D16-43853d?style=flat-square&logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![runtime](https://img.shields.io/badge/runtime-Node.js-5fa04e?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org/en/about)
[![downloader](https://img.shields.io/badge/downloader-SteamCMD-1b2838?style=flat-square&logo=steam&logoColor=white)](https://developer.valvesoftware.com/wiki/SteamCMD)
[![frontend](https://img.shields.io/badge/frontend-Vanilla%20JS-f7df1e?style=flat-square&logo=javascript&logoColor=000)](https://developer.mozilla.org/docs/Web/JavaScript)
[![dependency](https://img.shields.io/badge/dependency-zero-0ea5e9?style=flat-square)](https://nodejs.org/docs/latest/api/)

## 技术栈展示

<p>
  <a href="https://nodejs.org/" target="_blank" rel="noopener noreferrer"><img src="https://skillicons.dev/icons?i=nodejs" alt="Node.js" /></a>
  <a href="https://developer.valvesoftware.com/wiki/SteamCMD" target="_blank" rel="noopener noreferrer"><img src="https://cdn.simpleicons.org/steam/ffffff" alt="SteamCMD" width="48" height="48" /></a>
  <a href="https://developer.mozilla.org/" target="_blank" rel="noopener noreferrer"><img src="https://skillicons.dev/icons?i=js,html,css" alt="JavaScript, HTML, CSS" /></a>
</p>

## 项目简介

本项目是一个基于 Web 的 Steam 创意工坊下载工具，专为 Wallpaper Engine 设计。它通过网页界面提供壁纸搜索和下载功能。

**核心优势**：利用 **SteamCMD** 的匿名登录特性，无需登录个人 Steam 账号即可下载大部分公开的壁纸资源。

## 核心特点

- **免登录下载**：通过 SteamCMD 匿名模式获取资源，保护隐私。
- **智能解析**：自动抓取创意工坊页面，提取 FileID 和元数据。
- **自动打包规则**：
  - **场景/程序/网页类壁纸**：下载后自动打包为 `.zip` 压缩包，解压即可使用。
  - **视频类壁纸**：直接提取原始视频文件（.mp4等），下载后可直接播放。
- **零依赖构建**：仅使用 Node.js 原生模块，无需 `npm install`，开箱即用。

## 截图展示

<img width="1573" height="1142" alt="123123123" src="https://github.com/user-attachments/assets/624f6abe-1fd6-4ffe-afb4-b93a40ead201" />
</br>
<img width="1573" height="1351" alt="SnowShot_2026-03-08_13-57-40" src="https://github.com/user-attachments/assets/6903ac0e-3bcc-4f1e-9446-c3b2e0f65ca1" />
</br></br>
<img width="33%" height="1223" alt="333" src="https://github.com/user-attachments/assets/397b907a-b7fc-4b3c-b5da-0580b948e342" />
<img width="33%" height="1223" alt="444" src="https://github.com/user-attachments/assets/a3fe9cce-d0d4-4559-8511-1c52d3a9759e" />
<img width="33%" height="1224" alt="SnowShot_2026-03-08_13-54-12" src="https://github.com/user-attachments/assets/9f789a17-bbf1-4013-a72b-94036fe345fe" />
</br></br>
<img width="33%" height="1223" alt="111" src="https://github.com/user-attachments/assets/2882fcd9-023f-4952-bf9b-18e624f79e3c" />
<img width="33%" height="1223" alt="222" src="https://github.com/user-attachments/assets/36db3d9b-1074-4b9a-bc73-d405e21d5964" />
<img width="33%" height="1223" alt="555" src="https://github.com/user-attachments/assets/635a22c1-258a-469c-95fb-0cf00185892a" />

## 技术架构

- **运行环境**：Node.js (>=16)
- **核心下载器**：[SteamCMD](https://developer.valvesoftware.com/wiki/SteamCMD) (Valve 官方命令行工具)
- **前端**：原生 JavaScript (无框架)
- **后端**：Node.js 原生 `http` 模块

## 前置要求

1. **Node.js**：请确保设备已安装 Node.js (v16 或更高版本)。
2. **网络访问（按地区）**：是否需要代理取决于你的网络环境。若你所在地区可直连 Steam 创意工坊，则无需代理；若访问受限，再开启系统代理或配置代理环境变量。
3. **SteamCMD**：程序启动时会自动尝试查找或下载 SteamCMD。如果失败，请检查网络或手动下载 SteamCMD 放入 `steamcmd` 目录。

## 启动方式

1. **下载**本项目代码。
2. **启动服务**：
   ```bash
   node server.js
   ```
3. **访问网页**：在浏览器打开 `http://localhost:3090` (或控制台显示的地址)。

## 高级配置 (可选)

你可以通过设置环境变量来调整工具行为：

| 环境变量 | 说明 | 默认值 |
|----------|-------------|---------|
| `PORT` | 服务端口 | `3090` |
| `HTTP_PROXY` | 代理地址 (如 `http://127.0.0.1:7890`) | 自动读取系统代理 |
| `STEAM_USERNAME` | Steam 账号 (当匿名下载失败时使用) | - |
| `STEAM_PASSWORD` | Steam 密码 | - |
| `STEAM_COUNTRY` | 商店地区代码 | - |
| `STEAM_LANG` | 语言设置 | `schinese` |

> **注意**：虽然本工具主打免登录，但部分壁纸可能强制要求拥有 Wallpaper Engine 或登录账号才能下载。遇到此类情况，你可以尝试配置账号密码（风险自负）。

## 星标历史

[![Star History Chart](https://api.star-history.com/svg?repos=0ran/wallpaper-engine-download-web&type=Date)](https://star-history.com/#0ran/wallpaper-engine-download-web&Date)


## 开发声明

本项目全程依托人工智能辅助完成构建。发布者未审阅、未编写任何一行代码内容；若与其他项目存在代码雷同，均属巧合。仅供学习交流使用。
