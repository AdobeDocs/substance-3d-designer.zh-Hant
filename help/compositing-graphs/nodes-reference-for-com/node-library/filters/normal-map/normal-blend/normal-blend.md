---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-blend.html"
breadcrumb-title: ''
description: 使用 Normal Blend 節點將法線貼圖混合在一起，創造表面細節間的平滑過渡。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 一般混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 3%

---


# 一般混合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-blend.resources/normal-blend-01.png){width="128px"}

<b>收錄於：</b> 法線貼圖>濾波器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

法線混合允許你用可選的遮罩將兩個法線貼圖混合在一起，同時確保所有數值保持正規化狀態。 它和原子混合節點[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)差異不大，但增加了法線貼圖的內部計算。

法線混合並非用來合併（疊加）法線貼圖，因為上方貼圖會為下方貼圖增加細節。 為此，改用[普通聯合。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md)

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>普通射門</b> <i>色彩輸入</i> | 前景/頂法線貼圖。 |
| <b>正常血糖</b> <i>色彩輸入</i> | 背景/底部法線貼圖。 |
| <b>面具</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 可以用「使用遮罩」參數切換。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景與背景之間的不透明度融合 |
| <b>使用面具</b> <i>錯誤/真實</i> | 切換面具地圖的使用開關。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-blend.resources/normal-blend-02.gif" /><br><i>（.gif格式引入抖動，例如，應用內結果平滑）</i>
        </td>
    </tr>
</table>
