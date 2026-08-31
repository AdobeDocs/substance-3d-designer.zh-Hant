---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-gradient.html"
breadcrumb-title: ''
description: 使用泛光填充到漸層節點，將區域填充漸層值，以創造平滑的色彩過渡。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 從淹水填土到梯度
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 7%

---


# 從淹水填土到梯度

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-gradient.resources/flood-fill-to-gradient-01.png){width="128px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

將 [洪水填充](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) 基底轉換成（隨機定向的）漸層。 對於製作一個隨機傾斜和傾斜的高度圖非常有用。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>洪水填埋</b> <i>色彩輸入</i> | 基礎洪水填充數據。 |
| <b>角度輸入</b> <i>灰階輸入</i> | 視角圖用於用外部圖來判定每格子的角度。 |
| <b>斜率輸入</b> <i>灰階輸入</i> | 可選地圖用以判定每胞體梯度邊坡強度。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>角度</b> <i>0.0 - 1.0</i> | 為所有圖塊設定統一的全局角度/方向。 |
| <b>角度變化</b> <i>0.0 - 1.0</i> | 會隨機化每個格子的角度。 這是最有用且最強大的參數！ |
| <b>乘以包圍盒大小</b> <i>0.0 - 1.0</i> | 會根據圖塊的各個邊界框大小來縮放整個線性效果。 這代表較小的格子會比較大的格子顏色更深。 |
| <b>角度影像輸入乘法器</b> <i>0.0 - 1.0</i> | 設定可選角度輸入貼圖對產生的漸層方向的影響 |
| <b>斜率影像輸入乘法</b> <i>0.0 - 1.0</i> | 設定可選的坡度輸入地圖對生成的梯度坡度強度的影響。 |
| <b>乘以斜率強度</b> <i>0.0 - 1.0</i> |  |
| <b>平坡色</b> <i>（灰階）</i> | 允許設定平坦坡面的實心值。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-gradient.resources/flood-fill-to-gradient-02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-gradient.resources/flood-fill-to-gradient-03.png" />
        </td>
    </tr>
</table>
