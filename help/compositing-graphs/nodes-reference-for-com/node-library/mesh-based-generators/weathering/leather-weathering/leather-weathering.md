---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/leather-weathering.html"
breadcrumb-title: ''
description: 利用皮革老化節點，根據網狀曲線為皮革材料添加磨損模式和老化效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Leather Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 皮革風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 9%

---


# 皮革風化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](leather-weathering.resources/leather-weathering.png){width="128px"}

<b>收錄於：</b> 基於網狀的發電機>風化

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這是一種全材質效果，能同時在多個聲道上運作。 它增加了隨機的皮革磨損效果，並能控制老化和髒污程度。 它與布料風化[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/weathering/fabric-weathering/fabric-weathering.md)類似，但專為皮革調校。<br>除非你插入了正式烘焙的 AO 和世界空間法線貼圖，否則這個效果效果不太好，因為這需要這些來充分計算和產生所有東西。

使用完整素材時，務必充分理解 [連結創建模式](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes) 。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>環境遮蔽</b> <i>灰階輸入</i> | 烘焙貼圖用於內部效果和遮罩。 |
| <b>正常會是空間</b> <i>色彩輸入</i> |  |
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
| <b>塵埃</b> <i>0.0 - 1.0</i> | 根據世界空間法線貼圖中面向向上的區域，融合出較暗的塵埃效果。 |
| <b>骯髒</b> <i>0.0 - 1.0</i> | 會融合一個全域的髒污/暈染效果，主要是基於 AO 中遮蔽（暗）區域。 |
| <b>邊緣磨損</b> <i>0.0 - 1.0</i> | 根據材質法線，為邊緣加入銳利/強化效果。 |
| <b>使用過</b> <i>0.0 - 1.0</i> | 融合了全球磨損皮革的風格。 |
| <b>年代</b> <i>0.0 - 1.0</i> | 在AO的摺痕中融合出磨損皮革的感覺。 擺放位置很大程度上受年齡限制影響。 |
| <b>時代 Threshlod</b> <i>0.0 - 1.0</i> | 設定年齡效果的外觀限制。 |
| <b>裂紋量表</b> <i>1.0 - 16.0</i> | 設定二手皮革磨損深度，並依舊時間效果。 |
| <b>裂縫扭曲強度</b> <i>0.0 - 1.0</i> | 設定二手皮革的磨損強度和老化效果。 |
| <b>銳利邊緣刮痕 鱗片</b> <i>1.0 - 32.0</i> |  |
| <b>銳利邊緣刮痕 扭曲強度</b> <i>0.0 - 1.0</i> |  |
| <b>二手皮革脫飽和</b> <i>0.0 - 1.0</i> | 設定了 Age 和 Used Effects 中磨損皮革外觀的飽和度。 |
| <b>使用皮革亮度</b> <i>0.0 - 1.0</i> | 設定了 Age 和 Used Effects 中磨損皮革的明亮感。 |
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
            <img src="leather-weathering.resources/leather-ex.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="leather-weathering.resources/leather-ex2.png" />
        </td>
    </tr>
</table>
