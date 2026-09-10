---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/path-2d-transform.html"
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
source-git-commit: f9ae596767e754b5c0f62ed6bdb6f16dd33bb799
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 1%

---


# 路徑二維轉換

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](path-2d-transform.resources/path-2d-transform-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 路徑工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

用裝置轉換路徑。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>路徑</b> <i>顏色</i> | 一份編碼段路徑列表。 將此輸入連接到 Mask to Paths[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 的結果，或是連接到另一個 Path-processing 節點。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>路徑</b> <i>顏色</i> | 變形的路徑。 你可以使用[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)預覽路徑來了解結果代表什麼，使用其他路徑處理節點，或[輸入](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)到路徑到樣條線（Paths to Spline）中，進一步以樣條線處理。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>轉換矩陣</b> <i>Float4</i> | 將變換矩陣套用到樣條上。 有三種編輯矩陣參數的模式：<br>*- 轉換裝置：*&#x200B;當選擇樣條 2D 轉換節點時，調整 2D 視圖[&#128279;](../../../../../../interface/2d-view/2d-view.md)中顯示裝置的把手;<br>*- 旋轉/拉伸：*&#x200B;分別控制樣條的旋轉與拉伸。請注意，數值總是相對於電流變換來套用。 例如，兩次套用 50% 寬度會得到 25% 寬度;<br>*- 矩陣值：* 點擊 <b>「編輯矩陣值</b> 」按鈕，直接輸入矩陣的原始數值。 |
| <b>偏移</b> <i>Float2</i> | 對 X 的樣條線（水平）和 Y（垂直）套用位置偏移。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="path-2d-transform.resources/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>之前</i>
    </td>
    <td>
      <img src="path-2d-transform.resources/Paths2DTransform-Variant1.jpg" alt="Paths2DTransform-Variant1">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="path-2d-transform.resources/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>之前</i>
    </td>
    <td>
      <img src="path-2d-transform.resources/Paths2DTransform-Variant2.jpg" alt="Paths2DTransform-Variant2">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
