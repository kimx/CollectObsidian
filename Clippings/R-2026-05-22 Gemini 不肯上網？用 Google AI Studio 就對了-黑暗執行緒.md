---
title: "Gemini 不肯上網？用 Google AI Studio 就對了-黑暗執行緒"
source: "https://blog.darkthread.net/blog/ai-studio-tools/"
author:
created: 2026-05-22
description: "上篇文章提到 Gemini 打死不讀網頁的困擾，發文沒多久，上官大人現身開示，指引我一條明路...坦白說，我沒有很認真研究各種 AI 工具，不怎麼看教學跟文件，都是憑直覺胡亂摸索到能做事就好。(就跟 MIS 眼中典型 End User 一個樣，好孩子不要學) 先前有聽過 AI Studio，剛訂..."
tags:
  - "clippings"
---
[上篇文章](https://blog.darkthread.net/blog/anythingllm-web-browsing/) 提到 Gemini 打死不讀網頁的困擾，發文沒多久，上官大人現身開示，指引我一條明路...

![](https://blog.darkthread.net/Posts/files/2026/Fig1_639149736473990355.jpg)

坦白說，我沒有很認真研究各種 AI 工具，不怎麼看教學跟文件，都是憑直覺胡亂摸索到能做事就好。(就跟 MIS 眼中典型 End User 一個樣，好孩子不要學) 先前有聽過 AI Studio，剛訂閱 AI Pro 時有試了一下，但當時 Nano Banana 生圖要用 Gemini 網頁，我後來就都是用 Gemini；加上我主要是玩 AOAI 用 GPT 模型，沒什麼動機與機會深入 AI Studio。

今天重新看了 [Google AI Studio](https://aistudio.google.com/) ，它的操作概念類似 Gemini 網頁，一樣是輸入提示，上傳檔案，送出後請 AI 執行回傳結果。但 AI Studio 像是工程模式的 Gemini，可以指定溫度、設定思考深度，有一整套儀表板式的工具開關，並能指定安全限制、Top P，就是一堆普通使用者看了頭昏、工程師見了興奮的玩意兒。

其中有兩個我在意的重要選項：

1. Grounding with Google Search  
	可使用強大的 Google 搜尋引擎爬文 (這點狂勝 AnythingLLM + DuckDuckGo )  
	註：啟用後不能使用 Structed outputs、Code execution 及 Function calling
2. URL Context  
	可閱讀你提供的特定網頁、PDF 或技術文件

不囉嗦，直接用上篇文章提到的三個 Case 實測。

![](https://blog.darkthread.net/Posts/files/2026/Fig3_639149736482958820.png)

![](https://blog.darkthread.net/Posts/files/2026/Fig4_639149736488901453.png)

![](https://blog.darkthread.net/Posts/files/2026/Fig5_639149736496744971.png)

就不多做解釋了，AI Studio 的表現非常接近我的期望，若有差距我相信也能透過調整 Prompt 改善。

所以結論是：我一直用錯工具了，哈! 嚴格來說，Gemini WebUI 的介面更直覺易用，更接近一般使用者的習慣，而 AI Stuiod 介面就很工程師風格，連 Playground 命名都擺明是做實驗跟研究的地方，但啟用工具後根本開啟了桃花源，我決定以後會常來這裡玩。
test pat classic