---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/mosaic.html"
breadcrumb-title: ''
description: 利用 Mosaic 節點將材質分割成像素化方塊和圖案，來創造馬賽克磚塊效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Mosaic
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 馬賽克
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 6%

---


# 馬賽克

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](mosaic.resources/mosaic-1.png){width="128px"}

![](mosaic.resources/mosaic-grayscale.png){width="128px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

透過多重穿越 [曲速](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) 效果，將現有的平滑斜度梯度地圖「Facetising」。 當同一張地圖同時用於兩個輸入時，它會放大並強調最亮的區域。

這對於為灰階貼圖（如 Heightmap）增添更多細緻度很有用，因為它能為形狀帶來更多細緻度。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>顏色</b> <i>色彩/灰階輸入</i> |  |
| <b>馬賽克地圖</b> <i>灰階輸入</i> | 曲速引擎地圖。 可以和第一次輸入一樣。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>取樣</b> <i>0 - 16</i> | 決定多樣本品質。 |
| <b>強度</b> <i>0.0 - 1.0</i> | 效果的強度。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="mosaic.resources/mosaci-ex.png" />
        </td>
    </tr>
</table>
