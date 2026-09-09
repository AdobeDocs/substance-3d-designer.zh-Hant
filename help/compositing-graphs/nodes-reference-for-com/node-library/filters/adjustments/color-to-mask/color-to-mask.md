---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-to-mask.html"
breadcrumb-title: ''
description: 使用「色彩轉遮罩」節點，將特定顏色轉換成遮罩，以建立選擇性處理與遮罩效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color to mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 從顏色到遮罩
user-guide-description: ''
user-guide-title: ''
source-git-commit: 49bf753c2fa3d673b519b3ed87cc8bc82616bee6
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---


# 從顏色到遮罩

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![遮罩顏色 - 圖示](color-to-mask.resources/color_to_mask.png "遮罩顏色遮罩 - 圖示"){width="200px"}

<b>收錄於：</b> 篩選>調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

從彩色影像中選取的顏色中擷取灰階遮罩。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入</b> <i>顏色</i> | 遮罩應該根據顏色提取的輸入色彩影像。 |
| <b>色彩輸入</b> <i>顏色</i>   *當「使用色彩輸入」設為「真實」時，可用* | 輸入色彩影像用來定義每個像素的參考顏色。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>產出</b> <i>灰階</i> | 生成的遮罩會以灰階點陣圖形式呈現。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>使用色彩輸入</b> *布林值* | 使用輸入影像而非均勻顏色，以定義每個像素的參考顏色。    輸入影像由 <b>Color 輸入</b> 端提供。 |
| <b>顏色</b> *當「使用顏色輸入」設為「假」時，Float3*   *可用* | 參考均勻顏色，應以此為基礎進行顏色選擇。 |
| <b>門檻</b> *浮標* | 距離選取顏色下方參考色的距離。 |
| <b>選擇衰退</b> *浮標* | 根據與參考顏色的距離來淡化顏色選擇。 |
| <b>距離色彩空間</b> *整數* | 均衡過程是比較顏色以確定它們之間的距離。 某些色彩空間和距離演算法更適合特定使用情境。   這個下拉選單讓你選擇用來比較顏色的色彩空間：<ul data-preserve-html="true"> <li data-preserve-html="true"><b><i>RGB（資料）：</i></b> 顏色被分為紅、綠、藍三色通道，並沿這些軸線直接分布，完全不考慮人類感知。 這適用於包含原始資料的影像。</li> <li data-preserve-html="true"><i>線性 sRGB（彩色）：</i> 顏色分為紅、綠、藍三色通道，並依像素光強度線性分布。 這適用於可在顯示器上視覺化的影像。</li> <li data-preserve-html="true"><b><i>亮度（色彩）：</i></b> 顏色分為色相、色度、亮度值，且僅使用亮度值作為比較。 這適用於可在顯示器上視覺化的影像。</li> <li data-preserve-html="true"><i>Lab（顏色）：</i> 一個標準化的感知色彩空間，會以一種「感覺」接近的顏色在立方體中實際靠近的方式分配顏色。 這適用於可在顯示器上視覺化的影像。</li> <li data-preserve-html="true"><i>角度（法線）：</i> 顏色被分割成向量的 X、Y、Z 軸，並透過點積比較。 這適用於包含切空間法線的影像。</li> </ul> |
| <b>距離權重</b> *Float3* | Lab 色彩距離演算法（DeltaE2000）為每個亮度、色度和色相值引入特定的權重因子。   較低的數值會減少色差演算法中因素的影響。   由於眼睛通常接受的明度（L）差異大於色度（C）或色調（H）的差異，（L:C:H）的預設比值為 （0.5:1:1）。 0.5:1:與 1 的比例會讓亮度差異是色度或色相的兩倍。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
