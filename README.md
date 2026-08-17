# 節次課表

以節次為單位的可編輯課表，單頁、離線可用、可安裝到手機主畫面。

## 部署到 GitHub Pages

1. 把這個資料夾裡的所有檔案放進 repo 根目錄（或 `docs/`）。
2. Settings → Pages → Source 選 `Deploy from a branch`，分支選 `main`、資料夾選 `/ (root)` 或 `/docs`。
3. 等網址出現後用手機開。

檔案：

| 檔案 | 用途 |
| --- | --- |
| `index.html` | 整個 app（HTML/CSS/JS 都在裡面） |
| `manifest.webmanifest` | 安裝資訊：名稱、圖示、standalone 顯示 |
| `sw.js` | Service worker，離線快取 |
| `icon-192.png` / `icon-512.png` | 一般圖示 |
| `icon-maskable-512.png` | Android 自適應圖示 |
| `apple-touch-icon.png` | iOS 主畫面圖示 |

全部用相對路徑，放在 `使用者名稱.github.io/repo/` 這種子目錄也能運作。

## 安裝成 app

- **iPhone／iPad**：用 Safari 開網址 → 分享鍵 → 加入主畫面。從主畫面開啟就沒有網址列和底部工具列。
- **Android**：用 Chrome 開網址 → 網址列旁的安裝鍵，或畫面上的「安裝到主畫面」按鈕。
- **電腦**：Chrome / Edge 網址列右側的安裝圖示。

## 操作

- 點空格新增時段；**長按再往下拖**可一次選多節（手機）。電腦直接按住拖曳。
- 點方塊編輯或刪除。
- 圖例可點，用來淡化不想看的分類。
- 「設定」可改節次時間、顯示天數、學期起訖日。
- 「匯出行事曆」產生 `.ics`，匯入 Google／Apple 行事曆會變成每週重複到學期末的事件。
- 資料存在瀏覽器的 localStorage，換裝置前請先「匯出檔案」備份。

## 更新版本

改完 `index.html` 後，把 `sw.js` 第一行的 `timetable-v1` 改成 `timetable-v2`，否則舊的快取會繼續被用。
