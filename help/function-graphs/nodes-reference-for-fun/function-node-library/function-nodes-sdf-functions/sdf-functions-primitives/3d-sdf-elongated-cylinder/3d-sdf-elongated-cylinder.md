---
title: 細長圓柱體
description: Designer > Substance 合成圖 >節點參考 Node library > Node library > SDF 函式 > 原始>延長圓柱
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---


# 細長圓柱體

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![細長圓筒圖示](./3d-sdf-elongated-cylinder.png "長長圓筒")

<b>收錄於：</b> SDF 函數>原始

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

SDF函數用於可調整長度、半徑及邊緣圓潤度的細長圓柱體。<br>細長的圓柱是連接兩個圓柱體的結果。

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
| <b>高度</b> *浮標* | 起始與結束圓柱從底部起的Z-up高度。<br><br><i>預設值：0.5</i> |
| <b>半徑</b> *浮標* | 起始與結束圓柱的半徑。<br><br><i>預設值：0.5</i> |
| <b>四捨五入</b> *浮標* | 加在加長圓柱邊緣的圓弧半徑。<br><br><i>注意：</i> 在圓弧半徑交點處可能會出現硬邊。<br><br><i>預設值：0</i> |
| <b>中間位置</b> *Float3* | 延長圓柱軸的世界空間位置。<br><br><i>預設值：（0， 0， 0）</i> |
| <b>伸長距離</b> *浮標* | 起始圓柱體拉長的距離。<br>也就是起始圓柱與結束圓柱中心之間的距離。<br><br><i>預設值：0.5</i> |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
