---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/sharpen.html"
breadcrumb-title: ""
description: 使用銳化節點來強化貼圖細節和邊緣，創造清晰且明確的表面細節。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Sharpen
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 磨利
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 2%
---

# 磨利

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![銳利節點圖示 銳化節點圖示](sharpen.resources/sharpen-4.png "")

<b>收錄於：</b> 原子節點

</td>
<td style="border: 0;" valign="top">

## 說明

銳化節點會對輸入執行銳化操作。 它是為影像注入最後清晰度的好用節點。

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="sharpen.resources/sharpen-tooltip.gif" alt="銳利工具提示" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

雖然名稱不同，但數學上與 Photoshop 的 Unsharp Mask 非常相似。 它對像是基色貼圖這類的貼圖效果不錯，但在像法線貼圖和金屬貼圖這類貼圖上應該避免使用。

## 輸入

<b>輸入</b> *彩色/灰階* （原色）\
應該被銳化的影像。

## 參數

<b>強度</b> *浮標*\
設定銳利效果的強度。

<b>穿孔 Alpha</b> *布林值*（當彩色影像連接到輸入</b>時<b>可用）\
判斷影像的 alpha 通道是否應該銳化或保持原狀。

## 範例

![銳化節點 - 範例 1](sharpen.resources/sharpen-ex.png "銳化節點 - 範例 1")
