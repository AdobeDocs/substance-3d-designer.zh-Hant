---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/glow.html"
breadcrumb-title: ''
description: 使用Glow節點為材質添加發光效果，創造發光且發光的材質外觀。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 發光
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 5%

---


# 發光

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](glow.resources/glow-greyscale.png){width="128px"}

![](glow.resources/glow-3.png){width="128px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

能產生類似「外層光暈」的效果，類似其他熱門影像編輯軟體。 基本上是在輸入周圍加上漸變的漸層輪廓。

請注意，這並非針對帶有 Alpha 通道的影像設計，正如你所預期的。 即使是彩色版本，也只期望輸入二進位黑白遮罩;它只允許使用彩色螢光。 如果你想要能處理透明影像的版本，請參考 [Shape Glow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-glow/shape-glow.md)。

重要：務必使用適合你輸入的版本！ 用「Glow」來表示顏色輸入，或用「Glow Grayscale」來表示灰階輸入。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>光澤量</b> <i>0.0 - 1.0</i> | 全域不透明度用於發光效果。 |
| <b>清算金額</b> <i>0.0 - 1.0</i> | Treshold 是用來切斷發光效果的。 適合半透明區域。 |
| <b>發光尺寸</b> <i>0.0 - 20.0</i> | 控制發光效果的範圍。 |
| <b>螢光色彩</b> <i>（色彩值）（僅限彩色版本）</i> | 設定發光效果的顏色。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="glow.resources/glow-ex.png" />
        </td>
    </tr>
</table>
