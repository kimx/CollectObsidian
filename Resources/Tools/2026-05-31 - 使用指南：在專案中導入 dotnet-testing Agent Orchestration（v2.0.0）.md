---
title: "使用指南：在專案中導入 dotnet-testing Agent Orchestration（v2.0.0）"
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
  - topic/testing
  - topic/ai-agent
summary: "這篇是 dotnet-testing Agent Orchestration v2.0.0 的導入實作指南，重點在 mcp-local-rag 安裝、索引建立、Agent 安裝與疑難排解。"
key_points:
  - "v2.0.0 相較 v1.0.0 的核心差異是導入 mcp-local-rag，Skills 由本地語意索引查詢而非直接讀取檔案"
  - "完整導入流程包含：clone skills、安裝與設定 mcp-local-rag、安裝 Agent 定義檔、確認 VS Code Subagent 設定"
  - "Unit/Integration/Aspire/TUnit 四種 Orchestrator 的使用門檻與執行時間不同，需依測試場景選擇"
  - "執行後會產生 .orchestrator JSON 交接檔與 timing log，可用於診斷與優化流程"
  - "常見問題可從 Agent 檔案位置、VS Code 版本、mcp 設定與索引狀態四個面向優先排查"
actionable: "先在一個 .NET 專案完成最小導入（Step 1~5），並用單一 Service 驗證一次 workflow，再視需求導入進階 Orchestrator。"
---

# 📎 使用指南：在專案中導入 dotnet-testing Agent Orchestration（v2.0.0）

## 摘要

> 文章以實作角度說明如何在 .NET 專案導入 dotnet-testing Agent Orchestration v2.0.0。流程從準備 skills、設定 mcp-local-rag，到安裝 Agent 與實際執行測試生成，並補充常見錯誤排除與最佳實踐。

## 重點

- v2.0.0 導入 `mcp-local-rag` 後，Skills 讀取方式改為「本地語意索引 + 查詢」，提升載入效率與可維護性。
- 導入順序建議固定為：環境檢查 → skills clone → mcp-local-rag 安裝與索引 → Agent 檔案安裝 → VS Code 設定。
- Orchestrator 採 1+4 分工（Orchestrator + Analyzer/Writer/Executor/Reviewer），子代理由主代理自動調度。
- 四種 Orchestrator（Unit/Integration/Aspire/TUnit）在 Docker 與環境依賴上不同，應按目標測試類型選用。
- 失敗排查時優先看 `.orchestrator/{TargetName}/` 與 `orchestrator-timing.log`，可快速定位階段性問題。

## 可行動事項

- [ ] 在現有專案建立 `.vscode/mcp.json`，完成 mcp-local-rag 索引建立與驗證。
- [ ] 安裝 Unit Test Orchestrator（最小 5 個 Agent）並對一個 Service 試跑。
- [ ] 將本次導入步驟整理成團隊內部 SOP，統一測試生成流程。

## 原文整理

- 文章先定義 v2.0.0 所需環境（VS Code、Node.js、Python、.NET SDK 與部分場景的 Docker/Aspire workload）。
- 與 v1.0.0 最大差異是 Step 2：需先建立 mcp-local-rag 本地索引，讓 Subagent 能查詢 Skills。
- Step 3 安裝 `.github/agents`、`.github/skills` 與 `copilot-instructions.md`；並強調只有 Orchestrator 會出現在 Agent 選單。
- Step 4 需啟用 `chat.customAgentInSubagent.enabled`，否則流程可能停在 Analyzer 階段。
- Step 5/6 說明 Unit 與進階 Orchestrator 實際用法、時間成本與典型輸出。
- 文末整理 NuGet 套件建議、模型選擇、疑難排解與最佳實踐，適合作為導入檢核清單。

## 相關筆記

- [[Resources/Tools/2026-05-27 - CodeGraph 降低 AI 寫程式 Token 消耗]]
- [[Resources/AI/2026-05-20 - Microsoft AI Agents 入門 12 課]]

## 來源

- 原文：[使用指南 — 在你的專案中導入 dotnet-testing Agent Orchestration（v2.0.0）](https://dotblogs.com.tw/mrkt/2026/05/28/182946)
- 作者：[[mrkt的程式學習筆記]]
