<div align="center">

# 星狐Claw - 一键部署 OpenClaw

**零门槛部署 AI 智能体，让 AI 接入 Telegram、飞书、钉钉、Discord 等平台**

[![Release](https://img.shields.io/github/v/release/FoxProAI/xinghuclaw-releases?style=flat-square&label=%E6%9C%80%E6%96%B0%E7%89%88%E6%9C%AC)](https://github.com/FoxProAI/xinghuclaw-releases/releases/latest)
[![Platform](https://img.shields.io/badge/%E5%B9%B3%E5%8F%B0-Windows%20%7C%20macOS-blue?style=flat-square)](https://xinghuclaw.com)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

[官网下载](https://xinghuclaw.com) · [联系反馈](https://work.weixin.qq.com/ca/cawcde410affdc992a)

</div>

---

## 什么是星狐Claw？

星狐Claw 是一款**一键部署 OpenClaw 的桌面管理工具**。OpenClaw 是开源的 AI 网关编排平台，可以将 Claude、GPT、Gemini 等大模型接入 Telegram、飞书、钉钉、Discord 等消息平台。

传统部署 OpenClaw 需要手动安装 Node.js、Git、配置环境变量、运行命令行……**星狐Claw 帮你把这一切简化为：下载 → 双击 → 填写配置 → 完成。**

> 🕐 传统部署：60+ 分钟 → 星狐Claw：1 分钟

---

## 核心功能

### 🚀 一键部署
- 自动检测并安装 Node.js、Git 等依赖
- 自动安装 OpenClaw CLI
- 全程图形化操作，无需命令行

### 🤖 多模型支持

| Anthropic (Claude) | OpenAI (GPT) | Google (Gemini) |
|---|---|---|
| Claude Opus 4.6 | GPT-5.4 | Gemini 3.0 Flash |
| Claude Sonnet 4.6 | GPT-5.3 Codex | Gemini 3.1 Flash |
| Claude Haiku 4.5 | | Gemini 3.0 Pro |
| + Thinking 变体 | | Gemini 3.1 Pro |

### 💬 多渠道接入

| 渠道 | 说明 |
|---|---|
| **Telegram** | Bot Token 接入 |
| **飞书** | App ID + App Secret |
| **钉钉** | App Key + App Secret |
| **Discord** | Bot Token 接入 |
| **API** | WebSocket / CLI 直连 |

### 📊 图形化管理面板
- 实例创建向导（分步引导）
- 实例启动 / 停止 / 删除
- 实时日志查看
- 运行状态监控
- 版本检测与一键更新

---

## 快速开始

### 1. 下载

| 平台 | 下载 |
|---|---|
| **Windows 11** | [openclaw-manager-win11.exe](https://dl.xinghuclaw.com/openclaw-manager-win11.exe) |
| **macOS** | [OpenClaw-Manager-v2.pkg](https://dl.xinghuclaw.com/OpenClaw-Manager-v2.pkg) |

或前往 [GitHub Releases](https://github.com/FoxProAI/xinghuclaw-releases/releases/latest) 下载。

### 2. 运行

- **Windows**：双击 `.exe` 文件，程序将在系统托盘运行，自动打开浏览器管理面板
- **macOS**：安装 `.pkg` 后从应用程序启动

### 3. 创建实例

1. 点击「新建实例」
2. 输入实例名称
3. 选择 AI 模型（Claude / GPT / Gemini）
4. 填写 API Key
5. 选择消息渠道（Telegram / 飞书等）
6. 完成配对 → 开始使用！

---

## 系统要求

| 项目 | 要求 |
|---|---|
| 操作系统 | Windows 11 / macOS 12+ |
| 磁盘空间 | ≥ 200 MB |
| 网络 | 需要互联网连接 |
| 其他 | 无需预装 Node.js / Git（自动安装） |

---

## 技术架构

```
星狐Claw Manager (.exe / .pkg)
├── HTTP Server (localhost:51942)
├── React SPA 管理面板
├── 系统托盘图标
└── OpenClaw Gateway 子进程
    └── Node.js → AI 模型 API
        ├── Claude API
        ├── OpenAI API
        └── Gemini API
```

- **后端**：Go（单文件分发，嵌入前端资源）
- **前端**：React + TypeScript（中英文国际化）
- **自更新**：基于 GitHub Releases + CDN 加速

---

## 相关链接

- 🌐 官网：[xinghuclaw.com](https://xinghuclaw.com)
- 📦 下载：[GitHub Releases](https://github.com/FoxProAI/xinghuclaw-releases/releases)
- 💬 反馈：[联系我们](https://work.weixin.qq.com/ca/cawcde410affdc992a)
- 🦞 OpenClaw：[openclaw.com](https://openclaw.com)

---

## License

MIT License - 详见 [LICENSE](LICENSE)
