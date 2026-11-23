# AGENTS.md —『osu!mania 4K 作圖入門』LLM Wiki 操作規範

本檔案為本專案知識庫的最高架構規範與維護手冊（參考 Andrej Karpathy 的 LLM Wiki 工作流）。所有維護本知識庫的 AI Agent 在執行 **Ingest（編入）**、**Query（查詢）**、**Lint（健康檢查）** 或 **Slide Export（簡報產出）** 前，皆須完整閱讀並遵守本規範。

---

## 1. 專案定位與目標讀者

- **知識庫主題**：osu!mania 4K 作圖入門（Mapping Fundamentals）
- **目標讀者**：**完全零基礎的新手玩家**（可能玩過 4K，但剛接觸作圖編輯器，對紅線、綠線、鍵型、RC 規範與審圖皆無先備知識）。
- **寫作語氣與教學原則**：
  - 循序漸進、白話易懂，善用生活化比喻與具體數字舉例（例如實際帶入 BPM 算拍長、用軌道編號舉例鍵型）。
  - **禁止直接照抄 `raw/` 原文**：必須以零基礎友善的結構重新組織、拆解觀念並建立跨頁連結。
  - 避免未先解釋就出現進階社群術語；必要時先簡短說明，並加上內部連結指向對應頁面或術語表。
  - **嚴格忠於來源事實**：所有公式、數值門檻、座標與規範皆須對應 `raw/` 資料，不可憑空捏造未經證實的遊戲規則或數據。

---

## 2. 目錄架構與單一真相原則

```text
osu-mania-wiki/
├── AGENTS.md                   # 本規範檔（Schema 與工作流規則）
├── raw/                        # 【唯讀】原始資料來源（Immutable Source of Truth）
│   ├── 01_editor_and_timing.md
│   ├── 02_note_types_and_patterns.md
│   ├── 03_sv_and_bpm_mechanics.md
│   ├── 04_ranking_criteria_4k.md
│   └── 05_modding_and_playability.md
├── wiki/                       # 【AI 維護】主題式知識庫（Single Compiled Knowledge Base）
│   ├── index.md                # 總目錄、分類索引與新手閱讀路線
│   ├── log.md                  # 依時間序記錄每次 Ingest / Update / Lint / Export
│   ├── glossary.md             # 全站統一的中英文雙語術語對照表
│   ├── basics/                 # 編輯器、軌道、節拍線、Timing 紅線、綠線與 SV
│   ├── patterns/               # 物件類型（Rice / LN）與 4K 基礎鍵型圖鑑
│   ├── standards/              # 官方 Ranking Criteria（RC）核心規範與審圖（Modding）地雷
│   └── guides/                 # 零基礎實戰起步路線圖與送審前自我檢核清單
└── slides/                     # 【衍生輸出】由 wiki/ 產出的零依賴單一 HTML 教學簡報
```

### 權限邊界
- `raw/`：**嚴格唯讀**。Agent 不可修改、刪除或覆寫 `raw/` 內的原始檔案。
- `wiki/`：由 Agent 依據 `raw/` 編譯、重組與持續維護。
- `slides/`：只能以 `wiki/` 作為單一內容來源衍生產出，不可繞過 `wiki/` 直接另寫一套與知識庫矛盾的內容。

---

## 3. 頁面格式與寫作規範（完整 LLM Wiki 標準格式）

### 3.1 YAML Frontmatter（每頁必備）
`wiki/` 內的所有 Markdown 檔案（含主題頁、索引頁與術語表）頂部皆須具備以下 YAML Frontmatter：

```yaml
---
title: 頁面標題
category: basics | patterns | standards | guides | meta
sources:
  - raw/01_editor_and_timing.md
updated: YYYY-MM-DD
tags:
  - 關鍵字1
  - 關鍵字2
---
```

### 3.2 中英文術語規範（雙語並列）
- 全站重要專有名詞一律採**雙語並列**格式，預設為 **「中文（英文／縮寫）」**，例如：
  - `單鍵（Rice）`、`長條（Long Note，LN）`
  - `單點（Single）`、`雙押（Jump）`、`三押（Hand）`、`四押（Quad）`
  - `交互連打（Stream）`、`雙鍵交互（Trill）`、`同軌連打（Jack）`、`長縱連（Long Jack）`
  - `Timing 紅線（Uninherited Timing Point）`、`Timing 綠線（Inherited Timing Point）`
  - `視覺下落速度倍率（Slider Velocity，SV）`
  - `官方上架標準（Ranking Criteria，RC）`、`審圖（Modding）`
- 所有譯名須以 [wiki/glossary.md](wiki/glossary.md) 為全站唯一標準，避免同一概念在不同頁面出現混亂譯名。
- 若新增來自新 `raw/` 檔案的專有名詞，必須同步更新 [wiki/glossary.md](wiki/glossary.md)。

### 3.3 出處標記規範（章節層級）
- **頁面層級**：Frontmatter 的 `sources` 欄位列出本頁引用的所有 `raw/` 檔案路徑。
- **章節層級**：正文中每一個主要 `##` 章節（包含知識說明、公式、規範與實務原則）開頭必須附上明確的章節出處引用塊，格式如下：
  ```markdown
  > 來源：[raw/01_editor_and_timing.md](../../raw/01_editor_and_timing.md) §3 Timing 紅線（Uninherited Timing Point）
  ```
- 若某一小節綜合了多篇來源，以頓號或分號清楚列出所有對應檔名與章節編號。

### 3.4 內部連結與頁尾區塊
- 頁面互連一律使用**相對路徑 Markdown 連結**（例如 `[Timing 紅線與 BPM](../basics/timing-and-bpm.md)`），確保在 GitHub、VS Code 與本機瀏覽器皆可直接點擊跳轉。
- 每篇主題頁頁尾皆須提供 `## 相關頁面與延伸閱讀` 區塊，引導零基礎讀者順著學習路線閱讀下一篇或反查前置觀念。

---

## 4. 核心工作流（Workflows）

### 4.1 Ingest（資料編入）— 一次 2–3 篇
當 `raw/` 新增或尚未編入原始資料時，採用**一次 2–3 篇的小批次關聯整合**節奏：
1. **閱讀與規劃**：完整閱讀該批次的 2–3 篇 `raw/` 檔案，盤點概念、公式、數值、術語與跨篇關聯。
2. **建立或更新主題頁**：依 `basics/`、`patterns/`、`standards/`、`guides/` 主題分類寫入或融合更新（若新資料補充了既有主題，優先更新現有頁面並加上跨頁連結，而非無止盡開重複頁面）。
3. **標註章節出處**：確認每個主要小節都附上章節層級出處，並同步更新 Frontmatter 的 `sources` 與 `updated`。
4. **同步中樞檔案**：
   - 更新 `wiki/index.md`（加入新頁面摘要與閱讀路線）。
   - 更新 `wiki/glossary.md`（收錄新專有名詞並維持譯名一致）。
   - 在 `wiki/log.md` 頂部或底部依時間序新增一筆 `Ingest` 紀錄（註明日期、批次、來源檔名與建立／更新的頁面清單）。

### 4.2 Query（查詢與問答）
- 回答使用者關於 osu!mania 4K 作圖的問題時，**優先檢索 `wiki/index.md`、`wiki/glossary.md` 與相關主題頁**。
- 若發現高品質的綜合回答或常見新手疑問，可詢問使用者是否沉澱回 `wiki/guides/` 成為常駐頁面。

### 4.3 Lint（知識庫健康檢查）— 4 大類全面檢核
每次重大 Ingest 完成後，或使用者要求執行 Lint 時，必須依序檢查以下 **4 大類項目**並產出檢查報告（同時記錄於 `wiki/log.md`）：

1. **結構與連結完整度**
   - 檢查所有內部相對連結與 `raw/` 引用連結是否有效（零斷連 Broken Links）。
   - 檢查是否存在孤兒頁（未被 `wiki/index.md` 或任何其他頁面連入）。
   - 檢查所有 `wiki/` 檔案是否具備完整 YAML Frontmatter（`title`、`category`、`sources`、`updated`、`tags`）。
   - 檢查 `wiki/index.md` 是否涵蓋全部主題頁、且 `wiki/log.md` 是否同步記錄最新變更。
2. **來源與事實一致性**
   - 檢查各主題頁的主要 `##` 小節是否皆具備章節層級出處標記。
   - 交叉比對公式、座標與門檻數據是否與 `raw/` 100% 一致（例如：4K X 座標 `64 / 192 / 320 / 448`、拍長公式 `60000 / BPM`、SV 範圍 `0.10x–10.00x`、RC 最低 `100` 物件與 `30` 秒、Drain Time `3:30` / `4:15` 分界、Long Jack 定義等）。
3. **雙語術語一致性**
   - 檢查專有名詞是否遵守「雙語並列」規範且前後譯名一致。
   - 檢查各頁出現的專有名詞是否皆已收錄於 `wiki/glossary.md`。
4. **新手可讀性與知識缺口**
   - 檢查是否有未先解釋就直接冒出的進階術語。
   - 檢查是否存在概念過度重複分散、應整併的頁面。
   - 列出目前 `raw/` 尚未涵蓋、建議後續補充的新手主題（如：選歌與音訊準備、實際 Hitsounding 音效配置、譜面匯出與上傳流程等）。

---

## 5. 教學 HTML 簡報產出規範（Slide Export）

當使用者指示從知識庫產出教學簡報時，須嚴格遵守以下規格：

- **輸出位置**：統一存放在 `slides/` 資料夾（例如 `slides/osu-mania-4k-intro.html`）。
- **單一內容來源**：所有文字、數據、公式與術語必須直接萃取自 `wiki/`，維持雙語並列規範與準確數值，不可與 `wiki/` 矛盾。
- **零依賴單一 HTML 檔**：
  - 必須為單一自包含（Self-contained）的 `.html` 檔案，內嵌全部 CSS 與 JavaScript。
  - **禁止引用外部 CDN**（如外部字體、外部圖示庫或線上 Reveal.js CDN），確保檔案離線雙擊瀏覽器即可正常播放與顯示。
- **基礎操作體驗**：
  - 支援鍵盤方向鍵（`←` / `→`）、空白鍵、點擊按鈕翻頁，並顯示頁碼與頂部／底部進度條。
  - 響應式版面，在常見 16:9 投影與筆電螢幕皆不爆版、不裁切文字。
- **零基礎視覺圖解（SVG / HTML 原生繪製）**：
  - 至少涵蓋 4K 軌道與鍵位對應圖（`D / F / J / K` 與 X 座標）、節拍細分線色彩刻度（白／紅／藍／紫）、物件與基礎鍵型示意（Rice / LN / Single / Jump / Hand / Quad / Stream / Jack）以及 SV 高低速疏密視覺對照。
- **紀錄同步**：產出或更新簡報後，於 `wiki/log.md` 新增一筆 `Export` 紀錄。
