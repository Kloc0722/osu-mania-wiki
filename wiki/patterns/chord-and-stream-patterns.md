---
title: 4K 基礎鍵型圖鑑：同時按壓與連續移動
category: patterns
sources:
  - raw/02_note_types_and_patterns.md
  - raw/04_ranking_criteria_4k.md
  - raw/05_modding_and_playability.md
updated: 2026-11-23
tags:
  - Chord Patterns
  - Single
  - Jump
  - Hand
  - Quad
  - Stream
  - Trill
  - Jack
  - Long Jack
---

# 4K 基礎鍵型圖鑑：同時按壓與連續移動

學會[單鍵（Rice）與長條（Long Note，LN）](./note-types.md)後，當多個物件（Notes）在「同一時間點」或「連續拍點」上排列組合時，就會形成各種不同的**鍵型（Patterns）**。熟悉這些基礎術語，能幫你精準控制譜面的手感與難度。

以下示意圖中，`1 2 3 4` 代表由左至右的 4 條軌道（Column 1–4），`O` 代表物件，時間由下往上依序出現（最下方先按）。

---

## 1. 同時按壓類鍵型（Chord Patterns）

> 來源：[raw/02_note_types_and_patterns.md](../../raw/02_note_types_and_patterns.md) §2 同時按壓類鍵型（Chord Patterns）

依照**同一時間點**出現的物件數量，4K 的多押密度（Chord 密度）分為 4 個由弱到強的階梯：

| 鍵型（雙語） | 同時間物件數 | 4K 軌道示意 | 音樂表現與使用時機 |
| :--- | :---: | :---: | :--- |
| **單點（Single）** | `1` | `O . . .` | 適合呈現單音旋律、平緩段落或入門難度。 |
| **雙押（Jump）** | `2` | `O . O .` | 用於強調重拍（例如底鼓配小鼓）或和弦主音。 |
| **三押（Hand）** | `3` | `O O . O` | 需單手同時按兩鍵、另一手按一鍵；常見於高潮副歌或重音爆發。 |
| **四押（Quad）** | `4` | `O O O O` | 4 條軌道全滿，為最高強度的重音強調；在入門與進階難度應謹慎使用。 |

> **給零基礎新手的直覺口訣**：同時按的鍵越多，代表這一拍在音樂裡的「重量與音量」越大。把單點（Single）當日常說話、雙押（Jump）當加重語氣、三押（Hand）當吶喊、四押（Quad）當全場最炸的一拍，就能自然搭配歌曲能量。

---

## 2. 連續移動類鍵型（Stream & Jack Patterns）

> 來源：[raw/02_note_types_and_patterns.md](../../raw/02_note_types_and_patterns.md) §3 連續移動類鍵型（Stream & Jack Patterns）

當物件連續出現在密集的[節拍細分線（Beat Snap Divisor）](../basics/editor-and-beat-snap.md)（例如 1/4 藍色線）上時，依照軌道的排列方式可分為三種基本型態：

### 交互連打（Stream）
- **特徵**：物件在連續拍點上於**不同軌道**之間交替移動（像是樓梯或左右切換）。
- **手感重點**：玩家透過左右手輪流點擊完成，考驗手指協調性與讀譜流暢度。
- **軌道範例**（由下往上依序按下 `1 → 2 → 3 → 4`）：
  ```text
  . . . O   (第 4 拍點)
  . . O .   (第 3 拍點)
  . O . .   (第 2 拍點)
  O . . .   (第 1 拍點)
  ```

### 雙鍵交互（Trill）
- **特徵**：物件在**兩條固定軌道**之間快速來回交替（例如 `1-2-1-2` 或 `2-3-2-3`），像鋼琴的震音。
- **軌道範例**（`2-3-2-3`，左右手食指輪流點）：
  ```text
  . . O .   (第 4 拍點)
  . O . .   (第 3 拍點)
  . . O .   (第 2 拍點)
  . O . .   (第 1 拍點)
  ```

### 同軌連打（Jack）與長縱連（Long Jack）
- **同軌連打（Jack）**：物件在連續拍點上重複出現在**同一條軌道**（例如 `1-1-1`），考驗單指的爆發力與耐力。
- **長縱連（Long Jack）**：連續超過 **3 個以上**的快速同軌連打（例如 4 連同軌 `1-1-1-1`）。這類配置對新手極度不友好，在入門譜面中務必盡量避免。
- **軌道範例**（`1-1-1`）：
  ```text
  O . . .   (第 3 拍點)
  O . . .   (第 2 拍點)
  O . . .   (第 1 拍點)
  ```

---

## 3. 各難度配置上限與手感避雷

> 來源：[raw/04_ranking_criteria_4k.md](../../raw/04_ranking_criteria_4k.md) §3 難度分級定位標準（4K 基準）；[raw/05_modding_and_playability.md](../../raw/05_modding_and_playability.md) §1 過度堆疊（Overmapping）、§3 不合理的手部負擔（Unplayable Patterns）

把上述鍵型放進實際譜面時，請同時對照以下設計界線：
- **難度階梯對應**：`Easy` 以單點（Single）為主、嚴禁密集雙押；`Normal` 允許在重拍配置簡單雙押（Jump）；`Hard` 引入基礎交互連打（Stream）；`Insane / Expert` 才全面使用三押（Hand）、四押（Quad）與高速連打。
- **符合音樂能量對等原則（Intensity Matching）**：多押密度（Chord 密度）須跟隨音量與樂器多寡變化，不要在平緩段塞入高密度鍵型造成**過度堆疊（Overmapping）**。
- **維持左右手平衡（Hand Bias 平衡）**：高速 1/4 藍色線上應避免安排 4 個以上的**長縱連（Long Jack）**，改用交互切換分散單手壓力。

---

## 相關頁面與延伸閱讀

- 上一篇前置：[基本物件類型：單鍵（Rice）與長條（LN）](./note-types.md)
- 深入規範與避雷：[官方 Ranking Criteria（RC）核心規範](../standards/ranking-criteria.md)、[常見審圖（Modding）退件地雷與可玩性原則](../standards/modding-pitfalls.md)
- 理解細分拍點時間距離：[Timing 紅線與 BPM 對拍基礎](../basics/timing-and-bpm.md)
- 查詢陌生術語：[中英文雙語術語對照表](../glossary.md)
- 回到總目錄：[osu!mania 4K 作圖入門 Wiki 總覽](../index.md)
