---
title: "page-agent 自然語言控制網頁介面的 JS 代理工具"
date: 2026-06-23
source: "https://github.com/alibaba/page-agent"
author: ""
published: ""
category: Resources/Tools
tags:
  - type/clipping
  - status/processed
  - type/resource
summary: "alibaba/page-agent 是純 JavaScript 的網頁內 GUI 代理，用自然語言控制網頁介面，無需瀏覽器擴充套件或 headless browser，基於文字 DOM 操作，支援自帶 LLM 與 MCP Server。"
key_points:
  - "純網頁內 JavaScript，無需瀏覽器擴充、Python 或 headless browser"
  - "基於文字 DOM 操作，不需截圖或多模態 LLM"
  - "支援自帶 LLM（Bring Your Own LLM），可連接任意 AI 服務"
  - "適用場景：SaaS AI Copilot、表單自動化、無障礙訪問、多頁面代理、MCP 整合"
  - "NPM 套件一行安裝，MIT 授權開源"
actionable: "在現有 Web 專案中用 npm install page-agent 整合，測試用自然語言控制表單或工作流程。"
---

# 📎 page-agent 自然語言控制網頁介面的 JS 代理工具

## 摘要

> alibaba/page-agent 是阿里巴巴開源的網頁內 GUI 代理，讓使用者用自然語言控制任何網頁介面。完全在前端 JavaScript 執行，無需安裝瀏覽器擴充套件或 Python 後端，支援自帶 LLM，可整合 MCP Server 讓外部代理控制瀏覽器。

## 重點

- **純前端方案**：只需在網頁引入 JavaScript，所有操作在頁面內完成
- **文字 DOM 操作**：分析頁面 DOM 結構而非截圖，不需多模態 LLM 或特殊權限
- **BYOLLM**：可連接 OpenAI 相容介面（如阿里雲 DashScope），自備 API Key
- **多頁面擴展**：透過 Chrome 擴充套件支援跨頁面任務
- **MCP Server（Beta）**：允許外部代理客戶端（如 Claude Desktop）控制瀏覽器

## 可行動事項

- [ ] 用 `npm install page-agent` 在測試專案中整合，嘗試自然語言填表或操作流程
- [ ] 評估是否適合作為 SaaS 產品的 AI Copilot 層

## 原文整理

- 一行整合（CDN）可直接引入 Demo LLM 試用；NPM 套件適合生產環境
- 使用範例：`await agent.execute('Click the login button')`
- 專案定位：客戶端網頁增強（client-side web enhancement），非伺服器端自動化
- 基於 browser-use 專案的 DOM 處理元件與 Prompt 邏輯，MIT 授權

## 相關筆記

- [[Resources/Tools/2026-05-15 - html-anything Agent HTML 生成工具]]
- [[Resources/Tools/2026-05-22 - Google AI Studio 網頁讀取實測]]

## 來源

- 原文：[alibaba/page-agent on GitHub](https://github.com/alibaba/page-agent)
- 作者：阿里巴巴開源
