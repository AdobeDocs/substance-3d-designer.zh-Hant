---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/height-blend.html"
breadcrumb-title: ''
description: 使用 Height Blend 節點根據高度貼圖來混合材質，創造逼真的材質過渡。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 高度混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 5%

---


# 高度混合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-blend.resources/height-blend.png){width="128px"}

<b>收錄於：</b> 《材料濾>效應》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據高度資訊組合兩個高度圖。 會產生混合的高度圖，也會產生一個黑白遮罩，可用於其他地方。

這在你有兩個高品質高度貼圖要合併時很有用，但不一定是完整材質，因為材質高度混合[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/material-height-blend/material-height-blend.md)是必要的。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>高度頂端</b> <i>灰階輸入</i> |  |
| <b>身高底</b> <i>灰階輸入</i> |  |
| <b>面具（選用）</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>身高偏移</b> <i>0.0 - 1.0</i> | Offsets Heightmaps，讓混合層級沿高度軸移動。 這是混合的主要控制。 |
| <b>對比</b> <i>0.0 - 1.0</i> | 調整混合的對比度，讓轉場更銳利。 |
| <b>模式</b> <i>平衡高度，底部高度優先</i> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 混合前景高度的不透明度，讓它淡入或淡出。 |
