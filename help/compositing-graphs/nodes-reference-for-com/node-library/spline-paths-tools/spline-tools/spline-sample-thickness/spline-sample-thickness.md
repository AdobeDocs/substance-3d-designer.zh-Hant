---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-sample-thickness.html"
breadcrumb-title: ''
description: 使用樣條取樣厚度節點，沿著樣條線取樣厚度值以產生程序效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Sample Thickness
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 樣鍵樣本厚度
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---


# 樣鍵樣本厚度

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](spline-sample-thickness.resources/spline-sample-thickness-01.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

透過將輸入的厚度貼圖映射到輸入樣條上來修改其厚度。

映射高度圖的效果可以透過改變混合模式及效果的不透明度來調整。

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
| <b>厚度圖</b> <i>灰階</i> | 輸入的灰階影像用來改變輸入樣條曲線的厚度。 |

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
| <b>取樣模式</b> <i>整數</i> | 將厚度貼圖中的值映射到樣條曲線的方法：<br>- <i>紋理空間</i>：這些值會套用到樣條曲線上，若使用貼圖的 UV 座標放置，則在貼圖中放置時會放置的位置。 這實際上將值套用到「原位」的樣條曲線上;<br>- <i>沿樣條</i>線水平：這些值直接套用到編碼的樣條的座標（參見樣條座標輸入），每列從上到下分別套用到不同的樣條曲線;<br>- <i>Hor. 沿樣條曲線（蘭德。 偏移量 X）：</i>這些值直接套用到編碼後樣條的座標上（參見樣條座標輸入），每個樣條曲線（即樣條座標的每一列）在縮放映射中隨機進行水平偏移;<br>- <i>Hor。 沿樣條曲線（蘭德。 偏移 Y）：</i>這些值直接套用到編碼後樣條的座標（參見樣條座標輸入），每個樣條曲線（即樣條座標中的每一列）在縮放映射中隨機垂直偏移。 |
| <b>不透明度</b> <i>浮標</i> | 一個乘數，表示厚度圖輸入對樣條厚度的貢獻強度。 |
| <b>混合模式</b> <i>整數</i> | 將厚度貼圖資料與輸入樣條曲線 <span id="_Hlk135820484"></span>厚度混合的方法：<br>- <i>複製</i>：用 Height Map 值覆蓋樣條曲線的厚度;<br>- <i>加法</i>：將厚度映射值加到樣條曲線的厚度上;<br>- <i>減法</i>：將厚度映射值減去樣條曲線的厚度;<br>- <i>乘法</i>：將厚度映射值與樣條曲線的厚度相乘。 |
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
      <img src="spline-sample-thickness.resources/spline-sample-thickness-02.jpg" alt="SplineSampleThickness-變體1-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-sample-thickness.resources/spline-sample-thickness-03.jpg" alt="樣條樣本厚度變體1-之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-sample-thickness.resources/spline-sample-thickness-04.jpg" alt="SplineSampleThickness-變體2-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-sample-thickness.resources/spline-sample-thickness-05.jpg" alt="樣條樣本厚度變體2-之後">
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

![節點範例 1](spline-sample-thickness.resources/spline-sample-thickness-06.jpg "節點範例 1")

</td>
<td style="border: 0;" valign="top">

![節點範例 2](spline-sample-thickness.resources/spline-sample-thickness-07.gif "節點範例 2")

</td>
</tr>
</table>
