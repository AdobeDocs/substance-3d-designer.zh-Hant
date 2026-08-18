---
title: 有頂環面
description: Designer > Substance 合成圖 > Nodes >參考 Node 函式庫 > SDF 函式 > Primitive > Capped torus
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# 有頂環面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![有頂環圖示](./3d-sdf-capped-torus.png "有頂環")

<b>收錄於：</b> SDF 函數>原始

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個有蓋環面的SDF函數，其中沿大圓掃掠的次圓可以以一定角度被封。<br>兩個圓圈都有可調整的半徑。

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
| <b>主要半徑</b> *浮標* | 大圓的半徑，小圓沿著此方向掃過，形成環面的表面。<br><br><i>預設值：0.5</i> |
| <b>次半徑</b> *浮標* | 小圓沿大圓掃過形成環面表面的半徑。<br><br><i>預設值：0.2</i> |
| <b>角度</b> *浮標* | 中心角以轉角計算，定義大圓的修剪弧線，小圓不會沿著此弧掃過。<br><br><i>預設值：0.75</i> |
| <b>角度偏移</b> *浮標* | 沿主半徑的修剪弧線偏移量，該弧線不會沿小圓掃過。<br><br><i>預設值：0</i> |
| <b>對稱</b> *布林值* | 控制修剪弧線應該畫向一方向還是兩個方向。<br><br><i>預設值：真</i> |
| <b>中間位置</b> *Float3* | 頂環面樞軸的世界空間位置。<br><br><i>預設值：（0， 0， 0.5）</i> |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
