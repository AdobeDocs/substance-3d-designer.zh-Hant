---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic.html"
breadcrumb-title: ''
description: 使用 Spline 多邊形二次節點來建立具有多個控制點的複雜二次樣條。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Poly Quadratic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 樣條（多方二次曲線）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4ae20991693573dd44016a411c233b071fa96df6
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---


# 樣條（多方二次曲線）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](spline-poly-quadratic.resources/spline-poly-quadratic-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

在多個點上產生樣條曲線。 這些點的數量和位置可以是任意的，也可以是從 [點列表](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md) 節點收集的。

</td>
</tr>
</table>

樣條的軌跡可以從其中間點平滑，因為每個中間點都是其鄰近切線「出」與「入」切線的交會點。

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>預覽</b> <i>灰階</i> | 輸入樣條線預覽為灰階影像。 |
| <b>樣條座標</b> <i>顏色</i> | 彩色影像RGBA通道中編碼的輸入樣條點座標：<br><b>R</b> - X 位置<br><b>G</b> - Y 位置<br><b>B</b> - 高度<br><b>A</b> - 打包資料：<br>- 符號：樣條線為閉合（負）或開（正）;<br>- 絕對值：厚度 + 1。 |
| <b>樣條資料</b> <i>顏色</i> | 彩色影像的 RGBA 通道中編碼的輸入樣條線額外資料。<br><b>R</b> - 切線 x<br><b>G</b> - 切線 y<br><b>B</b> - 未使用<br><b>A</b> - 未使用 |
| <b>樣條量</b> <i>整數</i> | 輸入樣條的數量。 |
| <b>積分預覽</b> <i>灰階</i> | 點預覽為灰階影像。 |
| <b>輸入點列表</b> <i>顏色</i> | （當「使用輸入點清單」為真時可用）彩色影像RGBA通道中編碼的點列表：<br><b>R</b> - X 位置<br><b>G</b> - Y 位置<br><b>B</b> - 高度<br><b>A</b> - 打包資料：<br>- 整數部分：平滑度;<br>- 分數部分：厚度。 |
| <b>點數</b> <i>整數</i> | （當「使用輸入點清單」為真時可用）點數。 |

>[!IMPORTANT]
>
> <b>點表<b></b>與點數</b>連接器&#x200B;*與花鍵</b>座標、<b>花鍵資料</b>及<b>花鍵數量</b>連接器不相容*<b>，因為它們依賴不同的資料。

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
| <b>積分金額</b> <i>整數</i> | 用來製作樣條鍵所使用的任意點數。 |
| <b>輸入樣條鍵連接模式</b> <i>整數</i> | 連接輸入樣條鍵的方法：<br>- 自動：</i>最後一個輸入樣條的末端連接到產生樣條的起點，產生樣條的末端連接第一個輸入樣條的起點;<br>- <i>手動：</i>你可以指定哪些輸入樣條應連接到產生樣條的兩端，以及這些連接應該落在輸入樣條的<i>哪個位置。 |
| <b>閉合樣鍵</b> <i>布林值</i> | 控制樣條的終點是否應該連接到起點。<br>樣條曲線在起點與終點施加的平滑度由這些點的平滑度值決定。 |
| <b>翻轉方向</b> <i>布林值</i> | 會反轉花鍵的方向。 |
| <b>使用 Input Point List</b> <i>布林值</i> | 使用輸入點列表與點號輸入連接器所提供的點列表，而非任意的點列表。<br>點列表可由 [點列表](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md) 節點提供。 |
| <b>連接起始與輸入樣條鍵</b> <i>布林值</i> | 當 True（為真）時，產生樣條線的起始點會連接到輸入樣條中最後一個樣條的最後一個點。 |
| <b>起始連接樣條索引</b> <i>整數</i> | （當「輸入花鍵連接模式」設為「手動」且「連接起始至輸入花鍵」設為「真」時可用）輸入花鍵的索引，應連接至產生樣條的起始點。 |
| <b>開始連線位置</b> <i>浮標</i> | （當「輸入花鍵連接模式」設為「手動」且「連接起始至輸入花鍵」設為「真」時可用）在所選輸入花鍵上，連接至產生樣條起點的位置。<br>此值即為所選輸入樣條線的正規化長度。 |
| <b>將端點連接到輸入花鍵</b> <i>布林值</i> | 當為 True（真）時，產生樣條線的端點會連接到輸入樣條中第一個樣條線的第一點。 |
| <b>端點連接樣條索引</b> <i>整數</i> | （當「輸入樣條線連接模式」設為「手動」且「連接端點到輸入樣條線」設為「真」時可用）輸入樣條曲線的索引，應連接到產生樣條線的末端。 |
| <b>結束連接位置</b> <i>浮標</i> | （當「輸入花鍵連接模式」設為「手動」且「連接端點到輸入花鍵」設為「真」時可用）選擇輸入花鍵上連接點的位置，該花鍵應落在該端點。<br>此值即為所選輸入樣條線的正規化長度。 |
| <b>均勻分布</b> <i>布林值</i> | 當為真時，樣條曲線的點從起點到終點均勻分布。 |
| <b>附加輸入樣條</b> <i>布林值</i> | 將產生的樣條曲線加入連接樣條</b>輸入的樣條<b>線清單末尾。 |
| <b>非平方修正</b> <i>布林值</i> | 調整點的位置與厚度，以在非正方形解析度下保留樣條形狀。<br>這也影響均勻分布。 |
| <b>全域平滑度調整</b> <i>浮標</i> | 對所有點的平滑值施加均勻偏移。<br>所得的平滑度值會被夾在[0;1] 範圍內。 |
| <b>點的性質</b> |  |
| <b>p# 性質</b> <i>Float3</i> | 設定 p# 點的性質。<br>- 高度：</i>調整點的高度，當值越低代表位置越低或越深;<br>- <i>平滑度：</i>偏移樣條曲線在 p# 平滑起點的起點，值為 0 時為硬軌跡，在完全光滑軌跡中為 1;<br>- <i>厚度：</i>調整樣鍵在 p# <i>處的厚度。厚度則由特定的樣條節點使用。 |
| <b>點座標</b> |  |
| <b>p#</b> <i>Float2</i> | 設定 p# 點在貼圖空間中的位置。 |
| <b>預覽</b> |  |
| <b>節目旁線</b> <i>布林值</i> | 在預覽輸出中顯示 p1 和 p3 指向 p2 的切線。 |
| <b>節目指導助理</b> <i>布林值</i> | 在預覽輸出中，樣條曲線起始顯示一個點，末尾顯示箭頭。 |
| <b>顯示厚度包絡</b> <i>布林值</i> | 在樣鍵厚度邊緣顯示額外線條。 |
| <b>Show Points 標籤</b> <i>布林值</i> | 對於每個點，會在「預覽」輸出中旁邊顯示該點的名稱。 |
| <b>點標籤大小</b> <i>浮標</i> | （當「顯示點標籤」設為「True」時可用）貼圖空間中每個點的標籤大小，0.1 是貼圖寬度的十分之一。 |
| <b>節目重點</b> <i>布林值</i> | 顯示花鍵的控制點。 |
| <b>積分大小</b> <i>浮標</i> | （當「顯示點」設為「True」時可用）貼圖空間中點的半徑，0.1 是貼圖寬度的十分之一。 |
| <b>分段數量</b> <i>整數</i> | 調整預覽輸出中繪製樣條曲線視覺化所需的線段數。<br>數值越高，線條越平滑。 |
| <b>厚度（px）</b> <i>浮標</i> | 調整預覽輸出中樣條曲線的厚度（像素數）。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-poly-quadratic.resources/SplinePolyQuadratic-Variant1-Before.jpg" alt="樣條多二次變體1-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-poly-quadratic.resources/SplinePolyQuadratic-Variant1-After.jpg" alt="樣條多二次變體1-之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![節點範例 2](spline-poly-quadratic.resources/SplinePolyQuadratic-Demo.gif "節點範例 2")

</td>
</tr>
</table>
