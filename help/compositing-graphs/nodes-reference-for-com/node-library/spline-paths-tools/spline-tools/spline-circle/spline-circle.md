---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-circle.html"
breadcrumb-title: ''
description: 使用樣條圈節點來建立圓形樣條，產生圓形圖案和形狀。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Circle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 樣條圈
user-guide-description: ''
user-guide-title: ''
source-git-commit: 86e504c9dfe76516c56a7950f0bf70090270a60c
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---


# 樣條圈

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](spline-circle.resources/spline-circle-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

產生一個圓形的單樣條曲線。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>預覽</b> <i>灰階</i> | 輸入樣條線預覽為灰階影像。 |
| <b>樣條座標</b> <i>顏色</i> | 彩色影像RGBA通道中編碼的輸入樣條點座標：<br><b>R</b> - X 位置<br><b>G</b> - Y 位置<br><b>B</b> - 高度<br><b>A</b> - 填充資料：<br>符號：樣條線為閉合（負）或開（正）;<br>- 絕對值：厚度 + 1。 |
| <b>樣條資料</b> <i>顏色</i> | 彩色影像的 RGBA 通道中編碼的輸入樣條線額外資料。<br><b>R</b> - 切線 x<br><b>G</b> - 切線 y<br><b>B</b> - 未使用<br><b>A</b> - 未使用 |
| <b>樣條量</b> <i>整數</i> | 輸入樣條的數量。 |

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
| <b>圓半徑</b> <i>浮標</i> | 調整貼圖空間中圓的半徑。 |
| <b>圓圈預旋轉</b> <i>浮標</i> | 在套用尺寸前，對底圈施加旋轉。 |
| <b>圓圈大小</b> <i>Float2</i> | 調整圓的水平大小（X）與垂直大小（Y）。 |
| <b>輪轉結束後的循環</b> <i>浮標</i> | 套用 Size 後，對底圈套用旋轉。 |
| <b>圓圈位置</b> <i>Float2</i> | 設定圓心在貼圖空間中的位置。 |
| <b>起始厚度</b> <i>浮標</i> | 調整圓圈起始點的厚度。 此厚度沿樣條插值至端厚。<br>注意：厚度用於特定樣條節點。 |
| <b>端部厚度</b> <i>浮標</i> | 調整圓頂點的厚度。 此厚度沿樣條插值至起始厚度。<br>注意：厚度用於特定樣條節點。 |
| <b>起始高度</b> <i>浮標</i> | 調整圓圈起始點的高度，數值越低代表位置越低或越深。 此高度沿樣條線插值至終點高度。 |
| <b>端高度</b> <i>浮標</i> | 調整圓圈終點的高度，數值越低代表位置越低或越深。 此高度是從起始高度沿樣條插值而來。 |
| <b>飾邊</b> <i>Float2</i> | 偏移樣條曲線的起點與終點沿圓。 這些數值是正規化的。 |
| <b>螺旋</b> <i>浮標</i> | 將圓的起點從半徑移到中心。 接著將中心距離沿樣條線插值至樣條末端。 這個值是正規化的。 |
| <b>螺旋轉彎</b> <i>浮標</i> | 定義螺旋繞中心的轉彎次數。 |
| <b>螺旋動力</b> <i>浮標</i> | 對繪製螺旋線所用的中心距離施加冪次曲線。 值大於一表示螺旋中較大部分仍靠近中心。 |
| <b>翻轉方向</b> <i>布林值</i> | 會反轉花鍵的方向。 |
| <b>均勻分布</b> <i>布林值</i> | 當為真時，樣條曲線的點從起點到終點均勻分布。 |
| <b>附加輸入樣條</b> <i>布林值</i> | 將產生的樣條曲線加入連接樣條</b>輸入的樣條<b>線清單末尾。 |
| <b>非平方修正</b> <i>布林值</i> | 調整點的位置與厚度，以在非正方形解析度下保留樣條形狀。 這也影響均勻分布。 |
| <b>預覽</b> |  |
| <b>節目指導助理</b> <i>布林值</i> | 在預覽輸出中，樣條曲線起始顯示一個點，末尾顯示箭頭。 |
| <b>顯示厚度包絡</b> <i>布林值</i> | 在樣鍵厚度邊緣顯示額外線條。 |
| <b>分段數量</b> <i>整數</i> | 調整預覽輸出中繪製樣條視覺化所需的段數。 數值越高，線條越平滑。 |
| <b>厚度（px）</b> <i>浮標</i> | 調整預覽輸出中樣條曲線的像素厚度。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![節點範例 1](spline-circle.resources/SplineCircle-Variant1.jpg "節點範例 1")

</td>
<td style="border: 0;" valign="top">

![節點範例 2](spline-circle.resources/SplineCircle-Demo.gif "節點範例 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![範例3](spline-circle.resources/SplineCircle-Variant2.jpg "範例3")

</td>
<td style="border: 0;" valign="top">

![範例4](spline-circle.resources/SplineCircle-Variant3.jpg "範例4")

</td>
</tr>
</table>
