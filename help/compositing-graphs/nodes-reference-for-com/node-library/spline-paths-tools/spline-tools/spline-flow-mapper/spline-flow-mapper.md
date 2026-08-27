---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-flow-mapper.html"
breadcrumb-title: ''
description: 使用 Spline Flow Mapper 節點，沿著樣條路徑創建流暢的紋理圖案，產生有機效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Flow Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 樣條流映射器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---


# 樣條流映射器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/spline-flow-mapper-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

繪製一個流程圖，沿輸入樣條繪製流向量資料。

這讓你可以用樣條鍵控制流向、軌跡、強度和厚度，以及用來將繪製資料淡入中性背景的漸層斜坡。

</td>
</tr>
</table>

>[!IMPORTANT]
>
> 使用非常低厚度值時，結果可能會在樣條包絡外出現不想要的雜訊。 這是已知的問題。

## 輸入連接器

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

<b>衰減曲線</b> *灰階*<span id="_Hlk135812146"></span>&#x200B;描述曲線的影像，使用第一排像素的值。\
當衰減剖面參數設為輸入剖面曲線時，該輸入用來控制沿樣條曲線繪製的流向量資料衰減的梯度斜坡。\
你可以用 [Curve](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) 節點來撰寫曲線。

## 輸出連接器

<b>產出</b> *色彩*&#x200B;輸出流程圖以彩色影像編碼。

## 參數

<b>分段數量</b> *整數*&#x200B;樣條在向量流資料穿越前會被簡化為段。\
更多段數會使曲線上的流映射更為平滑。

<b>模式</b> *整數*&#x200B;選擇繪製向量流資料的樣條的方法：\
*- 繪製樣條表*：輸入列表中的所有樣條線都會被使用;\
*- 繪製單樣條曲線*：僅使用指定索引的樣條曲線;\
*- 繪製樣條範圍*：僅使用包含在指定範圍內的樣條。

<b>繪製樣條指數</b> *整數* （當「模式」設為「繪製單樣條線」時可用）向量流資料應沿著此方向繪製樣條曲線的索引。

<b>拉取樣條範圍</b> *Integer2* （當「模式」設為「繪製樣條範圍」時可用）向量流資料應沿著樣條曲線繪製的索引範圍。

<b>厚度模式</b> *整數*&#x200B;設定繪製向量流資料厚度的方法\
*- 手動*：以任意值明確設定厚度;\
*- 從樣條鍵*：使用樣鍵的厚度。

<b>厚度</b> *浮動* （當「厚度模式」設為「手動」時可用）是沿著樣條曲線繪製的向量流資料厚度的任意值。<b></b>

<b>厚度倍增器</b> *浮點* （當「厚度模式」設為「從樣條曲線」時可用）一個全域乘法器，用於繪製沿樣條曲線繪製的向量流資料厚度，當該厚度由樣條曲線的厚度驅動時。

<b>導演</b> *整數*&#x200B;指向量流相對於樣條的方向。\
*- 切線*：使用樣條線的切向量;\
*- 法線*：使用樣條的法線向量;\
*- 法線鏡像*：使用樣條曲線法線向量的鏡像版本。

<b>翻轉方向</b> *布林值*&#x200B;會反轉樣條曲線的方向，這也會影響流向量的方向。

<b>衰減曲線</b> *整數*&#x200B;用於繪製沿樣條曲線繪製流向量資料衰減的梯度斜坡：\
*- 線性：*&#x200B;使用線性梯度斜坡;\
*- 高斯：*&#x200B;使用高斯梯度斜坡\
*- 輸入曲線*&#x200B;曲線：將提供給衰減曲線曲線輸入的曲線作為梯度斜坡。

<b>起始衰減</b> *布林*<span id="_Hlk135769398"></span>&#x200B;在樣條曲線起始處加一個半圓。 半圓與樣條曲線使用相同的衰減。

<b>衰減結束</b> *布林*&#x200B;在樣條曲線末端加一個半圓。 半圓與樣條曲線使用相同的衰減。

<b>樣條高度衰減</b> *浮點*&#x200B;沿著樣條曲線繪製的流向量資料強度與樣條曲線高度相乘，當高度接近 0 時，繪製資料會逐漸淡入背景的中性色（0.5， 0.5， 0）。

<b>非正方修正&#x200B;</b>*布林*：調整點的位置與厚度，以在非正方形解析度下保留樣條形狀。\
這也影響均勻分布。

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineFlowMapper-Variant1-Before.jpg" alt="SplineFlowMapper-variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineFlowMapper-Variant1-After.jpg" alt="SplineFlowMapper-變體1-After">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![節點範例 2](../../../../../../assets/SplineFlowMapper-Demo.gif "節點範例 2")

</td>
</tr>
</table>
