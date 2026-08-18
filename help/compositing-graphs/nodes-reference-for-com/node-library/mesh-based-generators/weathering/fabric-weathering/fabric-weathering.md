---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/fabric-weathering.html"
breadcrumb-title: ''
description: 使用布料老化節點，根據網格幾何形狀和曲率為布料材料添加磨損與老化效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Fabric Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 布料風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---


# 布料風化

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fabric-weathering.png){width="128px"}

## 布料風化

**收錄於：***網狀發電機**/風化*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

這是一種全材質效果，能同時在多個聲道上運作。 它增加了隨機的布料磨損效果，並能控制年代和髒污度。\
除非你有正確烘焙的 AO 和 World Space Normalmaps，否則這個效果效果不佳，因為這需要這些來充分計算和產生所有東西。

使用完整素材時，務必充分理解 [連結創建模式](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) 。

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
  * **使用**&#x200B;量： *0.0 - 1.0*&#x200B;根據AO在非常深色的積垢痕跡中融合。 最大值和最小值通常非常極端，請謹慎使用。
  * **年齡**： *0.0 - 1.0*&#x200B;整體瓷磚磨損模式。 下方的限制控制AO的影響。 最大值和最小值通常非常極端。
  * **年齡 Threshlod**： *0.0 - 1.0*&#x200B;設定 AO 對年齡參數的影響程度。
  * **年齡摺痕**： *0.0 - 1.0*&#x200B;控制細微額外摺痕的混合效果。
  * **銳利邊緣刮痕比例**： *1.0 - 32.0*&#x200B;設定小刮痕的刻度，主要刮除使用過的痕跡和老化效果。
  * **銳利邊緣刮痕 經線強度**： *0.0 - 1.0*&#x200B;設定上述小刮痕的經線強度。
  * **舊布料去飽和度**： *0.0 - 1.0*&#x200B;控制老化效應的去飽和度。
  * **舊布料亮度**： *0.0 - 1.0*&#x200B;控制老化效果的亮度。 *這是個非常重要的參數，必須調整才能達到你喜歡的外觀，但效果可能非常極端：請搭配細微的調整。*
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

![](../../../../../../assets/fabric-ex.gif)

</td>
</tr>
</table>
