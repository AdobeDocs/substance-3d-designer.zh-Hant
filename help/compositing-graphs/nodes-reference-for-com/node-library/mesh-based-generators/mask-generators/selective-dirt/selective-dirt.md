---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/selective-dirt.html"
breadcrumb-title: ''
description: 使用選擇性泥土節點，根據網格幾何產生選擇性泥土累積遮罩，以實現逼真的風化效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Selective Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 選擇性泥土
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 5%

---


# 選擇性泥土

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](selective-dirt.resources/selective-dirt.png){width="128px"}

<b>收錄於：</b> 基於網格的生成器>遮罩生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

這個 [Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) 遮罩代表凸邊上的簡單泥土效果。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>曲率</b> <i>灰階輸入</i> | 烘焙貼圖用於內部效果和遮罩。 |
| <b>變異遮罩</b> <i>灰階輸入</i> | 可透過參數啟用可選的變異地圖。 |
| <b>面具（選用）</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>關卡</b> <i>0.0 - 1.0</i> | 設定效果的總強度，逐步揭露。 |
| <b>對比</b> <i>0.0 - 1.0</i> | 調整結果的對比度。 |
| <b>變體</b> <i>0.0 - 1.0</i> | 設定變化/垃圾搖滾的程度，讓它融入效果中。 |
| <b>覆寫變異遮罩</b> <i>錯誤/真實</i> | 可透過自訂輸入槽覆蓋變體。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="selective-dirt.resources/selective-dirt-ex.gif" />
        </td>
    </tr>
</table>
