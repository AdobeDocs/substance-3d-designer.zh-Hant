---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dirt.html"
breadcrumb-title: ''
description: 使用 Dirt 節點根據網格曲率、位置和遮蔽產生 dirt 累積遮罩。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 汙垢
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 2%

---


# 汙垢

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dirt.png){width="128px"}

## 汙垢

**收錄於：***基於網格的生成器**/遮罩生成器*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此遮罩代表遮蔽與凹陷邊緣與角落的泥土，基於烘焙的 AO 與曲率。

## 參數

### 輸入

* **曲率**： *灰階輸入*\
  烘焙貼圖用於內部效果和遮罩。 必備！
* **環境遮蔽**： *灰階輸入*\
  烘焙貼圖用於內部效果和遮罩。 必備！
* **垃圾搖滾輸入**： *灰階輸入*\
  自訂 grunge 地圖輸入，可選，並由參數啟用。
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。
* **世界空間法線**： *色彩輸入*\
  只用於三平面。
* **位置**： *顏色輸入*\
  只用於三平面。

### 參數

* **泥土等級**： *0.0 - 1.0*&#x200B;主要控制泥土量。
* **泥土對比**&#x200B;度： *0.0 - 1.0*&#x200B;控制遮罩內泥土的主要對比度。
* **垃圾搖滾量**： *0.0 - 1.0*&#x200B;設定泥土的粗糙程度。 設定為 0，讓土壤變得非常光滑。
* **邊緣遮罩**： *0.0 - 1.0*&#x200B;根據曲率貼圖，需去除凸起邊緣的髒土量。
* **使用自訂 Grunge**： *False/True*&#x200B;啟用自訂 grunge 地圖輸入，取代內建 Grunge。
* **垃圾搖滾等級**： *1 - 16*&#x200B;組 垃圾搖滾細節的平鋪等級。
* **使用三平面**&#x200B;投影：*假/真 使用[*&#x200B;三平面投影](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md)來做垃圾搖滾地圖，去除接縫。
* **三平面融合對比**&#x200B;度： *0.001 - 1.0*&#x200B;三平面投影的對比度。

## 範例圖片

![](../../../../../../assets/dirt-ex.gif)

</td>
</tr>
</table>
