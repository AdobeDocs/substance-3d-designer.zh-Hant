---
name: write-experience-league-markdown
description: |
  Adobe Experience League 發佈的 Markdown 內容撰寫時的語法規則、自訂擴充功能與陷阱。 在創建或編輯任何說明/本倉庫（或其他 Experience League 內容倉庫）頁面時，請使用此技能——標題、連結、圖片、表格、備註/警示區塊、UICONTROL/DNL 標籤、影片嵌入、錨點及已知的渲染陷阱。 資料來源：https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown
source-git-commit: ed17c57a1aa9669a602d4523bdef20cd7d82db75
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 4%
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
* 頁面內錨點會被宣告為標題（自動鎖扣式）或explicit `<span id="anchor-id"></span>` （HTML） / `{: #anchor-id}` （Markdown） 緊接在該詞之前 —請參閱 `help/glossary/glossary.md` 本報告中使用的模式。
* `TOC.md` 區塊錨點在標題/列表後方使用 `{#section-id}` 語法標籤，例如 `Getting started{#getting-started}`。

## 圖片

盡可能使用 Markdown 影像語法：

```markdown
![Alt text](path/to/image.png "Optional hover text")
```

* 該 `![...]` 文本為必修的可存取替代文本。 保持簡潔，然後去做不要使用底線;改用空格或連字號。
* 影像路徑可以相對於 Markdown 檔案或根關係路徑，例如作為 `/help/assets/shared-image.png`。 頁面專屬圖片應歸類於兄弟 `<page-name>.resources/` 資料夾（例如，
  `<page-name>.resources/image.png`). `help/assets/` 是一個舊有共享資料夾;請勿在那裡新增專屬頁面圖片。
* 可選的影像查詢參數可控制 CDN 處理：
  `?width=750&format=png&optimize=medium`. 這些參數要保留在影像上網址，在任何屬性區塊之前。
* 在結束 `)`之後立即加入影像屬性：
  `![Alt text](image.png "Hover text"){width="300" align="center"}`.
  `width` 是像素值或視圖面積的百分比;影像縮放按比例來說。 支援的對齊值為 `center` 和 `right`。
  `valign` 不支援。
* 使用 `modal="regular"` 或 `zoomable="yes"` 製作可點擊放大的圖片：
  `![Alt text](image.png){width="100" zoomable="yes"}`. 不要合併點擊放大並附有圖片連結;超連結優先。
* 要將圖片連結到另一個頁面，請將圖片包裝成 Markdown 連結：
  `[![Alt text](image.png)](../target/target.md)`.
* 對於大型影像，在可行的情況下，至少提供 640 像素的來源寬度，除非需要，否則不要使用約 2000 像素，並且圖片檔案保持在以下可能的話，5 MB。 該管線可接受最高 100 MB 的檔案，但檔案超過20 MB 的失敗驗證，且文章通常不應包含超過100張圖片（有些舊指引說是200張;請使用更嚴格的限制）。

只有在 Markdown 無法表達所需的版面配置時才使用 HTML特別的表格或客製化的線上呈現。 支援的 HTML 影像形式是：

```html
<img src="image.png" alt="Alt text" />
```

* 務必提供有意義的 `alt` 屬性，並使用親屬或根關係 `src` 與 Markdown 影像一致。
* 對於保留的內嵌 HTML 中的 HTML 圖片，請 add
  `data-preserve-html="true"` 當需要時，會被包含標籤周圍加價。 例如：

  ```html
  <div data-preserve-html="true" align="center">
    <img src="my-page.resources/preview.gif" alt="Preview" />
  </div>
  ```

* 要啟用 HTML 圖片的點擊縮放功能，請
  `class="modal-image"` 在標籤上 `<img>` 。
* 請勿使用不支援的 HTML 屬性或依賴 `valign`;偏好 Markdown寬度與對齊屬性。

## 表格

一般表格內容偏好使用原生 Markdown 表格：

```markdown
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

* 在桌前劃一條空白線。 Markdown 表格至少需要一個標頭列與一列正文列;使用HTML表格表示單列或無標頭桌子。
* 每個標頭分隔格至少使用三個連字號，且保持相同每排管子的數量。 逃逸字面上的管道，作為 `\|` 或
  `&vert;`.
* 必要時在分隔列使用對齊標記：
  `|---|:---:|---:|` 用於左、中、右三側的排列。
* 在 Markdown 表格儲存格中支援內嵌 HTML 以區隔段落，且基本清單。 用於 `<p>` 分段、 `<br>` 換行，以及
  `<ul>`/`<ol>` 有 `<li>` 清單項目。 新增
  `data-preserve-html="true"` 當周圍的儲存庫標記。

  ```markdown
  | Header | Details |
  |---|---|
  | Text | First paragraph.<p>Second paragraph.<br>New line.<ul><li>Item</li></ul> |
  ```

* 避免使用非常寬且非常高的桌子;這些桌子難以操作。
在表格中使用內嵌程式碼要小心，因為長程式碼可能會強行說明欄位寬度不成比例。
* 要選擇 Markdown 表格的表格版面，請在表格，中間以空白線分隔：

  ```markdown
  {style="table-layout:fixed"}
  ```

  當需要長文字或程式碼需要彈性時，使用 `table-layout:auto` （預設）欄寬。 用於 `fixed` 平衡欄位，例如包含尺寸相近的影像。

當 Markdown 無法表達所需的結構時，請使用 HTML 表格，例如省略標頭、將儲存格與跨度合併、平衡欄位或對齊儲存格內的內容：

```html
<table style="table-layout:fixed">
  <tr>
    <th>Property</th>
    <th>Value</th>
  </tr>
  <tr>
    <td align="center">Example</td>
    <td>Details</td>
  </tr>
</table>
```

* 支援的表格元素包括 `<table>`、 `<tbody>`、 `<thead>`&#x200B;`<tfoot>`、
  `<tr>`、、`<th>`&#x200B;`<td>`、`<col>`&#x200B;`<colgroup>`、以及 ，以及 ，以及 支持內嵌元素如 `<p>`、 `<br>`、 `<ol>`&#x200B;`<b>`&#x200B;`<i>`&#x200B;`<ul>`和
  `<li>`.
* 不要在 HTML 表格中使用 Markdown 語法。 例如，Markdown筆記、圖片和連結可能會直接呈現;請改用 HTML 語法。
  `UICONTROL` 而 `DNL` 本地化標籤則是例外。
* 當 `align="left"`使用 、 `align="center"`或 `align="right"` 在儲存格上時需要。 HTML 資料表不能包含巢狀資料表。
* 在開頭標籤上設定 HTML 表格的佈局：
  `<table style="table-layout:auto">` 或
  `<table style="table-layout:fixed">`.
* 對於無邊框的單列 HTML 表格，請使用
  `<tr style="border: 0;">`.

## 程式碼

* 內嵌代碼：單一回溯刻數。
* 有圍欄區塊：三重回溯，並可選語法語言標註（` `&#x200B;``python `、 ` ``&#x200B;`javascript `，等）。

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

支援類型：`NOTE`， `TIP`， `IMPORTANT`， `CAUTION`&#x200B;`WARNING`，
`ADMINISTRATION`, `AVAILABILITY`, `PREREQUISITES`, `ERROR`, `INFO`, `SUCCESS`.

## 影片嵌入

Experience League 不支援直接嵌入 MP4 或 YouTube 影片於 `[!VIDEO]` 區塊中。 如果你需要動畫預覽，可以在頁面的姊妹 `.resources` 資料夾裡用 GIF，必要時用內嵌 HTML 置中。

```markdown
<div data-preserve-html="true" align="center">
  <img src="my-page.resources/my-preview.gif" alt="My preview" />
</div>
```

不要用於 `[!VIDEO]` 本地 MP4 檔案、遠端 MP4 檔案或 YouTube 網址——發佈流程會拒絕這些檔案，CI 會失敗。

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

請參閱 AGENTS.md 的「頁面前言」區塊，以了解本倉庫的常規內容頁，以及 `metadata.md` 倉庫層級的內容繼承的田地。