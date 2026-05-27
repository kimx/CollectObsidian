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
