# CollectObsidian

使用 Obsidian 收集資料，交由 AI 整理成可回查的參考資源。

## 知識庫目錄結構

```text
CollectObsidian/
├── 00-Home.md              # 知識庫入口
├── AI/                     # 給 AI 讀的整理規則與操作說明
├── Clippings/              # 原始收集區
├── Resources/              # AI 整理後的參考資源
└── Templates/              # 必要樣板
```

## 各目錄說明

| 目錄 | 用途 |
|------|------|
| `AI/` | 放給 AI 讀的工作說明、整理規則與輸出要求 |
| `Clippings/` | 使用瀏覽器插件或手動收集的原始資料 |
| `Resources/` | AI 整理、摘要、歸類後的參考資源 |
| `Templates/` | Obsidian 建立剪藏與資源筆記時需要的樣板 |

## AI 整理原則

1. **先收集，再整理**：原始資料先進 `Clippings/`，整理後再移入 `Resources/`。
2. **保留來源**：每則資源需保留 `source`、`date`、`tags` 與 `summary`。
3. **輸出可回查**：AI 整理後的內容要能作為日後查詢、引用與延伸閱讀的參考。
4. **避免過度分類**：目前只維持必要資料夾，不新增 Notes、Areas、Archives 等分類。

## 推薦 Obsidian 插件

- **Templater** — 套用 `Templates/` 中的樣板
- **Dataview** — 查詢 Clippings 與 Resources
- **Obsidian Web Clipper** — 網頁剪藏至 `Clippings/`
