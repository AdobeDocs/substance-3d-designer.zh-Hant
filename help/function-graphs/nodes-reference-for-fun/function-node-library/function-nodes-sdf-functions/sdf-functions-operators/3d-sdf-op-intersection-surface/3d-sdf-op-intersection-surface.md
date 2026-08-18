---
title: 交集曲面
description: Designer > Substance 合成圖 >節點參考 Node library 中 >> SDF 函式 > 交集>運算子
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---


# 交集曲面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![交叉面圖示](./3d-sdf-op-intersection-surface.png "交叉面")

<b>收錄於：</b> SDF 函數>運算元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

回傳基底SDF形狀中與另一個SDF形狀相交部分的曲面，且厚度可調整。

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
| <b>基地自衛隊</b> *浮標* | 這是所依據的SDF形狀。 |
| <b>交會的SDF</b> *浮標* | SDF 形狀與基底 SDF 形狀相交。 |
| <b>厚度</b> *浮標* | 結果表面的厚度。<br><br><i>預設值：0.02</i> |
