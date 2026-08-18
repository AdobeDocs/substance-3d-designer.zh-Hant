---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-warp.html"
breadcrumb-title: ''
description: 使用 Vector Warp 節點利用向量場來扭曲材質，創造流暢且有機的變形效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 向量曲速
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# 向量曲速

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/vector-warp.png){width="128px"}

![](../../../../../../assets/vector-warp-grayscale.png){width="128px"}

## 向量扭曲（灰階）

**收錄於：***濾鏡/效果*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

向量扭曲是一種進階的變形效果，類似 [於扭曲](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) 和 [方向扭曲](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md)，主要差異在於它是由（彩色）向量點陣圖驅動，而非灰階映射。 這表示它比原子節點的親戚更強大且多功能。

向量貼圖類似法線貼圖，但不需要正規化，且只使用R與綠色（X與Y）通道。 如果你願意，藍色和 Alpha 通道可以保持黑色。 建立一個好的向量貼圖可能是使用此節點最大的挑戰;你可以將 [灰階貼圖轉為法線](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)，或是透過 RGBA 合併合成通道[來構建貼圖。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md) 另外，像是「流程圖」](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/painting/advanced-channel-painting/flow-map-painting)這類工具[也可以使用。

這個節點在你想做非常特定的失真和不同方向時很有用，而標準的 Warp 節點無法滿足需求。

## 參數

### 輸入

* **輸入**： *彩色輸入*\
  地圖要扭曲。
* **向量映射**： *色彩輸入*\
  失真驅動器地圖。 使用紅色與藍色通道。

### 參數

* **強度**： *0.0 - 1.0*&#x200B;向量地圖的強度乘數。
* **向量格式**： *DirectX，OpenGL*&#x200B;會在上行和下行的解讀間交換綠色通道。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/vector-warp-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
