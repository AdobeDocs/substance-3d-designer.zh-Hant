---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/manage-parameters.html"
breadcrumb-title: ''
description: 學習如何在 Substance 合成圖中管理與組織參數，以改善工作流程組織。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Manage parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 管理參數
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---


# 管理參數

當你需要以非直接調整參數的方式控制時，Designer 提供幾項實用操作：

* [複製並貼上](#copy-paste-parameters) 節點所有參數的值
* 將節點的值或所有參數儲存到 [預設檔案](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)，之後再用
* [公開](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) 節點參數以便可存取並將它們連結起來
* [根據其他參數的值來隱藏或顯示參數](../../compositing-graphs/visible-control-vis/visible-if-control-visibility-of-inputs-outputs-and-parameters.md)
* 使用 [Substance函數圖](../../function-graphs/function-graphs.md) 來計算參數的值

## 參數動作

用於管理參數的工具可在以下地點取得：

### 全球行動

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

當節點的屬性顯示在屬性底座時，可以透過以下章節標題中的「<b>管理參數</b>」選單全域管理節點參數：

* 對於 [原子節點](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)：特定參數
* 例如 [實例節點](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)：實例參數

</td>
<td width="33.33%" style="border: 0;" valign="top">

![全域「管理參數」選單在屬性](manage-parameters.resources/manage-parameters-menu-global.png "中 全域「管理參數」選單 在「屬性管理」選單"){zoomable="yes"}

</td>
</tr>
</table>

此選單中的動作將影響 *該區塊中列出的所有* 參數：

* <b>揭露參數：</b> 開啟「批次暴露參數」對話框。 對於每個暴露的參數，動作會建立一個新的圖形輸入，並自動根據該圖形輸入設定函式。 在這個專門頁面](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)了解更多關於暴露參數[的資訊。
* <b>複製參數：</b> 請參閱 [下方的「複製並貼上參數](#copy-paste-parameters) 」章節。
* <b>參數貼上：</b> 請參見 [下方的「複製並貼上參數](../../compositing-graphs/manage-parameters/manage-parameters.md) 」章節。
* <b>將參數儲存為預設檔：</b> 在此 [專頁](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)了解更多關於參數預設的資訊。
* <b>從預設檔案套用參數：</b> 在此 [專頁](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)了解更多關於參數預設的資訊。
* <b>重置全部：</b> 將所有參數重置為預設值與範圍。 若函數被應用於任何參數，則會被忽略。

>[!NOTE]
>
> 有些動作對某些原子節點無法執行。 請參見 [下方原子節點的限制](#atomic-nodes-limitations) 。

### 單參數動作

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

如果你想管理 *單一* 參數，請使用參數標籤對面的「<b>管理函式</b>」選單。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![屬性中的](manage-parameters.resources/manage-parameters-menu.png "本地「管理參數」選單 屬性中的本地「管理參數」選單"){zoomable="yes"}

</td>
</tr>
</table>

你可以用三種方式將 Substance 函數圖](../../function-graphs/the-function-graph/the-function-graph.md)套用[到該參數：

* <b>以新圖形輸入方式暴露：</b> 這會建立一個新的圖形輸入，並自動用該圖形輸入設定函數。 在這個專門頁面](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)了解更多關於暴露參數[的資訊。
* <b>空函式：</b> 從零開始編寫一個函式。
* <b>Constant value：</b>從設定為參數當前值的常數值節點](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md)開始編輯函式[。
* <b>重置：</b> 將參數重置為預設值與範圍。 若對參數套用函數，則該函數會被忽略。

>[!NOTE]
>
> 複製/貼上與預設檔案動作是全域的，因此無法針對單一參數使用。

### 節點上下文選單

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

上述全域&#x200B;*選單中的一些參數動作*&#x200B;可在節點上下文選單中取得。點選節點上的 RMB，然後到「管理參數」即可存取。

請注意，複製/貼上操作在此選單中不可使用。 你可以在上述節點屬性中找到它們。

以下對原子節點的限制同樣適用於此選單。

</td>
<td width="50.00%" style="border: 0;" valign="top">

![節點上下文選單中的「管理參數」選單「節點上下文選單](manage-parameters.resources/manage-parameters-node-menu.png "中的管理參數」選單"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 複製並貼上參數

可以複製來源節點的所有參數值，並貼上到目標節點上。 來源節點與目標節點的參數會根據 <b>其識別碼與類型</b>進行匹配。

例如，一個標識為「scale」且類型為「Float」的參數，若其識別碼同樣為「scale」且類型為「Float」，則可複製貼上到另一個參數「Shape Scale」。

此功能的運作方式與使用 [參數預設檔案](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)相同。 事實上，複製到剪貼簿的資料與 SBSPRS 預設檔案中的資料相同，且可貼上至任何文字編輯器中進行檢視與編輯。

</td>
<td style="border: 0;" valign="top">

![複製並貼上參數](manage-parameters.resources/copy-paste-parameters.gif "複製並貼上參數"){zoomable="yes"}

</td>
</tr>
</table>

## 原子節點的限制

部分原子節點因實作與控制方式不同而無法提供[](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)。

這些行為......

* [複製/貼上參數](#copy-paste-parameters)
* [儲存/套用預設檔案](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)

...這些原子節點無法使用：

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[位圖](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)

[曲線](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)

[距離](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md)

[效果圖](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)

[漸變（動態）](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-dynamic/gradient-dynamic.md)

</td>
<td style="border: 0;" valign="top">

[梯度圖](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md)

[輸入顏色](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)

[輸入灰階](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)

[輸入值](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)

[輸出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)

</td>
<td style="border: 0;" valign="top">

[像素處理器](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)

[SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)

[文字](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)

[制服顏色](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md)

[價值處理器](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
