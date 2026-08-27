---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-2-splines.html"
breadcrumb-title: ''
description: 使用 Spline Bridge 節點來橋接兩個樣條線之間的紋理，創造無縫連接。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge (2 Splines)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 花鍵橋（2個花鍵）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 0%

---


# 花鍵橋（2個花鍵）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](spline-bridge-2-splines.resources/spline-bridge-2splines-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

從樣條曲線 #1</b> 到 <b>樣條曲線 #2</b> 生成樣條<b>曲線。產生的樣條可以是線性（直線）或三次貝茲曲線（曲面）。

</td>
</tr>
</table>

>[!IMPORTANT]
>
> 若提供給 <b>樣條線 #1</b> 與 <b>樣條線 #2</b> 輸入的資料包含多個樣條線，則僅使用每個清單中最後一個樣條線。

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>預告 #1</b> <i>灰階</i> | 輸入樣條線 #1 的灰階影像預覽。 |
| <b>樣條座標 #1</b> <i>顏色</i> | 輸入樣條點 #1 的座標編碼在彩色影像的 RGBA 通道中。<br><b>R</b> - X 位置<br><b>G</b> - Y 位置<br><b>B</b> - 高度<br><b>A</b> - 填充資料：<br>符號：樣條線為閉（負）或開（正）;<br>- 絕對值：厚度 + 1。 |
| <b>樣條資料 #1</b> <i>顏色</i> | 輸入樣條 #1 的額外資料編碼在彩色影像的 RGBA 通道中。<br><b>R</b> - 切線 x<br><b>G</b> - 切線 y<br><b>B</b> - 未使用<br><b>A</b> - 未使用 |
| <b>花鍵量 #1</b> <i>整數</i> | 輸入樣條的數量 #1。 |
| <b>預告 #2</b> <i>灰階</i> | 輸入樣條 #2 的灰階影像預覽。 |
| <b>樣條座標 #2</b> <i>顏色</i> | 彩色影像RGBA通道中編碼的輸入樣條#2點的座標。<br><b>R</b> - X 位置<br><b>G</b> - Y 位置<br><b>B</b> - 高度<br><b>A</b> - 填充資料：<br>符號：樣條線為閉合（負）或開（正）;<br>- 絕對值：厚度 + 1。 |
| <b>樣條資料 #2</b> <i>顏色</i> | 輸入樣條 #2 的額外資料編碼在彩色影像的 RGBA 通道中。<br><b>R</b> - 切線 x<br><b>G</b> - 切線 y<br><b>B</b> - 未使用<br><b>A</b> - 未使用 |
| <b>花鍵量 #2</b> <i>整數</i> | 輸入樣條的數量 #2。 |
| <b>起始切線長度曲線</b> <i>灰階</i> （當「橋式樣條類型」設定為「立方貝茲」時可用） | 描述曲線的圖像，利用其第一排像素的值。<br>此輸入用來控制每個樣條曲線 #1 起點的「出線」切線長度。<br>您可以使用曲線節點來撰寫曲線。 |
| <b>開始切線旋轉曲線</b> <i>灰階</i> （當「橋式樣條類型」設定為「立方貝茲」時可用） | 描述曲線的圖像，利用其第一排像素的值。<br>此輸入用來控制每個產生樣條曲線起點的「出」切線旋轉，該點為樣條曲線 #1。<br>影像的灰階值代表彎道數。<br>你可以用 Curve 節點來撰寫曲線。 |
| <b>端切長度曲線</b> <i>灰階</i> （當「橋式樣條類型」設定為「立方貝茲」時可用） | 描述曲線的圖像，利用其第一排像素的值。<br>此輸入用來控制每個樣條線在樣條線 #2 上終點的「內切線」長度。<br>你可以使用 Curve 節點來撰寫曲線。 |
| <b>端切旋轉曲線</b> <i>灰階</i> （當「橋式樣條類型」設定為「立方貝茲」時可用） | 描述曲線的圖像，利用其第一排像素的值。<br>此輸入用來控制每個樣條曲線末點的「內」切線旋轉，該線條沿樣條曲線 #2 的終點。<br>影像的灰階值代表彎角數。<br>你可以用 Curve 節點來撰寫曲線。 |

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
| <b>橋式樣條量</b> <i>整數</i> | 從樣條線 #1 到 樣條線 #2 產生的樣條數。 |
| <b>橋式樣鍵類型</b> <i>整數</i> | 所產生的樣條曲線類型：<br><br>- 線性樣條：從起點到結束的直線樣條;<br>- 三次貝茲曲線：從起點到終點的曲線樣條，曲線由起點與終點的長度與角度控制。 |
| <b>起始樣條 #1</b> <i>浮標</i> | 將樣條曲線 #1 上的位置偏移於樣條曲線產生的位置。 該值為樣條線 #1 的正規化長度。<br>值越高，樣條數越多，排列得更緊密。 |
| <b>起始樣條 #2</b> <i>浮標</i> | 將樣條曲線 #2 上的位置與樣條曲線產生的位置偏移。 該值為樣條線 #2 的正規化長度。<br>值越高，樣條數越多，樣條線的排列會更緊密。 |
| <b>端點樣條 #1</b> <i>浮標</i> | 偏移樣條線 #1 的位置直到樣條曲線產生位置。 該值為樣條線 #1 的正規化長度。<br>值越小，相同數量的樣條會被更緊密地堆疊在一起。 |
| <b>端點樣條 #1</b> <i>浮標</i> | 偏移樣條線 #2 的位置直到樣條曲線產生位置。 該值為樣條線 #2 的正規化長度。<br>值越小，相同數量的樣條會被更緊密地壓縮在一起。 |
| <b>偏移樣條 #1</b> <i>浮標</i> | 對 Spline #1 上所有樣條曲線的起點施加偏移。 該值為樣條線 #1 的正規化長度。<br>與樣條起點或結束點相交的樣條線會留在那裡。 |
| <b>偏移樣條 #2</b> <i>浮標</i> | 對 Spline #2 上所有樣條線的起點施加偏移。 該值為樣條線 #2 的正規化長度。<br>與樣條曲線起點或終點相交的樣條線會留在那裡。 |
| <b>偏移隨機起始</b> <i>浮標</i> | 對每個樣條線 #1 的起點施加隨機偏移。 該值為樣條線 #1 上樣條線間的正規化距離。<br>當保持 0 時，樣條曲線在起始樣條線 #1 與結束樣條線 #1 點間距均勻。 |
| <b>偏移隨機終點</b> <i>浮標</i> | 對樣條線 #2 上的每個樣條線的終點施加隨機偏移。 該值為樣條線 #2 上樣條線間的正規化距離。<br>當 0 時，樣條曲線在起始樣條線 #2 點與結束樣條線 #2 點之間均勻分布。 |
| <b>切線長度起始</b> <i>浮動（</i> 當「橋樑樣條類型」設為「立方貝茲」時可用） | 所有產生樣條線中，樣條線 #1 起點的「出」切線長度。 |
| <b>切線長度端</b> <i>浮動（</i> 當「橋樑樣條類型」設為「立方貝茲」時可用） | 所有產生樣條線 #2 端點的「內切線」長度。 |
| <b>切線旋轉起始</b> <i>浮動（</i> 當「橋樑樣條類型」設為「立方貝茲」時可用） | 所有產生的樣條線中，樣條線 #1 起點的「出」切線旋轉。<br>其數值為回合數。 |
| <b>切線旋轉端</b> <i>浮動（</i> 當「橋樑樣條類型」設為「立方貝茲」時可用） | 所有產生樣條線中，樣條線 #2 端點的「內」切線旋轉。<br>其數值為回合數。 |
| <b>預覽</b> |  |
| <b>分段數量</b> <i>整數</i> | 調整預覽輸出中繪製樣條視覺化所需的段數。 數值越高，線條越平滑。 |
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
      <img src="spline-bridge-2-splines.resources/SplineBridge-2Splines_Variant1-Before.jpg" alt="樣條橋-2Splines_Variant1-前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-bridge-2-splines.resources/SplineBridge-2Splines_Variant1-After.jpg" alt="花鍵橋2Splines_Variant1之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![節點範例 2](spline-bridge-2-splines.resources/SplineBridge-2Splines_Demo.gif "節點範例 2")

</td>
</tr>
</table>
