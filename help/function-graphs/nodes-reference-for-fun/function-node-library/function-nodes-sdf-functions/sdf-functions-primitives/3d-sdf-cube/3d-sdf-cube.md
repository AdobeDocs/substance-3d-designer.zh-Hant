---
title: 立方體
description: Designer > Substance 合成圖 > Nodes 參考 Node 函式庫> Node 函式庫 > SDF 函式 > Primitive > Cube
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---


# 立方體

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![立方體圖示](./3d-sdf-cube.png "立方體")

<b>收錄於：</b> SDF 函數>原始

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

立方體的 SDF 函數，具備可調整的 XYZ 大小及邊緣圓角。

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
| <b>規模</b> *Float3* | 立方體在 X、Y 和 Z 上的大小。<br><br><i>預設值：（1， 1， 1）</i> |
| <b>四捨五入</b> *浮標* | 施加於立方體邊緣的圓弧半徑。<br><br><i>注意：</i> 硬邊可能會出現在圓弧半徑交點處。<br><br><i>預設值：0</i> |
| <b>樞軸位置（地方）</b> *Float3* | 立方體局部樞軸的世界空間位置，其中 （0， 0， 0） 將樞軸置於立方體中心。<br><br><i>預設值：（0， 0， -0.5）</i> |
| <b>中間位置</b> *Float3* | 立方體樞軸的世界空間位置。<br><br><i>預設值：（0， 0， 0）</i> |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
