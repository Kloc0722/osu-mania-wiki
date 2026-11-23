---
title: 知識庫維護與操作日誌（Log）
category: meta
sources:
  - raw/01_editor_and_timing.md
  - raw/02_note_types_and_patterns.md
  - raw/03_sv_and_bpm_mechanics.md
  - raw/04_ranking_criteria_4k.md
  - raw/05_modding_and_playability.md
updated: 2026-11-23
tags:
  - log
  - 維護日誌
  - ingest
  - lint
---

# 知識庫維護與操作日誌（Log）

本檔案依時間順序記錄所有對 `wiki/` 與 `slides/` 執行的 **Ingest（編入）**、**Update（更新）**、**Lint（健康檢查）** 與 **Export（簡報產出）** 操作。

---

## 2026-11-23

### 1. 初始化專案規範（Init）
- 建立 [AGENTS.md](../AGENTS.md)，確立零基礎受眾定位、主題式分類架構、雙語並列術語規範、章節層級出處標記、每次 2–3 篇 Ingest 節奏、4 大類 Lint 檢查規則，以及零依賴單一 HTML 簡報輸出規格。

### 2. Batch 1 Ingest（來源：`raw/01`、`raw/02`、`raw/03`）
- **處理來源**：
  - `raw/01_editor_and_timing.md`
  - `raw/02_note_types_and_patterns.md`
  - `raw/03_sv_and_bpm_mechanics.md`
- **建立頁面**：
  - [basics/editor-and-beat-snap.md](./basics/editor-and-beat-snap.md)
  - [basics/timing-and-bpm.md](./basics/timing-and-bpm.md)
  - [basics/sv-and-scroll-speed.md](./basics/sv-and-scroll-speed.md)
  - [patterns/note-types.md](./patterns/note-types.md)
  - [patterns/chord-and-stream-patterns.md](./patterns/chord-and-stream-patterns.md)

### 3. Batch 2 Ingest（來源：`raw/04`、`raw/05`）
- **處理來源**：
  - `raw/04_ranking_criteria_4k.md`
  - `raw/05_modding_and_playability.md`
- **建立頁面**：
  - [standards/ranking-criteria.md](./standards/ranking-criteria.md)
  - [standards/modding-pitfalls.md](./standards/modding-pitfalls.md)
  - [guides/beginner-mapping-roadmap.md](./guides/beginner-mapping-roadmap.md)
  - [guides/pre-mod-checklist.md](./guides/pre-mod-checklist.md)
- **增量更新與跨頁整合**：
  - 更新 [patterns/note-types.md](./patterns/note-types.md)：補入 RC 禁止 LN 尾端重疊規範與 Modding 尾端 1/4–1/2 拍緩衝原則。
  - 更新 [patterns/chord-and-stream-patterns.md](./patterns/chord-and-stream-patterns.md)：補入各難度鍵型上限、音樂能量對等原則與左右手平衡建議。
  - 更新 [basics/timing-and-bpm.md](./basics/timing-and-bpm.md)：補齊 Frontmatter 中對 `raw/03_sv_and_bpm_mechanics.md` 的來源標註。
- **同步中樞檔案**：
  - 建立 [index.md](./index.md)（主題目錄與零基礎閱讀路線）與 [glossary.md](./glossary.md)（收錄全站 42 組雙語對照術語）。

### 4. 初始 Lint 健康檢查（Lint）
- **結構與連結完整度**：通過（12 個 `wiki/` 檔案皆有完整 Frontmatter；0 斷連、0 孤兒頁、`index.md` 與 `log.md` 同步）。
- **來源與事實一致性**：通過（所有主題頁主要 `##` 小節均具備章節層級出處；Frontmatter `sources` 與內文引用 100% 一致；公式、座標與 RC 門檻數據均與 `raw/` 核對相符）。
- **雙語術語一致性**：通過（全站採「中文（英文／縮寫）」雙語並列，共 42 組術語集中收錄於 [glossary.md](./glossary.md)）。
- **新手可讀性與知識缺口**：
  - 現有 5 篇 `raw/` 內容已完整消化重組，無重複頁面或未解釋專有名詞。
  - **後續可擴充知識缺口建議**：① 音訊準備與新建譜面操作；② 打擊音效（Hitsounding）實作教學；③ 譜面上傳社群與請求審圖（Modding）禮儀。

### 5. 教學 HTML 簡報產出（Export）
- **單一內容來源**：僅使用 `wiki/`（涵蓋 11 份主題與索引頁）。
- **5 階段產物**：
  - 階段 1：[slides/sources.md](../slides/sources.md)、[slides/cards.md](../slides/cards.md)
  - 階段 2：[slides/outline.md](../slides/outline.md)（12 頁零基礎大綱，經人工確認通過）
  - 階段 3：[slides/drafts.md](../slides/drafts.md)（12 頁皆 ≤ 130 字且附 `來源：[[wiki/...]]`，針對 Slide 03 執行 1 輪局部精簡）
  - 階段 4：[slides/deck.html](../slides/deck.html)（零依賴單一 HTML 檔，12 頁內嵌 SVG 圖解，支援鍵盤翻頁，逐頁稿文字 0 處更動）
  - 階段 5：[slides/report.md](../slides/report.md)（完成逐頁文字一致、出處與 640p／720p 版面高度防溢出自檢，全數 PASS）

### 6. 簡報獨立事實審查修訂（Export Update）
- 依據獨立事實審查結果同步更新 [slides/drafts.md](../slides/drafts.md)、[slides/deck.html](../slides/deck.html) 與 [slides/report.md](../slides/report.md)：
  - 修正 Slide 06 將 RC 硬規定（LN 尾端禁重疊）與可玩性建議（尾端預留 1/4–1/2 拍緩衝）明確拆條。
  - 統一區分節拍細分「白色線／紅色線／藍色線」與「Timing 紅線」，補回 Slide 03 `4/4 拍` 前提與 Slide 05 `≈ 120` 約等號。
  - 補齊 Slide 09 各檔位最低難度要求與「僅 2 個難度時」前提，並依 [glossary.md](./glossary.md) 補全 Slide 09–10 雙語術語。
  - 補回 Slide 08／10／12 長縱連「快速／高速 1/4」限定詞，校正 SVG 文案並為全部 12 頁加上 `§` 小節與可點擊相對來源連結；複驗 0 差異、0 外部依賴、0 溢出。

---

## 相關頁面

- 回到總目錄：[osu!mania 4K 作圖入門 Wiki 總覽](./index.md)
- 查詢術語標準：[中英文雙語術語對照表](./glossary.md)
