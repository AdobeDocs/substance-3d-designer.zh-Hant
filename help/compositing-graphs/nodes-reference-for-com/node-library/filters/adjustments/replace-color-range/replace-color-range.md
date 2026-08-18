---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/replace-color-range.html"
breadcrumb-title: ''
description: 使用「替換色彩範圍」節點，將指定範圍內的顏色替換為新顏色以進行色彩校正。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Replace Color Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 替換色彩範圍
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---


# 替換色彩範圍

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/replace-color-range.png){width="128px"}

## 替換色彩範圍

**收錄於：***濾鏡/調整*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

將來源顏色替換為目標顏色，並加入額外控制項。 例如可以用來重新著色材質 ID 貼圖的部分（烘焙）。

欲了解更進階版本，請參見 [色彩匹配。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-match/color-match.md)

## 參數

* **來源顏色**：*（顏色值）*要替換的顏色。
* **目標顏色**：*（顏色值）*用來替換的顏色。
* **來源範圍**： *0.0 -* 1.0\
  選擇的源頭範圍或容忍度。 可以增加，使鄰近的顏色也會有色相偏移。
* **閾值**： *0.0 - 1.0*&#x200B;距離衰減/對比度。 設定低以只替換源色，調高則替換與源色融合的顏色。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/replace-color-range-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
