---
title: 橢球體
description: Designer > Substance 合成圖 > Nodes 參考 Node 函式庫 > SDF 函式 > Primitive > Ellipsoid 的 Substance 合成>圖
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# 橢球體

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![橢球圖示](./3d-sdf-ellipsoid.png "橢球體")

<b>收錄於：</b> SDF 函數>原始

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個橢球體的SDF函數，橢球體是一個可調整三維半徑的圓弧形狀。

</td>
</tr>
</table>

<a name='inputs'></a>

>[!INFO]
> 
> 欲了解更多涉及 SDF 函數的概念與工作流程，請前往專門頁面： [使用 SDF 函數](../../working-with-sdf-functions.md)

## 輸入

|  |  |
| :--- | :--- |
| <b>半徑</b> *Float3* | X、Y、Z 中橢球半徑。<br><br><i>預設值：（0.35， 0.35， 0.5）</i> |
| <b>中間位置</b> *Float3* | 橢球體樞軸的世界空間位置。<br><br><i>預設值：（0， 0， 0）</i> |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
