---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/perlin-noise.html"
breadcrumb-title: ''
description: 使用 Perlin Noise 節點生成流暢自然的噪音模式，創造有機的質感與變化。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Perlin noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Perlin 噪聲
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---


# Perlin 噪聲

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Perlin 噪音 - 圖示](perlin-noise.resources/perlin_noise.png "Perlin 噪音 - Icon"){width="200px"}

<b>收錄於：</b> 貼圖產生器>噪音

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

產生Perlin雜訊，這是一種廣泛使用的灰階平滑分布。

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
| <b>磁磚偏移</b> <i>Float2</i> | 控制用於渲染噪音的無限平面部分的位置。 |
| <b>非平方展開</b> <i>布林值</i> | 在非正方形影像中，保持產生的磁磚方正，並將雜訊產生擴展到影像的範圍。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Perlin 雜訊 - 範例 1](perlin-noise.resources/perlin_noise_1.png "Perlin 雜訊 - 範例 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Perlin 雜訊 - 範例 2](perlin-noise.resources/noise_perlin_noise_v2_speed0.6_aniso0.gif "Perlin 雜訊 - 範例 2"){zoomable="yes"}

</td>
</tr>
</table>
