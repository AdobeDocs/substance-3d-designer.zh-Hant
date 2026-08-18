---
title: 縮放
description: Designer > Substance 合成圖 > Nodes 參考 Node 函式庫>> SDF 函式 > Transform > Scale
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 2%

---


# 縮放

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![比例圖示](./3d-sdf-transform-scale.png "比例")

<b>收錄於：</b> SDF 函數> 變換

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

均勻縮放一個 SDF 形狀。

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
| <b>SDF</b> *浮標* | 輸入的 SDF 形狀。 |
| <b>規模</b> *浮標* | 均勻比例因子。<br><br><i>預設值：1</i> |
| <b>樞軸位置</b> *Float3* | SDF 形狀局部樞軸的世界空間位置，其中 （0， 0， 0） 將樞軸置於 SDF 形狀的中心。 <br>定義縮放的起點。<br><br><i>預設值：（0， 0， 0）</i> |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
