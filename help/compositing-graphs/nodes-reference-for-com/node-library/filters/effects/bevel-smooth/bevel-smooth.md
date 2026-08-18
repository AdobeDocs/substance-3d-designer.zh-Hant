---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-smooth.html"
breadcrumb-title: ''
description: 使用Bevel Smooth節點在形狀和圖案上創造平滑斜邊，讓表面更真實。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel smooth
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 斜角光滑
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---


# 斜角光滑

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![各向異性桑原灰階圖示 各向異性桑原灰階圖示](../../../../../../assets/bevel_smooth.png ""){width="200px"}

<b>收錄於：</b>濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

從遮罩邊界向外、向內或兩者同時畫出漸層或平面色。

重疊梯度會依反正規化距離排序，因此繪製出最近邊界的距離。

梯度的距離可以利用距離圖沿邊界動態調整。

</td>
</tr>
</table>

>[!TIP]
>
> [方向距離](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/directional-distance/directional-distance.md)節點提供類似功能，縮放是在特定方向進行。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### 輸出連接器

</td>
<td style="border: 0;" valign="top">

### 參數

</td>
</tr>
</table>

## 輸入連接器

|  |  |
| --- | --- |
| <b>遮罩輸入</b> *灰階* 初級 | 應該從中擷取遮罩的影像。 所有高於「遮罩閾值」的值在該遮罩中都是白色。 |
| <b>來源輸入</b> *灰階* | 僅在「輸出模式」參數設為「Dilation」時使用。 此時，影像會疊加在遮罩的白色區域上，邊界的灰階值會被放大。 |
| <b>距離圖</b> *灰階* | 當「距離映射乘數」參數值高於0時，這是可選輸入。 它用來調整遮罩邊界的斜面/膨脹距離，暗色值會使距離變短。 |

## 輸出連接器

|  |  |
| --- | --- |
| <b>產出</b> *灰階* | 根據所選的「輸出模式」呈現的結果影像。 |
| <b>紫外線</b> *顏色* | 一個 UV 貼圖，UV 沿著遮罩邊界放大。 它可以連接到 [UV 映射](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-color/uv-mapper-color.md) 節點，利用這些放大的 UV 映射其他影像。 |

## 參數

|  |  |
| --- | --- |
| <b>輸出模式</b> *整數* | 遮罩邊界擴張的方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>斜角：</b>從1畫到0的梯度，最大「距離」達到0</li> <li data-preserve-html="true"><b>放大：</b>畫出純色直到「最大距離」。 此顏色為白色，或遮罩邊界的「來源輸入」影像（若連接）為顏色</li> <li data-preserve-html="true"><b>距離：</b>在正規化影像空間中，距離最近遮罩邊界的原始距離，其中 1 是影像最短邊的長度</li> </ul> |
| <b>導演</b> *整數*   *：當「輸出模式」設為「倒角」或「膨脹」時可用* | 面罩邊框應該擴大的一側：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>在：</b>向面具內部畫</li> <li data-preserve-html="true"><b>向外</b>：向面具外側畫畫</li> <li data-preserve-html="true"><b>內外：</b>同時向面具內外兩側繪製</li> </ul> |
| <b>最大距離</b> *浮標* | 在正規化影像空間中，1 是輸入影像較短邊的長度，表示膨脹距離。 |
| <b>遮罩平滑度</b> *浮標* | 對遮罩施加的平滑強度。 這個數值是模糊的半徑，1 單位是影像的 1/256。 |
| <b>遮罩偏移量</b> *浮標* | 這樣可以將遮罩邊界向內或向外移動。 |
| <b>遮罩閾值</b> *浮標* | 用來偵測遮罩影像中遮罩邊界的值。 高於此門檻的數值為遮罩形狀的內部&#x200B;*，低於此範圍的數值為**外*&#x200B;層。 |
| <b>規模</b> *Float2* | 調整膨脹的水平（X）與垂直（Y）距離。 這些值是「最大距離」參數值的乘數。 |
| <b>距離圖乘數</b> *整數* | 調整「距離地圖」對「最大距離」的影響。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![斜面光滑：範例 1](../../../../../../assets/bevel_smooth_example_1.gif "斜面光滑：範例 1"){width="1024px" zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![斜角光滑：範例 8](../../../../../../assets/bevel_smooth_example_8.jpg "斜角光滑：範例 8"){width="1024px" zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_4_before.jpg" alt="bevel_smooth_example_4_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_4_after.jpg" alt="bevel_smooth_example_4_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_2_before.jpg" alt="bevel_smooth_example_2_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_2_after.jpg" alt="bevel_smooth_example_2_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_3_before.jpg" alt="bevel_smooth_example_3_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_3_after.jpg" alt="bevel_smooth_example_3_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_5_before.jpg" alt="bevel_smooth_example_5_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_5_after.jpg" alt="bevel_smooth_example_5_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_7_before.jpg" alt="bevel_smooth_example_7_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_7_after.jpg" alt="bevel_smooth_example_7_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>
