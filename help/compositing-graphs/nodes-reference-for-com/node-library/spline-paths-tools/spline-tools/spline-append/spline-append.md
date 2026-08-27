---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-append.html"
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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# 樣條附錄

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](spline-append.resources/spline-append-icon.png "節點圖示")

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

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>預告 #1</b> <i>灰階</i> | 第一組輸入樣條曲線預覽為灰階影像。 |
| <b>樣條 #1 座標</b> <i>顏色</i> | 第一組輸入樣條點的座標編碼在彩色影像的 RGBA 通道中。<br><b>R</b> - X 位置<br><b>G</b> - Y 位置<br><b>B</b> - 高度<br><b>A</b> - 填充資料：<br>符號：樣條線為閉合（負）或開（正）;<br>- 絕對值：厚度 + 1。 |
| <b>樣條線 #1 資料</b> <i>顏色</i> | 彩色影像RGBA通道中編碼的第一組輸入樣條的額外資料。<br><b>R</b> - 切線 x<br><b>G</b> - 切線 y<br><b>B</b> - 未使用<br><b>A</b> - 未使用 |
| <b>樣條線 #1 量</b> <i>整數</i> | 第一組輸入樣條的數量。 |
| <b>預告 #2</b> <i>灰階</i> | 第二組輸入樣條的預覽，作為灰階影像。 |
| <b>樣條 #2 座標</b> <i>顏色</i> | 第二組輸入樣條點的座標編碼在彩色影像的 RGBA 通道中。<br><b>R</b> - X 位置<br><b>G</b> - Y 位置<br><b>B</b> - 高度<br><b>A</b> - 填充資料：<br>符號：樣條線為閉合（負）或開（正）;<br>- 絕對值：厚度 + 1。 |
| <b>樣條線 #2 資料</b> <i>顏色</i> | 第二組輸入樣條的額外資料編碼在彩色影像的 RGBA 通道中。<br><b>R</b> - 切線 x<br><b>G</b> - 切線 y<br><b>B</b> - 未使用<br><b>A</b> - 未使用 |
| <b>樣條 #2 量</b> <i>整數</i> | 第二組輸入樣條的數量。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>預覽</b> <i>灰階</i> | 輸出時條線預覽為灰階影像。 |
| <b>樣條座標</b> <i>顏色</i> | 輸出樣條點的座標編碼在彩色影像的 RGBA 通道中。<br><b>R</b> - X 位置<br><b>G</b> - Y 位置<br><b>B</b> - 高度<br><b>A</b> - 打包資料：<br>符號：樣條線為閉合（負）或開（正）;<br>- 絕對值：厚度 + 1。 |
| <b>樣條資料</b> <i>顏色</i> | 彩色影像RGBA通道中編碼的輸出樣條額外資料。<br><b>R</b> - 切線 x<br><b>G</b> - 切線 y<br><b>B</b> - 未使用的<br><b>A</b> - 未使用的 |
| <b>樣條量</b> <i>整數</i> | 輸出花鍵的數量。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>翻轉樣鍵 #1 方向</b> <i>布林值</i> | 在第一組中，樣條曲線的方向會反轉。 |
| <b>翻轉樣鍵 #2 方向</b> <i>布林值</i> | 在第二組中，樣條曲線的方向會反轉。 |
| <b>預覽</b> |  |
| <b>分段數量</b> <i>整數</i> | 調整預覽輸出中繪製樣條視覺化所需的段數。 數值越高，線條越平滑。 |
| <b>節目指導助理</b> <i>布林值</i> | 在預覽輸出中，樣條曲線起始顯示一個點，末尾顯示箭頭。 |
| <b>顯示厚度包絡</b> <i>布林值</i> | 在樣鍵厚度邊緣顯示額外線條。 |
| <b>厚度（px）</b> <i>浮標</i> | 調整預覽輸出中樣條曲線的厚度（像素數）。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![節點範例 1](spline-append.resources/SplineAppend-Demo.jpg "節點範例 1")

</td>
<td style="border: 0;" valign="top">

![節點範例 2](spline-append.resources/SplineAppend-Graph.jpg "節點範例 2")

</td>
</tr>
</table>

![節點示範](spline-append.resources/SplineAppend-Demo2.gif "節點示範")
