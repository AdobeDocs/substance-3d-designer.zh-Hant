---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/3d-planar-projection.html"
breadcrumb-title: ''
description: 使用 3D 平面投影節點，將貼圖投影投影到網格表面上，並使用平面投影來做貼圖貼圖。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > 3D Planar Projection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 三維平面投影
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 6%

---


# 三維平面投影

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-planar-projection.resources/3d-planar-gray.png)![](3d-planar-projection.resources/3d-planar.png)

<b>收錄於：</b> 基於網狀的發電機>公用事業

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據烘焙的網格資料（位置與世界法線貼圖）執行平面投影。 允許你在接縫間投影並放置貼紙，獨立於原始 UV 映射。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>位置圖</b> <i>色彩輸入</i> | 烘焙位置圖 |
| <b>世界太空常態</b> <i>色彩輸入</i> | 烘焙世界空間法線貼圖 |
| <b>投影紋理</b> <i>色彩輸入</i> | 輸入貼圖來投影到目標上。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>定位</b> |  |
| <b>專案輸入</b> <i>紫外線位置，世界空間位置</i> | 選擇投影位置設定在 2D/UV 還是 3D/世界空間。 |
| <b>目標紫外線位置</b> | 只有在 UV Position Input 時才會這樣，最佳方式是用來在 Position map 的 2D 視圖中選擇一個點。 |
| <b>目標位置</b> <i>（色彩值）</i> | 只有用世界空間位置輸入，才能定義精確的三維座標。 |
| <b>目標普通</b> <i>（色彩值）</i> |  |
| <b>旋轉</b> <i>0.0 - 1.0</i> | 會沿著投影的貼圖軸旋轉。 |
| <b>規模</b> <i>0.0 - 1.0</i> | 設定投影材質的全域縮放。 |
| <b>規模</b> <i>0.0 - 2.0</i> | 對投影材質進行非均勻縮放。 |
| <b>遮蔽</b> |  |
| <b>最大深度</b> <i>0.0 - 1.0</i> | 控制投影材質的深度，以及何時會被切斷。 |
| <b>深度漸入淡出</b> <i>0.0 - 1.0</i> | 將截止深度的過渡設定為突然或漸弱。 |
| <b>正常閾值</b> <i>-1.0 - 1.0</i> | 將不完全對齊投影法線的表面設定不限。 |
| <b>普通淡出</b> <i>0.0 - 1.0</i> | 將未對齊表面的過渡設定為突然或漸入。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-planar-projection.resources/3d-planar-projection-ex.gif" />
        </td>
    </tr>
</table>
