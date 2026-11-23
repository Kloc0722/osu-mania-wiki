# 『osu!mania 4K 作圖入門』教學簡報大綱（12 頁）

> **目標讀者**：完全零基礎的 osu!mania 4K 新手玩家  
> **內容來源**：嚴格限定於 `wiki/` 知識庫（詳見 `slides/sources.md` 與 `slides/cards.md`）  
> **設計原則**：循序漸進、雙語術語並列、每頁正文控制在 130 中文字以內並搭配視覺化圖解  
> **狀態**：🟡 人工確認關卡（待使用者確認後，再進入階段 3 逐頁稿撰寫）

---

## 逐頁規劃總表

| 頁碼 | 階段 | 投影片標題 | 教學重點與保留數據 | 視覺化圖解規劃 | 來源頁面 |
| :---: | :---: | :--- | :--- | :--- | :--- |
| **01** | 導覽 | **osu!mania 4K 作圖入門：給零基礎新手的完全指南** | 破冰建立信心，總覽 4 大學習階段（基礎時間軸 → 物件鍵型 → 官方規範與避雷 → 實戰起步），說明全簡報採雙語術語並列。 | 4 階段學習路徑卡片圖 | `[[wiki/index.md]]` |
| **02** | 基礎 | **認識 4K 軌道結構與鍵位對應** | Column 1–4 對應鍵位 `D/F/J/K`、X 座標 `64/192/320/448`、底部判定線（Judgement Line）與左右手各管兩軌分工。 | **SVG 4K 垂直軌道、座標與按鍵圖解** | `[[wiki/basics/editor-and-beat-snap.md]]` |
| **03** | 基礎 | **節拍細分線（Beat Snap Divisor）怎麼看？** | 白 `1/1`（整拍／小節線）、紅 `1/2`、藍 `1/4`、紫 `1/3`、黃 `1/6`、橘 `1/8`；新手先掌握白紅再加藍。 | **SVG 時間軸彩色節拍刻度尺圖解** | `[[wiki/basics/editor-and-beat-snap.md]]` |
| **04** | 時間軸 | **Timing 紅線與 BPM 對拍基礎** | 紅線（Uninherited）管真實節拍；BPM 與 Offset（ms）對準波形圖／節拍器避開音畫不同步；公式 `60000 / BPM` 與 `BPM 150`（`400/200/100 ms`）。 | 公式高光卡＋BPM 150 節拍間隔橫軸圖 | `[[wiki/basics/timing-and-bpm.md]]` |
| **05** | 時間軸 | **Timing 綠線與 SV 視覺變速機制** | 綠線（Inherited）不改真實拍點，專控 SV（`0.10x–10.00x`）；`Base BPM × SV` 算例（`0.50x` 變密、`2.00x` 拉開）；Normalize 恆速化（`120/180 ≈ 0.67x`）與少用劇烈特效。 | **SVG 紅綠線與 SV 疏密（0.5x / 1.0x / 2.0x）視覺對照圖** | `[[wiki/basics/sv-and-scroll-speed.md]]` |
| **06** | 物件 | **兩種基本物件：單鍵（Rice）與長條（LN）** | Rice 按下判定；LN 具起點／終點，放開時機亦算準度（`300→200/100`）；RC 禁尾端重疊，尾端後預留 `1/4–1/2` 拍緩衝。 | **SVG Rice vs LN 結構與尾端緩衝示意圖** | `[[wiki/patterns/note-types.md]]` |
| **07** | 鍵型 | **同時按壓類鍵型（Chord Patterns）** | Single（1）、Jump（2）、Hand（3）、Quad（4）四階密度對應音樂能量強弱，入門慎用三四押。 | **SVG 4K 軌道 Single / Jump / Hand / Quad 四格圖解** | `[[wiki/patterns/chord-and-stream-patterns.md]]` |
| **08** | 鍵型 | **連續移動類鍵型（Stream & Jack）** | Stream 交互、Trill 雙鍵交互（`2-3-2-3`）、Jack 同軌連打（`1-1-1`）；點出連續 4 個以上的 Long Jack 是新手大忌，應靠左右手平衡分散壓力。 | **SVG 4K 軌道 Stream / Trill / Jack / Long Jack 圖解** | `[[wiki/patterns/chord-and-stream-patterns.md]]` |
| **09** | 規範 | **官方 Ranking Criteria（RC）核心規範** | 依 Drain Time（`<3:30` 至少 2 難度、`3:30–4:15` 至少 3、`>4:15` 至少 4）訂難度組；最低 `100` 物件與 `30` 秒、禁重疊；Easy～Expert 四級定位。 | RC 難度組與四級定位精簡對照表 | `[[wiki/standards/ranking-criteria.md]]` |
| **10** | 避雷 | **四大審圖（Modding）退件地雷** | 過度堆疊（對等能量）、採音不一致（固定層次）、不合理手部負擔（防 Long Jack／釋放衝突）、難度斷層（控管 Peak 上限）。 | 四象限「地雷 → 解法」視覺卡片 | `[[wiki/standards/modding-pitfalls.md]]` |
| **11** | 實戰 | **零基礎 4K 作圖起步 5 步驟** | ① 認軌道格線 → ② 定準紅線與恆速綠線 → ③ 選難度定層次 → ④ 鋪設順手鍵型 → ⑤ 試玩排除地雷。 | 5 步驟流程時間線圖解 | `[[wiki/guides/beginner-mapping-roadmap.md]]` |
| **12** | 總結 | **送審前自我檢核清單（Pre-Mod Checklist）** | 送審前 3 大檢查站（Timing／SV、RC 硬門檻、可玩性自檢），鼓勵新手帶著清單完成第一張譜面。 | 三欄互動式／清單式檢核卡片 | `[[wiki/guides/pre-mod-checklist.md]]` |

---

## 確認事項
請審閱以上 12 頁大綱的**頁數、教學順序與視覺圖解配置**。若確認無誤（或有想增刪調整的頁次），回覆確認後我將立即進入 **階段 3（撰寫逐頁稿，嚴格控管每頁 130 中文字以內並附上來源標註）**。
