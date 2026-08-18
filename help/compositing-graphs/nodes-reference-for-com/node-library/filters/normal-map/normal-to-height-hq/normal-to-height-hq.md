---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height-hq.html"
breadcrumb-title: ''
description: 使用「法線高度」節點將法線貼圖轉換成高品質的高度貼圖，以便擷取表面細節。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal To Height HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 標準至高度總部
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---


# 標準至高度總部

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-to-height-hq.png){width="128px"}

## 標準至高度總部

**收錄於：***濾鏡/法線貼圖*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

一個反向轉換節點，嘗試將切線空間法線貼圖轉換回高度圖。 這是較進階的節點; [法線到高度](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height/normal-to-height.md) 的選項較少，且使用不同的計算方式。

這對於只有法線貼圖來源，但又想將它與高度貼圖結合執行操作時非常有用。 請記住，這永遠無法提供百分之百正確的結果，因為當高度轉換成一般時，資訊會因過程而遺失。 它永遠無法取代正確生成的高度圖！

## 參數

* **一般格式**： *DirectX、OpenGL*\
  切換不同的法線貼圖格式（反轉綠色通道）。
* **緩解平衡**： *0.0 - 1.0*&#x200B;低頻與高頻偏壓的混合。
* **高度強度**： *0.0 - 1.0*&#x200B;強度或乘數，適用於高度圖，運作方式有點像全域不透明度。
* **高度標準化**： *False/True*&#x200B;會自動縮放高度圖範圍，使用全對比度，類似 [自動調平](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md)。
* **品質**： *正常，高速*，速度與品質間切換。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/normal2height-hq-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
