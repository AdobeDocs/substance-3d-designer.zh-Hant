---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/glow.html"
breadcrumb-title: ''
description: 使用Glow節點為材質添加發光效果，創造發光且發光的材質外觀。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 發光
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---


# 發光

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/glow-greyscale.png){width="128px"}

![](../../../../../../assets/glow-3.png){width="128px"}

## 發光

**收錄於：***濾鏡/效果*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

能產生類似「外層光暈」的效果，類似其他熱門影像編輯軟體。 基本上是在輸入周圍加上漸變的漸層輪廓。

請注意，這並非針對帶有 Alpha 通道的影像設計，正如你所預期的。 即使是彩色版本，也只期望輸入二進位黑白遮罩;它只允許使用彩色螢光。 如果你想要能處理透明影像的版本，請參考 [Shape Glow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-glow/shape-glow.md)。

重要：務必使用適合你輸入的版本！ 用「Glow」來表示顏色輸入，或用「Glow Grayscale」來表示灰階輸入。

## 參數

* **發光量**： *0.0 - 1.0*&#x200B;全域不透明度用於發光效果。
* **清除量**： *0.0 - 1.0* Treshold，用於何時切斷發光效果。 適合半透明區域。
* **發光大小**： *0.0 - 20.0*&#x200B;控制發光效果的範圍。
* **發光顏色**：*（色彩值）（僅限彩色版本）*設定發光效果的顏色。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/glow-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
