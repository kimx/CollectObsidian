---
title: "Alibaba page-agent 網頁自然語言控制工具"
date: 2026-06-23
source: "https://github.com/alibaba/page-agent"
author: ""
published: ""
category: Resources/Tools
tags:
  - type/clipping
  - status/processed
  - type/resource
  - topic/ai-agent
  - topic/javascript
  - topic/tool
summary: "Alibaba 開源的純前端 JavaScript GUI Agent，無需後端或瀏覽器擴充即可用自然語言控制網頁介面，支援 SaaS Copilot 嵌入與 MCP 整合。"
key_points:
  - "純 JavaScript 實作，直接在頁面內執行，不需 browser extension 或 headless browser"
  - "基於 DOM 文字分析，不需截圖或多模態 LLM"
  - "支援自帶 LLM（Bring Your Own LLM），可接 Qwen 等模型"
  - "可選 Chrome Extension 支援跨分頁多步驟任務"
  - "提供 MCP Server（Beta），允許 Agent 客戶端從外部控制瀏覽器"
  - "一行 script 標籤即可整合，或透過 NPM 安裝使用"
actionable: "在一個既有 Web 專案中嵌入 page-agent，測試自然語言填表或點選的基本流程。"
---

# 📎 Alibaba page-agent 網頁自然語言控制工具

## 摘要

> page-agent 是阿里巴巴開源的客戶端 JavaScript GUI Agent。它不需要 Python 後端或瀏覽器擴充，直接在網頁內執行，以 DOM 文字分析替代截圖，讓任何 Web 應用都能透過自然語言控制。適合嵌入 SaaS 產品作為 AI Copilot、或讓表單填寫流程從 20 步縮為一句話。

## 重點

- 一行 `<script>` 即可整合，使用 Demo CDN 或 NPM 安裝均可
- NPM 安裝後 `new PageAgent({ model, baseURL, apiKey })` 初始化，`await agent.execute('...')` 執行任務
- 核心特性：無需截圖、無需多模態 LLM、無需特殊權限
- Chrome Extension 可延伸控制能力至多頁面任務
- MCP Server（Beta）讓外部 Agent 客戶端控制瀏覽器
- 建立在 browser-use（MIT）的 DOM 處理與提示詞基礎之上

## 可行動事項

- [ ] 在測試專案用一行 script 嵌入 page-agent Demo，測試自然語言操作效果。
- [ ] 評估是否適合在 SaaS 產品中替換為自有 LLM API 的正式整合方案。

## 原文整理

- 專案定位：客戶端 Web 增強，非伺服器端自動化
- 使用案例：SaaS AI Copilot、智慧表單填寫（ERP/CRM）、無障礙存取、跨頁面 Agent
- 程式碼由 MIT 授權，歡迎社群貢獻，但純 Bot/AI 生成的 PR 不接受
- Demo CDN 有全球（jsDelivr）與中國（npmmirror）兩個鏡像
- 相關文件：[Docs](https://alibaba.github.io/page-agent/docs/introduction/overview)、[Demo](https://alibaba.github.io/page-agent/)

## 相關筆記

- [[Resources/Tools/2026-05-15 - html-anything Agent HTML 生成工具]]
- [[Resources/AI/2026-05-20 - Microsoft AI Agents 入門 12 課]]

## 來源

- 原文：[alibaba/page-agent: JavaScript in-page GUI agent](https://github.com/alibaba/page-agent)
