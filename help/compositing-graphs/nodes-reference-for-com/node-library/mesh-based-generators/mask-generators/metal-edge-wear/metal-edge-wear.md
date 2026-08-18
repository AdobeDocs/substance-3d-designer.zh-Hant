---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/metal-edge-wear.html"
breadcrumb-title: ''
description: 使用金屬邊緣磨損節點，根據網格曲率和位置生成金屬邊緣的磨損遮罩。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Metal Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 金屬邊緣磨損
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# 金屬邊緣磨損

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/metal-edge-wear.png){width="128px"}

## 金屬邊緣磨損

**收錄於：***基於網格的生成器**/遮罩生成器*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

這個遮罩代表金屬物件的邊緣磨損，凸起邊緣會出現刮痕和缺口，可能被烘焙的 AO 暗區遮蓋。

## 參數

### 輸入

* **曲率**： *灰階輸入*\
  烘焙貼圖用於內部效果和遮罩。
* **環境遮蔽**： *灰階輸入*\
  烘焙貼圖用於內部效果和遮罩。
* **垃圾搖滾輸入**： *灰階輸入*
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。
* **世界空間法線**： *色彩輸入*
* **位置**： *顏色輸入*

### 參數

* **磨損等級**： *0.0 - 1.0*&#x200B;設定總磨損程度，逐漸揭示。
* **磨損對比**&#x200B;度： *0.0 - 1.0*&#x200B;設定最終效果的對比度。
* **邊緣平滑度**： *0.0 - 16.0*&#x200B;設定曲率邊緣衰減的平滑度。
* **垃圾搖滾量**： *0.0 - 1.0*&#x200B;設定多少垃圾搖滾元素，讓它們在邊緣間融合。
* **垃圾搖滾等級**： *1 - 16*&#x200B;設定了垃圾搖滾的等級。
* **環境遮蔽遮罩**： *0.0 - 1.0*&#x200B;設定 AO 對最終效果的影響程度，暗區被遮蔽。
* **曲率權重**： *0.0 - 1.0*&#x200B;設定曲率凸邊對最終效果的影響。
* **使用自訂 Grunge：*False/True*啟用自訂 Grunge** 地圖輸入欄位。
* **使用三平面**： *假/真*&#x200B;啟用 [三平面](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) 投影來隱藏接縫。
* **三平面混合對比**&#x200B;度： *0.0 - 1.0*&#x200B;三平面投影的混合對比度設定。

## 範例圖片

![](../../../../../../assets/metal-edge-wear-ex.gif)

</td>
</tr>
</table>
