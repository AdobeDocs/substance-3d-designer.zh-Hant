---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/cracks-weathering.html"
breadcrumb-title: ''
description: 使用裂縫風化節點，根據網格曲率和應力點為材料添加裂紋圖案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Cracks Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 裂縫風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 1%

---


# 裂縫風化

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/cracks-weathering.png){width="128px"}

## 裂縫風化

**收錄於：***網狀發電機**/風化*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

這是一種全材質效果，能同時在多個聲道上運作。 它增加了隨機裂紋模式，並可控制裂紋的擴散與深度。

使用完整素材時，務必正確理解 [連結建立模式](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) 。

## 參數

### 輸入

* **曲率**： *灰階輸入*\
  烘焙或生成的貼圖用於內部特效和遮罩。
* **高度** ： *灰階輸入*\
  烘焙或生成的貼圖用於內部特效和遮罩。
* **遮罩** ： *灰階輸入*\
  遮罩槽用於遮蔽節點的效果。 可以用「遮罩」參數切換。

### 參數

* **頻道**
  * 在這個群組中切換材質通道，例如使用鏡面/光澤貼圖而非金屬/粗糙度時。
* **進階**
  * **一般格式**： *DirectX、OpenGL*\
    切換不同的法線貼圖格式（反轉綠色通道）。
  * **面具**： *虛假/真實*\
    切換面具地圖的使用開關。
* **影響**
  * **裂縫擴展**： *0.0 - 1.0*&#x200B;裂縫應該擴散的範圍。 這是這個效果的主要控制。
  * **裂縫深度**： *0.0 - 1.0*&#x200B;裂縫效應的深度。 這主要影響高度，並略微影響視角厚度。
* **混合**
  * 控制效果與每個聲道融合的強度。

## 範例圖片

![](../../../../../../assets/cracks-ex.gif)

</td>
</tr>
</table>
