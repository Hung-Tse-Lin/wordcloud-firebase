# 即時互動文字雲 (Live Word Cloud)

結合 **Firebase Cloud Firestore** 與 **GitHub Pages** 的即時課堂/研習互動文字雲工具。

## ✨ 特色亮點

- **零延遲即時同步**：基於 Firestore `onSnapshot`，多端學生手機送出後，大螢幕文字雲立即動態放大重繪。
- **高並發支撐**：Firebase 免費方案支援百萬連線，千人研習亦能穩定運行。
- **免登入互動**：學生掃描 QR Code 即可快速參與。
- **即時數據看板**：包含累計投稿數、不重複關鍵字、熱門排行 TOP 5 與即時投稿跑馬標籤。
- **一鍵清空管理**：主控台支援快速重設資料庫。

## 🛠️ 技術架構

- **前端**：Vanilla HTML5, CSS3, JavaScript (ESM)
- **視覺化**：`WordCloud2.js`, `QRCode.js`
- **資料庫**：Google Cloud Firestore (NoSQL)
- **部署平台**：GitHub Pages
