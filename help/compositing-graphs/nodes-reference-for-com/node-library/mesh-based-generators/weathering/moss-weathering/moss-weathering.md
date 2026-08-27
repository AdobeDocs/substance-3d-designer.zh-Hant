---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/moss-weathering.html"
breadcrumb-title: ''
description: 使用 Moss Weathering 節點，根據網格曲率和位置為材質添加苔蘚生長模式。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Moss Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 苔蘚風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 7%

---


# 苔蘚風化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](moss-weathering.resources/moss-weathering.png){width="128px"}

<b>收錄於：</b> 基於網狀的發電機>風化

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這是一種全材質效果，能同時在多個聲道上運作。 它會產生過度生長的苔蘚效應，只有一個控制點來控制繁殖。

這個效果最適合搭配烘焙的世界空間位置貼圖和額外的高度貼圖。 雖然這不是絕對要求，但讓效果的擺放更具說服力。

使用完整素材時，務必正確理解 [連結建立模式](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes) 。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>職位</b> <i>色彩輸入</i> | 烘焙世界空間位置。 |
| <b>高度</b> <i>灰階輸入</i> | 額外高度圖輸入。 |
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
| <b>苔蘚繁殖</b> <i>0.0 - 1.0</i> | 設定苔蘚的擴散範圍。 生長分階段，從輕微覆蓋到厚實、深色的苔蘚。 |
| <b>混合</b> |  |
| <b>擴散強度</b> <i>0.0 - 1.0</i> | 擴散劑的混合強度。 |
| <b>基色強度</b> <i>0.0 - 1.0</i> | 底色的混合強度。 |
| <b>正常強度</b> <i>0.0 - 1.0</i> | 融合正常的力量。 |
| <b>鏡面強度</b> <i>0.0 - 1.0</i> | 鏡面的融合強度。 |
| <b>光澤度強度</b> <i>0.0 - 1.0</i> | 融合光澤的強度。 |
| <b>粗糙度強度</b> <i>0.0 - 1.0</i> | 融合粗糙度的強度。 |
| <b>環境遮蔽強度</b> <i>0.0 - 1.0</i> | 融合環境遮蔽的強度。 |
| <b>高度強度</b> <i>0.0 - 1.0</i> | 融合高度強度。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="moss-weathering.resources/moss-ex.gif" />
        </td>
    </tr>
</table>
