---
title: 零基礎 4K 作圖起步 5 步驟路線圖
category: guides
sources:
  - raw/01_editor_and_timing.md
  - raw/02_note_types_and_patterns.md
  - raw/03_sv_and_bpm_mechanics.md
  - raw/04_ranking_criteria_4k.md
  - raw/05_modding_and_playability.md
updated: 2026-11-23
tags:
  - 新手教學
  - 作圖流程
  - 路線圖
  - 入門指南
---

# 零基礎 4K 作圖起步 5 步驟路線圖

如果你是完全零基礎的新手，剛打開編輯器不知道該從哪裡下手，請直接照著這 5 個步驟走完你的第一張 osu!mania 4K 譜面。每一步都對應到知識庫裡的專屬說明頁，遇到卡關隨時點進去複習。

---

## Step 1：先搞懂畫面座標與節拍格線

> 來源：[raw/01_editor_and_timing.md](../../raw/01_editor_and_timing.md) §1 軌道結構與鍵位對應、§2 節拍細分線（Beat Snap Divisor）

- 確認 4 條軌道（Column 1–4，對應預設鍵位 `D / F / J / K` 與 X 座標 `64 / 192 / 320 / 448`）。
- 熟悉最常用的三條**節拍細分線（Beat Snap Divisor）**：**白色線（1/1 整拍）**、**紅色線（1/2 半拍）**、**藍色線（1/4 四分之一拍）**。
- 詳細複習：[編輯器軌道與節拍細分線基礎](../basics/editor-and-beat-snap.md)

---

## Step 2：定好 Timing 紅線（並視需要用綠線恆速）

> 來源：[raw/01_editor_and_timing.md](../../raw/01_editor_and_timing.md) §3 Timing 紅線（Uninherited Timing Point）；[raw/03_sv_and_bpm_mechanics.md](../../raw/03_sv_and_bpm_mechanics.md) §3 SV 的兩大實務用途

- **所有物件都還沒放之前，先把 Timing 紅線（Uninherited Timing Point）對準**：利用波形圖與節拍器確認 BPM 與**偏移量（Offset）**完全貼齊鼓點，杜絕**音畫不同步（Off-sync）**。
- 若歌曲中途有變速（例如主歌 `BPM 120`、副歌 `BPM 180`），記得在新紅線同一毫秒處疊加**Timing 綠線（Inherited Timing Point）**進行**速度標準化（Normalize）**，維持**恆定下落速度（Constant Scroll Speed）**；新手請先避免炫技式的劇烈**變速特效（SV Effects）**。
- 詳細複習：[Timing 紅線與 BPM 對拍基礎](../basics/timing-and-bpm.md)、[Timing 綠線與 SV 變速機制](../basics/sv-and-scroll-speed.md)

---

## Step 3：決定目標難度與採音層次（Layering）

> 來源：[raw/04_ranking_criteria_4k.md](../../raw/04_ranking_criteria_4k.md) §1 難度組結構（Spread Requirements）、§3 難度分級定位標準（4K 基準）；[raw/05_modding_and_playability.md](../../raw/05_modding_and_playability.md) §2 採音不一致（Inconsistent Hitsounding / Layering）

- 建議新手先從 `Easy`（以 1/1、1/2 的**單點 Single** 為主）或 `Normal`（穩定 1/2＋少量 1/4 與重拍**雙押 Jump**）練起。
- 動工前先定下本難度的**採音層次（Layering）**（例如「只採人聲主旋律」或「主旋律＋小鼓」），全曲貫徹同一套標準，不要重複段忽採忽漏。
- 若打算做完整**譜面集（Beatmapset）**，先看歌曲的**有效遊玩時間（Drain Time）**決定最少難度數（小於 3 分 30 秒至少 2 個難度）。
- 詳細複習：[官方 Ranking Criteria（RC）核心規範](../standards/ranking-criteria.md)

---

## Step 4：擺放物件與設計順手鍵型

> 來源：[raw/02_note_types_and_patterns.md](../../raw/02_note_types_and_patterns.md) §1–§3；[raw/05_modding_and_playability.md](../../raw/05_modding_and_playability.md) §1 過度堆疊（Overmapping）、§3 不合理的手部負擔（Unplayable Patterns）

- 先用**單鍵（Rice）**鋪出清晰的主節奏，長音處再酌量配置**長條（Long Note，LN）**（記得 LN 尾端後保留至少 1/4 拍、高 BPM 建議 1/2 拍的緩衝再接同軌單鍵）。
- 遵守**音樂能量對等原則（Intensity Matching）**：平緩段不亂塞密集物件與多押（避免**過度堆疊 Overmapping**），重拍與副歌再依難度階梯升級。
- 兼顧**左右手平衡（Hand Bias 平衡）**，避免在高速 1/4 藍線放 4 個以上同軌連打（**長縱連 Long Jack**）。
- 詳細複習：[基本物件類型：單鍵（Rice）與長條（LN）](../patterns/note-types.md)、[4K 基礎鍵型圖鑑](../patterns/chord-and-stream-patterns.md)

---

## Step 5：親自試玩、排除地雷並準備審圖（Modding）

> 來源：[raw/04_ranking_criteria_4k.md](../../raw/04_ranking_criteria_4k.md) §2 物件數量與時間限制；[raw/05_modding_and_playability.md](../../raw/05_modding_and_playability.md) §4 難度斷層（Difficulty Spike）

- 自己從頭到尾打過至少 1–2 次，確認沒有**難度斷層（Difficulty Spike）**、手部不卡鍵，也符合最低 `100` 個物件與 `30` 秒時間跨度。
- 找人**審圖（Modding）**之前，先照著[送審前自我檢核清單](./pre-mod-checklist.md)逐項打勾檢查！

---

## 相關頁面與延伸閱讀

- 下一步實戰檢核：[送審前自我檢核清單](./pre-mod-checklist.md)
- 避開常見退件問題：[常見審圖（Modding）退件地雷與可玩性原則](../standards/modding-pitfalls.md)
- 查詢陌生術語：[中英文雙語術語對照表](../glossary.md)
- 回到總目錄：[osu!mania 4K 作圖入門 Wiki 總覽](../index.md)
