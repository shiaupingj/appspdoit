# appspdoit 開發者網站

appspdoit 的開發者官網，整合三款 App 的產品介紹、隱私權政策與使用條款。
純 HTML / CSS 靜態網站，可直接部署至 GitHub Pages。

## 網站結構

```
appspdoit/
├── index.html                 # 首頁（三款 App 總覽）
├── assets/
│   └── style.css              # 共用樣式表（亮/暗色、響應式）
├── apps/
│   ├── ira.html               # IRA 資產再平衡 產品頁
│   ├── planto.html            # Planto 產品頁
│   └── treway.html            # TreWay 找樹趣 產品頁
├── legal/
│   ├── ira-privacy.html       # IRA 隱私權政策
│   ├── ira-terms.html         # IRA 使用條款
│   ├── planto-privacy.html    # Planto 隱私權政策
│   ├── planto-terms.html      # Planto 使用條款
│   ├── treway-privacy.html    # TreWay 隱私權政策
│   └── treway-terms.html      # TreWay 使用條款
├── .nojekyll                  # 讓 GitHub Pages 原樣輸出，不經 Jekyll 處理
└── README.md
```

## 部署到 GitHub Pages

1. 在 GitHub 建立一個名為 `appspdoit` 的 repository。
2. 在本資料夾初始化並推送：

   ```bash
   cd /Users/shiaupingjian/dev/appspdoit
   git init
   git add .
   git commit -m "Initial developer site"
   git branch -M main
   git remote add origin https://github.com/shiaupingj/appspdoit.git
   git push -u origin main
   ```

3. 到 GitHub repo → **Settings** → **Pages** → Source 選 `Deploy from a branch`，
   Branch 選 `main` / `/(root)`，儲存。
4. 約 1 分鐘後即可在 `https://shiaupingj.github.io/appspdoit/` 看到網站。

## 各頁的公開網址（供商店填寫）

部署後，App 商店的「隱私權政策 URL」可填：

- IRA：`https://shiaupingj.github.io/appspdoit/legal/ira-privacy.html`
- Planto：`https://shiaupingj.github.io/appspdoit/legal/planto-privacy.html`
- TreWay：`https://shiaupingj.github.io/appspdoit/legal/treway-privacy.html`

## 之後可做的事

- **換上真實截圖**：產品頁中的手機外框為佔位區，將截圖存到 `assets/`
  後，把對應 `<div class="phone-screen">…</div>` 換成 `<img src="../assets/你的截圖.png" alt="…">` 即可。
- **綁自訂網域**：在 repo 根目錄新增 `CNAME` 檔（內容為網域名），
  並到網域商設定 DNS，即可用自己的網址。

---

法律頁（隱私權／使用條款）為依 App 現有描述撰寫的範本，上架前建議諮詢法律專業人士確認。
