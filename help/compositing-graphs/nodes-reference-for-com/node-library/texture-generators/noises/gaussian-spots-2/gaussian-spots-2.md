---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/gaussian-spots-2.html"
breadcrumb-title: ''
description: 使用 Gaussian Spots 2 節點來產生進階的高斯點圖案，以創造有機的紋理變化。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Gaussian spots 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 高斯斑點 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 3c2ada78db14be2b9c3380eff9b307aec11d40dc
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 1%

---


# 高斯斑點 2

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![高斯斑點 2 - 圖標](../../../../../../assets/gaussian_spots_2.png "高斯斑點 2 - 圖標"){width="200px"}

<b>收錄於：</b> 貼圖產生器>噪音

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

光滑高斯探測</b>噪聲的變體<b>。\
基於 [高斯雜訊](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md) 節點，梯度較窄且頻率較高。

另見： [高斯斑點1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-spots-1/gaussian-spots-1.md)

</td>
</tr>
</table>

## 輸出

|  |  |
| --- | --- |
| <b>產出</b> *灰階* | 產生的雜訊以灰階位圖形式呈現。 |

## 參數

|  |  |
| --- | --- |
| <b>尺度</b>  整數 | 用來產生噪音磚塊的網格細分。    數值越高，抽到的方塊越多，噪音也越密集。 |
| <b>混亂</b>  漂浮 | 取代噪音的成分。    這可以用來動畫噪音。 |
| <b>無序速度</b>  浮動 | 調整由 <b>無序</b> 參數所施加的位移距離。    這可用於控制噪聲動畫時的位移速度。 |
| <b>無序各向異性</b>  浮子 | 控制無序</b>參數所施加<b>的位移方向範圍，值越高，方向越窄且更明確。方向由 <b>無序各向異性角度</b> 參數控制。 |
| <b>無序各向異性角</b>  浮點 | 控制無序</b>參數施加位移<b>的方向，當<b>無序各向</b>異性參數非零時。 |
| <b>Tile offset</b>  Float2 | 控制用於渲染噪音的無限平面部分的位置。 |
| <b>非平方展開</b>  布林 | 在非正方形影像中，保持產生的磁磚方正，並將雜訊產生擴展到影像的範圍。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![高斯斑點 2 - 範例 1](../../../../../../assets/gaussian_spots_2_1.png "高斯斑點 2 - 範例 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![高斯斑點 2 - 範例 2](../../../../../../assets/noise_gaussian_spots_2_v2_speed0.6_aniso0.gif "高斯斑點 2 - 範例 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![高斯斑點2 - 範例3](../../../../../../assets/noise_gaussian_spots_2_v2_speed0.6_aniso1.gif "高斯斑點2 - 範例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![高斯斑點2 - 範例4](../../../../../../assets/noise_gaussian_spots_2_v2_speed0.3_aniso0.6.gif "高斯斑點2 - 範例4"){zoomable="yes"}

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
