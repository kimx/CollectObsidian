---
title: "給 AI 超能力？Superpowers 的設計與取捨"
date: 2026-05-06
source: https://kaochenlong.com/ai-superpowers-skills
author: "[[高見龍]]"
published: ""
category: Resources/AI
tags:
  - type/clipping
  - status/processed
  - topic/ai
  - topic/workflow
  - topic/tdd
summary: "介紹 Superpowers 如何用 Skills 與流程規範替 AI 寫程式補上紀律"
key_points:
  - "用 15 個 Skills 串起完整開發流程"
  - "從需求釐清到測試與審查都有規則"
  - "用硬性流程補足 AI 缺乏紀律的問題"
  - "適合代理式開發與一致性要求高的任務"
  - "設計激進，但很適合拿來當工作流參考"
actionable: "挑一個常用 AI 流程，先補上需求、測試與驗證規則。"
---

# 📎 給 AI 超能力？Superpowers 的設計與取捨

## 摘要

> Superpowers 不是單一工具，而是一套替 AI 建立工作紀律的流程規範。它用 Skills、hook 與明確步驟，把需求釐清、計畫、TDD、驗證與審查串成固定流程，目標是減少 AI 偷跑、漏測試或跳過驗證的情況。

## 重點

- 以 15 個 Skills 定義完整的 AI 開發流程
- 把需求釐清、計畫撰寫、TDD、除錯與審查標準化
- 透過 SessionStart hook，讓規範在對話一開始就生效
- 核心不是模型能力，而是用流程補足 AI 的紀律不足
- 適合代理式開發，但不一定適用所有情境

## 可行動事項

- [ ] 檢查你自己的 AI 開發流程，找出最常跳步驟的地方。
- [ ] 先替「需求釐清」和「驗證」補上固定規則。

## 原文整理

- 文章把 Superpowers 定位成 AI 的工作流規範，不是函式庫或單一功能。
- `brainstorming`、`writing-plans`、`test-driven-development`、`systematic-debugging` 等 Skills，分別負責需求、計畫、測試與除錯。
- 設計原則很硬：要先驗證、要先測試、不要跳過關鍵步驟。
- 兩階段審查與收到 review 後的處理流程，都是為了避免 AI 自顧自地完成工作。
- 作者也提到取捨：這套規範很強，但偏重、偏嚴格，未必適合所有工作場景。

## 相關筆記

- [[Resources/AI/2026-05-07 - Claude／GPT 反討好提示詞]]

## 來源

- 原文：[給 AI 超能力？Superpowers 的設計與取捨](https://kaochenlong.com/ai-superpowers-skills)
- 作者：[[高見龍]]