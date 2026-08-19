---
title: 2號圓柱點
description: Designer > Substance 合成圖 > Nodes >參考 Node 函式庫 > SDF 函式 > Primitive > Cylinder 2 點
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# 2號圓柱點

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![圓柱體2點圖示](./3d-sdf-cylinder-2-points.png "圓柱體2點")

<b>收錄於：</b> SDF 函數>原始

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個針對可調整半徑圓柱的SDF函數，該圓柱由起始與終點圓盤的位置定義。

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
| <b>開始</b> *Float3* | 圓柱起始盤的位置。<br><br><i>預設值：（0， 0， 0）</i> |
| <b>結束</b> *Float3* | 圓柱體末端盤的位置。<br><br><i>預設值：（0， 0， 1）</i> |
| <b>半徑</b> *浮標* | 圓柱半徑。<br><br><i>預設值：0.25</i> |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
