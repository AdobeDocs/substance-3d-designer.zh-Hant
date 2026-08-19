---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-damages.html"
breadcrumb-title: ''
description: 使用邊緣損傷節點在網格邊緣產生傷害遮罩，創造逼真的邊緣磨損與斷裂效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Damages
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 邊緣損害
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 1%

---


# 邊緣損害

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-damages.png){width="128px"}

## 邊緣損害

**收錄於：***基於網格的生成器**/遮罩生成器*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

這個遮罩代表根據曲率和烘焙AO對凸起邊緣造成的損害。

## 參數

### 輸入

* **曲率**： *灰階輸入*\
  用於效果放置的烘焙地圖。 必備！
* **環境遮蔽**： *灰階輸入*\
  用於效果放置的烘焙地圖。 必備！
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

### 參數

* **等級**： *0.0 - 1.0*\
  要施加的邊緣傷害量。
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整結果的對比度。
* **傷害強度**： *0.0 - 1.0*&#x200B;在剝落且穩定的外觀與混亂、刮痕嚴重損壞的外觀之間切換。

## 範例圖片

![](../../../../../../assets/edge-damages-ex.gif)

</td>
</tr>
</table>
