---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-4.html"
breadcrumb-title: ''
description: 使用 Cells 4 節點生成進階細胞圖案，創造有機與生物質感效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 細胞4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---


# 細胞4

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![格子 4 - 圖示](cells-4.resources/cells_4.png "格子 4 - 圖示"){width="200px"}

<b>收錄於：</b> 貼圖產生器>噪音

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

是細胞壁噪音的變體<b></b>。

每個儲存格都會被分配一種純色，顏色可以是隨機的，也可以是從輸入影像取樣的。

另見： [細胞1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md)、 [細胞2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md)、 [細胞3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md)

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入</b> <i>灰階</i> |  |

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
| <b>色彩來源</b> <i>整數</i> | 塗在格子上的純色來源：<ul data-preserve-html="true"> <li data-preserve-html="true"><b><i>隨機：</i></b> 使用由節點隨機種子控制的隨機顏色</li> <li data-preserve-html="true"><b><i>偽隨機：</i></b> 使用由獨立使用者設定值做種子的隨機顏色</li> <li data-preserve-html="true"><b><i>影像輸入：</i></b> 使用輸入影像中格子位置取樣的顏色</li> </ul> |
| <b>偽隨機種子</b> <i>整數</i>   *當「色彩來源」設為「偽隨機」時可用* | 允許在節點種子之外分別更改顏色的種子。 |
| <b>非平方展開</b> <i>布林值</i> | 在非正方形影像中，保持產生的磁磚方正，並將雜訊產生擴展到影像的範圍。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![格子 4 - 範例 1](cells-4.resources/cells_4_1.png "格子 4 - 範例 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![格子 4 - 範例 2](cells-4.resources/noise_cells_4_v2_speed0.3_aniso0.6.gif "格子 4 - 範例 2"){zoomable="yes"}

</td>
</tr>
</table>
