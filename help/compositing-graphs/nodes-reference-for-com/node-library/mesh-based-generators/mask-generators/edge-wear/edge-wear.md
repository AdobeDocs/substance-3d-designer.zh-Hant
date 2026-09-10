---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-wear.html"
breadcrumb-title: ''
description: 使用邊緣磨損節點在網格邊緣產生磨損遮罩，以創造逼真的邊緣損傷和風化效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 邊緣磨損
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 6%

---


# 邊緣磨損

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-wear.resources/edge-wear.png){width="128px"}

<b>收錄於：</b> 基於網格的生成器>遮罩生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此節點代表物件邊緣的磨損。 它有不少參數，但使用起來並不容易：我們建議你多試試看，感受一下。 節點功能相當強大，雖然無法自訂覆蓋遮罩。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>曲率</b> <i>灰階輸入</i> | 用於內部效果與遮罩的烘焙貼圖 |
| <b>面具（選用）</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>關卡</b> <i>0.0 - 1.0</i> | 設定效果的總擴散範圍。 |
| <b>對比</b> <i>0.0 - 1.0</i> | 調整結果的對比度。 |
| <b>門檻</b> <i>0.0 - 1.0</i> | 類似等級，設定效果的總擴散。 |
| <b>邊寬度</b> <i>0.0 - 1.0</i> | 設定高光效果的飽滿度。 減少讓它們更稀疏。 |
| <b>混亂</b> <i>0.0 - 1.0</i> | 這樣可以調整噪音的大小，讓聲音融合進去，打破平滑感。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-wear.resources/edge-wear-ex.gif" />
        </td>
    </tr>
</table>
