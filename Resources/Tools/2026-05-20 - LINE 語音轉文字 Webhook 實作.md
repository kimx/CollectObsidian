---
title: "LINE 語音轉文字 Webhook 實作"
date: 2026-05-20
source: "https://github.com/robinli/line-audio-text"
author: "[[robinli]]"
published: ""
category: Resources/Tools
tags:
  - type/clipping
  - status/processed
  - type/resource
summary: "整合 LINE、OpenAI 與 Firebase 的語音轉文字服務。"
key_points:
  - "接收 LINE Webhook 並驗證簽章"
  - "下載語音後用 OpenAI 進行轉錄"
  - "轉錄狀態寫入 Firestore 管理"
  - "支援兩階段回覆與單次回覆模式"
  - "可部署 Zeabur 並提供健康檢查端點"
actionable: "依 README 變數清單部署一版測試環境並跑通 webhook。"
---

# 📎 LINE 語音轉文字 Webhook 實作

## 摘要

> 這個專案示範如何串接 LINE 官方帳號、OpenAI Speech-to-Text 與 Firebase，建立可部署的語音轉文字 webhook 服務。流程完整且具備實務部署考量，適合做為整合範本。

## 重點

- 音訊事件可自動下載並轉文字
- LINE 簽章驗證確保 webhook 安全
- Firestore 記錄處理中與完成狀態
- 提供 two_step 與 single_reply 回覆模式
- 可搭配 Zeabur 與 Docker 快速上線

## 可行動事項

- [ ] 先用 `single_reply` 模式本機測試，再切換 `two_step` 上線。

## 原文整理

- 專案使用 Node.js + TypeScript，提供 `POST /webhook` 與 `GET /health` 端點。
- 服務流程為：接收 LINE 音訊事件 → 驗證簽章 → 下載音訊 → 呼叫 OpenAI 轉錄 → 寫入 Firestore → 回覆使用者。
- 支援是否保存原始音訊至 Firebase Storage，並用 `transcriptJobs` 管理工作狀態。
- README 提供完整環境變數、開發指令、Docker 與 Zeabur 部署說明。

## 相關筆記

- [[Resources/AI/2026-05-09 - OpenAI 聊天完成與回應 API]]
- [[Resources/Tools/2026-05-12 - Obsidian AI 側邊欄與語義搜尋]]

## 來源

- 原文：[robinli/line-audio-text](https://github.com/robinli/line-audio-text)
- 作者：[[robinli]]
