---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-select.html"
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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---


# 路徑選擇

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/paths-select-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 路徑工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

在 Paths 中從多個路徑中分離出一條路徑。

</td>
</tr>
</table>

## 輸入連接器

<b>唱片公司</b> *類型*\
一份編碼段路徑列表。 將此輸入連接到 Mask to Paths[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 的結果，或是連接到另一個 Path-processing 節點。

## 輸出連接器

<b>路徑</b> *顏色*\
路徑輸入只有一條路徑。 你可以使用[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)預覽路徑來了解結果代表什麼，使用其他路徑處理節點，或[輸入](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)到路徑到樣條線（Paths to Spline）中，進一步以樣條線處理。

## 參數

<b>選擇模式</b> *整數*&#x200B;選擇路徑的方法：\
*- 依 ID：*&#x200B;從列表中選擇索引與 Path ID</b> 指定<b>路徑相符的路徑;\
*- 依長度*&#x200B;選擇路徑長度高於或低於目標長度</b>所規定<b>的閾值。

<b>路徑識別碼</b> *整數* （當 <b>選擇模式</b> 設為 *ID* 時可用）\
選取路徑的索引。\
若數值超過<b>*路徑數，則輸出*</b>&#x200B;為空白。

<b>長度是大還是短？</b> *布林值* （當 <b>選擇模式</b> 設為 *按長度*&#x200B;時可用）\
控制選擇長度是否應包含或大於或更短 <b>於目標長度</b>。

<b>目標長度</b> *浮點*（當 <b>選取模式</b> 設為 *按長度*&#x200B;時可用）\
選擇樣條鍵的長度閾值。

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant2-Before.jpg" alt="路徑至斜線變體2-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsSelect-Variant1.jpg" alt="PathsSelect-Variant1">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant2-Before.jpg" alt="路徑至斜線變體2-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsSelect-Variant2.jpg" alt="PathsSelect-Variant2">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
