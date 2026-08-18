---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/grease.html"
breadcrumb-title: ''
description: 利用 Grease 節點根據網格幾何和接觸面積產生油脂累積遮罩。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Grease
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 油脂
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---


# 油脂

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/grease.png){width="128px"}

## 油脂

**收錄於：***基於網格的生成器**/遮罩生成器*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

這個面具專門用於角色臉部及其他特定區域。 在低厚度區域產生一種皮膚油脂型遮罩。

## 參數

### 輸入

* **厚度**： *灰階輸入*\
  整個效果的基礎是烘焙厚度圖。 必備！
* **雜訊**： *灰階輸入*\
  可選的噪音貼圖可以覆蓋 Grease 的垃圾搖滾。
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

### 參數

* **等級**： *0.0 - 1.0*\
  設定出現的效果總量。
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整結果的對比度。
* **厚度閾值**： *0.0 - 1.0*&#x200B;設定該效應應出現的最小厚度。 和等級一樣重要;調整它以符合你的厚度地圖。
* **覆蓋噪音**： *False/True* Set 用來用自訂輸入槽覆蓋內部油脂泥漿貼圖。

## 範例圖片

![](../../../../../../assets/grease-ex.gif)

</td>
</tr>
</table>
