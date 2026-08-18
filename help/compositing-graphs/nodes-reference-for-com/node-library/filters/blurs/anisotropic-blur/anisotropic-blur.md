---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/anisotropic-blur.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 1%

---


# 各向異性模糊

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/anisotropic-blur-grayscale.png){width="128px"}

![](../../../../../../assets/anisotropic-blur.png){width="128px"}

## 各向異性模糊（灰階）

**收錄於：***濾鏡/模糊*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

能執行高品質 [的方向模糊](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-blur/directional-blur.md)效果，並有幾個設定可自訂外觀。 也被稱為「動態模糊」。

重要：務必使用適合你輸入的版本！ 使用「各向異性模糊」作為色彩輸入，或使用「各向異性模糊灰階」作為灰階輸入。

## 參數

* **&#x200B;**&#x200B;強度：*0.0 - 16.0*&#x200B;模糊強度（半徑）。這個數值越高，模糊的距離就越遠。
* **各向異性**： *0.0 - 1.0*&#x200B;模糊的方向性。 把這個設定成 0.0 就等於做一般模糊。
* **角度**： *0.0 - 1.0*&#x200B;設定模糊方向的角度。
* **品質**： *0 - 1*&#x200B;內部在[盒子模糊](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) 和 HQ 模糊之間切換。 用速度換取品質。

## 範例圖片

![](../../../../../../assets/aniso-blur-example.gif)

</td>
</tr>
</table>
