---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/clouds-1.html"
breadcrumb-title: ''
description: 使用 Clouds 1 節點來產生基本的雲朵圖案，以創造大氣與體積紋理效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Clouds 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 雲 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# 雲 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![雲 1 - 圖示](clouds-1.resources/clouds_1.png "雲 1 - 圖示"){width="200px"}

<b>收錄於：</b> 貼圖產生器>噪音

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這是粗糙 <b>的雲</b> 聲變奏。

另見： [Clouds 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/clouds-2/clouds-2.md)、 [Clouds 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/clouds-3/clouds-3.md)

</td>
</tr>
</table>

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>產出</b> <i>灰階</i> | 產生的雜訊以灰階位圖形式呈現。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>規模</b> <i>整數</i> | 用來產生噪音磚塊的網格細分。    數值越高，抽到的方塊越多，噪音也越密集。 |
| <b>混亂</b> <i>浮標</i> | 取代噪音的成分。    這可以用來動畫噪音。 |
| <b>無序速度</b> <i>浮標</i> | 調整由 <b>無序</b> 參數所施加的位移距離。    這可用於控制噪聲動畫時的位移速度。 |
| <b>無序各向異性</b> <i>浮標</i> | 控制無序</b>參數所施加<b>的位移方向範圍，值越高，方向越窄且更明確。方向由 <b>無序各向異性角度</b> 參數控制。 |
| <b>無序各向異性角</b> <i>浮標</i> | 控制無序</b>參數施加位移<b>的方向，當<b>無序各向</b>異性參數非零時。 |
| <b>磁磚偏移</b> <i>Float2</i> | 控制用於渲染噪音的無限平面部分的位置。 |
| <b>非平方展開</b> <i>布林值</i> | 在非正方形影像中，保持產生的磁磚方正，並將雜訊產生擴展到影像的範圍。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![雲 1 - 範例 1](clouds-1.resources/clouds_1_1.png "雲 1 - 範例 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![雲 1 - 範例 2](clouds-1.resources/noise_clouds_1_v2_speed0.6_aniso0.gif "雲 1 - 範例 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![雲 1 - 範例 3](clouds-1.resources/noise_clouds_1_v2_speed0.6_aniso1.gif "雲 1 - 範例 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![雲 1 - 範例 4](clouds-1.resources/noise_clouds_1_v2_speed0.3_aniso0.6.gif "雲 1 - 範例 4"){zoomable="yes"}

</td>
</tr>
</table>
