---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/water-level.html"
breadcrumb-title: ''
description: 利用水位節點根據水位高度混合材質，創造逼真的水面效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Water Level
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 水位
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 1%

---


# 水位

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/water-level.png){width="128px"}

## 水位

**收錄於：***材質濾鏡/效果*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

一體化效果，會為完整材質輸入增加水位。 輸入材質必須有良好且高品質的高度圖，效果才會有效。 結果是 PBR 正確。

## 參數

### 輸入

* **遮罩**： *灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

### 參數

* **頻道**\
  在這個群組中切換材質通道，例如使用鏡面/光澤貼圖而非金屬/粗糙度時。
* **水位：***0.0 - 1.0*&#x200B;主要控制用來升降水位。
* **水面黑暗度**： *0.0 - 1.0*&#x200B;設定水面的一般「透明度」。
* **邊緣濕度**： *0.0 - 1.0*&#x200B;決定水邊應有多少濕潤感。
* **邊緣濕度距離**： *0.0 - 1.0*&#x200B;設定濕邊的長度。
* **深度模糊量**： *0.0 - 1.0*&#x200B;根據水下深度設定模糊程度。 修改模糊半徑。
* **深度模糊不透明度**： *0.0 - 1.0*&#x200B;決定深度模糊的混合程度，可用來降低模糊效果。
* **污泥顏色**：*（色彩值）*設定污泥效果的顏色。
* **污泥深度**： *0.0 - 1.0*&#x200B;設定污泥開始出現的水深，相對於水位。
* **污泥不透明度**： *0.0 - 1.0*&#x200B;設定污泥效應的全域不透明度。
* ****&#x200B;霜凍：*0.0 - 1.0*&#x200B;設定霜凍量。從外緣開始出現，並向內移動。
* **霜強度**： *0.0 - 1.0*&#x200B;設定霜凍強度，控制效果的「不透明度」。
* **霜裂：***0.0 - 1.0*&#x200B;設定從凍結到液態過渡的裂縫數量。
* **Frost Normal 格式：*DirectX/OpenGL*切換 Frost Normalmap 效果綠色**&#x200B;通道。

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
