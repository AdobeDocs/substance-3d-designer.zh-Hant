---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/tri-planar.html"
breadcrumb-title: ''
description: 使用三平面節點從三個正交平面投影貼圖，實現複雜幾何體的無縫貼圖。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Tri Planar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 三平面
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 6%

---


# 三平面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tri-planar.resources/tri-planar-01.png){width="128px"}

![](tri-planar.resources/tri-planar-02.png){width="128px"}

<b>收錄於：</b> 基於網狀的發電機>公用事業

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這個進階節點根據烘焙的「世界空間法線位置」資料，執行三面投影映射。 這表示它基本上會完全將 UV 座標轉換成（大致上）無接縫的貼圖，基於網格本身。

這是避免接縫的好方法，不用每次都重新烘烤（烘焙師也可以做到類似效果）。 缺點是這個節點相當重，因此速度不快。

請記得烘焙必須精準度高：8位元烘焙效果不會很好。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>職位</b> <i>色彩輸入</i> | 烘焙位置地圖。 理想狀況是 16 位元或更高的精度。 |
| <b>世界太空常態</b> <i>色彩輸入</i> | 烘焙世界空間法線貼圖，理想上是 16 位元或更高的精度。 |
| <b>輸入 X</b> <i>色彩輸入（灰階輸入）</i> | 輸入映射，透過三平面投影將 UV 重新映射到世界空間。 當影像輸入設為 1 時，用於所有軸;若設定為 3，則用於 X 軸。 |
| <b>輸入 Y</b> <i>色彩輸入（灰階輸入）</i> | 只有當影像輸入設定為 3 時才會被設定。 輸入映射，將 UV 重新映射到 Y 軸的世界空間。 |
| <b>輸入Z</b> <i>色彩輸入（灰階輸入）</i> | 只有當影像輸入設定為 3 時才會被設定。 輸入映射，將 UV 重新映射到 Z 軸的世界空間。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>投影</b> <i>全軸，只有X軸，只有Y軸，只有Z軸</i> | 設定要融合的軸線。 |
| <b>影像輸入</b> <i>1 個輸入，3 個輸入</i> | 設定是用一張地圖代表所有軸線，還是每個軸線用一張特定的地圖。 |
| <b>混合模式</b> <i>線性、進階</i> | 提升準確度與精確度。 |
| <b>混合對比</b> <i>0.001 - 1.0</i> | 過渡對比，在平滑或強烈過渡間融合。 |
| <b>正規化因子</b> <i>0.0 - 1.0</i> | 透過恢復混合區域的對比度損失，改善投影的混合效果。 |
| <b>貼圖平鋪</b> <i>0.0 - 10.0</i> | 輸入貼圖平鋪的次數。 |
| <b>全球旋轉</b> <i>0.0 - 1.0</i> | 所有軸的全域旋轉。 |
| <b>修正鏡像投影問題</b> <i>錯誤/真實</i> | 設定如何處理鏡像投影。 |
| <b>旋轉X階段</b> <i>0.0 - 1.0</i> | 在投影的 X 軸上進行個別旋轉。 |
| <b>旋轉 Y</b> <i>0.0 - 1.0</i> | 個別旋轉，沿著投影的Y軸。 |
| <b>旋轉Z</b> <i>0.0 - 1.0</i> | 在投影 Z 軸上進行個別旋轉。 |
| <b>偏移量 X</b> <i>0.0 - 1.0</i> | 偏移量為投影 X 軸。 |
| <b>隨機偏移 X</b> <i>0.0 - 1.0</i> | 允許X軸偏移的隨機化。 |
| <b>偏移 Y</b> <i>0.0 - 1.0</i> | 偏移於投影的Y軸。 |
| <b>隨機偏移 Y</b> <i>0.0 - 1.0</i> | 允許Y軸偏移的隨機化。 |
| <b>偏移Z</b> <i>0.0 - 1.0</i> | 偏移量為投影 Z 軸。 |
| <b>隨機偏移 Z</b> <i>0.0 - 1.0</i> | 允許 Z 軸偏移的隨機化。 |
