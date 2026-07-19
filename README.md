# AI 工作流自動化系統

這是一個可直接部署到 GitHub Pages 的單頁互動網站，介紹一整套 Claude Code 全域 slash command 工作流：把「想法 → 設計 → 實作 → 測試 → 部署 → 團隊對齊」串成一條連續的流程，共 16 個指令、5 組工作流。

🔗 線上瀏覽：**https://draiagent.github.io/AI-Workflow-Automation-System/**

## 五組工作流

| 組別 | 目的 | 指令 |
|---|---|---|
| 知識系統｜Context Loop | 動手寫程式前先建立 context | `/capture-idea` `/open-issue` `/write-spec` |
| Design-to-Code | 設計稿轉程式碼＋自動化測試 | `/figma-to-code` `/e2e-test` `/setup-supabase` |
| 數據分析 | 原始資料在數分鐘內轉為洞察 | `/analyze-excel` `/explore-db` `/notebook-analysis` |
| 部署與營運 | 加速 Release，確保系統穩定 | `/deploy-vercel` `/release-checklist`（`/dockerize` `/aws-plan` 為非必要備用） |
| 團隊對齊 | 圍繞產出的協調與對齊 | `/sync-to-notion` `/team-align` |

涵蓋工具：Obsidian、GitHub、Notion、Figma、Playwright、Supabase、Excel、PostgreSQL、Jupyter、Docker、AWS、Vercel、Chrome。

## 網站特色

- 繁體中文，適合教室投影（大字體、高對比深色主題）
- 單一 `index.html`，無需安裝套件，CSS/JS 皆內嵌
- 頂部互動流程圖，點節點可展開並捲動到對應區塊
- 每組工作流可展開，指令卡片再點一次看詳細說明與現況（可用／待授權／非必要備用）

## 專案結構

```text
AI-Workflow-Automation-System/
├── index.html   # 完整單頁互動網站
├── README.md    # 專案說明
└── .nojekyll    # 關閉 Jekyll 處理
```

## 本機預覽

直接用瀏覽器開啟 `index.html`，或在專案資料夾執行：

```bash
python -m http.server 8000
```

然後開啟 `http://localhost:8000`。

## 更新內容

修改 `index.html` 裡的 `DATA` 陣列即可調整工作流／指令內容，不需要改版面結構。

```bash
git add index.html
git commit -m "更新工作流內容"
git push
```
