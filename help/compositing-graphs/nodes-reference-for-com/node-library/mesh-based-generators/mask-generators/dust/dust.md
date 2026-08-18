---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dust.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---


# 塵埃

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dust.png){width="128px"}

## 塵埃

**收錄於：***基於網格的生成器**/遮罩生成器*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此遮罩代表積聚在遮蔽、低矮區域的塵埃，以及僅在朝上方的區域。 需要正確的 AO 和世界空間法線才能運作。

## 參數

### 輸入

* **環境遮蔽**： *灰階輸入*\
  用於塵埃擺放的烘焙地圖。 必備！
* **世界空間法線**： *色彩輸入*\
  用於塵埃擺放的烘焙地圖。 必備！
* **雜訊**： *灰階輸入*\
  自訂塵埃貼圖（可選），僅在覆蓋噪音設定為 True 時才會出現。
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

### 參數

* **等級**： *0.0 - 1.0*\
  設定總塵埃量。
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整灰塵的對比度。
* **遮蔽量**： *0.0 - 1.0* AO影響;阻塞區域會出現更多灰塵。
* **雜訊不透明度**： *0.0 - 1.0*&#x200B;設定灰塵區域可見的雜訊量。
* **覆蓋噪音**： *False/True*&#x200B;設定以使用自訂塵埃貼圖輸入。

## 範例圖片

![](../../../../../../assets/dust-ex.gif)

</td>
</tr>
</table>
