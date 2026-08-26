---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/median-filter-grayscale.html"
breadcrumb-title: ''
description: 使用中位數濾波器灰階節點來減少雜訊並保留灰階紋理中的邊緣。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Median filter grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 中位濾鏡灰階
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---


# 中位濾鏡灰階

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![中位數濾波器灰階：圖示](../../../../../../assets/MedianFilter_Icon_Grayscale.png "中位數濾波器灰階：圖示")

<b>收錄於：</b> 模糊>濾鏡

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這個濾波器能平滑影像中的雜訊，同時保留邊緣。

對於每個像素，節點會根據該像素鄰近像素的中位數值計算灰階值。

</td>
</tr>
</table>

>[!NOTE]
>
> 另 [見中位濾鏡顏色](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/median-filter-color/median-filter-color.md)。

## 輸入連接器

<b>輸入 </b>*灰階*&#x200B;濾鏡應該套用的灰階影像。

## 輸出連接器

<b>輸出&#x200B;</b>*灰階 灰階*&#x200B;影像是透過對輸入灰階影像應用濾波器而得出。

## 參數

<b>核心大小</b> *整數*&#x200B;核是一組用於濾波器計算的特定值。 在此語境下，它是相鄰像素的值。\
對於每個像素，濾波器會以正方核取該像素周圍的所有鄰居，並計算所有鄰居的中位數值。\
這個參數控制該正方形核的大小，單位為像素。 較大的核能產生更強且更廣的平滑效果，但會犧牲一些細節。\
*- 3x3：* 寬3像素、高3像素的核，總共8個鄰居像素。\
*- 5x5：* 核心寬 5 像素、高 5 像素，總共 24 個鄰居像素。

<b>濾波器類型</b> *整數*&#x200B;計算應用於核中取樣的鄰居。\
*- 中位數：* 直接使用所有鄰居的中位數值。\
*- MLMAD：* 代表「最小中位數絕對偏差中位數」。 偏差反映了值與中位數的差異。 MLMAD 方法不直接使用中位數值，因為中位值可能被偏移較大的離群點所偏斜，而是使用所有偏差的中位數。 此方法能產生更強的平滑效果，可能根據核粒大小使區域扁平。

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
      <img src="../../../../../../assets/MedianFilter_Variant4A.png" alt="MedianFilter_Variant4A">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant4B.png" alt="MedianFilter_Variant4B">
      <br><i>之後</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant1A.png" alt="MedianFilter_Variant1A">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant1B.png" alt="MedianFilter_Variant1B">
      <br><i>之後</i>
    </td>
  </tr>
</table>
