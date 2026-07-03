---
title: "alibaba page-agent 網頁自然語言控制工具"
date: 2026-06-23
source: "https://github.com/alibaba/page-agent"
author: ""
published: ""
category: Resources/Tools
tags:
  - type/clipping
  - status/processed
  - type/resource
summary: "alibaba 開源的純前端 JavaScript GUI Agent，無需截圖或多模態模型，僅用文字 DOM 操作即可以自然語言控制任意網頁介面。"
key_points:
  - "純前端方案：無需瀏覽器擴充套件、Python 或無頭瀏覽器，只需一個 script 標籤"
  - "基於文字 DOM 操作，不依賴截圖或多模態 LLM，效率更高"
  - "支援自帶 LLM，相容 qwen、openai 等多種 API"
  - "用途涵蓋 SaaS AI Copilot、智能表單填寫、無障礙存取、多頁面 Agent"
  - "提供 Chrome 擴充套件與 MCP Server（Beta）支援跨頁面與外部控制"
  - "MIT 授權開源，NPM 安裝一行搞定"
actionable: "在現有 Web 專案中加入 page-agent script 標籤，測試以自然語言完成一個常見操作流程。"
---

# 📎 alibaba page-agent 網頁自然語言控制工具

## 摘要

> alibaba 開源的 page-agent 是一個純前端 JavaScript GUI Agent，讓你用自然語言控制任意網頁介面。不需要截圖、多模態 LLM 或特殊權限，所有操作都在網頁內的 JavaScript 中完成，整合成本極低。

## 重點

- 一行 script 標籤即可整合，提供免費測試 LLM API 供技術評估使用
- DOM 文字處理不依賴截圖，效能與成本優於多模態方案
- 支援帶入自己的 LLM，設定 baseURL 與 apiKey 即可
- Chrome 擴充套件支援跨標籤頁的多頁面任務
- MCP Server（Beta）可讓外部 Agent 控制瀏覽器
- 底層參考 browser-use 的 DOM 處理組件，MIT 授權

## 可行動事項

- [ ] 用 NPM 安裝 `page-agent` 或使用 CDN 方式，在一個內部工具頁面中測試自然語言表單填寫場景。

## 原文整理

- 設計定位為客戶端網頁增強（client-side web enhancement），非伺服器端自動化
- 主要使用場景：為 SaaS 產品快速加入 AI Copilot、簡化 ERP/CRM 複雜操作、提升無障礙存取
- 安裝方式：全域 CDN（有 Global 和 China 鏡像）或 `npm install page-agent`
- 社群貢獻項目歡迎提 PR，但純 AI/Bot 生成的貢獻不會被接受

## 相關筆記

- [[Resources/Tools/2026-05-15 - html-anything Agent HTML 生成工具]]
- [[Resources/AI/2026-05-20 - Microsoft Agent Framework 與 Skill 解耦]]

## 來源

- 原文：[alibaba/page-agent: JavaScript in-page GUI agent](https://github.com/alibaba/page-agent)
- 作者：alibaba
