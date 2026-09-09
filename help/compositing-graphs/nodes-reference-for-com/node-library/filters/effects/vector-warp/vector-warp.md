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
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 2%

---


# 向量曲速

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](vector-warp.resources/vector-warp.png){width="128px"}

![](vector-warp.resources/vector-warp-grayscale.png){width="128px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

向量扭曲是一種進階的變形效果，類似 [於扭曲](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) 和 [方向扭曲](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md)，主要差異在於它是由（彩色）向量點陣圖驅動，而非灰階映射。 這表示它比原子節點的親戚更強大且多功能。

向量貼圖類似法線貼圖，但不需要正規化，且只使用R與綠色（X與Y）通道。 如果你願意，藍色和 Alpha 通道可以保持黑色。 建立一個好的向量貼圖可能是使用此節點最大的挑戰;你可以將 [灰階貼圖轉為法線](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)，或是透過 RGBA 合併合成通道[來構建貼圖。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md) 另外，像是「流程圖」](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/painting/advanced-channel-painting/flow-map-painting)這類工具[也可以使用。

這個節點在你想做非常特定的失真和不同方向時很有用，而標準的 Warp 節點無法滿足需求。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入</b> <i>色彩輸入</i> | 地圖要扭曲。 |
| <b>向量地圖</b> <i>色彩輸入</i> | 失真驅動器地圖。 使用紅色與藍色通道。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>強度</b> <i>0.0 - 1.0</i> | 向量圖的強度乘數。 |
| <b>向量格式</b> <i>DirectX、OpenGL</i> | 在向上和向下的解讀間交換綠色通道。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="vector-warp.resources/vector-warp-ex.png" />
        </td>
    </tr>
</table>
