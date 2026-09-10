---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-base.html"
breadcrumb-title: ''
description: 使用 Fractal Sum Base 節點來產生基底分形噪音模式，以創造複雜的有機紋理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum base
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 分形和基底
user-guide-description: ''
user-guide-title: ''
source-git-commit: a2d6381b9bf224008fa412ef70c9b63b9b2756e8
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---


# 分形和基底

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![分形和基底 - 圖示](fractal-sum-base.resources/fractal_sum_base.png "分形和基底 - 圖示"){width="200px"}

<b>收錄於：</b> 貼圖產生器>噪音

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一種可自訂的分形噪音，具備可調整的音域與八度平衡。

<b>分形和</b>的噪音家族皆基於此節點。

另見： [分形和1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-1/fractal-sum-1.md)、 [分形和2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-2/fractal-sum-2.md)、 [分形和3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-3/fractal-sum-3.md)、 [分形和4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-4/fractal-sum-4.md)

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
| <b>粗糙度</b> <i>浮標</i> | 噪音八度的平衡。    較高的數值會讓高頻八度更明顯。 |
| <b>敏。 關卡</b> <i>整數</i> | 噪音中使用的最低八度。    值越高，噪聲頻率越高。 |
| <b>Max。 關卡</b> <i>整數</i> | 噪音中使用的最大八度。    值越高，噪聲頻率越高。 |
| <b>混亂</b> <i>浮標</i> | 取代噪音的成分。    這可以用來動畫噪音。 |
| <b>無序速度</b> <i>浮標</i> | 調整由 <b>無序</b> 參數所施加的位移距離。    這可用於控制噪聲動畫時的位移速度。 |
| <b>對比</b> <i>浮標</i> | 最終結果的對比。 |
| <b>全域不透明度</b> <i>浮標</i> | 噪音八度的不透明度會累積成最終結果。    高值可能導致部分區域被燒成白色。 |
| <b>非平方展開</b> <i>布林值</i> | 在非正方形影像中，保持產生的磁磚方正，並將雜訊產生擴展到影像的範圍。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![分形和基底 - 範例 1](fractal-sum-base.resources/fractal_sum_base_1.png "分形和基底 - 範例 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![分形和基底 - 範例 2](fractal-sum-base.resources/noise_fractal_sum_base_v2_speed0.6_aniso0.gif "分形和基底 - 範例 2"){zoomable="yes"}

</td>
</tr>
</table>
