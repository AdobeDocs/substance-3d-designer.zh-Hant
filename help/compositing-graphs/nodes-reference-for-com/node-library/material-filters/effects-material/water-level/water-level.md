---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/water-level.html"
breadcrumb-title: ''
description: 利用水位節點根據水位高度混合材質，創造逼真的水面效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Water Level
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 水位
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 8%

---


# 水位

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](water-level.resources/water-level-01.png){width="128px"}

<b>收錄於：</b> 《材料濾>效應》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一體化效果，會為完整材質輸入增加水位。 輸入材質必須有良好且高品質的高度圖，效果才會有效。 結果是 PBR 正確。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>面具</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>頻道</b> | 在這個群組中切換材質通道，例如使用鏡面/光澤貼圖而非金屬/粗糙度時。 |
| <b>水位</b> <i>0.0 - 1.0</i> | 主控室用來升降水位。 |
| <b>水之黑暗</b> <i>0.0 - 1.0</i> | 能讓水的整體「透明度」下降。 |
| <b>邊緣濕度</b> <i>0.0 - 1.0</i> | 決定水邊應該有多少濕潤的外觀。 |
| <b>邊 濕度 距離</b> <i>0.0 - 1.0</i> | 這樣可以決定濕邊能延伸到什麼程度。 |
| <b>深度模糊量</b> <i>0.0 - 1.0</i> | 根據水下深度設定模糊的程度。 修改模糊半徑。 |
| <b>深度模糊不透明度</b> <i>0.0 - 1.0</i> | 它決定模糊的深度融合程度，可以用來降低模糊效果。 |
| <b>污泥顏色</b> <i>（色彩值）</i> | 設定污泥效果的顏色。 |
| <b>污泥深度</b> <i>0.0 - 1.0</i> | 設定污泥開始出現的深度，相對於水位。 |
| <b>污泥不透明度</b> <i>0.0 - 1.0</i> | 設定污泥效應的全域不透明度。 |
| <b>霜凍</b> <i>0.0 - 1.0</i> | 設定霜凍的量。 從外緣開始出現，並向內移動。 |
| <b>霜凍強度</b> <i>0.0 - 1.0</i> | 設定霜凍強度，控制效果的「不透明度」。 |
| <b>霜裂</b> <i>0.0 - 1.0</i> | 它會設定從冷凍到液體過渡時的裂縫數量。 |
| <b>霜凍標準格式</b> <i>DirectX/OpenGL</i> | 開關 霜法線貼圖效果 綠色通道。 |
