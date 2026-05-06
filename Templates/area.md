---
title: <% tp.file.title %>
date: <% tp.date.now("YYYY-MM-DD") %>
tags:
  - type/area
summary: 
---

# 🎯 <% tp.file.title %>

## 📌 此領域的核心目標

<!-- 我在這個領域想要維持什麼樣的標準？ -->

## 🗂️ 相關專案

```dataview
LIST
FROM "Projects"
WHERE area = "<% tp.file.title %>"
```

## 📚 相關資源

- 

## 📝 定期回顧紀錄

### <% tp.date.now("YYYY-MM") %> 回顧

- **現況：** 
- **改善點：** 
