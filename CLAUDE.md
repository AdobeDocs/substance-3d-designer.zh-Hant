---
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---
# CLAUDE.md

此檔案提供使用 Claude Code （claude.ai/code） 在本儲存庫中操作程式碼時的指引。

# Substance 3D Designer 文件

此資料庫包含 Substance 3D Designer 的文件。 沒有應用程式碼、建置步驟或測試套件——儲存 *庫是* 內容，以 Markdown 撰寫並發佈在 [Adobe Experience League](https://experienceleague.adobe.com/docs/substance3d-designer.html?lang=en) 上。

# 儲存庫結構

* `help/` — 所有文件內容，並以鏡像目錄的方式組織。
* `help/guide/TOC.md` ——目錄。 每個條目都是指向頁面 Markdown 檔案的相對連結（根點為 `/help/...`）。 `TOC.md`同時也攜帶頁面樹元資料（`user-guide-title`、`breadcrumb-title``nudge`區塊錨點，如 `{#section-id}`）。
* `help/assets/` — 分享的、非頁面特定圖片（e.g. app圖示在頁面間重複使用）。
* `help/glossary/glossary.md` — 一個大型詞彙表頁面，按字母順序組織，並以錨點跨度`<span id="term"></span>`（）作為透過片段交叉連結 `#term` 的標示。
* `metadata.md` — 倉庫層級前置事項（雲端/解決方案/產品 ID 等 `git-repo`） 該 會被每個 `TOC.md`繼承。 僅在整個倉庫的元資料變更時才編輯此處;頁面專屬的元資料應放在頁面本身的前置項目中。
* `redirects.csv`， `linkcheckexclude.json`， ， `markdownlint_custom.json`， — `pipeline.opts` 發佈管線設定（重定向、連結檢查例外、lint 規則覆寫、管線選項）。
* `fix-image-names.py` — 一次性工具，能用括號後綴重新命名 `help/assets` 圖片（例如 `foo(1).png` → `foo_1.png`），並重寫所有 Markdown 參考以匹配。 這不屬於任何常規工作流程;只有當這些檔名再次出現時才手動執行。

## 資料夾/目錄慣例

對於 的 `help/guide/TOC.md`每個項目：
* 在 下有一個對應的資料夾 `help/`，採用與目錄相同的巢狀方式。
* 那個資料夾裡有一個 Markdown 檔案，名稱是頁面標題的烤肉盒版本。
* 如果頁面有專屬媒體（圖片、GIF、影片），則會存在一個名為 `<md-file-name>.resources`的同檔子資料夾中。

新增或移動頁面時， `TOC.md` 更新與資料夾佈局必須同步。

## 頁面前言

一般內容頁會使用前言區塊，例如：

```yaml
---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/<section>/<page>.html"
breadcrumb-title: ""
description: <one/two sentence SEO description>
helpx_creative_field: ""
helpx_description: Designer > <Section> > <Page>
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: <Page title>
user-guide-description: ""
user-guide-title: ""
---
```

保持 `description` 準確與簡潔——它用於 SEO/搜尋摘要。

# 內容創作規則

* 英語是真理的來源;其他語言都是從英語翻譯而來。
* 所有指向其他文件頁面的連結必須是 **相對** 連結;所有指向外部資源的連結必須是 **絕對** 連結。
* 內容是以 GitHub 風格的 Markdown 撰寫，並搭配 Experience League 自訂的擴充功能/陷阱，詳情可 [在此](https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown)處說明。 具體細節就用 `write-experience-league-markdown` 技能（如果有的話）。
* 每個提交的變更都會經過自動的 lint 檢查和 CI 中的連結驗證（見下文）——在假設有規則適用或連結需要修正之前，先檢查 `markdownlint_custom.json` 並 `linkcheckexclude.json` 確認。

# 驗證/配置

* `.github/workflows/validate-articles.yml` 運行於 PR 上，並推送至 `main` （以及透過 `retest` PR 註解），呼叫共享 `Adobe-Enterprise-Docs/workflows` 的可重用工作流程以 lint Markdown 並驗證連結。 這個儲存庫中沒有本地對應的腳本——CI 是通過/不通過的真實來源。
* `.github/workflows/mirror.yml` 推送時鏡 `main` 像到公共倉庫;這是基礎設施，不是內容變更必須觸及的東西。
* `markdownlint_custom.json` 擴充共享 `markdownlint.json` 規則集，並停用數條與 Experience League 自訂 Markdown 擴充（如內嵌 HTML、非標準強調）衝突的規則（MD005、MD007、MD018、MD032、MD033、MD034、MD037、MD040）。 不要為了符合這些被禁止的規則而「修正」內容。
* `linkcheckexclude.json` 連結模式（目前 `example.com`為 /`example-end.com`）被列入白名單，連結檢查器應該跳過。

# 工作慣例

* 這是以發佈說明為主的文件——發佈說明存於 `help/release-notes/`，每個版本一個資料夾（例如`version-16-0`），以及`all-changes``old-versions`彙整頁面。新增新版本時，請依照現有版本資料夾作為範本。
