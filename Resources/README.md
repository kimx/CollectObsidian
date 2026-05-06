---
title: Resources — 主題參考資料
tags:
  - MOC
  - type/resource
---

# 📚 Resources — 主題參考資料

此目錄存放**以主題分類的參考資料**，不限於個人想法，可包含書籍筆記、研究摘要、教學資料等。

## 建議子目錄

```
Resources/
├── Books/             # 書籍摘要與心得
├── Courses/           # 課程筆記
├── Tools/             # 工具與軟體使用筆記
├── Concepts/          # 概念解釋（術語表）
└── Databases/         # 資料庫（人物、地點、組織等）
```

## AI 協作提示

- 讓 AI 根據多本書的筆記進行**跨書主題比較**
- 讓 AI 從 Clippings 中提取重點，自動生成 Resources 筆記
- 讓 AI 建立 Concepts 術語表，標準化知識庫中的用語

```dataview
TABLE summary, tags, file.mtime AS "最後更新"
FROM "Resources"
SORT file.mtime DESC
LIMIT 20
```

[[00-Home|← 返回首頁]]
