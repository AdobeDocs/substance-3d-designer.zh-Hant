---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-filter-node.html"
breadcrumb-title: ''
description: 利用 Bevel 濾鏡節點在形狀和圖案上製作斜邊，增加深度與立體感。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 斜角（濾波節點）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---


# 斜角（濾波節點）

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/bevel.png){width="128px"}

## 斜面

**收錄於：***濾鏡/效果*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

在輸入的灰階高度圖上呈現邊緣斜面效果。 會回傳斜角高度圖和基於該高度圖的法線貼圖。

這是一個有用的節點，用於在理想情況下的二元值（高縮約黑白）基本高度圖上套用精確曲線剖面。

## 參數

### 輸入

* **輸入**： *灰階輸入*\
  高度圖需要轉換。
* **自訂曲線**： *灰階輸入*\
  決定精確曲線/坡度的梯度。 理想狀況是有個漸層線性節點，可以做任何調整，比如 [等級](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) 或 [曲線](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)。 只有當「使用自訂曲線」為真時才會啟動。

### 參數

* **距離**： *-1.0 - 1.0*&#x200B;斜面效果應該延伸到多遠。
* **角型**： *圓形、角形*&#x200B;斜面輪廓應該是圓角還是直角。
* **平滑度**： *0.0 - 5.0*&#x200B;斜角後還要做多少額外的平滑（模糊）。
* **使用非均勻模糊**： *假/真*&#x200B;是否應該進行非均勻平滑。
* **使用自訂曲線**： *假/真*&#x200B;切換 使用你自己的自訂高度曲線。 更多資訊請參考上文。
* **法線強度**： *生成的法線貼圖強度為 0.0 - 50.0*。
* **一般格式**： *DirectX、OpenGL*\
  切換不同的法線貼圖格式（將綠色通道反轉）。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/bevel-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
