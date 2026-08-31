---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter.html"
breadcrumb-title: ''
description: 使用濺射節點將形狀散布到貼圖中，創造隨機圖案和有機貼圖細節。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 濺射
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 9%

---


# 濺射

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](splatter.resources/splatter-01.png)

![](splatter.resources/splatter-02.png)

<b>收錄於：</b> 紋理產生器>圖案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

Splatter 是一種設計用於隨機放置地圖輸入的圖案產生器。 它有許多幾何圖案放置的控制，使用比圖塊產生器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)更[簡單。後者也能達到類似的效果，但複雜得多。

Splatter 很適合快速壓印某些形狀，不需要太多調整。

請記住，預設的 Splatter 參數看起來一點也不隨機：你需要調整其中幾個參數才能達到隨機化（主要是 Disorder 參數）。 另外要記得，Splatter 需要地圖輸入才能運作。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>圖案尺寸寬度</b> <i>0.0 - 1000.0</i> | X 軸上可使用圖案數量。 |
| <b>圖案尺寸 高度</b> <i>0.0 - 1000.0</i> | Y軸上可用的圖案數量。 |
| <b>旋轉</b> <i>-360.0 - 360.0</i> | 會讓每個圖案輪流固定數量。 |
| <b>旋轉變化</b> <i>0.0 - 360.0</i> | 為每個獨立形狀引入隨機旋轉。 |
| <b>Zoom</b> <i>100.0 - 10000.0</i> | 放大最終成果。 請記得這會破壞磁磚！ |
| <b>增益</b> <i>0.0 - 10.0</i> | 調整每個圖案的混合增益。 這樣會讓他們更突出。 |
| <b>潘X</b> <i>-100.0 - 100.0</i> | 整個結果在 X 軸上平移。 |
| <b>泛Y公司</b> <i>-100.0 - 100.0</i> | 整個 Pan 結果在 Y 軸上。 |
| <b>混亂</b> <i>0.0 - 100.0</i> | 會隨機變換形狀。 |
| <b>起跑格號</b> <i>0 - 8</i> | 跳過不同格子大小以調整結果比例。 能維持磁磚。 |
| <b>無序角度</b> <i>0.0 - 360.0</i> | 控制無序移動的角度。 |
| <b>隨機無序</b> <i>錯誤/真實</i> | 隨機化了混亂的角度，增加了更多混亂。 |
| <b>圖案尺寸</b> <i>5 - 12</i> |  |
| <b>尺寸變化</b> <i>0.0 - 100.0</i> | 為每個形狀引入隨機縮放。 |
| <b>影像輸入過濾（僅限引擎 > v4）</b> <i>雙線性 + 多元映射、雙線性、最近</i> | 輸入影像該套用哪種濾波。 |
| <b>輸出電平最小值</b> <i>0.0 - 1.0</i> | 我們的最低調整水平。 |
| <b>輸出電平最大值</b> <i>0.0 - 1.0</i> | 我們的最大水位調整。 |
| <b>背景色</b> <i>（灰階）</i> | 設定純色背景色。 |
| <b>亮度變化</b> <i>0.0 - 1.0（僅灰階版本）</i> | 引入亮度變化。 |
| <b>顏色變化</b> <i>0.0 - 1.0（僅限彩色版本）</i> | 引入色彩變化。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="splatter.resources/splatter-03.gif" />
        </td>
    </tr>
</table>
