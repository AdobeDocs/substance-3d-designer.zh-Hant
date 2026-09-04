---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/min-max.html"
breadcrumb-title: ''
description: 使用最小最大節點（Min Max）來夾住貼圖值在最小與最大閾值之間，以控制值範圍。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Min Max
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 極限
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 2%

---


# 極限

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](min-max.resources/min-max-01.png){width="200px"}

<b>收錄於：</b> 篩選>調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

最小極大值會找出灰階輸入中最亮與最暗的值，並返回為 [值](../../../../../values-compositing-graphs/values-in-substance-compositing-graphs.md)。 它設計成一個更細緻、手動的[自動等級](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md)替代方案，透過暴露 Levels[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)節點的 Value Inputs，並將最小最大值的值輸入輸入到它。

要用這個節點搭配 Levels，你至少應該知道如何使用 [「Expose Parameter」下拉選單](../../../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)，以及 [「Value」輸入標籤](../../../../../values-compositing-graphs/values-in-substance-compositing-graphs.md)。

</td>
</tr>
</table>

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="min-max.resources/min-max-02.png" />
        </td>
    </tr>
</table>
