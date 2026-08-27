---
name: generate-node-documentation
description: ""
source-git-commit: 69f546a26d2e09127b1c79ef4003e235536289da
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 4%

---


# 產生節點文件

這個倉庫中的每個葉節點參考頁面都遵循一個一致的結構。 就是這樣技能是該結構的專精。 典範且完整的範例為
`.../node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md` —有疑問時，打開並鏡像它。

此技能僅涵蓋節點頁面 *結構*。 基礎體驗聯盟 Markdown（備註/警示區塊、相對連結與絕對連結、UICONTROL/DNL、影像查詢參數，Lint Gotchas）跟著技巧 `write-experience-league-markdown` 走。

## 節點頁面所在位置（資料夾/目錄慣例）

* 每個節點一個資料夾，位於匹配的類別/子類別路徑下，例如：
  `.../node-library/<category>/<subcategory>/<node-name>/<node-name>.md`.
* 該資料夾命名為 kebab-case 節點標題;它包含&#x200B;**一個**`.md`檔案名稱完全相同。
* 頁面內嵌的所有媒體（圖示、範例圖片、GIF 都存在於姊 **妹節點中
  `<node-name>.resources/`**`.md`資料夾 與 並列 ，並以相對路徑（例如 `<node-name>.resources/<file>.png`）。 不要將節點頁面指向共享 `help/assets/` 資料夾——也就是逐漸淘汰的舊有模式;新 和編輯後的頁面會使用自己的 `.resources` 資料夾。
* 每一頁在 中都有對應的條目。`help/guide/TOC.md`在新增或移動頁面、更新 `TOC.md` 與資料夾配置（參見 CLAUDE.md 的資料夾/目錄）大會）。

## 前言

節點頁面僅使用 **最小** 區塊， `title` 且採用麵包屑式
`description`. （這與 11 欄位的舊有區塊文件 CLAUDE.md 不同常規內容頁。）

```yaml
---
title: "Shape splatter v2"
description: "Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Generator > Pattern > Shape splatter v2"
---
```

## 車體結構

從頭到尾，前面以下的部分：

### &#x200B;1. H1 冠軍頭銜

每頁只有 `# <Node title>` 一個——正好一個H1。

### &#x200B;2. 圖示/描述表

一個 HTML 表格，一列，兩個儲存格。 左邊格子（`33.33%`）儲存圖示，然後
`In:` 麵包屑;右格（`100.00%`）保持， `## Description` 散文。

```html
<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![<Node title> icon](<node-name>.resources/<node-name>.png "<Node title>")

<b>In:</b> <Category> &gt; <Subcategory>

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

<Description prose.>

</td>
</tr>
</table>
```

描述單元散文慣例：
* 分開段落，（ `<br><br>` 儲存格內的空白行不可靠）。
* 內嵌重音為 `<b>…</b>` / `<i>…</i>`。
* 開場旁白在句首使用 `<i>Note:</i>` / `<i>Tip:</i>` 。
* 在 HTML 裡用`&gt;`來做 `In:` `>` 。以類別為例 /子類別名稱來自節點本身;不要自己創造。

### &#x200B;3. 可選的呼喊

`>[!INFO]`、、 `>[!TIP]`、 `>[!NOTE]`等等。接 **在** 圖示/描述表之後（非在牢房內）。 根據技能的語法。`write-experience-league-markdown`

### &#x200B;4. 輸入

只有當節點有輸入腳位時才包含。 在航向前加錨。

```markdown
<a name="inputs"></a>

## Inputs

|  |  |
|:---|:---|
| <b>Background height</b> <i>Grayscale</i> | The base height map in which shapes are scattered.<br><br>The contribution is controlled by the <b>Background input opacity</b> parameter. |
```

* 兩欄、空標題列、 `|:---|:---|` 對齊。
* 每個輸入一列：左格 `<b>Name</b> <i>Type</i>`，右格描述。
* 型別標記是 HTML 斜體 — `<i>Type</i>` — 而非 markdown `*Type*`。

### &#x200B;5. 輸出

形狀與輸入相同，且為 `<a name="outputs"></a>` + `## Outputs`。 僅在節點記錄不同的輸出（許多節點只有單一隱含輸出，且省略此點章節——不要自創一個）。

對於多聲道輸出，將聲道拆分成 `<br>` 和 縮排子點（ `&nbsp;` 參見參考資料）：

```markdown
| <b>Splatter UVW</b> | <b>R</b> - U component of the shapes' UVs.<br><b>G</b> - V component of the shapes' UVs.<br><b>B</b> - The shapes' height. (W)<br><b>A</b> - Packed data:<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- <i>Integer part:</i> The shapes' unique identifier. |
```

### &#x200B;6. 參數

相同表格形狀，但 `<a name="parameters"></a>` 為 + `## Parameters`。 省略整個如果節點沒有參數，則切入區段（切勿輸出空資料表或「無參數」訊息）。
行）。

* **分組參數**：在團體排位：

  ```markdown
  | <b>Positioning</b> |  |
  | <b>Project Input</b> <i>UV Position, World Space Position</i> | Choose whether the projection position is set in 2D/UV or in 3D/World space. |
  ```

* **列舉/多選項值**：在描述儲存格內列出選項，作為
  `<br>`- 分離儀表板列表：

  ```markdown
  | <b>Position distribution mode</b> <i>Integer</i> | The method of distributing the shapes:<br><br>- <b>2D grid:</b> A simple uniform grid.<br>- <b>Poisson disc:</b> Randomly offsets grid cells to prevent overlaps.<br>- <b>Uniform:</b> An even distribution of a set number of shapes. |
  ```

### &#x200B;7. 範例

僅在有範例圖片或 GIF 時才包含。 使用 HTML 圖庫表格;一個 `<td>`每張圖片附有可選說明;三張圖片後換行為新圖片 `<tr>` 。 媒體路徑指向頁面資料夾 `.resources` 。

```html
## Examples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="./<node-name>.resources/<file>.gif" /><br><i>Caption</i>
        </td>
        <td style="border: 0; background: transparent">
            <img src="./<node-name>.resources/<file2>.jpg" /><br><i>Another caption</i>
        </td>
    </tr>
</table>
```

在部分填滿的最後一行中，將尾隨單元格保持空（`<td …></td>`），而不是正在回流。 如果來源沒有說明文字，請省略。

## 典範型別值

重用節點自身的型別措辭;典型值： `Grayscale`， `Color`， `Integer`，
`Float`, `Float2`, `Float3`, `Float4`, `Integer2`, `Boolean`, `Grayscale Input`,
`Color Input`, `(Color value)`, `(Grayscale value)`. 不要發明或「標準化」一個類型節點實際上並沒有使用。

## 表格格規則

* 表格儲存格內沒有原始換行——將行 `<br>` 與 （以及 `<br><br>` 之間）連接段落）。
* 格內的強調為 `<b>`/`<i>`，類型標記永遠 `<i>Type</i>`為 。
* 縮排巢狀子點與 `&nbsp;` 序列。

## 規則/禁忌

* **不要製造** 節點沒有的輸入、輸出或參數;省略而是用區塊代替。 不要改寫、摘要或刪除現有的技術內容——只做重新格式化。
* **保持連結相對於** 其他 `.md` 頁面;外部連結絕對一致。
* **編輯舊頁面時丟棄舊版雜物** ：難度標籤（`**Simple**` / `**Intermediate**` / `**Complex**`），多餘的 `## <Title>`圖示單元內的副標題，像是「沒有附帶圖片於」這樣的短句此頁面。」以及早期遷移中剩餘的空導覽/包裝表。
* **每頁一頁 H1** ;章節使用 `##`，以及輸入/輸出/參數錨點（`inputs` / `outputs` / `parameters`） 必須置於標題前，故橫跨頁
  `#inputs` 連結會解決。
* **新增、改名或移動頁面時保持 `TOC.md` 同步** 。
