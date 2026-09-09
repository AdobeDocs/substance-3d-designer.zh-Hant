---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/anisotropic-blur.html"
breadcrumb-title: ''
description: 使用各向異性模糊節點來套用方向模糊效果，來製作動態模糊和條紋效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Anisotropic Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 各向異性模糊
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 8%

---


# 各向異性模糊

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](anisotropic-blur.resources/anisotropic-blur-grayscale.png){width="128px"}

![](anisotropic-blur.resources/anisotropic-blur.png){width="128px"}

<b>收錄於：</b> 模糊>濾鏡

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

能執行高品質 [的方向模糊](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-blur/directional-blur.md)效果，並有幾個設定可自訂外觀。 也被稱為「動態模糊」。

重要：務必使用適合你輸入的版本！ 使用「各向異性模糊」作為色彩輸入，或使用「各向異性模糊灰階」作為灰階輸入。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>強度</b> <i>0.0 - 16.0</i> | 模糊的強度（半徑）。 這個數值越高，模糊的距離就越遠。 |
| <b>各向異性</b> <i>0.0 - 1.0</i> | 模糊的方向性。 把這個設定成 0.0 就等於做一般模糊。 |
| <b>角度</b> <i>0.0 - 1.0</i> | 這樣可以設定模糊方向的角度。 |
| <b>品質</b> <i>0 - 1</i> | 內部會在[盒子模糊](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) 和總部模糊之間切換。 用速度換取品質。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="anisotropic-blur.resources/aniso-blur-example.gif" />
        </td>
    </tr>
</table>
