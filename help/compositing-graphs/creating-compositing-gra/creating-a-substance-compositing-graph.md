---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/creating-a-substance-compositing-graph.html"
breadcrumb-title: ""
description: 學習如何在 Substance 3D Designer 中建立 Substance 合成圖，以建立程序化貼圖工作流程。
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Creating a Substance graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 建立物質圖
user-guide-description: ""
user-guide-title: ""
source-git-commit: c460f605a97021efd2143941c28a977e12452299
workflow-type: tm+mt
source-wordcount: '1107'
ht-degree: 0%
---

# 建立物質圖

在 Designer 中製作貼圖的起點是建立 Substance 圖，無論是從預設模板或空圖。

<a name="create-graph"></a>

## 建立圖

要開始建立新的 [Substance 圖](../../compositing-graphs/substance-compositing-graphs.md)，你可以使用以下其中一種方法：

* 
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  在主畫面，點擊 <b>「新圖表</b> 」按鈕。

  </td>
  <td style="border: 0;" valign="top">

  ![新物質圖對話框 - 從主畫面](creating-a-substance-compositing-graph.resources/newGraphDialog-create-homeScreen.png "建立 新物質圖對話框 - 從主畫面建立"){zoomable="yes"}

  </td>
  </tr>
  </table>

* 
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  在檔案總管中任何&#x200B;*現有*&#x200B;的套件項目[，點擊 <b>RMB</b>，然後在情境選單中切換到<b>新 > Substance 圖表</b>。](../../interface/the-explorer-window/the-explorer-window.md)

  </td>
  <td style="border: 0;" valign="top">

  ![新實體圖對話框 - 從 Explorer](creating-a-substance-compositing-graph.resources/newGraphDialog-create-explorer.png "建立 新 Substance 圖對話框 - 從 Explorer 建立"){zoomable="yes"}

  </td>
  </tr>
  </table>

* 
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  在主工具列中，點擊![](creating-a-substance-compositing-graph.resources/image2021-6-22-20-36-44.png)<b>「新物質圖表</b>」按鈕。

  </td>
  <td style="border: 0;" valign="top">

  ![新實體圖對話框 - 從主工具列](creating-a-substance-compositing-graph.resources/newGraphDialog-create-mainToolbar.png "建立 新物質圖對話框 - 從主工具列建立"){zoomable="yes"}

  </td>
  </tr>
  </table>

* 
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  在主選單中，請前往 <b>檔案>新>物質圖表......</b>

  </td>
  <td style="border: 0;" valign="top">

  ![](creating-a-substance-compositing-graph.resources/newGraphDialog-create-mainMenu.png)

  </td>
  </tr>
  </table>

* 按下 <b>Ctrl+N</b> （Windows）/ <b>Cmd+N</b> （macOS）按鍵。

無論你選擇哪種方法，都會顯示 <b>「新物質圖</b> 」對話框。

<a name="graph-templates"></a>

## 圖範本

無論用哪種方法建立新的 Substance 圖，你都會 <b>看到「New Substance 圖</b> 」的對話框，讓你可以設定新的圖。

![新物質圖對話框 - 材料](creating-a-substance-compositing-graph.resources/newGraphDialog-materials.png "新物質圖對話框 - 材料"){zoomable="yes"}

### 範本

Designer 包含帶有預設節點的圖形範本，幫助你更快上手。 它們可能包含 [輸出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 節點，這些簡單的節點用來傳遞數值給這些輸出——例如 [統一顏色（Uniform color](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md)）以及 [輸入](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input-color/input-color.md) 節點。

雙擊列表中的範本，或選取該範本並點擊 <b>建立</b> 按鈕，使用該範本建立新的物質圖表。 預設情況下，新圖會被放入一個新的未儲存套件中。

>[!TIP]
>
> 從零開始
> 
> 若要從完全空白的圖表開始，請在「Empty」類別中選擇 <b>Empty</b> 範本。

>[!NOTE]
>
> 切換範本
> 
> 如果你選錯範本， *建立圖表後無法* 切換到其他範本。
> 
> 要將現有的圖表移植到另一個範本，你可以使用相應的範本建立一個新的圖表，然後複製貼上你的圖表到新的模板。 視情況重新連接節點，特別是輸出節點。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

每個範本都會依其標籤和副標題列出。

副標題提供了更多關於 *範本使用情境* 的背景：它所基於的材質模型、要整合的軟體等等。

在 <b>縮圖</b> 模式下，字幕會以較暗且較小的文字置於標籤下方。

在清單、套件與目錄檢視模式中，副標題會附加於標籤&#x200B;*後：標籤 - 字幕*。</b> <b></b> <b></b><b>

</td>
<td width="25.00%" style="border: 0;" valign="top">

![新物質圖表對話框 - 縮圖卡片](creating-a-substance-compositing-graph.resources/newGraphDialog-thumbnailCard.png "新物質圖表對話框 - 縮圖卡片")

</td>
</tr>
</table>

<a name="material-samples"></a>

### 材料樣本

<b>材料範例</b>類別包含[精選的圖表](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md)，供學習與實驗。

你也可以直接從主畫面 <b>使用「前往取樣</b> 」按鈕存取這些樣本。

所有範例皆基於 [OpenPBR 材質模型](../../interface/3d-view/material-properties/material-properties.md#openpbr)。

![材質範例 - 主畫面橫幅](creating-a-substance-compositing-graph.resources/materialSamples-banner.png "材質範例 - 主畫面橫幅"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 資訊提示

將每個範本項目的資訊圖示滑鼠移至，會顯示一個提示，裡面有關於該範本的額外資訊：

<b>類型：</b> 範本所要產生的資產類型。 這可以在圖屬性](../../compositing-graphs/graph-parameters/graph-parameters.md)中編輯[。

<b>說明：</b> 關於範本的詳細資訊，如其整合的工作流程、預期使用情境及使用建議。

<b>輸出：</b> 範本 [中的輸出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 節點（如果有的話）。

</td>
<td style="border: 0;" valign="top">

![新實體圖對話框 - 範本提示](creating-a-substance-compositing-graph.resources/newGraphDialog-tooltipTemplate.png "新物質圖對話框 - 範本提示"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 檢視模式

範本清單可透過 <b>「檢視模式</b> 」按鈕以不同模式顯示。

所選分類與專案檔案所執行的篩選會在所有檢視中套用。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![新物質圖對話框 - 檢視模式](creating-a-substance-compositing-graph.resources/newGraphDialog-viewModes.png "新物質圖對話框 - 檢視模式"){zoomable="yes"}

</td>
</tr>
</table>

+++檢視模式
![新物質圖對話框 - 縮圖檢視](creating-a-substance-compositing-graph.resources/newGraphDialog-viewMode-thumbnails.png "新物質圖對話框 - 縮圖檢視"){zoomable="yes"}



<b>縮圖</b>

卡片上有縮圖，提供範本類型的預覽或圖示。

![新實體圖對話框 - 列表檢視](creating-a-substance-compositing-graph.resources/newGraphDialog-viewMode-list.png "新物質圖對話框 - 列表檢視"){zoomable="yes"}



<b>列表</b>

範本僅依標籤列出。

![新實體圖對話框 - 套件檢視](creating-a-substance-compositing-graph.resources/newGraphDialog-viewMode-packages.png "新實體圖對話框 - 套件檢視"){zoomable="yes"}



<b>套裝</b>

範本依標籤列出，作為其所屬套件檔案的子範本。

將滑鼠移至套件檔案項目，即可顯示工具提示及其完整路徑。

![新實體圖對話框 - 目錄檢視](creating-a-substance-compositing-graph.resources/newGraphDialog-viewMode-directories.png "新實體圖對話框 - 目錄檢視"){zoomable="yes"}



<b>目錄</b>

範本依標籤列出，作為所屬套件檔案目錄的子目錄。

將滑鼠移至目錄項目，即可顯示工具提示及其完整路徑。

+++

### 屬性

選擇範本後，你可以設定新圖表的基本資訊。 建立圖後，任何時間都可以更改。

<b>圖名</b>：圖的識別碼。 它必須對特定套件唯一，且不能包含空格和某些特殊字元。

<b>大小</b>：圖表的父解析度，將控制大多數節點的輸出解析度——詳情請參閱 [輸出大小](../../compositing-graphs/output-size/output-size.md) 頁面。 寬度和高度預設是連結在一起的，你可以點擊寬高組合框之間的連結按鈕來解除連結。

<b>建立圖表：</b>你可以用這個組合框建立&#x200B;*新*&#x200B;圖形的新套件，或將新圖表加入已載入[於總管](../../interface/the-explorer-window/the-explorer-window.md)面板中的任何&#x200B;*現有*&#x200B;套件。

### 幫助提示

將問號圖示滑停即可顯示提示，並有一個按鈕直接連結到此頁面，方便你隨時回頭查看這份文件。

![新物質圖表對話框 - 說明提示](creating-a-substance-compositing-graph.resources/newGraphDialog-tooltipHelp.png "新物質圖表對話框 - 說明提示"){zoomable="yes"}

<a name="managing-templates"></a>

## 管理範本

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 依類別篩選

分類用來將依使用案例或資產類型相關的範本分組。

使用 <b>分類</b> 組合框選擇你想篩選範本的類別。

</td>
<td width="41.67%" style="border: 0;" valign="top">

![新實體圖對話框 - 依類別](creating-a-substance-compositing-graph.resources/newGraphDialog-categories.png "篩選新物質圖對話框 - 依類別篩選"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

範本的範本資料中可能有分類<b></b> [圖屬性](../../compositing-graphs/graph-parameters/graph-parameters.md)，作為篩選工具，縮小範本清單：

&lt;category>;&lt;subtitle>&lt;/category>

自訂分類可在專案檔案提供的範本中設定（見下文）。 接著，這些類別會被加入組合框的清單中。

</td>
<td width="50.00%" style="border: 0;" valign="top">

![新實體圖對話框 - 設定模板分類](creating-a-substance-compositing-graph.resources/newGraphDialog-templateCategorySetup.png "新物質圖表對話框 - 設定模板分類"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 依專案檔案篩選

如果任何活躍 [專案檔案](../../interface/preferences-window/project-settings/project-settings.md) 提供一個或多個範本路徑，則在這些路徑中找到的套件檔案中的圖表會被加入範本清單。

接著，使用 <b>「依專案檔案</b> 篩選」按鈕，將範本清單縮小到特定專案檔案提供的範本。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![新 Substance 圖表對話框 - 依專案檔案](creating-a-substance-compositing-graph.resources/newGraphDialog-projectFiles.png "篩選 新 Substance 圖表對話框 - 依專案檔案篩選"){zoomable="yes"}

</td>
</tr>
</table>
