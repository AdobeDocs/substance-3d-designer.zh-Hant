---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-1.html"
breadcrumb-title: ''
description: 利用 Cells 1 節點產生基本的細胞圖案，創造有機與生物紋理效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 細胞1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---


# 細胞1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![格子 1 - 圖示](../../../../../../assets/cells_1.png "格子 1 - 圖示"){width="200px"}

<b>收錄於：</b> 貼圖產生器>噪音

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

是細胞壁噪音的變體<b></b>。

使用者選擇的圖案會透過 Max 混合模式分散並疊加。

另見： [細胞2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md)、 [細胞3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md)、 [細胞4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| <b>無序各向異性角</b>  浮點 | 控制無序</b>參數所施加<b>的位移方向，當「無序各向異性」參數非零時。 |
| <b>整數模式</b> | 基底形狀在生成的影像中散落。 |
| <b>圖案尺寸</b>  Float2 | 一個乘子，表示其胞內散佈圖案大小，其中 1.0 是整個胞子的跨度。 |
| <b>圖案比例</b>  浮球 | 模式大小</b>的乘數<b>，其中 1.0 是完整大小。 |
| <b>亮度隨機</b>  浮點 | 亮度範圍是隨機從格子中減去的，其中1是整個範圍。 |
| <b>角度</b>  浮球 | 用來設定格子方向的角度，以轉彎數及從水平向右開始計算。 |
| <b>角度隨機</b>  浮動 | 隨機變化的最大幅度應用於 <b>角度</b> 值，以匝數計。 |
| <b>Tile offset</b>  Float2 | 控制用於渲染噪音的無限平面部分的位置。 |
| <b>非平方展開</b>  布林 | 在非正方形影像中，保持產生的磁磚方正，並將雜訊產生擴展到影像的範圍。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![格子 1 - 範例 1](../../../../../../assets/cells_1_1.png "格子 - 範例 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![格子 1 - 範例 2](../../../../../../assets/noise_cells_1_v2_speed0.3_aniso0.3.gif "格子 1 - 範例 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![格子 1 - 範例 3](../../../../../../assets/noise_cells_1_v2_speed0.5_aniso0.6.gif "格子 1 - 範例 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![格子 1 - 範例 4](../../../../../../assets/noise_cells_1_v2_speed0.3_aniso0.6.gif "格子 1 - 範例 4"){zoomable="yes"}

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
