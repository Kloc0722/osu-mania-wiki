---
title: osu!mania 4K 官方 Ranking Criteria（RC）核心規範
category: standards
sources:
  - raw/04_ranking_criteria_4k.md
updated: 2026-11-23
tags:
  - Ranking Criteria
  - RC
  - Spread Requirements
  - Drain Time
  - 難度分級
---

# osu!mania 4K 官方 Ranking Criteria（RC）核心規範

就算你目前只是想練手做自己的第一張圖，提早認識**官方上架標準（Ranking Criteria，簡稱 RC）**依然非常有幫助。RC 是 osu! 官方為了確保上架（Ranked）譜面具備基本品質與公平性所訂定的硬性規則，裡面的難度分級與防呆門檻，本身就是新手最可靠的設計參考尺。

---

## 1. 難度組結構（Spread Requirements）

> 來源：[raw/04_ranking_criteria_4k.md](../../raw/04_ranking_criteria_4k.md) §1 難度組結構（Spread Requirements）

一個完整的**譜面集（Beatmapset）**通常不會只有單一難度，而是會依照歌曲的**有效遊玩時間（Drain Time）**——也就是扣除前奏與間奏空白後的實際遊玩時長——要求包含足夠數量的難度，並且由低到高循序漸進：

| 有效遊玩時間（Drain Time） | 最少難度數量 | 最低難度要求 |
| :--- | :---: | :--- |
| **小於 3 分 30 秒** | 至少 **2 個** | 若僅有 2 個難度，最低難度必須為 `Easy`、`Normal` 或 `Hard` 之一 |
| **3 分 30 秒至 4 分 15 秒** | 至少 **3 個** | 最低難度必須為 `Easy` 或 `Normal` |
| **超過 4 分 15 秒** | 至少 **4 個** | 最低難度必須為 `Easy` 或 `Normal` |

> **新手建議**：剛入門時不必一次挑 5 分鐘的長曲，建議先選有效遊玩時間小於 3 分 30 秒的短曲，從 `Easy` 與 `Normal` 兩個難度開始練習。

---

## 2. 物件數量與時間硬性限制

> 來源：[raw/04_ranking_criteria_4k.md](../../raw/04_ranking_criteria_4k.md) §2 物件數量與時間限制

無論哪一個難度，都必須滿足以下三項硬性底線，否則無法通過官方審核：

1. **最低物件數**：每個難度至少必須包含 **100 個物件（Notes）**。
2. **最短時間跨度**：從第 1 個物件到最後 1 個物件之間的時間跨度，必須至少為 **30 秒**。
3. **禁止重疊物件**：
   - 同一條軌道在完全相同的時間點，**只能放置 1 個物件**。
   - **長條（Long Note，LN）**的終點（Tail）絕對不能與同一條軌道的下一個物件重疊（並建議額外保留手部放開緩衝，詳見[常見審圖退件地雷與可玩性原則](./modding-pitfalls.md)）。

---

## 3. 4K 難度分級定位標準

> 來源：[raw/04_ranking_criteria_4k.md](../../raw/04_ranking_criteria_4k.md) §3 難度分級定位標準（4K 基準）

規劃不同難度時，可以依照下表控制[節拍細分線（Beat Snap Divisor）](../basics/editor-and-beat-snap.md)與[基礎鍵型](../patterns/chord-and-stream-patterns.md)的使用上限：

| 難度分級 | 主要節拍細分線 | 鍵型與物件配置定位 |
| :--- | :--- | :--- |
| **Easy（入門）** | `1/1` 白色線、`1/2` 紅色線 | 以**單點（Single）**為主；**嚴禁**密集雙押（Jump）或複雜長條（LN）。 |
| **Normal（進階）** | 穩定的 `1/2` 紅色線＋少量 `1/4` 藍色線 | 允許在重拍處配置簡單的**雙押（Jump）**。 |
| **Hard（熟練）** | 完整呈現主旋律的 `1/4` 藍色線 | 包含基礎**交互連打（Stream）**與適當比例的**長條（Long Note，LN）**。 |
| **Insane / Expert（高階）** | 全面採音與高速細分 | 完整呈現鼓點、主旋律與伴奏層次，可使用**三押（Hand）**、**四押（Quad）**與高速連打。 |

---

## 相關頁面與延伸閱讀

- 下一篇推薦：[常見審圖（Modding）退件地雷與可玩性原則](./modding-pitfalls.md)（除了硬性規則，還要避開這些手感地雷）
- 實戰核對清單：[送審前自我檢核清單](../guides/pre-mod-checklist.md)
- 回顧鍵型定義：[4K 基礎鍵型圖鑑：同時按壓與連續移動](../patterns/chord-and-stream-patterns.md)
- 查詢陌生術語：[中英文雙語術語對照表](../glossary.md)
- 回到總目錄：[osu!mania 4K 作圖入門 Wiki 總覽](../index.md)
