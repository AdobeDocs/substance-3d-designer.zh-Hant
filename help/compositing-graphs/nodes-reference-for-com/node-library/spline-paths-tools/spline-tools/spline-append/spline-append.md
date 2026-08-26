---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-append.html"
breadcrumb-title: ''
description: 使用 Spline Append 節點將多個樣條線附加在一起，以建立更長的連續路徑。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Append
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 樣條附錄
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---


# 樣條附錄

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/spline-append-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

樣條線是以清單形式封裝。 此節點將輸入樣條線清單（集合 #2）附加到現有清單（集合 #1）上。

列表的順序會被保留，也就是說，將 D-E-F 附加到 A-B-C 列表上，會得到一個 A-B-C-D-E-F 的列表。

</td>
</tr>
</table>

>[!TIP]
>
> 要注意你添加樣條的順序，因為這個順序在其他節點也會被考慮，例如[樣條](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color/scatter-on-spline-color.md) [上的散佈、樣條橋](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md)節點等。

## 輸入連接器

<b>預告 #1</b> *灰階*&#x200B;第一組輸入樣條曲線的預覽，作為灰階影像。

<b>樣條 #1 座標</b> *顏色*：第一組輸入樣條點的座標編碼在彩色影像的 RGBA 通道中。\
<b>R</b> - X 位置\
<b>G</b> - Y 位置\
<b>B</b> - 身高\
<b>A</b> - 打包資料：\
* 符號：樣條鍵為閉（負）或開（正）;\
* 絕對值：厚度 + 1。

<b>樣條線 #1 資料</b> *色彩*&#x200B;第一組輸入樣條的額外資料編碼在彩色影像的 RGBA 通道中。\
<b>R</b> - 切線 X\
<b>G</b> - 切線 Y\
<b>B</b> - 未上場\
<b>A</b> - 未上場

<b>樣條線 #1 量</b> *整數*：第一組輸入樣條的數量。

<b>預告 #2</b> *灰階*&#x200B;第二組輸入樣條線的預覽，作為灰階影像。

<b>樣條 #2 座標</b> *顏色*：第二組輸入樣條點的座標，編碼在彩色影像的RGBA通道中。\
<b>R</b> - X 位置\
<b>G</b> - Y 位置\
<b>B</b> - 身高\
<b>A</b> - 打包資料：\
* 符號：樣條鍵為閉（負）或開（正）;\
* 絕對值：厚度 + 1。

<b>樣條線 #2 資料</b> *顏色*&#x200B;第二組輸入樣條的額外資料編碼在彩色影像的 RGBA 通道中。\
<b>R</b> - 切線 X\
<b>G</b> - 切線 Y\
<b>B</b> - 未上場\
<b>A</b> - 未上場

<b>樣條 #2 量</b> *整數*&#x200B;第二組輸入樣條線的數量。

## 輸出連接器

<b>預覽</b> *灰階*&#x200B;輸出樣條的預覽作為灰階影像。

<b>樣條座標</b> *顏色*&#x200B;指編碼在彩色影像RGBA通道中的輸出樣條點座標。\
<b>R</b> - X 位置\
<b>G</b> - Y 位置\
<b>B</b> - 身高\
<b>A</b> - 打包資料：\
* 符號：樣條鍵為閉（負）或開（正）;\
* 絕對值：厚度 + 1。

<b>樣條資料</b> *色彩*&#x200B;輸出樣條的額外資料編碼於彩色影像的RGBA通道中。\
<b>R</b> - 切線 X\
<b>G</b> - 切線 Y\
<b>B</b> - 未上場\
<b>A</b> - 未上場

<b>樣條量</b> *整數*：輸出樣條的數量。

## 參數

<b>翻轉樣條 #1 方向 </b>*布林*&#x200B;將第一組樣條曲線的方向反轉。

<b>翻轉樣條線 #2 方向 </b>*布林*&#x200B;將第二組樣條曲線的方向反轉。

+++預覽
<b>分段數量</b> *整數*&#x200B;調整預覽輸出中繪製樣條曲線視覺化所使用的段數。\
數值越高，線條越平滑。

<b>節目指導助理</b> *布林值*&#x200B;在預覽輸出中會在樣條曲線的起始處顯示一個點，在末端顯示一個箭頭。

<b>顯示厚度包絡</b> *布林值*\
在樣鍵厚度邊緣顯示額外線條。

<b>厚度（px）</b> *浮點*&#x200B;調整預覽輸出中樣條曲線的厚度（像素數）。

+++

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![節點範例 1](../../../../../../assets/SplineAppend-Demo.jpg "節點範例 1")

</td>
<td style="border: 0;" valign="top">

![節點範例 2](../../../../../../assets/SplineAppend-Graph.jpg "節點範例 2")

</td>
</tr>
</table>

![節點示範](../../../../../../assets/SplineAppend-Demo2.gif "節點示範")
