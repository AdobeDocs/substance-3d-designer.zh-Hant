---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/surface-brush.html"
breadcrumb-title: ''
description: 使用 Surface Brush 節點根據表面方向產生遮罩，以創造方向性的風化與磨損效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Surface Brush
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 表面刷
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---


# 表面刷

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/surface-brush.png){width="128px"}

## 表面刷

**收錄於：***基於網格的生成器**/遮罩生成器*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此遮罩代表了金屬刷洗在物體表面上的有趣效果，且物體幾何形狀與 AO 遮蔽。

## 參數

### 輸入

* **世界空間法線**： *色彩輸入*
* **曲率**： *灰階輸入*\
  烘焙貼圖用於內部效果和遮罩。
* **環境遮蔽**： *灰階輸入*\
  烘焙貼圖用於內部效果和遮罩。
* **位置**： *灰階輸入*
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

### 參數

* **等級**： *0.0 - 1.0*\
  設定全局效果等級，逐步揭示。
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整結果的對比度。
* **刮痕長度**： *0.0 - 8.0*&#x200B;設定刮痕長度。 較小的數值像點狀，較高的數值則是長連續。
* **遮擋軸**： *X、Y、Z、無*&#x200B;應該被刮傷的物體軸。 不會改變刮痕的方向。
* **遮擋軸強度**： *0.0 - 1.0*&#x200B;軸閉塞效應的強度。
* **閉合***：0.0 - 1.0* AO在閉塞刮痕上的強度。
* **銳利度**： *0.0 - 1.0*&#x200B;設定銳化後對刮痕施加的量。

## 範例圖片

![](../../../../../../assets/surface-brush-ex.gif)

</td>
</tr>
</table>
