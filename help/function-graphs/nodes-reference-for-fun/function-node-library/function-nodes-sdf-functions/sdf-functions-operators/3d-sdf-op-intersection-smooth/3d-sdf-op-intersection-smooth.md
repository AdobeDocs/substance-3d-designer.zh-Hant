---
title: 交集平滑
description: Designer > Substance 合成圖 > Nodes 參考 Node 函式庫 >> SDF 函式 > 交集平滑運算>子
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---


# 交集平滑

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![交集平滑圖示](./3d-sdf-op-intersection-smooth.png "，交集平滑")

<b>收錄於：</b> SDF 函數>運算元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

回傳兩個 SDF 形狀共有的體積，實際上是兩個形狀重疊處所產生的體積，並可調整其交集邊緣的平滑。

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
| <b>SDF 1</b> *浮標* | 第一個SDF形狀。 |
| <b>SDF 2</b> *浮標* | 第二個SDF陣型。 |
| <b>平滑度</b> *浮標* | 兩個 SDF 形狀交點處邊的平滑度。<br><br><i>注意：</i> 在平滑半徑交點處可能會出現硬邊。<br><br><i>預設值：0</i> |
