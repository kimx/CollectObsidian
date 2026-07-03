---
title: 知識庫首頁
date: 2026-05-06
tags:
  - MOC
  - index
---

# 知識庫首頁

> 目前只保留 AI、Clippings、Resources、Templates 四個工作區。

## 收集

- [[Clippings/README|Clippings — 原始收集區]]

```dataview
TABLE source, summary, date
FROM "Clippings"
WHERE file.name != "README"
SORT date DESC
```

## 最近整理


- [[Resources/Tools/2026-06-16 - Ponytail 讓 AI 少寫程式碼的決策工具]]
- [[Resources/Tools/2026-05-31 - dotnet-testing Agent Orchestration v2.0.0 使用指南]]
- [[Resources/Tools/2026-05-31 - 使用指南：在專案中導入 dotnet-testing Agent Orchestration（v2.0.0）]]
- [[Resources/Tools/2026-05-30 - Obsidian Digital Garden 建站插件]]
- [[Resources/AI/2026-05-29 - 一人公司、零員工、AI Agents：2 個月談下超過 400 萬台幣開發合約]]
- [[Resources/AI/2026-05-27 - Taste Skill 讓 AI 產生更有質感介面]]
- [[Resources/Tools/2026-05-27 - CodeGraph 降低 AI 寫程式 Token 消耗]]
- [[Resources/AI/2026-05-27 - Codex 一手包辦辦公流程自動化]]
- [[Resources/Tools/2026-05-23 - Docker 從入門到實踐]]
- [[Resources/AI/2026-05-22 - Anthropic 多晶片算力佈局]]
- [[Resources/Tools/2026-05-22 - Google AI Studio 網頁讀取實測]]
- [[Resources/AI/2026-05-21 - Markdown 給 AI HTML 給人看]]
- [[Resources/AI/2026-05-20 - Microsoft AI Agents 入門 12 課]]
- [[Resources/AI/2026-05-20 - Microsoft Agent Framework 與 Skill 解耦]]
- [[Resources/Tools/2026-05-20 - LINE 語音轉文字 Webhook 實作]]
- [[Resources/Tools/2026-05-15 - html-anything Agent HTML 生成工具]]
- [[Resources/Tools/2026-05-12 - Obsidian AI 側邊欄與語義搜尋]]

## 整理後參考資源

- [[Resources/README|Resources — AI 整理後參考資源]]

```dataview
TABLE summary, tags, file.mtime AS "最後更新"
FROM "Resources"
SORT file.mtime DESC
LIMIT 20
```

## AI 說明

- [[AI/README|AI — 給 AI 讀的整理規則]]

## 樣板

- [[Templates/README|Templates — 必要樣板]]

## 常用標籤

| 標籤 | 說明 |
|------|------|
| `#status/draft` | 尚未整理 |
| `#status/review` | AI 已整理，待人工確認 |
| `#status/done` | 已確認可作為參考 |
| `#type/clipping` | 原始收集 |
| `#type/resource` | 整理後參考資源 |
