# 專案交接檔 (handoff.md)

> 這是跨裝置、跨 Agent 與下次開工的唯一交接檔案。請維持精簡在一頁之內，詳細決策與長篇日誌請查閱 Obsidian。

---

### ⏯️ 目前做到哪
- 已完成 GitHub CLI 與 Firebase CLI 工具鏈之完整串接與全域 MCP 配置。
- 開發並發布「即時互動文字雲」網頁至 GitHub Pages，成功串接 Cloud Firestore `wordcloud_words` 集合。
- 驗證使用者從手機端實際輸入詞彙，Firestore 成功即時記錄，並由 Agent 透過 API 抓回 11 筆資料驗證成功。

---

### 🚦 目前狀態
- **可正常上線運行**：
  - 線上網址：`https://hung-tse-lin.github.io/wordcloud-firebase/`
  - GitHub 倉庫：`https://github.com/Hung-Tse-Lin/wordcloud-firebase`
  - Firebase 專案：`my-teaching-tools-69e57`（資料庫正常連線中）

---

### ➡️ 下一步具體待辦
1. 若需區分不同場次或班級，可於 `index.html` 與 Firestore 新增 `roomId` 或班級碼欄位。
2. 擴充更多教學互動工具（如課堂即時投票牆、抽籤互動），並在 `firestore.rules` 追加新集合白名單後部署。

---

### ⚠️ 注意事項
- 前端網頁之 `firebaseConfig`（含 apiKey）為瀏覽器公開配置，安全防護完全依賴 `firestore.rules` 白名單。
- 若需調整資料庫規則，請修改 `firestore.rules` 後執行 `npx firebase-tools deploy --only firestore:rules`，切勿直接在 Console 覆蓋測試模式。

---

### 🕐 狀態紀錄
- **最後更新時間**：2026-11-22 22:05
- **更新者**：Antigravity @ HTLIN-DELL
- **Git Push 狀態**：✅ 已推（origin/main）
