---
title: 金字塔
description: Designer > Substance 合成圖 > Node 參考 Node 函式庫 > SDF 函式 > Primitive > Pyramid 的 Substance 合成>圖
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---


# 金字塔

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![金字塔圖示](./3d-sdf-pyramid.png "金字塔")

<b>收錄於：</b> SDF 函數>原始

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

SDF 函數用於可調整高度、基底大小及基底位置的金字塔。

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
| <b>高度</b> *浮標* | 金字塔頂點從底部起的Z-up高度。<br><br><i>預設值：1</i> |
| <b>底座尺寸</b> *Float2* | 金字塔底面在 X 和 Y 的大小。<br><br><i>預設值：（1， 1）</i> |
| <b>基地位置</b> *Float3* | 金字塔底部的世界空間位置。<br><br><i>預設值：（0， 0， 0）</i> |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
