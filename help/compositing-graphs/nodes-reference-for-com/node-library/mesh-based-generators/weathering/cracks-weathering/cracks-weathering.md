---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/cracks-weathering.html"
breadcrumb-title: ''
description: 使用裂縫風化節點，根據網格曲率和應力點為材料添加裂紋圖案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Cracks Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 裂縫風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6eb38d6ccaadda1d070e4e0b67311312adb7d082
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 3%

---


# 裂縫風化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/cracks-weathering.png){width="128px"}

<b>收錄於：</b> 基於網狀的發電機>風化

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這是一種全材質效果，能同時在多個聲道上運作。 它增加了隨機裂紋模式，並可控制裂紋的擴散與深度。

使用完整素材時，務必正確理解 [連結建立模式](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) 。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>曲率</b> <i>灰階輸入</i> | 烘焙或生成的貼圖用於內部特效和遮罩。 |
| <b>高度</b> <i>灰階輸入</i> | 烘焙或生成的貼圖用於內部特效和遮罩。 |
| <b>面具</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 可以用「遮罩」參數切換。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>頻道</b> | 在這個群組中切換材質通道，例如使用鏡面/光澤貼圖而非金屬/粗糙度時。 |
| <b>進階</b> |  |
| <b>一般格式</b> <i>DirectX、OpenGL</i> | 切換不同的法線貼圖格式（反轉綠色通道）。 |
| <b>面具</b> <i>錯誤/真實</i> | 切換面具地圖的使用開關。 |
| <b>影響</b> |  |
| <b>裂縫傳播</b> <i>0.0 - 1.0</i> | 裂縫應該擴散多遠。 這是這個效果的主要控制。 |
| <b>裂縫深度</b> <i>0.0 - 1.0</i> | 裂縫效應的深度。 這主要影響高度，並略微影響視角厚度。 |
| <b>混合</b> | 控制效果與每個聲道融合的強度。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/cracks-ex.gif" />
        </td>
    </tr>
</table>
