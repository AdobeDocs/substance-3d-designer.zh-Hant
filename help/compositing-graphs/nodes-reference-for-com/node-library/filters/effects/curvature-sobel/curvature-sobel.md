---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-sobel.html"
breadcrumb-title: ''
description: 使用 Curvature Sobel 節點來偵測曲率邊，使用索貝爾運算子來建立基於邊緣的遮罩。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 曲率索貝爾
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 1%

---


# 曲率索貝爾

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/curvature-sobel.png){width="128px"}

## 曲率索貝爾

**收錄於：***濾鏡/效果*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

執行簡單且嚴格的單次曲率轉換為輸入 [法線貼](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)圖。 結果的地圖凸面區域帶有白色調，凹面則以黑色調呈現。 曲率總是會產生更粗的線條和銳利的過渡。

此節點有助於快速高亮或調暗特定邊緣。 它與 [Curvature](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md) 略有不同，因為它產生的效果品質較佳，但仍帶有銳利且刺耳的感覺。

## 參數

* **強度**： *0.0 - 1.0*&#x200B;效果強度，調整對比度。
* **一般類型**： *DirectX、OpenGL*

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/curv-sobel-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
