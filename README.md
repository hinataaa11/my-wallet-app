# 我的記帳｜GitHub PWA 版

## 你只需要先做一件事
打開 `index.html`，找到：

const APP_URL = "PASTE_YOUR_APPS_SCRIPT_WEB_APP_URL_HERE";

把雙引號裡換成你的 Apps Script Web App `/exec` 網址。

例如：

const APP_URL = "https://script.google.com/macros/s/xxxxxxxxxxxxxxxx/exec";

---

## GitHub Pages 部署

1. 登入 GitHub。
2. 新增一個 Repository，例如：
   `my-wallet-app`
3. 把這個資料夾內所有檔案上傳到 Repository 根目錄：
   - index.html
   - manifest.json
   - service-worker.js
   - app-icon-original.png
   - icons 資料夾
4. GitHub Repository 進入：
   Settings → Pages
5. Build and deployment：
   - Source：Deploy from a branch
   - Branch：main
   - Folder：/ (root)
6. 儲存後等待 GitHub Pages 建立完成。
7. GitHub 會提供一個網址，例如：
   https://你的帳號.github.io/my-wallet-app/

---

## iPhone 加到主畫面

1. 用 Safari 打開 GitHub Pages 網址。
2. 點下方「分享」。
3. 選「加入主畫面」。
4. 名稱可改成「我的記帳」。
5. 新增。

會使用你原本提供的整張圖片當圖示。

---

## Android

1. 用 Chrome 打開 GitHub Pages 網址。
2. 點右上角選單。
3. 選「安裝應用程式」或「加入主畫面」。

---

## 這版特別處理

- 使用原始整張圖片當 App icon。
- PWA standalone 模式。
- iPhone Apple Touch Icon。
- GitHub 外層頁面只負責 App 外觀。
- Google Apps Script 繼續負責實際記帳功能與 Google Sheet。
- 「Apps Script 載入失敗」備援提示預設隱藏。
- 超過 12 秒還沒載入才會出現。
- 備援提示放在畫面上方，不會蓋住記帳 App 底部的「記一筆」按鈕。
