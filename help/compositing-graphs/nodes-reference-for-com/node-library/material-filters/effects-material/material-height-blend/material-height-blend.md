---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/material-height-blend.html"
breadcrumb-title: ''
description: 使用 Material Height Blend 節點，根據高度圖混合多個材質，創造分層材質效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Material Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材料高度混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 1%

---


# 材料高度混合

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-height-blend.png){width="128px"}

## 材料高度混合

**收錄於：***材質濾鏡/效果*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

這個節點是 Height Blend](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/height-blend/height-blend.md) 的進階版本[，根據 Heightmap 混合兩個材質。沒有使用者自訂遮罩，因此你必須有兩個高度貼圖，分別對應每個材質，且至少有一個不是統一的值。

這對於結合兩種不同且高品質的材料，無需高品質的混色遮膜非常有用。

如果你想融入水或雪，則可以使用「雪覆蓋」](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md)和[「水位](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md)」這兩個節點[。

## 參數

### 參數

* **頻道**\
  在這個群組中切換材質通道，例如使用鏡面/光澤貼圖而非金屬/粗糙度時。
* **高度偏移**： *0.0 - 1.0*&#x200B;偏移高度貼圖，使混合層級沿高度軸移動。 這是混合的主要控制。
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整混合的對比度，讓轉場更銳利。
* **模式**： *平衡高度，底部高度優先，*&#x200B;可在兩種不同混合模式間切換。
* **不透明度**： *0.0 - 1.0*\
  混合前景高度的不透明度，讓它淡入或淡出。
* **反照率匹配**： *0.0 - 1.0*&#x200B;反照率顏色之間可進行的內部色彩匹配量。

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
