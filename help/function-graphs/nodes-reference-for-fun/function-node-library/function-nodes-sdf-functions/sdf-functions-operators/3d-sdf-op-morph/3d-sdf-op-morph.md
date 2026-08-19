---
title: 變形
description: Designer > Substance 合成圖 > Node 參考 Node 函式庫 > SDF 函式 > Operator > Morph 的 Substance 合成>圖
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---


# 變形

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![變形圖示](./3d-sdf-op-morph.png "變形")

<b>收錄於：</b> SDF 函數>運算元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

回傳根據可調整混合因子，基底 SDF 形狀與目標 SDF 形狀之間的線性插值值。

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
| <b>基地自衛隊</b> *浮標* | 基本的自衛隊形狀。 |
| <b>目標自衛隊</b> *浮標* | 目標自衛隊形狀。 |
| <b>混合因子</b> *浮標* | 混合因子用於變形輸入形狀，0 是基礎形狀，1 是目標形狀。 |
