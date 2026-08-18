---
title: 對稱性
description: Designer > Substance 合成圖 > Nodes 參考 Substance 合成圖 > Node 庫 > SDF 函數 > Operator > Symmetry
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---


# 對稱性

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![對稱圖示](./3d-sdf-op-symmetry.png "對稱")

<b>收錄於：</b> SDF 函數>運算元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

將 SDF 形狀翻轉並複製到鏡面平面，然後回傳基底 SDF 形狀與其複製件的聯集。<br>對稱性可同時套用於任意軸上。

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
| <b>鏡面位置</b> *Float3* | 鏡面平面中心的世界空間位置。<br>若將對稱性應用於多個軸上，所有鏡面皆共享此位置。<br><br><i>預設：（0， 0， 0）</i> |
| <b>鏡像軸</b> *整數3* | 設定所需的鏡像軸。<br><br>例如，（1， 0， 0） 會在 X 軸上施加對稱性。<br><br><i>預設值：（1， 0， 0）</i> |
| <b>翻轉軸</b> *整數3* | 設定哪些軸應該翻轉。<br><br>例如，（1， 0， 0） 會翻轉 X 軸上的對稱方向。<br><br><i>預設值：（0， 0， 0）</i> |
| <b>預偏移</b> *Float3* | 在對稱算符之前，先將 X、Y、Z 軸的偏移量施加在形狀上。 |
