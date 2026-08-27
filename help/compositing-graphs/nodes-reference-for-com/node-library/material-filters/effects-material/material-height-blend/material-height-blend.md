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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 4%

---


# 材料高度混合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-height-blend.resources/material-height-blend.png){width="128px"}

<b>收錄於：</b> 《材料濾>效應》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這個節點是 Height Blend[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/height-blend/height-blend.md) 的進階版本，根據 Heightmap 混合兩個材質。沒有使用者自訂遮罩，因此你必須有兩個高度貼圖，分別對應每個材質，且至少有一個不是統一的值。

這對於結合兩種不同且高品質的材料，無需高品質的混色遮膜非常有用。

如果你想融入水或雪，則可以使用「雪覆蓋」[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md)和[「水位](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md)」這兩個節點。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>頻道</b> | 在這個群組中切換材質通道，例如使用鏡面/光澤貼圖而非金屬/粗糙度時。 |
| <b>身高偏移</b> <i>0.0 - 1.0</i> | Offsets Heightmaps，讓混合層級沿高度軸移動。 這是混合的主要控制。 |
| <b>對比</b> <i>0.0 - 1.0</i> | 調整混合的對比度，讓轉場更銳利。 |
| <b>模式</b> <i>平衡高度，底部高度優先</i> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 混合前景高度的不透明度，讓它淡入或淡出。 |
| <b>反照率匹配</b> <i>0.0 - 1.0</i> | 反照率顏色之間需要進行的內部色彩匹配量。 |
