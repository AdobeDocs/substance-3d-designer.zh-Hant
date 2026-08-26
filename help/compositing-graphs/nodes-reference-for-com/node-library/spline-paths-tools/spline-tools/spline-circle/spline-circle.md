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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---


# 樣條圈

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/spline-circle-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

產生一個圓形的單樣條曲線。

</td>
</tr>
</table>

## 輸入連接器

<b>預覽</b> *灰階*&#x200B;輸入樣條的預覽為灰階影像。

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

<b>圓半徑</b> *浮標*\
調整貼圖空間中圓的半徑。

<b>圓圈預旋轉</b> *浮標*\
在套用尺寸前，對底圈施加旋轉。

<b>圓圈大小</b> *Float2*\
調整圓的水平大小（X）與垂直大小（Y）。

<b>輪轉結束後的循環</b> *浮標*\
套用 Size 後，對底圈套用旋轉。

<b>圓圈位置</b> *Float2*\
設定圓心在貼圖空間中的位置。

<b>起始厚度</b> *浮動*&#x200B;調整圓圈起始點的厚度。\
此厚度沿樣條插值至端厚。\
注意：厚度是針對特定樣條節點使用的。

<b>端部厚度</b> *浮動*&#x200B;調整圓圈末端的厚度。\
此厚度沿樣條插值至起始厚度。\
注意：厚度是針對特定樣條節點使用的。

<b>起始高度</b> *浮動*&#x200B;調整圓圈起始點的高度，數值越低代表位置越低或越深。\
此高度沿樣條線插值至終點高度。

<b>端高度</b> *浮動*&#x200B;調整圓圈終點的高度，數值越低表示位置越低或越深。\
此高度是從起始高度沿樣條插值而來。

<b>飾邊</b> *Float2*&#x200B;將樣條曲線的起點和終點沿圓偏移。\
這些數值是正規化的。

<b>螺旋</b> *浮動*&#x200B;將圓的起點從半徑移到中心。\
接著將中心距離沿樣條線插值至樣條末端。\
這個值是正規化的。

<b>螺旋轉彎</b> *浮動*&#x200B;定義螺旋繞中心旋轉的次數。

<b>螺旋動力</b> *浮動*&#x200B;對繪製螺旋的中心距離施加力量曲線。\
值大於一表示螺旋中較大部分仍靠近中心。

<b>翻轉方向</b> *布林值*\
會反轉花鍵的方向。

<b>均勻分布</b> *布林值*\
當為真時，樣條曲線的點從起點到終點均勻分布。

<b>附加輸入樣條</b> *布林值*\
將產生的樣條曲線加入連接樣條</b>輸入的樣條<b>線清單末尾。

<b>非正方修正&#x200B;</b>*布林*：調整點的位置與厚度，以在非正方形解析度下保留樣條形狀。\
這也影響均勻分布。

+++預覽
<b>節目指導助理</b> *布林值*&#x200B;在預覽輸出中會在樣條曲線的起始處顯示一個點，在末端顯示一個箭頭。

<b>顯示厚度包絡</b> *布林值*\
在樣鍵厚度邊緣顯示額外線條。

<b>分段數量</b> *整數*&#x200B;調整預覽輸出中繪製樣條曲線視覺化所使用的段數。\
數值越高，線條越平滑。

<b>厚度（px）</b> *浮點*&#x200B;調整預覽輸出中樣條線視覺化的像素厚度。

+++

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![節點範例 1](../../../../../../assets/SplineCircle-Variant1.jpg "節點範例 1")

</td>
<td style="border: 0;" valign="top">

![節點範例 2](../../../../../../assets/SplineCircle-Demo.gif "節點範例 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![範例3](../../../../../../assets/SplineCircle-Variant2.jpg "範例3")

</td>
<td style="border: 0;" valign="top">

![範例4](../../../../../../assets/SplineCircle-Variant3.jpg "範例4")

</td>
</tr>
</table>
