---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/anisotropic-noise.html"
breadcrumb-title: ''
description: 使用各向異性雜訊節點來產生方向性雜訊圖案，以創造各向異性紋理效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Anisotropic noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 各向異性雜訊
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 2%

---


# 各向異性雜訊

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![各向異性雜訊 - 圖像](../../../../../../assets/anisotropic_noise_v2.png "各向異性雜訊 - 各向異性雜訊 - 圖示"){width="200px"}

<b>收錄於：</b>貼圖產生器>噪音

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一疊水平或垂直排列的隨機顏色條狀條狀物，彼此漸漸融合。

紙條的數量可以調整，過渡的平滑程度也可以調整。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 輸出

</td>
<td style="border: 0;" valign="top">

### 參數

</td>
<td style="border: 0;" valign="top">

### 範例

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
| <b>X 個整</b>  數 | X 軸上的條帶數量。 |
| <b>Y 個整</b>  數 | Y軸條數。 |
| <b>y 個量以解析</b>  布林值計算 | 若為真，則Y軸上的條帶數量將等於該軸上的影像大小。 |
| <b>旋轉</b>  布林值 | 把噪音旋轉90度。 |
| <b>平滑</b>  浮球 | 條帶之間的漸變量，0 表示沒有漸入，1 則在整個長度上逐漸消失。 |
| <b>平滑性插值</b>  浮點 | 兩種插值方法的權重來衰落條帶，其中0為線性，1為高斯。 |
| <b>混亂</b>  漂浮 | 取代噪音的成分。 這可以用來動畫噪音。 |
| <b>無序速度</b>  浮動 | 調整由<b>無序</b>參數所施加的位移距離。 這可用於控制噪聲動畫時的位移速度。 |
| <b>非平方展開</b>  布林 | 在非正方形影像中，保持產生的磁磚方正，並將雜訊產生擴展到影像的範圍。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![各向異性雜訊 - 範例 1](../../../../../../assets/anisotropic_noise_v2_1.png "各向異性雜訊 - 範例 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![各向異性雜訊 - 範例 2](../../../../../../assets/noise_anisotropic_noise_v2_speed0.3_aniso0.6.gif "各向異性雜訊 - 範例 2"){zoomable="yes"}

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
