---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/mosaic.html"
breadcrumb-title: ''
description: 利用 Mosaic 節點將材質分割成像素化方塊和圖案，來創造馬賽克磚塊效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Mosaic
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 馬賽克
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 2%

---


# 馬賽克

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mosaic-1.png){width="128px"}

![](../../../../../../assets/mosaic-grayscale.png){width="128px"}

## 馬賽克（灰階）

**收錄於：***濾鏡/效果*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

透過多重穿越 [曲速](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) 效果，將現有的平滑斜度梯度地圖「Facetising」。 當同一張地圖同時用於兩個輸入時，它會放大並強調最亮的區域。

這對於為灰階貼圖（如 Heightmap）增添更多細緻度很有用，因為它能為形狀帶來更多細緻度。

## 參數

### 輸入

* **色彩**： *色彩/灰階輸入*
* **馬賽克地圖**： *灰階輸入*\
  曲速引擎地圖。 可以和第一次輸入一樣。

### 參數

* **樣本**&#x200B;數： *0 - 16*&#x200B;決定多樣本品質。
* **強度**： *0.0 - 1.0*&#x200B;效果強度。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/mosaci-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
