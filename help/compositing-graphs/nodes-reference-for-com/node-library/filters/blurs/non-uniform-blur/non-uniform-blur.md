---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/non-uniform-blur.html"
breadcrumb-title: ''
description: 使用非均勻模糊節點，在 X 和 Y 方向施加不同強度的模糊，以達到各向異性效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Non Uniform Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 非均勻模糊
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 8%

---


# 非均勻模糊

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](non-uniform-blur.resources/non-uniform-blur-grayscale.png){width="128px"}

![](non-uniform-blur.resources/non-uniform-blur.png){width="128px"}

<b>收錄於：</b> 模糊>濾鏡

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

執行高品質模糊，強度由輸入遮罩驅動。 選項允許加入各向異性與非對稱性。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>模糊地圖</b> <i>灰階輸入</i> | 用遮罩貼圖來驅動效果強度。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>強度</b> <i>0.0 - 50.0</i> | 用最大強度來塗抹模糊。 被模糊地圖遮蔽，因此這個設定對該地圖的黑色區域沒有影響。 |
| <b>各向異性</b> <i>0.0 - 1.0</i> | 可選擇性地為模糊效果增加方向性。 由角度參數驅動。 |
| <b>不對稱性</b> <i>0.0 - 1.0</i> | 可選擇性地在取樣中加入偏見。 由角度參數驅動。 |
| <b>角度</b> <i>0.0 - 1.0</i> | 角度與方向性及取樣偏差的設定。 |
| <b>取樣</b> <i>1 - 16</i> | 樣品的數量決定品質。 乘以刀刃數量。 |
| <b>刀刃</b> <i>1 - 9</i> | 抽樣區域的數量決定了品質。 乘以樣本數量。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="non-uniform-blur.resources/nonuniform-example.gif" /><br><i>下方範例是由模糊貼圖槽中90度的梯度斜坡驅動。</i>
        </td>
    </tr>
</table>
