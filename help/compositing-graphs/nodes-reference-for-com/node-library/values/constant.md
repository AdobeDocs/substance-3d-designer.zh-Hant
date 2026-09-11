---
helpx_url: ""
breadcrumb-title: ''
description: 在 Substance 3D Designer 中存取常數節點，以定義 Substance 圖中的常數值。
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 恆定
user-guide-description: ''
user-guide-title: ''
source-git-commit: b63bc7a45aa6eadef1b72eb05d4a6aded05866a8
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---


# 恆定

常數節點是一種在 Substance 圖中建立靜態值的方法。

你可以在 **函式庫的值>常數** 區找到這些節點。\
它們都包含一個簡單的 [Value 處理器](../../atomic-nodes/value-processor/value-processor.md) 節點來產生該值。

+++ 函式庫中的常數節點

![constants-library.png](constant.resources/constants-library.png)

+++

<p style="text-align: center;"><img src="./constant.resources/constants-float-01.png" alt="常數浮點節點" /></p>

## 整數

常數整數產生整數，步長為 1。

[它們可以轉換成浮點運算，](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) 建議在執行比加法、減法和簡單比較更複雜的操作時這麼做。

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![整數類型圖示 整數型別圖示](constant.resources/fn-constant-integer.png "")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>整數</b>

整數只有一個分量。 它作為選擇的索引非常有用，例如：

* 選擇以下拉選單形式呈現給使用者的選項（見本頁](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)的「下拉清單」）[。
* 選擇多交換](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md)節點的[輸入。<b></b>

>[!IMPORTANT]
>
> <b>參數函數&#x200B;*中不支援*&#x200B;負整數</b>。請參閱 [此頁](../../../../technical-issues/parameters-not-working/parameters-not-working-as-expected.md) 的「技術問題」區塊，尋找解決方法。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Integer2 type icon](constant.resources/fn-constant-integer2.png "Integer2 type icon")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>整數2</b>

Integer2 節點會產生一個靜態的 2 分量整數向量，分量為 （X， Y）。

Integer2 的一個常見使用情境是設定 X 和 Y 格子大小，就像 Tile 產生](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)器節點一樣[。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Integer3 類型圖示](constant.resources/fn-constant-integer3.png "Integer3 類型圖示")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>整數3</b>

Integer3 節點會產生一個靜態的三成分整數向量，其分量為 （X， Y， Z）。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Integer4 類型圖示](constant.resources/fn-constant-integer4.png "Integer4 類型圖示")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>整數4</b>

一個 Integer4 節點會產生一個靜態的四分量整數向量，分量為 （X， Y， Z， W）。

</td>
</tr>
</table>

## 花車

常數浮點數會產生小數，也就是說，它們支援小於小數點後的數值，且可以小於1的步驟進行調整。 （預設值：0.01）

[浮點數可以轉換成整數](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) ，但會被向上或向下取整到最近的整數，導致資料和準確度損失。

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![浮點類型圖示](constant.resources/fn-constant-float.png "浮點類型圖示")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>浮標</b>

浮點數只有一個分量，且非常常用來表示任何需要精確度的單一數值。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Float2 類型圖示](constant.resources/fn-constant-float2.png "Float2 類型圖示")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float2</b>

Float2 節點會產生一個具有 （X， Y） 分量的兩分量向量。

Float2 常用於 [取樣座標](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md)、 [偏移轉換](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/transforms.md) 及一般二維向量操作。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Float3 類型圖示](constant.resources/fn-constant-float3.png "Float3 類型圖示")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float3</b>

Float3 節點會產生一個三成分（X、Y、Z）向量。

Float3 主要用於處理 3D 物件及 [3D 縮放座標](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md)[，例如 3D SDF 節點](../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions)，以及作為儲存 RGB 顏色的更簡單方式——即不使用 Alpha。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Float4 類型圖示](constant.resources/fn-constant-float4.png "Float4 類型圖示")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float4</b>

Float4 產生一個四分量（X、Y、Z、W）向量。

Float4 是儲存和設定顏色資訊的首選方式，當 XYZW 值映射到 RGBA 時，例如 [Uniform color 節點](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md)中。

</td>
</tr>
</table>

## 非數值

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![布林型別圖示](constant.resources/fn-constant-boolean.png "")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>布林值</b>

布林值是最簡單的資料型態，只知道兩個狀態： <code>真</code> 或 <code>是假的</code>.

這種類型在處理切換參數和 [If/Else](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md) 條件時相當常見。<br>布林值是一種簡單且高效的方法，可以控制函數或圖的流動，例如使用 [開關節點](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md)。

</td>
</tr>
</table>
