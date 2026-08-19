---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-cubic.html"
breadcrumb-title: ''
description: 使用 Spline Cubic 節點來建立帶有四個控制點的平滑立方體樣條，用於曲線路徑。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Cubic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 樣條（立方曲線）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---


# 樣條（立方曲線）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/spline-cubic-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

在任意位置的兩點 <b>p1 </b>與 <b>p2</b> 之間產生單一樣條曲線。

樣條的軌跡由 p1</b> 的<b>「出」切線和 p2</b> 的<b>「入」切線控制。

</td>
</tr>
</table>

## 輸入連接器

<b>預覽</b> *灰階*&#x200B;輸入樣條的預覽為灰階影像。

<b>樣條座標</b> *色彩*&#x200B;輸入樣條點的座標編碼在彩色影像的 RGBA 通道中：\
<b>R</b> - X 位置\
<b>G</b> - Y 位置\
<b>B</b> - 身高\
    <b>A</b> - 打包資料：\
* 符號：樣條鍵為閉（負）或開（正）;\
* 絕對值：厚度 + 1。

<b>樣條資料</b> *色彩*&#x200B;輸入樣條的額外資料編碼於彩色影像的 RGBA 通道中。\
<b>R</b> - 切線 X\
<b>G</b> - 切線 Y\
<b>B</b> - 未上場\
<b>A</b> - 未上場

<b>樣條量</b> *整數*：輸入樣條的數量。

## 輸出連接器

<b>預覽</b> *灰階*&#x200B;輸出樣條的預覽作為灰階影像。

<b>樣條座標</b> *顏色*&#x200B;指編碼在彩色影像RGBA通道中的輸出樣條點座標。\
    <b>R</b> - X 位置\
    <b>G</b> - Y 位置\
    <b>B</b> - 身高\
    <b>A</b> - 打包資料：\
* 符號：樣條鍵為閉（負）或開（正）;\
* 絕對值：厚度 + 1。

<b>樣條資料</b> *色彩*&#x200B;輸出樣條的額外資料編碼於彩色影像的RGBA通道中。\
    <b>R</b> - 切線 X\
    <b>G</b> - 切線 Y\
    <b>B</b> - 未上場\
    <b>A</b> - 未上場

<b>樣條量</b> *整數*：輸出樣條的數量。

## 參數

<b>翻轉方向</b> *布林值*\
會反轉花鍵的方向。

<b>附加輸入樣條</b> *布林值*\
將產生的樣條曲線加入連接樣條</b>輸入的樣條<b>線清單末尾。

<b>非正方修正&#x200B;</b>*布林*：調整點的位置與厚度，以在非正方形解析度下保留樣條形狀。\
這也影響均勻分布。

+++高度
<b>起始高度</b> *浮點*&#x200B;調整 p1 點的高度，值越低表示位置越低或越深。\
這會影響花鍵在 p1 處的高度。

<b>端高度</b> *浮點*&#x200B;調整 p2 點的高度，值越低表示位置越低或越深。\
這會影響 p2 點樣鍵的厚度。

<b>自動切線高度</b> *布林*&#x200B;自動設定樣條切線的高度，從起始高度線性插值到結束高度。

<b>p1 切線高度</b> *浮點* （當「自動切線高度」為真時可用）\
調整 p1 點「出」切線的高度，較低代表位置較低或更深。\
這會影響樣鍵沿線的高度，當它從 p1 拉遠時。

<b>p2 切線高度</b> *浮點* （當「自動切線高度」為真時可用）\
調整 p2 點「內」切線的高度，當值越低代表位置越低或越深。\
這會影響樣鍵沿線的高度，當它從 p2 拉開時。

+++

+++厚度
<b>起始厚度</b> *浮子*&#x200B;調整 p1 尖端的厚度。\
這會影響 p1 點的花鍵厚度。\
注意：厚度是針對特定樣條節點使用的。

<b>端部厚度</b> *浮動*&#x200B;調整 p2 尖端的厚度。\
這會影響 p2 點樣鍵的厚度。\
注意：厚度是針對特定樣條節點使用的。

<b>自動切線厚度</b> *布林*&#x200B;值 自動設定樣條切線的厚度，從起始厚度線性插值到終值厚度。\
注意：厚度是針對特定樣條節點使用的。

<b>p1 切線厚度</b> *浮點* （當「自動切線厚度」為真時可用）\
調整 p1 點「出」切線的厚度。\
這會影響樣鍵沿線的厚度，因為它從 p1 拉遠。\
注意：厚度是針對特定樣條節點使用的。

<b>p2 切線厚度</b> *浮點* （當「自動切線厚度」為真時可用）\
調整 p2 點「內」切線的厚度。\
這會影響樣鍵沿線的厚度，當它從 p2 拉開時。\
注意：厚度是針對特定樣條節點使用的。

+++

+++點座標
<b>第1頁</b> *Float2*&#x200B;設定 p1 點在貼圖空間中的位置。

<b>p1 切線</b> *Float2*&#x200B;設定 p1 點「out」切線柄在貼圖空間中的位置。

<b>第二頁</b> *Float2*&#x200B;設定 p2 點在貼圖空間中的位置。

<b>p2 切線</b> *Float2*&#x200B;設定 p2 點「內」切線柄在貼圖空間中的位置。

+++

+++預覽
<b>節目旁線</b> *布林值*&#x200B;在預覽輸出中顯示 p1 點「出」切線和 p2 點「入」切線。

<b>節目指導助理</b> *布林值*&#x200B;在預覽輸出中會在樣條曲線的起始處顯示一個點，在末端顯示一個箭頭。

<b>分段數量</b> *整數*&#x200B;調整預覽輸出中繪製樣條曲線視覺化所使用的段數。\
數值越高，線條越平滑。

<b>厚度（px）</b> *浮點*&#x200B;調整預覽輸出中樣條線視覺化的像素厚度。

+++

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![節點範例 1](../../../../../../assets/SplineCubic-Variant1.jpg "節點範例 1")

</td>
<td style="border: 0;" valign="top">

![節點範例 2](../../../../../../assets/SplineCubic-Variant2.jpg "節點範例 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![節點範例 3](../../../../../../assets/SplineCubic-Demo.gif "節點範例 3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
