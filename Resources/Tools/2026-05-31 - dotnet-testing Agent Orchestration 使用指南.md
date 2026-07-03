---
title: "dotnet-testing Agent Orchestration 使用指南"
date: 2026-05-31
source: "https://dotblogs.com.tw/mrkt/2026/05/28/182946"
author: "[[mrkt的程式學習筆記]]"
published: ""
category: Resources/Tools
tags:
  - type/clipping
  - status/processed
  - type/resource
  - topic/dotnet
  - topic/ai-agent
  - topic/testing
summary: "dotnet-testing Agent Orchestration v2.0.0 的完整安裝指南，核心變更是引入 mcp-local-rag 建立本地語意索引取代直接讀取 Skill 檔案，需要 VS Code 1.118+。"
key_points:
  - "v2.0.0 最大變更：引入 mcp-local-rag，Skills 改以本地語意索引查詢，非逐個讀取"
  - "安裝四步驟：clone dotnet-testing-agent-skills → 設定 mcp-local-rag → 設定 Agent → 驗證"
  - "需要 VS Code 1.118+（Custom Agents 支援）、Node.js 18+、Python"
  - "mcp-local-rag 完全本機運行，不需外部 API 或 Docker"
  - ".vscode/mcp.json 設定 BASE_DIR 指向本機 skills 目錄，多專案可共用同一份"
  - "索引建立有線上（自動下載 embedding model）與離線兩種模式"
actionable: "按四步驟在一個 .NET 專案中完成 v2.0.0 安裝，測試 Subagent 透過 MCP 查詢 Skill 的效果。"
---

# 📎 dotnet-testing Agent Orchestration 使用指南

## 摘要

> 本文是 dotnet-testing Agent Orchestration v2.0.0 的完整安裝指南（系列第 10 篇）。相較於 v1.0.0，最大差異是引入 `mcp-local-rag`——Skills 不再直接放進專案目錄，而是 clone 一份技能庫到本機，建立本地語意索引後由各 Subagent 透過 MCP 查詢，提升效率並支援多專案共用。

## 重點

- v2.0.0 移除了 v1.0.0 的 16 個 Custom Prompts，使用入口統一到 Agent
- Skills 存放在獨立的 `dotnet-testing-agent-skills` 倉庫，clone 到本機後由 mcp-local-rag 建索引
- `mcp-local-rag` 是本地端語意搜尋 MCP server，完全離線、無需 Docker
- `.vscode/mcp.json` 需設定 `BASE_DIR`（技能路徑）、`DB_PATH`（向量索引）、`CACHE_DIR`
- `RAG_HYBRID_WEIGHT: 0.7` 控制語意搜尋與關鍵字的混合比例

## 可行動事項

- [ ] 確認 VS Code 版本 ≥ 1.118，安裝 GitHub Copilot Chat。
- [ ] Clone `dotnet-testing-agent-skills` 到本機統一目錄（多專案可共用）。
- [ ] 安裝 `mcp-local-rag`（`npm install -g mcp-local-rag`）並建立索引。
- [ ] 在專案建立 `.vscode/mcp.json`，設定正確的 `BASE_DIR` 路徑。

## 原文整理

- 環境需求：VS Code 1.118+、Copilot Chat、Node.js 18+、Python、.NET SDK 8/9/10
- 選用需求：Docker Desktop（Integration/Aspire 測試）、dotnet Aspire workload
- Step 1：`git clone https://github.com/kevintsengtw/dotnet-testing-agent-skills.git`
- Step 2：設定 mcp-local-rag——安裝套件、設定 `.vscode/mcp.json`、建立索引（線上或離線模式）
- 索引建立線上模式：執行 `mcp-local-rag-index-skills-online.ps1`（Windows）或對應腳本
- `DB_PATH` 使用 `${workspaceFolder}` 指向目前專案，讓向量索引隔離在各專案內

## 相關筆記

- [[Resources/AI/2026-05-20 - Microsoft AI Agents 入門 12 課]]
- [[Resources/AI/2026-05-20 - Microsoft Agent Framework 與 Skill 解耦]]

## 來源

- 原文：[使用指南 — 在你的專案中導入 dotnet-testing Agent Orchestration（v2.0.0）](https://dotblogs.com.tw/mrkt/2026/05/28/182946)
- 作者：[[mrkt的程式學習筆記]]
