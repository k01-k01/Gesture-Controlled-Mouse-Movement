# 🍕 LazyEat

<div align="center">
  
![GitHub stars](https://img.shields.io/github/stars/maplelost/lazyeat)
![GitHub forks](https://img.shields.io/github/forks/maplelost/lazyeat?style=flat)
![Platform](https://img.shields.io/badge/platform-windows%20%7C%20macos-lightgrey)

</div>

<h3 align="center">
  <img src="public/lazyeat.png" width="150" height="150" alt="LazyEat logo" />
</h3>

> 在吃饭时看剧/刷网页，不想让油腻的手接触设备？

**LazyEat** 是一个免触控操作工具，让你在吃饭时也能轻松控制视频播放和网页浏览，只需对着摄像头比划手势即可实现暂停视频、全屏、切换视频等功能！



## 🌟 特性

- 🖐️ 单指滑动控制光标
- ✌️ 双指/Rock 执行鼠标单击
- 👌 OK 手势控制页面滚动
- 🤏 四指并拢发送按键
- 🎤 支持语音输入
- 🚀 跨平台支持 (Windows & macOS)

![demo.gif](.readme/demo.gif)

## 📸 截图


<div align="center">
<img src=".readme/img.png" width="800" height="600" />
</div>

## 🚀 快速开始

### 系统要求

```
Python 3.11.x
Rust 1.85.1+
Node.js v22.14.0+
```

> ⚠️ 注意：Python 3.12.7 及以上版本目前打包会失败

### 安装依赖

1. 安装 [Rust](https://www.rust-lang.org/zh-CN/tools/install) 和 [Node.js](https://nodejs.org/zh-cn/)

2. 在项目根目录执行安装命令：
```bash
npm run install-reqs
```

3. 构建 Tauri 图标：
```bash
npm run build:icons
```

### 语音识别模型

下载 [Vosk 中文语音识别小模型](https://alphacephei.com/vosk/models/vosk-model-small-cn-0.22.zip) 并解压到 `model/` 文件夹下。

### 开发环境运行

```bash
npm run tauri dev
```

### 打包应用

1. 使用 PyInstaller 打包 Python 后端：
```bash
# Windows
npm run build:py

# macOS
# npm run build:py-mac

# Linux
# npm run build:py-linux
```

2. 打包成生产环境应用：
```bash
npm run tauri build
```

打包后的可执行文件位于 `src-tauri/target/release` 目录下。

## 📦 技术栈

- **前端**: Vue 3 + TypeScript + Vite + Element Plus
- **后端**: Python + FastAPI + Vosk + OpenCV
- **桌面框架**: Tauri 2.x
- **手势识别**: MediaPipe Tasks Vision
- **通信**: WebSocket

## 📢 语音识别模型替换

- [小模型 (推荐)](https://alphacephei.com/vosk/models/vosk-model-small-cn-0.22.zip) - 适用于一般场景
- [大模型](https://alphacephei.com/vosk/models/vosk-model-cn-0.22.zip) - 识别准确率更高

将下载的大模型解压并替换 `model/` 目录下的内容即可。

## 📝 TODO

- [ ] (2025 年 3 月 12 日) 嵌入 browser-use ，语音控制浏览器
- [ ] (2025 年 3 月 24 日) 开发安卓版本

