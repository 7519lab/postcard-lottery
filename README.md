# European Postcard Lottery

## 檔案
- `index.html` 前台（朋友用的）
- `admin.html` 後台（只有絲）
- `firebase-config.js` Firebase 設定
- `seed.js` 60 句小語 + 20 個稱號（匯入用）

## 第一次啟用
1. Firebase console → Authentication → 登入方式開「電子郵件/密碼」→ 使用者分頁新增你自己的帳號。
2. Firestore → 規則 → 貼上 `firestore.rules`，email 改成你的，發布。
3. 部署到 GitHub Pages 後，Authentication → 設定 → 已授權網域 → 加上 `你的帳號.github.io`。
4. 打開 `admin.html` → 登入 → 設定分頁 → 「匯入」。
5. 用 `index.html` 登記一個測試暱稱，確認結果頁正常，再去後台「參加者」刪掉。

## 兩個連結
- 卿卿我我圈（抽 10 張）：`index.html?g=ld`
- 現實朋友（抽 5 張）：`index.html?g=irl`
沒帶參數的話，登記頁會請她自己選。

## 流程
- 12 月初：把對應的連結發給兩群朋友。
- 12/18：後台 → 設定 → 關閉登記；抽籤分頁分別按「抽卿卿我我圈」「抽現實朋友」。
- 路上：後台 → 明信片 → 填城市、產生解鎖碼（抄在明信片背面）、狀態改 sent、儲存。
- 朋友收到：前台輸入解鎖碼，看到城市跟你寫的話。

## 隱私
- 地址不要放進任何檔案。中獎者你私下 LINE 要。
- `private/` 這個 collection 只有你登入後讀得到，中獎名單跟解鎖碼原文都在那裡。
