---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/path-2d-transform.html"
breadcrumb-title: ''
description: 使用 Path 2D Transform 節點來轉換帶有平移、旋轉和縮放操作的路徑。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Path 2D Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 路徑二維轉換
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# 路徑二維轉換

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/path-2d-transform-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 路徑工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

用裝置轉換路徑。

</td>
</tr>
</table>

## 輸入連接器

<b>路徑</b> *顏色*\
一份編碼段路徑列表。 將此輸入連接到 Mask to Paths[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 的結果，或是連接到另一個 Path-processing 節點。

## 輸出連接器

<b>路徑</b> *顏色*\
變形的路徑。 你可以使用[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)預覽路徑來了解結果代表什麼，使用其他路徑處理節點，或[輸入](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)到路徑到樣條線（Paths to Spline）中，進一步以樣條線處理。

## 參數

<b>轉換矩陣</b> *Float4*\
將變換矩陣套用到樣條上。 編輯矩陣參數有三種模式：\
*- 轉換裝置：*&#x200B;當選擇 Spline 2D 轉換節點時，調整 2D 視圖[&#128279;](../../../../../../interface/2d-view/2d-view.md)中顯示裝置的手柄;\
*- 旋轉/拉伸：* 個別控制花鍵的旋轉與拉伸。 請注意，數值總是相對於電流變換來套用。 例如，將 50% 寬度重複應用會得到 25% 寬度;\
*- 矩陣值：* 點擊 <b>「編輯矩陣值</b> 」按鈕，直接輸入矩陣的原始數值。

<b>偏移</b> *Float2*\
對 X 的樣條線（水平）和 Y（垂直）套用位置偏移。

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
      <img src="../../../../../../assets/Paths2DTransform-Variant1.jpg" alt="Paths2DTransform-Variant1">
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
      <img src="../../../../../../assets/Paths2DTransform-Variant2.jpg" alt="Paths2DTransform-Variant2">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
