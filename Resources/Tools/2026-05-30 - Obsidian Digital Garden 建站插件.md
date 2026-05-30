---
title: "Obsidian Digital Garden 建站插件"
date: 2026-05-30
source: "https://github.com/oleeskild/obsidian-digital-garden"
author: "[[oleeskild]]"
published: ""
category: Resources/Tools
tags:
  - type/clipping
  - status/processed
  - type/resource
  - topic/obsidian
  - topic/publishing
  - topic/opensource
summary: "這個 Obsidian 外掛可把筆記庫發布成可自管的數位花園網站。"
key_points:
  - "只發布標記 dg-publish 的筆記，避免私密內容意外公開"
  - "支援連結、搜尋、圖譜、Dataview、Canvas 與多種嵌入內容"
  - "可部署到 Vercel、Netlify，或改用 Forestry 託管"
  - "可用 CSS 變數與自訂元件調整網站外觀與功能"
  - "支援本機匯出與本地開發流程，方便自架與測試"
actionable: "挑一個公開筆記庫，用 Vercel 試部署數位花園並驗證發布流程。"
---

# 📎 Obsidian Digital Garden 建站插件

## 摘要

> Obsidian Digital Garden 是把 Obsidian 筆記發布成網站的開源方案。它主打只公開明確標記的筆記，並保留主題、樣式與部署方式的高度控制，適合想把知識庫做成可持續維護的數位花園。

## 重點

- 只會發布加上 `dg-publish: true` 的筆記，降低私密內容外流風險
- 支援 Obsidian 常見內容型態，包括雙向連結、圖譜、Dataview、Canvas、Mermaid 與 PDF
- 預設可部署到 Vercel 或 Netlify，也提供 Forestry 的代管方案
- 可透過 CSS 變數、自訂樣式與元件調整網站外觀
- 支援本機匯出與開發模式，方便自架與預覽

## 可行動事項

- [ ] 挑一個公開筆記庫，用 Vercel 試部署數位花園並驗證發布流程。

## 原文整理

- 這個專案把 Obsidian vault 轉成可公開瀏覽的網站，定位是可逐步生長的 digital garden，而不是傳統部落格。
- 發布流程核心是以 frontmatter 控制公開狀態，例如首頁用 `dg-home: true`，單篇公開用 `dg-publish: true`。
- 功能面支援豐富，從連結、反向連結、圖譜、目錄到各種嵌入內容都能保留。
- 部署面可直接接 Vercel、Netlify，也能改走 Forestry 或本機匯出，兼顧自架與低技術門檻需求。
- 對開發者來說，還能進一步調整樣式、模板與元件，將筆記網站客製成自己的知識入口。

## 相關筆記

- [[Resources/Tools/2026-05-12 - Obsidian AI 側邊欄與語義搜尋]]

## 來源

- 原文：[oleeskild/obsidian-digital-garden](https://github.com/oleeskild/obsidian-digital-garden)
- 作者：[[oleeskild]]
