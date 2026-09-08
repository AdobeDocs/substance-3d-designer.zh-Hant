---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/slope-blur.html"
breadcrumb-title: ''
description: 使用 Slope Blur 節點，根據高度圖斜率套用方向模糊效果來製作動態模糊。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Slope Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 斜坡模糊
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 3%

---


# 斜坡模糊

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/slope-blur.png){width="128px"}

![](../../../../../../assets/slope-blur-grayscale.png){width="128px"}

<b>收錄於：</b> 模糊>濾鏡

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

執行一種進階且高品質的模糊效果，其中各向異性/方向由灰階「斜率圖」驅動。 想像它像是斜坡模糊效果沿著斜坡地圖的斜坡移動，就像一個高度圖，類似 [於內部基於的方向扭曲（Directional Warp](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) ）。

這是 Designer 中最有趣且最強大的模糊之一。 它可以用來達成一些非常有趣且意想不到的效果，例如剝落和風化邊緣，或塗抹並滲漏污垢或鏽蝕。

重要：務必使用適合你輸入的版本！ 色彩輸入用「斜坡模糊」，灰階輸入用「斜坡模糊灰階」。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>坡度</b> <i>灰階輸入</i> | 斜率圖驅動各向異性角度。 理想狀況下應該包含斜度漸變;強烈、銳利的過渡效果不佳！ |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>取樣</b> <i>0 - 32</i> | 取樣數量會影響品質，但會犧牲速度。 |
| <b>強度</b> <i>0.0 - 16.0</i> | 模糊的量或強度。 |
| <b>模式</b> <i>模糊、敏、麥克斯</i> | 混合模式用於後續模糊通道。 「模糊」的行為更像標準 [的各向異性模糊](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md)，而最小區域會「侵蝕」現有區域，而最大空間則會「模糊」白色區域。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/slopeblur01.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/slopeblur02.gif" />
        </td>
    </tr>
</table>
