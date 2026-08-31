---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-select.html"
breadcrumb-title: ''
description: 使用 Spline Select 節點，根據圖中的樣條路徑選擇並遮罩特定區域。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 花鍵選擇
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---


# 花鍵選擇

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](spline-select.resources/spline-select-01.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

依照指定條件選擇輸入清單中的樣條線，並輸出包含所選樣條的新清單。

選取的樣條鍵也可以被裁剪。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>預覽</b> <i>灰階</i> | 輸入樣條線預覽為灰階影像。 |
| <b>樣條座標</b> <i>顏色</i> | 彩色影像RGBA通道中編碼的輸入樣條點座標：<br><b>R</b> - X 位置<br><b>G</b> - Y 位置<br><b>B</b> - 高度<br><b>A</b> - 打包資料：<br>- 符號：樣條線為閉合（負）或開（正）;<br>- 絕對值：厚度 + 1。 |
| <b>樣條資料</b> <i>顏色</i> | 彩色影像的 RGBA 通道中編碼的輸入樣條線額外資料。<br><b>R</b> - 切線 x<br><b>G</b> - 切線 y<br><b>B</b> - 未使用<br><b>A</b> - 未使用 |
| <b>樣條量</b> <i>整數</i> | 輸入樣條的數量。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>預覽</b> <i>灰階</i> | 輸出時條線預覽為灰階影像。 |
| <b>樣條座標</b> <i>顏色</i> | 彩色影像中編碼的輸出樣條點點座標。<br><b>R</b> - X 位置<br><b>G</b> - Y 位置<br><b>B</b> - 高度<br><b>A</b> - 打包資料：<br>- 符號：樣條線為閉合（負）或開（正）;<br>- 絕對值：厚度 + 1。 |
| <b>樣條資料</b> <i>顏色</i> | 彩色影像RGBA通道中編碼的輸出樣條額外資料。<br><b>R</b> - 切線 x<br><b>G</b> - 切線 y<br><b>B</b> - 未使用的<br><b>A</b> - 未使用的 |
| <b>樣條量</b> <i>整數</i> | 輸出花鍵的數量。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>選擇模式</b> <i>整數</i> | 選擇輸入清單中樣條線的方法：- 第一：選擇列表中的第一個樣條線;<br>- <i>最後</i>：選擇列表中最後一個樣條線;<br>- <i>索引</i>：選擇指定索引的樣條;<br>- <i>範圍</i>：選擇包含在指定範圍內的樣條。</i><i><br> |
| <b>樣條指數</b> <i>整數</i> | （當「選擇模式」設為「索引」時可用）應選擇的樣條曲線索引。 |
| <b>射程起始</b> <i>整數</i> | （當「選擇模式」設為「範圍」時可用）選取樣條範圍內的最低索引。 |
| <b>射程端</b> <i>整數</i> | （當「選擇模式」設為「範圍」時可用）選取樣條範圍內的最高索引。 |
| <b>開始</b> <i>浮標</i> | 偏移應該選擇樣條曲線部分的起始位置。 這實際上是修剪花鍵。<br>該值代表樣條的正規化長度。 |
| <b>結束</b> <i>浮標</i> | 偏移應該選擇的樣條曲線末端。 這實際上是修剪花鍵。<br>該值代表樣條的正規化長度。 |
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
      <img src="spline-select.resources/spline-select-02.jpg" alt="SplineSelect-變體1-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-select.resources/spline-select-03.jpg" alt="花條選擇-變體1-之後2">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-select.resources/spline-select-04.jpg" alt="SplineSelect-variant2-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-select.resources/spline-select-05.jpg" alt="SplineSelect-變體2-之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![節點範例 1](spline-select.resources/spline-select-06.gif "節點範例 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
