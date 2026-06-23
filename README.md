# 院內藥品手冊查詢系統

靜態網站，部署於 GitHub Pages，無需伺服器。

## 資料夾結構

```
drug-handbook/
├── index.html          # 前台查詢頁面
├── data/
│   └── drugs.json      # 藥品資料庫（唯一需要更新的檔案）
├── admin/
│   └── index.html      # 後台管理（本機使用）
└── README.md
```

## 部署至 GitHub Pages

1. 在 GitHub 建立新的 Repository（建議命名 `drug-handbook`）
2. 將此資料夾所有檔案上傳（含 `data/drugs.json`）
3. 進入 Settings → Pages → Source 選 `main` branch，root `/`
4. 等待 1~2 分鐘，即可透過 `https://<你的帳號>.github.io/drug-handbook/` 存取

## 更新藥品資料

### 方法一：使用後台管理（推薦）
1. 在本機開啟 `admin/index.html`
2. 至「匯入 Excel」頁籤，上傳藥品 Excel
3. 對應欄位後確認匯入
4. 至「匯出」頁籤，下載 `drugs.json`
5. 至 GitHub Repository，找到 `data/drugs.json`，點擊鉛筆圖示或直接上傳覆蓋

### 方法二：直接編輯 JSON
直接修改 `data/drugs.json` 後上傳至 GitHub。

## Excel 格式說明

Excel 第一列為欄位標題，後台會自動嘗試對應以下欄位：

| 系統欄位 | 說明 | 建議標題關鍵字 |
|---------|------|--------------|
| drug | 藥品名稱（英文）| 藥品名、drug |
| cname | 中文名稱 | 中文、cname |
| generic | 學名 | 學名、generic |
| brand | 商品名 | 商品、brand |
| indication | 適應症 | 適應症、indication |
| pharm | 藥理作用 | 藥理、pharm |
| dosage | 用法用量 | 劑量、用法、dosage |
| caution | 注意事項 | 注意、caution |
| sideEffect | 副作用 | 副作用、side |
| preg | 懷孕分級 | 懷孕、preg |
| appearance | 外觀 | 外觀、appearance |
| cat | 藥品分類 | 分類、cat |
