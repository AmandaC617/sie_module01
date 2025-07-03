# 網站 AI 就緒度與技術健康度檢測工具

本專案是一個前端靜態網站工具，協助用戶分析網站在 LLM 世代的 AI 友善度、技術健康度與內容策略，並支援一鍵下載分析報告與歷史紀錄查詢。

## 功能特色

- 網站技術健康度自動檢測（robots.txt、sitemap、結構化資料等）
- Open Graph/Meta 標籤、主要 CTA、FAQ 結構化資料自動偵測
- AI 生成消費者常見問題與內容覆蓋度分析
- AI 生成改善建議與消費者旅程洞察
- 分析報告一鍵下載（JSON/CSV/PDF）
- 分析歷史紀錄 localStorage 快速查詢
- 現代化美觀 UI，支援行動裝置

## 快速開始

1. **下載或 clone 本專案**
   ```bash
   git clone https://github.com/AmandaC617/sie_module01.git
   cd sie_module01
   ```

2. **直接用瀏覽器開啟 `index.html` 即可使用**

---

## GitHub Pages 自動部署

### 如何啟用 GitHub Pages

1. 前往你的 repo：[https://github.com/AmandaC617/sie_module01](https://github.com/AmandaC617/sie_module01)
2. 點選「Settings」→ 左側選單「Pages」
3. 在「Build and deployment」區塊：
   - Source 選 `main` branch
   - 資料夾選 `sie_module01/`
   - 按 Save
4. 幾分鐘後，GitHub Pages 網址會顯示在上方（通常為：  
   `https://amandac617.github.io/sie_module01/`）

### 注意事項

- 每次 push 會自動觸發 GitHub Pages 重新部署
- 若遇 404，請確認 `index.html` 是否在 `sie_module01/` 資料夾下，且 Pages 設定正確

---

## 進階自動化部署（可選）

如需自動化 workflow，可在 `.github/workflows/gh-pages.yml` 加入：

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [main]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Deploy static site
        uses: peaceiris/actions-gh-pages@v4
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./sie_module01
```

---

## 貢獻與授權

歡迎 PR 與 issue！  
本專案採用 MIT License。 