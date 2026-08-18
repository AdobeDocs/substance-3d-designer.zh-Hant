---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/function-node-library/function-nodes-random/hash-functions.html"
breadcrumb-title: ''
description: 在函數圖中使用雜湊函數，根據輸入座標產生確定性的隨機值。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Function node library > Random > Hash
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 雜湊函數
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 1%

---


# 雜湊函數

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![雜湊節點：圖示](../../../../../assets/hash-icon.png "雜湊節點：圖示"){width="200px"}

<b>收錄於：</b>隨機函數>

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據作為種子的輸入值，計算一個介於0與1之間的偽隨機值。

標題中的數字顯示的是入入值和出值的類型。 例如：雜湊 23 輸入 float2 並輸出 float3 值。

</td>
</tr>
</table>

當雜湊節點輸出多個成分的值時，每個成分具有不同的偽隨機值。

可用版本及其輸入類型與輸出類型：

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>雜湊 11：</b> 浮點數浮點數→浮點數

<b>雜湊 14：</b> 浮點數 → 浮點數 4

<b>雜湊 21：</b> Float2 → Float

<b>雜湊 22：</b> Float2 → Float2

</td>
<td style="border: 0;" valign="top">

<b>雜湊 24：</b> Float2 → Float4

<b>Hash31：</b> Float3 → Float

<b>雜湊 32：</b> Float3 → Float2

</td>
</tr>
</table>

## 輸入連接器

|  |  |
| --- | --- |
| <b>輸入</b> | 作為計算偽隨機輸出的種子值。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![雜湊 14 範例](../../../../../assets/hash14-example.png "雜湊 14 範例"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![雜湊 32 範例](../../../../../assets/hash32-example.png "雜湊 32 範例"){zoomable="yes"}

</td>
</tr>
</table>
