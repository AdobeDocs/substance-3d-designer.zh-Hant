---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dripping-rust.html"
breadcrumb-title: ''
description: 使用 Dripping Rust 節點根據網格幾何和重力方向生成 Rust 滴落模式。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dripping Rust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 滴落的鏽蝕
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---


# 滴落的鏽蝕

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dripping-rust.png){width="128px"}

## 滴落的鏽蝕

**收錄於：***基於網格的生成器**/遮罩生成器*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

這個面罩代表鏽蝕片和斑點，漏水沿著下方延伸。

## 參數

### 輸入

* **曲率**： *灰階輸入*\
  烘焙或生成的地圖來幫助放置生鏽。
* **環境遮蔽**： *灰階輸入*\
  烘焙或生成的地圖來幫助放置生鏽。
* **位置**： *灰階輸入*\
  用於滴水導向的烘焙或生成地圖。
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

### 參數

* **鏽蝕擴散**： *0.0 - 1.0*&#x200B;主要控制生鏽量。
* **鏽蝕對比**&#x200B;度： *0.0 - 1.0*&#x200B;設定產生鏽斑的對比度（不影響滴落）。
* **擴散平滑度**： *0.0 - 1.0*&#x200B;對鏽斑施加模糊/暈染效果。
* **滴滴強度**： *0.0 - 1.0*&#x200B;設定滴滴的強度與長度。
* **滴落的平滑度**： *0.0 - 1.0*&#x200B;滴落時需要進行模糊與平滑處理。
* **滴落取樣量**： *0 - 32*&#x200B;滴落效果的品質等級（步驟）。 會稍微影響速度。

## 範例圖片

![](../../../../../../assets/dripping-rust-ex3.gif)

</td>
</tr>
</table>
