---
title: Resources — AI 整理後參考資源
tags:
  - MOC
  - type/resource
---

# Resources — AI 整理後參考資源

此目錄存放 AI 從 `Clippings/` 整理後產生的參考資源。內容應可回查、可引用，並保留原始來源。

## 目前子目錄

```text
Resources/
├── AI/                # AI 主題、模型、提示詞與工具鏈相關資料
└── Tools/             # 工具與軟體使用筆記
```

## 筆記要求

- 保留 `source` 或原文連結。
- 用 `summary` 說明這份資源的核心價值。
- 重點整理以可掃讀、可回查為主。
- 不確定的內容標示「待確認」。

```dataview
TABLE summary, tags, file.mtime AS "最後更新"
FROM "Resources"
SORT file.mtime DESC
LIMIT 20
```

[[00-Home|← 返回首頁]]
