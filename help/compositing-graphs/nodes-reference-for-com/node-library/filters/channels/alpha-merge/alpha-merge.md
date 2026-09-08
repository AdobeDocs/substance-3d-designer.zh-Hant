---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/channels/alpha-merge.html"
breadcrumb-title: ''
description: 使用 Alpha Merge 節點將 RGB 材質與 alpha 通道結合，以建立 RGBA 材質。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Channels > Alpha Merge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Alpha 合併
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 1%

---


# Alpha 合併

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/rgb-a-merge.png)

<b>收錄於：</b> 濾波器>通道

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

在沒有 alpha 通道的輸入上加入一個 alpha 通道。 不要和 [RGBA 合併](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md)搞混，這個節點簡單很多，只會增加 alpha！

簡單但方便的節點，適合你想遮蔽某些東西，或是結果需要 alpha 時使用。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>RGB</b> <i>色彩輸入</i> | 無 alpha 的彩色影像 |
| <b>A</b> <i>灰階輸入</i> | 灰階影像將作為結果的 alpha。 |
