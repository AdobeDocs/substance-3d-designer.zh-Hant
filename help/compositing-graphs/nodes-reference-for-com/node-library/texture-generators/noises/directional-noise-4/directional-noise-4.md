---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-noise-4.html"
breadcrumb-title: ''
description: 使用 Directional Noise 4 節點產生具有四個八度的方向性噪音模式，以建立各向異性紋理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional noise 4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 方向性雜訊 4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---


# 方向性雜訊 4

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![方向性噪音 4 - 圖示](directional-noise-4.resources/directional-noise-4-01.png "方向性噪音 4 - 圖示"){width="200px"}

<b>收錄於：</b> 貼圖產生器>噪音

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

是定向噪音</b>的變體<b>。

另見： [方向性雜訊1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-1/directional-noise-1.md)、 [方向性雜訊2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-2/directional-noise-2.md)、 [方向性雜訊3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-3/directional-noise-3.md)

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
| <b>無序各向異性角</b> <i>浮標</i> | 控制無序</b>參數所施加<b>的位移方向，當「無序各向異性」參數非零時。 |
| <b>角度</b> <i>浮標</i> | 用來設定噪音方向的角度，以轉彎次數計算，從水平向右開始。 |
| <b>角度隨機</b> <i>浮標</i> | 隨機變化的最大幅度應用於 <b>角度</b> 值，以匝數計。 |
| <b>磁磚偏移</b> <i>Float2</i> | 控制用於渲染噪音的無限平面部分的位置。 |
| <b>非平方展開</b> <i>布林值</i> | 在非正方形影像中，保持產生的磁磚方正，並將雜訊產生擴展到影像的範圍。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![方向性雜訊 4 - 範例 1](directional-noise-4.resources/directional-noise-4-02.png "方向性雜訊 4 - 範例 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![方向性噪音 4 - 範例 2](directional-noise-4.resources/directional-noise-4-03.gif "方向性噪音 4 - 範例 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![方向性雜訊4 - 範例3](directional-noise-4.resources/directional-noise-4-04.gif "方向性雜訊4 - 範例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![方向性雜訊 4 - 範例 4](directional-noise-4.resources/directional-noise-4-05.gif "方向性雜訊 4 - 範例 4"){zoomable="yes"}

</td>
</tr>
</table>
