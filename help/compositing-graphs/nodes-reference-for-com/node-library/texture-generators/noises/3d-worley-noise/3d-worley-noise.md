---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-worley-noise.html"
breadcrumb-title: ''
description: 使用 3D Worley Noise 節點，根據 3D 位置產生 Worley 噪音，以創造體積紋理效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Worley Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 沃利噪音
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---


# 3D 沃利噪音

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-worley.png){width="128px"}

## 3D 沃利噪音

**收錄於：***材質產生器**/噪音*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

它是函式庫中最多功能且先進的噪音之一，根據輸入位置映射在三維空間中產生 Worley 噪音。 有很多選項，讓它比標準 [的 Cells](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md)或 [距離](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md)噪音更有力。

## 參數

* **比例**： *1 - 64*\
  設定效果的全域尺度。
* **尺寸**： *0.0 - 1.0*&#x200B;分別對 X、Y 和 Z 軸進行非均勻縮放。
* **模式**： *歐幾里得、曼哈頓、切比雪夫、明可夫斯基\
  改變距離指標。 這樣可以產生非常不同的噪音類型。*
* **明可夫斯基數：***0.0 - 20.0*&#x200B;僅限於明可夫斯基距離度量。混合不同指標類型。
* **風格**： *F1、F2、F2-F1、邊框、隨機顏色*&#x200B;設定公制組合數學。 這樣可以有更多組合。
* **邊框寬度**： *0.0 - 1.0*&#x200B;當邊框組合數學啟動時，控制邊框的寬度。
* **圓度：***0.0 - 1.0*&#x200B;僅適用於 F1、F2 及 F2-F1 模式。將水平設定在中間位置。
* **反轉**： *錯誤/真實*\
  結果會被反轉。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/3d-worley-ex04.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/3d-worley-ex03.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/3d-worley-ex02.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c3_image" src="../../../../../../assets/3d-worley-ex01.png" width="256px"/></div> |
| --- | --- | --- | --- |
|  |  |  |  |

</td>
</tr>
</table>
