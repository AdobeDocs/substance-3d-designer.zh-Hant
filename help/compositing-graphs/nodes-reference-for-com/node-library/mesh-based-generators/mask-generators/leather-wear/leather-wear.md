---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leather-wear.html"
breadcrumb-title: ''
description: 使用皮革穿戴節點，根據網格曲率和接觸點在皮革表面產生磨損面罩。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leather Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 皮革服飾
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 5%

---


# 皮革服飾

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](leather-wear.resources/leather-wear-01.png){width="128px"}

<b>收錄於：</b> 基於網格的生成器>遮罩生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此面具以皮革圖案代表磨損，邊緣磨損更多，基於曲線。 其功能類似 [玻璃纖維邊緣磨損](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear/fiber-glass-edge-wear.md) ，且參數大致相同。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>曲率</b> <i>灰階輸入</i> | 用於邊緣放置的烘焙地圖。 必備！ |
| <b>環境遮蔽</b> <i>灰階輸入</i> | 烘焙地圖會遮蔽某些區域。 建議，但不是必須的。 |
| <b>垃圾搖滾輸入</b> <i>灰階輸入</i> | 可選的 Grunge 地圖輸入槽，可透過「使用自訂 Grunge」參數切換。 |
| <b>面具（選用）</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>磨損程度</b> <i>0.0 - 1.0</i> | 設定全球磨損水平，逐步揭示。 |
| <b>戴對比</b> <i>0.0 - 1.0</i> | 設定效果的對比。 |
| <b>垃圾搖滾量</b> <i>0.0 - 1.0</i> | 設定髒污（預設皮革圖案）的量，讓邊緣間融合。 |
| <b>環境遮蔽</b> <i>0.0 - 1.0</i> | 設定 AO 掩蓋磨損影響的程度。 |
| <b>曲率權重</b> <i>0.0 - 1.0</i> | 設定曲率邊緣對最終結果的影響程度。 即使設定為 0，你仍然需要曲率貼圖。 |
| <b>使用自訂垃圾搖滾</b> <i>錯誤/真實</i> | 可覆蓋內建預設皮革圖案。 改用自訂輸入槽吧。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="leather-wear.resources/leather-wear-02.gif" />
        </td>
    </tr>
</table>
