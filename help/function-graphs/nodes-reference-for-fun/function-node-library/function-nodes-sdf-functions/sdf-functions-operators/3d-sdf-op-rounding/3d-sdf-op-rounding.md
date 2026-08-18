---
title: 四捨五入
description: Designer > Substance 合成圖 > Nodes 參考 Substance 合成圖 > Node 函式庫 > SDF 函式 > 運算子>四捨五入
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 1%

---


# 四捨五入

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![四捨五入圖示](./3d-sdf-op-rounding.png "四捨五入")

<b>收錄於：</b> SDF 函數>運算元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

擴大SDF形狀，使其充氣並磨平硬邊。

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
| <b>半徑</b> *浮標* | 加在形狀邊緣上的圓弧半徑。<br><br><i>注意：</i> 硬邊可能會出現在圓弧半徑交點處。<br><br><i>預設值：0.05</i> |
