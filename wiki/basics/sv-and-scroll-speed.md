---
title: Timing 綠線與 SV 變速機制
category: basics
sources:
  - raw/03_sv_and_bpm_mechanics.md
updated: 2026-11-23
tags:
  - Timing 綠線
  - Inherited Timing Point
  - SV
  - Slider Velocity
  - Normalize
---

# Timing 綠線與 SV 變速機制

搞懂掌控音樂真實拍點的[Timing 紅線（Uninherited Timing Point）](./timing-and-bpm.md)之後，你會在編輯器裡看到另一種線——**Timing 綠線（Inherited Timing Point）**。它跟音樂本身有沒有變快無關，而是專門控制「物件在螢幕上掉下來的視覺速度」。

---

## 1. 什麼是 Timing 綠線（Inherited Timing Point）？

> 來源：[raw/03_sv_and_bpm_mechanics.md](../../raw/03_sv_and_bpm_mechanics.md) §1 什麼是 Timing 綠線（Inherited Timing Point）？

**Timing 綠線（Inherited Timing Point）**會繼承它上方最近那一條 Timing 紅線的節拍設定：
- **它不會改變音樂的 BPM**，也不會改變任何節拍細分線的時間點。
- 它的唯一任務，就是調整**視覺下落速度倍率（Slider Velocity，簡稱 SV）**，讓物件在畫面上看起來移動得比較快或比較慢。

> **白話比喻**：歌曲的拍子就像火車準點進站的時間表（紅線決定），而 SV 則是你把火車軌道的畫面放大或縮小來看（綠線決定）。無論你把 SV 調成 `0.50x` 或 `2.00x`，玩家按下按鍵的**正確毫秒時刻完全不變**，改變的只是物件「掉下來的視覺距離感」。

---

## 2. 有效下落速度（Effective Scroll Speed）公式

> 來源：[raw/03_sv_and_bpm_mechanics.md](../../raw/03_sv_and_bpm_mechanics.md) §2 有效下落速度公式

在 osu!mania 中，綠線的 **SV 倍率**可調整範圍為 **`0.10x` 至 `10.00x`**，預設值為 **`1.00x`**。物件在螢幕上呈現的實際視覺速度，由以下公式決定：

$$\text{Effective Scroll Speed} = \text{Base BPM} \times \text{SV Multiplier}$$

### 數字實例：以基準 BPM = 180 為例
| 情境 | 綠線 SV 倍率 | 有效下落速度 | 畫面視覺效果 |
| :--- | :---: | :---: | :--- |
| 預設狀態 | `1.00x` | 等同 `BPM 180` | 正常間距 |
| 插入低速綠線 | `0.50x` | $180 \times 0.50 = 90$（等同 `BPM 90`） | 下落速度減半，物件間距縮短、看起來**變密集（低速段）** |
| 插入高速綠線 | `2.00x` | $180 \times 2.00 = 360$（等同 `BPM 360`） | 下落速度加倍，物件間距拉大、看起來**變稀疏（高速段）** |

---

## 3. SV 的兩大實務用途

> 來源：[raw/03_sv_and_bpm_mechanics.md](../../raw/03_sv_and_bpm_mechanics.md) §3 SV 的兩大實務用途

### 用途一：速度標準化（Normalize）／恆定下落速度（Constant Scroll Speed）
有些歌曲本身會變速——例如主歌是 `BPM 120`，進副歌時突然加速到 `BPM 180`。
- **如果不加綠線**：副歌的紅線會讓物件下落速度瞬間變成原本的 1.5 倍，玩家容易措手不及。
- **使用速度標準化（Normalize）的做法**：在 `BPM 180` 紅線的**同一毫秒**位置，疊加一條綠線，將 SV 設為：
  $$\text{SV} = \frac{120}{180} \approx 0.67\text{x}$$
  如此一來，$180 \times 0.67 \approx 120$，整首曲子的視覺下落速度就能維持恆定，保障流暢的讀譜體驗。

### 用途二：變速特效（SV Effects）
作圖者也可以刻意運用高低倍率的綠線，配合音樂的驟停（Stop）、漸快（Accelerando）或重低音衝擊，製造強烈的視覺張力。

> **給零基礎新手的建議**：入門譜面應優先把 SV 用在「多段變速曲的速度標準化（Normalize）」，**避免過度使用劇烈的變速特效（SV Effects）**，以免干擾玩家的基礎讀譜判斷。

---

## 相關頁面與延伸閱讀

- 上一篇前置：[Timing 紅線與 BPM 對拍基礎](./timing-and-bpm.md)
- 認識物件與鍵型：[基本物件類型：單鍵（Rice）與長條（LN）](../patterns/note-types.md)
- 查詢陌生術語：[中英文雙語術語對照表](../glossary.md)
- 回到總目錄：[osu!mania 4K 作圖入門 Wiki 總覽](../index.md)
