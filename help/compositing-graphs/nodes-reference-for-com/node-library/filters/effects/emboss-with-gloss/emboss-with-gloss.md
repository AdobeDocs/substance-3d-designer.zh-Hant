---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/emboss-with-gloss.html"
breadcrumb-title: ''
description: 使用 Emboss With Gloss 節點來製作帶有光澤貼圖的壓印效果，為材質增添層次感和光澤。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Emboss With Gloss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 光澤壓印
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 5%

---


# 光澤壓印

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](emboss-with-gloss.resources/emboss-with-gloss-01.png){width="128px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

在顏色與高度輸入上施加壓紋效果，並加光澤（鏡面反射）。 本質上是根據高度資訊，為影像添加假的烘焙光影。 對於某些需要將光照嵌入貼圖的貼圖風格非常有用。

若有更多選項，請參見 [Uber Emboss](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md)。 還有一個更簡單、原子化的 [Emboss](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md) 版本。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>顏色</b> <i>色彩輸入</i> |  |
| <b>高度</b> <i>灰階輸入</i> |  |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>高光色彩</b> <i>（色彩值）</i> | 高光的顏色。 |
| <b>陰影色</b> <i>（色彩值）</i> | 在陰影或無光區域使用的顏色。 |
| <b>光澤</b> <i>0.0 - 0.5</i> | 光澤度、高光、大小。 |
| <b>強度</b> <i>0.0 - 10.0</i> | 高光的強度。 |
| <b>光線角度</b> <i>0.0 - 1.0</i> | （假）光的入射角。 |
