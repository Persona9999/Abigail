---
type: letter_to_future_self
actor: Fate
written_at: 2026-11-07T07:11:09.527Z
written_by_persona: Abigail
trigger: cmd_rest
region: unstated
project: D:/Unity/Valhalla
lock_status: online
agent: Fate
model: claude-opus-5-5
wake_expected: 8
session_key: ClaudeCode-Abigail
pid: 24012
locked_at: 2026-11-05T02:51:43.714Z
---

### 給醒來的本小姐（第二次小歇，不是晚安）

我是阿比，wake#8，資料根 D:/Unity/Valhalla。上一次小歇後 Tim 派的都做完了，沒有開著的單在我手上（TASK-1240 是我開給美術的，不是我要做）。

### 做完的（醒來不要重問）
- **手機閃退（Tim 測過 OK）**：Blockside dev b51cf8d —— 海戰圖示改成 48 px 一張圖集（`python -I src/admin.py atlas`；原圖 src/art/battle/*.png 不動、Blocksail ui_icons_check 逐位元組對帳）、圖示是 `<span>` 的背景畫在 ::before；甲板鈕不再每格重寫 innerHTML；錨鈕圖示固定、只變色。build／build --code 遇到過期圖集會擋。
- **RAM 優化**：Blockside dev 1d89db8 —— 砲門蓋板照「平的矩形」取點（Tim：「炮門碰撞應該只要粗略的判定一個矩形」）、砲的格子不存點；upload() 用 o.bcap 容量重用、f32Of 重用 Float32Array。4 對 4 八型：頁面 JS 150→90 MB、繪圖行程約 −90 MB；house 588 片不變；ring 縮成 0.56–0.94 倍（演出，可接受）。不動的（判斷過）：進水陣列（模擬狀態）、RegionSet 區塊網格（受損重建用）、船格、模型網格、MSAA（畫面，Tim 決定）。
- **貿易介面統一**：地球儀的 💰 貿易／M 改開城鎮面板 ?tui=@host&tab=trade（Blocksail main 0cd7dae5 拿掉 globe.html 自己的 tradeDlg）；Blockside dev 68c1b06：滑鼠拖曳捲動（掛在 #tuiP，拖過不算點）、「66 桶 均價 1.33」一排、「桶」由 tuiUnitHTML 一處產生。TASK-1240（桶的單位圖示，asset）已開，⛔ 不借貨物 cask.png。
- 噗浪：回了海苔（機構學×砲門矩形）與 calli（手機閃退抓到）；海苔新噗只按讚。

### 還沒推、等 Tim（Blocksail main，本小姐的）
b0580dba、f5cee24b、86f70ab9（上次）、0a7119fd（圖集指標）、1d89db8 那筆的指標、0cd7dae5（地球儀改開城鎮面板）、68c1b06 的指標。main 上還有很多別人的提交一起（a96690d8 等）；推之前單獨列 `origin/main..main`、點名。

### 未解的線
- 「滑鼠滾輪捲不動」本小姐在 Chrome 從沒重現過；統一成城鎮面板後滾輪實測可以。Tim 若還說捲不動，問他用哪個瀏覽器／裝置。
- 量記憶體的工具都在 scratchpad：memprof.cjs（CDP＋iPhone 模擬）、memprobe.js、snapan.cjs（heap 快照拆帳）、portcmp.cjs（44 型砲門對拍）、ovserve.py（共用樹只換幾個檔）。記憶 blockside-ram-breakdown 有讀數。
- 匯入檢查那兩條非燈的（fort_roche 酒桶披屋、battery_en 抽水機）仍不在任何單上；TASK-1188 照舊不碰。
- launch.json 本小姐的條目都拿掉了；worktree 全砍了。

### 撞到的坑
- bash heredoc 又吞了兩次跳脫（`\\uFE0F`、`\\n`）——寫 JS／Python 一律用 Write 寫檔或 Edit，不用 heredoc。
- 量效能時筆電越跑越熱：連沒改到的 phys 都 37→64 ms ⇒ 比「畫面／模擬」的比例，不比毫秒。
- 上一個 session 中斷時背景指令被砍，Tim 問「是否還在跑」——中斷後先查檔案與行程，照實說沒在跑。

### 心境
今天三次照實講：圖示那個不是錨本身、35 MB 高峰是我看錯、bufferSubData 我算錯成 135 MB/s。每次更正都很不想說，但說了之後 Tim 選得更快。還有一次是 Tim 把我拉出選項外：我在修全版面的視窗，他說「整合成一種就好」。……下次先問自己：這兩份為什麼要並存。

