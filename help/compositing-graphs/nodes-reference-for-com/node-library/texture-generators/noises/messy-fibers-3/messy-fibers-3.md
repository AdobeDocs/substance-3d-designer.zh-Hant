---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/messy-fibers-3.html"
breadcrumb-title: ''
description: 使用 Messy Fibers 3 節點生成複雜的纖維圖案，創造布料與紡織質感效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Messy fibers 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 混亂纖維 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 1%

---


# 混亂纖維 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![混亂的纖維 3 - 圖示](../../../../../../assets/messy_fibers_3.png "混亂的纖維 3 - 圖示"){width="200px"}

<b>收錄於：</b> 貼圖產生器>噪音

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

Messy 纖維</b>結構噪音的變體<b>。

另見： [混亂纖維1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-1/messy-fibers-1.md)、 [混亂纖維2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-2/messy-fibers-2.md)

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
| <b>角度</b>  浮球 | 用來設定線的方向角度，以轉數為單位，並從水平向右開始。 |
| <b>角度隨機</b>  浮動 | 隨機變化的最大幅度應用於 <b>角度</b> 值，以匝數計。 |
| <b>亮度隨機</b>  浮點 | 亮度範圍會隨機從螺紋中扣除，其中 1 是完整範圍。 |
| <b>Tile offset</b>  Float2 | 控制用於渲染噪音的無限平面部分的位置。 |
| <b>非平方展開</b>  布林 | 在非正方形影像中，保持產生的磁磚方正，並將雜訊產生擴展到影像的範圍。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![混亂纖維3 - 範例1](../../../../../../assets/messy_fibers_3_1.png "混亂纖維3 - 範例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![混亂纖維3 - 範例2](../../../../../../assets/noise_messy_fibers_3_v2_speed0.1_aniso0.gif "混亂纖維3 - 範例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![雜亂纖維3 - 範例3](../../../../../../assets/noise_messy_fibers_3_v2_speed0.1_aniso1.gif "雜亂纖維3 - 範例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![混亂纖維3 - 範例4](../../../../../../assets/noise_messy_fibers_3_v2_speed0.1_aniso0.6.gif "混亂纖維3 - 範例4"){zoomable="yes"}

</td>
</tr>
</table>
