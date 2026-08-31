---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/paint-wear.html"
breadcrumb-title: ''
description: 使用 Paint Wear 節點根據網格幾何生成油漆磨損遮罩，創造逼真的油漆剝落效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Paint Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 油漆磨損
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 6%

---


# 油漆磨損

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](paint-wear.resources/paint-wear-01.png){width="128px"}

<b>收錄於：</b> 基於網格的生成器>遮罩生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

這個面具象徵油漆剝落與邊緣磨損。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>環境遮蔽</b> <i>灰階輸入</i> | 烘焙貼圖用於內部效果和遮罩。 |
| <b>曲率</b> <i>灰階輸入</i> | 烘焙貼圖用於內部效果和遮罩。 |
| <b>變異遮罩</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |
| <b>面具（選用）</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>關卡</b> <i>0.0 - 1.0</i> | 設定總油漆磨損量，逐漸顯現。 |
| <b>對比</b> <i>0.0 - 1.0</i> | 調整結果的對比度。 |
| <b>遮蔽</b> <i>0.0 - 1.0</i> | 它設定了烘烤 AO 在較暗區域防止磨損的效果。 |
| <b>半徑</b> <i>0.0 - 2.0</i> | 用以設定剝落效應從凸邊緣擴散的程度。 |
| <b>變體</b> <i>0.0 - 1.0</i> | 設定變化（如垃圾搖滾）以融入效果中。 |
| <b>覆寫變異遮罩</b> <i>錯誤/真實</i> | 啟用自訂變體（垃圾搖滾）地圖輸入槽。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="paint-wear.resources/paint-wear-02.gif" />
        </td>
    </tr>
</table>
