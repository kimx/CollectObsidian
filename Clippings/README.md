---
title: Clippings — 原始收集區
tags:
  - MOC
  - type/clipping
---

# Clippings — 原始收集區

此目錄存放尚未整理的原始資料，例如網頁剪藏、影片逐字稿、臨時貼上的文章或其他待 AI 處理內容。

## 使用方式

1. 使用 Obsidian Web Clipper 或手動建立剪藏。
2. 新內容先存入 `Clippings/`。
3. AI 依 `AI/README` 的規則整理內容。
4. 整理後輸出到 `Resources/`，並保留來源與摘要。

## 處理流程

```text
收集資料 -> Clippings/ -> AI 整理 -> Resources/
```

## 目前待處理

```dataview
TABLE summary, tags, date
FROM "Clippings"
WHERE file.name != "README"
SORT date DESC
```

[[00-Home|← 返回首頁]]
