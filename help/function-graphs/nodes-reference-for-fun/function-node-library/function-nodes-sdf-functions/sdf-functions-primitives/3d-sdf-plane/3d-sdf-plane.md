---
title: 平面
description: Designer > Substance 合成圖 > Nodes 參考，用於 Node 函式庫> SDF 函式 > Primitive > Plane 的 Substance 合成>圖
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 1%

---


# 平面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![平面圖示](./3d-sdf-plane.png "平面")

<b>收錄於：</b> SDF 函數>原始

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個可調整方向、位置與大小平面的 SDF 函數。

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
| <b>正常</b> *Float3* | 平面的世界空間法線向量，控制其方向。<br>向量已正規化。<br><br><i>預設值：（0， 0， 1）</i> |
| <b>規模</b> *Float2* | 平面尺寸在 X 和 Y 中。<br><br><i>預設值：（1， 1）</i> |
| <b>厚度</b> *浮標* | 平面厚度，向所有方向施加。<br>當厚度增加時，平面會被圓角化。<br><br><i>預設值：0</i> |
| <b>中間位置</b> *Float3* | 平面樞軸的世界空間位置。<br><br><i>預設值：（0， 0， 0）</i> |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
