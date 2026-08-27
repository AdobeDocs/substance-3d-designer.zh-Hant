---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-grayscale.html"
breadcrumb-title: ''
description: 使用 Spline Bridge Mapper 灰階節點，將兩個帶有灰階貼圖的樣條紋架接。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 樣條橋映射機灰階
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 1%

---


# 樣條橋映射機灰階

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](spline-bridge-mapper-grayscale.resources/spline-bridge-mapper-grayscale-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

將灰階影像映射到輸入樣條線清單中，使影像依序遍歷樣條線。

</td>
</tr>
</table>

>[!TIP]
>
> 映射從列表中第一個樣條線到最後一個樣條線，並嚴格依照列表中這些樣條線的順序遍歷中間樣條線。
> 
> 因此，你應該事先注意樣條的附加順序。

>[!NOTE]
>
> 另 [見樣條橋映射器顏色](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-col/spline-bridge-mapper-color.md)。

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>樣條座標</b> <i>顏色</i> | 彩色影像RGBA通道中編碼的輸入樣條點座標：<br><b>R</b> - X 位置<br><b>G</b> - Y 位置<br><b>B</b> - 高度<br><b>A</b> - 填充資料：<br>符號：樣條線為閉合（負）或開（正）;<br>- 絕對值：厚度 + 1。 |
| <b>樣條資料</b> <i>顏色</i> | 彩色影像的 RGBA 通道中編碼的輸入樣條線額外資料。<br><b>R</b> - 切線 x<br><b>G</b> - 切線 y<br><b>B</b> - 未使用<br><b>A</b> - 未使用 |
| <b>樣條量</b> <i>整數</i> | 輸入樣條的數量。 |
| <b>色彩地圖</b> <i>灰階</i> | 應該映射到輸入樣條上的輸入灰階影像。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>顏色</b> <i>灰階</i> | 這是將輸入的彩色影像映射到樣條曲線上的灰階影像。 |
| <b>高度</b> <i>灰階</i> | 樣條曲線的高度映射成灰階影像。 |
| <b>紫外線</b> <i>顏色</i> | 映射影像的 UV（即座標），編碼在彩色影像的紅色（U）和綠色（V）通道中。 |
| <b>面具</b> <i>灰階</i> | 一個樣條曲線映射的遮罩。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>分段數量</b> <i>整數</i> | 樣條會被簡化成段，然後影像座標會穿越它們。 線段越多，曲線上的映射就越平滑。 |
| <b>減少紫外線拉伸</b> <i>布林值</i> | 調整從一個樣條線插值到下一個樣條座標的方法，以減少樣條間距離不均時的拉伸。 |
| <b>紫外線尺度</b> <i>Float2</i> | 調整影像座標的比例。 數值越高，圖塊越密集。 |
| <b>紫外線旋轉</b> <i>浮標</i> | 會將影像座標繞中心旋轉。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-bridge-mapper-grayscale.resources/SplineBridgeMapperGrayscale-Variant1-Before.jpg" alt="SplineBridgeMapper灰階變體1-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-bridge-mapper-grayscale.resources/SplineBridgeMapperGrayscale-Variant1-After.jpg" alt="SplineBridgeMapper灰階變體1-之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![節點範例 2](spline-bridge-mapper-grayscale.resources/SplineBridgeMapper-Demo.gif "節點範例 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![節點範例 1](spline-bridge-mapper-grayscale.resources/SplineBridgeMapperGrayscale-Variant1-After1.jpg "節點範例 1")

</td>
<td style="border: 0;" valign="top">

![節點範例 2](spline-bridge-mapper-grayscale.resources/SplineBridgeMapperGrayscale-Graph.jpg "節點範例 2")

</td>
</tr>
</table>
