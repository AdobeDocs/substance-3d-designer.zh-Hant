---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/reaction-diffusion-fast.html"
breadcrumb-title: ''
description: 使用 Reaction Diffusion Fast 節點，利用快速反應擴散演算法生成程序紋理的有機圖案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Reaction Diffusion Fast
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 反應擴散快處理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 1%

---


# 反應擴散快處理

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![反應擴散節點圖示](../../../../../../assets/reaction-diffusion.png "反應擴散節點圖示")

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

此節點對輸入的灰階影像執行反應擴散效應。

反應擴散是一種物質擴散（擴散）並與其他物質相互作用（反應）的過程。 它是一個數學模型，模擬自然界中在動物皮膚上形成特定圖案時所發生的情況。

這個節點是為了效能優化的，並且在速度上做了一些準確度的取捨。

</td>
</tr>
</table>

## 輸入連接器

<b>輸入</b> *灰階*&#x200B;反應擴散效應應應用於灰階影像。

## 輸出連接器

<b>輸出&#x200B;</b>*灰階 灰階*&#x200B;影像代表對輸入影像施加的反應擴散效應。

## 參數

<b>半徑</b> *漂浮*：效果應該擴散到什麼程度。

<b>對比</b> *浮動*\
調整輸入的對比度，作為一種阻擋。

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![範例1](../../../../../../assets/reactdiff03.png "範例1")

</td>
<td style="border: 0;" valign="top">

![範例2](../../../../../../assets/reactdiff02.png "範例2")

</td>
<td style="border: 0;" valign="top">

![範例3](../../../../../../assets/reactdiff01.gif "範例3")

</td>
</tr>
</table>
