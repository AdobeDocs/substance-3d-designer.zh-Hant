---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-2.html"
breadcrumb-title: ''
description: 使用 Noise Upscale 2 節點，利用基於噪音的插值來提升貼圖，以維持更大尺寸下的貼圖品質。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 噪音升級 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 6%

---


# 噪音升級 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/noise-upscale.png){width="128px"}

<b>收錄於：</b> 《濾波器>轉換》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

它會將輸入噪音程序放大到雙倍解析度，保留細節但不會引入過多平鋪。 使用「X」型遮罩，混合時對比度比原始輸入低（內部混合模式為最大與最小）。

這個節點主要用來優化使用重且大雜訊的慢速圖形。 它讓你能使用更高解析度，且不會增加太多額外的運算時間。

另 [見噪音放大1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md) 和 [噪音放大3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md) ，了解此過程的不同變化。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>偏移1X</b> <i>0.0 - 1.0</i> | 上下部分沿 X 軸滑動。 |
| <b>偏移1年</b> <i>0.0 - 1.0</i> | 上下部分可沿著 Y 軸滑動。 |
| <b>偏移2X</b> <i>0.0 - 1.0</i> | 在 X 軸上滑動左右零件。 |
| <b>偏移2Y</b> <i>0.0 - 1.0</i> | 左右滑動零件在 Y 軸上。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/noise2ex.png" />
        </td>
    </tr>
</table>
