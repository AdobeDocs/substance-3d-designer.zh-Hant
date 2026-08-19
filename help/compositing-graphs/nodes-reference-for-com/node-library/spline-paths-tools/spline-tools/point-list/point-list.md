---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/point-list.html"
breadcrumb-title: ''
description: 使用點列表節點來建立和管理點清單，用於樣條線和路徑生成。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Point List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 點數列表
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# 點數列表

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/point-list-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

產生一份樣條曲線要遍歷的點清單。

如果提供現有的點清單給 <b>點</b> 輸入，產生的清單會附加到輸入清單中。

</td>
</tr>
</table>

>[!TIP]
>
> 此節點可用來向樣條（多元二次）[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md)節點提供點，以建立樣條曲線。

>[!IMPORTANT]
>
> <b>點表<b></b>與點數</b>連接器&#x200B;*與花鍵</b>座標、<b>花鍵資料</b>及<b>花鍵數量</b>連接器不相容*<b>，因為它們依賴不同的資料。

## 輸入連接器

<b>預覽&#x200B;</b>*灰階*&#x200B;將點預覽為灰階影像。

<b>點列表輸入</b> *顏色*\
彩色影像RGBA通道中編碼的輸入點列表：\
    <b>R</b> - X 位置\
    <b>G</b> - Y 位置\
    <b>B</b> - 身高\
    <b>A</b> - 打包資料：\
* 整數部分：平滑度;\
* 分數部分：厚度。

<b>點數輸入</b> *整數*\
輸入點的數量。

## 輸出連接器

<b>預覽&#x200B;</b>*灰階*&#x200B;將點預覽為灰階影像。

<b>點表 </b>*顏色*\
彩色影像RGBA通道中編碼的點的輸出清單：\
    <b>R</b> - X 位置\
    <b>G</b> - Y 位置\
    <b>B</b> - 身高\
    <b>A</b> - 打包資料：\
* 整數部分：平滑度;\
* 分數部分：厚度。

<b>點數整 </b>*數*\
輸出的點數。

## 參數

<b>點數</b> *整數*&#x200B;產生的點數。

<b>全域平滑度調整</b> *浮點*&#x200B;對所有點的平滑值施加均勻偏移。\
所得的平滑度值會被夾在[0;1] 範圍內。

+++點的性質
<b>p# 性質</b> *Float3*&#x200B;設定 p# 點的屬性。\
*- 高度：* 調整點的高度，當較低值代表較低或較深的位置時;\
*- 平滑性：* 偏移樣條平滑起點的 p#，值為 0 時產生硬軌跡，1 則為完全平滑軌跡;\
*- 厚度：* 調整 p# 處樣鍵的厚度。 厚度則由特定的樣條節點使用。

+++

+++點座標
<b>p#</b> *Float2*&#x200B;設定 p# 點在貼圖空間中的位置。

+++

+++預覽
<b>節目標籤：</b> *布林值*\
對於每個點，會在「預覽」輸出中旁邊顯示該點的名稱。

<b>標籤尺寸</b> *浮點*（當「顯示標籤」設為「真實」時可用）\
貼圖空間中每個點的標籤大小，0.1 是貼圖寬度的十分之一。

<b>顯示點布</b> *林值*\
顯示「預覽」輸出中的點數。

<b>點數大小</b> *浮點*&#x200B;數（當「顯示點數」設定為「真實」時可用）\
貼圖空間中點的半徑，0.1 是貼圖寬度的十分之一。

+++

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![節點範例 1](../../../../../../assets/PointList-Variant1.jpg "節點範例 1")

</td>
<td style="border: 0;" valign="top">

![節點範例 2](../../../../../../assets/PointList-Demo1.gif "節點範例 2")

</td>
</tr>
</table>
