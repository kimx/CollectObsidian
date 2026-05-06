---
title: AI Summaries — AI 摘要輸出
tags:
  - MOC
  - AI
  - type/ai-output
---

# 📄 AI Summaries — AI 摘要輸出

此目錄存放 AI 針對筆記、剪藏或主題所產生的摘要與報告。

## 命名規則

```
YYYY-MM-DD-<主題或來源>.md
```

範例：
- `2026-05-06-AI知識庫架構總結.md`
- `2026-05-06-Clippings-科技趨勢綜合報告.md`

## Frontmatter 規範

```yaml
---
title: 摘要標題
date: YYYY-MM-DD
source_notes:          # 來源筆記連結列表
  - "[[筆記A]]"
  - "[[筆記B]]"
ai_tool: ChatGPT-4o   # 使用的 AI 工具
tags:
  - type/ai-output
  - status/review
summary: 一句話描述此摘要的主題
---
```

---

[[AI/README|← 返回 AI 協作區]] | [[00-Home|← 返回首頁]]
