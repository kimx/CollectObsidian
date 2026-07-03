---
title: "dotnet-testing Agent Orchestration v2.0.0 使用指南"
date: 2026-05-31
source: "https://dotblogs.com.tw/mrkt/2026/05/28/182946"
author: "[[mrkt的程式學習筆記]]"
published: "2026-05-28"
category: Resources/Tools
tags:
  - type/clipping
  - status/processed
  - type/resource
summary: "完整說明如何在 .NET 專案中導入 dotnet-testing Agent Orchestration v2.0.0，涵蓋 mcp-local-rag 安裝、Agent 定義檔設置及四個 Orchestrator 的使用方式。"
key_points:
  - "v2.0.0 引入 mcp-local-rag 做本地語意技能索引，Skill 不再直接放入專案目錄"
  - "安裝分四步：clone skills、設定 mcp-local-rag、安裝 Agent 定義檔、設定 VS Code"
  - "共 20 個 Agent 定義檔，分 Unit Test、Integration、Aspire、TUnit 四組 Orchestrator，可按需選裝"
  - "JSON 交接機制與 Phase Timing 提升可觀測性，方便診斷各階段問題"
  - "索引建好後多專案共用，第二個專案只需重複 Step 3 與 Step 4"
actionable: "挑一個依賴少的 Service，完成 v2.0.0 四步驟安裝並跑一次完整 Unit Test workflow 驗收效果。"
---

# 📎 dotnet-testing Agent Orchestration v2.0.0 使用指南

## 摘要

> 本篇為系列第 10 篇，聚焦在「怎麼裝、怎麼用」。v2.0.0 最大的架構變化是引入 `mcp-local-rag`，Skills 改為本地語意索引查詢而非直接讀取。文章從環境需求、四大安裝步驟到各 Orchestrator 操作，提供完整的上手流程。

## 重點

- v2.0.0 引入 `mcp-local-rag` 做本地向量索引，Subagent 透過 MCP 查詢 Skill，延遲更低
- 安裝分四步：clone `dotnet-testing-agent-skills`、安裝並設定 mcp-local-rag、安裝 20 個 Agent 定義檔、啟用 VS Code Subagent 設定
- 四組 Orchestrator（Unit Test、Integration、Aspire、TUnit）可按需選裝，只需 Unit Test 功能裝 5 個就夠
- 每次 workflow 除產生測試程式碼，還會輸出 JSON 交接檔與 timing log，方便診斷
- 從 v1.0.0 升級需閱讀 `docs/v2_0_0/V1_TO_V2_MIGRATION_GUIDE.md`

## 可行動事項

- [ ] clone `dotnet-testing-agent-skills`，完成 mcp-local-rag 安裝與索引建立（Step 1–2）
- [ ] 安裝 Unit Test 的 5 個 Agent 定義檔，啟用 `chat.customAgentInSubagent.enabled`（Step 3–4）
- [ ] 挑一個簡單 Service 跑完整 Unit Test workflow，確認四個階段正常產出

## 原文整理

- **環境需求**：VS Code 1.118+、Copilot Chat、Node.js 18+、Python、.NET SDK 8/9/10；Integration/Aspire 測試另需 Docker Desktop
- **Step 1**：clone `dotnet-testing-agent-skills` 到固定位置，記住 `.github/skills` 路徑
- **Step 2**：`npm install -g mcp-local-rag`，設定 `.vscode/mcp.json`（`BASE_DIR` 指向 skills 路徑），建立並驗證索引
- **Step 3**：從 orchestration repo 複製 `.github/agents/*.agent.md` 與 `.github/skills/dotnet-test/`
- **Step 4**：VS Code 設定 `chat.customAgentInSubagent.enabled: true`；除錯時設 `chat.thinking.style: Detailed`
- **使用**：Agent Mode → 選擇 Orchestrator → 輸入需求 → 自動執行 Analyzer、Writer、Executor、Reviewer 四階段

## 相關筆記

- [[Resources/Tools/2026-05-27 - CodeGraph 降低 AI 寫程式 Token 消耗]]
- [[Resources/AI/2026-05-20 - Microsoft Agent Framework 與 Skill 解耦]]

## 來源

- 原文：[使用指南 — 在你的專案中導入 dotnet-testing Agent Orchestration（v2.0.0）](https://dotblogs.com.tw/mrkt/2026/05/28/182946)
- 作者：[[mrkt的程式學習筆記]]
- GitHub：[dotnet-testing-agent-orchestration](https://github.com/kevintsengtw/dotnet-testing-agent-orchestration)
