# Wallpaper-engine-download-web

> Download all wallpapers for Wallpaper Engine without logging in.

## Project Introduction

This tool is designed to retrieve and download wallpaper data from the Steam Workshop for Wallpaper Engine, with the core advantage of no requirement to log in to a Steam account for wallpaper downloading.

## Core Features

- No Login Required: Download wallpaper resources without logging into a Steam account

- Access Requirement: A network proxy must be enabled before use, otherwise access to the Steam Workshop will be unavailable

## Development Statement

This project was entirely constructed with the assistance of artificial intelligence. The publisher has not reviewed or written any line of code; any similarity with other projects is purely coincidental.

## Prerequisite

Please make sure Node.js is installed on your device before starting the tool; otherwise, the startup will fail.

## Startup Method

```bash
node server.js
```

## Download & Packaging Rules

- Scene/UI/Program-based wallpapers: Automatically packaged into .zip compressed files after download, requiring unzipping for access;

- Video-based wallpapers: Only the original video files are downloaded without compression or packaging, and can be played directly after download.

---

# Wallpaper Engine 创意工坊下载工具

## 项目简介

本工具用于获取并下载 Steam 创意工坊中 Wallpaper Engine 的壁纸数据，核心优势为无需登录 Steam 账号即可完成壁纸下载。

## 核心特点

- 免登录下载：无需登录 Steam 账号即可下载壁纸资源

- 访问要求：使用前必须开启网络代理，否则无法访问 Steam 创意工坊

## 开发声明

本项目全程依托人工智能辅助完成构建，发布者未审阅、未编写任何一行代码内容；若与其他项目存在代码雷同，均属巧合。

## 前置要求

启动工具前，请确保你的设备已安装 Node.js，否则将无法正常启动。

## 启动方式

node server.js

## 下载与打包规则

- 场景类 / 页面类 / 程序类壁纸：下载后自动打包为 .zip 压缩文件，需解压后访问；

- 视频类壁纸：仅下载原始视频文件，无压缩打包流程，下载后可直接播放。