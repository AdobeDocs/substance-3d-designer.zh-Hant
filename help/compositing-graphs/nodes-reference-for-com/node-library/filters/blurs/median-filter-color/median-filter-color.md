---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/median-filter-color.html"
breadcrumb-title: ''
description: 使用中位數濾鏡色彩節點來降低雜訊並保留色彩紋理中的邊緣。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Median filter color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 中位濾光色
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---


# 中位濾光色

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![中位數濾鏡顏色：圖示](../../../../../../assets/MedianFilter_Icon_Color.png "中位數濾鏡顏色：圖示")

<b>收錄於：</b> 模糊>濾鏡

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這個濾波器能平滑影像中的雜訊，同時保留邊緣。

對於每個像素，節點會根據該像素鄰近像素的中位數值計算一個顏色值。

</td>
</tr>
</table>

>[!NOTE]
>
> 另 [見中位數濾波器灰階](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/median-filter-grayscale/median-filter-grayscale.md)。

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入</b> <i>顏色</i> | 就是濾鏡應該應用的彩色影像。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>產出</b> <i>顏色</i> | 彩色影像是透過對輸入彩色影像應用濾波器來計算出來的。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>核心大小</b> *整數* | 核是用於濾波器計算的特定數值群組。 在此語境下，它是相鄰像素的值。<br><br>對於每個像素，濾波器會以正方核取該像素周圍的所有鄰居，並計算所有鄰居的中位數值。<br><br>這個參數控制該正方形核的大小，單位為像素。 較大的核會產生更強且更遠的平滑效果，但會犧牲部分細節。<br><br>*- 3x3：* 寬3像素、高3像素的核，總共8個鄰居像素。<br>*- 5x5：* 寬5像素、高5像素的核，總共24個鄰居像素。 |
| <b>濾波器類型</b> *整數* | 計算應用於核中取樣的鄰居。<br><br>*- 中位數：* 直接使用所有鄰居的中位數值。<br>*- MLMAD：* 代表「最小中位數絕對偏差中位數」。 偏差反映了值與中位數的差異。 MLMAD 方法不直接使用中位數值，因為中位值可能被偏移較大的離群點所偏斜，而是使用所有偏差的中位數。 此方法能產生更強的平滑效果，可能根據核粒大小使區域扁平。 |
| <b>情感阿爾法</b> *布林值* | 控制是否應對影像的 alpha 通道施加濾波器。 當 True *時*，alpha 通道不變。 |

## 範例

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant2A.png" alt="MedianFilter_Variant2A">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant2B.png" alt="MedianFilter_Variant2B">
      <br><i>之後</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant3A.png" alt="MedianFilter_Variant3A">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant3B.png" alt="MedianFilter_Variant3B">
      <br><i>之後</i>
    </td>
  </tr>
</table>
