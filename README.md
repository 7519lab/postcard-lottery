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
- Grace 的朋朋（抽 5 張）：`index.html?g=irl`
沒帶參數的話，登記頁會請她自己選。

## 流程
- 12 月初：把對應的連結發給兩群朋友。
- 12/18：後台 → 設定 → 關閉登記；抽籤分頁分別按「抽卿卿我我圈」「抽Grace 的朋朋」。
- 路上：後台 → 明信片 → 填城市、產生解鎖碼（抄在明信片背面）、狀態改 sent、儲存。
- 朋友收到：前台輸入解鎖碼，看到城市跟你寫的話。

## 首頁的聖誕樹
首頁是一棵樹，15 顆吊飾就是 EUROPE-01 到 15（最下面那排 11–15 剛好是 Grace 的朋朋那 5 張）。
吊飾直接讀後台「明信片」分頁的狀態，改完儲存樹就會變：
- waiting：暗的
- sent：金色發光
- arrived：紅色，露出國家代碼，點開看得到城市（所以朋友確認收到後再改成 arrived）
朋友看過自己的結果後，回到樹上，他的那顆會被圈起來寫「你的」。

## 隱私
- 地址不要放進任何檔案。中獎者你私下 LINE 要。
- `private/` 這個 collection 只有你登入後讀得到，中獎名單跟解鎖碼原文都在那裡。
