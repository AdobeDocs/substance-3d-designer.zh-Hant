---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/normal.html"
breadcrumb-title: ""
description: 使用法線節點來處理和操作法線貼圖貼圖，以控制表面細節和光照。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 正常
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 1%
---

# 正常

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![原子節點：正常](normal.resources/comp_normal_1.png "原子節點：正常"){width="100%"}

<b>收錄於：</b> 原子節點

</td>
<td style="border: 0;" valign="top">

從灰階影像（解讀為高度圖）計算法線貼圖。

節點會將輸入的灰階映射轉換成切空間法線映射輸出。 它有幾個使用者設定強度和編碼選項。

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="normal.resources/normal-tooltip.gif" alt="一般提示" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

這是一個非常實用的節點，經常用來將高度圖輸入轉換為即時就緒材質的法線貼圖。 在「正常 Sobel[&#128279;](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-sobel/normal-sobel.md)」和「身高到正常世界單位」中也有替代方案。



## 參數

|  |  |
| --- | --- |
| <b>強度</b> *浮標* | 修改高度圖的強度。   設定輸入高度圖轉換成法線時的強度。 根據輸入映射，超過 100 的數值影響不大。 |
| <b>標準格式</b> *布林值* | 將高度圖（OpenGL）的 Y 座標反轉。   設定綠色（Y）通道的編碼方式。 基本上就是一個「翻綠/Y」開關。 |
| <b>Alpha 通道內容</b> *布林值* | 用輸入貼圖填滿法線貼圖的 alpha 通道。   以輸入填充 Alpha/強制 Alpha 為 1：此方法允許將 Alpha 通道設為實心，而非將輸入作為額外的 Alpha。 |

## 輸入連接器

|  |  |
| --- | --- |
| <b>輸入</b> *灰階* 初級 | 輸入影像被解讀為高度圖。 |


## 範例

*即將推出。*
