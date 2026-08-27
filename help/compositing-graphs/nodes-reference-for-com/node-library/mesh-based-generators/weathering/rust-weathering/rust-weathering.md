---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/rust-weathering.html"
breadcrumb-title: ''
description: 使用防鏽老化節點根據網格幾何生成生鏽圖案，創造逼真的金屬腐蝕效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Rust Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 鏽蝕風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 13%

---


# 鏽蝕風化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](rust-weathering.resources/rust-weathering.png){width="128px"}

<b>收錄於：</b> 基於網狀的發電機>風化

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>環境遮蔽</b> <i>灰階輸入</i> | 烘焙貼圖用於內部效果和遮罩。 |
| <b>曲率</b> <i>灰階輸入</i> | 烘焙貼圖用於內部效果和遮罩。 |
| <b>職位</b> <i>色彩輸入</i> |  |
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
| <b>鏽蝕擴散</b> <i>0.0 - 1.0</i> |  |
| <b>擴散平滑度</b> <i>0.0 - 1.0</i> |  |
| <b>Vernish 損害等級</b> <i>0.0 - 1.0</i> |  |
| <b>滴水強度</b> <i>0.0 - 1.0</i> |  |
| <b>滴注樣本量</b> <i>0 - 32</i> |  |
| <b>滴水的順滑度</b> <i>0.0 - 1.0</i> |  |
| <b>混合</b> |  |
| <b>擴散強度</b> <i>0.0 - 1.0</i> | 擴散劑的混合強度。 |
| <b>基色強度</b> <i>0.0 - 1.0</i> | 底色的混合強度。 |
| <b>正常強度</b> <i>0.0 - 32.0</i> | 融合正常的力量。 |
| <b>鏡面強度</b> <i>0.0 - 1.0</i> | 鏡面的融合強度。 |
| <b>光澤度強度</b> <i>0.0 - 1.0</i> | 融合光澤的強度。 |
| <b>粗糙度強度</b> <i>0.0 - 1.0</i> | 融合粗糙度的強度。 |
| <b>金屬強度</b> <i>0.0 - 1.0</i> | 融合金屬的強度。 |
| <b>環境遮蔽強度</b> <i>0.0 - 1.0</i> | 融合環境遮蔽的強度。 |
| <b>高度強度</b> <i>0.0 - 1.0</i> | 融合高度強度。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rust-weathering.resources/rust-ex.gif" />
        </td>
    </tr>
</table>
