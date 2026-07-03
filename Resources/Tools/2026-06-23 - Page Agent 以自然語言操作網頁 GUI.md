---
title: "Page Agent 以自然語言操作網頁 GUI"
date: 2026-06-23
source: "https://github.com/alibaba/page-agent"
author:
  - "[[alibaba]]"
published: ""
category: Resources/Tools
tags:
  - type/clipping
  - status/processed
  - type/resource
summary: "Page Agent 是可嵌入網頁前端的 JavaScript GUI Agent，可用自然語言操作 DOM 與多頁工作流。"
key_points:
  - "主打純前端整合，不需額外瀏覽器自動化框架即可在頁內執行操作。"
  - "以文字式 DOM 操作為核心，降低對多模態模型與截圖流程的依賴。"
  - "支援自帶 LLM、Chrome extension 與 MCP Server 等擴充路徑。"
  - "提供 CDN 一行接入與 npm 套件兩種導入方式。"
actionable: "在一個內部表單頁面試作 Page Agent，評估自然語言操作是否能縮短重複點擊流程。"
---

# 📎 Page Agent 以自然語言操作網頁 GUI

## 摘要

> Page Agent 提供「在頁面內直接運作」的 GUI Agent 實作方式，目標是把自然語言操作能力嵌入既有 Web 介面。它兼顧快速接入與可擴充部署，適合用於 SaaS Copilot、表單自動化與無障礙操作場景。

## 重點

- 在既有網頁加載腳本即可啟用，降低導入門檻。
- DOM 為主要互動媒介，避免依賴截圖推理流程。
- 可自選模型與 API 端點，便於企業環境接入。
- 另有 Chrome extension/MCP Server 供跨頁任務與外部控制。

## 可行動事項

- [ ] 先以 CDN Demo 模式在測試站驗證 2–3 個實際操作任務，再評估改用自有模型部署。

## 原文整理

- 專案定位為「活在網頁裡的 GUI Agent」，強調低侵入整合。
- 文件展示快速上手、npm 整合與可選功能（extension、MCP）。
- 使用情境涵蓋 SaaS Copilot、智慧表單填寫、無障礙互動。
- 授權為 MIT，並註明部分 DOM 與提示流程承襲 browser-use 概念。

## 相關筆記

- [[Resources/Tools/2026-05-27 - CodeGraph 降低 AI 寫程式 Token 消耗]]
- [[Resources/AI/2026-05-20 - Microsoft Agent Framework 與 Skill 解耦]]

## 來源

- 原文：[alibaba/page-agent](https://github.com/alibaba/page-agent)
- 作者：[[alibaba]]
