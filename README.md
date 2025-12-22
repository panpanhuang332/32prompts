✨ 一指提示 (One Finger Prompt) - AI 繪圖咒語生成助手
一指提示 是一個專為 AI 繪圖（如 Midjourney, Stable Diffusion）設計的輕量級網頁工具。透過直觀的點選介面，讓使用者無需繁瑣輸入，即可快速組合成高品質的英文提示詞（Prompts）。專案整合了 Google Firebase 驗證系統，支援會員分級功能，並採用 PWA 技術，可直接安裝於手機桌面使用。
📱 功能特色 (Features)
👆 直觀操作：無需記憶複雜單字，透過下拉選單選擇人物、場景、光影、風格。
🔐 會員解鎖機制：整合 Google Firebase Authentication，登入後即可解鎖「攝影」、「藝術」、「動漫」等進階分類。
🌍 自動翻譯：支援輸入中文主題，自動透過 API 轉換為英文提示詞。
📱 PWA 支援：支援 Progressive Web App，可將網頁安裝至手機桌面，離線也能開啟（部分功能）。
🎲 隨機靈感：不知道畫什麼？內建隨機功能，一鍵產生創意組合。
🔄 反推模式：提供圖片上傳介面，協助使用者產生用於分析圖片的指令（需搭配 Gemini/GPT 使用）。
📋 一鍵複製：組合好的提示詞可一鍵複製，直接貼上至繪圖軟體。
🛠️ 技術架構 (Tech Stack)
Frontend: HTML5, CSS3 (Bootstrap 5), Vanilla JavaScript
Backend / Auth: Google Firebase (Authentication)
PWA: Service Worker, Manifest.json
Translation: MyMemory Translation API
🚀 安裝與執行 (Installation)
本專案為純靜態網頁結構，無需安裝 Node.js 或後端伺服器即可運行，但需要設定 Firebase。
1. 下載專案
   git clone https://github.com/panpanhuang332/32prompts.git
cd 32prompts
2. 設定 Firebase
本專案依賴 Firebase 進行 Google 登入驗證。你需要自行申請 Firebase 專案：
前往 Firebase Console。
建立新專案。
在 Authentication 中啟用 Google 登入供應商。
在 Project Settings (專案設定) 中新增 Web App，並取得 firebaseConfig 代碼。
3. 修改設定檔
打開 index.html，找到底部的 Firebase 設定區塊，填入你自己的金鑰：

JavaScript


const firebaseConfig = {
    apiKey: "你的_API_KEY",
    authDomain: "你的專案ID.firebaseapp.com",
    projectId: "你的專案ID",
    storageBucket: "你的專案ID.appspot.com",
    messagingSenderId: "你的SENDER_ID",
    appId: "你的APP_ID"
};


4. 啟動預覽
由於瀏覽器安全性限制（CORS 與 Module 載入），請勿直接雙擊 html 檔案開啟。
推薦方式：使用 VS Code 安裝 Live Server 套件，右鍵點擊 index.html 選擇 Open with Live Server。
此時瀏覽器將自動開啟 http://127.0.0.1:5500，登入功能即可正常運作。
📸 畫面預覽 (Screenshots)
(建議在此處放 1-2 張你的網頁截圖，例如一張是未登入畫面，一張是登入後解鎖畫面)
🤝 貢獻 (Contributing)
歡迎提交 Pull Request 或 Issue！如果你有新的分類點子或提示詞庫，歡迎擴充 database 物件內容。
Fork 本專案
建立你的 Feature Branch (git checkout -b feature/AmazingFeature)
提交你的修改 (git commit -m 'Add some AmazingFeature')
推送到分支 (git push origin feature/AmazingFeature)
開啟 Pull Request
📄 授權 (License)
本專案採用 MIT License 授權。
由 [panpanhuang332] 開發製作
