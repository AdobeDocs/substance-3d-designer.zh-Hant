---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-warp.html"
breadcrumb-title: ''
description: 使用 Spline Warp 節點沿著樣條路徑扭曲材質，創造曲線和有機圖案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 樣條曲
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1135'
ht-degree: 0%

---


# 樣條曲

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](spline-warp.resources/spline-warp-01.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據輸入的強度貼圖或向量貼圖來位移輸入樣條。

扭曲效應的強度可透過衰減控制沿樣條調整。

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
| <b>強度圖</b> <i>灰階</i> | （當「Use Vector Map」設定為「False」時可用）輸入灰階影像用於控制輸入樣條變形效果的方向與強度。<br>影像中每個像素的顏色指定一個乘數，用於將樣條線點沿法線（即垂直於樣條的方向）位移，範圍可達整個影像的跨度。<br>影像中的[0;1]值在以乘法方式讀取時會重新映射到[-1;1]範圍：0和1會使樣條鍵移動相同距離但方向相反。 0.5 則保留花鍵。 |
| <b>向量地圖</b> <i>灰階</i> | （當「Use Vector Map」設為「True」時可用）輸入色彩影像用於控制輸入樣條變形效果的方向與強度。<br>影像中每個像素的顏色指定向量（X， Y），該向量編碼在紅色（X）和綠色（Y）通道中。 +X 是對的，+Y 是下。<br>影像中的[0;1]值在向量座標讀取時會重新映射到[-1;1]範圍：0 紅色移位左點，0 綠色移位向上點。 0.5 的紅綠則保留花鍵原位。 |
| <b>衰減曲線</b> <i>灰階</i> | 描述曲線的圖像，利用其第一排像素的值。<br>當「使用衰減曲線」參數設為 True（真）時，此輸入用來控制樣條曲線起始與結束處的扭曲效應衰減。<br>曲線提供了衰減的輪廓，列中的第一個像素代表樣條起始處的扭曲強度，最後一個像素為末端的強度。 灰階值代表強度。<br>你可以用 Curve 節點來撰寫曲線。 |

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
| <b>曲速強度</b> <i>浮標</i> | 樣條位移的強度。 |
| <b>曲速中心</b> <i>浮標</i> | 指定強度映射值，對應於樣條曲線保持原位。<br>值為 0 或 1 表示樣條曲線只能在一側位移。 |
| <b>取樣模式</b> <i>整數</i> | 將強度貼圖或向量貼圖中的值映射到樣條的方法：<br>- <i>貼圖空間</i>：這些值會套用到貼圖中若依照貼圖的 UV 座標放置時，該位置會被套用到樣條曲線上。 這實際上將值套用到「原位」的樣條曲線上;<br>- <i>沿樣條</i>線水平：這些值直接套用到編碼的樣條的座標（參見樣條座標輸入），每列從上到下分別套用到不同的樣條曲線;<br>- <i>Hor. 沿樣條曲線（蘭德。 偏移量 X）：</i>這些值直接套用到編碼後樣條的座標上（參見樣條座標輸入），每個樣條曲線（即樣條座標的每一列）在縮放映射中隨機進行水平偏移;<br>- <i>Hor。 沿樣條曲線（蘭德。 偏移 Y）：</i>這些值直接套用到編碼後樣條的座標（參見樣條座標輸入），每個樣條曲線（即樣條座標中的每一列）在縮放映射中隨機垂直偏移。 |
| <b>使用向量地圖</b> <i>布林值</i> | 將樣條的位移方法改為使用向量映射輸入來指定位移方向。<br>影像中每個像素的顏色指定向量（X， Y），該向量編碼在紅色（X）和綠色（Y）通道中。 +X 是對的，+Y 是下。<br>影像中的[0;1]值在向量座標讀取時會重新映射到[-1;1]範圍：0 紅色移位左點，0 綠色移位向上點。 0.5 的紅綠則保留花鍵原位。 |
| <b>使用衰減曲線</b> <i>布林值</i> | 可利用衰減曲線輸入影像編碼的曲線，控制樣條曲線上的扭曲效應強度。 |
| <b>強度圖平鋪</b> <i>浮標</i> | （當「取樣模式」未設為「貼圖空間」時可用）當強度貼圖直接映射到樣條座標時，可調整其平鋪（參見樣條座標輸入）。 |
| <b>起始衰減</b> <i>浮標</i> | （當「使用衰減曲線」設為「假」時可用）一個乘數，表示樣條起始處的扭曲效應衰減。<br>值為 1 表示樣條起始處不會施加扭曲。 |
| <b>衰減結束</b> <i>浮標</i> | （當「使用衰減曲線」設為「假」時可用）一個乘數，表示樣條末端的扭曲效應衰減。<br>值為 1 表示樣條末端不會施加扭曲。 |
| <b>重新計算切線</b> <i>布林值</i> | 當為真時，樣條的切線會在套用扭曲效應後重新計算。<br>這確保樣條線的切線在如散佈於樣條線或樣條流映射器等節點中使用時，與其軌跡保持一致。 |
| <b>預覽</b> |  |
| <b>分段數量</b> <i>整數</i> | 調整預覽輸出中繪製樣條曲線視覺化所需的線段數。<br>數值越高，線條越平滑。 |
| <b>節目指導助理</b> <i>布林值</i> | 在預覽輸出中，樣條曲線起始顯示一個點，末尾顯示箭頭。 |
| <b>顯示厚度包絡</b> <i>布林值</i> | 在樣鍵厚度邊緣顯示額外線條。 |
| <b>厚度（px）</b> <i>浮標</i> | 調整預覽輸出中樣條曲線的厚度（像素數）。 |
| <b>背景預覽強度</b> <i>浮標</i> | 該值與背景預覽輸入影像相乘。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-warp.resources/spline-warp-02.jpg" alt="SplineWarp-變體1-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-warp.resources/spline-warp-03.jpg" alt="樣條曲速-變體1-之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-warp.resources/spline-warp-04.jpg" alt="SplineWarp-變體2-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-warp.resources/spline-warp-05.jpg" alt="SplineWarp-變體2-之後">
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

![節點範例 1](spline-warp.resources/spline-warp-06.gif "節點範例 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
