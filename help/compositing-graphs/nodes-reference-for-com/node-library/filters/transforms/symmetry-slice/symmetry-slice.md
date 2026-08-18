---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry-slice.html"
breadcrumb-title: ''
description: 使用 Symmetry Slice 節點沿著對稱軸切片貼圖，創造鏡像圖案和效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry Slice
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 對稱切片
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---


# 對稱切片

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mirror-2.png){width="128px"}

## 對稱切片

**收錄於：***濾波器/轉換*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

複雜對稱/鏡像操作節點。 允許進行多種幾何運算並完全控制，但需要一些實驗。

與 [鏡像](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md) 與 [對稱](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/symmetry/symmetry.md)相比，這個節點有更多選擇。

## 參數

* **對稱模式**： *0 - 6*&#x200B;選擇對稱幾何形狀/鏡面線。 選項有水平、垂直、對角左右、對角左右、垂直倒轉、角落和斜角。
* **傳輸模式**： *0 - 6\
  混合模式。 選項包括：*
* **Blend**： *0.0 - 1.0*&#x200B;將原始影像重新混合回結果中。
* **反面**： *假/真*&#x200B;反翻原點，意指原點的操作反轉。 例如，從左到右的對稱會變成從右到左。
* **反面2**： *假/真*&#x200B;僅在對稱模式為5或6時使用。 翻轉角落的起點。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/symslice.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
