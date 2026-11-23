# 03. 綠線與 SV（Slider Velocity）變速機制

## 1. 什麼是 Timing 綠線（Inherited Timing Point）？
與控制音樂真實節拍的「紅線」不同，**綠線（Inherited Timing Point）**繼承自上方最近的紅線，它**不會改變音樂的 BPM 或節拍刻度**，而是專門用來控制物件在畫面上的「視覺下落速度倍率（Slider Velocity，簡稱 SV）」。

## 2. 有效下落速度公式
在 osu!mania 中，綠線的 SV 倍率調整範圍為 `0.10x` 至 `10.00x`（預設為 `1.00x`）。物件實際在螢幕上移動的視覺速度由以下公式決定：
$$\text{Effective Scroll Speed} = \text{Base BPM} \times \text{SV Multiplier}$$
- 例如：基準 $\text{BPM} = 180$，若在某段落插入一條 $\text{SV} = 0.50\text{x}$ 的綠線，物件下落速度會瞬間減半（等同於 $\text{BPM } 90$ 的視覺速度），造成物件在畫面上看起來變密集（低速段）。
- 反之，若插入 $\text{SV} = 2.00\text{x}$ 的綠線，物件下落速度會加倍（等同於 $\text{BPM } 360$ 的視覺速度），物件間距拉大（高速段）。

## 3. SV 的兩大實務用途
1. **Normalize（速度標準化 / 恆速化）**：當一首歌曲本身有變速（例如主歌 $\text{BPM } 120$、副歌加速到 $\text{BPM } 180$）時，若不加綠線，副歌的下落速度會突然變快 1.5 倍。作圖者會在 $\text{BPM } 180$ 的紅線同一毫秒處疊加一條 $\text{SV} = \frac{120}{180} \approx 0.67\text{x}$ 的綠線，使整個曲目的視覺下落速度維持恆定（Constant Scroll Speed），保障玩家讀譜體驗。
2. **表現力特效（SV Effects）**：配合音樂的驟停（Stop）、漸快（Accelerando）或重低音衝擊，刻意利用高低倍率綠線製造視覺張力。但入門譜面應避免過度使用劇烈 SV，以免干擾基礎讀譜。
