---
title: 拉長型
description: Designer > Substance 合成圖 > Node 參考 Node 函式庫 >> SDF 函式 > Transform > Elongate
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---


# 拉長型

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![延伸圖示](./3d-sdf-transform-elongate.png "延伸")

<b>收錄於：</b> SDF 函數> 變換

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

從可調整位置拉長SDF形狀。<br>有效線性地擴展從可調整切片開始的 SDF 形狀體積。

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
| <b>伸長</b> *Float3* | X、Y、Z軸上的伸長長度。 |
| <b>中間位置</b> *Float3* | 圖形將被拉長的世界空間位置。<br>也就是被拉長的切片位置。 |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
