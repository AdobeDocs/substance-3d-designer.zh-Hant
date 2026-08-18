---
title: 有帽錐體
description: Designer > Substance 合成圖 > Nodes >參考 Node 函式庫 > SDF 函式 > Primitive > Capped 錐體
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# 有帽錐體

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![有帽錐圖示 有帽錐體](./3d-sdf-capped-cone.png "")

<b>收錄於：</b> SDF 函數>原始

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個針對可調整底半徑與頂部半徑的封頂錐形的SDF函數。

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
| <b>半徑底線</b> *浮標* | 蓋錐底半徑。<br><br><i>預設值：0.5</i> |
| <b>半徑頂部</b> *浮標* | 蓋錐頂頂部的半徑。<br><br><i>預設值：0.2</i> |
| <b>高度</b> *浮標* | 蓋錐從底部起的 Z 上高度。<br><br><i>預設值：1</i> |
| <b>中間位置</b> *Float3* | 頂錐體樞軸的世界空間位置。<br><br><i>預設值：（0， 0， 0）</i> |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
