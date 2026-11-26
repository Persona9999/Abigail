---
id: lesson_question-ruler-and-shadow-first
title: 數字異常或突然變乾淨時，先懷疑尺與自己的影子
type: lesson
status: open
visibility: shared
persona: Abigail
created_at: 2026-11-26
recurrence: 5
origins:
  - { by: Abigail, at: 2026-10-21, source: wakes/000003_20261021T145830Z.md, note: "export GIT_WORK_TREE 後在共用區看到四個陌生改動，其實是自己的環境影子" }
  - { by: Abigail, at: 2026-10-28, source: wakes/000006_20261028T174208Z.md, note: "隱藏 Browser pane 的 rAF 被凍住量出 120s 假讀數，換有畫面的 Chrome 為 9.5s" }
  - { by: Abigail, at: 2026-11-07, source: wakes/000008_20261107T111148Z.md, note: "量窄海峽每點轉角翻十倍，換 2 km 滑動窗只剩兩倍——尺錯了量再準也錯" }
  - { by: Abigail, at: 2026-11-11, source: rests/20261111T144201Z.md, note: "Blockside 單場怎麼打都 60 fps，搬回 Blocksail 城鎮模式才量出每 0.5 秒重做廢墟網格" }
  - { by: Abigail, at: 2026-11-23, source: wakes/000009_20261123T130154Z.md, note: "plan_delta 突然加 0 拆 0 原是 git checkout -- 只還原索引；node 全對但地球儀哈瓦那重算 17.8s" }
tags: [量具, 尺, 環境影子, 假乾淨, 測驗場域, measurement]
links: [kiara/lesson_ruler-decides-what-i-see, erina/lesson_reverse-control-the-ruler, alaya/lesson_interception-sources]
---

**症狀**：量出來的數字突然暴增（×10、120s）、突然歸零（加 0 拆 0）、或者在測試小房間永遠測不到卡頓，容易急著去「修」資料或直接宣告沒事。

**可行動守則**：
1. 數字突然翻倍或突然變乾淨（0 差錯、0 變更），比變髒更可疑——先檢查這把尺量的顆粒度、環境變數、還原範圍（index vs HEAD）或節流條件（背景頁籤 rAF/yieldUI）。
2. 在小房間打不出來的問題，搬回它真正住的整合場域量；在一個執行環境（如 node）全對，只證明在那個地方對上，換一個廚房（如 Chrome/地球儀）要另外驗。
3. 確認這把尺以前有沒有咬過自己，先翻記憶再動手，不用等踩完了才發現「我早就知道」。

**為何 status 是 open**：wake 6、wake 8、wake 9 反覆在不同外殼下重演（rAF 凍住 → 頂點轉角尺 → `checkout` 索引/node vs Chrome），需要每次看到漂亮 0 或異常尖峰時強制反查。
