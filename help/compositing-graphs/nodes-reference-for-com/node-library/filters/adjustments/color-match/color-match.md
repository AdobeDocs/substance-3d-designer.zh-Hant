---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-match.html"
breadcrumb-title: ''
description: 使用色彩匹配節點來匹配材質間的顏色，以創造一致的色彩調色盤並協調材質。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color Match
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 顏色配對
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 0%

---


# 顏色配對

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/color-match-3.png){width="128px"}

<b>收錄於：</b> 篩選>調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

嘗試將定義 *的來源色彩* 範圍與 *目標色彩* 範圍匹配，並支援輸入槽來定義來源與目標。

較簡單的版本請參見 [「替換色彩範圍](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color-range/replace-color-range.md) 」或 [「替換顏色](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color/replace-color.md)」。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入</b> <i>色彩輸入</i> | 主要輸入需修改以達成結果。 |
| <b>來源顏色</b> <i>色彩輸入</i> | 輸入槽用於來源色彩，僅在「來源色彩模式」設為 *輸入*&#x200B;時使用。 |
| <b>目標顏色</b> <i>色彩輸入</i> | 目標顏色輸入槽，僅在「目標色彩模式」設為 *輸入*&#x200B;時使用。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>來源色彩模式</b> <i>平均值、參數、輸入</i> | 設定來源色彩是透過平均輸入影像、設定參數，或使用輸入槽來定義。 |
| <b>來源顏色</b> <i>（色彩值）</i> | 若將來源色彩模式設為 *參數*，該參數決定來源顏色。 |
| <b>目標色彩模式</b> <i>參數，影像輸入</i> | 設定來源色彩是透過平均輸入影像、設定參數，或使用輸入槽來定義。 |
| <b>目標顏色</b> <i>（色彩值）</i> | 若目標色彩模式設為 *參數*，該參數決定目標顏色。 |
| <b>自訂色彩變化</b> <i>錯誤/真實</i> | 可增加顏色變化。 |
| <b>顏色變化</b> | 若啟用，則可設定色相、色度或亮度變化。 |
| <b>使用面具</b> <i>錯誤/真實</i> | 根據下方遮罩模式，切換遮罩輸入或輸出的使用。 |
| <b>遮罩模式</b> <i>參數、輸入</i> | 參數模式會輸出一個遮罩，詳細說明顏色的變化。 輸入模式讓遮罩能控制色彩匹配效果的強度。 |
| <b>面具</b> | 輸出一個遮罩，顯示色彩匹配效果的精確位置，並附加平滑與模糊遮罩的控制。 |
