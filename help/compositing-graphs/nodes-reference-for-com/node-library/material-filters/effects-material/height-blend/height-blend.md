---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/height-blend.html"
breadcrumb-title: ''
description: 使用 Height Blend 節點根據高度貼圖來混合材質，創造逼真的材質過渡。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 高度混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---


# 高度混合

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-blend.png){width="128px"}

## 高度混合

**收錄於：***材質濾鏡/效果*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

根據高度資訊組合兩個高度圖。 會產生混合的高度圖，也會產生一個黑白遮罩，可用於其他地方。

這在你有兩個高品質高度貼圖要合併時很有用，但不一定是完整材質，因為材質高度混合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/material-height-blend/material-height-blend.md)是必要的[。

## 參數

### 輸入

* **高度 頂**&#x200B;端： *灰階輸入*
* **高度 底部**： *灰階輸入*
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

### 參數

* **高度偏移**： *0.0 - 1.0*&#x200B;偏移高度貼圖，使混合層級沿高度軸移動。 這是混合的主要控制。
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整混合的對比度，讓轉場更銳利。
* **模式**： *平衡高度，底部高度優先，*&#x200B;可在兩種不同混合模式間切換。
* **不透明度**： *0.0 - 1.0*\
  混合前景高度的不透明度，讓它淡入或淡出。

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
