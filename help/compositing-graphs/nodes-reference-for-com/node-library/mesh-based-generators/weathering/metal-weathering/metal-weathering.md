---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/metal-weathering.html"
breadcrumb-title: ''
description: 利用金屬風化節點，根據網格幾何體為金屬材料添加逼真的生鏽和腐蝕效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Metal Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 金屬風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 14%

---


# 金屬風化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](metal-weathering.resources/metal-weathering.png){width="128px"}

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
| <b>正常的 WS</b> <i>色彩輸入</i> | 烘焙世界空間法線貼圖用於內部效果與遮罩。 |
| <b>環境遮蔽</b> <i>灰階輸入</i> | 烘焙貼圖用於內部效果和遮罩。 |
| <b>面具</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 可以用「遮罩」參數切換。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>頻道</b> | 在這個群組中切換材質通道，例如使用鏡面/光澤貼圖而非金屬/粗糙度時。 |
| <b>進階</b> |  |
| <b>一般格式</b> <i>Direct X，開放GL</i> | 切換不同的法線貼圖格式（反轉綠色通道）。 |
| <b>面具</b> <i>錯誤/真實</i> | 切換面具地圖的使用開關。 |
| <b>影響</b> |  |
| <b>塵埃</b> <i>0.0 - 1.0</i> |  |
| <b>骯髒</b> <i>0.0 - 1.0</i> |  |
| <b>邊緣磨損</b> <i>0.0 - 1.0</i> |  |
| <b>油漆剝落</b> <i>0.0 - 1.0</i> |  |
| <b>生鏽</b> <i>0.0 - 1.0</i> |  |
| <b>鏽蝕剝落</b> <i>0.0 - 1.0</i> |  |
| <b>銹綠</b> <i>銹，綠斑</i> |  |
| <b>油漆裂縫量表</b> <i>1.0 - 16.0</i> |  |
| <b>油漆裂縫 變形強度</b> <i>0.0 - 1.0</i> |  |
| <b>銳利邊緣刮痕 鱗片</b> <i>1.0 - 32.0</i> |  |
| <b>銳利邊緣刮痕 扭曲強度</b> <i>0.0 - 1.0</i> |  |
| <b>原金屬色</b> <i>（色彩值）</i> |  |
| <b>原金屬鏡面色彩</b> <i>（色彩值）</i> |  |
| <b>原始金屬光澤價值</b> <i>（灰階）</i> |  |
| <b>原金屬粗糙度值</b> <i>（灰階）</i> |  |
| <b>混合</b> |  |
| <b>擴散強度</b> <i>0.0 - 1.0</i> | 擴散劑的混合強度。 |
| <b>基色強度</b> <i>0.0 - 1.0</i> | 底色的混合強度。 |
| <b>正常強度</b> <i>0.0 - 64.0</i> | 融合正常的力量。 |
| <b>鏡面強度</b> <i>0.0 - 1.0</i> | 鏡面的融合強度。 |
| <b>光澤度強度</b> <i>0.0 - 1.0</i> | 融合光澤的強度。 |
| <b>粗糙度強度</b> <i>0.0 - 1.0</i> | 融合粗糙度的強度。 |
| <b>金屬強度</b> <i>0.0 - 1.0</i> | 融合金屬的強度。 |
| <b>環境遮蔽強度</b> <i>0.0 - 1.0</i> | 融合環境遮蔽的強度。 |
| <b>高度強度</b> <i>0.0 - 1.0</i> | 融合高度強度。 |
