---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/hdr-merge.html"
breadcrumb-title: ''
description: 使用 HDR 合併節點將多張 HDR 影像合併成單一全景圖，以建立複合環境貼圖。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > HDR Merge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: HDR 合併
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 8%

---


# HDR 合併

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](hdr-merge.resources/hdr-merge.png){width="200px"}

<b>收錄於：</b> HDRI 工具> 3D 視圖

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

將多張照片曝光合併，創造高動態範圍影像。 第一個輸入是曝光最不足的影像。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入1-16</b> <i>色彩輸入</i> | 輸入影像。 可用數量取決於參數。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>輸入</b> <i>2 - 16</i> | 設定可用輸入的數量。 |
| <b>暴露 Delta（EV）</b> <i>0.0 - 4.0</i> | 設定曝光差異以解讀不同影像。 |
| <b>懷特波因特</b> <i>0.0 - 13.0</i> | 設定白點來調整最終結果。 |
