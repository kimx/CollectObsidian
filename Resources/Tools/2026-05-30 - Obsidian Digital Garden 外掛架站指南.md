---
title: "Obsidian Digital Garden 外掛架站指南"
date: 2026-05-30
source: "https://github.com/oleeskild/obsidian-digital-garden"
author: "[[oleeskild]]"
published: ""
category: Resources/Tools
tags:
  - type/clipping
  - status/processed
  - type/resource
  - obsidian
  - digital-garden
summary: "Obsidian Digital Garden 外掛可將 Obsidian 筆記選擇性發布為個人網站，支援 Dataview、Canvas、Mermaid 與多種佈景自訂。"
key_points:
  - "以 `dg-publish: true` 控制公開範圍，未標記筆記不會被發布。"
  - "預設可搭配 Vercel、Netlify 部署，也可用 Forestry.md 簡化託管流程。"
  - "支援 Dataview、Canvas、Excalidraw、Mermaid、PDF 與反向連結等常見知識庫內容。"
  - "可透過 CSS 變數與自訂元件調整站點外觀與互動行為。"
actionable: "以現有 Obsidian vault 建立一個測試 digital garden，先發布首頁與 3 篇筆記驗證發佈與隱私控制流程。"
---

# 📎 Obsidian Digital Garden 外掛架站指南

## 摘要

> 這個開源外掛讓使用者把 Obsidian vault 轉成可公開瀏覽的 digital garden，並維持「只發布明確標記筆記」的隱私模型，兼顧內容分享與個人知識管理。

## 重點

- 核心概念是「選擇性發布」，僅有 `dg-publish: true` 的筆記會被上傳。
- 初始安裝流程以 GitHub + Vercel 為主，約 10 分鐘可完成第一版網站上線。
- 內容支援度高，涵蓋 Dataview、Canvas、Excalidraw、Mermaid 與多種嵌入內容。
- 可用 Forestry.md 走免 GitHub 的託管路線，降低非技術使用者門檻。
- 站點模板可持續更新，並透過 PR 流程將新版模板合併回自己的 garden repo。

## 可行動事項

- [ ] 在個人 vault 建立 `dg-home` 與 `dg-publish` 範例頁，實測部署與更新流程。
- [ ] 比較 Vercel 與 Forestry.md 的維運成本，決定長期託管方案。

## 原文整理

- 專案定位為將 Obsidian 筆記轉為「持續成長的數位花園」，強調內容可逐步演進而非一次性發布。
- 官方教學主流程包含：建立 GitHub/Vercel 帳號、部署樣板、建立 fine-grained token、填入外掛設定、發布首篇筆記。
- 發布規則明確：不會因為連結關係自動公開其他筆記，避免意外外洩私人內容。
- 提供進階客製能力，如 CSS 覆寫、Nunjucks 自訂元件、模板升級與本地匯出開發流程。

## 相關筆記

- [[Resources/Tools/2026-05-12 - Obsidian AI 側邊欄與語義搜尋]]
- [[Resources/Tools/2026-05-27 - CodeGraph 降低 AI 寫程式 Token 消耗]]

## 來源

- 原文：[oleeskild/obsidian-digital-garden](https://github.com/oleeskild/obsidian-digital-garden)
- 作者：[[oleeskild]]
