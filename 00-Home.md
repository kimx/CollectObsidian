---
title: 🏠 知識庫首頁
date: 2026-05-06
tags:
  - MOC
  - index
---

# 🏠 知識庫首頁（Map of Content）

> 這是整個 Obsidian 知識庫的入口。所有重要的主題索引都從這裡出發。

---

## 📥 最近收集

- [[Resources/Tools/2026-05-15 - html-anything Agent HTML 生成工具]]
- [[Resources/Tools/2026-05-12 - Obsidian AI 側邊欄與語義搜尋]]
- [[Resources/AI/2026-05-09 - OpenAI 聊天完成與回應 API]]
- [[Resources/Tools/2026-05-09 - SuperSplat 3D Gaussian Splat 編輯器]]

## 📝 筆記區

- [[Notes/Daily/README|每日筆記（Daily Notes）]]
- [[Notes/Fleeting/README|靈感速記（Fleeting Notes）]]
- [[Notes/Permanent/README|永久筆記（Permanent Notes）]]

## 🗂️ 領域

- [[Areas/README|領域（Areas）]]

## 📚 資源庫

- [[Resources/README|參考資料（Resources）]]

## 🤖 AI 協作區

- [[AI/README|AI 工作區]]
- [[AI/Prompts/README|Prompt 模板庫]]
- [[AI/Summaries/README|AI 摘要]]
- [[AI/Conversations/README|AI 對話紀錄]]

## 🗄️ 封存

- [[Archives/README|封存（Archives）]]

---

## 🏷️ 常用標籤（Tags）

| 標籤 | 說明 |
|------|------|
| `#status/draft` | 草稿，尚未整理 |
| `#status/review` | 待審閱或待深化 |
| `#status/done` | 已完成、精煉完畢 |
| `#type/clipping` | 網路剪藏 |
| `#type/note` | 個人筆記 |
| `#type/resource` | 參考資料 |
| `#type/ai-output` | AI 產出內容 |
| `#area/work` | 工作領域 |
| `#area/learning` | 學習領域 |
| `#area/life` | 生活領域 |

---

## 📊 Dataview 快速查詢範例

列出所有草稿筆記：
```dataview
LIST
FROM #status/draft
SORT file.mtime DESC
```

列出本週新增的剪藏：
```dataview
TABLE source, summary
FROM "Clippings"
WHERE date >= date(today) - dur(7 days)
SORT date DESC
```
