---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/sun-bleach.html"
breadcrumb-title: ''
description: 使用 Sun Bleach 節點根據陽光照射產生遮罩，創造逼真的陽光漂白和褪色效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Sun Bleach
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 日曬漂白
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 5%

---


# 日曬漂白

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](sun-bleach.resources/sun-bleach-01.png){width="128px"}

<b>收錄於：</b> 基於網格的生成器>遮罩生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

這個遮罩類似 [光](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/light/light.md)，但也支援 AO，形成一個代表光線漂白與漸淡的遮罩，疊加在效果之上。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>正常世界空間</b> <i>色彩輸入</i> |  |
| <b>環境遮蔽</b> <i>灰階輸入</i> | 烘焙貼圖用於內部效果和遮罩。 |
| <b>面具（選用）</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>關卡</b> <i>0.0 - 1.0</i> | 設定漂白總量，效果會往下移動。 |
| <b>對比</b> <i>0.0 - 1.0</i> | 調整結果的對比度。 |
| <b>遮蔽</b> <i>0.0 - 1.0</i> | 設定AO對最終結果的影響。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="sun-bleach.resources/sun-bleach-02.gif" />
        </td>
    </tr>
</table>
