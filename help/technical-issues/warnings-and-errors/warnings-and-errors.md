---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/technical-issues/warnings-and-errors.html"
breadcrumb-title: ''
description: 在 Substance 3D Designer 中尋找常見問題與錯誤的解決方案，快速排除問題。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Warnings and errors
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 警告與錯誤
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---


# 警告與錯誤

本頁說明 Substance 3D Designer[&#128279;](https://www.adobe.com/tw/products/substance3d-designer.html) 中可能出現的警告與錯誤訊息的回報，並連結到根據警告來源的故障排除方法。

## 概觀

在 Designer 中工作時，你可能會遇到警告和錯誤訊息，告知你專案中出現問題：

* **警告**&#x200B;以黃色&#x200B;*文字顯示*，提醒您注意可能因缺乏輸入或設定錯誤而導致不良結果的問題。他們通常 *不會阻擋* 你的作品。
* **錯誤**&#x200B;以紅色&#x200B;*文字顯示*，表示計算失敗、意外結果或無法執行任務。他們通常 *會阻擋* 你的工作。

通常，警告和錯誤會顯示在觸發它們的項目上，並 *會在該項目的每個父* 項目中顯示。 以下是常見的警告與錯誤報告地點清單：

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### 總管

對於檔案總管[&#128279;](../../interface/the-explorer-window/the-explorer-window.md)面板中任何有警告的項目，該警告會在列表中該項目條目最右側邊緣顯示![](../../assets/warning-icon.png)。將游標停留在該圖示上幾秒鐘，會顯示 *一個詳細列出所有警告的工具提示* 。

他們遵循以下規則：

* 如果該項目被置於其他物品下方（例如資料夾），該物品會因摺疊而顯示警告。
* 警告清單是 *累積性的*，因為它們是物品的警告 *與* 其子項目所有表面警告的總和。
* 包裹內容物中回報的所有警告都會顯示到 *包裹* 項目中，並加入 *包裹本身* 的警告中。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/warning-overview-explorer.png){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### 圖視圖

對於圖形檢視面板中[任何有警告的項目，該警告會在視窗左下角&#x200B;*以彩色文字*](../../interface/the-graph-view/the-graph-view.md)顯示。如果警告是由特定節點觸發，該節點會有 ![](../../assets/warning-badge.png) 警告徽章。 將游標停留在該徽章上幾秒鐘，會顯示 *一個詳細列出所有警告的提示* 。

他們遵循以下規則：

* 如果一個實例化到其他主機圖中的來源圖&#x200B;*有一個或多個警告，[該來源圖的實例節點](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)將有一個**`The referenced data has some warnings`警告。*
* 警告清單是 *累積性的*，因為它們是圖的警告 *與* 其子節點所有警告的總和。
* 圖表中所有的警告都會在 Explorer 面板中回報該圖表的項目上。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/warning-overview-graph.png){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### 屬性

對於屬性面板中[任何有警告的項目，該警告會在列表中該項目條目最右邊的圖示顯示![](../../assets/warning-icon.png)。](../../interface/properties/properties.md)將游標停留在該圖示上幾秒鐘，會顯示 *一個詳細列出所有警告的工具提示* 。

他們遵循以下規則：

* 如果該項目被置於其他項目下方（例如區塊標題），該項目若被摺疊，則會顯示警告。
* 警告清單是 *累積性的*，因為它們是物品的警告 *與* 其子項目所有表面警告的總和。
* 如果[&#128279;](../../function-graphs/function-graphs.md)應用於[輸入參數](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)的函式圖包含一個或多個警告，該參數項目將只有&#x200B;*一個*`The [x] parameter's function has some warnings`警告。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/warning-overview-properties.png){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### 主機

警告和錯誤都會在&#x200B;**主控台**&#x200B;面板中回報，你可以透過&#x200B;**主選單[&#128279;](../../interface/the-main-toolbar/the-main-toolbar.md)的 Windows** 選單進入。你可以將警告和錯誤與其他主控台條目隔離，方法是將 **頻道** 設定設為 `ErrorMgr`。

>[!NOTE]
>
> 由於主控台中的所有文字皆可&#x200B;**&#x200B;選擇，您可以使用此面板&#x200B;*輕鬆複製警告與錯誤訊息*，並貼上至本文件的&#x200B;**&#x200B;本地搜尋**&#x200B;工具或任何網路搜尋引擎。這加快了尋找故障排除指引的過程。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/warning-overview-console.png){width="256px"}

</td>
</tr>
</table>

### 帶有「（# times）」的訊息

在同一&#x200B;**&#x200B;個警告或錯誤中，若某個項目&#x200B;*及其*&#x200B;子項目多次觸發&#x200B;**，這些警告會合併&#x200B;*為一*，並`(# times)`加上後綴，告訴你該警告或錯誤被回報了多少次。

## 類別

以下是你在 Designer 中可能遇到的警告與錯誤清單，依來源排序。 分類標題會連結到他們的專屬頁面，該頁面提供解答說明及解決每個問題的故障排除指南。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 物質圖中的警告

* 未定義輸出節點
* [x] 參數的功能有一些警告
* 參考資料中有一些警告
* 找不到參考資源
* 文字節點使用無效字型

</td>
<td style="border: 0;" valign="top">

### 函數圖中的警告

* 未定義輸出節點
* 當前輸出節點回傳的值為 x
* 有些 Get 節點沒有變數名稱
* 有些 Set 節點沒有變數名稱

</td>
</tr>
</table>

### 依賴性警告

* 無效的依賴套件
* 檢查你的專案中是否有定義別名 &#39;x&#39;
* 找不到與此資源相符的檔案
* 找不到連結檔案
* 找不到色彩空間
* 找不到參考資源
* UV 圖塊會被多次指定
* 無效的 UV 圖塊
