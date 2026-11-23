---
title: osu!mania 4K 作圖入門 Wiki 總覽
category: meta
sources:
  - raw/01_editor_and_timing.md
  - raw/02_note_types_and_patterns.md
  - raw/03_sv_and_bpm_mechanics.md
  - raw/04_ranking_criteria_4k.md
  - raw/05_modding_and_playability.md
updated: 2026-11-23
tags:
  - index
  - osu!mania
  - 4K
  - 作圖入門
---

# osu!mania 4K 作圖入門 Wiki 總覽

歡迎來到 **osu!mania 4K 作圖入門** 知識庫！本 Wiki 專為**完全零基礎的新手玩家**設計，將所有作圖核心概念、鍵型術語、官方規範與審圖避雷原則，依主題系統化整理並統一採**中英文雙語並列**撰寫。

---

## 新手建議閱讀路線（從零到完成第一張譜面）

如果你是第一次接觸作圖，建議照以下順序一步步讀完：

1. 先認識軌道與格線：[編輯器軌道與節拍細分線基礎](./basics/editor-and-beat-snap.md)
2. 學會對拍打地基：[Timing 紅線與 BPM 對拍基礎](./basics/timing-and-bpm.md)
3. 認識視覺變速機制：[Timing 綠線與 SV 變速機制](./basics/sv-and-scroll-speed.md)
4. 認識兩種基本物件：[基本物件類型：單鍵（Rice）與長條（LN）](./patterns/note-types.md)
5. 學看鍵型與手感：[4K 基礎鍵型圖鑑：同時按壓與連續移動](./patterns/chord-and-stream-patterns.md)
6. 掌握官方基準與避雷：[官方 Ranking Criteria（RC）核心規範](./standards/ranking-criteria.md) → [常見審圖（Modding）退件地雷與可玩性原則](./standards/modding-pitfalls.md)
7. 實際動手與自檢：[零基礎 4K 作圖起步 5 步驟路線圖](./guides/beginner-mapping-roadmap.md) → [送審前自我檢核清單](./guides/pre-mod-checklist.md)

> 閱讀過程中遇到任何陌生詞彙，隨時可以跳到[中英文雙語術語對照表](./glossary.md)反查。

---

## 主題分類目錄

### 1. 編輯器與時間軸基礎（`basics/`）
- [編輯器軌道與節拍細分線基礎](./basics/editor-and-beat-snap.md) — 4K 軌道鍵位（`D/F/J/K`）、`.osu` X 座標（`64/192/320/448`）與白／紅／藍／紫／黃／橘節拍細分線。
- [Timing 紅線與 BPM 對拍基礎](./basics/timing-and-bpm.md) — Timing 紅線（Uninherited Timing Point）、拍長計算公式 `60000 / BPM`、偏移量（Offset）與避免音畫不同步。
- [Timing 綠線與 SV 變速機制](./basics/sv-and-scroll-speed.md) — Timing 綠線（Inherited Timing Point）、有效下落速度公式、速度標準化（Normalize）與變速特效（SV Effects）。

### 2. 物件與 4K 鍵型圖鑑（`patterns/`）
- [基本物件類型：單鍵（Rice）與長條（LN）](./patterns/note-types.md) — Rice 與 Long Note 結構差異、放開時機（Release Timing）判定、禁止重疊與尾端緩衝原則。
- [4K 基礎鍵型圖鑑：同時按壓與連續移動](./patterns/chord-and-stream-patterns.md) — Single / Jump / Hand / Quad 四階密度，以及 Stream / Trill / Jack / Long Jack 連續移動鍵型。

### 3. 官方規範與審圖原則（`standards/`）
- [osu!mania 4K 官方 Ranking Criteria（RC）核心規範](./standards/ranking-criteria.md) — 依有效遊玩時間（Drain Time）劃分的難度組結構、最低 100 物件與 30 秒限制，以及 Easy 至 Expert 難度定位。
- [常見審圖（Modding）退件地雷與可玩性原則](./standards/modding-pitfalls.md) — 過度堆疊（Overmapping）、採音不一致、不合理手部負擔與難度斷層（Difficulty Spike）的診斷與修正。

### 4. 新手實戰指南（`guides/`）
- [零基礎 4K 作圖起步 5 步驟路線圖](./guides/beginner-mapping-roadmap.md) — 整合全站概念的 5 步驟實作藍圖，帶新手從空白音訊完成第一張可玩譜面。
- [送審前自我檢核清單（Pre-Mod Checklist）](./guides/pre-mod-checklist.md) — 提交審圖（Modding）前必查的 Timing／SV、RC 硬性門檻與可玩性核對表。

---

## 知識庫中樞與維護檔案

- [中英文雙語術語對照表（Glossary）](./glossary.md) — 全站統一譯名基準與速查表。
- [知識庫維護與操作日誌（Log）](./log.md) — 記錄每次 Ingest、更新、Lint 檢查與簡報產出歷史。
- [專案操作規範（AGENTS.md）](../AGENTS.md) — 本 LLM Wiki 的編譯、出處、Lint 與 HTML 簡報產出標準。
