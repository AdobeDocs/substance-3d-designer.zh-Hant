---
title: 重複鏡片範圍
description: Designer > Substance 合成圖 > Nodes 參考 Node 函式庫 >> SDF 函式 > 運算子 > 重複鏡像範圍
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---


# 重複鏡片範圍

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![重複鏡面範圍圖示](./3d-sdf-op-repeat-mirror.png "重複鏡面範圍")

<b>收錄於：</b> SDF 函數>運算元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

在 X、Y 和 Z 正負軸上，可以任意次數以規則間距鏡像並複製 SDF 形狀。<br>每次這個運算子重複一個形狀時，也會同時鏡像該形狀。 這在視覺上會在形狀的原始方向與翻轉的複製品之間交替出現。

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
| <b>金額 +</b> *整數3* | 沿著正 X、Y、Z 軸的重複數量。<br><br><i>預設值：（2， 0， 0）</i> |
| <b>金額 -</b> *整數3* | 沿著負 X、Y、Z 軸的重複數量。<br><br><i>預設值：（2， 0， 0）</i> |
| <b>間距</b> *Float3* | 每個複製品之間的世界空間。<br><br>間距由立方體輔助器視覺化，大小為 X、Y 和 Z 方向重複件之間的空間。 間距從原點位置</b>開始<b>，並從原點位置對稱增加。<br><br><i>預設值：（2， 2， 2）</i> |
| <b>起源位置</b> *Float3* | 定義將被複製的SDF形狀中心。<br><br>原點位置由立方體輔助器的中心位置視覺化。<br><br><i>預設值：（0， 0， 0）</i> |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
