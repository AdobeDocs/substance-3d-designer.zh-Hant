---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-compute.html"
breadcrumb-title: ''
description: 使用直方圖計算節點，從紋理中計算直方圖資料，進行分析與處理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram compute
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 直方圖計算
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 1%

---


# 直方圖計算

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![直方圖計算：圖示](histogram-compute.resources/histogram_compute.png "直方圖計算：圖示"){width="200px"}

<b>收錄於：</b> 篩選>調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

計算灰階影像的直方圖。

直方圖以影像中的一列像素編碼，每個像素值為 *與 X 軸像素位置相符的顏色值總體* 。\
例如，在 （0.25， 0） 處像素值為 75，表示影像中有 75 個像素具有 0.25 色彩值。

</td>
</tr>
</table>

節點同時輸出 *為影像計算的累積分布函數* （CDF）。

可利用節點計算的資料建立自訂工具，例如自訂遮罩，如下方「範例」章節所示。

>[!IMPORTANT]
>
> 所有超出[0,1]範圍的數值都會被夾住，因此直方圖對HDR影像可能不準確。

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入</b> <i>灰階</i> 初級 | 應該計算直方圖的影像。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>直方圖</b> <i>灰階</i> | 輸入影像計算的直方圖以一列像素編碼，每個像素值為 *與 X 軸像素位置匹配的色彩值總體* 。   例如，在 （0.25， 0） 處像素值為 75，表示影像中有 75 個像素具有 0.25 色彩值。 |
| <b>教區長</b> <i>灰階</i> | 這是 *為影像計算出的累積分布函數* （CDF）結果，編碼在一列像素中，每個像素是其左側所有像素值的總和。   接著 *將該總和與影像中像素總數進行正規化* 。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>直方圖解析度</b> *整數* | 直方圖的寬度。 較高的值能讓更細緻的值分布。   可用解析度以像素為單位：256、512、1024、2048、4096 |

## 範例

![直方圖計算：範例 1](histogram-compute.resources/histogram_compute_example_1.jpg "直方圖計算：範例 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="histogram-compute.resources/histogram_compute_example_2_before.jpg" alt="histogram_compute_example_2_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="histogram-compute.resources/histogram_compute_example_2_after.jpg" alt="histogram_compute_example_2_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>
