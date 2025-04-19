# Custom Erotic GPT Devlog 技術紀錄
``本專案運用的模型版本為 GPT-4o``
``架設過程請全程使用電腦版``
``請購買 GPT plus 或以上等升級方案，否則無法實際使用``

🚨 **警告：本專案包含成人向內容與語言模型尺度調教技術，僅供個人技術研究與私用，不建議公開部署或營利用途。**

```txt
## 一些個人聲明
因為這個專案是事後才打算公開的，所以很多遇到問題的當下我其實沒截到圖，因此可能會讓你們有種我寫得很順遂的感覺。
老實說，這比起我過去的創角經驗來說確實是較為輕鬆的，不過這東西還是花了我無數個凌晨才完成的，所以要用可以，但拜託偷。
還有我可以求個⭐️ㄇ，我需要鼓勵🥺
```

本專案紀錄一套針對 GPT（Generative Pretrained Transformer）模型進行個性化調教、格式約束、尺度優化與角色持續性建構的完整流程，目標是打造出一隻**能穩定輸出高品質肉文、保持角色語氣一致、不中途自我審查、嚴格遵守自定排版格式**的 AI 創作模組。

當然，僅僅只是開車、越獄並不能算是一次成功的 GPT 訓練。以下是我們持續對抗與改良的幾個重點問題：
- 模型在後期逐漸遺忘 prompt 指令、語氣轉為保守
- 系統對特定關鍵字觸發自我審查機制，進而閹割輸出
- 長文生成中格式崩壞、描述密度下降、角色語氣漂移
- 整段性愛遭模型自動濃縮為一句「他們激情了一夜」

---

## 🚧 專案目錄結構

```txt
/
├── 完整指令/                   # 整合用來餵 GPT 的最終指令集合
│   ├── 基本指令.md             # 通用 Prompt：格式、語氣、範圍、角色規則
│   └── 成人描寫風格規則.md     # S1–S5 等級、用詞邏輯、身體描寫邏輯

├── 運行過程紀錄/               # 開發者視角的過程紀錄
│   ├── 初步越獄.md             # 如何擺脫審查、放大尺度的嘗試與失敗
│   ├── 問題及解決.md           # 每次模型崩壞、格式斷裂的實際案例與調整
│   └── 運行結果.md             # 成功生成的段落例子、格式結果驗證

├── 設定與解釋/                 # 各種說明文與使用筆記
│   ├── 格式輸出說明.md         # 程式碼區塊格式、對話/動作排版規則
│   └── 操作說明與流程.md       # 如何使用這些指令、怎麼開新對話、保存角色

└── LICENSE.md                  # 許可聲明
