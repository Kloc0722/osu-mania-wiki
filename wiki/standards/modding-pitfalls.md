---
title: 常見審圖（Modding）退件地雷與可玩性原則
category: standards
sources:
  - raw/05_modding_and_playability.md
updated: 2026-11-23
tags:
  - Modding
  - 審圖
  - Overmapping
  - Layering
  - Hand Bias
  - Difficulty Spike
---

# 常見審圖（Modding）退件地雷與可玩性原則

把譜面初稿做完後，下一個成長最快的方式就是交給其他作圖者進行**審圖（Modding）**，由對方提出手感、採音與規範上的修改建議。以下整理新手最容易踩中的四大退件地雷與對應的修正原則，只要在作圖當下就避開，就能省下大量重工時間。

---

## 1. 過度堆疊（Overmapping）

> 來源：[raw/05_modding_and_playability.md](../../raw/05_modding_and_playability.md) §1 過度堆疊（Overmapping）

- **常見問題**：在音樂很平緩、安靜的段落（例如純鋼琴前奏或人聲清唱）強行塞滿密集的 1/4 藍色線，或硬放**三押（Hand）**、**四押（Quad）**，導致譜面的壓迫感遠遠超過音樂本身的能量。
- **修正原則——音樂能量對等原則（Intensity Matching）**：
  - 物件數量與同時按壓數（**多押密度，Chord 密度**）必須隨著樂器層次與音量起伏同步變化。
  - 安靜段落用**單點（Single）**與疏鬆拍點，副歌高潮再把密度拉高，整張譜面才會有呼吸感與情緒張力。

---

## 2. 採音不一致（Inconsistent Hitsounding / Layering）

> 來源：[raw/05_modding_and_playability.md](../../raw/05_modding_and_playability.md) §2 採音不一致（Inconsistent Hitsounding / Layering）

- **常見問題**：歌曲中明明出現完全相同的鼓點或副歌主旋律，第一次作圖者採在 1/4 拍、第二次重複時卻漏採或突然跑去採另一種樂器，會讓玩家感到混亂與困惑。
- **修正原則——預先規劃採音層次（Layering）**：
  - 在開始擺物件之前，先幫這個難度訂好「我要採哪些聲音」。
  - 例如：低難度（`Easy` / `Normal`）規定**只採人聲主旋律**；較高難度則固定為**「主旋律＋小鼓（Snare）」**，全曲前後維持同一套邏輯。

---

## 3. 不合理的手部負擔（Unplayable Patterns）

> 來源：[raw/05_modding_and_playability.md](../../raw/05_modding_and_playability.md) §3 不合理的手部負擔（Unplayable Patterns）

- **常見問題**：
  1. 在高速 1/4 藍色線中，連續安排 **4 個以上**的**同軌連打（Jack）**——即**長縱連（Long Jack）**，逼迫單指承受過高負荷。
  2. 在**長條（Long Note，LN）**按住期間，於同一隻手負責的另一條軌道塞進過度密集的單鍵（Rice），造成手指釋放與點擊打架（釋放衝突）。
- **修正原則**：
  1. **左右手平衡（Hand Bias 平衡）**：透過左右手輪流交替分散點擊壓力，避免單手連續承受超出體能負荷的高頻連點。
  2. **LN 尾端緩衝空間**：在長條（LN）的終點（Tail）之後，應預留至少 **1/4 拍**（若歌曲 BPM 較高，建議預留 **1/2 拍**）的空白緩衝，再接同一條軌道的下一個單鍵（Rice）。

---

## 4. 難度斷層（Difficulty Spike）

> 來源：[raw/05_modding_and_playability.md](../../raw/05_modding_and_playability.md) §4 難度斷層（Difficulty Spike）

- **常見問題**：整張譜面有 90% 都是輕鬆的 1/2 拍單點（符合 `Normal` 水準），卻在副歌最後 4 個小節突然塞入高速 1/4 拍雙押連打（瞬間飆升到 `Hard` 甚至 `Insane` 水準），害原本打得順手的玩家在結尾突然爆掉。
- **修正原則——控管最高難度段落（Peak）上限**：
  - 每個難度在動工前都應明確對照[官方 Ranking Criteria（RC）難度分級](./ranking-criteria.md)設定技術上限。
  - 整張譜面的**最高難度段落（Peak）**可以略高於平均強度，但必須始終落在該難度的整體定位之內。

---

## 相關頁面與延伸閱讀

- 前置規範：[osu!mania 4K 官方 Ranking Criteria（RC）核心規範](./ranking-criteria.md)
- 實際應用清單：[送審前自我檢核清單](../guides/pre-mod-checklist.md)
- 零基礎全流程：[零基礎 4K 作圖起步 5 步驟路線圖](../guides/beginner-mapping-roadmap.md)
- 檢視物件與鍵型限制：[基本物件類型：單鍵（Rice）與長條（LN）](../patterns/note-types.md)、[4K 基礎鍵型圖鑑](../patterns/chord-and-stream-patterns.md)
- 查詢陌生術語：[中英文雙語術語對照表](../glossary.md)
- 回到總目錄：[osu!mania 4K 作圖入門 Wiki 總覽](../index.md)
