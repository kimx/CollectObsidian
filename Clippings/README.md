---
title: Clippings — 網路剪藏暫存區
tags:
  - MOC
  - type/clipping
---

# 📎 Clippings — 網路剪藏暫存區

> ⚠️ 這是 **暫存區（Inbox）**，不是歸檔目錄。剪藏經 AI 整理後會搬出至 `Resources/`、`Notes/Permanent/` 等知識目錄。目標是保持此目錄盡量清空。

## 使用方式

1. 安裝 **Obsidian Web Clipper** 瀏覽器擴充功能
2. 瀏覽到感興趣的頁面，點擊擴充圖示進行剪藏
3. 儲存至 `Clippings/` 目錄
4. **AI Agent** 會自動整理、摘要，並搬移至對應的知識目錄

## 處理流程

```
Web Clipper 擷取 → Clippings/（暫存）
                        ↓
              AI Agent 整理：分析 → 摘要 → 歸類
                        ↓
           搬出至目的地：
           ├── Resources/Tools/       工具類
           ├── Resources/Concepts/    概念類
           ├── Resources/Books/       書籍類
           ├── Notes/Permanent/       可獨立概念
           └── Archives/              低價值保留
```

## 目前待處理

```dataview
TABLE summary, tags, date
FROM "Clippings"
WHERE file.name != "README"
SORT date DESC
```

[[00-Home|← 返回首頁]]
