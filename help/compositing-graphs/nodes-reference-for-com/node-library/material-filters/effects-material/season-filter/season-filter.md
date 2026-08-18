---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/season-filter.html"
breadcrumb-title: ''
description: 使用季節過濾節點對材料套用季節效果，創造春、夏、秋、冬季變化。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Season Filter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 季節濾鏡
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---


# 季節濾鏡

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/default-icon.png){width="128px"}

## 季節濾鏡

**收錄於：***材質濾鏡/效果*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

這個節點會加入像是動畫水面關卡、雪、冰和/或苔蘚等效果。

請記住，這是較舊的濾網，並非設計成完全符合PBR標準。 它主要是為了保留舊有或相容性，雖然在某些情況下仍然有用。 較新的PBR正確版本可在《雪覆蓋[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md)》和[《水位》](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md)中找到。

節點需要一套適當的材質輸入，主要是需要相當詳細的高度圖或法線貼圖。

## 參數

### 輸入

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
  * **光強**： *0.0 - 1.0*\
    （假）光的強度。
  * **光角**： *0.0 - 1.0*\
    （假）光的入射角
* **影響**
  * **從高度或法線**&#x200B;的效果： *高度、法線*&#x200B;選擇哪個輸入映射來驅動效果。
  * **水位**： *0.0 - 1.0*&#x200B;根據高度/法線資訊升降水位。
  * **水面細節**： *0.0 - 1.0*&#x200B;設定水中細節量。
  * **折射：***0.0 - 1.0*&#x200B;設定效果中假折射的程度。
  * **反射**： *0.0 - 1.0*&#x200B;設定效果中假反射的數量。
  * **反射距離**： *0.0 - 1.0*&#x200B;控制反射視覺效果。
  * **反射角度**： *0.0 - 1.0*&#x200B;控制反射視覺效果。
  * **流程方向**： *0.0 - 1.0*&#x200B;控制動畫流程（使用 Substance Player 進行視覺化）。
  * **冰：***0.0 - 1.0*&#x200B;設定水的結冰程度。
  * **冰面細節**： *0.0 - 1.0*&#x200B;設定冰面細節量。
  * **降雪**&#x200B;量： *0.0 - 1.0*&#x200B;設定積雪覆蓋量。
  * **苔蘚**： *0.0 - 1.0*&#x200B;設定苔蘚覆蓋範圍。
  * **苔蘚比例**： *1 - 4*&#x200B;組生成苔蘚貼圖的比例。
  * **苔蘚顏色**：*（顏色值）*設定苔蘚的顏色。
  * **水色**：*（顏色值）*設定水的顏色，包括透明度/透明度。
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

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
