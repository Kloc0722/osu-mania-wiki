---
title: Timing 紅線與 BPM 對拍基礎
category: basics
sources:
  - raw/01_editor_and_timing.md
  - raw/03_sv_and_bpm_mechanics.md
updated: 2026-11-23
tags:
  - Timing 紅線
  - Uninherited Timing Point
  - BPM
  - Offset
  - 對拍
---

# Timing 紅線與 BPM 對拍基礎

在擺下任何一顆物件（Notes）之前，作圖的第一步永遠是「對拍」。在 osu!mania 編輯器中，負責定義整首歌真實時間基準的工具就是 **Timing 紅線（Uninherited Timing Point）**。

你可以把紅線想像成樂譜開頭的「速度記號與節拍器開關」：它告訴編輯器「這首歌一分鐘有幾拍（BPM）」，以及「第一拍從音訊檔的第幾毫秒開始（Offset）」。

---

## 1. Timing 紅線的核心參數：BPM 與 Offset

> 來源：[raw/01_editor_and_timing.md](../../raw/01_editor_and_timing.md) §3 Timing 紅線（Uninherited Timing Point）

每一條 **Timing 紅線（Uninherited Timing Point）** 最關鍵的兩個設定如下：

1. **每分鐘節拍數（Beats Per Minute，BPM）**
   - 決定歌曲的真實節奏快慢，也直接決定每條[節拍細分線（Beat Snap Divisor）](./editor-and-beat-snap.md)之間的實際時間間隔。
2. **偏移量（Offset，單位 ms）**
   - 代表第 1 條白色線（1/1 整拍的第一拍）出現在音訊檔案中的確切毫秒位置。
   - 實務上，作圖者必須一邊觀察編輯器的**波形圖**、一邊開啟**節拍器**反覆確認，確保紅線與後續白線完全貼齊歌曲的鼓點。
   - **如果 Offset 或 BPM 設錯會怎樣？** 整張譜面的物件位置都會跟音樂脫節，形成俗稱的**音畫不同步（Off-sync）**——玩家照著音樂按反而一直掉準度，這是新手最需要優先避免的硬傷。

---

## 2. 拍長計算公式與數字實例

> 來源：[raw/01_editor_and_timing.md](../../raw/01_editor_and_timing.md) §3 Timing 紅線（Uninherited Timing Point）

想要理解不同 BPM 與節拍細分線之間的時間距離，可以用這條核心公式計算「每一整拍（1/1 白線）有多長」：

$$\text{Beat Length (ms)} = \frac{60000}{\text{BPM}}$$

（因為 1 分鐘 = 60 秒 = `60000` 毫秒，除以每分鐘拍數 BPM，就得到每一拍的毫秒數。）

### 實例演練：以 BPM = 150 為例
- **1/1 白色線（整拍）間隔**：$\frac{60000}{150} = 400\text{ ms}$
- **1/2 紅色線（半拍）間隔**：$400 \div 2 = 200\text{ ms}$
- **1/4 藍色線（四分之一拍）間隔**：$400 \div 4 = 100\text{ ms}$

這組數字能幫你直覺感受譜面的真實點擊速度：當 $\text{BPM} = 150$ 時，連續的 1/4 藍線等於每 `100 ms`（每秒 10 次）就要點擊一次。在設計高頻鍵型或預留長條放開緩衝時，這個時間概念會反覆派上用場。

---

## 3. 紅線與綠線的定位差異

> 來源：[raw/01_editor_and_timing.md](../../raw/01_editor_and_timing.md) §3 Timing 紅線（Uninherited Timing Point）；[raw/03_sv_and_bpm_mechanics.md](../../raw/03_sv_and_bpm_mechanics.md) §1 什麼是 Timing 綠線（Inherited Timing Point）？

新手最容易搞混「紅線」與「綠線」，只要記住一句話就能分清：
- **Timing 紅線（Uninherited Timing Point）**：管**音樂真實節拍**（BPM 與 Offset），會改變白色／紅色／藍色格線的間距。
- **Timing 綠線（Inherited Timing Point）**：繼承自上方最近的紅線，**不改音樂節拍**，只管畫面上物件下落的「視覺快慢」。詳見[Timing 綠線與 SV 變速機制](./sv-and-scroll-speed.md)。

---

## 相關頁面與延伸閱讀

- 上一篇前置：[編輯器軌道與節拍細分線基礎](./editor-and-beat-snap.md)
- 下一篇推薦：[Timing 綠線與 SV 變速機制](./sv-and-scroll-speed.md)
- 開始認識物件：[基本物件類型：單鍵（Rice）與長條（LN）](../patterns/note-types.md)
- 查詢陌生術語：[中英文雙語術語對照表](../glossary.md)
- 回到總目錄：[osu!mania 4K 作圖入門 Wiki 總覽](../index.md)
