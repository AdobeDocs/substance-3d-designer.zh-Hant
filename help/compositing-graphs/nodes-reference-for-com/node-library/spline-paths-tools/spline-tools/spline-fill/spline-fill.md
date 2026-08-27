---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-fill.html"
breadcrumb-title: ''
description: 使用 Spline Fill 節點來填充由封閉樣條定義的區域，並用貼圖或顏色填滿。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Fill
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 樣條填充
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---


# 樣條填充

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/spline-fill-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

會用實心白色填滿輸入樣條的內部。 外牆則是純黑色。

開放樣條線是從開始到結束以直線封閉的。 樣條與曲線交叉的交叉點，透過在這些交會點將線的內側與外側反轉來解決。

</td>
</tr>
</table>

>[!IMPORTANT]
>
> 不建議在 [0,1] 圖塊外的樣條線上使用此節點。 在這種情況下，填充過程就不可靠了。

## 輸入連接器

<b>樣條座標</b> *色彩*&#x200B;輸入樣條點的座標編碼在彩色影像的 RGBA 通道中：\
<b>    R</b> - X 位置\
<b>    G</b> - Y 位置\
<b>    B</b> - 身高\
<b>A</b> - 打包資料：\
* 符號：樣條鍵為閉（負）或開（正）;\
* 絕對值：厚度 + 1。

<b>樣條資料</b> *色彩*&#x200B;輸入樣條的額外資料編碼於彩色影像的 RGBA 通道中。\
<b>    R</b> - 切線 X\
<b>    G</b> - 切線 Y\
<b>    B</b> - 未上場\
<b>    A</b> - 未上場

<b>樣條量</b> *整數*：輸入樣條的數量。

## 輸出連接器

<b>產出</b> *灰階*\
結果圖像是將輸入樣條線填滿平面白色，背景為平面黑色。

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineFill-Variant1-Before.jpg" alt="樣條填充變體1-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineFill-Variant1-After.jpg" alt="樣條填充變體1-之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![節點範例 2](../../../../../../assets/SplineFill-Demo.gif "節點範例 2")

</td>
</tr>
</table>
