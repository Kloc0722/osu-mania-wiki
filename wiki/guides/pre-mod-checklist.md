---
title: 送審前自我檢核清單（Pre-Mod Checklist）
category: guides
sources:
  - raw/01_editor_and_timing.md
  - raw/03_sv_and_bpm_mechanics.md
  - raw/04_ranking_criteria_4k.md
  - raw/05_modding_and_playability.md
updated: 2026-11-23
tags:
  - 檢核清單
  - Modding
  - Ranking Criteria
  - 自檢
---

# 送審前自我檢核清單（Pre-Mod Checklist）

把譜面交給他人進行**審圖（Modding）**之前，建議先花 5 分鐘逐項核對這份清單。提早抓出硬性違規與常見手感問題，能讓審圖者把時間花在更有價值的進階建議上。

---

## 1. Timing 紅線與 SV 綠線檢核

> 來源：[raw/01_editor_and_timing.md](../../raw/01_editor_and_timing.md) §3 Timing 紅線（Uninherited Timing Point）；[raw/03_sv_and_bpm_mechanics.md](../../raw/03_sv_and_bpm_mechanics.md) §2–§3

- [ ] 已透過波形圖與節拍器確認 **Timing 紅線（Uninherited Timing Point）** 的 BPM 與**偏移量（Offset）**完全貼齊鼓點，全曲無**音畫不同步（Off-sync）**。
- [ ] 若歌曲有多段變速，已在變速紅線的同一毫秒處疊加 **Timing 綠線（Inherited Timing Point）** 完成**速度標準化（Normalize）**。
- [ ] 入門難度未使用過度劇烈的**變速特效（SV Effects）**，且所有綠線倍率皆落在合理範圍（系統範圍為 `0.10x`–`10.00x`）。

---

## 2. 官方 Ranking Criteria（RC）硬性門檻檢核

> 來源：[raw/04_ranking_criteria_4k.md](../../raw/04_ranking_criteria_4k.md) §1–§3

- [ ] **物件數門檻**：每個難度皆包含至少 **100 個物件（Notes）**。
- [ ] **時間跨度門檻**：第一個物件到最後一個物件的跨度至少 **30 秒**。
- [ ] **禁止重疊**：同一軌道在同一時間點沒有重疊物件；所有**長條（Long Note，LN）**終點（Tail）均未與同軌下一個物件重疊。
- [ ] **難度組結構（Spread Requirements）**符合歌曲**有效遊玩時間（Drain Time）**要求：
  - 小於 3 分 30 秒：至少 2 難度（若僅 2 個，最低須為 `Easy`、`Normal` 或 `Hard`）
  - 3 分 30 秒至 4 分 15 秒：至少 3 難度（最低須為 `Easy` 或 `Normal`）
  - 超過 4 分 15 秒：至少 4 難度（最低須為 `Easy` 或 `Normal`）
- [ ] 節拍細分線與鍵型未超出該難度的分級定位（例如 `Easy` 不出現密集**雙押 Jump** 或複雜**長條 LN**）。

---

## 3. 可玩性與審圖避雷檢核

> 來源：[raw/05_modding_and_playability.md](../../raw/05_modding_and_playability.md) §1–§4

- [ ] **無過度堆疊（Overmapping）**：安靜或清唱段落未強塞密集 1/4 藍線或多押，符合**音樂能量對等原則（Intensity Matching）**。
- [ ] **採音層次（Layering）前後一致**：重複出現的主旋律與鼓點，前後採音規則統一無無故漏採或亂換樂器。
- [ ] **手部負擔合理**：
  - 高速 1/4 藍線中無 4 個以上的**長縱連（Long Jack）**。
  - **左右手平衡（Hand Bias 平衡）**得當，單手不會連續超負荷連點。
  - **長條（LN）**按住期間，同手另一軌無造成釋放衝突的密集單鍵。
  - **長條（LN）**終點（Tail）後預留至少 **1/4 拍**（高 BPM 建議 **1/2 拍**）緩衝再接同軌單鍵。
- [ ] **無難度斷層（Difficulty Spike）**：全曲**最高難度段落（Peak）**與該難度的整體定位一致，結尾或副歌不會突然跨級暴衝。

---

## 相關頁面與延伸閱讀

- 對應規範詳解：[osu!mania 4K 官方 Ranking Criteria（RC）核心規範](../standards/ranking-criteria.md)
- 退件原因與修正原理：[常見審圖（Modding）退件地雷與可玩性原則](../standards/modding-pitfalls.md)
- 回顧完整入門步驟：[零基礎 4K 作圖起步 5 步驟路線圖](./beginner-mapping-roadmap.md)
- 查詢陌生術語：[中英文雙語術語對照表](../glossary.md)
- 回到總目錄：[osu!mania 4K 作圖入門 Wiki 總覽](../index.md)
