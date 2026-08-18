---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/rock-weathering.html"
breadcrumb-title: ''
description: 使用岩石風化節點，根據網格幾何在岩石表面產生風化圖案，以呈現逼真的侵蝕效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Rock Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 岩石風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---


# 岩石風化

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/rock-weathering.png){width="128px"}

## 岩石風化

**收錄於：***網狀發電機**/風化*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

## 參數

### 輸入

* **環境遮蔽**： *灰階輸入*\
  烘焙貼圖用於內部效果和遮罩。
* **曲率**： *灰階輸入*\
  烘焙貼圖用於內部效果和遮罩。
* **一般 WS：***色彩輸入*\
  烘焙世界空間法線貼圖用於內部效果與遮罩。
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
  * **塵埃**： *0.0 - 1.0*
  * **髒污度**： *0.0 - 1.0*
  * **邊緣磨損**： *0.0 - 1.0*
  * **使用過的石頭**： *0.0 - 1.0*
  * **裂紋等級**： *1.0 - 60.0*
  * **裂紋強度**： *0.0 - 1.0*
  * **年齡**： *0.0 - 1.0*
  * **年齡 Threshlod**： *0.0 - 1.0*
  * **銳利邊緣刮痕***：1.0 - 32.0*
  * **銳利邊緣 刮痕 變形強度**： *0.0 - 1.0*
  * **使用岩石去飽和度**： *0.0 - 1.0*
  * **使用岩石亮度**： *0.0 - 1.0*
* **混合**
  * **擴散強度**： *0.0 - 1.0*\
    擴散劑的混合強度。
  * **基色強度**： *0.0 - 1.0*\
    底色的混合強度。
  * **正常強度**： *0.0 - 64.0*\
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

![](../../../../../../assets/rock-ex.gif)

</td>
</tr>
</table>
