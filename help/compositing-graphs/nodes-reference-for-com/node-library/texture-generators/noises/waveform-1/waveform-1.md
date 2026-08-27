---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/waveform-1.html"
breadcrumb-title: ''
description: 使用 Waveform 1 節點來產生波形圖案，以創造有機的紋理與程序變化。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Waveform 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 波形 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 1%

---


# 波形 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![波形 1 - 圖示](waveform-1.resources/waveform_01_v2.png "波形 1 - 圖示"){width="200px"}

<b>收錄於：</b> 貼圖產生器>噪音

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一組用戶選擇的圖案水平排列，堆疊成類似波形的形狀。

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
| <b>取樣</b> <i>整數</i> | 沿著 X 軸放置的圖案數量，用來繪製波形，數值越低，波形呈現較階梯狀的外觀。 |
| <b>功能</b> <i>整數</i> | 用來繪製波形的函數。   這控制了每個樣本所放置圖案的垂直尺寸：<ul data-preserve-html="true"> <li data-preserve-html="true"><i>價值雜訊：</i> 數值的隨機分布</li> <li data-preserve-html="true"><i>餘弦：</i> 數值隨餘弦函數的進展而變化</li> <li data-preserve-html="true"><i>自訂函式：</i> 使用使用者自創函式來驅動數值</li> </ul> |
| <b>自訂功能</b> <i>浮標</i>   *當「功能」設為「自訂功能」時可用* | 計算每個樣本放置圖案的垂直尺寸。   可用變數：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>pos</b> （<i>浮點</i>）圖案在 X 軸上的位置。 這可以用來選擇圖案。</li> </ul> |
| <b>粗糙度</b> <i>浮標</i> | 在乾淨且平滑的波形與較粗糙且分布均勻的波形之間插值。    這可以被理解為乾淨訊號與白噪音的差別。 |
| <b>規模</b> <i>整數</i> | 影像中可見的波形水平跨度。 |
| <b>振幅最小。</b> <i>浮標</i> | 波形的最小值（或厚度）。 |
| <b>振幅最大。</b> <i>浮標</i> | 波形的最大值（或厚度）。 |
| <b>噪音</b> <i>浮標</i> | 對波形施加雜訊，隨機從垂直跨度中減去。 |
| <b>職位</b> <i>整數</i> | 波形在影像中的位置：<ul data-preserve-html="true"> <li data-preserve-html="true"><i>居中：</i> 原點位於影像的垂直中心</li> <li data-preserve-html="true"><i>底部：</i> 原點是圖片底部</li> </ul> |
| <b>模式</b> <i>整數</i> | 波形每個取樣點所放置的圖案。 |
| <b>模式變化</b> <i>浮標</i> | 有些圖案還能額外調整。 |
| <b>混亂</b> <i>浮標</i> | 波形的數值會被位移。    這可以用來動畫化。 |
| <b>無序速度</b> <i>浮標</i> | 調整由 <b>無序</b> 參數所施加的位移距離。    這可以用來控制波形動畫時的位移速度。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![波形1 - 範例1](waveform-1.resources/waveform_01_v2_speed0.1_aniso0.gif "波形1 - 範例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
