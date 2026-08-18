---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-2.html"
breadcrumb-title: ''
description: 使用 Noise Upscale 2 節點，利用基於噪音的插值來提升貼圖，以維持更大尺寸下的貼圖品質。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 噪音升級 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 1%

---


# 噪音升級 2

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/noise-upscale.png){width="128px"}

## 噪音升級 2

**收錄於：***濾波器/轉換*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

它會將輸入噪音程序放大到雙倍解析度，保留細節但不會引入過多平鋪。 使用「X」型遮罩，混合時對比度比原始輸入低（內部混合模式為最大與最小）。

這個節點主要用來優化使用重且大雜訊的慢速圖形。 它讓你能使用更高解析度，且不會增加太多額外的運算時間。

另 [見噪音放大1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md) 和 [噪音放大3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md) ，了解此過程的不同變化。

## 參數

* **Offset1X**： *0.0 - 1.0*&#x200B;將上下部分滑動於 X 軸上。
* **偏移1Y**： *0.0 - 1.0*\
  上下部分可沿著 Y 軸滑動。
* **Offset2X**： *0.0 - 1.0*&#x200B;將左右零件滑動於 X 軸上。
* **偏移2Y**： *0.0 - 1.0*&#x200B;左右零件滑動於Y軸上。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/noise2ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
