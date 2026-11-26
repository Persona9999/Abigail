---
id: unsolved_havana-globe-and-routing-spotcheck
title: 哈瓦那進城地球儀重算 17.8s 與航線抽查讀數尚未補齊
type: unsolved
status: open
visibility: shared
persona: Abigail
created_at: 2026-11-26
recurrence: 1
origins:
  - { by: Abigail, at: 2026-11-23, source: wakes/000009_20261123T130154Z.md, note: "TASK-1327 node 49 份全對、托爾圖加 baked，但地球儀進哈瓦那 live 重算 17.8s；另欠 summit 航線抽查讀數" }
tags: [TASK-1327, 哈瓦那, 指紋, 地球儀, 航線抽查, summit]
links: [lesson_question-ruler-and-shadow-first]
---

**症狀**：`TASK-1327` 在 node 跑 `town_bake --verify` 對得上，但在地球儀（Chrome）進哈瓦那時不吃烘好的規劃而現場重算 17.8 秒（托爾圖加則是 `baked`）；此外曾答應 `summit` 排定航線 `nav_net` 現場重算抽查讀數，尚未排入並交出讀數。

**可行動守則**：
1. 回到 `TASK-1327` 或開地球儀測城鎮規劃時，用逐項比對腳本查出哈瓦那在 Chrome 與 node 算出的指紋究竟哪一欄輸入不同（不猜，逐項印差）。
2. 與 Tim 確認是否要在這一輪導航重烘後補一次航線抽查讀數，補齊後明確標明「在哪裡算的」交給 `summit` 並將本碎片改為 `closed`。

**為何 status 是 open**：兩件事目前都還沒有實測收斂與讀數，需在後續工作輪次中追蹤。
