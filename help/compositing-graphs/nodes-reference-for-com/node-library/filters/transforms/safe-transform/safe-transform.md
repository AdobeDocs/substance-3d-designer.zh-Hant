---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
breadcrumb-title: ''
description: 使用安全轉換節點來套用轉換，同時保留貼圖邊界並避免產生瑕疵。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Safe Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 安全變形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 5%

---


# 安全變形

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](safe-transform.resources/safe-transform.png)

![](safe-transform.resources/safe-transform-grayscale.png)

<b>收錄於：</b> 《濾波器>轉換》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

Transform 2D[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) 的平鋪安全版本。它允許你在不破壞平鋪的情況下縮放、旋轉和偏移，也不會因為小幅偏移和旋轉而損失像素細節（銳利度或銳利度）。

當需要最大控制或完美銳利度時，對轉換噪音非常有用。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>瓷磚</b> <i>1 - 16</i> | 透過平鋪來縮減輸入。 |
| <b>偏移模式</b> <i>手動，隨機</i> | 切換到隨機偏移，而不是手動設定的。 |
| <b>偏移</b> <i>0.0 - 1.0</i> | 移動或翻譯結果。 確保像素是被吸附而非插值。 |
| <b>旋轉</b> <i>0.0 - 1.0</i> | 沿著角度旋轉輸入。 |
| <b>磁磚安全旋轉</b> <i>錯誤/真實</i> | 決定旋轉的行為，判斷是否應該吸附到不會模糊像素的安全值。 |
| <b>對稱性</b> <i>無、X、Y、X+Y</i> |  |
| <b>背景色</b> <i>（色彩值）（僅限彩色版本）</i> |  |
| <b>Mipmap 模式</b> <i>自動、手動</i> | 決定 mipmapping 模式。 把這個設定設為手動模式，效果會更銳利。 |
| <b>Mipmap 等級</b> <i>0 - 10</i> | 當 Mipmap 模式設為手動時，你可以選擇不同的 Mipmap。 |
