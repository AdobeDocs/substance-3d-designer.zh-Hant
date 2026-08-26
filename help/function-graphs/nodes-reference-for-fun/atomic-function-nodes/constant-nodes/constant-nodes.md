---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/constant-nodes.html"
breadcrumb-title: ''
description: 存取 Substance 3D Designer 函式圖中的常數節點，以定義常數值與參數。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Constant
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 恆定
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 0%

---


# 恆定

常數節點是一種建立靜態值，用於 Substance 函數圖的方法。 與變[&#128279;](../../../../function-graphs/variables/variables.md)數不同，它們無法外部修改。

此外，本頁還提供每種資料類型及常見使用案例的額外資訊。

## 整數

常數整數產生整數，步長為 1。

[它們可以轉換成浮點運算，](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) 建議在執行比加法、減法和簡單比較更複雜的操作時這麼做。

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![整數類型圖示 整數型別圖示](../../../../assets/fn-constant-integer.png "")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>整數</b>

整數只有一個分量。 它作為選擇的索引非常有用，例如：

* 選擇以下拉選單形式呈現給使用者的選項（見本頁[&#128279;](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)的「下拉清單」）。
* 選擇多交換[&#128279;](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md)節點的輸入。<b></b>

>[!IMPORTANT]
>
> <b>參數函數&#x200B;*中不支援*&#x200B;負整數</b>。請參閱 [此頁](../../../../technical-issues/parameters-not-working/parameters-not-working-as-expected.md) 的「技術問題」區塊，尋找解決方法。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Integer2 type icon](../../../../assets/fn-constant-integer2.png "Integer2 type icon")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>整數2</b>

Integer2 節點會產生一個靜態的 2 分量整數向量，分量為 （X， Y）。

Integer2 並不常見，但例如用於在圖塊產生器[&#128279;](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)中設定 X 和 Y 的二維平鋪。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Integer3 類型圖示](../../../../assets/fn-constant-integer3.png "Integer3 類型圖示")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>整數3</b>

Integer3 節點會產生一個靜態的三成分整數向量，其分量為 （X， Y， Z）。

整數 3 並不常見，也不太可能遇到。<b>\
</b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Integer4 類型圖示](../../../../assets/fn-constant-integer4.png "Integer4 類型圖示")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>整數4</b>

一個 Integer4 節點會產生一個靜態的四分量整數向量，分量為 （X， Y， Z， W）。

整數 4 並不常見，也不太可能遇到。<b>\
</b>

</td>
</tr>
</table>

## 花車

常數浮點數產生的是小數，而非整數，這表示它們的值總是在小於十進位符號後，且可以以小於1的步數（預設為0.01）來減或增。

[浮點數可以轉換成整數](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) ，但會被向上或向下取整到最近的整數，導致資料和準確度損失。

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![浮點類型圖示](../../../../assets/fn-constant-float.png "浮點類型圖示")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>浮標</b>

浮點數只有一個成分，為了簡潔起見，名稱中省略了（1）。 浮點非常常見，用於任何需要精確控制的數值，例如滑桿或角度。 你幾乎可以在每個節點的參數中找到它。 它也是灰階值的首選資料類型！<b></b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Float2 類型圖示](../../../../assets/fn-constant-float2.png "Float2 類型圖示")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float2</b>

Float2 節點會產生靜態的雙成分 Float 向量。 分量命名為 X、Y。Float2 相當常見，用於 [取樣](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md)座標及轉換 [偏移量](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/transforms.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Float3 類型圖示](../../../../assets/fn-constant-float3.png "Float3 類型圖示")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float3</b>

Float3 節點會產生一個靜態的三成分浮點向量。 元件名稱為 X、Y、Z。FLOAT3 較少見，主要用於表示 [3D 比例座標](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md)，以及作為一種更簡單的無 Alpha 資料色彩儲存方式。<b>\
</b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Float4 類型圖示](../../../../assets/fn-constant-float4.png "Float4 類型圖示")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float4</b>

Float4 會產生靜態的四分量浮點向量。元件名稱為 X、Y、Z、W。Float4 非常常見，因為它是儲存與設定 [色彩資訊的首選方式，其中 XYZW 資料代表 RGBA 值。](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md)<b>\
</b>

</td>
</tr>
</table>

## 其他

Substance 函式圖中還有兩種額外的資料型態：布林值與字串。 字串與 Text[&#128279;](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) 節點一同在 Designer 6 版本中引入。

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![布林型別圖示](../../../../assets/fn-constant-boolean.png "")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>布林值</b>

布林值是最簡單的資料型態，只知道兩個狀態：真或假、1 或 0。 它以白色表示。 在不施放[&#128279;](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md)或使用邏輯節點的情況下，無法在布[林與整數之間交換。](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) 布林運算相當常見，是控制函數或圖流的絕佳方式，典型的用途是切換 [節點。](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md)<b></b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![字串類型圖示](../../../../assets/fn-constant-string.png "字串類型圖示")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>弦</b>

字串節點會產生靜態字串，也就是一段文字。 它是函數中最特殊的資料類型，通常無法與其他函數節點一起使用。 它的主要目標是作為文本節點的最終輸出 [。](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)

</td>
</tr>
</table>
