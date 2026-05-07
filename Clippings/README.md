---
title: Clippings — 網路剪藏
tags:
  - MOC
  - type/clipping
---

# 📎 Clippings — 網路剪藏

此目錄存放使用 [Obsidian Web Clipper](https://obsidian.md/clipper) 或其他工具擷取的網頁文章、參考連結。

## 使用方式

1. 安裝 **Obsidian Web Clipper** 瀏覽器擴充功能
2. 瀏覽到感興趣的頁面，點擊擴充圖示進行剪藏
3. 選擇儲存至 `Clippings/` 目錄
4. 套用 `Templates/clipping` 模板

## 建議子目錄（依主題分類）

```
Clippings/
├── Tech/         # 技術文章
├── Business/     # 商業管理
├── Science/      # 科學研究
├── Life/         # 生活健康
└── Misc/         # 其他
```

## AI 協作提示

- 累積足夠剪藏後，可讓 AI 對同一主題的剪藏進行**綜合摘要**，輸出至 `AI/Summaries/`
- 使用 Dataview 查詢此目錄下待閱讀的文章：

## 近期剪藏

- [[Clippings/R-2026-05-06 給 AI 超能力？Superpowers 的設計與取捨]]
- [[Clippings/R-2026-05-06 截圖軟體 ShareX]]
- [[Clippings/R-2026-05-06 這 20 個提示詞教你深度使用 Claude：變身你的私人助理、教練與分析師]]

```dataview
TABLE source, summary, tags
FROM "Clippings"
WHERE !contains(tags, "status/done")
SORT date DESC
```

[[00-Home|← 返回首頁]]
