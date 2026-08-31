---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/season-filter.html"
breadcrumb-title: ''
description: 使用季節過濾節點對材料套用季節效果，創造春、夏、秋、冬季變化。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Season Filter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 季節濾鏡
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 10%

---


# 季節濾鏡

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](season-filter.resources/season-filter-01.png){width="128px"}

<b>收錄於：</b> 《材料濾>效應》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這個節點會加入像是動畫水面關卡、雪、冰和/或苔蘚等效果。

請記住，這是較舊的濾網，並非設計成完全符合PBR標準。 它主要是為了保留舊有或相容性，雖然在某些情況下仍然有用。 較新的PBR正確版本可在《雪覆蓋](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md)》和[《水位》](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md)中找到[。

節點需要一套適當的材質輸入，主要是需要相當詳細的高度圖或法線貼圖。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>面具</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 可以用「遮罩」參數切換。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>頻道</b> | 在這個群組中切換材質通道，例如使用鏡面/光澤貼圖而非金屬/粗糙度時。 |
| <b>進階</b> |  |
| <b>一般格式</b> <i>DirectX、OpenGL</i> | 切換不同的法線貼圖格式（反轉綠色通道）。 |
| <b>面具</b> <i>錯誤/真實</i> | 切換面具地圖的使用開關。 |
| <b>光強</b> <i>0.0 - 1.0</i> | （假）光的強度。 |
| <b>光線角度</b> <i>0.0 - 1.0</i> | （假）光的入射角 |
| <b>影響</b> |  |
| <b>高度或正常影響</b> <i>身高，正常</i> | 選擇哪個輸入映射來驅動效果。 |
| <b>水位</b> <i>0.0 - 1.0</i> | 根據高度/法線資訊來升降水位。 |
| <b>水資源詳情</b> <i>0.0 - 1.0</i> | 設定水中細節的數量。 |
| <b>折射</b> <i>0.0 - 1.0</i> | 在效果中設定假折射的量。 |
| <b>反思</b> <i>0.0 - 1.0</i> | 在效果中設定了假反射的量。 |
| <b>反射距離</b> <i>0.0 - 1.0</i> | 控制反射、視覺效果。 |
| <b>反射角</b> <i>0.0 - 1.0</i> | 控制反射、視覺效果。 |
| <b>流向</b> <i>0.0 - 1.0</i> | 控制動畫流程（使用 Substance Player 來視覺化）。 |
| <b>冰</b> <i>0.0 - 1.0</i> | 用來設定水的結冰程度。 |
| <b>冰面細節</b> <i>0.0 - 1.0</i> | 冰面上設定了細節的數量。 |
| <b>雪</b> <i>0.0 - 1.0</i> | 設定積雪覆蓋量。 |
| <b>苔蘚</b> <i>0.0 - 1.0</i> | 設定苔蘚覆蓋面積。 |
| <b>苔蘚秤</b> <i>1 - 4</i> | 設定生成苔蘚紋理的縮放。 |
| <b>苔蘚色</b> <i>（色彩值）</i> | 設定苔蘚色。 |
| <b>水彩</b> <i>（色彩值）</i> | 設定水的顏色，包括透明度/透明度。 |
| <b>混合</b> |  |
| <b>擴散強度</b> <i>0.0 - 1.0</i> | 擴散劑的混合強度。 |
| <b>基色強度</b> <i>0.0 - 1.0</i> | 底色的混合強度。 |
| <b>正常強度</b> <i>0.0 - 1.0</i> | 融合正常的力量。 |
| <b>鏡面強度</b> <i>0.0 - 1.0</i> | 鏡面的融合強度。 |
| <b>光澤度強度</b> <i>0.0 - 1.0</i> | 融合光澤的強度。 |
| <b>粗糙度強度</b> <i>0.0 - 1.0</i> | 融合粗糙度的強度。 |
| <b>環境遮蔽強度</b> <i>0.0 - 1.0</i> | 融合環境遮蔽的強度。 |
| <b>高度強度</b> <i>0.0 - 1.0</i> | 融合高度強度。 |
