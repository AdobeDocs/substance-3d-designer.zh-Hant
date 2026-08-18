---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-color.html"
breadcrumb-title: ''
description: 使用 Spline Bridge Mapper Color 節點，將兩個帶有色彩映射的樣條紋架接。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 樣條橋映射器顏色
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# 樣條橋映射器顏色

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/spline-bridge-mapper-color-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

將彩色影像映射到輸入樣條列中，使影像依序遍歷樣條曲線。

</td>
</tr>
</table>

>[!TIP]
>
> 映射從列表中第一個樣條線到最後一個樣條線，並嚴格依照列表中這些樣條線的順序遍歷中間樣條線。
> 
> 因此，你應該事先注意樣條的附加順序。

>[!NOTE]
>
> 另 [見樣條橋映射灰階](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-gra/spline-bridge-mapper-grayscale.md)。

## 輸入連接器

<b>樣條座標</b> *色彩*&#x200B;輸入樣條點的座標編碼在彩色影像的 RGBA 通道中：\
<b>R</b> - X 位置\
<b>G</b> - Y 位置\
<b>B</b> - 身高\
    <b>A</b> - 打包資料：\
* 符號：樣條鍵為閉（負）或開（正）;\
* 絕對值：厚度 + 1。

<b>樣條資料</b> *色彩*&#x200B;輸入樣條的額外資料編碼於彩色影像的 RGBA 通道中。\
<b>R</b> - 切線 X\
<b>G</b> - 切線 Y\
<b>B</b> - 未上場\
<b>A</b> - 未上場

<b>樣條量</b> *整數*：輸入樣條的數量。

<b>色彩映射&#x200B;</b>*顏色*&#x200B;應映射到輸入樣條的輸入色彩影像。

## 輸出連接器

<b>顏色</b> *灰階*&#x200B;將輸入的彩色影像映射到背景上的樣條，作為彩色影像。

<b>高度</b> *灰階*&#x200B;樣條曲線的高度映射在樣條曲線上，作為灰階影像。

<b>紫外線</b> *色彩*&#x200B;映射影像的 UV（即座標），編碼於彩色影像的紅色（U）與綠色（V）通道中。

<b>面具</b> *灰階*：樣條曲線上映射的遮罩。

## 參數

<b>分段數量</b> *整數*&#x200B;樣條在影像座標穿越前會被簡化為段。\
線段越多，曲線上的映射就越平滑。

<b>減少紫外線拉伸</b> *布林值*：調整從一個樣條線插值到下一個樣條線的方法，以減少樣條間距離不均勻時的拉伸。

<b>紫外線尺度</b> *Float2*&#x200B;調整影像座標的縮放。 數值越高，圖塊越密集。

<b>紫外線旋轉</b> *浮動*&#x200B;將影像座標繞中心旋轉。

<b>背景色</b> *Float4*&#x200B;輸出影像中背景的顏色。

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineBridgeMapperGrayscale-Variant1-Before.jpg" alt="SplineBridgeMapper灰階變體1-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineBridgeMapperColor-Variant1-After.jpg" alt="樣條橋映射器顏色變體1-之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![節點範例 2](../../../../../../assets/SplineBridgeMapperColor-Demo.gif "節點範例 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![節點範例 1](../../../../../../assets/SplineBridgeMapperColor-Variant1-After1.jpg "節點範例 1")

</td>
<td style="border: 0;" valign="top">

![節點範例 2](../../../../../../assets/SplineBridgeMapperColor-Graph.jpg "節點範例 2")

</td>
</tr>
</table>
