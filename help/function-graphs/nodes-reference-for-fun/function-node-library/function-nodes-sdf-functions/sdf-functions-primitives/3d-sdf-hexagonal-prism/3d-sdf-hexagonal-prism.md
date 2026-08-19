---
title: 六角柱
description: Designer > Substance 合成圖 > Nodes >參考 Node 圖庫 > SDF 函式 > Primitive > Hexagonal prim。
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# 六角柱

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![六角柱圖像](./3d-sdf-hexagonal-prism.png "六角柱")

<b>收錄於：</b> SDF 函數>原始

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

SDF函數用於可調整高度、半徑及邊緣圓角的六面棱鏡。

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
| <b>高度</b> *浮標* | 六角柱柱從底部起的 Z 上高度。<br><br><i>預設值：1</i> |
| <b>半徑</b> *浮標* | 六角柱的半徑。<br><br><i>預設值：0.5</i> |
| <b>四捨五入</b> *浮標* | 施加於六角柱邊的圓弧半徑。<br><br><i>注意：</i> 在圓角半徑交點處可能會出現硬邊。<br><br><i>預設值：0</i> |
| <b>中間位置</b> *Float3* | 六角柱樞軸的世界空間位置。<br><br><i>預設值：（0， 0， 0）</i> |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
