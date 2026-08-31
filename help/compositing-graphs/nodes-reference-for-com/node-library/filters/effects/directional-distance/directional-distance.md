---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/directional-distance.html"
breadcrumb-title: ''
description: 使用方向距離節點來計算特定方向的距離場，以產生程序效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Directional distance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 方向距離
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---


# 方向距離

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![各向異性桑原灰階圖示 各向異性桑原灰階圖示](directional-distance.resources/directional-distance-01.png ""){width="200px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

從遮罩邊界沿指定方向繪製距離梯度。

重疊梯度會依反正規化距離排序，因此繪製出最近邊界的距離。

梯度的距離可以利用距離圖沿邊界動態調整。

</td>
</tr>
</table>

>[!TIP]
>
> [斜角平滑](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/bevel-smooth/bevel-smooth.md)節點提供類似功能，膨脹可向所有方向進行。

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入</b> <i>灰階</i> 初級 | 應該從中擷取遮罩的影像。   該遮罩中所有高於 0.5 的值皆為白色。 |
| <b>距離圖</b> <i>灰階</i> | 當「距離映射乘數」參數值高於0時，這是可選輸入。   它用來調整遮罩邊界的斜面/膨脹距離，暗色值會使距離變短。 |
| <b>角度圖</b> <i>灰階</i> | 當「角度圖乘數」參數值高於0時，會選用此輸入。   它用來調整距離梯度的方向，方法是將距離梯度的值加到方向角上，以轉彎次數計算。   「角度貼圖偏移」參數允許你透過指定哪個值是 0 來重新映射這些值。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>產出</b> <i>灰階</i> | 根據所選的「輸出模式」呈現的結果影像。 |
| <b>紫外線</b> <i>顏色</i> | 一個 UV 貼圖，UV 從遮罩邊界沿指定方向放大。   它可以連接到 [UV 映射](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-color/uv-mapper-color.md) 節點，利用這些放大的 UV 映射其他影像。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>輸出模式</b> *整數* | 從遮罩邊界繪製距離梯度的方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>反正規化距離：</b> 從 1 到 0 的梯度，當「最大距離」達到 0，若連接時乘以「距離圖」</li> <li data-preserve-html="true"><b>距離：</b> 從遮罩邊界開始的原始距離值漸變，其中 1 是輸入影像較短邊的長度</li> </ul> |
| <b>最大距離</b> *浮標* | 距離梯度在正規化影像空間中行進的距離，其中 1 是輸入影像較短邊的長度。 |
| <b>角度</b> *浮標* | 距離梯度的方向，以轉彎數為單位，0 為水平且向右——即一個 （1,0） 向量。 |
| <b>距離圖乘數</b> *浮標* | 調整「距離地圖」對「最大距離」的影響。   注意：當「距離地圖」輸入未連接時，此參數不影響。 |
| <b>角度圖乘數</b> *浮標* | 調整「角度圖」相對於「角度」的影響。 |
| <b>角度圖偏移</b> *浮標* | 透過指定該映射中應為 0 的值來重新映射「角度圖」中的值。   例如，偏移為0.5表示0.75為0.25回合，0.3為-0.2回合。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="directional-distance.resources/directional-distance-02.jpg" alt="directional_distance_example_1_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional-distance-03.jpg" alt="directional_distance_example_1_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="directional-distance.resources/directional-distance-04.jpg" alt="directional_distance_example_3_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional-distance-05.jpg" alt="directional_distance_example_3_after">
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
      <img src="directional-distance.resources/directional-distance-06.jpg" alt="directional_distance_example_2_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional-distance-07.jpg" alt="directional_distance_example_2_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="directional-distance.resources/directional-distance-08.jpg" alt="directional_distance_example_5_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional-distance-09.jpg" alt="directional_distance_example_5_after">
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
      <img src="directional-distance.resources/directional-distance-10.jpg" alt="directional_distance_example_4_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional-distance-11.jpg" alt="directional_distance_example_4_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>
