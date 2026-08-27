---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/lighting-cancel-high-frequencies.html"
breadcrumb-title: ''
description: 使用光照取消高頻節點，將材質分析時的貼圖中高頻光照細節移除。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Lighting Cancel High Frequencies
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 燈光抵消高頻
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 7%

---


# 燈光抵消高頻

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](lighting-cancel-high-frequencies.resources/lighting-cancel-high-frequencies.png){width="128px"}

<b>收錄於：</b> 篩選>調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

類似 [於 Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)，但更適合全彩影像（不會讓結果去飽和度那麼高），這個節點試圖抵消高頻和細微的光照細節。

另見 [「Light Cancel Low Frequencys」](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md)以及更進階且推薦 [的 Luminance Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/luminance-highpass/luminance-highpass.md)。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>強度</b> <i>0.0 - 1.0</i> | 光影抵消效果的強度。 |
| <b>半徑</b> <i>0.0 - 10.0</i> | 可以取消燈光細節的半徑或大小。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="lighting-cancel-high-frequencies.resources/lighting-cancel-highfrequencies-example.png" />
        </td>
    </tr>
</table>
