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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

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

## 輸入連接器

<b>輸入 </b>*顏色*&#x200B;濾鏡應該應用於的彩色影像。

## 輸出連接器

<b>產出</b> *顏色*&#x200B;透過對輸入色彩影像應用濾波器而得出的彩色影像。

## 參數

<b>核心大小</b> *整數*&#x200B;核是一組用於濾波器計算的特定值。 在此語境下，它是相鄰像素的值。\
對於每個像素，濾波器會以正方核取該像素周圍的所有鄰居，並計算所有鄰居的中位數值。\
這個參數控制該正方形核的大小，單位為像素。 較大的核能產生更強且更廣的平滑效果，但會犧牲一些細節。\
*- 3x3：* 寬3像素、高3像素的核，總共8個鄰居像素。\
*- 5x5：* 核心寬 5 像素、高 5 像素，總共 24 個鄰居像素。

<b>濾波器類型</b> *整數*&#x200B;計算應用於核中取樣的鄰居。\
*- 中位數：* 直接使用所有鄰居的中位數值。\
*- MLMAD：* 代表「最小中位數絕對偏差中位數」。 偏差反映了值與中位數的差異。 MLMAD 方法不直接使用中位數值，因為中位值可能被偏移較大的離群點所偏斜，而是使用所有偏差的中位數。 此方法能產生更強的平滑效果，可能根據核粒大小使區域扁平。

<b>情感阿爾法</b> *布林運算*&#x200B;控制是否應將濾波器套用於影像的 alpha 通道。 當 True *時*，alpha 通道不變。

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
