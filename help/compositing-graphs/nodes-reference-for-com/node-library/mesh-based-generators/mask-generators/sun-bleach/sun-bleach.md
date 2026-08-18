---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/sun-bleach.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# 日曬漂白

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/sun-bleach.png){width="128px"}

## 日曬漂白

**收錄於：***基於網格的生成器**/遮罩生成器*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

這個遮罩類似 [光](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/light/light.md)，但也支援 AO，形成一個代表光線漂白與漸淡的遮罩，疊加在效果之上。

## 輸入

* **正常世界空間**： *色彩輸入*
* **環境遮蔽**： *灰階輸入*\
  烘焙貼圖用於內部效果和遮罩。
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

## 參數

* **等級**： *0.0 - 1.0*\
  設定漂白總量，效果會往下移動。
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整結果的對比度。
* **遮蔽**： *0.0 - 1.0*&#x200B;設定 AO 對最終結果的影響。

## 範例圖片

![](../../../../../../assets/sun-bleach-ex.gif)

</td>
</tr>
</table>
