---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-selector.html"
breadcrumb-title: ''
description: 使用材質選擇節點，根據網格資料選擇材質，以建立多材質材質效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Selector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材質選擇器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---


# 材質選擇器

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-selector.png){width="128px"}

## 材質選擇器

**收錄於：***基於網狀的發電機**/工具*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

將全彩 ID 映射轉換為二進位黑白遮罩。 允許將不同顏色混合並組合成一個遮罩。

如果你不想用 [多材質混合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md) ，偏好手動使用遮罩，或者想在其他地方手動使用相同的遮罩，這很方便。

## 參數

* **材料**：1 - 16\
  集合可啟用的材料數量。
* **啟用資料 #1-16**：錯誤/真實\
  切換顏色混合與組合到最終輸出遮罩中。 你可以啟用任意多種顏色組合。
* **材料 #1-16**：（色彩值）\
  用來選色材料的顏色，這些材質會轉成黑白。
* **色彩選擇器的參數**\
  修改色彩的混合與黑白轉換。
  * **模糊度**：0.01 - 1.0\
    要與鄰近的顏色融合多少。
  * **填充：** 0.0 - 1.0\
    過渡的銳利度，就像對比。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/matselector-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
