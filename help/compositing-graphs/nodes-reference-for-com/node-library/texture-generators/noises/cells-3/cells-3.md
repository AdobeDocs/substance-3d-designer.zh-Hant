---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-3.html"
breadcrumb-title: ''
description: 利用 Cells 3 節點產生中間細胞模式，創造有機與生物質地效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 細胞 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---


# 細胞 3

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![格子 3 - 圖示](../../../../../../assets/cells_3.png "格子 3 - 圖示"){width="200px"}

<b>收錄於：</b> 貼圖產生器>噪音

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

是細胞壁噪音的變體<b></b>。

椎間盤的交會產生細胞壁薄且柔軟度不平整。

另見： [單元1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md)、 [單元2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md)、 [單元4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| <b>硬度</b>  浮子 | 細胞壁的定義，值越高，壁面越清晰、清晰。 |
| <b>反布</b>  林 | 將影像輸出的灰階值反轉。 |
| <b>混亂</b>  漂浮 | 取代噪音的成分。    這可以用來動畫噪音。 |
| <b>無序速度</b>  浮動 | 調整由 <b>無序</b> 參數所施加的位移距離。    這可用於控制噪聲動畫時的位移速度。 |
| <b>無序各向異性</b>  浮子 | 控制無序</b>參數所施加<b>的位移方向範圍，值越高，方向越窄且更明確。方向由 <b>無序各向異性角度</b> 參數控制。 |
| <b>無序各向異性角</b>  浮點 | 控制無序</b>參數所施加<b>的位移方向，當「無序各向異性」參數非零時。 |
| <b>圖案尺寸</b>  Float2 | 一個乘子，表示散佈圓盤在其胞內的大小，其中 1.0 是整個胞子的跨度。 |
| <b>圖案比例</b>  浮球 | 模式大小</b>的乘數<b>，其中 1.0 是完整大小。 |
| <b>角度</b>  浮球 | 用來設定圓盤方向的角度，以旋轉數計算，且從水平向右開始。 |
| <b>角度隨機</b>  浮動 | 隨機變化的最大幅度應用於 <b>角度</b> 值，以匝數計。 |
| <b>Tile offset</b>  Float2 | 控制用於渲染噪音的無限平面部分的位置。 |
| <b>非平方展開</b>  布林 | 在非正方形影像中，保持產生的磁磚方正，並將雜訊產生擴展到影像的範圍。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![格子 3 - 範例 1](../../../../../../assets/cells_3_1.png "格子 3 - 範例 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![單元 3 - 範例 2](../../../../../../assets/noise_cells_3_v2_speed0.6_aniso0.gif "單元格 3 - 範例 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![格子 3 - 範例 3](../../../../../../assets/noise_cells_3_v2_speed0.6_aniso1.gif "格子 - 範例 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![格子 3 - 範例 4](../../../../../../assets/noise_cells_3_v2_speed0.3_aniso0.6.gif "格子 3 - 範例 4"){zoomable="yes"}

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
