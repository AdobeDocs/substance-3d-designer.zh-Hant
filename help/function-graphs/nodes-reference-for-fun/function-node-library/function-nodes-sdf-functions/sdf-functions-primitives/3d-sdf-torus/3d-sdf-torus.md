---
title: 環面
description: Designer > Substance 合成圖 > Node 參考 Node 函式庫>> SDF 函式 >Primitive > Torus 的 Node 函式
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---


# 環面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![托魯斯圖示](./3d-sdf-torus.png "托魯斯")

<b>收錄於：</b> SDF 函數>原始

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個 SDF 函數用於環面，環面是由沿大圓掃過一個小圓所形成的形狀。<i>兩個圓圈都有可調整的半徑。

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
| <b>半徑大修</b> *浮標* | 小圓盤被掃過形成環面表面的圓半徑。<br><br><i>預設值：0.5</i> |
| <b>小半徑</b> *浮標* | 圓的半徑沿著主圓掃動，形成環面的表面。<br><br><i>預設值：0.2</i> |
| <b>中間位置</b> *Float3* | 環面樞軸的世界空間位置。<br><br><i>預設值：（0， 0， 0）</i> |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
