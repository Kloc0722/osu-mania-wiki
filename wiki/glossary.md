---
title: 中英文雙語術語對照表（Glossary）
category: meta
sources:
  - raw/01_editor_and_timing.md
  - raw/02_note_types_and_patterns.md
  - raw/03_sv_and_bpm_mechanics.md
  - raw/04_ranking_criteria_4k.md
  - raw/05_modding_and_playability.md
updated: 2026-11-23
tags:
  - glossary
  - 術語表
  - 雙語對照
---

# 中英文雙語術語對照表（Glossary）

本頁為『osu!mania 4K 作圖入門』Wiki 的**唯一雙語譯名基準**。全站所有專有名詞皆依本表採「中文（英文／縮寫）」雙語並列格式撰寫，方便零基礎新手對照編輯器介面與國際社群討論。

---

## 1. 編輯器與 Timing 基礎術語

> 來源：[raw/01_editor_and_timing.md](../raw/01_editor_and_timing.md) §1–§3

| 標準雙語寫法 | 白話解釋 | 詳見頁面 |
| :--- | :--- | :--- |
| **軌道（Column）** | 4K 模式由左至右的 4 條垂直下落軌（Column 1–4，X 座標 `64/192/320/448`）。 | [編輯器與節拍細分線](./basics/editor-and-beat-snap.md) |
| **物件（Notes）** | 沿著軌道向下移動、需依節奏點擊或按住的遊戲元素統稱。 | [基本物件類型](./patterns/note-types.md) |
| **判定線（Judgement Line）** | 位於軌道底部的基準線，物件抵達此線時按下／放開即判定準度。 | [編輯器與節拍細分線](./basics/editor-and-beat-snap.md) |
| **節拍細分線（Beat Snap Divisor）** | 時間軸上代表拍點細分刻度的彩色水平線（白 1/1、紅 1/2、藍 1/4、紫 1/3、黃 1/6、橘 1/8）。 | [編輯器與節拍細分線](./basics/editor-and-beat-snap.md) |
| **Timing 紅線（Uninherited Timing Point）** | 決定歌曲真實速度（BPM）與對拍起點（Offset）的時間基準線。 | [Timing 紅線與 BPM](./basics/timing-and-bpm.md) |
| **每分鐘節拍數（Beats Per Minute，BPM）** | 歌曲每分鐘包含的拍數，拍長計算公式為 `60000 / BPM`（ms）。 | [Timing 紅線與 BPM](./basics/timing-and-bpm.md) |
| **偏移量（Offset）** | 第一條白色線（第一拍）在音訊檔案中出現的時間位置（單位 ms）。 | [Timing 紅線與 BPM](./basics/timing-and-bpm.md) |
| **音畫不同步（Off-sync）** | 紅線未貼齊音樂鼓點，導致物件時間點與音樂聽感脫節的現象。 | [Timing 紅線與 BPM](./basics/timing-and-bpm.md) |

---

## 2. 綠線與 SV 變速術語

> 來源：[raw/03_sv_and_bpm_mechanics.md](../raw/03_sv_and_bpm_mechanics.md) §1–§3

| 標準雙語寫法 | 白話解釋 | 詳見頁面 |
| :--- | :--- | :--- |
| **Timing 綠線（Inherited Timing Point）** | 繼承上方最近紅線的輔助線，不改真實 BPM，只控制視覺下落速度倍率。 | [Timing 綠線與 SV](./basics/sv-and-scroll-speed.md) |
| **視覺下落速度倍率（Slider Velocity，SV）** | 綠線用來調整下落快慢的倍率參數，可調範圍為 `0.10x` 至 `10.00x`（預設 `1.00x`）。 | [Timing 綠線與 SV](./basics/sv-and-scroll-speed.md) |
| **有效下落速度（Effective Scroll Speed）** | 實際視覺移動速度，公式為 `Base BPM × SV Multiplier`。 | [Timing 綠線與 SV](./basics/sv-and-scroll-speed.md) |
| **速度標準化（Normalize）** | 歌曲變速時，在新紅線同一毫秒處疊加綠線以抵銷視覺加速的技巧。 | [Timing 綠線與 SV](./basics/sv-and-scroll-speed.md) |
| **恆定下落速度（Constant Scroll Speed）** | 透過速度標準化讓整首變速曲維持一致的視覺下落速度。 | [Timing 綠線與 SV](./basics/sv-and-scroll-speed.md) |
| **變速特效（SV Effects）** | 配合驟停（Stop）、漸快（Accelerando）等音樂張力刻意製造的高低速視覺效果。 | [Timing 綠線與 SV](./basics/sv-and-scroll-speed.md) |

---

## 3. 物件類型與 4K 鍵型術語

> 來源：[raw/02_note_types_and_patterns.md](../raw/02_note_types_and_patterns.md) §1–§3

| 標準雙語寫法 | 白話解釋 | 詳見頁面 |
| :--- | :--- | :--- |
| **單鍵（Rice）** | 俗稱米粒，抵達判定線時按下一次即可完成判定的基本物件。 | [基本物件類型](./patterns/note-types.md) |
| **長條（Long Note，LN）** | 具有起點（Head）與終點（Tail）的持續性物件，須按住直到終點才放開。 | [基本物件類型](./patterns/note-types.md) |
| **起點（Head）／終點（Tail）** | 長條物件的開頭按下位置與結尾放開位置。 | [基本物件類型](./patterns/note-types.md) |
| **放開時機（Release Timing）** | 長條終點放開按鍵的準度，過早或過晚放開都會導致判定降級。 | [基本物件類型](./patterns/note-types.md) |
| **同時按壓類鍵型（Chord Patterns）** | 依同一時間點同時出現的物件數量分類的鍵型統稱（單點至四押）。 | [4K 基礎鍵型圖鑑](./patterns/chord-and-stream-patterns.md) |
| **多押密度（Chord 密度）** | 同一時間點要求同時按下的按鍵數量密集程度。 | [4K 基礎鍵型圖鑑](./patterns/chord-and-stream-patterns.md) |
| **單點（Single）** | 同一時間點只有 `1` 個物件。 | [4K 基礎鍵型圖鑑](./patterns/chord-and-stream-patterns.md) |
| **雙押（Jump）** | 同一時間點同時出現 `2` 個物件。 | [4K 基礎鍵型圖鑑](./patterns/chord-and-stream-patterns.md) |
| **三押（Hand）** | 同一時間點同時出現 `3` 個物件（單手按兩鍵、另一手按一鍵）。 | [4K 基礎鍵型圖鑑](./patterns/chord-and-stream-patterns.md) |
| **四押（Quad）** | 同一時間點 4 條軌道全滿（`4` 個物件）。 | [4K 基礎鍵型圖鑑](./patterns/chord-and-stream-patterns.md) |
| **連續移動類鍵型（Stream & Jack Patterns）** | 物件在連續細分拍點上依不同軌道排列延伸出的連打型態。 | [4K 基礎鍵型圖鑑](./patterns/chord-and-stream-patterns.md) |
| **交互連打（Stream）** | 物件在連續拍點上於不同軌道交替出現，由左右手輪流點擊完成。 | [4K 基礎鍵型圖鑑](./patterns/chord-and-stream-patterns.md) |
| **雙鍵交互（Trill）** | 物件在兩條固定軌道之間快速來回交替（如 `1-2-1-2`、`2-3-2-3`）。 | [4K 基礎鍵型圖鑑](./patterns/chord-and-stream-patterns.md) |
| **同軌連打（Jack）** | 物件在連續拍點上重複出現在同一條軌道（如 `1-1-1`），俗稱縱連。 | [4K 基礎鍵型圖鑑](./patterns/chord-and-stream-patterns.md) |
| **長縱連（Long Jack）** | 連續超過 3 個以上（即 4 個以上）的快速同軌連打，對新手負擔極高。 | [4K 基礎鍵型圖鑑](./patterns/chord-and-stream-patterns.md) |

---

## 4. 官方規範與審圖（Modding）術語

> 來源：[raw/04_ranking_criteria_4k.md](../raw/04_ranking_criteria_4k.md) §1–§3；[raw/05_modding_and_playability.md](../raw/05_modding_and_playability.md) §1–§4

| 標準雙語寫法 | 白話解釋 | 詳見頁面 |
| :--- | :--- | :--- |
| **官方上架標準（Ranking Criteria，RC）** | osu! 官方針對上架（Ranked）譜面訂定的品質與公平性硬性規範。 | [官方 RC 核心規範](./standards/ranking-criteria.md) |
| **譜面集（Beatmapset）** | 同一首歌曲底下的整組難度集合。 | [官方 RC 核心規範](./standards/ranking-criteria.md) |
| **難度組結構（Spread Requirements）** | 官方依據有效遊玩時間規定譜面集必須包含的最少難度數與最低難度等級。 | [官方 RC 核心規範](./standards/ranking-criteria.md) |
| **有效遊玩時間（Drain Time）** | 扣除歌曲前奏與間奏空白後的實際遊玩時長。 | [官方 RC 核心規範](./standards/ranking-criteria.md) |
| **審圖（Modding）** | 將譜面初稿交由其他作圖者檢視並提出修正建議的同儕審查流程。 | [常見審圖退件地雷](./standards/modding-pitfalls.md) |
| **過度堆疊（Overmapping）** | 在平緩音樂段落強塞密集拍點或多押，使譜面密度遠超音樂能量。 | [常見審圖退件地雷](./standards/modding-pitfalls.md) |
| **音樂能量對等原則（Intensity Matching）** | 物件數量與多押密度須隨樂器層次與音量起伏同步變化的設計原則。 | [常見審圖退件地雷](./standards/modding-pitfalls.md) |
| **採音不一致（Inconsistent Hitsounding / Layering）** | 相同旋律或鼓點重複出現時，前後採音規則不統一造成玩家混亂。 | [常見審圖退件地雷](./standards/modding-pitfalls.md) |
| **採音層次（Layering）** | 事前規劃各難度要對應採集哪些聲音元素（如人聲主旋律、小鼓）的規則。 | [常見審圖退件地雷](./standards/modding-pitfalls.md) |
| **不合理的手部負擔（Unplayable Patterns）** | 超出合理負荷的配置，如高速長縱連或長條期間同手釋放衝突。 | [常見審圖退件地雷](./standards/modding-pitfalls.md) |
| **左右手平衡（Hand Bias 平衡）** | 透過左右手交替分散壓力，避免單手連續超負荷點擊的原則。 | [常見審圖退件地雷](./standards/modding-pitfalls.md) |
| **難度斷層（Difficulty Spike）** | 譜面大多數區段維持某難度，卻在局部突然飆升數個等級的失衡現象。 | [常見審圖退件地雷](./standards/modding-pitfalls.md) |
| **最高難度段落（Peak）** | 整張譜面中密度或技巧要求最高的區段，應與該難度整體定位一致。 | [常見審圖退件地雷](./standards/modding-pitfalls.md) |

---

## 相關頁面與延伸閱讀

- 回到總目錄：[osu!mania 4K 作圖入門 Wiki 總覽](./index.md)
- 新手從頭開始：[零基礎 4K 作圖起步 5 步驟路線圖](./guides/beginner-mapping-roadmap.md)
