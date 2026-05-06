---
title: Projects — 專案
tags:
  - MOC
  - type/project
---

# 🗂️ Projects — 專案

此目錄存放**有明確開始與結束時間**的目標導向工作。每個專案一個子目錄或單一筆記。

## 專案筆記結構

```
Projects/
├── ProjectA/
│   ├── README.md      # 專案概覽（目標、期程、狀態）
│   ├── Tasks.md       # 任務清單
│   └── Notes/         # 專案相關筆記
└── ProjectB.md        # 小型專案可用單一檔案
```

## 專案狀態標籤

| 標籤 | 說明 |
|------|------|
| `#status/planning` | 規劃中 |
| `#status/active` | 進行中 |
| `#status/paused` | 暫停 |
| `#status/done` | 已完成（移至 Archives） |

## AI 協作提示

- 請 AI 根據專案筆記產生**週報摘要**
- 請 AI 協助分解大目標為可執行的子任務
- 完成的專案移至 `Archives/Projects/`

```dataview
TABLE status, due, file.mtime AS "最後更新"
FROM "Projects"
WHERE status != "done"
SORT due ASC
```

[[00-Home|← 返回首頁]]
