---
title: 翻轉
description: Designer > Substance 合成圖 > Nodes 參考 Node 圖庫 > SDF 函式 > Transform > Flip 的 Node 函式 > SDF 函式
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# 翻轉

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![翻轉圖示](./3d-sdf-transform-flip.png "翻轉")

<b>收錄於：</b> SDF 函數> 變換

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

對輸入的 SDF 形狀套用鏡像轉換。<br>基本上是在選取的軸上執行負刻度。

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
| <b>鏡像軸</b> *整數3* | 使用整數三元來設定所需的鏡像軸。<br>例如： （1， 0， 0） 會鏡像 X 軸。<br><br><i>預設值：（1， 0， 0）</i> |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
