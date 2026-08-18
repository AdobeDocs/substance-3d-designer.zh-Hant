---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/slope-blur.html"
breadcrumb-title: ''
description: 使用 Slope Blur 節點，根據高度圖斜率套用方向模糊效果來製作動態模糊。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Slope Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 斜坡模糊
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 1%

---


# 斜坡模糊

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/slope-blur.png){width="128px"}

![](../../../../../../assets/slope-blur-grayscale.png){width="128px"}

## 斜坡模糊（灰階）

**收錄於：***濾鏡/模糊*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

執行一種進階且高品質的模糊效果，其中各向異性/方向由灰階「斜率圖」驅動。 想像它像是斜坡模糊效果沿著斜坡地圖的斜坡移動，就像一個高度圖，類似 [於內部基於的方向扭曲（Directional Warp](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) ）。

這是 Designer 中最有趣且最強大的模糊之一。 它可以用來達成一些非常有趣且意想不到的效果，例如剝落和風化邊緣，或塗抹並滲漏污垢或鏽蝕。

重要：務必使用適合你輸入的版本！ 色彩輸入用「斜坡模糊」，灰階輸入用「斜坡模糊灰階」。

## 參數

### 輸入

* **斜率**： *灰階輸入*&#x200B;斜率圖以驅動各向異性角度。 理想狀況下應該包含斜度漸變;強烈、銳利的過渡效果不佳！

### 參數

* **取樣**&#x200B;數： *0 - 32*&#x200B;取樣數，會影響品質，但會犧牲速度。
* **強度**： *0.0 - 16.0*\
  模糊的量或強度。
* **模式**： *模糊、最小、極限*|\
  混合模式用於後續模糊通道。 「模糊」的行為更像標準 [的各向異性模糊](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md)，而最小區域會「侵蝕」現有區域，而最大空間則會「模糊」白色區域。

## 範例圖片

![](../../../../../../assets/slopeblur01.gif)

![](../../../../../../assets/slopeblur02.gif)

</td>
</tr>
</table>
