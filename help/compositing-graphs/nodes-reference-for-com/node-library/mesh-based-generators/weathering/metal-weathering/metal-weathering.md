---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/metal-weathering.html"
breadcrumb-title: ''
description: 利用金屬風化節點，根據網格幾何體為金屬材料添加逼真的生鏽和腐蝕效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Metal Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 金屬風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 1%

---


# 金屬風化

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/metal-weathering.png){width="128px"}

## 金屬風化

**收錄於：***網狀發電機**/風化*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

## 參數

### 輸入

* **一般 WS：***色彩輸入*\
  烘焙世界空間法線貼圖用於內部效果與遮罩。
* **環境遮蔽**： *灰階輸入*\
  烘焙貼圖用於內部效果和遮罩。
* **遮罩** ： *灰階輸入*\
  遮罩槽用於遮蔽節點的效果。 可以用「遮罩」參數切換。

### 參數

* **頻道**
  * 在這個群組中切換材質通道，例如使用鏡面/光澤貼圖而非金屬/粗糙度時。
* **進階**
  * **一般格式**： *Direct X，Open GL*\
    切換不同的法線貼圖格式（反轉綠色通道）。
  * **面具**： *虛假/真實*\
    切換面具地圖的使用開關。
* **影響**
  * **塵埃**： *0.0 - 1.0*
  * **髒污度**： *0.0 - 1.0*
  * **邊緣磨損**： *0.0 - 1.0*
  * **油漆剝落**： *0.0 - 1.0*
  * **鏽蝕**： *0.0 - 1.0*
  * **鏽蝕剝落**： *0.0 - 1.0*
  * **銹綠**： *銹，綠*
  * **油漆裂縫等級**： *1.0 - 16.0*
  * **油漆裂縫 變形強度**： *0.0 - 1.0*
  * **銳利邊緣刮痕***：1.0 - 32.0*
  * **銳利邊緣 刮痕 變形強度**： *0.0 - 1.0*
  * **原金屬顏色**： *（顏色值）*
  * **原金屬鏡面色彩**： *（色彩值）*
  * **原金屬光澤度值**： *（灰階值）*
  * **原金屬粗糙度值**： *（灰階值）*
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
  * **金屬強度**： *0.0 - 1.0*\
    融合金屬的強度。
  * **環境遮蔽強度**： *0.0 - 1.0*\
    融合環境遮蔽的強度。
  * **身高強度**： *0.0 - 1.0*\
    融合高度強度。

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
