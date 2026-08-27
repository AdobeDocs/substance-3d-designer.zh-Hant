---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/gradient-radial.html"
breadcrumb-title: ''
description: 使用漸層輻射節點來建立從中心點輻射的放射狀漸層，以實現圓形色彩過渡。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Gradient Radial
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 梯度徑向
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 1%

---


# 梯度徑向

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](gradient-radial.resources/gradient-radial.png){width="128px"}

<b>收錄於：</b> 紋理產生器>圖案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

類似於 [Gradient Circular](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-circular/gradient-circular.md)，會以兩個垂直方式自訂的點組成灰階漸變。 躍遷是從 a 到 b，由中心點和半徑定義。 請記住，結果不一定一定是磁磚。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>形狀</b> <i>錐體，半球</i> | 決定過渡曲線。 錐形是一個銳利且線性的過渡，半球則是中央柔和且圓潤的。 |
| <b>第一點</b> | 梯度的中心點。 一開始是白色。 |
| <b>第二點</b> | 半徑點用來判斷梯度範圍。 結尾是黑色。 |
| <b>非平方展開</b> <i>錯誤/真實</i> | 以非平方比率補償擠壓與拉伸。 |
