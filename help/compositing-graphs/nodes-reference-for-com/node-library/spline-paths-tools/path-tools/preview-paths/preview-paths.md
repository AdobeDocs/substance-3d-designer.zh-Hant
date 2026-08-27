---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/preview-paths.html"
breadcrumb-title: ''
description: 使用預覽路徑節點在 2D 視圖中視覺化路徑資料，方便除錯與驗證。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Preview Paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 預覽路徑
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%

---


# 預覽路徑

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/preview-paths-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 路徑工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

在給定背景上描繪路徑的段與頂點。 每條路徑隨機一個顏色。

你會得到類似 Mask</b> to Path](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 預覽輸出[的結果<b>，但選項更多。

</td>
</tr>
</table>

## 輸入連接器

<b>背景</b> *顏色*\
背景圖片放在上面，顯示路徑。 這也控制渲染大小。

<b>路徑</b> *顏色*\
一份編碼段路徑列表。 將此輸入連接到 Mask to Paths](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 的結果[，或是連接到另一個 Path-processing 節點。

## 參數

<b>展覽角</b> *布林值*\
每個頂點上顯示一個標記為角點的正方形（加法混合）。

<b>展示頂點</b> *布林值*\
每個頂點顯示一個圓形（加法混合）。 角落仍以方格形式顯示。

<b>段厚（px）</b> *浮標*\
調整渲染片段的像素厚度。

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![節點範例 1](../../../../../../assets/PathsToSpline-Variant2-Before_1.jpg "節點範例 1")

</td>
<td style="border: 0;" valign="top">

![節點範例 2](../../../../../../assets/PathsToSpline-Variant1-Before_1.jpg "節點範例 2")

</td>
</tr>
</table>
