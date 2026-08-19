---
title: '減法平滑 '
description: 'Designer > Substance 合成圖 > Nodes 參考 Substance 合成圖 > Node 函式庫 > SDF 函數 > 運算子 > 減法平滑 '
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---


# 減法平滑

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![減法平滑圖示](./3d-sdf-op-subtraction-smooth.png "減法平滑 ")

<b>收錄於：</b> SDF 函數>運算元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

從 SDF 2 形狀減去 SDF 1 形狀的體積，並在兩者交點處施加可調整平滑。

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
| <b>SDF 1</b> *浮標* | 自衛隊形狀被減去。 |
| <b>SDF 2</b> *浮標* | SDF 形狀從 SDF 1 形狀中減去。 |
| <b>平滑度</b> *浮標* | 在兩個形狀<br><br><i>交點處施加的平滑。注意：</i> 在平滑半徑交點處可能會出現硬邊。 |
