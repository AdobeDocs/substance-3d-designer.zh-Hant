---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/white-noise.html"
breadcrumb-title: ''
description: 利用白噪音節點產生白噪音模式，創造材質變化與隨機效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > White noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 白噪音
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8774511f26429071b91a2eeeb8728ac36dc31ed5
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 2%

---


# 白噪音

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![白噪音 - 圖示](../../../../../../assets/white_noise_v2.png "白噪音 - 圖示"){width="200px"}

<b>收錄於：</b> 貼圖產生器>噪音

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

利用三種方法之一產生白噪音，針對不同的直方圖形狀：均勻直方圖、高斯圖與三角圖。

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
| <b>雜訊分布</b> <i>整數</i> | 分配成分以達成直方圖形狀的方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><i>制服：</i> 平面直方圖。</li> <li data-preserve-html="true"><i>高斯分布：</i> 表示常態分布的直方圖，類似鐘形曲線。</li> <li data-preserve-html="true"><i>三角形：</i> 一個三角形直方圖。</li> </ul> |
| <b>混亂</b> <i>浮標</i> | 取代噪音的成分。    這可以用來動畫噪音。 |
| <b>無序速度</b> <i>浮標</i> | 調整由 <b>無序</b> 參數所施加的位移距離。    這可用於控制噪聲動畫時的位移速度。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![白噪音 - 範例1](../../../../../../assets/white_noise_v2_1.png "白噪音 - 範例 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![白噪音 - 範例2](../../../../../../assets/white_noise_v2_speed0.6_aniso0.gif "白噪音 - 範例2"){zoomable="yes"}

</td>
</tr>
</table>
