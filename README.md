# CollectObsidian
使用 Obsidian 收集筆記，並規劃一個 AI 可協助的知識庫架構。

## 知識庫目錄結構

```
CollectObsidian/
├── 00-Home.md              # 主儀表板（Map of Content）
├── Clippings/              # 網路剪藏（Web Clippings）
├── Notes/                  # 個人筆記
│   ├── Daily/              # 每日筆記
│   ├── Fleeting/           # 靈感速記
│   └── Permanent/          # 精煉永久筆記
├── Projects/               # 專案管理
├── Areas/                  # 持續關注的領域
├── Resources/              # 主題參考資料
├── Archives/               # 封存（已完成或不活躍）
├── AI/                     # AI 協作區
│   ├── Prompts/            # Prompt 模板庫
│   ├── Summaries/          # AI 摘要輸出
│   └── Conversations/      # AI 對話紀錄
└── Templates/              # 筆記模板
```

## 各目錄說明

| 目錄 | 用途 |
|------|------|
| `Clippings/` | 使用瀏覽器插件（如 Obsidian Web Clipper）擷取的網頁文章 |
| `Notes/Daily/` | 每天的日誌、反思、快速記錄 |
| `Notes/Fleeting/` | 尚未整理的靈感、想法片段 |
| `Notes/Permanent/` | 深度整理後的「常青筆記」（Evergreen Notes）|
| `Projects/` | 有開始與結束的目標導向工作 |
| `Areas/` | 長期持續關注的責任範疇（如：健康、財務、學習）|
| `Resources/` | 以主題分類的參考資料庫 |
| `Archives/` | 封存舊有或已完成的內容 |
| `AI/Prompts/` | 可重複使用的 AI Prompt 模板 |
| `AI/Summaries/` | AI 對長文、剪藏的自動摘要 |
| `AI/Conversations/` | 與 AI 工具的對話紀錄與成果 |
| `Templates/` | Obsidian 筆記模板（可搭配 Templater 插件使用）|

## AI 協作設計原則

1. **標籤（Tags）統一** — 使用 `#status/draft`、`#status/review`、`#status/done` 管理筆記狀態，讓 AI 可快速篩選需要處理的內容。
2. **YAML Frontmatter** — 每則筆記均包含結構化 Frontmatter（`title`、`date`、`tags`、`source`），方便 AI 解析與索引。
3. **雙向連結（Backlinks）** — 透過 `[[Wiki Link]]` 建立知識網絡，輔助 AI 進行關聯推理。
4. **摘要欄位（summary）** — Permanent Notes 與 Resources 包含 `summary` 欄位，方便 AI 快速理解筆記主旨。
5. **MOC（Map of Content）** — `00-Home.md` 作為全庫入口，AI 可從此出發導航整個知識庫。

## 推薦 Obsidian 插件

- **Templater** — 自動套用筆記模板
- **Dataview** — SQL 式查詢筆記資料
- **Obsidian Web Clipper** — 網頁剪藏至 Clippings
- **Smart Connections** — AI 語意搜尋與關聯筆記
