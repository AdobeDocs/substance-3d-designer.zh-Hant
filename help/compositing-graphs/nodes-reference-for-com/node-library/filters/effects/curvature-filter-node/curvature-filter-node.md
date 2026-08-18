---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-filter-node.html"
breadcrumb-title: ''
description: 使用曲率濾波器節點，從高度圖產生曲率圖，以偵測凸面與凹面。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 曲率（濾波節點）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---


# 曲率（濾波節點）

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/curvature-1.png){width="128px"}

## 曲率

**收錄於：***濾鏡/效果*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

執行簡單且嚴格的單次曲率轉換為輸入 [法線貼](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)圖。 結果的地圖凸面區域帶有白色調，凹面則以黑色調呈現。 曲率總是會產生像素級的細線和銳利的過渡。

這個節點對於快速高亮或調暗某些邊緣很有用。 與 Curvature Smooth](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md)（品質較高）和 [Curvature Sobel](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md)（選項較多）相比[，它有限制。

## 參數

* **強度**： *0.0 - 10.0*&#x200B;效果強度。 這樣可以增加結果的對比度。
* **一般格式**： *DirectX、OpenGL*\
  切換不同的法線貼圖格式（反轉綠色通道）。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/curvature-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
