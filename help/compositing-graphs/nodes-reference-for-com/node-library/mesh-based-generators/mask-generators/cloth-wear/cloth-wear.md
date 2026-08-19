---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/cloth-wear.html"
breadcrumb-title: ''
description: 使用 Cloth Wear 節點根據網格曲率和接觸面積在布料表面生成磨損遮罩。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Cloth Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 布料穿著
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 1%

---


# 布料穿著

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/cloth-wear.png){width="128px"}

## 布料穿著

**收錄於：***基於網格的生成器**/遮罩生成器*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

面具象徵布料上磨損的邊緣。 它使用布料細節高度圖來決定大部分視覺效果;沒有適當的地圖，效果看起來非常簡單。

## 參數

### 輸入

* **布料高度**： *灰階輸入*\
  只有布料圖案的高度。 這不是你（烘焙）物件的高度，而是平鋪細節圖案。
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。
* **曲率**： *灰階輸入*\
  烘焙/產生曲率來決定凸起的邊緣。

### 參數

* **硬邊量**： *0.0 - 1.0*
* **磨損柔軟度**： *0.0 - 5.0*&#x200B;決定磨損邊緣的模糊程度與柔軟度。

## 範例圖片

![](../../../../../../assets/cloth-wear-ex.gif)

</td>
</tr>
</table>
