---
title: "dotnet-testing Agent Orchestration v2.0.0 使用指南"
date: 2026-05-31
source: "https://dotblogs.com.tw/mrkt/2026/05/28/182946"
author: "[[mrkt的程式學習筆記]]"
published: ""
category: Resources/Tools
tags:
  - type/clipping
  - status/processed
  - type/resource
summary: "說明如何在 .NET 專案中導入 dotnet-testing Agent Orchestration v2.0.0，涵蓋 mcp-local-rag 本地語意索引安裝、Agent 定義檔設定與啟用流程。"
key_points:
  - "v2.0.0 引入 mcp-local-rag，Skills 改為本地語意索引查詢，而非逐個讀取 SKILL.md"
  - "安裝分四步：clone skills repo、設定 mcp-local-rag、安裝 Agent 定義檔、啟用 Agent"
  - "共 20 個 Agent 定義檔，分屬 4 個 Orchestrator（每組 1+4 架構）"
  - "VS Code 最低需求 1.118+，Node.js 18+，Python 已安裝"
  - "mcp.json 中設定 BASE_DIR、DB_PATH、CACHE_DIR、RAG_HYBRID_WEIGHT 等環境變數"
  - "索引支援線上（自動下載 embedding model）與離線（預建 zip）兩種建立方式"
actionable: "在現有 .NET 專案中依四步驟完成 v2.0.0 安裝，並執行一次索引驗證確認 mcp-local-rag 可正常查詢。"
---

# 📎 dotnet-testing Agent Orchestration v2.0.0 使用指南

## 摘要

> 本文為系列第 10 篇，說明 dotnet-testing Agent Orchestration v2.0.0 的完整安裝流程。與 v1.0.0 最大差異在於引入 mcp-local-rag 本地語意索引，Subagent 改以 MCP 查詢方式取得相關 Skill，安裝步驟因此增加了 mcp-local-rag 的設定環節。

## 重點

- 安裝四步驟：clone `dotnet-testing-agent-skills` → 設定 mcp-local-rag → 安裝 Agent 定義檔 → 啟用
- `mcp.json` 中 `BASE_DIR` 指向本機 skills 目錄，多個專案可共用同一份
- 索引建立使用 PowerShell script 或 Python script，支援增量更新與完整重建
- v2.0.0 移除了 v1.0.0 的 16 個 Custom Prompts，使用入口統一到 Agent
- 4 個 Orchestrator 分別對應不同 .NET 測試領域，每組架構為 1 Orchestrator + 4 Subagent

## 可行動事項

- [ ] 在 .NET 測試專案中按四步驟完成安裝，執行 `mcp-local-rag-verify-skills-index` 驗證索引，再觸發一次 Agent 確認可正常查詢 Skills。

## 原文整理

- 系列說明 AI 自動建立 .NET 測試的完整方案，本篇聚焦實際安裝操作
- mcp-local-rag 為本地端語意搜尋 MCP server，完全離線運行，無需外部 API 或 Docker
- 環境變數 `RAG_HYBRID_WEIGHT: 0.7` 控制語意搜尋與關鍵字加權比例
- 詳細排查文件集中在 orchestration repo 的 `docs/mcp_local_rag/` 目錄

## 相關筆記

- [[Resources/AI/2026-05-20 - Microsoft Agent Framework 與 Skill 解耦]]
- [[Resources/Tools/2026-05-23 - Docker 從入門到實踐]]

## 來源

- 原文：[使用指南 — 在你的專案中導入 dotnet-testing Agent Orchestration（v2.0.0）](https://dotblogs.com.tw/mrkt/2026/05/28/182946)
- 作者：[[mrkt的程式學習筆記]]
