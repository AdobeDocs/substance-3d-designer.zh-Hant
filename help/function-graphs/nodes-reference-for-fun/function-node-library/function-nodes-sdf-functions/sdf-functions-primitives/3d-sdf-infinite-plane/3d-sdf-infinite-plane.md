---
title: 無限平面
description: Designer > Substance 合成圖 > Nodes 參考，> Node 函式庫 > SDF 函式 > Primitive > Infinite 平面
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# 無限平面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![無限平面圖示](./3d-sdf-infinite-plane.png "無限平面")

<b>收錄於：</b> SDF 函數>原始

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個用於無限可調整方向與位置平面的SDF函數。

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
| <b>正常</b> *Float3* | 無限平面的世界空間法線向量，控制其方向。<br>向量已正規化。<br><br><i>預設值：（0， 0， 1）</i> |
| <b>中間位置</b> *浮標* | 平面樞軸在世界空間中的位置，作為平面法線上距離世界原點的距離。<br><br><i>預設值：0</i> |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
