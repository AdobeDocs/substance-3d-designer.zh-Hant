---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/quad-transform-on-path.html"
breadcrumb-title: ''
description: 使用路徑上的四元轉換節點，對路徑曲線上的元素套用二次變換。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Quad Transform on Path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 路徑上的四邊變換
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 1%

---


# 路徑上的四邊變換

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/quad-transform-on-paths-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 路徑工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

用四個 handle 來變形路徑。

</td>
</tr>
</table>

## 輸入連接器

<b>路徑</b> *顏色*\
一份編碼段路徑列表。 將此輸入連接到 Mask to Paths[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 的結果，或是連接到另一個 *Path-processing* 節點。

## 輸出連接器

<b>路徑</b> *顏色*\
變形的路徑。 你可以使用[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)預覽路徑來了解結果代表什麼，使用其他路徑處理節點，或[輸入](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)到路徑到樣條線（Paths to Spline）中，進一步以樣條線處理。

## 參數

<b>p00</b> *Float2*\
左上角把手的位置。

<b>第01</b> *頁 Float2*\
右上方把手的位置。

<b>第2</b> *頁 Float2*\
左下角把手的位置。

<b>第03</b> *頁 Float2*\
右下角把手的位置。

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/QuadTransformOnPaths-Variant1-After.jpg" alt="QuadTransformOnPaths-Variant1-After">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/QuadTransformOnPaths-Variant2-After.jpg" alt="QuadTransformOnPaths-Variant2-After">
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

![節點範例 1](../../../../../../assets/QuadTransformOnPaths-Demo2.gif "節點範例 1")

</td>
<td style="border: 0;" valign="top">

![節點範例 2](../../../../../../assets/QuadTransformOnPaths-Demo1.gif "節點範例 2")

</td>
</tr>
</table>
