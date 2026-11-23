# 簡報證據卡（Evidence Cards）

> 所有卡片皆萃取自 `wiki/`，完整保留公式、座標、數據門檻與雙語術語標準，作為後續撰寫逐頁稿與繪製圖解的唯一事實依據。

---

## Card 01：專案定位與零基礎學習路徑
- **來源頁面**：`[[wiki/index.md]]`、`[[wiki/glossary.md]]`
- **核心重點**：
  - 對象：完全零基礎的 osu!mania 4K 新手玩家。
  - 全站雙語標準：一律採「中文（英文／縮寫）」並列（如 `單鍵（Rice）`、`長條（Long Note，LN）`、`審圖（Modding）`）。
  - 學習四階段：編輯器與時間軸基礎 → 物件與 4K 鍵型 → 官方規範與審圖避雷 → 實戰起步與送審自檢。

---

## Card 02：4K 軌道結構與鍵位對應
- **來源頁面**：`[[wiki/basics/editor-and-beat-snap.md]]`
- **核心重點**：
  - 4 條垂直下落軌道由左至右為 Column 1 至 Column 4。
  - 物件（Notes）由上往下移動，抵達底部**判定線（Judgement Line）**時精準按下對應按鍵。
  - 左兩軌由左手負責（中指／食指），右兩軌由右手負責（食指／中指）。
- **精準數據**：
  - Column 1：`D`，X 座標 `64`
  - Column 2：`F`，X 座標 `192`
  - Column 3：`J`，X 座標 `320`
  - Column 4：`K`，X 座標 `448`

---

## Card 03：節拍細分線（Beat Snap Divisor）
- **來源頁面**：`[[wiki/basics/editor-and-beat-snap.md]]`
- **核心重點**：
  - 時間軸上的彩色水平線，協助將物件吸附至正確音樂拍點。
  - 新手優先掌握白（1/1）、紅（1/2），熟練後再加入藍（1/4）；黃／橘多用於高難度裝飾音。
- **精準色碼與拍點對應**：
  - 白色線：`1/1`（整拍／四分音符；4/4 拍每小節 4 條白線，第 1 條較粗為小節線）
  - 紅色線：`1/2`（半拍／八分音符；流行／搖滾常見鼓點）
  - 藍色線：`1/4`（四分之一拍／十六分音符；快節奏旋律或連打）
  - 紫色線：`1/3`（三連音／十二分音符；三拍子律動或切分音）
  - 黃色線：`1/6`（六連音）與橘色線：`1/8`（三十二分音符）

---

## Card 04：Timing 紅線（Uninherited Timing Point）與 BPM 計算
- **來源頁面**：`[[wiki/basics/timing-and-bpm.md]]`
- **核心重點**：
  - 作圖第一步永遠是對拍：透過波形圖與節拍器確認紅線完全貼齊鼓點，避免**音畫不同步（Off-sync）**。
  - 兩大核心參數：**每分鐘節拍數（Beats Per Minute，BPM）**與**偏移量（Offset，單位 ms，第 1 條白線出現時刻）**。
  - 紅線管真實節拍；綠線不改真實節拍，只管視覺下落速度。
- **精準公式與算例**：
  - 拍長公式：`Beat Length (ms) = 60000 / BPM`
  - 當 `BPM = 150`：1/1 白線 = `400 ms`，1/2 紅線 = `200 ms`，1/4 藍線 = `100 ms`。

---

## Card 05：Timing 綠線（Inherited Timing Point）與 SV 變速機制
- **來源頁面**：`[[wiki/basics/sv-and-scroll-speed.md]]`
- **核心重點**：
  - 綠線繼承上方最近紅線，不改真實 BPM 或拍點，專控**視覺下落速度倍率（Slider Velocity，SV）**。
  - 兩大用途：
    1. **速度標準化（Normalize）**：歌曲變速時，在新紅線同一毫秒疊加綠線抵銷加速，維持**恆定下落速度（Constant Scroll Speed）**。
    2. **變速特效（SV Effects）**：配合驟停（Stop）、漸快（Accelerando）製造張力（新手入門應避免過度劇烈特效）。
- **精準公式與算例**：
  - SV 倍率範圍：`0.10x` 至 `10.00x`（預設 `1.00x`）
  - 有效下落速度公式：`Effective Scroll Speed = Base BPM × SV Multiplier`
  - 算例 1（基準 `BPM 180`）：`SV 0.50x` → 等同 `BPM 90`（變密集低速段）；`SV 2.00x` → 等同 `BPM 360`（拉大間距高速段）。
  - 算例 2（Normalize）：主歌 `BPM 120` 變速至副歌 `BPM 180`，疊加 `SV = 120 / 180 ≈ 0.67x`。

---

## Card 06：基本物件類型——單鍵（Rice）與長條（Long Note，LN）
- **來源頁面**：`[[wiki/patterns/note-types.md]]`
- **核心重點**：
  - **單鍵（Rice）**：俗稱米粒，抵達判定線按下即完成判定，適合短促鼓點與基礎旋律。
  - **長條（Long Note，LN）**：具**起點（Head）**與**終點（Tail）**，需按住至終點再放開。
  - **放開時機（Release Timing）**同樣計算準度，過早或過晚放開會導致判定降級（如 `300` 降為 `200` 或 `100`）。
- **精準規範數據**：
  - RC 硬規定：LN 終點（Tail）**不得**與同一軌道下一個物件重疊。
  - 可玩性緩衝：LN 尾端後預留至少 `1/4` 拍（高 BPM 建議 `1/2` 拍）再接同軌單鍵；按住 LN 時避免同手另一軌出現密集單鍵（釋放衝突）。

---

## Card 07：同時按壓類鍵型（Chord Patterns）
- **來源頁面**：`[[wiki/patterns/chord-and-stream-patterns.md]]`
- **核心重點**：
  - 依同一時間點物件數分 4 階，反映音樂能量與多押密度（Chord 密度）。
  - 應遵循**音樂能量對等原則（Intensity Matching）**，不可在平緩段硬塞高密度多押。
- **精準數據與階梯**：
  - **單點（Single）**：`1` 個物件（單音旋律／入門）
  - **雙押（Jump）**：`2` 個物件（重拍／和弦主音）
  - **三押（Hand）**：`3` 個物件（單手按兩鍵＋另一手按一鍵；副歌高潮）
  - **四押（Quad）**：`4` 個物件（4 軌全滿；最高強度重音，入門謹慎使用）

---

## Card 08：連續移動類鍵型（Stream & Jack Patterns）
- **來源頁面**：`[[wiki/patterns/chord-and-stream-patterns.md]]`
- **核心重點**：
  - **交互連打（Stream）**：連續細分拍點（如 1/4 藍線）於不同軌道交替（如 `1-2-3-4`），左右手輪流點擊。
  - **雙鍵交互（Trill）**：固定兩條軌道快速來回交替（如 `1-2-1-2` 或 `2-3-2-3`）。
  - **同軌連打（Jack）**：連續拍點重複於同一軌道（如 `1-1-1`），考驗單指爆發力。
  - **長縱連（Long Jack）**：連續超過 `3` 個以上（即 `4` 個以上）的快速同軌連打，對新手極度不友好，應透過**左右手平衡（Hand Bias 平衡）**避免。

---

## Card 09：官方 Ranking Criteria（RC）核心規範
- **來源頁面**：`[[wiki/standards/ranking-criteria.md]]`
- **核心重點與精準數據**：
  - **難度組結構（Spread Requirements）**依**有效遊玩時間（Drain Time）**分級：
    - `< 3 分 30 秒`：至少 `2` 個難度（若僅 2 個，最低須為 `Easy`、`Normal` 或 `Hard`）
    - `3 分 30 秒–4 分 15 秒`：至少 `3` 個難度（最低須為 `Easy` 或 `Normal`）
    - `> 4 分 15 秒`：至少 `4` 個難度（最低須為 `Easy` 或 `Normal`）
  - **硬性底線**：每難度至少 `100` 個物件、首尾跨度至少 `30` 秒、同軌同時禁重疊且 LN 尾端禁重疊。
  - **4K 難度定位**：
    - `Easy`：`1/1` 白＋`1/2` 紅、Single 為主、禁密集雙押與複雜 LN
    - `Normal`：穩定 `1/2`＋少量 `1/4`、重拍可配簡單 Jump
    - `Hard`：完整主旋律 `1/4`、基礎 Stream＋適量 LN
    - `Insane / Expert`：全面採音、可用 Hand / Quad 與高速連打

---

## Card 10：常見審圖（Modding）退件地雷與修正原則
- **來源頁面**：`[[wiki/standards/modding-pitfalls.md]]`
- **核心重點**：
  1. **過度堆疊（Overmapping）**：安靜段硬塞密集 1/4 或三四押 → 改循**音樂能量對等原則（Intensity Matching）**。
  2. **採音不一致（Inconsistent Hitsounding / Layering）**：相同旋律重複時忽採忽漏 → 動工前先固定**採音層次（Layering）**（如低難度只採人聲，高難度採主旋律＋小鼓）。
  3. **不合理手部負擔（Unplayable Patterns）**：高速 1/4 放 4 個以上 Long Jack 或 LN 同手釋放衝突 → 維持**左右手平衡（Hand Bias 平衡）**與 LN 尾端 `1/4–1/2` 拍緩衝。
  4. **難度斷層（Difficulty Spike）**：全曲 90% Normal 卻在結尾突飆 Hard/Insane → 控管**最高難度段落（Peak）**上限。

---

## Card 11：零基礎起步 5 步驟與送審前檢核
- **來源頁面**：`[[wiki/guides/beginner-mapping-roadmap.md]]`、`[[wiki/guides/pre-mod-checklist.md]]`
- **核心重點**：
  - **起步 5 步驟**：① 認識 4K 軌道與格線 → ② 定準紅線 BPM／Offset（變速加綠線 Normalize）→ ③ 選定難度與採音層次 → ④ 鋪設順手物件與鍵型 → ⑤ 親自試玩排除地雷並對照清單。
  - **送審前 3 大檢核**：Timing／SV 對拍與恆速、RC 硬門檻（100 物件／30 秒／禁重疊／Spread）、可玩性四大避雷全項通過。
