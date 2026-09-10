---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-merge-list.html"
breadcrumb-title: ''
description: 使用 Spline Merge List 節點，將多個樣條線合併成單一樣條清單以進行合併操作。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Merge List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 樣條合併列表
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4ae20991693573dd44016a411c233b071fa96df6
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 1%

---


# 樣條合併列表

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](spline-merge-list.resources/spline-merge-list-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

將輸入清單中的所有樣條線合併成單一樣條線。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>樣條座標</b> <i>顏色</i> | 彩色影像RGBA通道中編碼的輸入樣條點座標：<br><b>R</b> - X 位置<br><b>G</b> - Y 位置<br><b>B</b> - 高度<br><b>A</b> - 打包資料：<br>- 符號：樣條線為閉合（負）或開（正）;<br>- 絕對值：厚度 + 1。 |
| <b>樣條資料</b> <i>顏色</i> | 彩色影像的 RGBA 通道中編碼的輸入樣條線額外資料。<br><b>R</b> - 切線 x<br><b>G</b> - 切線 y<br><b>B</b> - 未使用<br><b>A</b> - 未使用 |
| <b>樣條量</b> <i>整數</i> | 輸入樣條的數量。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>預覽</b> <i>灰階</i> | 合併後樣條線的灰階影像預覽。 |
| <b>樣條座標</b> <i>顏色</i> | 合併後樣條點的座標編碼在彩色影像的 RGBA 通道中。<br><b>R</b> - X 位置<br><b>G</b> - Y 位置<br><b>B</b> - 高度<br><b>A</b> - 打包資料：<br>- 符號：樣條為閉合（負）或開（正<br>）;- 絕對值：厚度 + 1。 |
| <b>樣條資料</b> <i>顏色</i> | 彩色影像 RGBA 通道中編碼的合併樣條線額外資料。<br><b>R</b> - 切線 x<br><b>G</b> - 切線 y<br><b>B</b> - 未使用<br><b>A</b> - 未使用 |
| <b>樣條量</b> <i>整數</i> | 合併樣條的數量。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>封閉樣條距離閾值</b> <i>浮標</i> | 紋理空間中，當同一樣條曲線的兩端被處理為一個收斂該樣條線的單點時，距離也算是。<br>這可避免在散射形狀或將影像映射到樣條曲線時產生重疊。 |
| <b>預覽</b> |  |
| <b>分段數量</b> <i>整數</i> | 調整預覽輸出中繪製樣條曲線視覺化所需的線段數。<br>數值越高，線條越平滑。 |
| <b>節目指導助理</b> <i>布林值</i> | 在預覽輸出中，樣條曲線起始顯示一個點，末尾顯示箭頭。 |
| <b>顯示厚度包絡</b> <i>布林值</i> | 在樣鍵厚度邊緣顯示額外線條。 |
| <b>厚度（px）</b> <i>浮標</i> | 調整預覽輸出中樣條曲線的厚度（像素數）。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-merge-list.resources/SplineMergeList-Variant2-Before.jpg" alt="SplineMergeList-變體2-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-merge-list.resources/SplineMergeList-Variant2-After.jpg" alt="SplineMergeList-變體2-之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-merge-list.resources/SplineMergeList-Variant1-Before.jpg" alt="SplineMergeList-variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-merge-list.resources/SplineMergeList-Variant1-After.jpg" alt="SplineMergeList-變體1-After">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![節點示範](spline-merge-list.resources/SplineMergeList-Demo.gif "節點示範")
