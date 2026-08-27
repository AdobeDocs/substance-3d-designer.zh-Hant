---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/blur-hq.html"
breadcrumb-title: ''
description: 使用 Blur HQ 節點對材質施加高品質模糊效果，創造流暢且專業的模糊效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Blur HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 模糊總部
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 6%

---


# 模糊總部

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](blur-hq.resources/blur-hq-1.png){width="128px"}

![](blur-hq.resources/blur-hq-grayscale.png){width="128px"}

<b>收錄於：</b> 模糊>濾鏡

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

對結果進行高品質高斯模糊處理。 品質比 [標準的原子盒模糊](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) [好多了。](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)

重要：務必使用適合你輸入的版本！ 用「Blur HQ」來輸入顏色，或用「Blur HQ Grayscale」來輸入灰階。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>強度</b> <i>0.0 - 16.0</i> | 模糊的強度（半徑）。 這個數值越高，模糊的距離就越遠。 |
| <b>品質</b> <i>0 - 1</i> | 增加內部取樣量以提升品質，但計算速度降低。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="blur-hq.resources/hqblur-example.gif" />
        </td>
    </tr>
</table>
