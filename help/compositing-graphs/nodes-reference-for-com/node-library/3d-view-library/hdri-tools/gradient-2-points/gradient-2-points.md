---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/gradient-2-points.html"
breadcrumb-title: ''
description: 使用 Gradient 2 Points 節點在 HDRI 環境中為天空與地面色過渡製作雙點漸層。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Gradient 2 Points
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 梯度2點
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 5%

---


# 梯度2點

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](gradient-2-points.resources/gradient-2-points.png){width="250px"}

<b>收錄於：</b> HDRI 工具> 3D 視圖

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

在兩個使用者選擇的點之間產生兩種顏色的漸層。 結果會根據球面投影進行調整。 類似 [於漸層線性（HDRI），](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/gradient-linear-hdri/gradient-linear-hdri.md)但採用兩個點而非一個。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>點一 立場</b> | 使用者選擇的第一點位置。 在2D視角下有把手。 |
| <b>第一點 顏色</b> <i>（色彩值）</i> | 漸層開始時要上色。 |
| <b>第一點 對比</b> <i>0.0 - 1.0</i> | 第一點遮罩的對比。 |
| <b>點二 立場</b> | 用戶選擇的第二點位置。 在2D視角下有把手。 |
| <b>第二點 顏色</b> <i>（色彩值）</i> | 漸層端的顏色。 |
| <b>第二點 對比</b> <i>0.0 - 1.0</i> | 第二點遮罩的對比。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="gradient-2-points.resources/gradient-ex2.gif" />
        </td>
    </tr>
</table>
