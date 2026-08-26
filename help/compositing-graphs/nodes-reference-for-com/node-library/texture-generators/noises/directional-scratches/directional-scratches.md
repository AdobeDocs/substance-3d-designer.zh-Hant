---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-scratches.html"
breadcrumb-title: ''
description: 使用方向刮痕節點來創造方向性刮痕圖案，為材質添加磨損和損壞效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional scratches
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 方向刮擦
user-guide-description: ''
user-guide-title: ''
source-git-commit: 3c2ada78db14be2b9c3380eff9b307aec11d40dc
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---


# 方向刮擦

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![方向刮痕 - 圖示](../../../../../../assets/directional_scratches.png "方向刮痕 - 圖示"){width="200px"}

<b>收錄於：</b> 貼圖產生器>噪音

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

隨機散落的刮痕圖案，角度和大小可調整。

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
| <b>角度</b>  浮球 | 角度用來設定刮痕方向，從水平向右開始轉彎數。 |
| <b>角度隨機</b>  浮動 | 隨機變化的最大幅度應用於 <b>角度</b> 值，以匝數計。 |
| <b>模式量</b>  浮動 | 這是散落在刮痕圖案數量上的乘數。 |
| <b>圖案尺寸</b>  Float2 | 抓刮圖的邊界盒大小。    Y 值控制刮痕的最大長度。 |
| <b>圖案大小</b>  隨機 Float2 | 這是針對刮痕隨機降比例的乘數。    Y 值是用來計算刮痕長度的。 |
| <b>Tile offset</b>  Float2 | 控制用於渲染噪音的無限平面部分的位置。 |
| <b>非平方展開</b>  布林 | 在非正方形影像中，保持產生的磁磚方正，並將雜訊產生擴展到影像的範圍。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![方向刮擦 - 範例 1](../../../../../../assets/directional_scratches_1.png "方向刮擦 - 範例 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![方向刮擦 - 範例 2](../../../../../../assets/noise-directional-scratches-speed0.3-aniso0.gif "方向刮擦 - 範例 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![方向刮擦 - 範例 3](../../../../../../assets/noise-directional-scratches-speed0.3-aniso0.6.gif "方向刮擦 - 範例 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![方向刮痕 - 範例 4](../../../../../../assets/noise-directional-scrat-1.gif "方向刮痕 - 範例 4"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![方向性刮擦 - 範例 5](../../../../../../assets/noise-directional-scrat-2.gif "方向性刮擦 - 範例 5"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



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
