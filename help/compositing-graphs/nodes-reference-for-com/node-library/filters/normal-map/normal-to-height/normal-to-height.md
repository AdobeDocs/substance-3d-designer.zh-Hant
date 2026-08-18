---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height.html"
breadcrumb-title: ''
description: 使用法線到高度節點將法線貼圖轉換成高度貼圖，以提取表面深度資訊。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal to Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 法線至高度
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---


# 法線至高度

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-to-height.png){width="128px"}

## 法線至高度

**收錄於：***濾鏡/法線貼圖*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

一個反向轉換節點，嘗試將切線空間法線貼圖轉換回高度圖。 這是稍微簡化的版本; [法線高度的總部](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height-hq/normal-to-height-hq.md) 有更多選項。

這對於只有法線貼圖來源，但又想將它與高度貼圖結合執行操作時非常有用。 請記住，這永遠無法提供百分之百正確的結果，因為當高度轉換成一般時，資訊會因過程而遺失。 如果你調整設定，這個非 HQ 版本在轉換簡單細節方面做得還不錯。

## 參數

* **緩解平衡**： *0.0 - 1.0*&#x200B;調整不同頻率對最終結果的影響程度。 這很大程度上取決於輸入地圖，需要相當多的調整。
* **一般格式**： *DirectX、OpenGL*\
  切換不同的法線貼圖格式（反轉綠色通道）。
* **全域不透明度**： *0.0 - 1.0*&#x200B;調整效果的全域不透明度。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/normal2heightex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
