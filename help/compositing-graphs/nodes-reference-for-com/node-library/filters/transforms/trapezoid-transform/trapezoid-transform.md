---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/trapezoid-transform.html"
breadcrumb-title: ''
description: 使用梯形變換節點對貼圖施加梯形變形，以創造透視修正效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Trapezoid Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 梯形轉換
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 6%

---


# 梯形轉換

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](trapezoid-transform.resources/trapeze-transform.png){width="128px"}

![](trapezoid-transform.resources/trapeze-transform-grayscale.png){width="128px"}

<b>收錄於：</b> 《濾波器>轉換》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

特殊的變換節點，會以透視/梯形扭曲的方式改變輸入。 可以控制上下兩邊的伸展。 數值可以被推到極限以達到更強的效果。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>頂直線</b> <i>0.0 - 1.0</i> | 在頂部設定拉伸或壓碎的量。 |
| <b>底部直線</b> <i>0.0 - 1.0</i> | 在底板設定拉伸或壓擠的量。 |
| <b>背景色</b> <i>（灰階/色彩值）</i> | 如果關閉平鋪，請設定為純色背景色。 |
| <b>抽樣</b> <i>雙線性，最近</i> | 設定取樣品質。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="trapezoid-transform.resources/trapeze-example.gif" />
        </td>
    </tr>
</table>
