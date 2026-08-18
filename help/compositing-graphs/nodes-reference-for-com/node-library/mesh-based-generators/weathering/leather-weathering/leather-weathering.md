---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/leather-weathering.html"
breadcrumb-title: ''
description: 利用皮革老化節點，根據網狀曲線為皮革材料添加磨損模式和老化效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Leather Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 皮革風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---


# 皮革風化

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leather-weathering.png){width="128px"}

## 皮革風化

**收錄於：***網狀發電機**/風化*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

這是一種全材質效果，能同時在多個聲道上運作。 它增加了隨機的皮革磨損效果，並能控制老化和髒污程度。 它與布料風化](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/weathering/fabric-weathering/fabric-weathering.md)類似[，但專為皮革調校。\
除非你插入了正式烘焙的 AO 和世界空間法線貼圖，否則這個效果效果不太好，因為這需要這些來充分計算和產生所有東西。

使用完整素材時，務必充分理解 [連結創建模式](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes) 。

## 參數

### 輸入

* **環境遮蔽**： *灰階輸入*\
  烘焙貼圖用於內部效果和遮罩。
* **一般 Would 空間**： *顏色輸入*
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
  * **塵埃**： *0.0 - 1.0*&#x200B;根據世界空間法線貼圖中面向向上的區域，融合出較暗的塵埃效果。
  * **髒污度**： *0.0 - 1.0*&#x200B;根據 AO 中遮蔽（暗）區域，混合出全域的髒污/污漬效果。
  * **邊緣磨損**： *0.0 - 1.0*&#x200B;根據材質法線為邊緣添加銳利/強化效果。
  * **使用**&#x200B;量： *0.0 - 1.0*&#x200B;融合出全球磨損皮革的風格。
  * **年齡**： *0.0 - 1.0*&#x200B;根據 AO 的摺痕，融合出磨損皮革的外觀。 擺放位置很大程度上受年齡限制影響。
  * **年齡 Threshlod**： *0.0 - 1.0*&#x200B;設定年齡效果的外觀限制。
  * **裂紋等級**： *1.0 - 16.0*&#x200B;設定使用過和年代效果中磨損皮革的深度。
  * **裂縫變形強度**： *0.0 - 1.0*&#x200B;設定使用過與年代效果中磨損皮革的強度。
  * **銳利邊緣刮痕***：1.0 - 32.0*
  * **銳利邊緣 刮痕 變形強度**： *0.0 - 1.0*
  * **二手皮革去飽和**&#x200B;度： *0.0 - 1.0*&#x200B;設定了磨損皮革外觀的飽和度，來自 Age 和 Used 效果。
  * **二手皮革亮度**： *0.0 - 1.0*&#x200B;設定了磨損皮革外觀的亮度，來自 Age 和 Used 效果。
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

![](../../../../../../assets/leather-ex.gif)

![](../../../../../../assets/leather-ex2.png){width="233px"}

</td>
</tr>
</table>
