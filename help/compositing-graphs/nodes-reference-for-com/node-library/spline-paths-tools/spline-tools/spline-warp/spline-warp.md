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
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 0%

---


# 樣條曲

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/spline-warp-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據輸入的強度貼圖或向量貼圖來位移輸入樣條。

扭曲效應的強度可透過衰減控制沿樣條調整。

</td>
</tr>
</table>

## 輸入連接器

<b>預覽</b> *灰階*&#x200B;輸入樣條的預覽為灰階影像。

<b>樣條座標</b> *色彩*&#x200B;輸入樣條點的座標編碼在彩色影像的 RGBA 通道中：\
<b>R</b> - X 位置\
<b>G</b> - Y 位置\
<b>B</b> - 身高\
    <b>A</b> - 打包資料：\
* 符號：樣條鍵為閉（負）或開（正）;\
* 絕對值：厚度 + 1。

<b>樣條資料</b> *色彩*&#x200B;輸入樣條的額外資料編碼於彩色影像的 RGBA 通道中。\
<b>R</b> - 切線 X\
<b>G</b> - 切線 Y\
<b>B</b> - 未上場\
<b>A</b> - 未上場

<b>樣條量</b> *整數*：輸入樣條的數量。

<b>強度圖</b> *灰階* （當「Use Vector Map」設定為「False」時可用）\
輸入灰階影像用來控制輸入樣條曲線的扭曲方向與強度。\
影像中每個像素的顏色指定一個乘數，用於將樣條線點沿法線（即垂直於樣條的方向）位移，範圍可達整個影像的跨度。\
影像中的[0;1]值在以乘法方式讀取時會重新映射到[-1;1]範圍：0和1會使樣條鍵移動相同距離但方向相反。 0.5 則保留花鍵。

<b>向量地圖</b> *灰階* （當「Use Vector Map」設定為「True」時可用）輸入彩色影像，用來控制輸入樣條扭曲效果的方向與強度。\
影像中每個像素的顏色指定向量（X， Y），該向量編碼在紅色（X）和綠色（Y）通道中。 +X 是對的，+Y 是下。\
影像中的[0;1]值在向量座標讀取時會重新映射到[-1;1]範圍：0 紅色移位左點，0 綠色移位向上點。 0.5 的紅綠則保留花鍵原位。

<b>衰減曲線</b> *灰階*&#x200B;描述曲線的影像，使用第一排像素的值。\
當「使用衰減曲線」參數設為 True（真）時，此輸入用來控制樣條曲線起始與結束處的扭曲效應衰減。\
曲線提供了衰減的輪廓，列中的第一個像素代表樣條起始處的扭曲強度，最後一個像素為末端的強度。 灰階值代表強度。\
你可以用 Curve 節點來撰寫曲線。

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

<b>曲速強度</b> *浮點*&#x200B;指樣鍵位移的強度。

<b>曲速中心</b> *Float*&#x200B;指定強度圖值，對應於保留樣條線的位置。\
值為 0 或 1 則表示樣條曲線只能在一側位移。

<b>取樣模式</b> *整數*&#x200B;將強度映射或向量映射中的值映射到樣條的方法：\
*- 貼圖空間*：這些值會套用到樣條（spline）上，若使用貼圖的 UV 座標放置於貼圖中，該點樣條會放在的位置。 這實際上將值套用到「已就位」的樣條曲線上;\
*- 水平沿樣條線*：數值直接套用到編碼的樣條座標（參見樣條座標輸入），每列從上到下分別套用到不同的樣條曲線;\
*- 霍爾。 沿樣條曲線（蘭德。 偏移量 X）：*&#x200B;這些值直接套用到編碼後樣條的座標（參見樣條座標輸入），每個樣條曲線（即樣條座標中的每一列）在縮放映射中隨機進行水平偏移;\
*- 霍爾。 沿樣條曲線（蘭德。 偏移 Y）：*&#x200B;這些值直接套用到編碼後樣條的座標（參見樣條座標輸入），每個樣條曲線（即樣條座標中的每一列）在縮放映射中隨機垂直偏移。

<b>使用向量地圖</b> *布林*&#x200B;切換將位移樣條的方法轉為使用向量映射輸入來指定位移方向。\
影像中每個像素的顏色指定向量（X， Y），該向量編碼在紅色（X）和綠色（Y）通道中。 +X 是對的，+Y 是下。\
影像中的[0;1]值在向量座標讀取時會重新映射到[-1;1]範圍：0 紅色移位左點，0 綠色移位向上點。 0.5 的紅綠則保留花鍵原位。

<b>使用衰減曲線</b> *布林運算*&#x200B;允許利用編碼在衰減曲線輸入影像中的曲線，控制沿樣條曲線的扭曲效應強度。<b></b>

<b>強度圖平鋪</b> *浮動* （當「取樣模式」未設定為「貼圖空間」時可用）當強度貼圖直接映射到樣條座標時，調整其鋪砌（參見樣條座標輸入）。<b></b>

<b>起始衰減</b> *浮點* （當「使用衰減曲線」設定為「假」時可用）一種乘數，用於樣條曲線起始附近扭曲效應的衰減。\
值為 1 表示樣條起始處不會發生變形。

<b>衰減結束</b> *浮點* （當「使用衰減曲線」設定為「假」時可用）一種乘數，用於樣條末端扭曲效應的衰減。\
值為 1 表示樣條末端不會發生變形。<b></b>

<b>重新計算切線</b> *布林*&#x200B;當 True 時，樣條曲線的切線在套用扭曲效應後會重新計算。\
這確保樣條線的切線在如散佈於樣條線或樣條流映射器等節點中使用時，與其軌跡保持一致。

+++預覽
<b>分段數量</b> *整數*&#x200B;調整預覽輸出中繪製樣條曲線視覺化所使用的段數。\
數值越高，線條越平滑。

<b>節目指導助理</b> *布林值*&#x200B;在預覽輸出中會在樣條曲線的起始處顯示一個點，在末端顯示一個箭頭。

<b>顯示厚度包絡</b> *布林值*\
在樣鍵厚度邊緣顯示額外線條。

<b>厚度（px）</b> *浮點*&#x200B;調整預覽輸出中樣條曲線的厚度（像素數）。

<b>背景預覽強度</b> *浮標*\
該值與背景預覽輸入影像相乘。

+++

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant1-Before.jpg" alt="SplineWarp-變體1-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant1-After.jpg" alt="樣條曲速-變體1-之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant2-Before.jpg" alt="SplineWarp-變體2-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant2-After.jpg" alt="SplineWarp-變體2-之後">
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

![節點範例 1](../../../../../../assets/SplineWarp-Demo.gif "節點範例 1")

</td>
<td style="border: 0;" valign="top">



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
