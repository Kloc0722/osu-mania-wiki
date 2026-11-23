---
title: 基本物件類型：單鍵（Rice）與長條（LN）
category: patterns
sources:
  - raw/02_note_types_and_patterns.md
  - raw/04_ranking_criteria_4k.md
  - raw/05_modding_and_playability.md
updated: 2026-11-23
tags:
  - Rice
  - Long Note
  - LN
  - 單鍵
  - 長條
  - 放開時機
---

# 基本物件類型：單鍵（Rice）與長條（LN）

設定好軌道觀念與[Timing 紅線（Uninherited Timing Point）](../basics/timing-and-bpm.md)後，接下來就是把**物件（Notes）**放上時間軸。在 osu!mania 4K 中，所有看似複雜的譜面，其實都只由兩種最基本的物件組成：**單鍵（Rice）**與**長條（Long Note，LN）**。

---

## 1. 兩種基本物件（Note Types）

> 來源：[raw/02_note_types_and_patterns.md](../../raw/02_note_types_and_patterns.md) §1 兩種基本物件（Note Types）

### 單鍵（Rice）
- **外型與俗稱**：單獨一顆下落物件，社群常暱稱為「米粒」。
- **操作方式**：最基礎的點擊物件，玩家只需在物件抵達底部**判定線（Judgement Line）**時，精準按下對應按鍵即可完成判定。
- **常見用途**：對應短促的鼓點（如底鼓、小鼓）、俐落的彈撥音或一般旋律音符。

### 長條（Long Note，LN）
- **結構組成**：具備明確的**起點（Head）**與**終點（Tail）**，中間以長條相連，用來表達持續性的聲音（例如拉長的人聲、和弦鋪底或持續電子音）。
- **操作方式**：玩家必須在起點（Head）抵達判定線時按下並**持續按住**，直到終點（Tail）抵達判定線的瞬間再放開按鍵。
- **放開時機（Release Timing）的關鍵判定**：在 osu!mania 的判定機制中，**長條的放開時機同樣計算準度**。如果玩家過早放開或按太久太晚放開，都會導致該物件的判定降級（例如從 `300` 降為 `200` 或 `100`）。

| 比較項目 | 單鍵（Rice） | 長條（Long Note，LN） |
| :--- | :--- | :--- |
| 結構 | 單一拍點 | 起點（Head）＋持續段＋終點（Tail） |
| 判定重點 | 按下時機 | **按下時機**＋**放開時機（Release Timing）** |
| 對新手門檻 | 低，最容易上手 | 中，需同時顧及按住與準時放開 |

---

## 2. 長條（LN）的官方規範與手部緩衝原則

> 來源：[raw/04_ranking_criteria_4k.md](../../raw/04_ranking_criteria_4k.md) §2 物件數量與時間限制、§3 難度分級定位標準（4K 基準）；[raw/05_modding_and_playability.md](../../raw/05_modding_and_playability.md) §3 不合理的手部負擔（Unplayable Patterns）

因為長條（Long Note，LN）同時要求「按準頭」與「放準尾」，擺放時除了留意難度分級外，還必須遵守兩項關鍵規則：

1. **禁止尾端重疊（RC 硬性規定）**：長條的終點（Tail）**絕對不得**與同一條軌道的下一個物件重疊，否則直接違反[官方 Ranking Criteria（RC）](../standards/ranking-criteria.md)。
2. **預留尾端緩衝空間（可玩性原則）**：長條終點（Tail）結束後，建議預留至少 **1/4 拍**（若歌曲 BPM 較高，建議預留 **1/2 拍**）的空白再接同一軌道的下一個單鍵（Rice）；同時避免在按住 LN 期間，於同一隻手負責的另一條軌道安排過於密集的單鍵（避免釋放衝突）。
3. **依難度節制使用**：`Easy`（入門）難度嚴禁複雜長條；進入 `Hard`（熟練）難度後再加入適當比例的長條。

---

## 相關頁面與延伸閱讀

- 下一篇推薦：[4K 基礎鍵型圖鑑：同時按壓與連續移動](./chord-and-stream-patterns.md)
- 相關規範與避雷：[官方 Ranking Criteria（RC）核心規範](../standards/ranking-criteria.md)、[常見審圖（Modding）退件地雷與可玩性原則](../standards/modding-pitfalls.md)
- 回顧軌道與拍點：[編輯器軌道與節拍細分線基礎](../basics/editor-and-beat-snap.md)
- 查詢陌生術語：[中英文雙語術語對照表](../glossary.md)
- 回到總目錄：[osu!mania 4K 作圖入門 Wiki 總覽](../index.md)
