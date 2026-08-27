---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dust.html"
breadcrumb-title: ''
description: 利用 Dust 節點根據網格幾何產生塵埃累積遮罩，創造逼真的塵埃與污垢效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 塵埃
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 5%

---


# 塵埃

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dust.resources/dust.png){width="128px"}

<b>收錄於：</b> 基於網格的生成器>遮罩生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此遮罩代表積聚在遮蔽、低矮區域的塵埃，以及僅在朝上方的區域。 需要正確的 AO 和世界空間法線才能運作。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>環境遮蔽</b> <i>灰階輸入</i> | 用於塵埃擺放的烘焙地圖。 必備！ |
| <b>世界太空常態</b> <i>色彩輸入</i> | 用於塵埃擺放的烘焙地圖。 必備！ |
| <b>噪音</b> <i>灰階輸入</i> | 自訂塵埃貼圖（可選），僅在覆蓋噪音設定為 True 時才會出現。 |
| <b>面具（選用）</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>關卡</b> <i>0.0 - 1.0</i> | 設定總塵埃量。 |
| <b>對比</b> <i>0.0 - 1.0</i> | 調整灰塵的對比度。 |
| <b>遮蔽量</b> <i>0.0 - 1.0</i> | AO的影響;在被遮蔽的區域會出現更多灰塵。 |
| <b>雜訊不透明度</b> <i>0.0 - 1.0</i> | 設定在塵封區域可見的噪音量。 |
| <b>覆蓋噪音</b> <i>錯誤/真實</i> | 設定為使用自訂塵埃地圖輸入。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dust.resources/dust-ex.gif" />
        </td>
    </tr>
</table>
