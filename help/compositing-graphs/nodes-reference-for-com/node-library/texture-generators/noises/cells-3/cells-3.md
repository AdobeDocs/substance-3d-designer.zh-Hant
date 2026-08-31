---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-3.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---


# 細胞 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![格子 3 - 圖示](cells-3.resources/cells-3-01.png "格子 3 - 圖示"){width="200px"}

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
| <b>硬度</b> <i>浮標</i> | 細胞壁的定義，值越高，壁面越清晰、清晰。 |
| <b>倒轉</b> <i>布林值</i> | 將影像輸出的灰階值反轉。 |
| <b>混亂</b> <i>浮標</i> | 取代噪音的成分。    這可以用來動畫噪音。 |
| <b>無序速度</b> <i>浮標</i> | 調整由 <b>無序</b> 參數所施加的位移距離。    這可用於控制噪聲動畫時的位移速度。 |
| <b>無序各向異性</b> <i>浮標</i> | 控制無序</b>參數所施加<b>的位移方向範圍，值越高，方向越窄且更明確。方向由 <b>無序各向異性角度</b> 參數控制。 |
| <b>無序各向異性角</b> <i>浮標</i> | 控制無序</b>參數所施加<b>的位移方向，當「無序各向異性」參數非零時。 |
| <b>圖案尺寸</b> <i>Float2</i> | 一個乘子，表示散佈圓盤在其胞內的大小，其中 1.0 是整個胞子的跨度。 |
| <b>圖案尺度</b> <i>浮標</i> | 模式大小</b>的乘數<b>，其中 1.0 是完整大小。 |
| <b>角度</b> <i>浮標</i> | 用來設定圓盤方向的角度，以旋轉數計算，且從水平向右開始。 |
| <b>角度隨機</b> <i>浮標</i> | 隨機變化的最大幅度應用於 <b>角度</b> 值，以匝數計。 |
| <b>磁磚偏移</b> <i>Float2</i> | 控制用於渲染噪音的無限平面部分的位置。 |
| <b>非平方展開</b> <i>布林值</i> | 在非正方形影像中，保持產生的磁磚方正，並將雜訊產生擴展到影像的範圍。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![格子 3 - 範例 1](cells-3.resources/cells-3-02.png "格子 3 - 範例 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![單元 3 - 範例 2](cells-3.resources/cells-3-03.gif "單元格 3 - 範例 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![格子 3 - 範例 3](cells-3.resources/cells-3-04.gif "格子 - 範例 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![格子 3 - 範例 4](cells-3.resources/cells-3-05.gif "格子 3 - 範例 4"){zoomable="yes"}

</td>
</tr>
</table>
