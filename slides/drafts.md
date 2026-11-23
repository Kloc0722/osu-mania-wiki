# 『osu!mania 4K 作圖入門』逐頁稿（Drafts）

> 規範：每頁正文控制在 **130 中文字以內**，每頁底部皆標註 `來源：[[wiki/xxx.md]]`（附對應章節），後續渲染 HTML 時嚴禁偷改逐頁稿文字內容。

---

## Slide 01：osu!mania 4K 作圖入門：給零基礎新手的完全指南

- 專為零基礎玩家設計，帶你從空白音訊完成第一張 4K 譜面。
- 全篇採中英文雙語並列，直接接軌編輯器與社群術語。
- 階段一：編輯器軌道、節拍細分線與紅綠線變速。
- 階段二：單鍵、長條與 4K 基礎鍵型圖鑑。
- 階段三：官方規範（RC）與審圖避雷。
- 階段四：五步驟實戰起步與送審檢核。

來源：[[wiki/index.md]]

---

## Slide 02：認識 4K 軌道結構與鍵位對應

- 4K 由左至右為 Column 1 至 4，物件落至底部判定線（Judgement Line）時按下對應按鍵。
- Column 1：`D`（X 座標 `64`），左手負責左兩軌。
- Column 2：`F`（X 座標 `192`），左手食指操控。
- Column 3：`J`（X 座標 `320`），右手負責右兩軌。
- Column 4：`K`（X 座標 `448`），右手中指操控。

來源：[[wiki/basics/editor-and-beat-snap.md]] §1

---

## Slide 03：節拍細分線（Beat Snap Divisor）怎麼看？

- 時間軸彩色橫線像刻度尺，讓物件精準吸附拍點。
- 白色線（1/1）：整拍四分音符，4/4 拍每小節 4 條，首條較粗為小節線。
- 紅色線（1/2）：半拍八分音符，常見基本鼓點。
- 藍色線（1/4）：四分之一拍十六分音符，用於快旋律或連打。
- 紫色線（1/3）三連音；黃（1/6）、橘（1/8）用於高難度。
- 新手先看白色線與紅色線，熟練後再加藍色線。

來源：[[wiki/basics/editor-and-beat-snap.md]] §2

---

## Slide 04：Timing 紅線與 BPM 對拍基礎

- Timing 紅線（Uninherited Timing Point）決定真實節奏與拍點基準。
- BPM 為每分鐘節拍數；偏移量（Offset，ms）為第一拍位置。
- 拍長公式：`Beat Length (ms) = 60000 / BPM`。
- 例：BPM 150 時，1/1 白色線 400 ms、1/2 紅色線 200 ms、1/4 藍色線 100 ms。
- 須用波形圖與節拍器對齊鼓點，避免音畫不同步（Off-sync）。

來源：[[wiki/basics/timing-and-bpm.md]] §1–§2

---

## Slide 05：Timing 綠線與 SV 視覺變速機制

- Timing 綠線（Inherited Timing Point）不改真實拍點，專控視覺下落倍率（SV，`0.10x–10.00x`）。
- 公式：`Effective Scroll Speed = Base BPM × SV`。
- 基準 BPM 180 時，`0.50x` 如 BPM 90（變密），`2.00x` 如 BPM 360（拉開）。
- 速度標準化（Normalize）：BPM 120 加速至 180，同毫秒疊 `≈ 0.67x` 維持恆速。
- 新手應避免過度劇烈變速特效（SV Effects）。

來源：[[wiki/basics/sv-and-scroll-speed.md]] §1–§3

---

## Slide 06：兩種基本物件：單鍵（Rice）與長條（LN）

- 單鍵（Rice）：俗稱米粒，抵達判定線按下即完成判定，適合鼓點與短音。
- 長條（Long Note，LN）：具起點（Head）與終點（Tail），須按住至終點再放開。
- 放開時機（Release Timing）同算準度，過早或過晚會使 300 降級為 200 或 100。
- RC 硬規定：長條（LN）終點（Tail）不得與同一軌道下個物件重疊。
- 可玩性建議：終點後預留至少 1/4 拍（高 BPM 建議 1/2 拍）緩衝再接同軌單鍵。

來源：[[wiki/patterns/note-types.md]] §1–§2

---

## Slide 07：同時按壓類鍵型（Chord Patterns）

- 依同一時間點物件數分四階，呈現音樂重量與多押密度（Chord 密度）。
- 單點（Single，1 鍵）：呈現單音旋律與入門難度。
- 雙押（Jump，2 鍵）：強調重拍或和弦主音。
- 三押（Hand，3 鍵）：單手按兩鍵、另一手按一鍵，用於副歌高潮。
- 四押（Quad，4 鍵）：四軌全滿最高重音，入門與進階應謹慎使用。

來源：[[wiki/patterns/chord-and-stream-patterns.md]] §1

---

## Slide 08：連續移動類鍵型（Stream & Jack）

- 連續細分拍點（如 1/4 藍色線）依軌道排列形成三種連打。
- 交互連打（Stream）：不同軌道交替出現（如 1-2-3-4），左右手輪流點擊。
- 雙鍵交互（Trill）：固定兩軌快速來回（如 1-2-1-2、2-3-2-3）。
- 同軌連打（Jack）：同軌連續點擊（如 1-1-1），考驗單指爆發力。
- 連續超過 3 個（4 個以上）的快速同軌連打稱長縱連（Long Jack），入門譜面務必盡量避免。

來源：[[wiki/patterns/chord-and-stream-patterns.md]] §2–§3

---

## Slide 09：官方 Ranking Criteria（RC）核心規範

- 難度組（Spread）依有效遊玩時間（Drain Time）：未滿 3:30 至少 2 個（僅 2 個時最低 Easy/Normal/Hard）。
- 3:30–4:15 至少 3 難度、超過 4:15 至少 4 難度，此兩檔最低皆須為 Easy 或 Normal。
- 硬性底線：每難度至少 100 物件（Notes）、首尾跨度至少 30 秒、禁止同軌重疊。
- Easy 用 1/1、1/2 單點（Single）；Normal 加重拍雙押（Jump）；Hard 加 1/4 交互連打（Stream）與長條（LN）；Insane/Expert 全面採音。

來源：[[wiki/standards/ranking-criteria.md]] §1–§3

---

## Slide 10：四大審圖（Modding）退件地雷

- 過度堆疊（Overmapping）：平緩段硬塞密集鍵型 → 循音樂能量對等原則（Intensity Matching）。
- 採音不一致（Inconsistent Hitsounding / Layering）：重複段忽採忽漏 → 事前固定採音層次（Layering）。
- 不合理手部負擔（Unplayable Patterns）：高速 1/4 長縱連或 LN 衝突 → 維持左右手平衡（Hand Bias 平衡）與尾端緩衝。
- 難度斷層（Difficulty Spike）：結尾突飆高難 → 控管最高難度段落（Peak）上限。

來源：[[wiki/standards/modding-pitfalls.md]] §1–§4

---

## Slide 11：零基礎 4K 作圖起步 5 步驟

- 步驟 1：熟悉 4K 軌道（D/F/J/K）與白色、紅色、藍色節拍細分線。
- 步驟 2：先用波形圖與節拍器對準 Timing 紅線，變速段疊綠線恆速。
- 步驟 3：選定 Easy 或 Normal 難度，固定採音層次（Layering）。
- 步驟 4：先鋪單鍵骨架再酌加長條，兼顧能量對等與左右手平衡。
- 步驟 5：親自試玩排除難度斷層，對照清單後提交審圖。

來源：[[wiki/guides/beginner-mapping-roadmap.md]] Step 1–5

---

## Slide 12：送審前自我檢核清單（Pre-Mod Checklist）

- Timing 與 SV：紅線貼齊鼓點無 Off-sync；變速已完成 Normalize；入門無劇烈特效。
- RC 硬性門檻：滿 100 物件、滿 30 秒、無重疊、難度組與分級符合規定。
- 可玩性自檢：無過度堆疊、採音前後一致、無高速 1/4 長縱連與難度斷層。
- 長條（LN）終點預留 1/4 至 1/2 拍緩衝；先自檢能讓審圖者專注於進階建議。

來源：[[wiki/guides/pre-mod-checklist.md]] §1–§3
