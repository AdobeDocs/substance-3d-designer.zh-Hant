---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-select.html"
breadcrumb-title: ''
description: 使用路徑選擇節點，根據條件從路徑列表中選取並篩選特定路徑。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 路徑選擇
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---


# 路徑選擇

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](paths-select.resources/paths-select-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 路徑工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

在 Paths 中從多個路徑中分離出一條路徑。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>唱片公司</b> <i>類型</i> | 一份編碼段路徑列表。 將此輸入連接到 Mask to Paths[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 的結果，或是連接到另一個 Path-processing 節點。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>路徑</b> <i>顏色</i> | 路徑輸入只有一條路徑。 你可以使用[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)預覽路徑來了解結果代表什麼，使用其他路徑處理節點，或[輸入](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)到路徑到樣條線（Paths to Spline）中，進一步以樣條線處理。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>選擇模式</b> <i>整數</i> | 選擇路徑的方法：<br>*- 依 ID：*&#x200B;從列表中選擇索引與路徑 ID</b> 中指定的<b>路徑相符;<br>*- 依長度*：選擇長度高於或低於目標長度</b>所指定<b>閾值的路徑。 |
| <b>路徑識別碼</b> <i>整數</i> （當 <b>選擇模式</b> 設為 *ID* 時可用） | 選取路徑的索引。<br>若值大於路徑&#x200B;*數量，<b>則輸出*</b>&#x200B;為空白。 |
| <b>長度是大還是短？</b> <i>布林值</i> （當 <b>選擇模式</b> 設為 *按長度*&#x200B;時可用） | 控制選擇長度是否應包含或大於或更短 <b>於目標長度</b>。 |
| <b>目標長度</b> <i>浮點</i> （當 <b>選取模式</b> 設為 *按長度*&#x200B;時可用） | 選擇樣條鍵的長度閾值。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-select.resources/PathsToSpline-Variant2-Before.jpg" alt="路徑至斜線變體2-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="paths-select.resources/PathsSelect-Variant1.jpg" alt="PathsSelect-Variant1">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-select.resources/PathsToSpline-Variant2-Before.jpg" alt="路徑至斜線變體2-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="paths-select.resources/PathsSelect-Variant2.jpg" alt="PathsSelect-Variant2">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
