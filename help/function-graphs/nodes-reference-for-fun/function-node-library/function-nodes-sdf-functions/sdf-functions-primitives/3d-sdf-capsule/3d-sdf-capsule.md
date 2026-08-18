---
title: 膠囊
description: Designer > Substance 合成圖 > Nodes >參考 Node 函式庫 > SDF 函式 > Primitive > Capsule
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---


# 膠囊

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![膠囊圖示](./3d-sdf-capsule.png "膠囊")

<b>收錄於：</b> SDF 函數>原始

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個可調整長度與半徑膠囊的SDF函數。<br>膠囊是兩個球體橋接而成的。

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
| <b>開始</b> *Float3* | 起始球體的位置。<br><br><i>預設值：（0， 0， 0）</i> |
| <b>結束</b> *Float3* | 端點球體的位置。<br><br><i>預設值：（0， 0， 1）</i> |
| <b>半徑</b> *浮標* | 起始球體與終點球體的半徑。<br><br><i>預設值：0.25</i> |
| <b>起點/結束點</b> *布林值* | 控制起始與結束位置是否<b>應位於球體的兩端。<br>也就是控制膠囊高度是否應包含球體的半徑。<br><br><i>預設值：錯誤</b> <b></b></i> |
| <b>中間位置</b> *Float3* | 膠囊樞軸的世界空間位置。<br><br><i>預設值：（0， 0， 0）</i> |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
