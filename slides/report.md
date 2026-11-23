# 教學簡報自我檢查報告（Stage 5 Audit Report）

- **檢查目標**：`slides/deck.html`（比對基準：`slides/drafts.md`、`wiki/`）
- **最新複驗日期**：2026-11-23（含獨立事實審查修訂版）
- **最終結論**：✅ **ALL PASS（12 / 12 頁全數通過，0 項事實／術語／版面缺失）**

---

## 1. 全域合規總覽

| 檢查項目 | 檢查結果 | 說明 |
| :--- | :---: | :--- |
| **單一真相來源限制（僅使用 `wiki/`）** | ✅ PASS | 全部 12 頁內容與圖解皆萃取自 `wiki/`，未引入 `wiki/` 未記載之修飾語或保證語氣。 |
| **零外部依賴（Self-contained HTML）** | ✅ PASS | 掃描 `slides/deck.html` 確認 **0 個** 外部 CDN／字體／樣式／腳本依賴，離線雙擊即可播放。 |
| **鍵盤與基礎互動操作** | ✅ PASS | 支援 `ArrowLeft`、`ArrowRight`、`Space`、`PageUp`、`PageDown`、`Home`、`End`、上下頁按鈕、圓點導覽與頂部進度條。 |
| **逐頁稿零偷改驗證（Verbatim Check）** | ✅ PASS | 以腳本逐字比對 12 頁標題、全部條列正文與頁尾出處，`slides/drafts.md` 與 `slides/deck.html` **差異數 = 0**。 |
| **出處標記與可點擊跳轉** | ✅ PASS | 12 頁底部皆標註 `來源：[[wiki/xxx.md]]` 並補上對應 `§` 小節，同時以相對路徑 `<a href="../wiki/...">` 實現可點擊跳轉（12/12 路徑皆存在）。 |
| **視覺化圖解覆蓋率** | ✅ PASS | 12 / 12 頁皆內嵌原生 SVG 圖解，且圖內用詞與數據條件皆與正文及 `wiki/` 完全一致。 |

---

## 2. 審查與修正迴圈紀錄

### A. 階段 3 局部 Loop（字數控管）
- 首輪精簡 Slide 03；修訂後全 12 頁純中文字數介於 `56–110` 字，全數嚴格低於 `130` 中文字上限。

### B. 階段 4／5 局部 Loop（版面高度防溢出）
- 調整 CSS 內距、字級（`13.2px–15px`）與列間距（`8px`），使 `640p` 筆電瀏覽器可用區淨高維持 `416 px`（`720p` 為 `494 px`），全 12 頁預估正文高度控制在 `228–320 px`（安全餘裕 ≥ `96 px`）。

### C. 獨立事實審查修訂紀錄（v2）
針對獨立事實審查報告指出之所有事實、限定條件、用詞歧義、雙語漏標與出處限制，已於 `slides/drafts.md` 與 `slides/deck.html` 同步完成修正：
1. **Slide 06（關鍵事實修正）**：將原本併列於「硬規定」下的兩項規範拆為獨立條目——明確區分 **「RC 硬規定：長條（LN）終點（Tail）不得與同一軌道下個物件重疊」** 與 **「可玩性建議：終點後預留至少 1/4 拍（高 BPM 建議 1/2 拍）緩衝再接同軌單鍵」**，並同步更新 SVG 標題標籤。
2. **Slide 03、04、08、11（用詞區分與前提補齊）**：節拍細分線正文與 SVG 全面改稱「白色線／紅色線／藍色線／紫色線」，避免與「Timing 紅線」混淆；Slide 03 補回「`4/4 拍` 每小節 4 條」前提，並將 SVG 中「進階主力」改為忠於 `wiki/` 的「較快旋律片段與連續點擊」。
3. **Slide 05（數值精確度）**：正文與 SVG 的 Normalize 算例同步補上約等號（`≈ 0.67x`、`恆速 ≈ 120`）。
4. **Slide 08、10、12（限定詞與語氣校正）**：
   - Slide 08 補回長縱連（Long Jack）的「**快速**同軌連打」限定詞，語氣對齊 `wiki/` 改為「入門譜面務必盡量避免」。
   - Slide 10 補齊 `採音不一致（Inconsistent Hitsounding / Layering）`、`不合理手部負擔（Unplayable Patterns）`、`左右手平衡（Hand Bias 平衡）` 雙語並列；修正 SVG「鋼琴清唱」為「純鋼琴前奏或清唱塞多押」，並補回「高速 1/4 排 4 連 Long Jack」。
   - Slide 12 移除「即可安心送審」保證語氣，改為忠於 `wiki/` 的「先自檢能讓審圖者專注於進階建議」；正文與 SVG 均補回「高速 1/4」前提。
5. **Slide 09（RC 條件完整與雙語對齊）**：正文與 SVG 完整補齊「僅 2 個難度時最低 Easy/Normal/Hard」及 `3:30–4:15`、`> 4:15` 兩檔「最低皆須為 Easy 或 Normal」之條件，並依 `glossary.md` 補齊 `單點（Single）`、`雙押（Jump）`、`交互連打（Stream）`、`長條（LN）` 雙語標示。
6. **全站 12 頁來源強化**：頁尾補上 `§` 小節編號並加上相對路徑可點擊 `<a>` 連結。

---

## 3. 逐頁詳細檢核表（v2 修訂後）

| 頁碼 | 純中文字數（≤130） | 逐字一致 | 底部出處標記（含小節與可點擊連結） | 內嵌 SVG 圖解 | 預估正文高度（`640p` 上限 416px） | 狀態 |
| :---: | :---: | :---: | :--- | :---: | :---: | :---: |
| **01** | 105 | ✅ | `來源：[[wiki/index.md]]` ✅ | ✅ 4 階段路線圖 | `280 px`（餘裕 136px） | ✅ PASS |
| **02** | 56 | ✅ | `來源：[[wiki/basics/editor-and-beat-snap.md]] §1` ✅ | ✅ 4K 軌道／座標／手部 | `254 px`（餘裕 162px） | ✅ PASS |
| **03** | 110 | ✅ | `來源：[[wiki/basics/editor-and-beat-snap.md]] §2` ✅ | ✅ 6 色節拍細分刻度 | `302 px`（餘裕 114px） | ✅ PASS |
| **04** | 64 | ✅ | `來源：[[wiki/basics/timing-and-bpm.md]] §1–§2` ✅ | ✅ Timing 紅線與 BPM150 尺 | `254 px`（餘裕 162px） | ✅ PASS |
| **05** | 56 | ✅ | `來源：[[wiki/basics/sv-and-scroll-speed.md]] §1–§3` ✅ | ✅ SV 疏密＋Normalize（≈120） | `298 px`（餘裕 118px） | ✅ PASS |
| **06** | 106 | ✅ | `來源：[[wiki/patterns/note-types.md]] §1–§2` ✅ | ✅ Rice／LN（RC 禁重疊 vs 建議緩衝） | `320 px`（餘裕 96px） | ✅ PASS |
| **07** | 92 | ✅ | `來源：[[wiki/patterns/chord-and-stream-patterns.md]] §1` ✅ | ✅ Chord 四階軌道圖 | `232 px`（餘裕 184px） | ✅ PASS |
| **08** | 101 | ✅ | `來源：[[wiki/patterns/chord-and-stream-patterns.md]] §2–§3` ✅ | ✅ Stream/Trill/Jack/快速 Long Jack | `276 px`（餘裕 140px） | ✅ PASS |
| **09** | 83 | ✅ | `來源：[[wiki/standards/ranking-criteria.md]] §1–§3` ✅ | ✅ RC 完整最低難度與門檻圖 | `272 px`（餘裕 144px） | ✅ PASS |
| **10** | 91 | ✅ | `來源：[[wiki/standards/modding-pitfalls.md]] §1–§4` ✅ | ✅ 四大審圖避雷對照 | `272 px`（餘裕 144px） | ✅ PASS |
| **11** | 100 | ✅ | `來源：[[wiki/guides/beginner-mapping-roadmap.md]] Step 1–5` ✅ | ✅ 5 步驟實作流程圖 | `232 px`（餘裕 184px） | ✅ PASS |
| **12** | 94 | ✅ | `來源：[[wiki/guides/pre-mod-checklist.md]] §1–§3` ✅ | ✅ 三大送審檢核站 | `228 px`（餘裕 188px） | ✅ PASS |
