---
title: 無限接地平面
description: Designer > Substance 合成圖 >節點參考 Node 圖>庫> SDF 函式 > Primitive > Infinite ground plane 的 Substance 合成圖
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---


# 無限接地平面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![無限地面平面圖示](./3d-sdf-ground-plane.png "無限地面平面")

<b>收錄於：</b> SDF 函數>原始

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個用於無限地面平面且高度可調整的 SDF 函數。

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
| <b>高度</b> *浮標* | Z 軸高度。<br><br><i>預設：0</i> |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
