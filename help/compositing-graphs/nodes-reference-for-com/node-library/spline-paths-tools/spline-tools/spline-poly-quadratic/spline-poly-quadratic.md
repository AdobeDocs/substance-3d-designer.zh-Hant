---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic.html"
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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1147'
ht-degree: 0%

---


# 樣條（多方二次曲線）

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/spline-poly-quadratic-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

在多個點上產生樣條曲線。 這些點的數量和位置可以是任意的，也可以是從 [點列表](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md) 節點收集的。

</td>
</tr>
</table>

樣條的軌跡可以從其中間點平滑，因為每個中間點都是其鄰近切線「出」與「入」切線的交會點。

## 輸入連接器

<b>預覽</b> *灰階*&#x200B;輸入樣條的預覽為灰階影像。

<b>樣條座標</b> *色彩*&#x200B;輸入樣條點的座標編碼在彩色影像的 RGBA 通道中：\
<b>    R</b> - X 位置\
<b>    G</b> - Y 位置\
<b>    B</b> - 身高\
<b>    A</b> - 打包資料：\
* 符號：樣條鍵為閉（負）或開（正）;\
* 絕對值：厚度 + 1。

<b>樣條資料</b> *色彩*&#x200B;輸入樣條的額外資料編碼於彩色影像的 RGBA 通道中。\
<b>    R</b> - 切線 X\
<b>    G</b> - 切線 Y\
<b>    B</b> - 未上場\
<b>    A</b> - 未上場

<b>樣條量</b> *整數*：輸入樣條的數量。

<b>點預覽&#x200B;</b>*灰階*&#x200B;點以灰階影像預覽。

<b>輸入點列表</b> *顏色* （當「使用輸入點清單」為真時可用）\
彩色影像RGBA通道中編碼的點列表：\
<b>R</b> - X 位置\
<b>G</b> - Y 位置\
<b>B</b> - 身高\
<b>A</b> - 打包資料：\
* 整數部分：平滑度;\
* 分數部分：厚度。

<b>點數</b> *整數* （當「使用輸入點清單」為真時可用）\
分數。

>[!IMPORTANT]
>
> <b>點表<b></b>與點數</b>連接器&#x200B;*與花鍵</b>座標、<b>花鍵資料</b>及<b>花鍵數量</b>連接器不相容*<b>，因為它們依賴不同的資料。

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

<b>積分金額</b> *整數*&#x200B;用於構建樣條的任意點數。

<b>輸入樣條鍵連接模式</b> *整數*&#x200B;連接輸入樣條的方法：\
*- 自動：* 最後一個輸入樣條的末端連接至產生樣條的起始點，產生樣條的末端連接至第一個輸入樣條的起始點;\
*- 手動：* 你可以指定哪些輸入樣條曲線應該連接到產生樣條的兩端，以及這些連接應該落在輸入樣條的哪個位置。

<b>閉合樣鍵</b> *布林值*&#x200B;控制樣條曲線的端點是否應該連接到起點。\
樣條曲線在起點與終點施加的平滑度由這些點的平滑度值決定。

<b>翻轉方向</b> *布林值*\
會反轉花鍵的方向。

<b>使用 Input Point List</b> *布林運算*：使用輸入點列表與點號輸入連接器所提供的點清單，而非任意的點列表。\
點列表可由 [點列表](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md) 節點提供。

<b>連接起始與輸入樣條鍵</b> *布林值*&#x200B;當 True，產生的樣條曲線的起點會連接到輸入樣條中最後一個樣條線的最後一點。

<b>起始連接樣條索引</b> *整數* （當「輸入樣條線連接模式」設為「手動」且「連接起始到輸入樣條線」設為「真實」時可用）輸入樣條曲線的索引，應連接到產生樣條的起始點。

<b>開始連線位置</b> *浮點* （當「輸入樣條線連接模式」設為「手動」且「連接起點到輸入樣條鍵」設為「真」時可用）選擇輸入樣條鍵上連接起點應落點的位置。\
此值即為所選輸入樣條線的正規化長度。

<b>將端點連接到輸入花鍵</b> *布林當*&#x200B;為真時，產生的樣條線末端會連接到輸入樣條中第一個樣條線的第一點。

<b>端點連接樣條索引</b> *整數* （當「輸入樣條線連接模式」設為「手動」且「連接端點到輸入樣條線」設為「真」時可用）輸入樣條曲線的索引，應連接到產生樣條的端點。

<b>結束連接位置</b> *浮點* （當「輸入樣條線連接模式」設為「手動」且「連接端點到輸入樣條鍵」設為「真」時可用）在所選輸入樣條鍵上，產生樣條曲線應該落點的連接點位置。\
此值即為所選輸入樣條線的正規化長度。

<b>均勻分布</b> *布林值*\
當為真時，樣條曲線的點從起點到終點均勻分布。

<b>附加輸入樣條</b> *布林值*\
將產生的樣條曲線加入連接樣條</b>輸入的樣條<b>線清單末尾。

<b>非正方修正&#x200B;</b>*布林*：調整點的位置與厚度，以在非正方形解析度下保留樣條形狀。\
這也影響均勻分布。

<b>全域平滑度調整</b> *浮點*&#x200B;對所有點的平滑值施加均勻偏移。\
所得的平滑度值會被夾在[0;1] 範圍內。

+++點的性質
<b>p# 性質</b> *Float3*&#x200B;設定 p# 點的屬性。\
*- 高度：* 調整點的高度，當較低值代表較低或較深的位置時;\
*- 平滑性：* 偏移樣條平滑起點的 p#，值為 0 時產生硬軌跡，1 則為完全平滑軌跡;\
*- 厚度：* 調整 p# 處樣鍵的厚度。 厚度則由特定的樣條節點使用。

+++

+++點座標
<b>p#</b> *Float2*&#x200B;設定 p# 點在貼圖空間中的位置。

+++

+++預覽
<b>節目旁線</b> *布林值*&#x200B;在預覽輸出中顯示 p1 和 p3 點到 p2 的切線。

<b>節目指導助理</b> *布林值*&#x200B;在預覽輸出中會在樣條曲線的起始處顯示一個點，在末端顯示一個箭頭。

<b>顯示厚度包絡</b> *布林值*\
在樣鍵厚度邊緣顯示額外線條。

<b>Show Points 標籤</b> *布林值*\
對於每個點，會在「預覽」輸出中旁邊顯示該點的名稱。

<b>點標籤大小</b> *浮點* （當「顯示點數標籤」設為「真實」時可用）\
貼圖空間中每個點的標籤大小，0.1 是貼圖寬度的十分之一。

<b>節目重點</b> *布林值*\
顯示花鍵的控制點。

<b>積分大小</b> *浮動（* 當「顯示點數」設為「真實」時可用）\
貼圖空間中點的半徑，0.1 是貼圖寬度的十分之一。

<b>分段數量</b> *整數*&#x200B;調整預覽輸出中繪製樣條曲線視覺化所使用的段數。\
數值越高，線條越平滑。

<b>厚度（px）</b> *浮點*&#x200B;調整預覽輸出中樣條曲線的厚度（像素數）。

+++

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplinePolyQuadratic-Variant1-Before.jpg" alt="樣條多二次變體1-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplinePolyQuadratic-Variant1-After.jpg" alt="樣條多二次變體1-之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![節點範例 2](../../../../../../assets/SplinePolyQuadratic-Demo.gif "節點範例 2")

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
