---
title: 螺旋（約）
description: Designer > Substance 合成圖 > Nodes 參考 Node 函式庫 > Node 函式庫 > SDF 函數 > Primitive > Helix（約）
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# 螺旋（約）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![螺旋（約） 圖示](./3d-sdf-helix.png "螺旋（約）")

<b>收錄於：</b> SDF 函數>原始

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

SDF 函數用於螺旋的近似，螺旋是沿著繞軸向上曲線繞行的曲線掃動圓圈所形成的形狀。<br><br><i>注意：</i>由於此 SDF 函數為近似值，渲染時可能會出現瑕疵。

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
| <b>主要半徑</b> *浮標* | 繞曲線與軸線的距離。<br><br><i>預設值：0.4</i> |
| <b>次半徑</b> *浮標* | 圓沿曲線掃動形成螺旋表面的半徑。<br><br><i>預設值：0.1</i> |
| <b>高度</b> *浮標* | 螺旋的Z-up高度。<br><br><i>預設值：0.5</i> |
| <b>繞組</b> *浮標* | 曲線繞軸繞行的次數以 0.5 步為單位。<br>也就是說，螺旋會在 0.5 高度內旋轉多少圈。<br><br><i>預設值：4</i> |
| <b>中間位置</b> *Float3* | 螺旋軸心的世界空間位置。<br><br><i>預設值：（0， 0， 0）</i> |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
