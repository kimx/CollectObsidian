---
title: "Taste-Skill 提升 AI 介面設計品味"
date: 2026-05-27
source: "https://github.com/Leonxlnx/taste-skill"
author: "[[Leonxlnx]]"
published: ""
category: Resources/AI
tags:
  - type/clipping
  - status/processed
  - type/resource
summary: "Taste-Skill 提供可攜式 Agent Skills，強化 AI 產生前端介面的版面、字體與動態品質，減少制式化輸出。"
key_points:
  - "以可安裝的 Skill 套件提升 AI 產出的視覺一致性與設計層次"
  - "支援多種技能組合，涵蓋前端實作、重設計與 image-to-code 流程"
  - "可用 npx skills add 安裝，並針對特定 skill 名稱精準載入"
  - "內建可調參數（變化度、動態強度、密度）以控制設計風格"
actionable: "挑選一個現有前端頁面，套用 taste-skill 與基準提示詞各產出一次，比較可讀性與視覺一致性。"
---

# 📎 Taste-Skill 提升 AI 介面設計品味

## 摘要

> 這個專案將「設計品味」封裝成可重用的 Agent Skills，目標是減少 AI 生成前端時常見的模板化與單調感，讓輸出更接近可上線的設計品質。

## 重點

- 提供 anti-slop 設計規則，強化版面結構、字體層級與動態細節
- 支援多種技能（例如 redesign、image-to-code、風格化輸出）
- 安裝方式統一，可整包安裝或只安裝特定 skill
- 透過參數旋鈕調整輸出風格，適配不同產品情境

## 可行動事項

- [ ] 在團隊常用 AI 開發流程中加入 taste-skill，建立一份前端視覺品質對照基準。

## 原文整理

- 專案定位為可攜式技能框架，可與 Codex、Cursor、Claude Code 等工具搭配。
- 核心價值是把設計規則系統化，避免 AI 只產生「看起來都一樣」的介面。
- 除了程式碼產生技能，也包含影像生成技能，支援先圖後碼的流程。

## 相關筆記

- [[Resources/AI/2026-05-20 - Microsoft Agent Framework 與 Skill 解耦]]
- [[Resources/AI/2026-05-21 - Markdown 給 AI HTML 給人看]]

## 來源

- 原文：[Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill)
- 作者：[[Leonxlnx]]
