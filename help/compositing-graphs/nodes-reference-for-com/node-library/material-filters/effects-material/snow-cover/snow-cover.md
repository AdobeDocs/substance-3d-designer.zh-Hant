---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/snow-cover.html"
breadcrumb-title: ''
description: 使用雪覆蓋節點，根據表面角度和位置為材質添加積雪效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Snow Cover
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 雪覆蓋
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 7%

---


# 雪覆蓋

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](snow-cover.resources/snow-cover.png){width="128px"}

<b>收錄於：</b> 《材料濾>效應》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一體化效果，能在整塊材質上增加積雪。 非常依賴高品質的高度圖，例如掃描影像。 結果旨在達到PBR正確。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>面具（選用）</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>頻道</b> | 在這個群組中切換材質通道，例如使用鏡面/光澤貼圖而非金屬/粗糙度時。 |
| <b>新雪</b> <i>0.0 - 1.0</i> | 在高架區域設定積雪量。 結果與融雪參數相關。 |
| <b>融化的雪</b> <i>0.0 - 1.0</i> | 在低窪角落放置融化的雪量。 |
| <b>積累過程</b> <i>0.0 - 1.0</i> | 主要影響高度輸出，決定高度堆疊效應。 |
| <b>平滑度</b> <i>0.0 - 1.0</i> | 場景因積雪而讓高度細節變得平滑。 |
| <b>Flakes 強度</b> <i>0.0 - 1.0</i> | 主要影響法線貼圖，以及片狀細節的強度。 |
