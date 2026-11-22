# 專案藍圖 (AGENTS.md) - 261121_Firebase_GitHub

> **專案目標**：建構基於 Google Firebase Cloud Firestore 與 GitHub Pages 的即時互動教學工具（如即時文字雲、課堂投票），並實現 AI Agent（Antigravity）透過自然語言直接操控資料庫與一鍵部署。

---

## 📌 同步層級對照

| 層級 | 平台 / 媒介 | 位置與狀態 |
| :--- | :--- | :--- |
| **L1 本地藍圖** | 專案根目錄 | `AGENTS.md`、`handoff.md` |
| **L2 GitHub 私有/公開庫** | GitHub 儲存庫 | [https://github.com/Hung-Tse-Lin/wordcloud-firebase](https://github.com/Hung-Tse-Lin/wordcloud-firebase) |
| **L3 Obsidian 詳細筆記** | 本機工作筆記庫 | `D:\Visual Studio\Note\Obsidian_Agent\Projects\261121_Firebase_GitHub\_Dashboard.md` |

---

## 🛠️ 技術架構

- **前端視覺化**：Vanilla HTML5 + CSS3 (Glassmorphism) + JavaScript (ESM)
- **文字雲引擎**：`WordCloud2.js`
- **掃碼互動**：`QRCode.js`
- **雲端資料庫**：Google Cloud Firestore（NoSQL）
  - 專案 ID：`my-teaching-tools-69e57`
  - 集合名稱：`wordcloud_words`（白名單讀寫規則已部署）
  - 監聽模式：`onSnapshot` 零延遲雙向同步
- **託管與發布平台**：GitHub Pages（`https://hung-tse-lin.github.io/wordcloud-firebase/`）
- **工具鏈整合**：GitHub CLI (`gh`)、Firebase CLI (`firebase-tools`)、Antigravity 全域 MCP Server

---

## 🗺️ 專案路線圖 (Roadmap)

- [x] **階段一：GitHub 連接與驗證**
  - [x] Git 全域使用者設定 (`cmlin` / `cmlin.phone@gmail.com`)
  - [x] GitHub CLI 認證登入 (`Hung-Tse-Lin`)
  - [x] 取得 `delete_repo` 權限並完成端到端測試
- [x] **階段二：Firebase 資料庫串接與 MCP 配置**
  - [x] Firebase CLI 登入與專案綁定 (`my-teaching-tools-69e57`)
  - [x] Firestore 白名單安全性規則自動化部署 (`firestore.rules`)
  - [x] Antigravity 全域 MCP (`mcp_config.json`) 配置成功
  - [x] Firestore CRUD 讀寫與刪除全流程驗證
- [x] **階段三：即時文字雲網頁開發與上線**
  - [x] 撰寫響應式前端網頁 (`index.html`)
  - [x] 整合手機掃碼投影彈窗 (QR Code) 與老師清空管理機制
  - [x] 推送至 GitHub 並啟用 GitHub Pages 正式發布
  - [x] 雙向資料傳輸測試（使用者手機輸入 $\rightarrow$ 雲端 Firestore $\rightarrow$ 本機 Agent 抓回驗證）
- [ ] **階段四：後續擴展（待辦）**
  - [ ] 支援多房間/不同班級分類代碼（Room Code）
  - [ ] 增加詞彙過濾黑名單機制
  - [ ] 擴展課堂即時投票（Polls）或選擇題測驗功能

---

## 📁 專案目錄結構

```text
261121_Firebase_GitHub/
├── .firebaserc          # Firebase 專案綁定設定檔
├── .gitignore           # 機密憑證與暫存過濾
├── AGENTS.md            # 本專案藍圖
├── handoff.md           # 跨裝置 / 跨 Agent 交接檔案
├── firebase.json        # Firestore 規則對應配置
├── firestore.rules      # Firestore 安全性規則（白名單）
├── index.html           # 文字雲主要前端單頁應用程式
└── README.md            # 專案公開說明文件
```
