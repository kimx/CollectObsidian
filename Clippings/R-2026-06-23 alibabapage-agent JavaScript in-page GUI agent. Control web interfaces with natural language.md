---
title: "alibaba/page-agent: JavaScript in-page GUI agent. Control web interfaces with natural language."
source: "https://github.com/alibaba/page-agent"
author:
created: 2026-06-23
description: "JavaScript in-page GUI agent. Control web interfaces with natural language. - alibaba/page-agent"
tags:
  - "clippings"
---
## Page Agent

![Page Agent Banner](https://camo.githubusercontent.com/79058d74ca2396ef43f2bdb2fd2c90024a3dc22ed53c202c975e84d63fb6ce8b/68747470733a2f2f696d672e616c6963646e2e636f6d2f696d6765787472612f69312f4f31434e30314e434d4b586a31476e34746b46547378665f2121363030303030303030303636362d322d7470732d313238302d3235362e706e67)

The GUI Agent Living in Your Webpage. Control web interfaces with natural language.

🌐 **English** | [中文](https://github.com/alibaba/page-agent/blob/main/docs/README-zh.md)

[**🚀 Demo**](https://alibaba.github.io/page-agent/) | [**📖 Docs**](https://alibaba.github.io/page-agent/docs/introduction/overview) | [**📢 HN Discussion**](https://news.ycombinator.com/item?id=47264138) | [**𝕏 Follow on X**](https://x.com/simonluvramen)

page-agent-demo-0227.mp4<video src="https://private-user-images.githubusercontent.com/10131203/559172930-a1f2eae2-13fb-4aae-98cf-a3fc1620a6c2.mp4?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3ODIxOTY4MDIsIm5iZiI6MTc4MjE5NjUwMiwicGF0aCI6Ii8xMDEzMTIwMy81NTkxNzI5MzAtYTFmMmVhZTItMTNmYi00YWFlLTk4Y2YtYTNmYzE2MjBhNmMyLm1wND9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNjA2MjMlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjYwNjIzVDA2MzUwMlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTk4MTM0N2Y2NzJmMjBiMGNkOTIzNmZmN2UzMzMyYzBmMzI2YzRkMjA1ZDAyMzQ4N2VjMWEzY2UwMzUzNTdlYmYmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JnJlc3BvbnNlLWNvbnRlbnQtdHlwZT12aWRlbyUyRm1wNCJ9.NoOo67WeX-El6afIw2bbJf00IsPevr_xBiW0-gLS8aM" controls="controls"></video>

---

## ✨ Features

- **🎯 Easy integration**
	- No need for `browser extension` / `python` / `headless browser`.
		- Just in-page javascript. Everything happens in your web page.
- **📖 Text-based DOM manipulation**
	- No screenshots. No multi-modal LLMs or special permissions needed.
- **🧠 Bring your own LLMs**
- **🐙 Optional [chrome extension](https://alibaba.github.io/page-agent/docs/features/chrome-extension) for multi-page tasks.**
	- And an [MCP Server (Beta)](https://alibaba.github.io/page-agent/docs/features/mcp-server) to control it from outside

## 💡 Use Cases

- **SaaS AI Copilot** — Ship an AI copilot in your product in lines of code. No backend rewrite.
- **Smart Form Filling** — Turn 20-click workflows into one sentence. Perfect for ERP, CRM, and admin systems.
- **Accessibility** — Make any web app accessible through natural language. Voice commands, screen readers, zero barrier.
- **Multi-page Agent** — Extend your own web agent's reach across browser tabs [chrome extension](https://alibaba.github.io/page-agent/docs/features/chrome-extension).
- **MCP** - Allow your agent clients to control your browser.

## 🚀 Quick Start

### One-line integration

Fastest way to try PageAgent with our free Demo LLM:

```
<script src="{URL}" crossorigin="true"></script>
```

> **⚠️**
> 
> **For technical evaluation only.** This demo CDN uses our free [testing LLM API](https://alibaba.github.io/page-agent/docs/features/models#free-testing-api). By using it, you agree to its [terms](https://github.com/alibaba/page-agent/blob/main/docs/terms-and-privacy.md).

| Mirrors | URL |
| --- | --- |
| Global | [https://cdn.jsdelivr.net/npm/page-agent@1.10.0/dist/iife/page-agent.demo.js](https://cdn.jsdelivr.net/npm/page-agent@1.10.0/dist/iife/page-agent.demo.js) |
| China | [https://registry.npmmirror.com/page-agent/1.10.0/files/dist/iife/page-agent.demo.js](https://registry.npmmirror.com/page-agent/1.10.0/files/dist/iife/page-agent.demo.js) |

Add `?autoInit=false` to load the script without creating the demo agent automatically. You can then instantiate it with `new window.PageAgent(...)`.

### NPM Installation

```
npm install page-agent
```
```
import { PageAgent } from 'page-agent'

const agent = new PageAgent({
    model: 'qwen3.5-plus',
    baseURL: 'https://dashscope.aliyuncs.com/compatible-mode/v1',
    apiKey: 'YOUR_API_KEY',
    language: 'en-US',
})

await agent.execute('Click the login button')
```

For more programmatic usage, see [📖 Documentations](https://alibaba.github.io/page-agent/docs/introduction/overview).

## 🌟 Awesome Page Agent

Built something cool with PageAgent? Add it here! Open a PR to share your project.

> These are community projects — not maintained or endorsed by us. Use at your own discretion.

| Project | Description |
| --- | --- |
| *Yours?* | [Open a PR](https://github.com/alibaba/page-agent/pulls) 🙌 |

## 🤝 Contributing

We welcome contributions from the community! See [CONTRIBUTING.md](https://github.com/alibaba/page-agent/blob/main/CONTRIBUTING.md) for guidelines and [docs/developer-guide.md](https://github.com/alibaba/page-agent/blob/main/docs/developer-guide.md) for local development workflows.

Please read the [maintainer's note](https://github.com/alibaba/page-agent/issues/349) on principles and current state.

Contributions generated entirely by **bots or AI** without substantial human involvement will **not be accepted**.

## ⚖️ License

[MIT License](https://github.com/alibaba/page-agent/blob/main/LICENSE)

## 👏 Acknowledgments

This project builds upon the excellent work of **[`browser-use`](https://github.com/browser-use/browser-use)**.

`PageAgent` is designed for **client-side web enhancement**, not server-side automation.

```
DOM processing components and prompt are derived from browser-use:

Browser Use <https://github.com/browser-use/browser-use>
Copyright (c) 2024 Gregor Zunic
Licensed under the MIT License

We gratefully acknowledge the browser-use project and its contributors for their
excellent work on web automation and DOM interaction patterns that helped make
this project possible.
```

---

**⭐ Star this repo if you find PageAgent helpful!**