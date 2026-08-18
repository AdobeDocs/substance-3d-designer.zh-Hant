---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/moss-weathering.html"
breadcrumb-title: ''
description: 使用 Moss Weathering 節點，根據網格曲率和位置為材質添加苔蘚生長模式。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Moss Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 苔蘚風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 1%

---


# 苔蘚風化

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/moss-weathering.png){width="128px"}

## 苔蘚風化

**收錄於：***網狀發電機**/風化*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

這是一種全材質效果，能同時在多個聲道上運作。 它會產生過度生長的苔蘚效應，只有一個控制點來控制繁殖。

這個效果最適合搭配烘焙的世界空間位置貼圖和額外的高度貼圖。 雖然這不是絕對要求，但讓效果的擺放更具說服力。

使用完整素材時，務必正確理解 [連結建立模式](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes) 。

## 參數

### 輸入

* **位置**： *顏色輸入*\
  烘焙世界空間位置。
* **高度** ： *灰階輸入*\
  額外高度圖輸入。
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
  * **苔蘚繁殖**： *0.0 - 1.0*&#x200B;設定苔蘚的擴散範圍。 生長分階段，從輕微覆蓋到厚實、深色的苔蘚。
* **混合**
  * **擴散強度**： *0.0 - 1.0*\
    擴散劑的混合強度。
  * **基色強度**： *0.0 - 1.0*\
    底色的混合強度。
  * **正常強度**： *0.0 - 1.0*\
    融合正常的力量。
  * **鏡面強度**： *0.0 - 1.0*\
    鏡面的融合強度。
  * **光澤度強度**： *0.0 - 1.0*\
    融合光澤的強度。
  * **粗糙度強度**： *0.0 - 1.0*\
    融合粗糙度的強度。
  * **環境遮蔽強度**： *0.0 - 1.0*\
    融合環境遮蔽的強度。
  * **身高強度**： *0.0 - 1.0*\
    融合高度強度。

## 範例圖片

![](../../../../../../assets/moss-ex.gif)

</td>
</tr>
</table>
