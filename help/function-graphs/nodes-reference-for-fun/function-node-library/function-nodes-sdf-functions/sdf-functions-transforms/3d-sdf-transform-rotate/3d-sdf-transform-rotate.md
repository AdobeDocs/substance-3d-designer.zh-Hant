---
title: 旋轉
description: Designer > Substance 合成圖 > Node 參考 Node 圖庫>> SDF 函式 > Transform > Rotate
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---


# 旋轉

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![旋轉圖示](./3d-sdf-transform-rotate.png "旋轉")

<b>收錄於：</b> SDF 函數> 變換

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

從可調整的樞軸點開始，繞著一個或多個軸旋轉一個 SDF 形狀。<br>使用 <b>3D 檢視</b>器的 Transform pivot</b> 輔助<b>工具來視覺化已完成的旋轉。

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
| <b>角度</b> *浮標* | 旋轉SDF形狀的角度依序為準。<br><br>角度會在 3D 檢視</b>器的 Transform 樞軸</b>輔助器<b>中以圓<b>圈顯示。將相機對準，使軸<b></b>向箭頭成為圓心，清楚看到旋轉角度，以轉彎的分數為單位。<br><br><i>預設值：0</i> |
| <b>軸心國</b> *Float3* | 定義 SDF 形狀旋轉軸的正規化向量。<br>例如： （0， 1， 0） 會使其 SDF 形狀繞其局部樞軸的 Y 軸旋轉。<br><br>軸線由 3D Viewer</b> 的 Transform 樞軸</b>輔助工具<b>中的箭頭<b>顯示。箭頭的顏色映射在這個向量的 XYZ 分量上。<br><br><i>預設值：（0， 1， 0）</i> |
| <b>樞軸位置</b> *Float3* | SDF 形狀局部樞軸的世界空間位置，其中 （0， 0， 0） 將樞軸置於 SDF 形狀的中心。 定義旋轉的起點。<br><br>樞軸在 3D 檢視</b>器的 Transform 樞軸</b>輔助工具<b>中，透過箭頭<b>起始點來視覺化。 |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
