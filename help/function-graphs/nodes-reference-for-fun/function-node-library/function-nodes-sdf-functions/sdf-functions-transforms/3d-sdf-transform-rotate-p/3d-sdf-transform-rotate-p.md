---
title: 旋轉P
description: Designer > Substance 合成圖 >節點參考 Node 函式庫 >> SDF 函式 > Transform > Rotate P
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# 旋轉P

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![旋轉P圖示 旋轉P。](./3d-sdf-transform-rotate-p.png "")

<b>收錄於：</b> SDF 函數> 變換

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

繞軸旋轉世界空間，並以可調整角度旋轉。<br>輸出的轉換後世界位置可與 <b>大多數 SDF 函數的 P</b> 輸入連接，以定義它們在這個轉換後的世界空間中。<br><br>使用 <b>3D 檢視</b>器的 Transform pivot</b> 輔助工具<b>來視覺化所執行的旋轉。<br><br><i>提示：</i>P 變換可以串連，但請記得結果取決於操作順序。

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
| <b>角度</b> *浮標* | 世界空間旋轉的角度，輪流轉向。<br><br>角度會在 3D 檢視</b>器的 Transform 樞軸</b>輔助器<b>中以圓<b>圈顯示。將相機對齊，讓軸<b></b>向箭頭成為圓心，這樣才能清楚看到旋轉角度，視角為轉彎的一小部分。 |
| <b>軸心國</b> *Float3* | 定義世界空間旋轉軸的正規化向量。<br>例如： （0， 1， 0） 會使世界空間繞樞軸的 Y 軸旋轉。<br><br>軸線由 3D Viewer</b> 的 Transform 樞軸</b>輔助工具<b>中的箭頭<b>顯示。箭頭的顏色映射在這個向量的 XYZ 分量上。<br><br><i>預設值：（0， 1， 0）</i> |
| <b>樞軸位置</b> *Float3* | 定義旋轉原點的樞軸世界空間位置。<br><br>樞軸點可透過 3D Viewer</b> 的 Transform 樞軸</b>輔助<b>工具中箭頭<b>起始點來視覺化。 |
| <b>P</b> *Float3* | 轉型後的世界空間位置。 利用此輸入，透過 <b>Offset P</b> 和 <b>Rotate P</b> 節點套用額外的變換。<br><br><i>預設：未變換的世界空間位置。</i> |
