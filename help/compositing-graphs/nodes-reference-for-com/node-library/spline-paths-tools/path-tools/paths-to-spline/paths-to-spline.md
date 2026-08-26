---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-to-spline.html"
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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---


# 通往樣條的路徑

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/paths-to-splines-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 路徑工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

將路徑轉換成樣條曲線，並可透過[樣條線渲染](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-render/spline-render.md)節點視覺化並處理[](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-tools.md)。

</td>
</tr>
</table>

>[!NOTE]
>
> 樣條曲線是曲線，因此無法保留路徑的銳利度。 在將路徑轉換成樣條曲線時，可以預期形狀會有些平滑。

>[!TIP]
>
> 此節點可在 Mask to Paths](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 節點之後[使用，形成一條將遮罩轉換為樣條的鏈。

## 輸入連接器

<b>路徑</b> *顏色*\
一份編碼段路徑列表。 將此輸入連接到 Mask to Paths](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 的結果[，或是連接到另一個 Path-processing 節點。

## 輸出連接器

<b>樣條座標&#x200B;</b>*顏色*&#x200B;輸入樣條點的座標編碼在彩色影像的 RGBA 通道中：\
<b>R</b> - X 位置\
<b>G</b> - Y 位置\
<b>B</b> - 身高\
<b>A</b> - 打包資料：\
* 符號：樣條鍵為閉（負）或開（正）;\
* 絕對值：厚度 + 1。

<b>樣條資料</b> *顏色*\
彩色影像RGBA通道<b></b>中編碼的輸入樣條的額外資料：\
<b>R</b> - 切線 X\
<b>G</b> - 切線 Y\
<b>B</b> - 未上場\
<b>A</b> - 未上場

<b>樣條量</b> *整數*\
輸入樣條的數量。

## 參數

<b>樣條精度</b> *整數*\
以 Paths 輸入每條路徑中取樣頂點數的底數對數（log²）來建立對應的樣條。

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant1-Before.jpg" alt="路徑至縱線變體1-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant1-After.jpg" alt="路徑至樣線變體1-之後">
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
      <img src="../../../../../../assets/PathsToSpline-Variant2-After.jpg" alt="路徑至斜線變體2-之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
