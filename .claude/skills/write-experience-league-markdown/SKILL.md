---
name: write-experience-league-markdown
description: ""
Source: https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown
source-git-commit: 9f19a0232c1f355ba2450995b4a6d23b7ed846d1
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 6%

---


# 寫作體驗聯盟折扣

Experience League 透過自訂流程渲染 GitHub 風味的 Markdown還有自己的擴充功能和渲染特性。 標準的GFM大致上是可行的，但以下物品為經驗聯盟專屬——錯誤且內容豐富要麼是 lint/link-check CI 失敗，要麼在 live 網站上呈現錯誤。

## 標題

* `#` 直到 `#####` （第1至5級）。 該頁面 `title` 的前言是實際上是 0 級;正文中的第一個 Markdown 標題應該是單一 `# Level 1` 標題與頁名相符（或接近）。
* 不要隨意跳過關卡;迷你目錄是從標題產生的。

## 文字格式

* `**bold**`, `*italic*`, `***bold and italic***`.
* 以反斜線`\*`（、 `\_`等）逃離字面特殊字元。
* **標題/標題中的&amp;符號** 必須寫出（`and`）或編碼為
  `&amp;` — 標題中的 raw `&` 可能會破壞解析。
* **用作字面文字（非真實 HTML）的角括號** 必須編碼：
  `<placeholder>` → `&lt;placeholder&gt;`。
* **從文字處理器貼上的智慧引號** 必須編碼，不能像字面捲字：左雙、`&#8220;`右雙，`&#8221;`撇號/右單曲 `&#8217;`。

## 列表

* 編號清單：每個項目都以 `1.` （或 `1)`）開頭 — GitHub/Experience聯盟自動號碼，不管輸入字面數字。
* 項目符號列表：使用 `*`、 `-`、或 `+`，但 **不要混合項目符號在同一個清單/文件**&#x200B;裡。
* `TOC.md` 列表巢套使用 `+` 一致 — 跟隨現有檔案的子彈風格，而不是引入不同的方式。

## 連結

* 內部交叉參考必須是 **Markdown 連結的相對**&#x200B;目標 `.md` 檔案： `[Overview](../../overview.md)`。
* 外部參考必須是 **絕對** 網址。
* 錨定到另一頁的標題/跨度：附加 `#anchor-id`，例如
  `[Mesh](../../glossary/glossary.md#mesh)`.
* 頁面內錨點會被宣告為標題（自動鎖扣式）或明確地在該詞之前——`<span id="anchor-id"></span>`請參閱 `help/glossary/glossary.md` 本報告中使用的模式。
* `TOC.md` 區塊錨點在標題/列表後方使用 `{#section-id}` 語法標籤，例如 `Getting started{#getting-started}`。

## 圖片

* `![Alt text](path/to/image.png "Optional hover title")`.
* 支援可選的大小/優化查詢參數：
  `![Adobe logo](my-page.resources/logo.png?width=750&format=png&optimize=medium)`.
* **替代文字必須不包含底線——因為下線** 不會正確呈現;改用連字號或空格。
* 專屬頁面的圖片會存放在同一個資料夾 `<page-name>.resources/` 中在 旁邊 `.md`，相對參考（例如
  `<page-name>.resources/image.png`). `help/assets/` 是共享的遺產資料夾 — 不要在那裡新增圖片（見 CLAUDE.md）。

## 表格

* 管道分隔，並以連字號標頭分隔符列：

  ```markdown
  | Header | Another header | Yet another header |
  |--- |--- |--- |
  | row 1 | column 2 | column 3 |
  | row 2 | row 2 column 2 | row 2 column 3 |
  ```

* 表格前必須有空行，否則表格無法被渲染成表格。
* 表格無法乾淨地保存多段或複雜的區塊內容cell — 此儲存庫需要在資料表儲存格內放置圖片/清單（例如比較表在 `overview.md`，它會退回到內嵌 HTML（`<div>`， `<b>`， /`<ul>``<li>`） 每個`data-preserve-html="true"`標記是為了避免管線剝光。 還是照這個現有模式走吧除非必要，否則會發明新的內嵌 HTML。

## 程式碼

* 內嵌代碼：單一回溯刻數。
* 有圍欄區塊：三重回溯，並可選語法語言標註（` ```python `、 ` ```javascript `，等）。

## 筆記/警示區塊

自訂區塊引號語法，每個區塊一個類型，區塊間空格引號行標籤與正文：

```markdown
>[!NOTE]
>
>This is a standard NOTE block.

>[!TIP]
>
>This is a standard TIP.

>[!IMPORTANT]
>
>This is an IMPORTANT note.
```

支援類型：`NOTE`， `TIP`， `IMPORTANT`， `CAUTION``WARNING`，
`ADMINISTRATION`, `AVAILABILITY`, `PREREQUISITES`, `ERROR`, `INFO`, `SUCCESS`.

## 影片嵌入

```markdown
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

## UICONTROL 標籤

會將 UI 元素名稱（按鈕標籤、選單項目、欄位名稱）內嵌包裝，所以本地化管線知道要檢查翻譯字串並落下如果沒有英文標籤，則回到：

```markdown
Click [!UICONTROL Save] to apply changes.
Go to [!UICONTROL Tools] > [!UICONTROL Settings].
```

用它來處理教學文字中每個字面上的 UI 標籤（選單）物品、按鈕名稱、對話標題、面板名稱）。

## DNL 標籤（「請勿定位」）

包裝產品名稱、第三方功能名稱，或任何必須的片語絕不被機器翻譯：

```markdown
Use [!DNL Adobe Analytics] to track metrics.
The [!DNL Target] implementation requires configuration.
```

在這個倉庫中，可以用它來命名像 `[!DNL Substance 3D Designer]`是 ，
`[!DNL Substance 3D Sampler]`，等等，關於每頁首次或顯著提及，與現有頁面一致。

## 內嵌 HTML

允許使用原始 HTML（這個倉庫 `markdownlint_custom.json` 會停用 MD033正因如此），但只有透過當標籤攜帶 `data-preserve-html="true"`時，管線 。 保留內嵌 HTML對於 Markdown 無法表達的情況，（表格儲存格內的圖片/列表，
`<span id="...">` 錨點）而非作為 Markdown 的通用替代品。

## 前言

請參閱 CLAUDE.md 的「頁面前言」區塊，了解本倉庫的常規內容頁，以及 `metadata.md` 倉庫層級的內容繼承的田地。