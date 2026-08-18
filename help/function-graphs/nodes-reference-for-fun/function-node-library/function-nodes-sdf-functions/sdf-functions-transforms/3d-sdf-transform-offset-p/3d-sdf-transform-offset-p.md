---
title: 偏移P
description: Designer > Substance 合成圖 > Node 參考 Node 函式庫 >> SDF 函式 > Transform > Offset P
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---


# 偏移P

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![偏移 P 圖示](./3d-sdf-transform-offset-p.png "偏移 P")

<b>收錄於：</b> SDF 函數> 變換

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

會沿著向量偏移世界空間。<br>輸出的轉換世界位置可與 <b>大多數 SDF 函數的 P</b> 輸入連結，以定義其於轉換後的世界空間中。<br><br><i>提示：</i> P 轉換可串連，但結果取決於操作順序。

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
| <b>偏移</b> *Float3* | 世界空間的距離會偏移在 X、Y 和 Z 方向。 |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
