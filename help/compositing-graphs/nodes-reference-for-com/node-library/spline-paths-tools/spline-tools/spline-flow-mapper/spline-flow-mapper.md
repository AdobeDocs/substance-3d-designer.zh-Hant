---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-flow-mapper.html"
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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---


# 樣條流映射器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](spline-flow-mapper.resources/spline-flow-mapper-icon.png "節點圖示")

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

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>樣條座標</b> <i>顏色</i> | 彩色影像RGBA通道中編碼的輸入樣條點座標：<br><b>R</b> - X 位置<br><b>G</b> - Y 位置<br><b>B</b> - 高度<br><b>A</b> - 填充資料：<br>符號：樣條線為閉合（負）或開（正）;<br>- 絕對值：厚度 + 1。 |
| <b>樣條資料</b> <i>顏色</i> | 彩色影像的 RGBA 通道中編碼的輸入樣條線額外資料。<br><b>R</b> - 切線 x<br><b>G</b> - 切線 y<br><b>B</b> - 未使用<br><b>A</b> - 未使用 |
| <b>樣條量</b> <i>整數</i> | 輸入樣條的數量。 |
| <b>衰減曲線</b> <i>灰階</i> | <span id="_Hlk135812146"></span>描述曲線的圖像，利用其第一排像素的值。 當衰減剖面參數設為輸入剖面曲線時，該輸入用來控制沿樣條曲線繪製的流向量資料衰減的梯度斜坡。<br>你可以用 [Curve](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) 節點來撰寫曲線。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>產出</b> <i>顏色</i> | 輸出流程圖以彩色影像編碼。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>分段數量</b> <i>整數</i> | 樣條會被簡化為段，然後向量流資料會穿越它們。 更多段數會使曲線上的流映射更為平滑。 |
| <b>模式</b> <i>整數</i> | 選擇應繪製向量流資料的樣條的方法：<br><br>- <i>繪製樣條表</i>：使用<br>輸入列表中的所有樣條;- <i>繪製單樣條：</i>僅使用<br>指定索引的樣條;- <i>繪製樣條範圍</i>：僅使用該範圍內索引的樣條。 |
| <b>繪製樣條指數</b> <i>整數</i> （當「模式」設定為「繪製單樣條鍵」時可用） | 應繪製向量流資料的樣條曲線指標。 |
| <b>拉取樣條範圍</b> <i>Integer2</i> （當「模式」設定為「繪製樣條範圍」時可用） | 向量流資料應繪製的樣條曲線的索引範圍。 |
| <b>厚度模式</b> <i>整數</i> | 設定繪製向量流資料<br><br>厚度的方法- <i>手動</i>：明確設定厚度並設定任意值;<br>- <i>從樣條</i>曲線：使用樣條厚度。 |
| <b>厚度</b> <i>浮動</i> （當「厚度模式」設為「手動」時可用） | 沿著樣條繪製的向量流資料厚度的任意值。 |
| <b>厚度倍增器</b> <i>浮動</i> （當「厚度模式」設為「From Spline」時可用） | 一個全域乘數，表示沿著樣條曲線繪製的向量流資料厚度，當該厚度由樣條曲線的厚度驅動時。 |
| <b>導演</b> <i>整數</i> | 向量流動相對於樣條的方向。<br><br>- 切線</i>：使用樣條線的切向量;<br>- <i>法線</i>：使用樣條線的法向量;<br>- <i>法線鏡像</i>：使用樣條法線向量的<i>鏡像版本。 |
| <b>翻轉方向</b> <i>布林值</i> | 會反轉樣條方向，這也會影響流向量的方向。 |
| <b>衰減曲線</b> <i>整數</i> | 用於繪製沿樣條<br><br>曲線繪製流向量資料衰減的梯度斜坡：- <i>線性</i>斜坡：使用線性梯度斜坡;<br>- <i>高斯斜坡</i>：使用高斯梯度斜坡<br>- <i>輸入剖面曲線</i>：使用衰減剖面曲線輸入的曲線作為梯度斜坡。 |
| <b>起始衰減</b> <i>布林值</i> | <span id="_Hlk135769398"></span>在樣條線起始處加一個半圓形。 半圓與樣條曲線使用相同的衰減。 |
| <b>衰減結束</b> <i>布林值</i> | 在樣條線末端加上半圓形。 半圓與樣條曲線使用相同的衰減。 |
| <b>樣條高度衰減</b> <i>浮標</i> | 沿著樣條曲線繪製的流向量資料強度會乘以樣條曲線的高度，當高度接近 0 時，繪製資料會逐漸淡入背景的中性色（0.5， 0.5， 0）。 |
| <b>非平方修正</b> <i>布林值</i> | 調整點的位置與厚度，以在非正方形解析度下保留樣條形狀。 這也影響均勻分布。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-flow-mapper.resources/SplineFlowMapper-Variant1-Before.jpg" alt="SplineFlowMapper-variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-flow-mapper.resources/SplineFlowMapper-Variant1-After.jpg" alt="SplineFlowMapper-變體1-After">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![節點範例 2](spline-flow-mapper.resources/SplineFlowMapper-Demo.gif "節點範例 2")

</td>
</tr>
</table>
