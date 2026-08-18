---
title: 有帽錐2點
description: 設計者> Substance 合成圖 > Node 參考 Node 函式庫>> SDF 函式 > Primitive > Capped 錐體 2 點
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---


# 有帽錐2點

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![有蓋錐 2 點圖示](./3d-sdf-capped-cone-2-points.png "有蓋錐 2 點")

<b>收錄於：</b> SDF 函數>原始

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個由底面與頂端位置定義的有帽錐的 SDF 函數。<br>底座和頂部都有可調整的半徑。

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
| <b>位置基礎</b> *Float3* | 蓋錐底的位置。<br><br><i>預設值：（0， 0， 0）</i> |
| <b>排名頂端</b> *Float3* | 蓋錐頂的位置。<br><br><i>預設值：（0， 0， 1）</i> |
| <b>半徑底線</b> *浮標* | 蓋錐底半徑。<br><br><i>預設值：0.5</i> |
| <b>半徑頂部</b> *浮標* | 蓋錐頂頂部的半徑。<br><br><i>預設值：0.2</i> |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
