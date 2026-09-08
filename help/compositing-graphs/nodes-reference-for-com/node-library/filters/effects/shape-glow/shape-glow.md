---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-glow.html"
breadcrumb-title: ''
description: 使用 Shape Glow 節點為形狀和材質添加發光效果，創造明亮且具氛圍感的視覺效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形狀光芒
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 4%

---


# 形狀光芒

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/shape-glow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-glow.png){width="128px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

在輸入遮罩（灰階版本）或帶有 alpha 通道的形狀（彩色版本）周圍產生柔和的光暈。 與 Glow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/glow/glow.md) 相比[，這種效果更接近其他 2D 影像編輯軟體，因為它是更完整的效果，且控制更多。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>模式</b> <i>柔和、精確</i> | 可在兩種精度模式間切換。 |
| <b>寬度</b> <i>-1.0 - 1.0</i> | 控制光芒的傳播範圍。 |
| <b>擴散</b> <i>0.0 - 1.0</i> | 模糊效果的截止/斷裂讓光暈在形狀附近看起來很實心。 |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 暈染透明度以產生光暈效果。 |
| <b>（影子）顏色</b> <i>（色彩值）</i> | 要在光暈上色。 |
| <b>面具顏色</b> <i>（色彩值）（僅灰階版本）</i> | 純色用於透明度映射輸出。 |
| <b>輸入是預先乘法的</b> <i>錯誤/真實（僅彩色版本）</i> | 輸入是否應假設為預先乘法。 |
| <b>乘法前輸出</b> <i>錯誤/真實</i> | 輸出是否應該預先乘法。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/shapeglow-ex.png" />
        </td>
    </tr>
</table>
