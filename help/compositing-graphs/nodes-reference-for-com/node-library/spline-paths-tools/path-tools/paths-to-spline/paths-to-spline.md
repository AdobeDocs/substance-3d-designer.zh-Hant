---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-to-spline.html"
breadcrumb-title: ''
description: 使用 Paths to Spline 節點將路徑資料轉換為樣條線，以便用於基於樣條的節點。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths to Spline
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 通往樣條的路徑
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# 通往樣條的路徑

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](paths-to-spline.resources/paths-to-splines-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 路徑工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

將路徑轉換成樣條曲線，並可透過[樣條線渲染](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-render/spline-render.md)節點視覺化並處理[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-tools.md)。

</td>
</tr>
</table>

>[!NOTE]
>
> 樣條曲線是曲線，因此無法保留路徑的銳利度。 在將路徑轉換成樣條曲線時，可以預期形狀會有些平滑。

>[!TIP]
>
> 此節點可在 Mask to Paths[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 節點之後使用，形成一條將遮罩轉換為樣條的鏈。

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>路徑</b> <i>顏色</i> | 一份編碼段路徑列表。 將此輸入連接到 Mask to Paths[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 的結果，或是連接到另一個 Path-processing 節點。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>樣條座標</b> <i>顏色</i> | 彩色影像RGBA通道中編碼的輸入樣條點座標：<br><b>R</b> - X 位置<br><b>G</b> - Y 位置<br><b>B</b> - 高度<br><b>A</b> - 打包資料：<br>* 符號：樣條鍵為閉合（負）或開（正）;<br>* 絕對值：厚度 + 1。 |
| <b>樣條資料</b> <i>顏色</i> | 彩色影像RGBA通道<b></b>中編碼的輸入樣條額外資料：<br><b>R</b> - 切線 X<br><b>G</b> - 切線 Y<br><b>B</b> - 未使用<br><b>A</b> - 未使用 |
| <b>樣條量</b> <i>整數</i> | 輸入樣條的數量。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>樣條精度</b> <i>整數</i> | 以 Paths 輸入每條路徑中取樣頂點數的底數對數（log²）來建立對應的樣條。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-to-spline.resources/PathsToSpline-Variant1-Before.jpg" alt="路徑至縱線變體1-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="paths-to-spline.resources/PathsToSpline-Variant1-After.jpg" alt="路徑至樣線變體1-之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-to-spline.resources/PathsToSpline-Variant2-Before.jpg" alt="路徑至斜線變體2-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="paths-to-spline.resources/PathsToSpline-Variant2-After.jpg" alt="路徑至斜線變體2-之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
